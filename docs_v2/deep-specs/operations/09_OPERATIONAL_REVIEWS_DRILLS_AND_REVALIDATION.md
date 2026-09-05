# 09 — Operational Reviews, Drills and Revalidation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Mandatory review layers are continuous alerts, recent operator exceptions, periodic model/simulator/Q_validated/incident review, monthly/periodic capability/SLO/infra/security review, release/change impact review and post-incident review. Exact calendar timing is calibrated.

Review inputs include health/unsafe time by cause; reconciliation/unknown/recovery; data quality; PnL decomposition; predicted/actual calibration; drift/OOD; Q_validated/support; SLO/error budgets; infrastructure economics; security/release/retention; incidents and open deviations. Positive total PnL does not close an unsafe finding.

Restore drills prove backups, manifests, journals/checkpoints and evidence can be recovered. Reconciliation drills prove orders→fills→balances→reservations under missing/duplicate/late evidence. Safe-stop, crash, update/rollback, secret rotation and ownership/fencing drills apply to the deployed profile.

Each drill emits EvidenceId, expected/actual state/actions, timing, artifacts, deviations, owner and rerun. Revalidation triggers include material code/config/model/formula/schema/data/infra/exchange changes, size/market/mode expansion, drift/SLO breach, incident and evidence expiry.
