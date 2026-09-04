# Risk Legacy Comparison

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Comparison was performed only after the V2 master and deep specifications existed. Legacy files remain `LEGACY_REFERENCE_ONLY` and were not modified.

## Files compared

`docs/09_RISK_CONSTITUTION.md`, `docs/10_EXECUTION_STATE_MACHINE.md`, `docs/11_DATA_CONTRACTS.md`, `docs/07_COUNTERFACTUAL_SIMULATOR.md`, `docs/16_VALIDATION_MATRIX.md`, `docs/18_OPERATIONS_AND_MONITORING.md`, and relevant `docs/specs/{RiskEngine,ExecutionTransport,RecoveryEngine,InventoryEngine}.md`.

| Area | Legacy state | V2 recovery/improvement | Disposition |
|---|---|---|---|
| Priority and EV boundary | Correct compact hierarchy and “EV cannot violate invariant.” | Exact safe-set optimization statement and exact seven-action scheduler priority. | RECOVERED/EXPANDED |
| `INV-001..030` | All names listed. | Exhaustive per-invariant inputs, conditions, permissions, reasons, formulas, tests, locators and owners. | RECOVERED/EXPANDED |
| Gate ordering | Two compact pre-reserve/pre-submit lists. | Exact 13-stage SRC-005 pipeline plus fast-reject/hot-path contract. | LEGACY OMISSION RECOVERED |
| Market/data anomaly | General freshness/validity. | Sequence integrity, no silent repair, cross-market consistency and unsupported huge-edge policy. | LEGACY OMISSION RECOVERED |
| Model/OOD | Confidence mentioned. | Hard/soft OOD, disagreement, dependency fallback, Simulator/Participant kills and “confidence cannot be purchased with size.” | LEGACY OMISSION RECOVERED |
| Tail risk | P+/ES/CVaR named. | Loss/VaR/ES roles, route/recovery/portfolio tails and no double counting. | LEGACY OMISSION RECOVERED |
| Inventory/capital | Limits summarized. | Soft/hard regions, strict reducing exception, net flow, concentration, transit/terminal/stranded, reservations and hidden leverage. | LEGACY OMISSION RECOVERED |
| RiskDecision | Generic allow/reject/degrade/halt. | Exact frozen fields, exact seven actions, semantic-to-contract mapping and transport enforcement. | LEGACY OMISSION RECOVERED |
| TTL/revalidation | Pre-submit/next-leg idea. | Exact T0–T5 and calibrated TTL/invalidation semantics. | LEGACY OMISSION RECOVERED |
| Action classes | Reducing permission mentioned. | Explicit increasing/neutral/reducing matrix across execution/kill states. | LEGACY OMISSION RECOVERED |
| Kill switches | Seven names and generic triggers. | Scope/dependency/reset/telemetry/test matrix plus five quality/change switch families. | LEGACY OMISSION RECOVERED |
| Drawdown/loss | Limits named. | NORMAL/CAUTION/RISK_OFF/HALT, multi-window loss velocity and no martingale/relaxation. | LEGACY OMISSION RECOVERED |
| Recovery risk | Negative-EV/bounded concept. | Known-exposure predicate, loss/tail/attempt/time/price/reservation bounds and escalation. | LEGACY OMISSION RECOVERED |
| Scaling | No detailed evidence gate. | `Q_validated`, no capital-only scaling, micro-live/tail/capacity/infra evidence. | LEGACY OMISSION RECOVERED |
| Config governance | Version/review/rollback summary. | Constitutional/tunable/provenance classes, parameter-family inventory, plan pinning, client/operator bounds. | LEGACY OMISSION RECOVERED |
| Audit/reject data | Reason/evidence summary. | Immutable snapshot/decision trace, rejected-opportunity dataset and selection-bias calibration. | LEGACY OMISSION RECOVERED |
| Validation/failures | Broad failure list and maturity matrix. | Risk-specific property/fault map, dependency STOPS/LIES/LATE/DUP/OOD/STALE matrix, percentile requirements. | LEGACY OMISSION RECOVERED |
| Data schema precision | Generic snapshot/decision/plan description. | Exact Dossier 4 fields and four explicitly deferred schema gaps. | LEGACY OMISSION RECOVERED |

Legacy omissions recovered: 16 material areas. Legacy contradictions introduced: 0. Legacy files modified: 0.
