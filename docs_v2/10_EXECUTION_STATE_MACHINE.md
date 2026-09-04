# 10 — Execution State Machine

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## 1. Purpose

This specification defines how an approved economic opportunity becomes exchange-observed fills, inventory, recovery, reconciliation, and evidence. Its governing order is:

```text
ExchangeTruth > LocalAssumption
SafetyOfExistingExposure > NewOpportunity
```

The module is safe only if uncertainty reduces activity, actual fills determine exposure, and duplicate or late events cannot create duplicate economic effects.

## 2. Scope

Execution owns the ordered coordination of validation, reservations, immutable plans, order intents, signing, transport effects, order/route states, fill application, continuation, recovery entry, and reconciliation. It exposes accounting facts and state transitions.

It does not discover routes, approve Risk policy, estimate participant behaviour, invent exchange rules, own exact Data schemas, or decide deployment and monitoring policy. Those are cross-domain contracts.

## 3. Authority

SRC-004 Dossier 1, sections 1–142, is the execution-closure authority. SRC-005 closes Risk and Data Contracts. SRC-006 closes validation/deployment where applicable. Earlier sources remain provenance and operational context; a conflicting earlier execution description cannot override closure.

Date-sensitive Hyperliquid facts are not silently treated as current. They remain `EXTERNAL_REVALIDATION` in §35.

## 4. Core principles

1. Strategy never talks to the exchange. It proposes; Risk authorizes; Execution alone requests effects.
2. One logical single writer owns critical execution state. Readers receive immutable versioned snapshots.
3. Validate current state immediately before any risk-increasing effect; stale asynchronous results are discarded or revalidated.
4. Reserve balance, book capacity, and Risk capacity before creating orders.
5. `ExecutionPlan` becomes economically immutable in `PLANNED`; a material change creates a linked version/new intent.
6. A stable CLOID identifies one logical intent. A timeout never authorizes a blind resend.
7. Signing freezes economics. `SENT` means the order may have executed, even if no ACK arrived.
8. `UNKNOWN` is a first-class economic uncertainty state; affected reservations stay locked.
9. Append-only, deduplicated actual fills drive inventory, next-leg size, recovery, reconciliation, and accounting.
10. Cancel requested is not canceled. Fill-during-cancel is normal.
11. Existing exposure reduction has priority over new opportunity capture.
12. Replay, Shadow, Micro-live, and Live share the reducer and machine semantics; only explicit adapters/effect boundaries differ.

## 5. Ownership architecture

```text
Strategy -> candidate -> Simulator forecast -> RiskDecision
                                              |
                                              v
                                     ExecutionCoordinator (single writer)
                                      | route | order | reservations
                                      v       v       v
                               ExecutionTransport -> exchange/emulator/null
                                      |
                         OrderEvents / FillEvents / queries
                                      v
                                  EventReducer
                                      |
                      actual account + inventory + recovery/reconcile
```

Workers may compute from immutable snapshots only. Each result carries the input version; the coordinator refuses stale commits. The reducer is as pure as practical; it emits effect requests rather than doing network or blocking journal I/O inside state mutation.

## 6. Five state machines

| Machine | Exact states | Initial | Success / safe terminal |
|---|---|---|---|
| `EngineState` | `BOOTING`, `SYNCING`, `RECONCILING`, `READY`, `DEGRADED`, `RECOVERY_ONLY`, `HALTED`, `SHUTTING_DOWN`, `STOPPED` | `BOOTING` | operational `READY`; process `STOPPED` |
| `RouteExecutionState` | `DETECTED`, `VALIDATING`, `RESERVING`, `PLANNED`, `EXECUTING`, `COMPLETED`, `ABORTED`, `RECOVERY_REQUIRED`, `RECONCILING`, `FAILED_SAFE` | `DETECTED` | `COMPLETED`, `ABORTED`, `FAILED_SAFE` after truth is resolved |
| `OrderState` | `CREATED`, `NONCE_ASSIGNED`, `SIGNED`, `SENT`, `PENDING_RESOLUTION`, `RESTING`, `PARTIALLY_FILLED`, `FILLED`, `CANCEL_REQUESTED`, `CANCELED`, `REJECTED`, `UNKNOWN`, `TERMINAL_RECONCILED` | `CREATED` | `TERMINAL_RECONCILED` |
| `RecoveryState` | `RECOVERY_REQUIRED`, `RECOVERY_PLANNING`, `RECOVERY_RESERVED`, `RECOVERY_EXECUTING`, `RECOVERY_VERIFYING`, `RECOVERED`, `RECOVERY_FAILED` | `RECOVERY_REQUIRED` | `RECOVERED`; `RECOVERY_FAILED` escalates to manual/hard halt |
| `ReconciliationState` | `RECONCILE_REQUESTED`, `FETCHING`, `COMPARING`, `RESOLVING`, `CONSISTENT`, `UNRESOLVED` | `RECONCILE_REQUESTED` | `CONSISTENT`; `UNRESOLVED` blocks affected new risk |

There are 45 machine-state entries and 43 distinct symbols because `RECONCILING` is shared by Engine and Route, while `RECOVERY_REQUIRED` is shared by Route and Recovery. Detailed entry/exit permissions and full matrices are in deep specs 01–03, 09, and 10.

## 7. EngineState

`BOOTING` constructs local services without admitting risk. `SYNCING` obtains metadata, feeds, orders, fills, balances, and time health. `RECONCILING` proves local/exchange consistency. Only then may `READY` admit new risk.

`DEGRADED` preserves bounded operation while a non-fatal dependency is impaired; it must never silently widen permissions. `RECOVERY_ONLY` rejects new opportunities while permitting cancel, recovery, queries, and reconciliation. `HALTED` forbids automated risk-increasing effects. `SHUTTING_DOWN` cancels/settles/persists as policy requires; `STOPPED` has no execution effects.

Market staleness, account-feed loss, clock unsafety, unresolved order exposure, or balance mismatch must move permission toward degradation/recovery/reconciliation, never toward greater activity.

## 8. RouteExecutionState

The canonical path is:

```text
DETECTED -> VALIDATING -> RESERVING -> PLANNED -> EXECUTING
          -> ABORTED on a known safe pre-exposure stop
EXECUTING -> COMPLETED when every order/fill/reservation/inventory condition closes
EXECUTING -> RECOVERY_REQUIRED when actual exposure cannot follow the safe continuation
any ambiguity -> RECONCILING -> prior safe state or FAILED_SAFE
```

`COMPLETED` requires all intended orders terminal, all known fills applied, intermediate exposure within permitted dust, reservations reconciled, inventory updated, and route PnL computed. An HTTP ACK or individual `FILLED` never completes a route by itself.

## 9. Reservations

Reservation order is `VALIDATE -> RESERVE -> PLAN -> CREATE INTENT -> SEND`. At minimum:

```text
AvailableBalance[a] = ActualBalance[a] - ReservedBalance[a]       (QF-073)
AvailableBookCapacity = ObservedCapacity - ReservedCapacity       (QF-074)
```

`BalanceReservation`, `BookCapacityReservation`, and `RiskReservation` prevent concurrent plans from spending the same capacity. A fill converts the used reservation into actual exposure. Known cancel/reject/zero-fill releases only the unused remainder after terminal reconciliation. `UNKNOWN` keeps potentially consumed capacity locked. Reservations cannot go negative and are versioned against account/book state.

## 10. ExecutionPlan

The SRC-005 contract contains: `execution_id`, `opportunity_id`, `route_id`, `size`, `legs[]`, `execution_mode`, `reservations[]`, `risk_decision_id`, `model_versions`, `config_versions`, `created_at`, and `plan_version`.

Once `PLANNED`, economic fields are immutable. A changed size, route, price envelope, model/config basis, or leg policy creates a linked plan version and new logical intent where applicable. Before send, current book/account/inventory/reservation/infra versions are checked against the validity envelope; breach means replan or abort, not mutation in place.

## 11. OrderIntent

The frozen SRC-005 schema is: `intent_id`, `execution_id`, `leg_id`, `market_id`, `side`, `price_ticks`, `size_lots`, `tif`, `cloid`, optional `nonce`, `risk_decision_id`, and `created_at`. Price and size are quantized before the intent; floating-point strategy values cannot bypass this boundary.

`SignedOrderIntent` wraps `intent`, `nonce`, `signature`, and `signed_at`. After signing it is immutable.

## 12. CLOID

CLOID is stable per logical intent and is the primary bridge across submit response loss, status queries, open-order queries, fills, journal replay, and restart reconciliation. Retrying a transport request reuses the same intent identity; creating another economically equivalent order without resolving the original is forbidden.

Exact CLOID width, formatting, lookup/cancel behaviour, and current exchange support are external facts to revalidate.

## 13. Nonce

The source requires one `NonceManager` owner per signer/process. Nonce assignment precedes signing and produces `NONCE_ASSIGNED`. The conceptual source rule is `max(atomic_increment(), current_unix_ms_if_needed)`; its exact current Hyperliquid semantics, wallet/subaccount interaction, and concurrency constraints remain external.

Nonce uncertainty is not order-state certainty. After possible transmission, a new nonce plus duplicate economic intent is not a safe retry strategy.

## 14. OrderState

Normal pre-send transitions are `CREATED -> NONCE_ASSIGNED -> SIGNED -> SENT`. From `SENT`, transport/order evidence may produce `PENDING_RESOLUTION`, `RESTING`, `PARTIALLY_FILLED`, `FILLED`, `CANCEL_REQUESTED`, `CANCELED`, `REJECTED`, or `UNKNOWN` through valid paths.

`RESTING` applies to a known live maker/resting order. `PARTIALLY_FILLED` records `q_remaining = q_requested - q_filled`, actual VWAP, fees, and asset delta. `FILLED` closes only the individual order within lot/rounding tolerance. Final states converge to `TERMINAL_RECONCILED` only after final status, all known fills, and balance effect are accounted.

Monotonicity is mandatory: `FILLED` cannot become `RESTING`. A late incompatible event is recorded as `OUT_OF_ORDER_EVENT` and reconciled; the machine does not regress.

## 15. Send/ACK uncertainty

Before confirmed transmission, a local send failure may return to a known safe abort/replan path. Once transmission might have happened, economic state is uncertain. `SENT` therefore means “possibly executed,” not “ACK received.” A successful HTTP envelope says a request was processed; it does not prove a fill or profitable route.

ACK timeout is derived from the observed ACK latency distribution (for example a validated high percentile plus safety margin). Timeout triggers `PENDING_RESOLUTION`/`UNKNOWN` and status/fill/open-order reconciliation; it never maps directly to `REJECTED` or authorizes a blind resend.

## 16. UNKNOWN

`UNKNOWN` means: the bot may have changed economic exposure but cannot yet prove the outcome. Allowed actions are status/fill/open-order/balance queries, reconciliation, bounded cancel when semantically valid, and risk reduction based on proven exposure. Forbidden actions are blind resend and new use of affected capital.

The order reservation remains locked. The engine disables affected new risk and may enter `RECOVERY_ONLY`; it does not necessarily halt unrelated, proven-safe resources. Resolution uses exchange truth and converges to the observed order/fill state, then `TERMINAL_RECONCILED` when complete.

## 17. Fills

`FillEvent` carries the SRC-005 fields `fill_id`, optional `cloid`/`oid`, `market_id`, `side`, `price_ticks`, `size_lots`, optional `fee_asset`, `fee_amount`, optional `exchange_ts`, `recv_ts`, and `source`.

The `FillLedger` is append-only and deduplicates by stable fill identity across stream, snapshot, and reconciliation. Applying the same fill twice changes nothing:

```text
Reduce(Reduce(S, e), e) = Reduce(S, e)
```

Every accepted fill immediately updates order totals, actual inventory, used reservation, leg accounting, and continuation/recovery inputs. It is never deferred until route completion.

## 18. Partial fills

Partial fill is a normal branch. The engine records actual quantity, VWAP, fees, rounding, and output asset; recomputes next-leg minimum notional, book, edge, slippage, forecasts, and Risk; then chooses continuation or recovery from current state.

The next leg uses actual available output, never the pre-trade theoretical quantity. A second/third-leg partial routes the completed fraction onward only if newly valid and sends residual intermediate exposure to Recovery. Maker partials create exposure immediately, even while a remainder is resting or canceling.

## 19. Dust / intermediate buffers

If an actual partial is below the next-leg minimum, it becomes explicit `DUST_EXPOSURE`; the route is not falsely closed. Policies may retain permitted dust, rebalance periodically, recover by another valid route, or aggregate it in `PendingIntermediateBuffer`.

Aggregation is allowed only for the same asset and compatible economic/risk context, with traceable contributing fills and calibrated maximum age, inventory, and adverse move. A buffer exceeding any gate routes to recovery/rebalance. Inventory and accounting retain the exposure throughout; permitted dust is a policy tolerance, not zero.

## 20. Cancel semantics

`CANCEL_REQUESTED` records that a cancel effect was sent; it is not proof that the order is inactive. Until the exchange truth is known, the remaining quantity may still fill and its reservation remains locked. A fill arriving during cancellation is applied exactly once, may require hedge/recovery, and changes the residual cancel quantity.

`CANCELED` is accepted only with exchange evidence, after which fills accumulated before effective cancellation are reconciled. Only `TERMINAL_RECONCILED` allows final unused-reservation release.

## 21. Taker execution

Taker legs use protected IOC/marketable limits with a bounded worst acceptable price; no unbounded market order is canonical. BUY protection cannot exceed the maximum acceptable price; SELL protection cannot fall below the minimum. QF-007/008 enforce exchange precision; QF-009–016 derive book-walk quantities, actual VWAP, slippage, fees, and conversion.

Zero fill aborts before any next leg and releases reconciled unused reservations. Full fill continues only after actual inventory and fresh-state revalidation. Partial fill continues at the smaller actual amount if valid, otherwise Recovery handles current exposure.

## 22. Maker execution

Maker ALO lifecycle is represented by canonical order states: submitted intent becomes `SENT`, then known `RESTING`, one or more `PARTIALLY_FILLED`, `FILLED`, or `CANCEL_REQUESTED -> CANCELED`, with uncertainty/reconciliation branches.

While resting, Execution consumes edge survival, route EV, maker fill/queue forecast, adverse selection, inventory limits, and market freshness. `MAKER_MAX_AGE` is calibrated from fill distribution, edge survival, adverse selection, and regime—never a universal constant. Each economically executable maker partial is evaluated promptly for its taker continuation; the remainder may rest only while the route stays permitted.

## 23. TT / MT / TTT / MTT

| Mode | Legs | Canonical behaviour | Initial status |
|---|---|---|---|
| `TT` | taker -> taker | Protected IOC; revalidate and resize after leg 1 | supported; activation/capital still evidence-gated |
| `MT` | maker -> taker | ALO maker; actual partial/full drives prompt taker evaluation | supported; maker authority evidence-gated |
| `TTT` | taker -> taker -> taker | Non-atomic; actual fill and new decision after every leg | supported; activation/capital evidence-gated |
| `MTT` | maker -> taker -> taker | Maker partial/full becomes an actual two-taker continuation | supported; maker authority evidence-gated |

Every leg has independent zero/full/partial/reject/unknown outcomes. Batching cannot turn a triangle into an atomic transaction.

## 24. TM / MM disabled

`TM` and `MM` remain representable in `ExecutionMode`, but disabled by default. A maker leg after earlier exposure can strand the intermediate asset while waiting. Activation requires an explicit strategy flag, validated queue/fill/adverse-selection model, dedicated Risk limits, recovery evidence, and a human decision. “Type supported,” “enabled,” and “capital validated” are three different claims.

## 25. Recovery

Triggers include a partial fill, lost continuation edge, rejection after prior exposure, ambiguous order with possible exposure, unexpected balance, or later-leg failure. New risk using the same capital is forbidden.

The flow is `RECOVERY_REQUIRED -> RECOVERY_PLANNING -> RECOVERY_RESERVED -> RECOVERY_EXECUTING -> RECOVERY_VERIFYING -> RECOVERED`; failure produces `RECOVERY_FAILED` and manual/hard-halt escalation. Planning starts from actual current exposure and current books, not the original narrative.

QF-079 selects the action maximizing expected portfolio value after recovery/equivalently minimizing expected recovery loss under constraints. QF-080 measures loss from recovery-start state; sunk losses do not authorize unlimited new loss. Candidate exits may include intended destination, original asset, core inventory, or split exits. Negative-EV risk reduction is permissible only within dedicated maximum slippage, notional, freshness, time, and attempt constraints. A failed recovery order is reconciled, remaining exposure recomputed, and a new plan created—never blindly retried.

## 26. Reconciliation

The canonical machine is `RECONCILE_REQUESTED -> FETCHING -> COMPARING -> RESOLVING -> CONSISTENT | UNRESOLVED`. It compares local non-terminal orders by CLOID/OID with current orders/status, deduplicated fills, balances, inventory, and reservations.

Required order of truth is orders -> fills -> balances/exposure. `Diff[a] = ExchangeBalance[a] - ExpectedLocalBalance[a]`; only a policy-approved dust tolerance may be accepted. A material mismatch prevents `READY`. Hot-path streams/responses provide speed; queries/snapshots provide ambiguity resolution. Exact endpoints/subscription names remain external.

## 27. Crash/restart

Startup is always `BOOTING -> SYNCING -> RECONCILING`; never automatic `READY`. A crash after send but before ACK persistence is resolved by CLOID/order/fill/balance evidence. A crash after fill or during recovery reconstructs journal/checkpoint state, then lets exchange truth correct it before any new risk.

The execution journal is append-only. Critical source events include `ExecutionCreated`, `ReservationCreated`, `OrderIntentCreated`, `OrderSent`, `FillApplied`, `CancelRequested`, `RecoveryStarted`, and `ExecutionCompleted`. Persistence is queued/asynchronous so the hot path does not block, but durability loss is tolerated only because reconciliation can reconstruct economic truth. Checkpoint + journal + exchange reconciliation is the recovery basis.

## 28. Timers

Strategic timers are explicit replayable `TimerEvent`s: `RiskRecheck`, `MakerExpiry`, `UnknownResolutionTimeout`, `ReconciliationTrigger`, and `MetricsFlush`. ACK timeout, maker age, route horizon, recovery timeout, and reconciliation timeout come from measured/calibrated distributions and policy. No magic millisecond value is normative.

A timer event requests a guarded transition; it does not manufacture economic truth. In particular, ACK/unknown/reconciliation timeouts increase uncertainty or escalate state, not fabricate rejection/cancellation.

## 29. Dead-man switch

The Dead Man's Switch is an additional safety mechanism for resting maker/GTC-like orders: while such exposure exists, the bot refreshes a scheduled cancel deadline so a complete process failure can cancel open orders. It is not the normal cancel path and does not replace local state, recovery, or reconciliation. IOC orders do not rest, so the mechanism is mainly relevant to maker orders.

Current schedule semantics, minimum future deadline, daily trigger limit, supported scope, and API behaviour are `EXTERNAL_REVALIDATION`.

## 30. Transport abstraction

`ExecutionTransport` exposes conceptual `submit`, `cancel`, and `query` effects. SRC-005 lists `HyperliquidHttpTransport`, `HyperliquidWsTransport`, `ReplayTransport`, `PaperTransport`, and `NullShadowTransport`. `TransportRequest` contains `signed_intent`, `transport_type`, `request_id`, and optional `send_at`.

Transport state and order economic state are separate. Direct vs batched and HTTP vs WebSocket are benchmarked implementations; no provider/transport-specific branch changes Strategy, Risk, or reducer semantics.

## 31. Replay/Shadow/Live parity

`RunMode` is exactly `Replay`, `Paper`, `Shadow`, `MicroLive`, or `Live`. Replay sends intents to the exchange emulator, which emits the same Order/Fill event schemas. Shadow uses `NullShadowTransport` and emits `WouldSubmitEvent`; it never mutates the actual account. Micro-live uses real effects at calibrated small authority and validates send/ACK/fill/partial/fees/recovery/reconciliation. Live uses the real transport under promoted limits.

The same ordered inputs, resolved config, model/formula versions, state versions, and seed must reproduce the same intents, transitions, Risk decisions, and accounting. Timers are events, duplicate fills are idempotent, and all stochasticity is explicit/seeded.

## 32. Accounting/inventory interfaces

Each fill emits actual price, size, fee, side, IDs, timestamps, inventory delta, used reservation, and correlation chain. Each leg accumulates `actual_input`, `actual_output`, `actual_fee`, actual VWAP/slippage/latency. Each route exposes expected versus actual PnL, fees, slippage, and latency.

Execution does not collapse Strategy PnL, Execution PnL, Recovery Loss, Inventory mark-to-market, Bridge/Rebalance, fees, or infrastructure cost. QF-011/014/015/016 and accounting QF-106–108 remain Formula/PASS 11 authority. Inventory changes immediately on fills, not on route completion.

## 33. Risk interfaces

Before each risk-increasing transition, a current `RiskDecision` and version-compatible snapshot are mandatory. The hierarchy remains Global -> Inventory/Allocation -> Route -> Leg -> Order. Execution cannot bypass, mutate, or infer Risk approval.

Cancel and recovery use safety/recovery gates appropriate to existing exposure. Global daily profit cannot widen price protection, allow blind retries, ignore `UNKNOWN`, or excuse extra partial exposure. Scheduler priority is cancels/safety, recovery, reconciliation, existing continuation, then new opportunities.

## 34. Validation

Required evidence includes unit/property tests, deterministic Replay, fault injection, Shadow evidence, and calibrated Micro-live evidence. Mandatory scenarios cover zero/full/partial fills, duplicate/out-of-order events, response loss after send, lost ACK/cancel, cancel race, restart after send/fill/during recovery, balance mismatch, feed loss/reconnect, stale maker, price protection, dust/minimum notional, recovery failure, and reconciliation timeout.

Core invariants include non-negative fills/reservations; filled not above requested beyond declared tolerance; no terminal regression; duplicate fill no-op; unknown capital locked; new risk only in allowed EngineState; actual-fill-driven continuation; and deterministic replay identity. Numeric promotion thresholds are not invented here.

## 35. External revalidation

Before implementation or Live reliance, revalidate current Hyperliquid support and semantics for IOC/FOK/ALO/GTC, protected marketable limits, tick/lot/minimum-notional rules, CLOID format/query/cancel, nonce and signer/API-wallet/subaccount rules, order-status/open-order/fill/balance APIs, WebSocket names/snapshots/reconnect, HTTP versus WS submission, batching, rejection/status values, and Dead Man's Switch limits. PASS 04 performs no web research and records no claim of current validity.

## 36. Deep-spec links

- [Architecture, ownership, five machines](deep-specs/execution/01_ARCHITECTURE_OWNERSHIP_AND_FIVE_STATE_MACHINES.md)
- [Engine and Route transitions](deep-specs/execution/02_ENGINE_AND_ROUTE_EXECUTION_STATE_MACHINES.md)
- [Intent, CLOID, nonce, Order lifecycle](deep-specs/execution/03_ORDER_INTENT_CLOID_NONCE_AND_ORDER_LIFECYCLE.md)
- [Reservations and immutable plan](deep-specs/execution/04_RESERVATIONS_BALANCES_AND_EXECUTION_PLAN.md)
- [Taker TT/TTT](deep-specs/execution/05_TAKER_EXECUTION_TT_AND_TTT.md)
- [Maker MT/MTT and disabled modes](deep-specs/execution/06_MAKER_EXECUTION_MT_MTT_AND_DISABLED_MODES.md)
- [Partial fills, dust, buffers](deep-specs/execution/07_PARTIAL_FILLS_DUST_AND_INTERMEDIATE_BUFFERS.md)
- [Cancel races, timers, uncertainty](deep-specs/execution/08_CANCEL_RACES_TIMERS_AND_ORDER_UNCERTAINTY.md)
- [Recovery](deep-specs/execution/09_RECOVERY_STATE_MACHINE_AND_EXIT_SELECTION.md)
- [Reconciliation and restart](deep-specs/execution/10_RECONCILIATION_RESTART_AND_CRASH_CONSISTENCY.md)
- [Transport and mode parity](deep-specs/execution/11_EXECUTION_TRANSPORT_REPLAY_SHADOW_AND_LIVE.md)
- [Failures, reason codes, validation](deep-specs/execution/12_FAILURE_MODES_REASON_CODES_AND_VALIDATION.md)

Analysis evidence, formula/data crosschecks, transition/failure matrices, requirement dispositions, external facts, conflicts, and legacy comparison are under `_analysis/pass04_execution/`.
