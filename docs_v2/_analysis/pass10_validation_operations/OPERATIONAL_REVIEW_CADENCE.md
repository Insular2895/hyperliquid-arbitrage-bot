# Operational Review Cadence

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Exact wall-clock schedules remain `CALIBRATED`. The mandatory review layers are:

| Layer | Trigger/cadence class | Required output |
|---|---|---|
| continuous | safety alerts, readiness, drift and SLO signals | automated safe action, evidence and escalation |
| shift/daily-style | recent incidents, unknown/reconciliation, data quality, risk/PNL decomposition | operator exceptions and open actions |
| weekly-style | model/simulator calibration, reject data, Q_validated, failure trends, capacity/support | scoped health/demotion decision |
| monthly/periodic | capability manifests, SLO/error budgets, infrastructure economics, retention/security, restore/reconciliation drills | review record, expiries and revalidation plan |
| release/change | build/config/model/formula/schema/infra/exchange-rule scope | impact analysis and required validation ladder |
| incident | immediate containment then postmortem | root cause, actions, evidence and resume gate |

Reviews include negative results and unresolved deviations. They do not infer readiness from positive total PnL. Restore drills prove protected state/evidence can be recovered; reconciliation drills prove current exchange truth and capital locks are correct; each applicable failure drill proves its expected safe action. Drill success/failure is an EvidenceId, with remediation owner and rerun date.
