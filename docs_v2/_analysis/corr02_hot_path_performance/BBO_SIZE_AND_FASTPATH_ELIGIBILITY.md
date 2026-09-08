# BBO Size and Fast-Path Eligibility

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

## Governing distinction

L1 size is an implementation eligibility condition, never a general economic validity rule.

| Condition | C3 result | Economic result |
|---|---|---|
| required legal input/output fits entirely at valid best level and all parity preconditions hold | `FAST_L1_ELIGIBLE` | run exact specialized QF-016 implementation |
| L1 is insufficient, ambiguous or protected-limit/rule proof is incomplete | `FALLBACK_REQUIRED` | run canonical full L2 |
| state invalid under existing contract | `NOT_EVALUABLE` through C1 | canonical invalid reason |
| separate complete C2 proof rejects | `NOT_NEEDED` | canonical conservative rejection |

## Directional obligations

For Base→Quote, the legal quantized base input must fit the best-bid executable quantity, the protected SELL constraint must allow that price, and fee/minimum/output transforms must not require deeper inspection.

For Quote→Base, the proof must derive the legal base quantity and quote spend under ask price, base-size quantization, quote/base/third-asset fees, minima and protected BUY price. The expression `quote_input <= ask_price × ask_qty` is not sufficient by itself.

A partial L1 result never competes with the full evaluator. Ineligibility emits no alternative economic output.
