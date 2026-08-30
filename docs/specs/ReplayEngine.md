# ReplayEngine

## Purpose

Rejouer les événements historiques dans le même core de façon reproductible.
## Responsibilities

Manifest validation, ordering, Clock/RNG, checkpoint restore, exact/fast modes.
## Non-responsibilities

Ne réécrit pas l'historique et ne garantit pas un contrefactuel exact.
## Inputs

Dataset/chunks/checkpoints and RunManifest.
## Outputs

Normalized events, deterministic run outputs and data-quality report.
## Dependencies

Recorder contracts, ClockAndRng, all core consumers.
## State

Cursor/cutoff/simulated clock/seed/checkpoint.
## Algorithms / formulas

Recorder order and timing; no-lookahead; optional simulator integration.
## Invariants

Same manifest→same output; future invisible; gaps declared.
## Failure modes

Corrupt/missing chunk, incompatible schema, bad checkpoint, clock leakage.
## Risk interactions

Invalid fidelity blocks promotion evidence.
## Performance requirements

Exact and accelerated; deterministic before speed.
## Metrics

Events/s, determinism hashes, gaps, checkpoint speed, parity.
## Persistence

RunManifest/results/logical output hashes.
## Configuration

Mode/speed/fidelity/dataset/config/model/seed explicit.
## Tests

Repeat hashes, checkpoint equivalence, no-lookahead, schema/gap failures.
## Maturity requirement

M2 foundation before advanced strategy.
## Open calibrated parameters

Checkpoint cadence/cache and acceptable data quality by experiment.
