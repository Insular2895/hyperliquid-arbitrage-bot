# Global Notation, Units, Signs and Numerical Policy

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Contract

The symbol registry is [GLOBAL_SYMBOL_TABLE](../../_analysis/pass11_formula_book/GLOBAL_SYMBOL_TABLE.md) and the dimensional proof is [GLOBAL_UNIT_AND_DIMENSION_MATRIX](../../_analysis/pass11_formula_book/GLOBAL_UNIT_AND_DIMENSION_MATRIX.md). Formula-local names override no global meaning; ambiguous `q`, `P`, `L`, `S` or `E` must be qualified at the API/schema boundary.

## Unit taxonomy

| Class | Canonical representation | Examples |
|---|---|---|
| asset quantity | asset-qualified base/quote unit or integer lots | `q_A`, `I_a`, fill size |
| price | quote units per base unit or integer ticks plus scale | Bid, Ask, VWAP, Mid |
| value/PnL/cost | explicit asset or chosen numeraire | `Gain_B`, `EconomicPnL`, ES |
| ratio/probability | dimensionless | edge, QI, survival, Brier |
| bps | labelled dimensionless scale | `ratio×10^4`; `1 bp=10^-4` |
| time | declared unit and clock/domain | latency, fill time, horizon |
| hazard | probability per discrete bin or rate per time | `h_k`, `λ_c` |
| count/cycles | integer/count unit | `N`, `N_BE` |

No sum/subtraction may cross assets, currencies, horizons or time bases without a named conversion. No implicit percent↔fraction↔bps conversion is permitted.

## Direction and sign constitution

`BaseToQuote` sells base into bids; `QuoteToBase` buys base from asks. Positive PnL/gain/edge is favorable. Positive BUY/SELL slippage, mechanical impact and adverse selection is a cost. `Loss=-PnL`; upper positive Loss is the loss tail. A positive `PnLError` means actual PnL exceeded forecast, while positive `SlippageError` means actual execution cost exceeded forecast. `ΔI_a>0` is inventory inflow; bridge/recovery/infra costs are positive burdens.

## Fixed-point boundary and rounding

Exchange-bound quantities, prices, reservations, available balance/capacity and final order comparisons use integer lots/ticks or mathematically equivalent exact fixed point. Non-exceeding size quantization uses floor. Price validity uses a versioned exchange-aware quantizer. Each NetConvert leg walks the selected immutable book, applies the actual fee-debit contract and quantizes exactly once at the specified boundary before its output becomes the next input. Rounding mode and scale are part of Formula/MetadataVersion.

Floating point is permitted for learned models, distributions, integrals, regressions and diagnostic ratios. A floating result may drive an order only after finite/range validation and conversion to the exact legal boundary. Never use a single global tolerance.

## Zero, NaN, infinity and overflow

Preconditions decide whether a zero is valid. Division by zero, `log(nonpositive)`, square root of a negative value, empty quantile/sample, invalid probability, NaN and overflow produce typed invalid/unknown results and fail closed. Conceptual `+∞` in QF-040 or QF-071 is a decision semantic (`reject`/`never breaks even`), not a serializable floating value. Integer multiplication/summation must be checked or safely widened; the concrete integer width/decimal library remains an implementation choice.

## Status boundary

- `LOCKED` fixes the equation and semantic contract.
- `CALIBRATED` fixes structure while parameter values come from evidence/config.
- `LEARNED` fixes target/contract while output comes from a versioned artifact.
- `MODEL DEPENDENT` fixes range/direction and provenance, not an estimator.
- `SOURCE_DERIVED_FROM_CONTEXT` is used only where SRC-004 gives a fixed definition but omits a formal headline status.
- External rules remain versioned and revalidated; they are not silently promoted to timeless constants.

## Version and evidence tuple

Every evaluation is attributable to `FormulaVersion`, input state/BookVersion, metadata/fee/config versions, event/evaluation time and consumer. Learned outputs also carry feature schema, model/artifact and training/validation identities. Golden vectors record exact inputs, expected output or expected typed failure, arithmetic domain and tolerance.
