# PASS 02 — Participant Formula Crosscheck

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 02 REVIEW COMPLETE`

SRC-004 is authoritative. Expressions below were reopened in the original Formula Book, not copied from legacy documentation. `LOCKED` means mathematical definition/structure; `LEARNED` means the distribution or coefficients require data; `CALIBRATED` parameters remain versioned.

## Microstructure

| Formula | Status | Authoritative expression / rule | PASS 02 use | Result |
|---|---|---|---|---|
| QF-028 Queue Imbalance | `LOCKED` | `QI=(Q_bid-Q_ask)/(Q_bid+Q_ask)`; zero denominator invalid. | Feature. | Verified. |
| QF-029 Multi-Level Imbalance | `LOCKED` structure; weights `CALIBRATED` | Weighted bid-minus-ask depth divided by weighted total depth. | Feature. | Verified; dependency recovered. |
| QF-030 Bid OFI contribution | `LOCKED` | `e^b_n=1[P^b_n>=P^b_{n-1}]Q^b_n-1[P^b_n<=P^b_{n-1}]Q^b_{n-1}`. | Event OFI. | Verified; equality cases preserved. |
| QF-031 Ask OFI contribution | `LOCKED` | `e^a_n=1[P^a_n<=P^a_{n-1}]Q^a_n-1[P^a_n>=P^a_{n-1}]Q^a_{n-1}`. | Event OFI. | Verified. |
| QF-032 OFI | `LOCKED` | `OFI_n=e^b_n-e^a_n`; `OFI_W=sum_{n in W}OFI_n`. | Feature. | Verified. |
| QF-033 Multi-Level OFI | `LOCKED` structure; weights `CALIBRATED` | `MLOFI=sum_{k=1..K}w_k OFI^(k)`. | Feature. | Verified. |
| QF-034 Microprice | `LOCKED` | `(Ask*Q_bid+Bid*Q_ask)/(Q_bid+Q_ask)`. | Feature. | Verified; must lie within valid BBO. |
| QF-035 Microprice Dislocation | `LOCKED` | `(MicroPrice-Mid)/Mid`; bps multiply by `10^4`. | Feature. | Verified. |

True event OFI and a snapshot-difference proxy are different features. No Formula Book number is invented for the proxy.

## Liquidity, survival and capture

| Formula | Status | Authoritative expression / rule | Boundary | Result |
|---|---|---|---|---|
| QF-043 Liquidity Resilience | `LOCKED` | `(D_t-D_s)/(D_0-D_s)`; display clamp optional, raw over-replenishment retained. | Invalid when denominator is zero. | Verified. |
| QF-044 Survival Function | `LOCKED` | `S(t|X)=P(T>t|X)`. | `T` is remaining economically executable edge lifetime. | Verified. |
| QF-045 Discrete Hazard | `LEARNED` | `h_k(X)=P(T in [t_k,t_{k+1})|T>=t_k,X)`; baseline may use `sigma(beta_k^T X)`. | Coefficients learned. | Verified. |
| QF-046 Survival from Hazard | `LOCKED` | `S_k=product_{j=1..k}(1-h_j)`. | Probability coherence required. | Verified. |
| QF-047 Edge Half-Life | `LOCKED` | `t50=inf{t:S(t)<=0.5}`. | If not crossed, report beyond model horizon. | Verified. |
| QF-048 Capture Probability | `LOCKED` | `P_capture=E_L[S(L)]`; histogram sum over latency buckets. | Uses full latency distribution. | Verified. |
| QF-049 Expected Edge at Arrival | `LEARNED` | `E_arrival=E[Edge_{t+L}|X_t]`. | No assumed exponential decay. | Verified; dependency recovered. |
| QF-050 Probability Above Execution Threshold | `LEARNED` | `P_exec=P(Edge_{t+L}>E_minimum|X_t)`. | `E_minimum` owned elsewhere. | Verified; dependency recovered. |

`S(E[L])` is not substituted for `E[S(L)]`. Positive arrival edge is not automatically executable if it is below the authoritative threshold.

## Maker

| Formula | Status | Authoritative expression / rule | Boundary | Result |
|---|---|---|---|---|
| QF-051 Maker Fill Survival | `LEARNED` | `S_f(t|X)=P(T_f>t|X)`. | Distribution learned. | Verified. |
| QF-052 Maker Fill CDF | `LOCKED` | `F_f(t|X)=1-S_f(t|X)=P(T_f<=t|X)`. | Coherent with survival. | Verified. |
| QF-053 Expected Fill Time | `LOCKED` | `E[T_f]=integral_0^infinity S_f(t)dt`; discrete sum analogue. | Conditioning within finite horizon must be declared. | Verified; dependency recovered. |
| QF-054 Adverse Selection BUY | `LOCKED` | `(P_f-Mid_{t_f+h})/P_f`; positive is adverse. | Horizon calibrated. | Verified. |
| QF-055 Adverse Selection SELL | `LOCKED` | `(Mid_{t_f+h}-P_f)/P_f`; positive is adverse. | Horizon calibrated. | Verified. |
| QF-058 MT EV | `LOCKED` structure | `sum_k P(T_f in B_k)EV_leg2(t_k)-C_adverse-C_recovery` (continuous analogue permitted). | **REFERENCE ONLY — Formula/Execution owned.** | Verified; not redefined. |

## Cross-market and validation

| Formula | Status | Authoritative expression / rule | PASS 02 use | Result |
|---|---|---|---|---|
| QF-081 Cross-Market Response | `LEARNED` | `R_{i->j}(h)=P(Delta Market_j(h)|Shock_i,X)`. | Sparse learned distribution. | Verified. |
| QF-082 Correction Velocity | `LOCKED` | `(E_0-E_h)/E_0`; `1` death, `>1` crosses zero. | Survival complement. | Verified. |
| QF-083 Competition Hazard | `LEARNED` | Competition hazard object; initial global edge hazard is more observable. | Cause decomposition later. | Verified. |
| QF-085 Capture vs Infrastructure | `LOCKED` | `P_capture,s=E_{L_s}[S(L_s)]`. | Infrastructure comparison. | Verified. |
| QF-094 Empirical Opportunity Survival | `LOCKED` | `ObservedSurvival(h)=N_alive(h)/N_eligible`; censored episodes handled correctly. | Validation baseline. | Verified. |
| QF-095 Brier | `LOCKED` | `(1/N)sum_i(p_i-y_i)^2`. | Probability calibration/error. | Verified; dependency recovered. |
| QF-096 Log Loss | `LOCKED` | Negative binary log likelihood with probability clipping. | Probability metric. | Verified; dependency recovered. |
| QF-099 Fill Calibration Error | `LOCKED` | Observed fill rate minus mean predicted fill per bucket. | Maker validation. | Verified; dependency recovered. |
| QF-100 EconomicLift | `LOCKED` | `NetPnL_model-NetPnL_baseline` on comparable inputs/budgets. | Promotion gate. | Verified; dependency recovered. |
| QF-101 ModelValue | `LOCKED` definition | PnL gain minus PnL lost to added latency and operational cost. | Complexity gate. | Verified; dependency recovered. |
| QF-102 Model Disagreement | `LOCKED` feature | Standard deviation-like dispersion of model probabilities. | Uncertainty input. | Verified; penalty calibrated. |
| QF-103 OOD Distance | `MODEL DEPENDENT` method; locked contract | `OODScore>=0`; larger is farther outside support. | Safe extrapolation boundary. | Verified. |

## Inconsistency result

No source-level mathematical inconsistency was found. PASS 00's Formula Index has truncated/mis-selected “expression locator” text for several vertically rendered formulas (notably QF-028, QF-044, QF-054/055, QF-082/083, QF-095 and QF-103). PASS 02 corrected presentation from original SRC-004 without changing formulas. PASS 11 should repair Formula Index extraction metadata globally.
