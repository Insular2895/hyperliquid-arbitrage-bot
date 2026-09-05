# 04 — Alert Severities, Automated Actions and Escalation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Severity | Operational meaning | Action |
|---|---|---|
| P0 | critical safety/security/authority/exposure incident | immediate no-new-risk/fencing as scoped, page, evidence, reconcile/contain |
| P1 | serious capability degradation or imminent unsafe condition | disable/degrade affected scope and urgent escalation |
| P2 | persistent non-critical degradation/evidence issue | investigate inside calibrated objective |
| P3 | informational/maintenance trend | retain and review |

Locked actions come from domain safety semantics: `UNKNOWN_ORDER`, unreconciled account, stale/corrupt book, failed Recovery, unhealthy clock, infra unsafe, critical persistence failure, secret compromise and split brain can remove new risk. Model/Simulator drift reduces size/falls back/disables dependents according to support and materiality.

Threshold values, windows, hold times, paging destinations and response objectives are calibrated/versioned. Alert hysteresis requires sustained good evidence and necessary reconciliation. Notification clear does not restore capability maturity.

Alert records include type/severity/scope, first/last seen, evidence window/value/validity, threshold version, current state/action, runbook, acknowledgement/escalation and optional IncidentId. Repeated symptoms correlate into incidents without losing individual evidence.
