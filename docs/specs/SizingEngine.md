# SizingEngine

## Purpose

Choisir le notional total optimal et sa capacité validée.
## Responsibilities

Candidate grid/refinement, constraints, RAEV curve and Q_validated.
## Non-responsibilities

Ne découpe pas les ordres et ne réserve pas.
## Inputs

Edge/outcome curves, balances/book capacity, inventory/risk/confidence.
## Outputs

SizeProposal with feasible interval and evidence.
## Dependencies

QuantEngine, InventoryEngine, ReservationEngine, CounterfactualSimulator.
## State

Pur sur snapshots/version IDs.
## Algorithms / formulas

QF-026/027 and 075..077.
## Invariants

No assumed smoothness; every quantity precision-valid; visible depth≠capacity.
## Failure modes

Missed discontinuity, stale capacity, optimistic unsupported extrapolation.
## Risk interactions

All hard gates/ES/P+/confidence constrain output.
## Performance requirements

Bounded candidate count in live; offline validation exhaustive enough.
## Metrics

Latency/evaluations, selected/Q_validated, regret, constraint binding.
## Persistence

Grid/curve/constraints/selection in DecisionRecord.
## Configuration

Grid/refinement and minimum evidence calibrated.
## Tests

Discontinuous curves, boundaries, shared capacity, property constraints.
## Maturity requirement

M2 replay; M4 actual size bands before scaling.
## Open calibrated parameters

Grid/refinement, limits and confidence thresholds.
