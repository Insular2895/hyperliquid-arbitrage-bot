# Formula Deep Specifications

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

This directory is the implementation audit layer for the canonical [Formula Book](../../04_FORMULA_BOOK.md). It preserves one QF identity per source contract and supplies the conditions, failures and test requirements that a compact master table cannot fully express.

| File | Scope |
|---|---|
| [01](01_GLOBAL_NOTATION_UNITS_SIGNS_AND_NUMERICAL_POLICY.md) | notation, units, signs, fixed-point/float boundary, invalid-number policy |
| [02](02_QF001_QF016_PRICING_DEPTH_PRECISION_FEES_NETCONVERT.md) | QF-001–016 |
| [03](03_QF017_QF027_ROUTES_OWA_TRIANGLE_AND_ALPHA.md) | QF-017–027 |
| [04](04_QF028_QF043_MICROSTRUCTURE_VOLATILITY_AND_LIQUIDITY.md) | QF-028–043 |
| [05](05_QF044_QF055_SURVIVAL_CAPTURE_MAKER_AND_ADVERSE_SELECTION.md) | QF-044–055 |
| [06](06_QF056_QF063_EV_VAR_ES_AND_RISK_ADJUSTED_VALUE.md) | QF-056–063 |
| [07](07_QF064_QF080_INVENTORY_BRIDGE_SIZING_ALLOCATION_AND_RECOVERY.md) | QF-064–080 |
| [08](08_QF081_QF094_CROSS_MARKET_COMPETITION_AND_INFRASTRUCTURE.md) | QF-081–094 |
| [09](09_QF095_QF104_CALIBRATION_MODEL_VALUE_OOD_AND_CONFIDENCE.md) | QF-095–104 |
| [10](10_QF105_QF110_CAPITAL_ACCOUNTING_AND_DRAWDOWN.md) | QF-105–110 |
| [11](11_FORMULA_DEPENDENCIES_AND_DOUBLE_COUNTING.md) | dependency and cost ownership |
| [12](12_GOLDEN_VECTORS_PARITY_AND_CHANGE_CONTROL.md) | vectors, Rust/Python parity, versioning |

The audit ledger, matrices and issue registers are under [`_analysis/pass11_formula_book`](../../_analysis/pass11_formula_book/FORMULA_AUDIT_LEDGER.md). SRC-004 is the equation/status authority; a deep spec cannot override it.
