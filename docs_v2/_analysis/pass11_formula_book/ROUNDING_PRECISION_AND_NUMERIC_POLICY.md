# Rounding, Precision and Numeric Policy

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Arithmetic domains

| Domain | Required arithmetic | Exact outputs |
|---|---|---|
| exchange price/size | integer ticks/lots or equivalent exact fixed point | legal prices/sizes, QF-007/008 decisions |
| book walk/reservation | checked exact quantities and value accumulation at declared scales | level fills, residuals, spent amounts, capacity/reservations |
| fees/account deltas | exchange-compatible exact debits plus explicit converted economic value | fee asset deltas/reconciliation |
| route composition | exact quantization at each leg boundary | each legal intermediate input/output |
| stochastic/statistical | deterministic floating/reference algorithms allowed | validity/range predicates exact; numeric values toleranced |
| accounting | explicit currency/numeraire, preferably fixed-point at ledger boundary | reconciled component sums/identities |

## Rules

1. QF-007 floors a non-exceeding size; an exact lot stays unchanged, below-minimum becomes zero then fails any applicable minimum gate, and a negative/nonfinite input is invalid.
2. QF-008 uses the current versioned `PriceQuantizer`; significant digits and decimal places are separate constraints. Generic decimal rounding is forbidden.
3. QF-009/010 consume levels in book order. Multiplication/division is checked. Filled, spent and residual fields preserve conservation.
4. QF-016 applies gross conversion, actual debit-asset fee semantics, output legality and minimums in the source-defined order. The exact legal net output becomes the next leg input; no recomputed ideal amount is permitted.
5. Comparisons at lot/tick/limit boundaries use exact domain values. A floating model proposal is finite/range-checked and conservatively discretized before a gate.
6. Sums use deterministic ordering; no hash-map iteration or thread completion order may change a result. Compensated summation may be used for floating research if identically specified/versioned; it is not silently introduced.
7. Integer overflow must be detected or prevented with a proven wider domain. The concrete integer width/decimal library remains open implementation design.
8. NaN is never a missing-value encoding; infinity is never emitted as a decision value. Conceptual infinity produces a typed outcome (`NO_DEPTH`, `NO_BREAK_EVEN`).

## Tolerance policy

Exact equality: ticks, lots, fill quantities, residuals, fee asset deltas, minimum/validity predicates, boolean gates, confidence categories, IDs, versions and failure reasons. Formula-specific floating tolerance: logs, roots, integrals, expectations, learned probabilities, quantiles and diagnostic ratios. Each vector states absolute/relative tolerance and reference algorithm. A tolerance cannot cross a sign, threshold, category, lot/tick or hard-risk boundary.

## Open numerical choices

Finite-sample QF-061/062 quantile/tie/interpolation; QF-041/043/064/109/110 source-omitted invalid cases; exact QF-047 time-grid crossing; QF-053 integration/tail truncation; QF-091 LCB estimator; QF-094 censoring estimator; QF-096 epsilon; sizing grid/refinement and portfolio solver. These are registered and must be versioned once validated.
