# ReservationEngine

## Purpose

Empêcher double dépense de balances, book capacity et risk budget.
## Responsibilities

Atomic reserve/commit/release/expire/reconcile and ownership.
## Non-responsibilities

Ne suppose pas order terminal et ne calcule pas size.
## Inputs

Resource proposal, actual snapshots, order/fill/reconcile events.
## Outputs

ReservationSet/token or typed conflict; availability snapshots.
## Dependencies

InventoryEngine, RouteDependencies, OrderStateMachine, ReconciliationEngine.
## State

Single-owner ledger by ReservationId/resource.
## Algorithms / formulas

QF-073/074 and constraint accounting.
## Invariants

Reserve before order; availability nonnegative; unknown/cancel-request retains.
## Failure modes

Race, leak, premature release, duplicate commit, crash.
## Risk interactions

Invariant breach triggers no-new-risk/reconcile.
## Performance requirements

Atomic bounded operation; avoid coarse contention after benchmark.
## Metrics

Utilization/conflicts/leaks/age/reconcile mismatch/latency.
## Persistence

Reservation events/checkpoints linked plans/orders.
## Configuration

Expiry only where safe; resource categories versioned.
## Tests

Concurrency/property/crash/unknown/cancel/partial/reconciliation.
## Maturity requirement

M2 before submits; M4 proven restart.
## Open calibrated parameters

Safe expiries/timeouts; never automatic for unknown exposure.
