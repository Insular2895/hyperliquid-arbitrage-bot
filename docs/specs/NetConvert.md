# NetConvert

## Purpose

Calculer l'output exécutable unique d'une conversion directionnelle.
## Responsibilities

Side, L2 walk, fees, precision, minimums, price limit et breakdown.
## Non-responsibilities

Ne prévoit ni survie/fill futur ni inventory utility.
## Inputs

Assets, input typed amount, BookState, FeeQuote, metadata, mode.
## Outputs

ConversionQuote ou typed rejection; consumed slices/costs.
## Dependencies

BookEngine, FeeEngine, PrecisionEngine.
## State

Pur fonctionnel sur snapshots/version IDs.
## Algorithms / formulas

QF-007..016.
## Invariants

Bon côté du book, chaque rounding appliqué, aucune profondeur fantôme.
## Failure modes

Insufficient depth, stale input, rounding zero, unit/fee error.
## Risk interactions

Toute input invalide hard reject; breakdown auditable.
## Performance requirements

Déterministe, bounded by retained levels; benchmark candidate sizes.
## Metrics

Latency, levels walked, rejects, slippage/rounding/fee components.
## Persistence

Inputs/output/version/breakdown dans Opportunity/Decision.
## Configuration

Aucune fee/precision dupliquée; execution limits explicit.
## Tests

Golden multi-level, buy/sell, fees, rounding, boundaries, parity.
## Maturity requirement

M1 golden; M2 replay; M4 actual slippage calibration.
## Open calibrated parameters

Candidate sizes/price protection viennent de Sizing/Risk.
