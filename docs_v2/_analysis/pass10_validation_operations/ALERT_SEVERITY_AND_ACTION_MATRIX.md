# Alert Severity and Action Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

P0–P3 is the PASS 10 normalized operational severity model. Numeric trigger thresholds, windows, routing targets and response-time objectives are `CALIBRATED`; locked safety actions derive from Risk/Execution/Deployment contracts.

| Severity | Meaning | Default action |
|---|---|---|
| P0 | active or credible critical safety/security/exposure failure | immediate affected/global no-new-risk, preserve evidence, page human, reconcile/contain |
| P1 | serious degradation likely to become unsafe or materially invalidate capability | scope-degrade/disable, urgent escalation and runbook |
| P2 | non-critical persistent degradation or evidence-quality issue | investigate within calibrated window; no automatic widening |
| P3 | informational/maintenance signal | record/review; no direct capital permission change |

| Alert class | Minimum severity/action | Locked behavior |
|---|---|---|
| `UNKNOWN_ORDER`, `ACCOUNT_UNRECONCILED`, `RECOVERY_FAILED` | P0/P1 by exposure scope | affected capital locked; no new risk until reconciliation |
| `BOOK_STALE`, feed/account loss | P0/P1 by scope | affected new risk off; rebuild/reconcile |
| `CLOCK_UNHEALTHY`, `INFRA_UNSAFE` | P0/P1 | latency-sensitive/new risk removed according to Risk |
| `DISK_CRITICAL`/critical persistence loss | P0/P1 | protect evidence; escalate Risk state |
| secret compromise/split brain | P0 | fence signer/owner; global or affected no-new-risk |
| `MODEL_DRIFT`/Simulator miscalibration | P1/P2 by support and materiality | fallback/reduce/disable dependents, never auto-promote |
| update/license failure | P1/P2 | retain current safe version or no-new-risk; safe exits remain |
| latency/backlog/resource warning | P2 before unsafe threshold | investigate/degrade if it crosses Risk policy |

Alert payload includes alert/incident correlation, severity, scope, state, first/last seen, evidence window, observed value/validity, threshold/version, current automated action, recommended runbook and acknowledgement/escalation state. Alert recovery clears notification state only; it does not silently re-promote maturity.
