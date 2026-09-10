# Async Concurrency and Ordered Commit

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Constitutional rule

The V1 runtime remains one client OCI container and one main Rust modular-monolith process. It uses asynchronous I/O and may use bounded parallel pure computation, but has exactly one logical ordered canonical mutation authority:

> **parallel to calculate; ordered to decide; single-writer to commit.**

The concurrency classes are `C0 ORDERED_CANONICAL_COMMIT`, `C1 INLINE_BOUNDED_HOT_PATH`, `C2 SNAPSHOT_PARALLEL_COMPUTE`, `C3 ASYNC_EXTERNAL_EFFECT`, `C4 BACKGROUND_RUNTIME` and `C5 OFFLINE_RESEARCH`. These are responsibility classes, not mandated implementation types.

## Ownership

Only C0 owners mutate canonical Book, Account, Fill, Inventory, Reservation, Risk, Execution, Recovery, Reconciliation and Accounting state. C1 returns bounded inline values. C2 returns proposals with full input versions/generation/deadline. C3 returns normalized observations. C4 returns durability/health/control evidence. C5 returns research artifacts through existing validation/promotion gates.

Worker or I/O completion is never commit. C0 rejects or revalidates stale proposals, uses deterministic ordering independent of completion time, runs current final Risk and performs ordered atomic Reservation before an immutable plan/intent can request an effect.

## Initial baseline

- persistent market/account/metadata and order/cancel/query network work is async;
- canonical reducers, `pair_to_routes`, BBO, FastL1, full-L2 QF-016 and a small q-grid run inline initially;
- rolling features/health are maintained incrementally where exact;
- advanced features, Participant inference, F2/F3 and large route/q/allocation computation are bounded C2 candidates;
- final sizing/allocation, Risk, Reservation and plan commit stay C0;
- local signing is bounded inline initially;
- Recorder disk, compression, checksums, checkpoint serialization, archive and metrics formatting/export run C4;
- Replay campaigns, F4/Monte Carlo, training, discovery, parameter search and comparative VPS analysis run C5 outside Live resources.

Additional parallelism requires profiling, exact semantic parity, local+queue+end-to-end latency, scheduler/stale/deadline evidence, Replay, Shadow and capture/economic evidence where material. On a small two-vCPU-class VPS, avoid unnecessary oversubscription and scheduler/queue/cache overhead; exact pool sizes and capacities remain calibrated.

## Ordering, legs and external effects

TT/TTT later legs use only the actual unique prior fill committed through Account/Fill/Inventory/Reservation reducers. Pure preparation may occur early, but executable quantity, final Risk, signing and send wait for actual fill/current state. Predicted fill never drives execution.

Submit, cancel, status and reconciliation HTTP/WS calls are C3 effects and never block the coordinator. ACK is not fill; cancel requested is not canceled; ambiguous transmission becomes `UNKNOWN` and no blind retry occurs. Responses re-enter through canonical ordered events.

## Boundedness and liveness

Every queue and task population is bounded. There is no per-event unbounded spawn and no indefinite hot-path await. Derived work may be canceled/superseded, but correctness relies on version checks rather than successful cancellation. Canonical source events are not causally dropped; a market gap invalidates/resyncs and account ambiguity disables new risk/reconciles. Background degradation is explicit and scoped by evidence criticality.

## Route decision policy

Both `BATCH_SELECT` and deterministic `EARLY_COMMIT` are safe candidates when they obey current-version, bounded-deadline, capacity, Risk and Reservation rules. Neither is selected canonically yet. Replay + Shadow must compare policy-versioned end-to-end, scheduler, capture and economic results. First-worker-wins is forbidden; an adaptive policy is Research only.

## Authoritative evidence

- [Async architecture analysis](../../_analysis/async_concurrency_architecture/BASELINE_AND_SCOPE.md)
- [Function matrix](../../_analysis/async_concurrency_architecture/FUNCTION_CONCURRENCY_MATRIX.md)
- [Queue/backpressure matrix](../../_analysis/async_concurrency_architecture/ASYNC_QUEUE_AND_BACKPRESSURE_MATRIX.md)
- [Stale result contract](../../_analysis/async_concurrency_architecture/STALE_RESULT_AND_VERSIONING_CONTRACT.md)
- [Replay determinism](../../_analysis/async_concurrency_architecture/CONCURRENCY_REPLAY_DETERMINISM_CONTRACT.md)

This contract changes no QF, Risk gate, Execution transition, Recovery/Reconciliation behavior, accounting term, `Q_validated` meaning or public-feed/node boundary. It authorizes no implementation.
