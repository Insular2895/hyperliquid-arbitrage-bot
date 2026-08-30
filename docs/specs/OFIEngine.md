# OFIEngine

## Purpose

Maintenir imbalance, OFI et MLOFI point-in-time.
## Responsibilities

Event contributions, multi-window/level features et lineage.
## Non-responsibilities

Ne prédit pas seul et n'autorise pas l'exécution.
## Inputs

Ordered book/trade events, BookState, Clock.
## Outputs

OFIFeatureSnapshot.
## Dependencies

BookEngine, ClockAndRng.
## State

Rolling bounded accumulators by market/window/level.
## Algorithms / formulas

QF-028..033.
## Invariants

No future events; reset/gap handling explicit.
## Failure modes

Reorder/gap, zero denominator, window leakage, unbounded memory.
## Risk interactions

Unknown feature lowers confidence; never substitutes book validity.
## Performance requirements

Incremental and bounded; no history scan in hot path.
## Metrics

Update latency, coverage, resets/gaps, distributions.
## Persistence

Feature snapshots and definition/version.
## Configuration

Windows/levels/weights calibrated.
## Tests

Hand-computed sequences, gap/reset, temporal no-lookahead, load.
## Maturity requirement

M2 observe-only; decision use after OOS lift.
## Open calibrated parameters

Weights, horizons, normalization and activation.
