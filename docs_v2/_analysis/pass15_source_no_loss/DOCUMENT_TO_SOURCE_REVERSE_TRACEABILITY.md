# Document-to-Source Reverse Traceability

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Canonical Master | Material supporting sources | Closure authority | PASS15 recovery effect |
|---|---|---|---|
| `00_MASTER_ARCHITECTURE.md` | all, strongest SRC-004/005/006 closures plus later refinements | closure is domain-specific; no single source replaces all owners | none; recovered items already fit existing architecture |
| `03_MARKET_GRAPH_AND_ROUTES.md` | SRC-001/002/003/004/005/007 | SRC-004 formulas; SRC-005 Risk/Data | SRC001 execution-mode scenario axis is a consumer only |
| `04_FORMULA_BOOK.md` | SRC-004 primary; SRC-002/003/007/008 support | SRC-004 Dossier 2 | none |
| `05_MARKET_MICROSTRUCTURE.md` | SRC-001/002/004/005/007/008 | SRC-004 formulas; SRC-005 Data/Risk | none |
| `06_MARKET_PARTICIPANTS.md` | SRC-007 primary; SRC-004/005/006/008 support | SRC-004 formulas and SRC-005 Data/Risk constrain | none |
| `07_COUNTERFACTUAL_SIMULATOR.md` | SRC-008 primary; SRC-003/005/007 support | SRC-005 Data/Replay; SRC-004 formulas | SRC001 mode-axis trace confirms scenario dimensions |
| `08_INVENTORY_AND_CAPITAL.md` | SRC-002/003/004/005/007 | SRC-004/005 plus later SRC-003/007 refinements | none |
| `09_RISK_CONSTITUTION.md` | SRC-005 primary; all others support | SRC-005 Dossier 3 | none |
| `10_EXECUTION_STATE_MACHINE.md` | SRC-004 primary; all others support | SRC-004 Dossier 1 | SRC001 TT/MT/TTT/MTT scenario axis linked to §23 |
| `11_DATA_CONTRACTS.md` | SRC-005 primary; SRC-001/003/006/008 support | SRC-005 Dossier 4 | SRC003 Recorder purpose remains compatible |
| `12_RECORDER_AND_REPLAY.md` | SRC-003 detail; SRC-005 closure; SRC-001/006 support | SRC-005 for ordering/determinism; SRC-003 uncontradicted storage | SRC003 four production purposes restored in §1 |
| `13_INFRASTRUCTURE.md` | SRC-008 primary; SRC-004/005/006 support | SRC-004 QF and SRC-005 Risk/Data constrain | none |
| `14_DEPLOYMENT_AND_DOCKER.md` | SRC-006 primary; SRC-007/008 support | SRC-006 Dossier 5 | none |
| `16_VALIDATION_MATRIX.md` | SRC-006 primary; all sources contribute evidence | SRC-006 Dossier 6 | SRC001 explicit execution-mode scenario axis traced |
| `17_IMPLEMENTATION_ROADMAP.md` | all sources via reconstructed owners | canonical masters and dependency graph | none; no new dependency |
| `18_OPERATIONS_AND_MONITORING.md` | SRC-005/006 primary; SRC-001/003/008 support | Risk plus Validation/Operations closure | SRC003 reconstruction/drift purposes already consumed |
| `19_BUILD_VALIDATE_SCALE_ROADMAP.md` | all source evidence stages | SRC-006 validation closure plus canonical owners | none; no phase change |

Reverse lookup for a runtime rule continues from Master/deep section to its domain requirement ledger, then stable `RequirementId`, PASS00 item and original locator. The CSV provides the forward join and `MASTER_REQUIREMENT_LEDGER.md` retains source statements and dependencies.
