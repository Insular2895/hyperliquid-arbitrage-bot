# OrderSlicingEngine

## Purpose

Découper une taille déjà validée en child orders sans créer d'alpha fictif.
## Responsibilities

Slice schedule, child limits, reservation mapping and execution constraints.
## Non-responsibilities

Ne choisit pas le total et ne prétend pas créer de profondeur.
## Inputs

Validated total size, mode, book/latency/risk plan.
## Outputs

Ordered child intents or no-slice plan.
## Dependencies

SizingEngine, PrecisionEngine, ReservationEngine.
## State

Per-plan remaining/fills/child IDs.
## Algorithms / formulas

Policy explicitly evaluated against unsliced baseline; no fixed fragmentation.
## Invariants

Sum children≤reserved total; actual fills drive remaining; no TWAP default.
## Failure modes

Over-reservation, stale schedule, adverse delay, duplicate child.
## Risk interactions

Each child obeys price/risk; later children cancel on revalidation failure.
## Performance requirements

Bounded children; no async task forest.
## Metrics

Children/fill/slippage/delay vs baseline.
## Persistence

Parent-child map and outcomes.
## Configuration

Disabled by default unless policy validated.
## Tests

Rounding/sums, partials/cancels, no-depth-creation property.
## Maturity requirement

M2 research; M4 before live enablement.
## Open calibrated parameters

When/how many slices and child timing.
