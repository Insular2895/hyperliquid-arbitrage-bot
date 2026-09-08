# Rust Performance and C++ Escalation

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

Infrastructure supplies reproducible measurement, not economic authority. Real Hot-Path CPU benchmarks bind CORR-01 timing stages to CORR-02 component profiles and record route/evaluation amplification, BBO disposition quality, full/fast L2 work, stale work, queue wait, allocations/copies, footprint, cycles/instructions/IPC, cache/branch misses, context switches, migrations, scheduler delay and faults.

Comparisons hold workload, commit, config, formula/models/routes, compiler and host constant except the declared variable. They separate cold, warm and steady state and report P50/P95/P99/P99.9, max, dispersion, repetitions and counter coverage. Profilers and allocation instrumentation declare their overhead.

Rust compiler candidates—release profiles, LTO, codegen units, panic strategy, target CPU, PGO, possible post-link layout and SIMD—are experiments. `target-cpu=native` creates a build-host compatibility constraint for client artifacts. PGO uses representative training and held-out workloads; an instrumented binary is not the production comparator.

C++ is not baseline. Only a measured irreducible pure bounded kernel may reach a 12-condition escalation review after Rust optimization and net FFI overhead measurement. Risk, Inventory, Reservations, Execution, Recovery, Reconciliation, Accounting, nonce, signer and capability authority stay in Rust. See [research](../../_analysis/corr02_hot_path_performance/EXTERNAL_PERFORMANCE_RESEARCH.md), [Rust ladder](../../_analysis/corr02_hot_path_performance/RUST_OPTIMIZATION_LADDER.md) and [C++ gate](../../_analysis/corr02_hot_path_performance/CXX_ESCALATION_GATE.md).

CORR-04 extends the same doctrine to host/network work: measure queue wait/kernel cost first; affinity, scheduler, IRQ/RSS/RPS/RFS and socket settings are controlled treatments. AF_XDP and DPDK do not themselves provide the current TCP/TLS/WebSocket path; F-Stack is more protocol-relevant but still must prove Rust/TLS/client/security/operations integration. All remain Research behind simpler fixes, semantic parity, end-to-end capture/economic evidence and rollback.
