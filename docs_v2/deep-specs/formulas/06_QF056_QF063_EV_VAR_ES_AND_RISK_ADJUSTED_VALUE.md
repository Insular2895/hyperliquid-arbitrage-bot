# QF-056–QF-063 — EV, VaR, Expected Shortfall and Risk-Adjusted Value

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-056 | `EV=Σ_ip_iPnL_i`; `Σp_i=1` | explicit PnL numeraire | mutually exclusive/exhaustive scenarios; p_i∈[0,1] | probability mass/unit mismatch invalid | deterministic, mixed gain/loss, bad mass reject |
| QF-057 | `P_FE[PnL∣F]+P_PE[PnL∣P]+P_RE[PnL∣R]+P_XE[PnL∣X]` | PnL numeraire | F/P/R/X partition exclusive/exhaustive; conditional values aligned | missing/double-counted scenario or bad mass invalid | one-hot scenarios, weighted partition, overlap reject |
| QF-058 | `∫f_fill(t∣X)EV_leg2(t)dt-C_adverse-C_recovery`; discrete bin sum | PnL numeraire | valid fill distribution, time-varying leg-2 EV and disjoint costs | probability/support/unit mismatch invalid | analytic/discrete parity, no-fill mass, costs once |
| QF-059 | `P_+=P(PnL>0)`; MC `N^-1Σ1[PnL_i>0]` | probability | common PnL definition; N>0 for sample | empty sample invalid; PnL=0 is not positive | negative/zero/positive sample; strict indicator |
| QF-060 | `Loss=-PnL` | same numeraire | finite PnL | nonfinite/unitless invalid | gain→negative loss, loss→positive, zero |
| QF-061 | `VaR_α=F_Loss^{-1}(α)` | Loss numeraire | QF-060 distribution; 0<α<1 | empty distribution/bad α invalid; finite-sample interpolation remains open | analytic quantile and declared empirical method |
| QF-062 | continuous `E[Loss∣Loss≥VaR_α]`; robust `ES_α=(1-α)^-1∫_α^1VaR_u du` | Loss numeraire | valid distribution/VaR/α | empty tail/tie estimator ambiguity requires declared version; open finite-sample policy | continuous reference, empirical ties after policy closure |
| QF-063 | `RAEV=EV_execution-InventoryPenalty-StrandedPenalty-ModelUncertaintyPenalty` | common numeraire | all components aligned/disjoint; calibrated penalties | duplicated or unit-mismatched cost invalidates value | each penalty isolated; fee/slippage/recovery already in EV not subtracted again |

`Loss=-PnL` is the sole tail-risk sign conversion. ExpectedShortfall is the internal term. The robust quantile-integral definition is canonical; a finite-sample interpolation/tie rule must be closed and versioned before an implementation can claim identical empirical ES.

CORR-05 fixes the consumer semantics: F/P/R/X supplies one `Π_exec(q,state)` distribution; QF-059 and QF-060–062 derive from it. Arrival survival and empirical completion calibrate that distribution rather than discount it again. QF-063's three penalties remain external and non-overlapping. See [ExecutionEV Scenario Ownership](../../_analysis/corr05_economic_integration/EXECUTION_EV_SCENARIO_OWNERSHIP.md).
