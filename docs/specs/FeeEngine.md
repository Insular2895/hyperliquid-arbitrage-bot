# FeeEngine

## Purpose

Résoudre le taux et delta de frais exacts par compte/marché/mode/temps.
## Responsibilities

Historisation, lookup, rebate, economic value et wallet delta.
## Non-responsibilities

Ne marche pas le book et n'estime pas le slippage.
## Inputs

User fee state, metadata, mode, notional, timestamp.
## Outputs

FeeQuote versionné et FeeAssetDelta attendu.
## Dependencies

MetadataEngine, Recorder.
## State

Fee schedule/account tier effective-dated.
## Algorithms / formulas

QF-014/015.
## Invariants

Aucun taux hardcodé; unknown/stale fee = hard reject.
## Failure modes

Tier change, wrong asset delta, double subtraction, stale cache.
## Risk interactions

Fee uncertainty interdit route; reconciliation compare actual.
## Performance requirements

Lookup mémoire borné.
## Metrics

Age, misses, predicted-vs-actual fee error.
## Persistence

Fee events/snapshots et version ID.
## Configuration

Source/refetch policy, non valeur économique.
## Tests

Maker/taker/rebate/change/history/rounding/golden.
## Maturity requirement

M2 parity; M4 actual fee calibration.
## Open calibrated parameters

Freshness/refetch threshold; mechanics external verification.
