# QuantEngine

## Purpose

Orchestrer les formules versionnées et distributions économiques.
## Responsibilities

QF registry, EV/RAEV/tails/confidence, parity artifacts.
## Non-responsibilities

Ne contourne aucun gate hard et ne cache pas les composantes.
## Inputs

Quotes, scenario outcomes, features, inventory/model versions.
## Outputs

QuantAssessment avec breakdown et formula versions.
## Dependencies

NetConvert, simulator/model engines, InventoryEngine.
## State

Immutable formula/config/model registry.
## Algorithms / formulas

QF-001..110 selon domaine; QF-056..063 central.
## Invariants

Units/signs explicites; probabilities sum; aucun double cost.
## Failure modes

NaN/overflow, mixed versions, invalid distribution, unit mismatch.
## Risk interactions

Invalid/nonfinite/LOW confidence = reject conservateur.
## Performance requirements

Hot subset borné; heavy aggregation offline.
## Metrics

Latency, numerical errors, EV/tail/calibration drift.
## Persistence

Inputs/outputs/formula/config/model IDs.
## Configuration

Paramètres CALIBRATED versionnés; aucun default caché.
## Tests

Golden Rust-Python, property, numerical boundaries, scenario sums.
## Maturity requirement

M1 formula core; M2 distributions; M4 calibration.
## Open calibrated parameters

E_min, P_min, ES limits, uncertainty penalties, confidence gates.
