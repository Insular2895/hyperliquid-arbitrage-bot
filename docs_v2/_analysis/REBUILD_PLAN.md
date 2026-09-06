# Documentation Rebuild Plan

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Pass | Scope | Primary sources / authority | Expected outputs | Dependencies |
|---|---|---|---|---|
| PASS 00 | Master Requirement Ledger | all 8 sources | clean-room map and registers | none |
| PASS 01 | Infrastructure | SRC-008 depth; SRC-004/005/006 closures | Infrastructure master + deep specs | PASS 00 review |
| PASS 02 | Market Participants / Competition | SRC-007; Formula/Data closures | Participants master + survival/response specs | PASS 00 |
| PASS 03 | Counterfactual Simulator | SRC-008; Formula/Data/Risk closures | Simulator master + fidelities | PASS 02 interfaces |
| PASS 04 | Execution | SRC-004 Dossier 1/6 | Execution master + order/recovery specs | Data/Risk contracts indexed |
| PASS 05 | Risk Constitution | SRC-005 Dossier 3/6 | Risk master + gates/budgets | Execution interfaces |
| PASS 06 | Data / Recorder / Replay / Determinism | SRC-005 Dossier 4/6 + SRC-003 | Data/Recorder/Replay masters/specs | Clock/schema authority |
| PASS 07 | Inventory / Capital / Bridge / Sizing | SRC-003/007 + closures | Inventory/capital master + specs | Execution/Simulator/Risk |
| PASS 08 | Graph / Routes / Market Atlas / Quant | SRC-001/002/003/007 + Formula closure | Graph/routes/quant masters/specs | Data/Inventory |
| PASS 09 | Deployment / Security / Client | SRC-006 Dossier 5/6 | Deployment/security master + specs | Infra/Data |
| PASS 10 | Operations / Monitoring / Validation | SRC-006 Dossier 6/6 + Risk | Validation/operations master + runbooks | all critical domains |
| PASS 11 | Formula Book Audit | SRC-004 Dossier 2/6 | audited QF-001..110 index/book | domain masters |
| PASS 12 | Build / Validate / Scale Journey — COMPLETE, HUMAN REVIEW REQUIRED | SRC-006 + cross-domain requirements | `17_IMPLEMENTATION_ROADMAP.md`, `19_BUILD_VALIDATE_SCALE_ROADMAP.md`, matrices and deep specs | PASS 01–11 |
| PASS 13 | Master Architecture Reconstruction — COMPLETE, HUMAN REVIEW REQUIRED | all resolved domain docs + 647 original architecture locators | `00_MASTER_ARCHITECTURE.md`, architecture deep specs and ownership/flow matrices | PASS 01–12 |
| PASS 14 | Cross-Domain Consistency Audit | all | conflict/dependency closure | PASS 13 |
| PASS 15 | Source-by-Source No-Loss Audit | all 8 sources | final source coverage | PASS 14 |
| PASS 16 | Human Review Package | all artifacts | review bundle, no self-approval | PASS 15 |

The Technical Implementation Roadmap and Build/Validate/Scale Journey are reconstructed and remain separate. Governing philosophy: `SPECIFICATION → IMPLEMENTATION → EVIDENCE → VALIDATED CAPABILITY → CAPITAL`, with final-capable architecture and progressive capability activation rather than a throwaway MVP.

**NEXT:** PASS 14 — Cross-Domain Consistency Audit, only after human review of PASS 13. Implementation has not started and is not authorized.
