# CrossMarketResponseEngine

## Purpose

Estimer la réponse de marchés voisins à un shock source.
## Responsibilities

Sparse neighborhoods, conditional distributions, lead-lag candidates and confidence.
## Non-responsibilities

Ne déduit pas causalité d'une corrélation et n'utilise pas matrice dense naïve.
## Inputs

Synchronized point-in-time events/features and shock definitions.
## Outputs

`R_{i→j}(h)` distributions with support/OOD.
## Dependencies

ParticipantEngine, LiquidityResponseEngine, ClockAndRng.
## State

Approved sparse graph/model version.
## Algorithms / formulas

QF-081/082; event-study candidates then learned model.
## Invariants

No lookahead; source/target clocks aligned within declared uncertainty.
## Failure modes

Spurious lead-lag, clock skew, dense overfit, regime drift.
## Risk interactions

Adds uncertainty/correlation; fallback no-response/conservative bounds declared.
## Performance requirements

Only sparse relevant neighbors in live.
## Metrics

Calibration/lift/OOD/neighborhood stability/latency.
## Persistence

Response graph/model/data manifests.
## Configuration

Neighborhood/horizon/feature set versioned.
## Tests

Clock perturbation, null data, OOS, sparsity and ablation.
## Maturity requirement

M2 research; F3 only after validated lift.
## Open calibrated parameters

Neighborhoods, horizons, model/fallback.
