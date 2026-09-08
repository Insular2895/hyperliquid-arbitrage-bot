# Infrastructure Promotion and Demotion Gate

`STATUS: SPECIFIED — NO CANDIDATE PROMOTED`

| Gate | Requirement |
|---|---|
| `P1` | canonical correctness and semantic parity |
| `P2` | valid clocks, alignment, population and comparable treatment |
| `P3` | reproducible technical end-to-end improvement |
| `P4` | no continuity, gap, reconnect or availability regression |
| `P5` | no Risk, ownership, evidence, deployment or security regression |
| `P6` | measured capture effect or defensible `RecoverablePnL` |
| `P7` | positive incremental net value under uncertainty using QF-086–QF-091 authority |
| `P8` | operable, observable, patchable and supportable |
| `P9` | tested rollback with state rebuild/readiness/reconciliation |

Promotion is scoped in the existing CapabilityManifest/maturity model and requires explicit approval. Lower RTT alone fails. Demotion is symmetric and may result from vanished value, gaps, lag, resource contention, drift, incident, security issue, unsupported software or invalid evidence. A rollback restores software/feed profile but never rewinds exchange/account truth.
