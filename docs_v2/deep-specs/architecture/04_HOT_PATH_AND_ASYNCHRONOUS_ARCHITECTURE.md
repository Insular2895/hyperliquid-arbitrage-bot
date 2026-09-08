# 04 — Hot Path and Asynchronous Architecture

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Compute classes

| Class | Examples | Contract |
|---|---|---|
| Hot path | normalize accepted event, Book reduce, affected routes, exact formulas, bounded inference, sizing/Risk/reservation/plan | In-memory, versioned, bounded and instrumented |
| Near-line fast async | Recorder enqueue/write, derived snapshots, slow Atlas aggregates, health aggregation | Bounded queues; cannot mutate decision state without coordinator/version gate |
| Background | compression, archive, Replay jobs, infra analysis, reports, diagnostics | Backpressure and failure visible; no hot-path dependency |
| Offline training/research | datasets, Python training, calibration, Challenger analysis | Point-in-time, reproducible, no Live shared-memory mutation |
| Control plane | config, capability promotion, release, license, operator action | Atomic/versioned input; safety available during outage |

No synchronous disk/database/object storage/license/admin call, model training, large Monte Carlo, whole-universe graph traversal, unbounded allocation/loop or hidden network dependency belongs in the trading path. `pair_to_routes`, precomputation, incremental state, activated HWC scope and bounded q/model budgets control work.

Lock-free/zero-copy, affinity, kernel tuning and C++ are profiling/economic candidates, not universal architecture requirements. Latency targets remain benchmark/calibration hypotheses. Details: [Hot Path](../../_analysis/pass13_master_architecture/HOT_PATH_ARCHITECTURE.md) and [Async Architecture](../../_analysis/pass13_master_architecture/ASYNC_AND_BACKGROUND_ARCHITECTURE.md).

CORR-04 adds a Research-only speculative lane. It may prepare pure structural/economic work off canonical state ownership, but the canonical path never waits for it and reuses economic output only after exact canonical fingerprint/version equality and fresh-result parity. Public and challenger feeds cannot concurrently own `BookState`; feed fusion remains outside the architecture.
