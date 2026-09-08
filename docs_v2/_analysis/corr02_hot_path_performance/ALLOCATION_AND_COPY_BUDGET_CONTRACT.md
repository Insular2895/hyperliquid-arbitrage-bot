# Allocation and Copy Budget Contract

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

Steady state begins only after process startup, subscriptions, initial topology publication, caches/model artifacts, queues/pools and representative buffers have warmed. Cold start, topology change, recovery and stress remain separate populations.

## Required measures

- allocations and allocated bytes per received event;
- allocations/bytes per affected route and per exact L2 leg;
- allocations/bytes per Opportunity and execution attempt;
- capacity growth/reallocation count and peak temporary bytes;
- explicit clone/copy count and bytes by boundary;
- retained footprint and high-water mark;
- P50/P95/P99/P99.9 component latency with instrumentation state declared.

Measurements state allocator, instrumentation method, sampling, build, host, workload and overhead. Special allocation instrumentation may perturb timing; paired instrumented/non-instrumented runs separate attribution from production latency.

Exact targets remain calibrated. “Zero avoidable steady-state allocation” is a hypothesis objective. A budget breach is evidence for investigation, not permission to truncate data, skip validation, hide telemetry loss or use unsafe memory.
