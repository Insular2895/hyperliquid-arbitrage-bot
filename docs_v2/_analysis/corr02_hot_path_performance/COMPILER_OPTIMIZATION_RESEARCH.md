# Compiler Optimization Research

DOCUMENTATION STATUS: IMPLEMENTATION OPTIONS — NOT SELECTED

| Candidate | Hypothesis | Required controls | Principal risk/status |
|---|---|---|---|
| optimized Cargo release | establish deployable baseline | exact profile/toolchain recorded | baseline only |
| Thin LTO | cross-crate optimization with moderate build cost | same workload/binary provenance | `TO BENCHMARK` |
| Fat LTO | broader whole-program optimization | build time, size, runtime tails | `TO BENCHMARK` |
| fewer/one codegen units | improve optimization opportunity | link time and runtime A/B | `TO BENCHMARK` |
| `panic=abort` | size/code-path change | crash/recovery/test/debug impact | `DESIGN + BENCHMARK GATE` |
| explicit target CPU | exploit deployed CPU features | host fleet compatibility and artifact routing | `DEPLOYMENT DECISION REQUIRED` |
| `target-cpu=native` | build-host-specific code | build host exactly equals allowed runtime CPU | not portable default |
| PGO | use representative branch/layout profiles | clean profiles, representative runs, separate final build | `TO BENCHMARK` |
| post-link/BOLT-style layout | improve instruction locality | supported toolchain and stable symbols | future optional research |
| SIMD/target features | accelerate proven bounded kernel | feature detection/artifact compatibility/exact parity | not general policy |

Cargo/rustc documentation makes these options possible, not automatically beneficial. Every artifact binds compiler version, target triple/CPU/features, profile flags, dependencies and training dataset where applicable. Instrumented PGO binaries and allocation profilers are not production latency comparators. Stripping symbols must preserve required profiling and incident diagnostics.

No Cargo, build, Docker or CI setting is changed by CORR-02.
