# Recorder Background-I/O Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Boundary

The hot path performs only a minimal bounded handoff of an already-identified typed record/reference and explicit enqueue outcome. Filesystem open/write/flush/fsync, large serialization, compression, checksum traversal, rotation, checkpoint encoding, archive upload, retention cleanup and report formatting are excluded from the economic coordinator.

## Priority

| Priority | Examples | Saturation rule |
|---|---|---|
| P0 | intents, order/fill/account, Risk, Reservations, Execution, Recovery, Reconciliation, journal | never silently drop; declare critical Recorder health and stop new risk before evidence integrity is lost |
| P1 | RAW/normalized market evidence required for reconstruction | explicit dataset/Book-quality invalidation and controlled degradation |
| P2 | derived features/opportunities/performance detail | versioned sample/coarsen/drop with missingness |
| P3 | verbose diagnostics/formatted logs | shed first, counted |

## Checkpoints

C0 captures a coherent state cursor/version boundary and immutable snapshot handle in bounded time. Serialization, checksum and write happen in C4. Only a complete compatible checkpoint is eligible at restart. Journal plus exchange reconciliation remain truth; a checkpoint is acceleration. An older not-started checkpoint job may be superseded without losing canonical evidence.

## Failure and lifecycle

- Queue pressure produces visible backlog/full/drop/degradation events; no false completeness.
- Writer/compression/archive failure is scoped. Archive unavailability cannot block decisions; P0 durability threat can disable new risk while cancellation/Recovery/Reconciliation remain available.
- Chunk close orders encode → write → verify/checksum → atomic manifest completion. Partial output is never a complete chunk.
- Safe shutdown stops new risk, drains critical records within a bound, finalizes what can be proved and records unresolved/incomplete state. A timeout never claims clean durability.
- Retention cleanup requires manifest/policy checks and cannot delete evidence still required for recovery, validation, incident or configured retention.

## Measurements

Enqueue cost, queue wait/backlog/full time, bytes/records by priority, writer throughput/tails, flush/fsync where used, compression CPU, chunk close time, checkpoint capture versus background write, drop/missingness, disk pressure and EventToDecision/Send interference.
