# Research Knowledge Base

STATUS: STRUCTURE SPECIFIED / ZERO RECORDED RESEARCH ARTIFACTS / GENERATION NOT IMPLEMENTED

This directory is the future human-readable and machine-indexable evidence registry. Creating this structure does not activate Strategy Discovery, Monte Carlo, Champion/Challenger, drift automation or Live learning.

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
