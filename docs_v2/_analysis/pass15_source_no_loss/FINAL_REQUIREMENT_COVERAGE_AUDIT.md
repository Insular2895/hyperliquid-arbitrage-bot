# Final Requirement Coverage Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Population and final target status

| Status | PASS00 atomic | Overlay | Total requirements |
|---|---:|---:|---:|
| LOCKED | 1,589 | 10 | 1,599 |
| CALIBRATED | 60 | 0 | 60 |
| LEARNED | 6 | 0 | 6 |
| RESEARCH | 636 | 3 | 639 |
| FUTURE | 116 | 0 | 116 |
| SOURCE_SNAPSHOT | 9 | 0 | 9 |
| EXTERNAL_REVALIDATION | 116 | 0 | 116 |
| OPEN | 11 | 0 | 11 |
| SUPERSEDED | 2 | 0 | 2 |
| REJECTED | 32 | 0 | 32 |
| **Total** | **2,577** | **13** | **2,590** |

These are the current statuses in `DOCUMENT_TARGET_MAP.md`, joined without changing stable PASS00 item IDs. Deeper domain-pass reviewed overlays still control where keyword heuristics were corrected, and nine SRC-008 provider rows remain `SOURCE_SNAPSHOT` through the PASS01 overlay.

## Requirements by source

| Source population | Requirements |
|---|---:|
| SRC-001 | 145 |
| SRC-002 | 198 |
| SRC-003 | 199 |
| SRC-004 | 279 |
| SRC-005 | 599 |
| SRC-006 | 629 |
| SRC-007 | 310 |
| SRC-008 | 218 |
| MULTI canonical derivations | 13 |
| **Total** | **2,590** |

## Requirements by primary domain

| Primary domain | Requirements |
|---|---:|
| ACCOUNTING | 67 |
| ARCH | 97 |
| BENCHMARK | 21 |
| BRIDGE | 12 |
| CAPITAL | 22 |
| CLIENT | 29 |
| CLOCK | 15 |
| CROSS_EXCHANGE | 6 |
| CROSS_MARKET | 16 |
| DATA | 319 |
| DEPLOYMENT | 220 |
| DETERMINISM | 16 |
| EXECUTION | 341 |
| FORMULA | 153 |
| FUTURE | 13 |
| GRAPH | 14 |
| HOT_WARM_COLD | 31 |
| INFRA | 103 |
| INVENTORY | 24 |
| LICENSE | 7 |
| LIQUIDITY_RESPONSE | 10 |
| MAKER_MODEL | 2 |
| MARKET_ATLAS | 3 |
| MICROSTRUCTURE | 29 |
| NODE | 3 |
| OPERATIONS | 23 |
| OWA | 9 |
| PARTICIPANTS | 27 |
| PORTFOLIO | 4 |
| PRODUCT | 23 |
| QUANT | 34 |
| RECONCILIATION | 1 |
| RECORDER | 11 |
| RECOVERY | 24 |
| REPLAY | 21 |
| RESEARCH | 16 |
| RISK | 332 |
| ROUTING | 39 |
| SECURITY | 21 |
| SIMULATOR | 12 |
| SIZING | 7 |
| SLICING | 7 |
| SURVIVAL | 23 |
| TRIANGLE | 5 |
| VALIDATION | 378 |
| **Total** | **2,590** |

## Destination audit

| Logical PASS00 target | Requirements | Physical canonical/trace destination | Deep-spec or trace destination | Gaps |
|---|---:|---|---|---:|
| Accounting | 67 | `docs_v2/08_INVENTORY_AND_CAPITAL.md; docs_v2/04_FORMULA_BOOK.md` | `docs_v2/deep-specs/inventory-capital/10_ECONOMIC_PNL_ACCOUNTING_AND_CAPITAL_EFFICIENCY.md; docs_v2/deep-specs/formulas/10_QF105_QF110_CAPITAL_ACCOUNTING_AND_DRAWDOWN.md` | 0 |
| Counterfactual Simulator | 12 | `docs_v2/07_COUNTERFACTUAL_SIMULATOR.md` | `docs_v2/deep-specs/simulator/README.md` | 0 |
| Data Contracts | 350 | `docs_v2/11_DATA_CONTRACTS.md` | `docs_v2/deep-specs/data/README.md` | 0 |
| Data and Replay | 1 | `docs_v2/11_DATA_CONTRACTS.md; docs_v2/12_RECORDER_AND_REPLAY.md` | `docs_v2/deep-specs/data/README.md; docs_v2/deep-specs/recorder-replay/README.md` | 0 |
| Deployment and Docker | 220 | `docs_v2/14_DEPLOYMENT_AND_DOCKER.md` | `docs_v2/deep-specs/deployment-security/README.md` | 0 |
| Deployment and Security | 28 | `docs_v2/14_DEPLOYMENT_AND_DOCKER.md` | `docs_v2/deep-specs/deployment-security/README.md` | 0 |
| Execution State Machine | 373 | `docs_v2/10_EXECUTION_STATE_MACHINE.md` | `docs_v2/deep-specs/execution/README.md` | 0 |
| Formula Book | 187 | `docs_v2/04_FORMULA_BOOK.md` | `docs_v2/deep-specs/formulas/README.md` | 0 |
| Future Architecture | 19 | `docs_v2/00_MASTER_ARCHITECTURE.md` | `docs_v2/deep-specs/architecture/README.md` | 0 |
| Infrastructure Master | 127 | `docs_v2/13_INFRASTRUCTURE.md` | `docs_v2/deep-specs/infrastructure/README.md` | 0 |
| Inventory and Capital | 69 | `docs_v2/08_INVENTORY_AND_CAPITAL.md` | `docs_v2/deep-specs/inventory-capital/README.md` | 0 |
| Market Graph and Routes | 70 | `docs_v2/03_MARKET_GRAPH_AND_ROUTES.md` | `docs_v2/deep-specs/market-graph/README.md` | 0 |
| Market Microstructure | 29 | `docs_v2/05_MARKET_MICROSTRUCTURE.md` | `docs_v2/deep-specs/market-microstructure/README.md` | 0 |
| Market Participants | 78 | `docs_v2/06_MARKET_PARTICIPANTS.md` | `docs_v2/deep-specs/participants/README.md` | 0 |
| Master Architecture | 128 | `docs_v2/00_MASTER_ARCHITECTURE.md` | `docs_v2/deep-specs/architecture/README.md` | 0 |
| Operations and Monitoring | 23 | `docs_v2/18_OPERATIONS_AND_MONITORING.md` | `docs_v2/deep-specs/operations/README.md` | 0 |
| Product and Deployment | 29 | `docs_v2/14_DEPLOYMENT_AND_DOCKER.md` | `docs_v2/deep-specs/deployment-security/README.md` | 0 |
| Product and Scope | 23 | `docs_v2/00_MASTER_ARCHITECTURE.md; docs_v2/17_IMPLEMENTATION_ROADMAP.md` | `docs_v2/deep-specs/architecture/README.md; docs_v2/deep-specs/roadmaps/README.md` | 0 |
| Recorder and Replay | 31 | `docs_v2/12_RECORDER_AND_REPLAY.md` | `docs_v2/deep-specs/recorder-replay/README.md` | 0 |
| Research Appendix | 16 | `docs_v2/00_MASTER_ARCHITECTURE.md` | `docs_v2/_analysis/pass15_source_no_loss/SUPERSEDED_REJECTED_RESEARCH_TRACEABILITY.md` | 0 |
| Risk Constitution | 332 | `docs_v2/09_RISK_CONSTITUTION.md` | `docs_v2/deep-specs/risk/README.md` | 0 |
| Validation Matrix | 378 | `docs_v2/16_VALIDATION_MATRIX.md` | `docs_v2/deep-specs/validation/README.md` | 0 |

## Coverage quality

| Quality | Meaning | Rows |
|---|---|---:|
| EXACT | QF source definition maps to the exact audited QF contract | 110 |
| FULL | implementation semantics or non-active disposition fully preserved | 2396 |
| TRACE_ONLY | external/snapshot, superseded or rejected history with explicit fate | 163 |
| SUBSTANTIAL | explained exception requiring manual acceptance | 0 |
| PARTIAL | unexplained partial coverage | 0 |
| MISSING | absent final coverage | 0 |

The 79 PASS15 recovered items are outside the 2,590 requirement count: 75 have `FULL` coverage and 4 have intentional `TRACE_ONLY` non-current disposition. Formula count is independently verified from canonical headings/IDs as **110/110**.

Destinationless current requirements: **0**. Current requirements with MISSING coverage: **0**. Current requirements with unexplained PARTIAL coverage: **0**.
