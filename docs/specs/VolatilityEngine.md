# VolatilityEngine

## Purpose

Maintenir returns, variance, volatilité, jumps et régimes online.
## Responsibilities

Multi-horizon point-in-time features et health.
## Non-responsibilities

Ne price pas options et ne fixe pas seul les risk limits.
## Inputs

Valid mid series, Clock, data quality.
## Outputs

VolatilitySnapshot/regime candidates.
## Dependencies

BookEngine, ClockAndRng.
## State

Rolling returns/variance accumulators.
## Algorithms / formulas

QF-036..039.
## Invariants

No centered/future window; invalid books break/reset series explicitly.
## Failure modes

Clock anomalies, gaps, zero epsilon abuse, regime thrash.
## Risk interactions

Alimente risk/survival; unknown augmente conservatisme.
## Performance requirements

Incremental bounded work.
## Metrics

Latency, coverage, jump/regime rates, drift.
## Persistence

Features/definitions and gap markers.
## Configuration

Horizons, epsilon, jump/regime thresholds calibrated.
## Tests

Synthetic returns, gaps, clock, no-lookahead, golden parity.
## Maturity requirement

M2 observe; risk use validated OOS.
## Open calibrated parameters

Horizons, jump threshold, regime method.
