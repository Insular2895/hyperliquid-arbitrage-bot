# CORR-03 — Cross-Domain Change Map

DOCUMENTATION STATUS: OWNERSHIP INTEGRATION

| Domain | CORR-03 role | Explicit non-role |
|---|---|---|
| Execution | authoritative actual orders/fills/route state | no prediction/training |
| Recovery/Reconciliation | actual exposure resolution and finality | Recovery success is not route completion |
| Inventory/Accounting | actual exposure and separate economic truth | prediction never mutates Inventory |
| Data | snapshot/join/label/artifact versions and validity | no second fill ledger |
| Recorder/Replay | retain/reconstruct all outcomes and fixtures | simulated labels not Live actuals |
| Simulator | owns final versioned `ExecutionForecast` | prediction is not state/Risk permission |
| Participants | optional survival/liquidity/maker features | not full-route truth owner |
| Risk | future consumer after promotion | no new hard gate or model training |
| Validation | labels, OOS calibration, support, promotion/demotion | no authority from accuracy alone |
| Operations | outcome/failure/join/calibration/support/drift views | no raw-ID metric labels |
| Roadmap | implementation/evidence sequence in existing phases | no Phase 27 |
| Formula | existing QF-056/057, 095/096/100 reused | no new QF or double-counted probability penalty |
