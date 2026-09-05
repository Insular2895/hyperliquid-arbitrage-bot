# 08 — Incident Evidence, Timeline, Redaction and Postmortem

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

`IncidentRecord` is keyed by IncidentId and contains severity, affected markets/executions, start/end, triggers, actions and resolution. Alerts, state transitions and operator actions link to it.

The evidence package resolves RunManifest/build/image/config/model/formula/schema/capability/infra; checksummed RAW/quality window; ordered market/account/order/fill/timer/infra/control events; state versions/hashes; opportunities/rejects/decisions/plans/intents/journal/reservations; actual fills/fees/inventory/reconciliation/PnL; predicted/actual data; alerts/metrics/logs; runbook steps; reproduction and remediation.

Canonical recorder sequence defines order. Source and receive timestamps plus clock uncertainty remain visible; conflicting times are not rewritten. Pin calibrated pre/post windows for P0/P1.

Export is local and client-controlled. Allowlist content, remove secrets/tokens/seeds/raw environment/unnecessary identifiers/history/dumps, run denylist/entropy/canary tests and fail closed. Include a sanitized manifest and hashes.

Postmortem separates facts, hypotheses, root cause, contributing conditions, impact, detection/response/recovery, counterfactual analysis, corrective/preventive actions, owners/dates and revalidation. M5 may be demoted before root cause is fully known.
