# Infrastructure Deep Specs

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

This directory is the normative detail layer for [13 — Infrastructure](../../13_INFRASTRUCTURE.md). Closure authorities still prevail where a topic belongs to the Formula Book, Risk Constitution, Data Contracts, Deployment, Validation, Recorder or Execution domains.

| Document | Responsibility |
|---|---|
| [01 — Baseline and Deployment Profiles](01_BASELINE_AND_DEPLOYMENT_PROFILES.md) | Initial topology, Tokyo-first, provider-agnostic boundaries, resource roles and client profiles. |
| [02 — Provider Candidates](02_PROVIDER_CANDIDATES.md) | Historical provider snapshots, benchmark roles, waves and revalidation status. |
| [03 — Benchmark Protocol](03_BENCHMARK_PROTOCOL.md) | Comparable-run contract, phases and all twelve benchmarks. |
| [04 — Clock and Measurement Contract](04_CLOCK_AND_MEASUREMENT_CONTRACT.md) | Monotonic/wall-clock semantics, uncertainty and cross-machine validity. |
| [05 — Infrastructure Economics and ROI](05_INFRA_ECONOMICS_AND_ROI.md) | QF-084–QF-093, InfraLostPnL, upgrade and downgrade gates. |
| [06 — Node, Feed and Scale Gates](06_NODE_FEED_AND_SCALE_GATES.md) | Public-feed-first, node compatibility and evidence-gated escalation. |
| [07 — Operations, Resilience and Client Diagnostics](07_OPERATIONS_RESILIENCE_AND_CLIENT_DIAGNOSTICS.md) | Health outputs, rolling metrics, alerts, recovery, standby and client benchmark. |

## Reading order

Start with the master, then Baseline. Provider Candidates and Benchmark Protocol establish selection evidence. Clock is mandatory before interpreting relative network results. Economics governs production choice. Node/Feed and Operations cover future escalation and continuous safety.

## Requirement evidence

The per-ID PASS 01 review is maintained in [INFRA_REQUIREMENT_LEDGER.md](../../_analysis/pass01_infrastructure/INFRA_REQUIREMENT_LEDGER.md). Deep specs synthesize those requirements; they do not erase cross-domain destinations or historical statuses.
