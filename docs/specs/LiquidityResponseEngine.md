# LiquidityResponseEngine

## Purpose

Modéliser add/cancel/aggression/replenishment après shock.
## Responsibilities

Conditional response distributions and resilience calibration.
## Non-responsibilities

Ne mélange pas impact mécanique local et response.
## Inputs

Shock/event episodes, books/trades/features.
## Outputs

LiquidityResponseDistribution by horizon/regime.
## Dependencies

OFIEngine, VolatilityEngine, ParticipantEngine.
## State

Approved response artifact/version.
## Algorithms / formulas

QF-043 and learned conditional distributions.
## Invariants

Mechanical consumption excluded from learned residual response.
## Failure modes

Double impact, sparse support, causality claims, negative invalid depth.
## Risk interactions

Widens simulator uncertainty/capacity; no hard gate override.
## Performance requirements

Heavy sampling offline; compact quantiles online.
## Metrics

Calibration/coverage/resilience error/OOD/economic lift.
## Persistence

Episodes, models, predictions/outcomes.
## Configuration

Horizons, shocks, neighborhoods, fallback.
## Tests

Synthetic shocks, decomposition, OOS, impossible-depth guards.
## Maturity requirement

M2 research; F3 use after shadow/micro-live calibration.
## Open calibrated parameters

Response representation, horizons and support gates.
