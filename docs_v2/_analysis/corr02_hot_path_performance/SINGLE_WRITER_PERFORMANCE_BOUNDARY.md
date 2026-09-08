# Single-Writer Performance Boundary

DOCUMENTATION STATUS: LOCKED REFINEMENT — AWAITING FINAL HUMAN REVIEW

One logical writer remains mandatory for `BookState`, `AccountState`, `InventoryState`, `ReservationState`, Execution, Recovery, Reconciliation and Accounting truth. Performance work may change layout, immutable publication and communication, never introduce competing mutable authority.

This is the existing **single logical writer** rule; it is preserved, not weakened or replaced by atomics.

Workers may:

- read immutable versioned snapshots;
- compute BBO classification, exact economics, features, forecasts or compression;
- return a proposal carrying the complete input tuple and validity envelope.

Only the owning ordered coordinator may commit. It compares current state, discards or revalidates stale work, performs applicable Risk checks and preserves deterministic order. Atomics or a lock-free queue at a handoff do not turn the payload state into multi-writer state.

Measure owner execution, queue wait, worker execution, stale discard and revalidation separately. If the writer is a bottleneck, first eliminate work and improve layout/batching that preserves order. Sharding is a future architectural/semantic decision requiring ownership, cross-shard reservation and Replay proof; it is not authorized here.
