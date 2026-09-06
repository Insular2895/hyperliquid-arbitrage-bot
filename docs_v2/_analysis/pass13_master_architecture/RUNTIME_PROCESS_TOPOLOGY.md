# Runtime Process Topology

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Initial topology

```text
CLIENT HOST
└── one OCI trading container
    └── one main Rust process (modular Core)
        ├── feed/account/metadata I/O tasks
        ├── ordered event coordinator and state reducers
        ├── bounded Book/Graph/Formula/Opportunity/Risk/Execution work
        ├── bounded inference/simulation workers with version checks
        ├── non-blocking Recorder queue + background writer/compression
        ├── health/metrics and local admin interface
        └── mode-specific execution transport

SEPARATE/OFFLINE
├── Python research/training/calibration/report jobs
├── historical Replay/benchmark jobs when isolated from production load
└── archive/artifact/release systems
```

## Rules

- Logical components are not mandated crates, threads or microservices.
- One ordered coordinator is the economic commit boundary; workers cannot race mutations.
- Async tasks have bounded queues/budgets and failure/health reporting.
- Replay may run the same Core in a separate process/context; it never shares mutable Live state.
- Python does not sign, mutate Live state or perform synchronous production inference.
- C++ and lock-free/zero-copy specialization require profiling plus robust economics.
- Redis, Postgres, Kafka, Kubernetes and remote control services are not baseline hot-path dependencies.

Exact Tokio channel types, task count, CPU pinning and scheduling are implementation/calibration decisions, intentionally not frozen here.
