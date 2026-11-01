# Research Knowledge Base

STATUS: STRUCTURE SPECIFIED / ZERO RECORDED RESEARCH ARTIFACTS / GENERATION NOT IMPLEMENTED

This directory is the future human-readable and machine-indexable evidence registry. Creating this structure does not activate Strategy Discovery, Monte Carlo, Champion/Challenger, drift automation or Live learning.

It consumes the canonical [Strategy Research registry contract](../deep-specs/strategy-research/09_REPORTING_AND_KNOWLEDGE_BASE.md)
and [orchestration boundary](../deep-specs/strategy-research/11_RESEARCH_ORCHESTRATION_AND_WORKERS.md).
There are still zero real hypotheses, experiments, strategies or registry runs in this directory.

| Family | Identity authority | Index | Initial count |
|---|---|---|---:|
| hypotheses | documentary `HYP-*` | [Hypotheses](HYPOTHESIS_INDEX.md) | 0 |
| experiments | documentary `EXP-*` | [Experiments](EXPERIMENT_INDEX.md) | 0 |
| benchmarks | documentary `BENCH-*` | [Benchmarks](BENCHMARK_INDEX.md) | 0 |
| strategies | documentary `STRAT-*` | [Strategies](STRATEGY_INDEX.md) | 0 |
| architecture decisions | documentary `ADR-*` | [Decisions](DECISION_INDEX.md) | 0 new records |
| incidents/post/rel. | canonical runtime IDs plus `POST-*`/`REL-*` reports | [Operations](OPERATIONS_REPORT_INDEX.md) | 0 new records |
| external facts | existing `EXT-*` register | [External facts](EXTERNAL_FACT_INDEX.md) | linked, not duplicated |
| datasets/runs | canonical `DatasetId`/`RunId` | [Datasets and runs](DATASET_RUN_INDEX.md) | 0 registry rows |

IDs are never reused. Records are immutable or explicitly superseded. Failed, negative, aborted, invalid, censored and inconclusive work stays indexed. Deletion from an index requires an integrity incident, not an unfavorable result.

Exact duplicates, manual reruns, compute retries, timeouts and results later invalidated by
data-quality findings also remain linked. Job/attempt identifiers are orchestration metadata;
canonical `DatasetId`, `RunId`, `EvidenceId` and `IncidentId` remain the runtime identities.
`StrategyFamily`, Configuration and `StrategyVersion` are fields/versions under the existing
identity system, not new ID namespaces.

## Registry invariants

- An `EXP-*` version freezes protocol, domains, budget, splits, selection/region rules, T2 and final
  holdout policy before any data-dependent T0 cell.
- Each run binds exact Dataset/build/config/dependency versions, scenario/fidelity/tier and seed.
- Compute state is distinct from scientific validity and economic disposition.
- Worker completion order never determines result order or selection.
- Machine facts/hashes are append-only; human/AI interpretation is separate and cannot overwrite.
- Every aggregate/report/dashboard value drills down to canonical IDs and immutable artifacts.
- Research statuses and positive results grant no Risk, q, capital, execution or Live permission.
- Empty indexes retain their zero-artifact status; examples live only in templates/specifications.

Templates:

- [Experiment report](templates/EXPERIMENT_REPORT_TEMPLATE.md)
- [Benchmark report](templates/BENCHMARK_REPORT_TEMPLATE.md)
- [Research synthesis](templates/RESEARCH_REPORT_TEMPLATE.md)
- [Monte Carlo report](templates/MONTE_CARLO_REPORT_TEMPLATE.md)
- [ADR](templates/ADR_TEMPLATE.md)
- [Incident report](templates/INCIDENT_REPORT_TEMPLATE.md)
- [Postmortem](templates/POSTMORTEM_REPORT_TEMPLATE.md)
- [Release report](templates/RELEASE_REPORT_TEMPLATE.md)

The canonical behavior is defined in [Reporting and Knowledge Base](../deep-specs/strategy-research/09_REPORTING_AND_KNOWLEDGE_BASE.md).

Final schemas, storage/generator and any Dashboard remain `HUMAN_DECISION_REQUIRED` and
unimplemented.
