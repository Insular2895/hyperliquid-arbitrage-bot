# Verified Formula Index — PASS11

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

SRC-004 was fully reread. `M§` links the canonical master section; `D` links the individual-audit deep spec. External `Y` means revalidation required, not performed. Every QF requires a golden vector.

| ID | Name | Final status | Master | Deep | SRC-004 lines | Consumers | External | Golden | Audit result |
|---|---|---|---|---|---|---:|---|---|---|
| QF-001 | Mid Price | LOCKED | [M10] | [D02] | 3519–3536 | 3 | N | Y | VERIFIED |
| QF-002 | Absolute Spread | LOCKED | [M10] | [D02] | 3563–3588 | 3 | N | Y | VERIFIED |
| QF-003 | Relative Spread | LOCKED | [M10] | [D02] | 3589–3640 | 2 | N | Y | VERIFIED |
| QF-004 | Cumulative Base Depth | LOCKED | [M10] | [D02] | 3651–3682 | 3 | N | Y | VERIFIED |
| QF-005 | Cumulative Quote Depth | LOCKED | [M10] | [D02] | 3683–3709 | 3 | N | Y | VERIFIED |
| QF-006 | Depth Within Price Band | LOCKED | [M10] | [D02] | 3719–3792 | 3 | N | Y | VERIFIED |
| QF-007 | Size Quantization | LOCKED | [M11] | [D02] | 3793–3826 | 3 | Y | Y | VERIFIED / REVALIDATE |
| QF-008 | Price Validity | LOCKED EXCHANGE RULE | [M11] | [D02] | 3827–3847 | 3 | Y | Y | VERIFIED / REVALIDATE |
| QF-009 | Book Walk Base→Quote | LOCKED | [M11] | [D02] | 3848–3913 | 3 | Y | Y | VERIFIED / PARTIAL EXPLICIT |
| QF-010 | Book Walk Quote→Base | LOCKED | [M11] | [D02] | 3914–3971 | 3 | Y | Y | VERIFIED / PARTIAL EXPLICIT |
| QF-011 | VWAP | LOCKED | [M11] | [D02] | 3972–4012 | 3 | N | Y | VERIFIED |
| QF-012 | Mechanical Slippage BUY | LOCKED | [M11] | [D02] | 4013–4076 | 3 | N | Y | VERIFIED |
| QF-013 | Mechanical Slippage SELL | LOCKED | [M11] | [D02] | 4077–4120 | 3 | N | Y | VERIFIED |
| QF-014 | Fee Rate | LOCKED SOURCE, DYNAMIC VALUE | [M12] | [D02] | 4121–4148 | 3 | Y | Y | VERIFIED / REVALIDATE |
| QF-015 | Fee Amount | LOCKED | [M12] | [D02] | 4149–4181 | 3 | Y | Y | VERIFIED / REVALIDATE |
| QF-016 | NetConvert | LOCKED ARCHITECTURE | [M12] | [D02] | 4182–4325 | 5 | Y | Y | VERIFIED / REVALIDATE |
| QF-017 | Direct Route Output | LOCKED | [M13] | [D03] | 4326–4358 | 3 | Y | Y | VERIFIED |
| QF-018 | Two-Leg Indirect Output | LOCKED | [M13] | [D03] | 4359–4415 | 3 | Y | Y | VERIFIED |
| QF-019 | OWA Relative Edge | LOCKED | [M13] | [D03] | 4416–4466 | 3 | N | Y | VERIFIED |
| QF-020 | OWA Absolute Gain | LOCKED | [M13] | [D03] | 4467–4493 | 3 | N | Y | VERIFIED |
| QF-021 | Triangular Output | LOCKED | [M13] | [D03] | 4494–4572 | 3 | Y | Y | VERIFIED |
| QF-022 | Triangle Return | LOCKED | [M13] | [D03] | 4573–4597 | 2 | N | Y | VERIFIED |
| QF-023 | Triangle PnL | LOCKED | [M13] | [D03] | 4598–4616 | 3 | N | Y | VERIFIED |
| QF-024 | Conversion Alpha | LOCKED | [M14] | [D03] | 4617–4671 | 3 | N | Y | VERIFIED |
| QF-025 | Execution Alpha MT | LOCKED | [M14] | [D03] | 4672–4739 | 3 | N | Y | VERIFIED |
| QF-026 | Edge Curve | LOCKED OBJECT | [M14] | [D03] | 4740–4765 | 3 | Y | Y | VERIFIED |
| QF-027 | Maximum Profitable Size | LOCKED DEFINITION | [M14] | [D03] | 4766–4803 | 3 | N | Y | VERIFIED |
| QF-028 | Queue Imbalance | LOCKED | [M15] | [D04] | 4804–4859 | 2 | N | Y | VERIFIED |
| QF-029 | Multi-Level Imbalance | LOCKED / CALIBRATED WEIGHTS | [M15] | [D04] | 4860–4925 | 2 | N | Y | VERIFIED |
| QF-030 | Bid OFI Contribution | LOCKED DEFINITION | [M15] | [D04] | 4926–4971 | 2 | N | Y | VERIFIED |
| QF-031 | Ask OFI Contribution | LOCKED | [M15] | [D04] | 4972–5008 | 2 | N | Y | VERIFIED |
| QF-032 | OFI | LOCKED | [M15] | [D04] | 5009–5041 | 2 | N | Y | VERIFIED |
| QF-033 | Multi-Level OFI | LOCKED STRUCTURE / CALIBRATED WEIGHTS | [M15] | [D04] | 5051–5094 | 2 | N | Y | VERIFIED |
| QF-034 | Microprice | LOCKED | [M15] | [D04] | 5095–5154 | 3 | N | Y | VERIFIED |
| QF-035 | Microprice Dislocation | LOCKED | [M15] | [D04] | 5155–5232 | 2 | N | Y | VERIFIED |
| QF-036 | Log Return | LOCKED | [M16] | [D04] | 5233–5262 | 2 | N | Y | VERIFIED |
| QF-037 | Realized Variance | LOCKED | [M16] | [D04] | 5263–5281 | 2 | N | Y | VERIFIED |
| QF-038 | Realized Volatility | LOCKED | [M16] | [D04] | 5282–5298 | 3 | N | Y | VERIFIED |
| QF-039 | Robust Jump Score | LOCKED STRUCTURE / CALIBRATED THRESHOLD | [M16] | [D04] | 5299–5363 | 3 | N | Y | VERIFIED |
| QF-040 | Depth Participation | LOCKED | [M17] | [D04] | 5364–5409 | 3 | N | Y | VERIFIED |
| QF-041 | Volume Participation | LOCKED | [M17] | [D04] | 5410–5446 | 3 | N | Y | VERIFIED / OPEN ZERO RULE |
| QF-042 | Mechanical Impact | LOCKED | [M17] | [D04] | 5460–5515 | 3 | N | Y | VERIFIED |
| QF-043 | Liquidity Resilience | LOCKED | [M17] | [D04] | 5516–5583 | 3 | N | Y | VERIFIED / OPEN ZERO RULE |
| QF-044 | Survival Function | LOCKED OBJECT | [M18] | [D05] | 5584–5610 | 3 | N | Y | VERIFIED |
| QF-045 | Discrete Hazard | LEARNED | [M18] | [D05] | 5611–5674 | 3 | N | Y | VERIFIED |
| QF-046 | Survival from Hazard | LOCKED | [M18] | [D05] | 5675–5693 | 2 | N | Y | VERIFIED / LEGACY FIX |
| QF-047 | Edge Half-Life | LOCKED | [M18] | [D05] | 5694–5726 | 2 | N | Y | VERIFIED |
| QF-048 | Capture Probability | LOCKED | [M18] | [D05] | 5727–5784 | 3 | N | Y | VERIFIED |
| QF-049 | Expected Edge at Arrival | LEARNED DISTRIBUTION | [M18] | [D05] | 5785–5817 | 4 | N | Y | VERIFIED |
| QF-050 | Probability Above Threshold | LEARNED | [M18] | [D05] | 5818–5861 | 4 | N | Y | VERIFIED |
| QF-051 | Maker Fill Survival | LEARNED | [M19] | [D05] | 5862–5889 | 4 | N | Y | VERIFIED |
| QF-052 | Maker Fill CDF | LOCKED FROM SURVIVAL | [M19] | [D05] | 5890–5925 | 3 | N | Y | VERIFIED |
| QF-053 | Expected Fill Time | LOCKED DEFINITION | [M19] | [D05] | 5926–5971 | 3 | N | Y | VERIFIED / OPEN TAIL POLICY |
| QF-054 | Adverse Selection BUY | LOCKED | [M19] | [D05] | 5972–6021 | 3 | N | Y | VERIFIED |
| QF-055 | Adverse Selection SELL | LOCKED | [M19] | [D05] | 6022–6054 | 3 | N | Y | VERIFIED |
| QF-056 | Expected Value | LOCKED | [M20] | [D06] | 6055–6081 | 3 | N | Y | VERIFIED |
| QF-057 | Execution EV | LOCKED STRUCTURE | [M20] | [D06] | 6082–6149 | 3 | N | Y | VERIFIED |
| QF-058 | MT EV | LOCKED STRUCTURE / LEARNED COMPONENTS | [M20] | [D06] | 6150–6245 | 3 | N | Y | VERIFIED |
| QF-059 | Probability Positive PnL | LOCKED | [M20] | [D06] | 6246–6282 | 3 | N | Y | VERIFIED |
| QF-060 | Loss Variable | LOCKED | [M20] | [D06] | 6283–6313 | 3 | N | Y | VERIFIED |
| QF-061 | VaR | LOCKED | [M21] | [D06] | 6314–6342 | 3 | N | Y | VERIFIED / OPEN ESTIMATOR |
| QF-062 | Expected Shortfall | LOCKED | [M21] | [D06] | 6343–6391 | 3 | N | Y | VERIFIED / OPEN ESTIMATOR |
| QF-063 | Risk-Adjusted EV | CALIBRATED | [M21] | [D06] | 6392–6491 | 3 | N | Y | VERIFIED |
| QF-064 | Inventory Deviation | LOCKED | [M22] | [D07] | 6492–6517 | 3 | N | Y | VERIFIED / OPEN ZERO BAND |
| QF-065 | Soft Inventory Penalty | CALIBRATED | [M22] | [D07] | 6518–6542 | 3 | N | Y | VERIFIED |
| QF-066 | Hard Inventory Gate | LOCKED | [M22] | [D07] | 6543–6589 | 3 | N | Y | VERIFIED |
| QF-067 | Inventory Net Flow | LOCKED | [M22] | [D07] | 6590–6622 | 3 | N | Y | VERIFIED |
| QF-068 | Exit Cost | LOCKED STRUCTURE | [M22] | [D07] | 6623–6692 | 4 | Y | Y | VERIFIED |
| QF-069 | Stranded Penalty | CALIBRATED STRUCTURE | [M22] | [D07] | 6693–6763 | 3 | N | Y | VERIFIED |
| QF-070 | Bridge Cost | LOCKED STRUCTURE | [M23] | [D07] | 6764–6820 | 3 | Y | Y | VERIFIED |
| QF-071 | Bridge Break-Even Cycles | LOCKED | [M23] | [D07] | 6821–6886 | 2 | N | Y | VERIFIED |
| QF-072 | Capital Relocation Value | LOCKED STRUCTURE | [M23] | [D07] | 6887–7003 | 3 | N | Y | VERIFIED |
| QF-073 | Available Balance | LOCKED | [M24] | [D07] | 7004–7078 | 3 | N | Y | VERIFIED |
| QF-074 | Available Book Capacity | LOCKED | [M24] | [D07] | 7079–7140 | 3 | N | Y | VERIFIED |
| QF-075 | Optimal Sizing | LOCKED OPTIMIZATION PROBLEM | [M25] | [D07] | 7141–7273 | 3 | Y | Y | VERIFIED |
| QF-076 | Validated Capacity | LOCKED DEFINITION | [M25] | [D07] | 7274–7313 | 3 | N | Y | VERIFIED |
| QF-077 | Sizing Search | LOCKED ALGORITHM | [M25] | [D07] | 7314–7342 | 2 | N | Y | VERIFIED / CONFIG OPEN |
| QF-078 | Portfolio Allocation | LOCKED OPTIMIZATION PROBLEM | [M26] | [D07] | 7343–7380 | 3 | N | Y | VERIFIED / SOLVER OPEN |
| QF-079 | Recovery Objective | LOCKED | [M27] | [D07] | 7381–7468 | 3 | Y | Y | VERIFIED |
| QF-080 | Recovery Loss | LOCKED | [M27] | [D07] | 7469–7546 | 3 | N | Y | VERIFIED |
| QF-081 | Cross-Market Response | LEARNED | [M28] | [D08] | 7547–7587 | 4 | N | Y | VERIFIED |
| QF-082 | Correction Velocity | LOCKED | [M28] | [D08] | 7588–7638 | 2 | N | Y | VERIFIED |
| QF-083 | Competition Hazard | LEARNED | [M28] | [D08] | 7639–7659 | 4 | N | Y | VERIFIED |
| QF-084 | Infrastructure Latency | LOCKED DECOMPOSITION | [M29] | [D08] | 7660–7765 | 3 | N | Y | VERIFIED |
| QF-085 | Capture vs Infrastructure | LOCKED | [M29] | [D08] | 7766–7801 | 3 | N | Y | VERIFIED |
| QF-086 | Infra Gross PnL Difference | LOCKED | [M29] | [D08] | 7802–7855 | 3 | N | Y | VERIFIED |
| QF-087 | Incremental Infra Cost | LOCKED | [M29] | [D08] | 7856–7890 | 2 | N | Y | VERIFIED |
| QF-088 | Net Upgrade Value | LOCKED | [M29] | [D08] | 7891–7925 | 3 | N | Y | VERIFIED |
| QF-089 | Infrastructure ROI | LOCKED | [M29] | [D08] | 7926–7971 | 2 | N | Y | VERIFIED |
| QF-090 | Infrastructure Net PnL | LOCKED | [M29] | [D08] | 7972–8035 | 3 | N | Y | VERIFIED |
| QF-091 | Infrastructure Upgrade Gate | CALIBRATED SAFETY FACTOR | [M29] | [D08] | 8036–8076 | 3 | N | Y | VERIFIED / ESTIMATOR OPEN |
| QF-092 | Infrastructure Efficiency | LOCKED | [M29] | [D08] | 8077–8123 | 3 | N | Y | VERIFIED / ZERO RULE OPEN |
| QF-093 | Capture Ratio | LOCKED | [M29] | [D08] | 8124–8227 | 3 | N | Y | VERIFIED / ZERO RULE OPEN |
| QF-094 | Observed Survival | LOCKED | [M29] | [D08] | 8228–8274 | 3 | N | Y | VERIFIED / CENSOR POLICY OPEN |
| QF-095 | Brier Score | LOCKED | [M30] | [D09] | 8275–8308 | 2 | N | Y | VERIFIED |
| QF-096 | Log Loss | LOCKED | [M30] | [D09] | 8309–8360 | 2 | N | Y | VERIFIED / EPSILON OPEN |
| QF-097 | PnL Prediction Error | LOCKED | [M30] | [D09] | 8361–8430 | 3 | N | Y | VERIFIED |
| QF-098 | Slippage Prediction Error | LOCKED | [M30] | [D09] | 8431–8486 | 3 | N | Y | VERIFIED |
| QF-099 | Fill Calibration Error | SOURCE_DERIVED_FROM_CONTEXT | [M30] | [D09] | 8487–8559 | 3 | N | Y | VERIFIED / STATUS RESOLVED |
| QF-100 | Model Economic Lift | LOCKED | [M30] | [D09] | 8560–8611 | 3 | N | Y | VERIFIED |
| QF-101 | Model Value after Latency | LOCKED DEFINITION | [M31] | [D09] | 8612–8701 | 4 | N | Y | VERIFIED |
| QF-102 | Model Disagreement | LOCKED FEATURE | [M31] | [D09] | 8702–8750 | 3 | N | Y | VERIFIED |
| QF-103 | OOD Distance | MODEL DEPENDENT | [M31] | [D09] | 8751–8781 | 3 | N | Y | VERIFIED / STATUS FIXED |
| QF-104 | Simulation Confidence | SOURCE-EXPLICIT GATED CONTRACT | [M31] | [D09] | 8782–8832 | 3 | N | Y | VERIFIED / NON-SCALAR |
| QF-105 | Expected Idle Cost | CALIBRATED | [M32] | [D10] | 8833–8890 | 3 | N | Y | VERIFIED |
| QF-106 | Global Economic PnL | SOURCE_DERIVED_FROM_CONTEXT | [M32] | [D10] | 8891–8984 | 3 | N | Y | VERIFIED / STATUS PROVENANCE |
| QF-107 | Inventory Mark-to-Market | SOURCE_DERIVED_FROM_CONTEXT | [M32] | [D10] | 8985–9048 | 3 | N | Y | VERIFIED / STATUS PROVENANCE |
| QF-108 | Total Strategy PnL | SOURCE_DERIVED_FROM_CONTEXT | [M32] | [D10] | 9049–9147 | 3 | N | Y | VERIFIED / STATUS PROVENANCE |
| QF-109 | Drawdown | SOURCE_DERIVED_FROM_CONTEXT | [M33] | [D10] | 9148–9204 | 3 | N | Y | VERIFIED / ZERO PEAK OPEN |
| QF-110 | Maximum Drawdown | SOURCE_DERIVED_FROM_CONTEXT | [M33] | [D10] | 9205–9224 | 3 | N | Y | VERIFIED / EMPTY INTERVAL OPEN |

Expected `110`; indexed `110`; missing `0`; duplicate `0`; every row has master/deep locators, source, consumer count, flags and audit result.

[M10]: ../04_FORMULA_BOOK.md#10-pricing--spread--depth--qf-001006
[M11]: ../04_FORMULA_BOOK.md#11-precision--book-walking--qf-007013
[M12]: ../04_FORMULA_BOOK.md#12-fees--netconvert--qf-014016
[M13]: ../04_FORMULA_BOOK.md#13-routes--owa--triangle--qf-017023
[M14]: ../04_FORMULA_BOOK.md#14-conversionalpha--executionalpha--edge--qf-024027
[M15]: ../04_FORMULA_BOOK.md#15-microstructure--ofi--microprice--qf-028035
[M16]: ../04_FORMULA_BOOK.md#16-volatility--jumps--qf-036039
[M17]: ../04_FORMULA_BOOK.md#17-liquidity--participation--resilience--qf-040043
[M18]: ../04_FORMULA_BOOK.md#18-survival--capture--qf-044050
[M19]: ../04_FORMULA_BOOK.md#19-maker-fill--adverse-selection--qf-051055
[M20]: ../04_FORMULA_BOOK.md#20-ev--pnl-distributions--qf-056060
[M21]: ../04_FORMULA_BOOK.md#21-var--es--raev--qf-061063
[M22]: ../04_FORMULA_BOOK.md#22-inventory--qf-064069
[M23]: ../04_FORMULA_BOOK.md#23-bridge--relocation--qf-070072
[M24]: ../04_FORMULA_BOOK.md#24-balance--book-capacity--qf-073074
[M25]: ../04_FORMULA_BOOK.md#25-sizing--q_validated--qf-075077
[M26]: ../04_FORMULA_BOOK.md#26-multi-op-allocation--qf-078
[M27]: ../04_FORMULA_BOOK.md#27-recovery--qf-079080
[M28]: ../04_FORMULA_BOOK.md#28-cross-market--competition--qf-081083
[M29]: ../04_FORMULA_BOOK.md#29-infrastructure-economics--qf-084094
[M30]: ../04_FORMULA_BOOK.md#30-calibration--prediction-errors--qf-095100
[M31]: ../04_FORMULA_BOOK.md#31-model-value--ood--confidence--qf-101104
[M32]: ../04_FORMULA_BOOK.md#32-idle-capital--accounting--qf-105108
[M33]: ../04_FORMULA_BOOK.md#33-drawdown--mdd--qf-109110
[D02]: ../deep-specs/formulas/02_QF001_QF016_PRICING_DEPTH_PRECISION_FEES_NETCONVERT.md
[D03]: ../deep-specs/formulas/03_QF017_QF027_ROUTES_OWA_TRIANGLE_AND_ALPHA.md
[D04]: ../deep-specs/formulas/04_QF028_QF043_MICROSTRUCTURE_VOLATILITY_AND_LIQUIDITY.md
[D05]: ../deep-specs/formulas/05_QF044_QF055_SURVIVAL_CAPTURE_MAKER_AND_ADVERSE_SELECTION.md
[D06]: ../deep-specs/formulas/06_QF056_QF063_EV_VAR_ES_AND_RISK_ADJUSTED_VALUE.md
[D07]: ../deep-specs/formulas/07_QF064_QF080_INVENTORY_BRIDGE_SIZING_ALLOCATION_AND_RECOVERY.md
[D08]: ../deep-specs/formulas/08_QF081_QF094_CROSS_MARKET_COMPETITION_AND_INFRASTRUCTURE.md
[D09]: ../deep-specs/formulas/09_QF095_QF104_CALIBRATION_MODEL_VALUE_OOD_AND_CONFIDENCE.md
[D10]: ../deep-specs/formulas/10_QF105_QF110_CAPITAL_ACCOUNTING_AND_DRAWDOWN.md
