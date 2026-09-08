# NetConvert Fast/Full Parity Contract

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

## Oracle

Canonical full-L2 `NetConvert` is the oracle. For every input where FastL1 declares eligible:

`FastL1(input) == FullL2(input)`

Equality is exchange-critical and covers bits/accepted fixed-point values as defined by the numeric contract, validity, reason code, completion, filled and residual quantities, gross/net outputs, fee rate/value/asset/deltas, VWAP, consumed-level evidence, timestamps and all versions.

## Test families

- both conversion directions;
- exact L1 boundary, one quantum below/above and insufficient L1;
- empty, invalid, crossed and stale books;
- protected BUY/SELL boundary and prohibited next level;
- fee in input, output or third asset; zero fee and rebate where supported;
- lot/tick/output quantization and minimum size/notional boundaries;
- zero, negative, overflow and precision-invalid input;
- multi-level books whose deeper values must be irrelevant when eligible;
- property/fuzz generation over broad valid rule/book state;
- golden, deterministic Replay and Shadow comparison.

Fast-ineligible cases must select full L2 and reproduce the baseline. Any eligibility false positive, output difference, reason difference, version difference or `DecisionTrace` difference fails promotion.
