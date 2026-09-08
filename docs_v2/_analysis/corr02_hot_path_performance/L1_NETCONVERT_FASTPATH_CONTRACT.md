# L1 NetConvert Fast-Path Contract

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

`FastL1NetConvert` is a possible implementation specialization of QF-016, not a new formula, result type or economic primitive.

## Eligibility contract

The caller supplies the same immutable identity, direction, positive typed quantity, BookVersion, MetadataVersion, FeeVersion, execution/protected-price context and FormulaVersion as full `NetConvert`. Eligibility requires:

1. valid immutable book and coherent best side;
2. exact direction and asset roles;
3. current fee, precision, lot/tick, minimum and debit-asset rules known;
4. protected price permits the best level;
5. legal quantized consumption can be completed at L1;
6. no output, fee or minimum calculation needs deeper levels;
7. all arithmetic uses the canonical numeric policy and operation ordering.

## Result

When eligible, it returns exactly the canonical `NetConvert` shape: filled/unfilled input, gross/net output, actual asset deltas including `FeeAssetDelta`, fee evidence, VWAP, consumed-level evidence, residual/dust, completion, validity/reason, timestamps and every consumed version.

When any condition is unproved, it returns only `FALLBACK_REQUIRED`. It cannot return a partial competing result or a tradable rejection.

## Change control

FastL1 changes traversal only. `FormulaVersion`, QF-016, fees, minima, quantization, route composition, protected prices and failure semantics do not change. A later implementation must be removable without changing replayed economic truth.
