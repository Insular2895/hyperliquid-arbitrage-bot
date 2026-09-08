# Profiling and Bottleneck Protocol

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

## Levels

1. **Component:** lookup, BBO classifier, full/fast NetConvert, dedup, allocation/copy and queue primitives.
2. **End-to-end local:** ingest through ordered decision/plan boundary using CORR-01 timing points.
3. **Capture/economics:** comparable Replay/Shadow/Micro-live cohorts, funnel movement and realized economic labels.

## Controlled run contract

Hold commit, resolved config, dataset/order, formulas, models, graph/routes, compiler/toolchain, host/CPU mode and measurement endpoints constant unless one is the declared variable. Record kernel/PMU, image/build, affinity/noise state, instrumentation, sample count, repetitions and exclusions.

Separate cold, warm-up and steady state. Workloads cover quiet/normal/burst feed, low/high route degree, direct/OWA/triangle mix, HOT/WARM/COLD activation, shallow/deep/volatile books, Recorder pressure, feature/model on/off, two/three-leg economics and fault/stale-result cases.

Report count, P50, P95, P99, P99.9, max, dispersion and replicate variation. Attribute cycles, instructions/IPC, cache references/misses, branches/misses, context switches, migrations, scheduler delay and page faults where supported. Record counter multiplexing/coverage. Allocation/copy profiling is a declared special mode.

## Decision rule

`baseline → profile → identify hotspot → hypothesis → safe change → correctness parity → microbenchmark → Replay → Shadow → capture comparison → economic validation if material`.

No fixed universal latency or percentage threshold is invented. Regression guardrails are calibrated from stable distributions. A microbenchmark win without representative end-to-end improvement and semantic parity is not promotable.
