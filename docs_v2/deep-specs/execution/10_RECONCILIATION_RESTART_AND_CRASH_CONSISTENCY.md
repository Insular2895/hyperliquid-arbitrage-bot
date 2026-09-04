# 10 — Reconciliation, restart, and crash consistency

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Authority of observed exchange state

Hot-path order updates, fills, and submission responses provide low-latency evidence. Ambiguity is resolved from current open orders/order status, fills, and account/balance state plus local Order/Fill ledgers. Endpoint names and snapshot semantics remain external facts; the internal proof order is fixed:

```text
orders -> fills -> balances/exposure -> reservations/inventory -> readiness
```

## Exact `ReconciliationState`

| State | Work | Prohibited | Exit |
|---|---|---|---|
| `RECONCILE_REQUESTED` | define affected scope/reason and freeze its new risk | releasing unknown capacity | fetch starts |
| `FETCHING` | obtain exchange orders/status, fills, balances and local ledgers | infer missing response as no order | sufficient snapshot or timeout |
| `COMPARING` | match CLOID/OID; dedupe fills; compute balance/inventory/reservation differences | mutate truth to fit local state | consistent or discrepancies |
| `RESOLVING` | apply missing unique fills/status; correct derived local state; recompute exposure | blind resend or assumption-based READY | consistent or unresolved |
| `CONSISTENT` | record proof/version and release only proven remainder | none beyond normal gates | caller resumes safe state |
| `UNRESOLVED` | preserve evidence/locks; escalate scope | affected new risk | later explicit retry/manual process |

## Canonical algorithm

1. For each local non-terminal intent, find exchange evidence by CLOID/OID.
2. Classify it as open/resting, filled, canceled, rejected, or missing/unknown without inventing a terminal state.
3. Fetch and deduplicate all corresponding fills from stream/snapshot/query.
4. Apply missing fills exactly once and derive actual fees/inventory.
5. Compare exchange and expected local balances: `Diff[a] = ExchangeBalance[a] - ExpectedLocalBalance[a]`.
6. Accept only configured per-asset dust tolerance; material mismatch is `BALANCE_MISMATCH`.
7. Recompute actual reservations and exposure from proven status/fills.
8. Emit `CONSISTENT` only if the affected scope is fully explained; otherwise `UNRESOLVED`.

`UNRESOLVED` is a safety result, not permission to discard the local record. It keeps relevant reservations unavailable and prevents Engine `READY` for the affected required scope.

## Startup and crash points

Startup is `BOOTING -> SYNCING -> RECONCILING`; no route admission occurs earlier.

| Crash point | Local uncertainty | Required reconstruction |
|---|---|---|
| before send | whether effect began must be proven by effect record | if provably unsent, safe abort; otherwise query CLOID |
| after send, before ACK persisted | order may be live/filled | CLOID/order/fill/balance reconciliation |
| after ACK, before fill persisted | fills may be missed | fetch/dedupe fills, apply inventory |
| after fill, before inventory persisted | local exposure understated | journal + exchange fill, then account comparison |
| during cancel | remainder may fill | resolve final fills and cancel status |
| during recovery | recovery may partially/fully execute | rebuild all recovery child intents/fills and remaining exposure |
| after completion marker, before release persisted | reservation may look held | prove terminality/accounting, then idempotent release |

## Journal/checkpoint contract

SRC-005 exact `ExecutionJournalEvent` fields are `journal_seq`, `event`, `timestamp`, optional `checksum`. Canonical event names include `ExecutionCreated`, `ReservationCreated`, `OrderIntentCreated`, `OrderSent`, `FillApplied`, `CancelRequested`, `RecoveryStarted`, `ExecutionCompleted`.

The journal is append-only and asynchronously durable so logging/persistence does not block the reducer. Periodic checkpoints cover Account, Inventory, Reservation, and execution summaries. A checkpoint is never sole truth; restart combines checkpoint, journal, and exchange reconciliation. Applying the same journal/fill event again must be idempotent.

## Disconnect/reconnect

Market-feed staleness disables new risk beyond calibrated freshness; resting maker cancellation follows Risk policy and active exposure may force `RECOVERY_ONLY`. Account/order/fill-feed loss disables new risk immediately and requires query-based reconciliation.

Reconnect sequence is disconnect -> disable new risk -> reconnect -> subscribe -> consume snapshot -> query missed state as needed -> reconcile -> `READY` only on consistency. Neither TCP reconnect nor subscription ACK is reconciliation.

## READY gate

Engine can return `READY` only when required feeds/time/infra are healthy enough, every required reconciliation scope is `CONSISTENT`, no unexplained balance mismatch/unknown order remains, reservations match actual exposure, and Risk permits new admission. Numeric freshness/dust/timeout thresholds remain calibrated.
