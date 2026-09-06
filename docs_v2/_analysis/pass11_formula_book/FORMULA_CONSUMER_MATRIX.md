# Formula Consumer Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| QF | Primary owner | Runtime/research consumers | Consumer count | Required output evidence |
|---|---|---|---:|---|
| QF-001 | Feature | Graph,Simulator | 3 | Book/FormulaVersion, price unit |
| QF-002 | Feature | Graph,Risk | 3 | BBO/version |
| QF-003 | Feature | Risk | 2 | fraction/bps label |
| QF-004 | Feature | Graph,Sizing | 3 | side,K,BookVersion |
| QF-005 | Feature | Graph,Sizing | 3 | side,K,unit/version |
| QF-006 | Feature | Risk,Sizing | 3 | side,δ,BookVersion |
| QF-007 | Precision | Conversion,Execution | 3 | metadata/formula version |
| QF-008 | Precision | Conversion,Execution | 3 | external rule evidence/version |
| QF-009 | Conversion | Simulator,Execution | 3 | fills/residual/book |
| QF-010 | Conversion | Simulator,Execution | 3 | fills/spend/residual/book |
| QF-011 | Feature | Conversion,Simulator | 3 | fill set/side/book |
| QF-012 | Conversion | Risk,Simulator | 3 | side/reference/unit |
| QF-013 | Conversion | Risk,Simulator | 3 | side/reference/unit |
| QF-014 | Fee | Conversion,Accounting | 3 | account/market/mode/time/version |
| QF-015 | Fee | Conversion,Accounting | 3 | debit asset/economic unit |
| QF-016 | Conversion | Graph,Simulator,Execution,Accounting | 5 | state,fill,residual,asset deltas,versions |
| QF-017 | Graph | Route,Simulator | 3 | route/state/terminal asset |
| QF-018 | Graph | Route,Simulator | 3 | both legs/net intermediate |
| QF-019 | Route | Risk,Sizing | 3 | comparator tuple |
| QF-020 | Route | Risk,Accounting | 3 | comparator tuple/B unit |
| QF-021 | Graph | Route,Simulator | 3 | closed path/leg evidence |
| QF-022 | Route | Risk | 2 | start/end A |
| QF-023 | Route | Accounting,Risk | 3 | A-unit PnL |
| QF-024 | Route | Execution,Simulator | 3 | T/TT comparable outputs |
| QF-025 | Execution | Simulator,Route | 3 | MT/TT comparable outputs |
| QF-026 | Route | Simulator,Sizing | 3 | evaluated points/validity |
| QF-027 | Sizing | Risk,Validation | 3 | grid/threshold/sup result |
| QF-028 | Feature | Participants | 2 | BBO version |
| QF-029 | Feature | Participants | 2 | levels/weight version |
| QF-030 | Feature | Participants | 2 | ordered event pair |
| QF-031 | Feature | Participants | 2 | ordered event pair |
| QF-032 | Feature | Participants | 2 | window/fidelity label |
| QF-033 | Feature | Participants | 2 | levels/weights/window |
| QF-034 | Feature | Participants,Simulator | 3 | BBO/version |
| QF-035 | Feature | Participants | 2 | reference/bps unit |
| QF-036 | Feature | Participants | 2 | series/window/time |
| QF-037 | Feature | Risk | 2 | window/sampling |
| QF-038 | Feature | Risk,Route | 3 | window/scaling |
| QF-039 | Feature | Risk,Atlas | 3 | epsilon/threshold/version |
| QF-040 | Feature | Risk,Sizing | 3 | side/band/book/q |
| QF-041 | Feature | Execution,Risk | 3 | volume source/window |
| QF-042 | Feature | Simulator,Risk | 3 | side/walk/arrival state |
| QF-043 | Feature | Participants,Simulator | 3 | shock/depth/horizon |
| QF-044 | Participants | Simulator,Infra | 3 | event/model/horizon |
| QF-045 | Model | Participants,Simulator | 3 | artifact/features/bin |
| QF-046 | Participants | Simulator | 2 | hazard vector/index |
| QF-047 | Participants | Infra | 2 | horizon/censor flag |
| QF-048 | Simulator | Infra,Quant | 3 | latency/survival versions |
| QF-049 | Model | Participants,Simulator,Risk | 4 | artifact/support/horizon |
| QF-050 | Model | Participants,Risk,Sizing | 4 | threshold/artifact/support |
| QF-051 | Model | Maker,Execution,Simulator | 4 | order/features/artifact |
| QF-052 | Maker | Execution,Simulator | 3 | source survival identity |
| QF-053 | Maker | Execution,Simulator | 3 | tail/censor convention |
| QF-054 | Maker | Execution,Simulator | 3 | fill/side/horizon |
| QF-055 | Maker | Execution,Simulator | 3 | fill/side/horizon |
| QF-056 | Simulator | Risk,Accounting | 3 | scenario/probability/PnL units |
| QF-057 | Simulator | Execution,Risk | 3 | F/P/R/X partition |
| QF-058 | Simulator | Execution,Recovery | 3 | fill distribution/cost ownership |
| QF-059 | Simulator | Risk,Validation | 3 | outcome set/N |
| QF-060 | Risk | Simulator,Accounting | 3 | PnL identity/numeraire |
| QF-061 | Risk | Simulator,Validation | 3 | alpha/distribution/estimator |
| QF-062 | Risk | Simulator,Validation | 3 | alpha/tail/estimator |
| QF-063 | Risk | Sizing,Simulator | 3 | component ownership/parameters |
| QF-064 | Inventory | Risk,Sizing | 3 | asset/target/band |
| QF-065 | Inventory | Risk,Sizing | 3 | kappa/config/candidate |
| QF-066 | Risk | Inventory,Execution | 3 | projected state/limits |
| QF-067 | Inventory | Accounting,Risk | 3 | ordered trade deltas |
| QF-068 | Inventory | Bridge,Recovery,Risk | 4 | valuation/executable exit |
| QF-069 | Inventory | Risk,Sizing | 3 | three component ledger |
| QF-070 | Bridge | Inventory,Accounting | 3 | path/net end/risk |
| QF-071 | Bridge | Capital | 2 | costs/cycle EV |
| QF-072 | Capital | Bridge,Risk | 3 | alternatives/threshold state |
| QF-073 | Inventory | Sizing,Execution | 3 | reconciled balance/reservation |
| QF-074 | Graph | Sizing,Execution | 3 | book/capacity/reservation |
| QF-075 | Sizing | Risk,Execution | 3 | candidates/gates/objective |
| QF-076 | Validation | Risk,Sizing | 3 | exact evidence tuple |
| QF-077 | Sizing | Validation | 2 | grid/refinement/tie |
| QF-078 | Portfolio | Risk,Sizing | 3 | constraint matrix/solution |
| QF-079 | Recovery | Risk,Execution | 3 | current state/action outcomes |
| QF-080 | Recovery | Accounting,Risk | 3 | before/after valuation |
| QF-081 | Model | Participants,Simulator,Atlas | 4 | markets/shock/horizon/artifact |
| QF-082 | Participants | Simulator | 2 | E0/Eh/horizon |
| QF-083 | Model | Participants,Simulator,Risk | 4 | event/time/artifact |
| QF-084 | Infra | Ops,Simulator | 3 | stage boundaries/clock |
| QF-085 | Infra | Simulator,Participants | 3 | server latency/survival |
| QF-086 | Infra | Accounting,Validation | 3 | comparison cohort |
| QF-087 | Infra | Accounting | 2 | cost scope/horizon |
| QF-088 | Infra | Accounting,Validation | 3 | aligned deltas |
| QF-089 | Infra | Accounting | 2 | positive denominator |
| QF-090 | Accounting | Infra,Validation | 3 | disjoint ledger/period |
| QF-091 | Infra | Risk,Validation | 3 | LCB/alpha/SF/evidence |
| QF-092 | Infra | Accounting,Ops | 3 | cost denominator/scope |
| QF-093 | Accounting | Infra,Ops | 3 | eligible cohort/sums |
| QF-094 | Participants | Validation,Ops | 3 | cohort/censor/horizon |
| QF-095 | Model | Validation | 2 | aligned p/y/sample |
| QF-096 | Model | Validation | 2 | p/y/epsilon/sample |
| QF-097 | Model | Simulator,Accounting | 3 | outcome/prediction alignment |
| QF-098 | Model | Simulator,Execution | 3 | side/reference/unit |
| QF-099 | Model | Maker,Validation | 3 | bucket/event/model |
| QF-100 | Model | Accounting,Validation | 3 | like-for-like runs |
| QF-101 | Model | Infra,Validation,Operations | 4 | experiment/cost attribution |
| QF-102 | Model | Risk,Simulator | 3 | aligned ensemble |
| QF-103 | Model | Risk,Simulator | 3 | support/estimator/artifact |
| QF-104 | Simulator | Risk,Validation | 3 | six gate results/rules |
| QF-105 | Capital | Inventory,Accounting | 3 | rate evidence/horizon |
| QF-106 | Accounting | Risk,Ops | 3 | component ledger/period |
| QF-107 | Accounting | Inventory,Risk | 3 | valuation/external flows |
| QF-108 | Accounting | Risk,Ops | 3 | attribution/global reconciliation |
| QF-109 | Risk | Accounting,Ops | 3 | ordered equity series |
| QF-110 | Risk | Capital,Validation | 3 | interval/drawdown series |

All 110 QFs have an owner and at least one consumer. Consumer count is the number of named modules in the row including the primary owner; it is an audit locator, not an authorization count.
