# 03 — Order intent, CLOID, nonce, and order lifecycle

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Immutable identity chain

```text
OpportunityId -> RiskDecisionId -> ExecutionId -> LegId
-> IntentId -> CLOID -> optional exchange OID -> FillIds -> PnL
```

Each identifier is a distinct type. `OrderIntent` fields are exactly those frozen in SRC-005: `intent_id`, `execution_id`, `leg_id`, `market_id`, `side`, `price_ticks`, `size_lots`, `tif`, `cloid`, optional `nonce`, `risk_decision_id`, `created_at`. `SignedOrderIntent` contains `intent`, `nonce`, `signature`, `signed_at`. No new field is implied here.

## CLOID and no-blind-retry protocol

One logical intent gets one stable CLOID. On response loss or timeout:

1. record possible transmission (`SENT`/`PENDING_RESOLUTION`);
2. keep all affected reservations locked;
3. query by CLOID/OID plus open orders/fills;
4. reduce evidence idempotently;
5. reconcile balance/inventory;
6. only after terminal truth may a genuinely new intent be planned.

Resubmitting an economically duplicate order with a new identity before step 6 is forbidden. A transport retry, if the exact transport/API contract eventually allows one, must preserve logical identity and still be reconciled; exact Hyperliquid idempotency behaviour remains external.

## Nonce ownership and signing

One `NonceManager` owns nonce assignment per signer/process. `CREATED -> NONCE_ASSIGNED` occurs once for the intent; then signing creates immutable signed economics and `SIGNED`. Multiple concurrent nonce owners for one signer are invalid architecture. Exact timestamp monotonicity, API-wallet/subaccount rules, and cross-process constraints require current external validation.

## Exact `OrderState` semantics

| State | Meaning | Entry action/data | Exit proof | Reservation rule |
|---|---|---|---|---|
| `CREATED` | valid unsent logical intent exists | persist intent identity | nonce assignment or local abort | held by plan |
| `NONCE_ASSIGNED` | signer owner assigned nonce | persist nonce event | signature success/failure | held |
| `SIGNED` | economics/signature frozen | create transport request | send attempt | held |
| `SENT` | transmission happened or may have happened | persist send-before/with effect | response/event/timeout | held |
| `PENDING_RESOLUTION` | submitted outcome not terminal/clear | await/query order/fill evidence | known live/terminal or ambiguity escalation | held |
| `RESTING` | exchange evidence says order is active/resting | start maker monitoring/timers | fill/cancel/reject/unknown | held for remaining size |
| `PARTIALLY_FILLED` | `0 < filled < requested` | append/dedupe fills; update actuals immediately | more fills, cancel, terminal, recovery | used part converts; remainder held |
| `FILLED` | requested quantity met within declared tolerance | apply all known fills | final reconciliation | used reservation becomes exposure |
| `CANCEL_REQUESTED` | cancel effect sent, not effective proof | monitor fills and status | canceled/filled/partial/unknown | remaining reservation held |
| `CANCELED` | exchange proves no longer active | account prior fills | terminal reconciliation | unused remainder releasable only after reconcile |
| `REJECTED` | exchange proves rejection | map `InternalRejectReason`; assess mismatch | terminal reconciliation/recovery if prior exposure | unused remainder after reconcile |
| `UNKNOWN` | economic effect may exist but is not provable yet | query/reconcile; block affected new risk | observed known state or escalation | fully conservative lock |
| `TERMINAL_RECONCILED` | final status, fills, and balance effect agree | release proven unused remainder | none for this lifecycle | final converted/released allocation |

The source does not define separate canonical `OPEN`, `SUBMITTED`, or `FAILED` enum values. “Open” is exchange evidence mapped to `RESTING`/current lifecycle; “submitted” describes transport, and generic `FAILED` would erase economic uncertainty.

## Canonical order transitions

| From | Evidence/event | Guard/action | To |
|---|---|---|---|
| `CREATED` | nonce assigned by owner | persist once | `NONCE_ASSIGNED` |
| `NONCE_ASSIGNED` | signature succeeds | freeze economics | `SIGNED` |
| `NONCE_ASSIGNED` | signature fails before any send | structured local failure; route abort/replan | no exchange-state transition |
| `SIGNED` | send initiated/possible | persist identity and request correlation | `SENT` |
| `SIGNED` | definite pre-transmission failure | record safe local failure | no exchange-state transition |
| `SENT` | non-terminal response/awaiting event | start resolution timer | `PENDING_RESOLUTION` |
| `SENT`/`PENDING_RESOLUTION` | exchange says resting | start maker lifecycle | `RESTING` |
| `SENT`/`PENDING_RESOLUTION` | fill total is partial | apply actual fill | `PARTIALLY_FILLED` |
| `SENT`/`PENDING_RESOLUTION` | fill total is full | apply actual fills | `FILLED` |
| `SENT`/`PENDING_RESOLUTION` | explicit reject | map reason | `REJECTED` |
| `SENT`/`PENDING_RESOLUTION` | outcome cannot be proved / timeout | query and reconcile | `UNKNOWN` |
| `RESTING` | partial fill | recalc maker/remainder/hedge | `PARTIALLY_FILLED` |
| `RESTING` | complete fill | apply actuals | `FILLED` |
| `RESTING`/`PARTIALLY_FILLED` | cancel requested | keep remainder potentially live | `CANCEL_REQUESTED` |
| `PARTIALLY_FILLED` | more but incomplete fills | idempotently update totals | `PARTIALLY_FILLED` |
| `PARTIALLY_FILLED` | cumulative full | apply actuals | `FILLED` |
| `CANCEL_REQUESTED` | fill during race | apply; recompute remaining | `PARTIALLY_FILLED` or `FILLED` |
| `CANCEL_REQUESTED` | exchange proves inactive with residual unfilled | reconcile prior fills | `CANCELED` |
| `CANCEL_REQUESTED` | cannot prove outcome | retain lock | `UNKNOWN` |
| `UNKNOWN` | queries prove live | resume monitoring | `RESTING`/`PARTIALLY_FILLED` |
| `UNKNOWN` | queries prove full/canceled/rejected | apply all fills first | corresponding known terminal state |
| `FILLED`/`CANCELED`/`REJECTED` | status + fills + balance agree | final accounting/release | `TERMINAL_RECONCILED` |

Terminal regression is forbidden. Duplicate events are no-ops after dedupe; incompatible late events generate evidence/reconciliation rather than state reversal.
