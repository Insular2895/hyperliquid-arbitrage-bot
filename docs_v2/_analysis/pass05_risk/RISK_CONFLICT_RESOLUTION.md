# Risk Conflict Resolution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| ID | Apparent conflict | Authority analysis | Resolution | Status |
|---|---|---|---|---|
| `RISK-C01` | Safety represented as a negative EV penalty versus a forbidden action. | SRC-005 constitutional sections 1–4 and 224; Formula QF-063 is subordinate to safe eligibility. | Hard failure removes the action from `A_safe`; RAEV ranks only safe actions. | RESOLVED |
| `RISK-C02` | Global/portfolio PnL could justify looser leg/order limits. | SRC-005 sections 5–6 and priority hierarchy are explicit. | Higher layers may reduce/block only; profit never relaxes freshness, price, inventory or order safety. | RESOLVED |
| `RISK-C03` | Dossier 3 semantic RiskDecision has `required_price_limit`, execution mode/config/models; Dossier 4 frozen contract has plural price limits and fewer fields. | Dossier 4 is the explicit Data Contract closure. | Frozen fields win; semantic extras travel through RiskSnapshot/ExecutionPlan/version references. No fields invented. | RESOLVED |
| `RISK-C04` | Seven kill scopes versus Dossier 4 `ControlEvent` containing only market/strategy/global kill variants. | Constitutional taxonomy is complete; Data schema is narrower. | Preserve all seven scopes; mark exact event encoding for asset/mode/model/infra as a Data closure gap. | RESOLVED (cross-domain gap) |
| `RISK-C05` | “Fail-open exception” could imply generic availability-first behavior. | SRC-005 section 138 limits it to actions reducing known exposure under RecoveryRiskPolicy. | Rename semantically as bounded risk-reducing exception; unknown safety remains no-new-risk. | RESOLVED |
| `RISK-C06` | More capital/profit or premium infrastructure could imply larger safe size. | SRC-005 scaling sections plus QF-076 and PASS 01 Infra authority. | `Q_validated` and intersection of risk/capacity bounds control size; capital/server price creates no safety permission. | RESOLVED |
| `RISK-C07` | Backtest looks strong while persistent live fills/calibration are poor; or a few live losses seem decisive. | SRC-005 sections 183–184 and Simulator/Participant closures. | Persistent supported live evidence outranks backtest; isolated samples do not establish drift. Promotion uses statistical support. | RESOLVED |
| `RISK-C08` | PASS 00 heuristic statuses label canonical rejection/future words as `REJECTED`, `FUTURE`, `OPEN` or `RESEARCH`. | Full sequential SRC-005 reading shows they are prescriptive constitutional sections. | Correct 14 SRC-005 status false positives in PASS 05 artifacts; keep original ledger history intact. | RESOLVED |

## PASS 00 status corrections

The following source requirements are canonical `LOCKED` structures under SRC-005, regardless of heuristic status in the initial index:

- `REQ-RISK-0072` INV-020 Sunk Costs Are Sunk (`FUTURE` → `LOCKED`).
- `REQ-RISK-0090` Volatility Gate (`REJECTED` → `LOCKED`; exact bound calibrated).
- `REQ-RISK-0111` Hard Inventory Region (`FUTURE` → `LOCKED`; exact bands calibrated).
- `REQ-RISK-0117` Terminal Viability Gate (`FUTURE` → `LOCKED`; metrics/bounds calibrated).
- `REQ-RISK-0134` Global Capital Risk (`OPEN` → `LOCKED`; exact limit calibrated/open).
- `REQ-RISK-0187` bounded risk-reducing exception (`OPEN` → `LOCKED`).
- `REQ-RISK-0190` machine-readable reject reasons (`REJECTED` → `LOCKED`).
- `REQ-RISK-0202` optimizer subordinate to hard gates (`REJECTED` → `LOCKED`).
- `REQ-RISK-0210` startup risk sequence (`OPEN` → `LOCKED`).
- `REQ-RISK-0238` unvalidated research cannot affect production (`RESEARCH` → `LOCKED`).
- `REQ-RISK-0245` hard-inventory property test (`FUTURE` → `LOCKED`).
- `REQ-RISK-0264` Reject Dataset (`FUTURE` → `LOCKED`).
- `REQ-RISK-0271` Risk Accounting (`REJECTED` → `LOCKED`).
- `REQ-RISK-0274` Risk Reproducibility (`REJECTED` → `LOCKED`).

No existing global conflict is reopened. `CONFLICT-004` is reinforced: fixed numerical examples are calibrated rather than constitutional. `CONFLICT-005` remains owned by PASS 11 formula review; no conflicting formula was promoted here. `CONFLICT-023` is reinforced by live-evidence governance.

Conflicts found: 8. Resolved: 8. Remaining constitutional conflicts: 0. Cross-domain schema gaps: 4, all explicitly routed to Data/Operations rather than silently guessed.
