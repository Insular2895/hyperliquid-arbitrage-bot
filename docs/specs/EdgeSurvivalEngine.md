# EdgeSurvivalEngine

## Purpose

Estimer survie/hazard/edge à l'arrivée et capture probability.
## Responsibilities

Episode construction contract, inference, calibration and uncertainty.
## Non-responsibilities

Ne décide pas seul et ne suppose pas une latence constante.
## Inputs

Opportunity features, latency distribution, survival model.
## Outputs

S(t|X), hazard, half-life, P_capture, P(edge>E_min), confidence.
## Dependencies

ParticipantEngine, InfrastructureMonitor, ClockAndRng.
## State

Approved model/version and lookup summaries.
## Algorithms / formulas

QF-044..050, 083, 085, 094..096.
## Invariants

Censoring handled; temporal/OOS; S nonincreasing and in [0,1].
## Failure modes

Miscalibration, regime drift, extrapolation, sparse tails.
## Risk interactions

Alimente EV/confidence; unsupported size/regime rejected.
## Performance requirements

Lookup/small inference bounded.
## Metrics

Brier/log loss/calibration by horizon, capture bias, latency.
## Persistence

Episodes, predictions/outcomes and model manifests.
## Configuration

Horizons, strata, champion/fallback.
## Tests

Survival properties, censoring, walk-forward, OOD, parity.
## Maturity requirement

M2 replay; M3 shadow; M4 actual calibration before scaling.
## Open calibrated parameters

Model, horizons, sample support and thresholds.
