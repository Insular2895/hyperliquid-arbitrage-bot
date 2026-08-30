# ShadowBook

## Purpose

Représenter le carnet alternatif après nos ordres simulés.
## Responsibilities

Clone/overlay, mechanical consumption, reservations and branch/rejoin.
## Non-responsibilities

Ne simule pas participant/cross-market response lui-même.
## Inputs

Historical BookState, shadow actions/fills, branch policy.
## Outputs

Counterfactual BookState and mechanical impact trace.
## Dependencies

BookEngine, NetConvert, ClockAndRng.
## State

Per-branch overlays and consumed levels.
## Algorithms / formulas

QF-009..013/042; deterministic level depletion.
## Invariants

No negative depth; no double consumption; base history immutable.
## Failure modes

Historical conflict after intervention, invalid rejoin, memory explosion.
## Risk interactions

Constrains capacity/recovery scenarios.
## Performance requirements

Copy-on-write/overlay may be optimized after benchmark; bounded horizon.
## Metrics

Levels/bytes per branch, impact, conflicts/rejoins.
## Persistence

Branch manifest and impact trace, not rewritten RAW.
## Configuration

Branch horizon/rejoin policy/fidelity.
## Tests

Golden walks, concurrent routes, branch determinism, conflict policies.
## Maturity requirement

M2 F1; advanced response later.
## Open calibrated parameters

Horizon/rejoin and data structure performance.
