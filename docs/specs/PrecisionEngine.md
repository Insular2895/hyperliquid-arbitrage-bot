# PrecisionEngine

## Purpose

Normaliser prix/quantités/notionals selon règles effectives.
## Responsibilities

Quantization, validation, minimums et reason codes.
## Non-responsibilities

Ne choisit ni size économique ni price limit.
## Inputs

Typed amount/price, MarketMetadata version.
## Outputs

Valid normalized values ou rejection.
## Dependencies

MetadataEngine.
## State

Règles effectives par market/version.
## Algorithms / formulas

QF-007/008 et intermediate rounding de QF-016.
## Invariants

Floor/rounding direction explicite; jamais de dépassement de réserve/limit.
## Failure modes

Overflow, wrong unit, invalid significant digits, below minimum.
## Risk interactions

Normalization failure est hard reject.
## Performance requirements

Déterministe, allocation-free cible si benchmark utile.
## Metrics

Rejects par règle, rounding deltas, latency.
## Persistence

Metadata version et valeurs pré/post dans Decision/Order.
## Configuration

Aucune règle manuelle; source officielle revalidée.
## Tests

Boundaries/property/golden Rust-Python et historical changes.
## Maturity requirement

M1 avant NetConvert/order; M2 parity.
## Open calibrated parameters

Aucun threshold stratégique; règles externes à vérifier.
