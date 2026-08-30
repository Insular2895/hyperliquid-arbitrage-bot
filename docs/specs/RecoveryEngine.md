# RecoveryEngine

## Purpose

Réduire une exposition existante avec perte attendue minimale.
## Responsibilities

Enumerate exits/splits, price current state, risk gate and execute recovery plans.
## Non-responsibilities

Ne poursuit pas le PnL initial, ne martingale pas, ne prend pas nouveau risque spéculatif.
## Inputs

Actual exposure, current books/fees/inventory/risk and allowed exits.
## Outputs

RecoveryPlan/events/outcome/loss.
## Dependencies

NetConvert, Quant, Risk, Reservation, ExecutionCoordinator, Reconciliation.
## State

RECOVERY_REQUIRED/PLANNING/RESERVED/EXECUTING/VERIFYING/RECOVERED ou
RECOVERY_FAILED→MANUAL/HARD HALT; residual exposure/reservations.
## Algorithms / formulas

QF-079/080; full/split candidates, sunk costs excluded.
## Invariants

Original route no privilege; actual state only; recovery permission survives licence.
## Failure modes

No liquid exit, repeated partial/unknown, stale books, cascading failure.
## Risk interactions

May act in RECOVERY_ONLY under stricter reducing-risk permissions.
## Performance requirements

Fast bounded safe candidate set; fallback deterministic.
## Metrics

Time/loss/residual, attempts, split/full, failures.
## Persistence

Every candidate/decision/order/fill/state.
## Configuration

Eligible safety assets, max attempts/time/loss reviewed.
## Tests

Partial chains, no exit, split optimum, stale/unknown/crash.
## Maturity requirement

M2 adversarial; M3 shadow; M4 before scaling.
## Open calibrated parameters

Candidate limits, reserves, time/loss thresholds.
