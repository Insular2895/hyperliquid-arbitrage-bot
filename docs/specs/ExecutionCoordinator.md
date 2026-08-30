# ExecutionCoordinator

## Purpose

Orchestrer une route de plan validé jusqu'à terminalité sûre.
## Responsibilities

Route state, reserve, submit sequencing, actual-fill replanning, recovery handoff.
## Non-responsibilities

Ne possède pas la vérité exchange et ne fait aucun blind retry.
## Inputs

ExecutionPlan, RiskDecision, reservations, order/fill/account/book events.
## Outputs

RouteExecution events/state, submits, recovery/reconcile requests.
## Dependencies

Risk/Reservation, OrderStateMachine, Transport, Recovery/Reconciliation.
## State

RouteExecutionState and linked IDs/actual exposure.
## Algorithms / formulas

After event compare completion/EV_continue/QF-079 recovery.
## Invariants

Actual fill only; original route no privilege; only READY opens new risk.
## Failure modes

Lost event, partial, unknown, crash, stale repricing, duplicate command.
## Risk interactions

Revalidates before every new leg; failure moves recovery-only.
## Performance requirements

Event handling deterministic/bounded; no blocking diagnostics.
## Metrics

State durations, outcomes, partial/recovery/unknown, decision latency.
## Persistence

All transitions/commands/events before or atomically with effects.
## Configuration

Mode permissions and calibrated timers via policy.
## Tests

State/property, all fill/cancel/timeout/crash interleavings.
## Maturity requirement

M2 emulator; M3 shadow; M4 protected real flow.
## Open calibrated parameters

Wait/cancel/continuation timers and policy margins.
