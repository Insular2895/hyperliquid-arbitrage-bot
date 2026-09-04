# 01 — Architecture, ownership, and five state machines

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Effect boundary

Strategy produces opportunity/candidate information; Simulator produces an `ExecutionForecast`; Risk produces a `RiskDecision`; only the `ExecutionCoordinator` may convert an allowed immutable `ExecutionPlan` into `ExecutionTransport` effects. A Strategy-to-exchange code path is constitutionally invalid.

The coordinator is the single logical writer of `ExecutionState`, coordinating the single-owned `AccountState` and `ReservationState`. Network callbacks, timer callbacks, workers, and model tasks enqueue typed events or immutable results; none mutate critical state directly.

## Five coordinated machines

| Machine | Owns | Does not own | Main signals |
|---|---|---|---|
| `EngineState` | global execution permission/readiness | individual order truth | feed/clock/infra health, reconciliation result, shutdown |
| `RouteExecutionState` | one plan across legs | exchange order lifecycle | validation, reservation, leg results, recovery/reconciliation completion |
| `OrderState` | one logical intent/order | route profitability | nonce/sign/send, order update, fill, cancel, query result |
| `RecoveryState` | existing-exposure reduction plan | new opportunity capture | actual exposure, candidate exits, recovery fills/failure |
| `ReconciliationState` | proof of local/exchange consistency | strategy ranking | fetched orders/fills/balances, comparison/resolution result |

`RECOVERY_REQUIRED` is a deliberate cross-machine signal and state name in both Route and Recovery. Route completion waits for order terminality, fill application, reservation/inventory reconciliation, and dust policy. Engine `READY` waits for reconciliation confidence.

## Ordered event contract

All concurrent inputs enter the central `EngineInputEvent` stream and receive a deterministic total order. The source proposes event/replay time, source priority on ties, then recorder sequence; PASS 06 must freeze the exact ordering schema. Strategic timers are recorded events. Event IDs, fill IDs, intent IDs, execution IDs, CLOIDs, and state versions make duplicate and stale inputs detectable.

Reducers must satisfy idempotence for deduplicated events and monotonicity for terminal states. An incompatible late event is evidence requiring reconciliation, never permission to regress a terminal state.

## Worker/version boundary

Workers receive immutable `BookState`, account, inventory, reservation, configuration, model, and formula versions. Their result includes `input_state_version`. Before commit/send, the coordinator compares that version and the plan validity envelope with current state. A material change causes revalidation, replan, or abort; it cannot be ignored because the computation completed first.

## Persistence boundary

State mutation emits an in-memory journal event and effect requests. Persistence uses a durable asynchronous queue so blocking disk I/O is outside the hot-path reducer. Checkpoints accelerate recovery but are not economic truth. On restart:

```text
checkpoint + append-only journal + exchange orders/fills/balances
-> reconstructed and reconciled state
```

Account/order/fill events receive higher retention priority than droppable raw market diagnostics. Exact durability/latency tradeoffs remain Data/Operations-owned and calibrated.

## Permission lattice

| Condition | New risk | Continue existing | Cancel | Recover | Reconcile |
|---|---:|---:|---:|---:|---:|
| `READY` and current gates pass | yes | yes | yes | yes | yes |
| `DEGRADED` | only explicit bounded policy | guarded | yes | yes | yes |
| `RECOVERY_ONLY` | no | risk-reducing only | yes | yes | yes |
| `HALTED` | no | no risk increase | policy/manual safety only | policy/manual | yes |
| affected order `UNKNOWN` | no on affected resources | no unproven reuse | guarded | proven-exposure only | required |

This lattice is fail-conservative: failure can only retain or reduce authority.
