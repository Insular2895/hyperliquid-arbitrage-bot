# botctl

## Purpose

Fournir l'interface opérateur sûre et auditable.
## Responsibilities

Install/preflight/status/health/start/safe-stop/reconcile/update/rollback/risk-off/diagnose.
## Non-responsibilities

Ne contourne pas RiskEngine et n'affiche pas les secrets.
## Inputs

Explicit command/options, local auth/config/deployment state.
## Outputs

Human/structured redacted result, exit code and audit event.
## Dependencies

Deployment, ReconciliationEngine, InfrastructureMonitor, Recorder.
## State

No hidden daemon state; operates on declared instance.
## Algorithms / formulas

Idempotent command workflows; confirmations for sensitive actions.
## Invariants

Install/start never implies READY/live; stop safe before process stop.
## Failure modes

Partial command, privilege error, stale status, update interruption.
## Risk interactions

Emergency/risk-off preserved; actions respect engine permissions.
## Performance requirements

Operator path only; bounded waits/status streaming.
## Metrics

Commands/outcomes/durations/failures without sensitive args.
## Persistence

Local audit and support bundle hashes/redaction.
## Configuration

Instance paths/policies, no secret CLI arguments.
## Tests

Idempotence, interruption, exit codes, redaction, permissions, rollback.
## Maturity requirement

M1 contracts; M3 canary; M4 operator drills.
## Open calibrated parameters

UX/timeouts/confirmation and telemetry opt-in.
