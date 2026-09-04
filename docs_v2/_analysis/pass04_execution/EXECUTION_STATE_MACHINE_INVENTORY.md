# PASS 04 — Execution State Machine Inventory

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

SRC-004 Dossier 1 is authoritative. Exact state locators: Engine §§7–16 (source lines 161–470), Route §§17–18 (471–533), Order §§22–39 (605–1043), Recovery §§67–74 (1534–1746), Reconciliation §§75–81 (1747–1940). Line endpoints are discovery locators; section names control if rendering changes.

| Machine | Exact enum/state names | Owner | Purpose | Initial | Terminal/safe result | Persistent fields | Cross-machine signals | Risk permissions | Replay requirement |
|---|---|---|---|---|---|---|---|---|---|
| `EngineState` | `BOOTING`; `SYNCING`; `RECONCILING`; `READY`; `DEGRADED`; `RECOVERY_ONLY`; `HALTED`; `SHUTTING_DOWN`; `STOPPED` | global ExecutionCoordinator | global readiness and effect permissions | `BOOTING` | operational `READY`; process `STOPPED` | state, reason, health/snapshot versions, transition time/correlation | reconciliation result, route recovery/failure, feed/clock/infra/control | new risk only in `READY` or explicitly bounded `DEGRADED`; recovery/cancel remains prioritized | same ordered health/timer/control events reproduce transitions |
| `RouteExecutionState` | `DETECTED`; `VALIDATING`; `RESERVING`; `PLANNED`; `EXECUTING`; `COMPLETED`; `ABORTED`; `RECOVERY_REQUIRED`; `RECONCILING`; `FAILED_SAFE` | one route execution actor/coordinator | coordinate approved plan across legs and terminal accounting | `DETECTED` | `COMPLETED`; known-safe `ABORTED`; conservative `FAILED_SAFE` | execution/route/plan IDs, plan version, legs, reservations, actual inventory delta, expected/realized PnL, recovery, times | Order fill/terminal/unknown, Recovery result, Reconciliation result | every risk-increasing leg current-gated; same-capital new risk blocked in recovery/ambiguity | actual event ordering and state versions determine same route path |
| `OrderState` | `CREATED`; `NONCE_ASSIGNED`; `SIGNED`; `SENT`; `PENDING_RESOLUTION`; `RESTING`; `PARTIALLY_FILLED`; `FILLED`; `CANCEL_REQUESTED`; `CANCELED`; `REJECTED`; `UNKNOWN`; `TERMINAL_RECONCILED` | route/order reducer under coordinator | one logical intent’s economic lifecycle | `CREATED` | `TERMINAL_RECONCILED` | intent/CLOID/OID/nonce, requested/filled, VWAP/fees, timestamps, state, transport correlation | fills update Route/Inventory; unknown requests Reconciliation; partial may request Recovery | `UNKNOWN` locks resource; cancel/recovery allowed; no blind resend | duplicate fills no-op; terminal monotonic; emulator/live schema identical |
| `RecoveryState` | `RECOVERY_REQUIRED`; `RECOVERY_PLANNING`; `RECOVERY_RESERVED`; `RECOVERY_EXECUTING`; `RECOVERY_VERIFYING`; `RECOVERED`; `RECOVERY_FAILED` | RecoveryEngine coordinated by Execution | reduce existing actual exposure by best current exit | `RECOVERY_REQUIRED` | `RECOVERED`; failure `RECOVERY_FAILED` escalates | recovery ID/parent execution, exposure snapshot, candidates/plan versions, reservations, child intents/fills, attempts/times, actual loss | Route trigger/result, Order events, Reconciliation proof, Risk recovery gate | negative EV may be allowed only for bounded reduction; no unlimited loop/new risk | identical candidate inputs/order/fill events reproduce selection/remaining exposure |
| `ReconciliationState` | `RECONCILE_REQUESTED`; `FETCHING`; `COMPARING`; `RESOLVING`; `CONSISTENT`; `UNRESOLVED` | Reconciliation engine/single account-state owner | prove local state against exchange truth | `RECONCILE_REQUESTED` | `CONSISTENT`; conservative `UNRESOLVED` | scope/reason, fetched order/fill/balance references, comparison diffs, applied events, versions/times | Engine readiness, Order unknown resolution, Route/Recovery continuation | affected new risk forbidden until `CONSISTENT`; locks retained on unresolved | recorded queries/snapshots and stable dedupe/order reproduce result |

## State count

- Machine-state entries: **45**.
- Distinct state symbols: **43** (`RECONCILING` and `RECOVERY_REQUIRED` are each deliberately shared across machines).
- Generic `OPEN`, `SUBMITTED`, `FAILED`, and `ORDER_FAILED` are **not** additional canonical enum values.

## Per-state common contract

Every state implementation/documented transition must carry meaning, owner, entry/exit evidence, permitted/prohibited actions, current data/reservation effect, Risk permission, timer conditions, terminality, failure path, reconciliation need, and persistence event. The complete row-level crosscheck is `EXECUTION_TRANSITION_MATRIX.md`.
