# QF-081–QF-094 — Cross-Market, Competition and Infrastructure

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-081 | `R_i→j(h)=P(ΔMarket_j(h)∣Shock_i,X)` | learned distribution | ordered source/target markets, horizon, shock/features/artifact | unsupported/OOD/missing alignment → unavailable | distribution normalization, direction/horizon labels |
| QF-082 | `(E_0-E_h)/E_0` | ratio | aligned edge measure; E_0>0 | E_0≤0 or unit mismatch invalid | 0 no correction, 1 disappearance, >1 cross-zero |
| QF-083 | `λ_c(t∣X)` | hazard rate | defined edge-death event/time unit/features/model | negative/nonfinite/unsupported invalid | nonnegative range and global-before-cause behavior |
| QF-084 | `L_total=L_feed+L_compute+L_sign+L_send+L_exchange`; compute sub-sum | time | same clock/unit; nonnegative nonoverlapping stages | missing/double-counted stage invalidates attribution | exact sum, zero stages, boundary instrumentation |
| QF-085 | `P_capture,s=E_{L_s}[S(L_s)]` | probability | QF-044/048 and valid server latency distribution | misaligned time/model/server invalid | deterministic and discrete latency vectors |
| QF-086 | `GrossPnL_candidate-GrossPnL_current` | numeraire | same opportunity universe/strategy/capital/horizon | incomparable cohorts invalid | identical→0, candidate better/worse |
| QF-087 | `Cost_candidate-Cost_current` | numeraire | same period/cost scope/currency | scope/unit mismatch invalid | positive/zero/negative incremental cost |
| QF-088 | `ΔGrossPnL-ΔCost` | numeraire | QF-086/087 aligned | invalid dependency propagates | gain/cost combinations |
| QF-089 | `ΔGrossPnL/ΔCost` | ratio | aligned QF-086/087; ΔCost>0 | zero/negative ΔCost: ratio invalid; use NetPnL/value | positive ratio, zero/negative denominator |
| QF-090 | `GrossTradingPnL-TradingCosts-InfrastructureCost` | numeraire | disjoint cost components, same period | repeated/omitted cost invalid | each component isolated, reconciliation equality |
| QF-091 | `LCB_α(ΔGrossPnL)>SF×ΔCost` | boolean over numeraire | valid like-for-like distribution; α/SF calibrated | missing uncertainty/evidence fails gate | equality fails strict gate; strong/weak LCB |
| QF-092 | `NetPnL/InfraCost` | ratio | aligned scope; InfraCost>0 | denominator≤0 invalid diagnostic | positive case, zero/negative reject |
| QF-093 | `ΣRealizedPnL/ΣExpectedExecutablePnL` | ratio | same eligible set/numeraire; denominator>0 | zero/negative denominator or cohort mismatch invalid | ratio-of-sums vs mean-of-ratios counterexample |
| QF-094 | `N_alive(h)/N_eligible` | probability | eligible cohort, horizon, censoring policy; N_eligible>0 | empty cohort invalid; censored naïve count forbidden | all/none/some alive and censored cohort |

Infrastructure comparisons are like-for-like experiments, not raw host scorecards. Latency components must have nonoverlapping boundaries; attribution uncertainty remains evidence, not a hidden correction term. QF-093 is explicitly a ratio of sums.

CORR-05 assigns one coherent outcome distribution to each profile. QF-085, completion evidence and lost/recoverable-PnL attribution inform or validate that distribution; they are not stackable multipliers. QF-086 compares its gross outcomes, QF-087/QF-090 charge incremental infrastructure cost once, and QF-093 remains diagnostic rather than completion probability.
