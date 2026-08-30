# OpportunityPortfolioEngine

## Purpose

Allouer capital/capacités partagés entre opportunités concurrentes.
## Responsibilities

Build constraints, optimize/approximate, explain selections.
## Non-responsibilities

Ne crée pas de capacité et n'exécute pas.
## Inputs

Size/RAEV curves, RouteDependencies, balances, inventory/risk budgets.
## Outputs

PortfolioProposal `{route,size}` and resource plan.
## Dependencies

SizingEngine, ReservationEngine, InventoryEngine, QuantEngine.
## State

Point-in-time optimization snapshot.
## Algorithms / formulas

QF-078 `max ΣRAEV_i(q_i), Aq≤b`; approximation must be declared.
## Invariants

No balance/book/risk double count; feasibility independently verifiable.
## Failure modes

Stale candidates, solver timeout, infeasible/unstable solution.
## Risk interactions

Risk budgets are constraints, not tradable costs alone.
## Performance requirements

Strict time budget/fallback feasible baseline.
## Metrics

Solve time, objective/lift/regret, binding constraints, rejects.
## Persistence

Candidate set/constraints/solution/solver version.
## Configuration

Solver/time budget/fallback versioned.
## Tests

Small exhaustive optimum, infeasible cases, shared resources, timeout.
## Maturity requirement

M2 versus baseline; M4 capability-specific.
## Open calibrated parameters

Solver, horizon, batching and approximation tolerance.
