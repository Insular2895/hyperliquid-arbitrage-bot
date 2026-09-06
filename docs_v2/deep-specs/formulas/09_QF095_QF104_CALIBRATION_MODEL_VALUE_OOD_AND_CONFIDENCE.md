# QF-095–QF-104 — Calibration, Model Value, OOD and Confidence

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-095 | `N^-1Σ(p_i-y_i)^2` | ratio score | aligned binary event/label; p∈[0,1], y∈{0,1}, N>0 | invalid probability/empty/misaligned sample invalid | perfect/worst/mixed and bounds |
| QF-096 | `-N^-1Σ[y_i ln p_i+(1-y_i)ln(1-p_i)]` | dimensionless loss | QF-095 alignment; p clipped `[ε,1-ε]`; 0<ε<.5 | no log(0); invalid ε/sample invalid | p=0/1 clipping, perfect/wrong labels; finite output |
| QF-097 | `RealizedPnL-PredictedPnL`; bias `E[PnLError]` | PnL numeraire | aligned outcome/opportunity/horizon/accounting | missing prediction/outcome/unit mismatch invalid | positive/negative/zero and sample bias |
| QF-098 | `ActualSlippage-PredictedSlippage` | same fraction or bps unit | same side/reference/order/horizon/unit | fraction-vs-bps or sign mismatch invalid | under/over/exact cost forecasts |
| QF-099 | `ObservedFillRate_B-MeanPredictedFill_B` | probability-point difference | nonempty bucket, aligned fill event/horizon/model and predictions | empty/misaligned bucket invalid; source status absence is documented | perfect calibration, under/overprediction; bucket boundary |
| QF-100 | `NetPnL_model-NetPnL_baseline` | numeraire | same dataset/opportunities/capital/fees/risk/accounting | non-comparable runs invalid | identical 0; model lift ±; cost parity |
| QF-101 | `PnL_with-PnL_without-PnLLostDueToAddedLatency-OperationalCost` | numeraire | like-for-like OOS experiment; disjoint latency/ops costs | in-sample/noncomparable or duplicated cost invalid | each term isolated and robust-positive gate |
| QF-102 | `p̄=M^-1Σp_m`; `sqrt(M^-1Σ(p_m-p̄)^2)` | probability dispersion | M>0; aligned event/horizon and p_m∈[0,1] | empty/misaligned/invalid prediction set invalid | unanimous 0, known two-model spread, permutation invariance |
| QF-103 | `OODScore≥0`; larger = farther outside support | model-defined score | identified estimator/artifact/support/version | negative/NaN/missing support rejects; no universal substitute | in-support/out-of-support order and range |
| QF-104 | six named gates → `HIGH/MEDIUM/LOW/REJECT` | ordered category | each gate evaluated under versioned explicit rules | missing/invalid gate cannot yield HIGH; REJECT blocks | truth table including every single-gate failure |

QF-099 source evidence: the SRC-004 section gives the fixed bucket difference and its interpretation but no bold formal status line. The surrounding calibration-metric closure and FormulaRegistry/golden governance support `SOURCE_DERIVED_FROM_CONTEXT`; this is not `SOURCE_EXPLICIT`. QF-103 is `MODEL DEPENDENT`, not LOCKED. QF-104 deliberately rejects a fixed weighted scalar confidence score.
