# Hot-Path Performance and Work Elimination

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

This specification incorporates human refinements `HDC-007..019`. Formula, Risk, Data, Execution and Recorder authorities remain unchanged.

## Doctrine

Optimize in this order: eliminate unnecessary work; improve locality/data layout; avoid measured allocations/copies; preallocate/reuse safely; specialize exact cases; tune Rust/compiler; remove proven contention; only then review a bounded foreign-language kernel. Semantic parity precedes speed. A faster wrong answer fails.

The critical path is event ingest/normalize, ordered Book commit, affected-route lookup, BBO classification, exact route economics, bounded downstream gates, ordered revalidation/reservation/plan commit and asynchronous evidence handoff. Every interval uses CORR-01 endpoints and separates execution, queue and scheduler delay.

## Memory and work identity

Static/topology, run, market-mutable, per-event, per-opportunity and per-execution lifetimes are distinct. Runtime compact IDs and scratch memory are valid only inside their generation/owner. Stable canonical IDs remain authoritative.

Avoidable steady-state allocation and copying are objectives. Steady state starts after subscriptions, topology, caches/models, queues and representative buffers warm. Required measures include allocation/copy counts and bytes by event/route/leg/opportunity/attempt, capacity growth, temporary/retained footprint and latency tails. Preallocation has a capacity source, safe growth/fallback and observable exhaustion; reuse is reset/poison tested.

## Ownership and concurrency

Book, Account, Inventory, Reservations, Execution, Recovery, Reconciliation and Accounting retain one logical writer. Workers compute on immutable snapshots and return complete input versions; the coordinator discards or revalidates stale proposals.

Lock-free is not a philosophy or requirement. A bounded queue advances only after measured contention, simpler alternatives, topology, capacity, overflow, priority, shutdown, memory ordering, ABA/reclamation and stress/model evidence are resolved. Critical account/fill evidence cannot be dropped. Every atomic has an explicit causality invariant.

## Optimization evidence

Each change passes correctness/golden/property as applicable, deterministic Replay parity, controlled micro/macro performance, Shadow, and capture/economic evaluation when material. Workload, build, host, PMU, instrumentation and cold/warm/steady populations are recorded. See the [profiling protocol](../../_analysis/corr02_hot_path_performance/PROFILING_AND_BOTTLENECK_PROTOCOL.md), [benchmark matrix](../../_analysis/corr02_hot_path_performance/PERFORMANCE_BENCHMARK_MATRIX.md) and [validation matrix](../../_analysis/corr02_hot_path_performance/CORR02_VALIDATION_MATRIX.md).

## Rust and C++

Rust is production baseline. The R0–R11 ladder ends with foreign language only after algorithm/layout/allocation/copy/specialization/synchronization/compiler/PGO work. C++ is neither V1 plan nor baseline. Any future pure bounded candidate passes the [C++ escalation gate](../../_analysis/corr02_hot_path_performance/CXX_ESCALATION_GATE.md) and [FFI contract](../../_analysis/corr02_hot_path_performance/CXX_FFI_SAFETY_CONTRACT.md); all economic state and authority domains are excluded.
