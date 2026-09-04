# Failure Modes, Tests and Definition of Done

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Failure rule

Every dependency is tested for stopped, lying/corrupt, late, duplicate, stale and OOD behavior where meaningful. The safe direction is less capability: invalidate, preserve uncertain reservations, reconcile, reduce, scope-kill or halt. No failure produces aggression.

Key injections cover market/feed gap, crossed/corrupt/stale book, unknown balance/order, lost HTTP response, duplicate fill/event, unavailable/NaN/OOD model, Simulator miscalibration, infra/clock/scheduler degradation, disk full/recorder backlog, invalid config, reservation mismatch, exchange disconnect and reconciliation failure.

## Required properties

- Unsafe state cannot create new risk.
- Reserved balance never exceeds actual balance and cannot be double spent.
- Filled size cannot exceed requested size beyond authorized numeric tolerance.
- `NEW_RISK` cannot intentionally produce inventory outside hard bounds.
- UNKNOWN capital remains unavailable to another route.
- Global PnL cannot relax leg/order risk.
- Optimizer cannot resurrect a rejected route.
- Mandatory invalid/OOD model support cannot be bypassed merely with smaller size.
- Recovery attempt/time/loss bounds terminate.
- Client configuration cannot remove an invariant.
- Same snapshot/config/models produces the same decision.

## Operational sequences

Startup: `BOOT → CONFIG VALIDATE → CLOCK → FEEDS → BOOKS → ACCOUNT → OPEN ORDERS → FILLS → RECONCILIATION → RISK HEALTH → READY`.

Shutdown: `STOP NEW RISK → HANDLE RESTING ORDERS → RESOLVE ACTIVE EXECUTIONS → PERSIST → STOP`.

Automatic process restart returns through startup and reconciliation; it never directly resumes trading.

## Acceptance

SRC-006 requires unit/property/fault tests per invariant as applicable, plus mandatory stale, unknown-state, hard-inventory, CVaR, OOD and infra-unsafe tests. Risk determinism is verified with identical inputs. Evaluation latency is measured at P50, P95, P99 and P99.9; acceptable bounds require calibration.

Constitutional compliance additionally requires complete reason/audit output, kill/reset drills, config/version rollback, no missing `INV-*`, no destinationless risk requirement and validated capability gating. Code support alone is not live authorization.

Source: SRC-005 lines 3644–3783, 4090–4458 and 5030–5241; SRC-006 lines 4550–4589 and 5976–6010.
