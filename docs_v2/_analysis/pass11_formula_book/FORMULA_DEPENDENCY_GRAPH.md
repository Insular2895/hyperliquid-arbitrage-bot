# Formula Dependency Graph

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Edges mean the downstream formula consumes the upstream mathematical result or its exact contract. Raw inputs are listed as `root`. Model/evidence dependencies remain versioned even when no QF edge exists.

| QF | Direct QF dependencies | External/non-QF dependency |
|---|---|---|
| QF-001 | root | coherent BBO |
| QF-002 | root | coherent BBO |
| QF-003 | 001,002 | bps scale |
| QF-004 | root | ordered book levels |
| QF-005 | 004 concept | price levels |
| QF-006 | 001,005 | calibrated band |
| QF-007 | root | size metadata |
| QF-008 | root | exchange price rule/metadata |
| QF-009 | 004/005 evidence | bid book/protection |
| QF-010 | 004/005 evidence | ask book/protection |
| QF-011 | 009 or 010 fills | nonzero fill |
| QF-012 | 010,011 | BUY BBO reference |
| QF-013 | 009,011 | SELL BBO reference |
| QF-014 | root | point-in-time fee source |
| QF-015 | 014 | notional/debit asset |
| QF-016 | 007–010,014,015 | minimums/state |
| QF-017 | 016 | direct route |
| QF-018 | 016 | route continuity |
| QF-019 | 017,018 | comparable state |
| QF-020 | 017,018 | comparable state |
| QF-021 | 016 | closed path |
| QF-022 | 021 | positive input |
| QF-023 | 021 | — |
| QF-024 | 017,018 | T/TT mode semantics |
| QF-025 | 018 | MT/TT mode semantics |
| QF-026 | 019/022/024/025 chosen edge | repeated exact simulation |
| QF-027 | 026 | calibrated threshold |
| QF-028 | root | BBO sizes |
| QF-029 | 028 concept | level weights |
| QF-030 | root | ordered bid events |
| QF-031 | root | ordered ask events |
| QF-032 | 030,031 | window |
| QF-033 | 032 | calibrated weights |
| QF-034 | 001,028 inputs | BBO prices/sizes |
| QF-035 | 001,034 | — |
| QF-036 | root | named price series |
| QF-037 | 036 | sampling window |
| QF-038 | 037 | — |
| QF-039 | 036,038 | epsilon/threshold |
| QF-040 | 005,006 | proposal notional |
| QF-041 | root | executed-volume window |
| QF-042 | 009–011 | arrival mid/side |
| QF-043 | 004/005 depth convention | shock time series |
| QF-044 | root | edge-death event/model |
| QF-045 | root | learned artifact/at-risk data |
| QF-046 | 045 | exact bin indexing |
| QF-047 | 044 or 046 | model horizon |
| QF-048 | 044/046 | latency distribution |
| QF-049 | 044/048 context | learned edge distribution |
| QF-050 | 049 distribution | economic threshold |
| QF-051 | root | maker-fill artifact |
| QF-052 | 051 | — |
| QF-053 | 051 | integration/tail support |
| QF-054 | root | BUY fill/future mid |
| QF-055 | root | SELL fill/future mid |
| QF-056 | root | scenario distribution |
| QF-057 | 056 structure | F/P/R/X outcomes |
| QF-058 | 051–055,056 | leg-2 value/cost ownership |
| QF-059 | 056/057 outcomes | sample |
| QF-060 | root | canonical PnL |
| QF-061 | 060 | quantile convention |
| QF-062 | 060,061 | tail estimator |
| QF-063 | 057,065,069,102-derived penalty | calibrated coefficients |
| QF-064 | root | target/band |
| QF-065 | 064 | calibrated kappa |
| QF-066 | root | projected inventory/hard limits |
| QF-067 | root | reconciled trades |
| QF-068 | 016 | valuation policy |
| QF-069 | 068,105 | expected risk component |
| QF-070 | 016 | bridge path/risk cost |
| QF-071 | 068,070 | cycle EV |
| QF-072 | 068,070 | destination/stay EV; relocation risk |
| QF-073 | root | account/reservation state |
| QF-074 | root | book/reservation state |
| QF-075 | 040,059,062,063,066,073,074,104 | size candidates |
| QF-076 | 066,073–075 | evidence/capability scope |
| QF-077 | 075,076 | grid/refinement config |
| QF-078 | 063,073–076 | shared constraint matrix |
| QF-079 | 056 structure | current exposure/action outcomes |
| QF-080 | 079 | valuation boundary |
| QF-081 | root | cross-market learned artifact |
| QF-082 | 081 evidence | initial/future edge |
| QF-083 | 044 event concept | learned hazard artifact |
| QF-084 | root | instrumentation boundaries |
| QF-085 | 044/048,084 | server latency distribution |
| QF-086 | root | like-for-like experiment |
| QF-087 | root | cost accounting scope |
| QF-088 | 086,087 | — |
| QF-089 | 086,087 | positive incremental cost |
| QF-090 | root | disjoint accounting components |
| QF-091 | 086,087 | calibrated LCB/alpha/SF |
| QF-092 | 090 | positive infra cost |
| QF-093 | root | aligned eligible PnL cohort |
| QF-094 | root | censoring/eligible cohort |
| QF-095 | root | aligned probability labels |
| QF-096 | root | aligned labels/epsilon |
| QF-097 | root | matured actual/prediction |
| QF-098 | 012/013 sign contract | matured actual/prediction |
| QF-099 | 051/052 event definition | bucket calibration cohort |
| QF-100 | 090 | comparable model/baseline run |
| QF-101 | 084,100 evidence | latency/operational attribution |
| QF-102 | root | aligned model ensemble |
| QF-103 | root | model support/estimator |
| QF-104 | 094,102,103 | fidelity/freshness/latency gates |
| QF-105 | root | empirical opportunity rate |
| QF-106 | 090,107,108 accounting contracts | disjoint PnL ledger |
| QF-107 | root | inventory/valuation/external flows |
| QF-108 | 080,107 | disjoint attribution ledger |
| QF-109 | 106/108-derived equity | ordered series |
| QF-110 | 109 | nonempty interval |

No cycles exist in the formula graph. Candidate-size evaluation prevents a false QF-063↔QF-075 cycle: projected inventory/penalties are pure functions of candidate `q`, and only afterward does QF-075 choose `q*`.
