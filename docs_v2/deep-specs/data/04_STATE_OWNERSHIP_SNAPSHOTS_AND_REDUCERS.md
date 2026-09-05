# State Ownership, Snapshots and Reducers

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Ownership

Critical state has one logical writer: one BookState per market and one AccountState, InventoryState, ReservationState and ExecutionState per run/context. Adapters, Strategy and Risk cannot mutate them. Other modules read immutable snapshots.

The owner applies a total ordered event stream, increments the applicable version, verifies invariants, creates an immutable snapshot and publishes it atomically. A RiskSnapshot pins exact market/account/inventory/reservation/feature/infra/config versions.

## Reducer boundary

`Reducer(State, Event) → (NewState, Effects[])` is deterministic and performs no network I/O, blocking persistence or hidden randomness. EffectExecutor translates `SubmitOrder`, `CancelOrder`, `Persist`, `EmitMetric`, `RequestReconciliation` and related requests into environment actions, whose observed results return as events.

Commands never certify facts. A requested cancel may race with a fill; only ordered exchange/account events mutate state. Actual fills, never expected fills, update balances and inventory.

## Workers and TOCTOU

Workers receive immutable input and return `input_state_version` plus their result/validity envelope. The coordinator compares current versions and forecast TTL/validity. A stale result is discarded or revalidated, never committed automatically. Pre-send checks compare the plan's version/price/edge envelope against current state.

## Acceptance

Property tests cover duplicates, gaps, reorderings, partial fills, concurrent worker completion, state hashes and repeated replay. No thread completion order may change the canonical transition sequence.
