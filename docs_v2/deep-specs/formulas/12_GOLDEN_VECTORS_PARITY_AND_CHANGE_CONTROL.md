# Golden Vectors, Parity and Change Control

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Golden vector schema

Each vector records `vector_id`, QF ID/version, exact input values and units, state/metadata/fee/config/model versions, arithmetic domain, expected value or typed failure, tolerance if applicable, source/provenance and consumers. Boundary vectors include zero/empty/negative/nonfinite inputs, exact lot/tick/threshold equality, one unit below/above, insufficient depth and overflow candidates.

## Mandatory source vectors

- `GV-SRC-001`: Bid 99, Ask 101 → QF-001 Mid 100, QF-002 Spread 2, QF-003 200 bps.
- `GV-SRC-002`: asks 100×2 and 101×3; a BUY of 4 base spends 402 quote, QF-011 VWAP 100.5 and QF-012 slippage 50 bps from Ask 100.

The catalog adds mandatory vectors for QF-007/008 precision, both walk directions/partial fills, fee debit assets/rebates, NetConvert sequential composition, OWA/Triangle denominators and closure, OFI equality branches, hazard product index `1..k`, censored half-life, EV partitions, Loss/VaR/ES, hard limits, discrete sizing, shared capacity, Recovery sunk-cost exclusion, like-for-like infrastructure comparisons, log clipping, QF-099 sign, categorical confidence, accounting and drawdown.

## Equality and tolerance

Ticks, lots, quantized sizes/prices, actual fee-asset deltas, reservations/capacity, identifiers, categories, booleans, state transitions and expected failure codes require exact equality. Rational examples representable in the selected exact scale also require equality. Learned/continuous distribution outputs, logs, integrals, roots and other floating analytics use per-QF absolute and relative tolerances derived from reference conditioning and documented in the vector. Probability range/normalization and sign invariants remain exact predicates. No global epsilon masks semantic drift.

## Rust/Python parity

Both languages consume the same serialized vectors, version tuple and canonical input ordering. Exchange-boundary logic is compared after the same quantization with exact equality. Floating outputs compare value, validity/failure, units and invariants under the vector's tolerances. Parity tests reject language-specific default rounding, unordered iteration, NaN payload differences used as values and inconsistent empirical quantile/bin definitions.

## Replay

`RunManifest` and every decision-relevant trace resolve FormulaVersion plus metadata/fee/config and applicable model versions. Historical Replay uses the historical formula/version and point-in-time parameters. Counterfactual Replay under new semantics is separately labelled and never overwrites historical truth. The first FormulaVersion divergence must be reportable.

## Change control

A semantic formula change increments FormulaVersion, revises affected vectors, performs dependency/consumer/Risk/model impact analysis, reruns Rust/Python parity and golden Replay, and invalidates dependent CapabilityManifest evidence until PASS10 gates are re-satisfied. Parameter-only or learned-artifact changes update their own version and dependent evidence even if the locked equation is unchanged. Exchange-rule changes update external evidence and Metadata/Fee/Formula compatibility as applicable.
