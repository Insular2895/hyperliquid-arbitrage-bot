# 04 — Formula Book

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## 1. Purpose

This is the canonical V2 mathematical contract for `QF-001` through `QF-110`. The same identified formula, parameter snapshot and numerical boundary applies to production Rust, research Python, Replay, Shadow and Live. An implementation must not infer a missing unit, sign, rounding rule or failure value.

## 2. Authority

SRC-004, Dossier 2/6 Formula Book, is the closure source. Domain masters remain authoritative for state ownership and consumption, not for changing an equation. Current exchange rules are external dependencies and require revalidation. The [audit ledger](./_analysis/pass11_formula_book/FORMULA_AUDIT_LEDGER.md), [symbol table](./_analysis/pass11_formula_book/GLOBAL_SYMBOL_TABLE.md) and [failure matrix](./_analysis/pass11_formula_book/FORMULA_PRECONDITION_AND_FAILURE_MATRIX.md) complete the implementable contract.

## 3. Governance

Every result records `FormulaVersion`; stochastic results additionally record model/artifact and feature versions, while dynamic exchange inputs record metadata and fee versions. A semantic change requires a new FormulaVersion, updated golden vectors, consumer/model/Risk impact analysis and revalidation. A calibrated value is configuration evidence, not part of a locked equation. A learned quantity is an artifact output, not a hard-coded formula.

## 4. Global notation

`A,B,X` are assets; `B→Q` means sell base into bids and `Q→B` means buy base from asks. `q` is base quantity unless asset-qualified; `p` is quote/base price; `t` is event time; `W` is a declared window; `S` is the immutable state/snapshot bundle. Subscripts must identify asset, market, side, horizon or scenario whenever ambiguity is possible. See the global symbol table for the complete registry.

## 5. Units

Prices are quote/base, sizes are base, notionals are quote, latency is one declared time unit, probabilities and ratios are dimensionless, and PnL/costs carry an explicit asset or numeraire. `1 bp = 10^-4`; bps outputs equal `10^4` times their fractional ratio. Sums and differences require equal units; ratios require compatible numerator and denominator.

## 6. Sign conventions

Positive `PnL`/gain is favorable; `Loss=-PnL`, so upper positive Loss is the risk tail. BUY/SELL mechanical slippage and impact are positive when execution costs us. Positive adverse selection is unfavorable on both sides. Positive prediction error means realized PnL exceeded prediction; positive slippage error means cost was underestimated. Inventory deltas are positive inflows.

## 7. Numerical precision

Exchange-boundary price/size and reservation arithmetic use exact ticks/lots or an equivalent fixed-point representation. Size that must not exceed a limit floors to the valid quantum. Price legality is delegated to the versioned `PriceQuantizer`. Intermediate stochastic/model math may use floating point; NaN and unrequested infinity never cross a decision boundary. Undefined or invalid results are typed failures, never zero. Overflow is checked. Exact discrete outputs use equality; floating analytics use formula-specific absolute/relative tolerances recorded with their golden vector.

## 8. Formula statuses

The `Source status` column preserves the exact SRC-004 label. `LOCKED ...` fixes the mathematical structure; `CALIBRATED ...` requires evidence/versioned parameters; `LEARNED ...` requires an identified model; `MODEL DEPENDENT` fixes only the output contract. For QF-099 and QF-106–110 the section has no formal status line: their equations are retained as `SOURCE_DERIVED_FROM_CONTEXT`, not falsely presented as source-explicit. QF-104 is a source-explicit prohibition plus gated categorical contract, not a scalar weighted formula.

## 9. External exchange rules

QF-007, QF-008, QF-014–016 and every minimum/fee/debit-asset/precision assumption consume point-in-time exchange evidence. Before implementation or Live use, validate current size/price rules, minimums, fee rates/tier/rebate semantics and fee debit assets against official exchange material; record effective time and evidence. No external lookup was performed in PASS11.

## 10. Pricing / spread / depth — QF-001–006

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-001 | Mid Price | LOCKED | `Mid_t=(Bid_t+Ask_t)/2` | Price; valid positive coherent BBO required; not executable price. |
| QF-002 | Absolute Spread | LOCKED | `Spread_t=Ask_t-Bid_t` | Price; crossed/non-positive BBO is invalid input state. |
| QF-003 | Relative Spread | LOCKED | `SpreadRel_t=(Ask_t-Bid_t)/Mid_t`; `SpreadBps_t=10^4 SpreadRel_t` | Dimensionless/bps; `Mid_t>0`. |
| QF-004 | Cumulative Base Depth | LOCKED | `DepthBase_s(K)=Σ_{i=1}^K q_i` | Base units; declared side/order, `K≥1`, valid nonnegative levels. |
| QF-005 | Cumulative Quote Depth | LOCKED | `DepthQuote_s(K)=Σ_{i=1}^K p_iq_i` | Quote units; same conditions as QF-004, positive prices. |
| QF-006 | Depth Within Price Band | LOCKED | `D_ask(δ)=Σ_{p_i≤Ask_1(1+δ)}p_iq_i`; `D_bid(δ)=Σ_{p_i≥Bid_1(1-δ)}p_iq_i` | Quote; side-specific, `δ≥0` configured/calibrated, coherent BBO. |

## 11. Precision / book walking — QF-007–013

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-007 | Hyperliquid Size Quantization | LOCKED | `Δq=10^{-d}`; `q_valid=floor(q10^d)10^{-d}` | Base; nonnegative finite `q`, valid `d`; floor prevents excess exposure. |
| QF-008 | Hyperliquid Price Validity | LOCKED EXCHANGE RULE | spot: `max_significant_figures=5`; `max_decimal_places=8-szDecimals`; integer prices permitted | Boolean/legal price via `PriceQuantizer`, never generic `round(price,5)`; external revalidation mandatory. |
| QF-009 | Book Walk Base→Quote | LOCKED | `x_i=min(q_remaining,q_i)`; `GrossQuote=Σ_ix_ip_i`; `Σ_ix_i=q_B^filled` | Sell base into bids. Return filled and residual explicitly; a full-fill consumer rejects insufficient depth. |
| QF-010 | Book Walk Quote→Base | LOCKED | `x_i=min(q_i,Q_remaining/p_i)`; `Q_i=x_ip_i`; `GrossBase=Σ_ix_i` | Spend quote into asks. Return spent/residual and fill explicitly; positive price required. |
| QF-011 | VWAP | LOCKED | `VWAP=Σ_ip_ix_i/Σ_ix_i` | Quote/base; undefined typed result when total base fill is zero. |
| QF-012 | Mechanical Slippage BUY | LOCKED | `Slippage_buy=(VWAP-Ask_1)/Ask_1`; `SlippageBps=10^4 Slippage_buy` | Positive is cost; `Ask_1>0`, valid BUY walk/VWAP. |
| QF-013 | Mechanical Slippage SELL | LOCKED | `Slippage_sell=(Bid_1-VWAP)/Bid_1`; `SlippageBps=10^4 Slippage_sell` | Positive is cost; `Bid_1>0`, valid SELL walk/VWAP. |

## 12. Fees / NetConvert — QF-014–016

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-014 | Fee Rate | LOCKED SOURCE, DYNAMIC VALUE | `f_{market,mode}=FeeEngine(account,market,mode,t)` | Dimensionless; point-in-time `userFees`; rebates may make `f<0`; stale/missing tier invalid. |
| QF-015 | Fee Amount | LOCKED | `FeeValue=Notional×f` | Explicit asset/numeraire; economic value and actual `FeeAssetDelta` are distinct. |
| QF-016 | NetConvert | LOCKED ARCHITECTURE | `NetConvert(A,B,q_A,S)=q_B^net`; if fee debited in B: `q_B^net=Quantize_B(GrossConvert(A,B,q_A)-FeeDebit_B)` | One directed book walk plus fee/debit-asset/minimum/precision state. Other debit asset returns actual asset deltas and converted economic value. Never assume universal `output×(1-fee)`. Invalid leg/minimum/depth/precision fails. |

## 13. Routes / OWA / Triangle — QF-017–023

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-017 | Direct Route Output | LOCKED | `D(q_A)=NetConvert(A,B,q_A)` | B units; exact same input/state conventions as comparator. |
| QF-018 | Two-Leg Indirect Output | LOCKED | `q_X=NetConvert(A,X,q_A)`; `I(q_A)=NetConvert(X,B,q_X)` | B units; valid net/quantized leg-1 output is leg-2 input. |
| QF-019 | OWA Relative Edge | LOCKED | `Edge_OWA(q_A)=I(q_A)/D(q_A)-1`; bps `=10^4Edge_OWA` | Dimensionless; `D(q_A)>0`; same q, terminal B, books, fees, precision and time policy. |
| QF-020 | OWA Absolute Gain | LOCKED | `Gain_B(q_A)=I(q_A)-D(q_A)` | B units; positive favors indirect route. |
| QF-021 | Triangular Output | LOCKED | `q_X=NC(A,X,q_A)`; `q_B=NC(X,B,q_X)`; `q'_A=NC(B,A,q_B)` | Returns A; every net valid output feeds the next leg. |
| QF-022 | Triangle Return | LOCKED | `R_triangle(q_A)=q'_A/q_A-1` | Dimensionless; `q_A>0`, closed A→X→B→A path. |
| QF-023 | Triangle PnL | LOCKED | `PnL_A(q_A)=q'_A-q_A` | A units; positive is gain. |

## 14. ConversionAlpha / ExecutionAlpha / Edge — QF-024–027

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-024 | Conversion Alpha | LOCKED | `ConversionAlpha=Output_Indirect,TT/Output_Direct,T-1` | Same input/terminal asset; isolates route conversion under immediate execution; denominator >0. |
| QF-025 | Execution Alpha MT | LOCKED | `ExecutionAlpha_MT=Output_Indirect,MT/Output_Indirect,TT-1` | Same route/input/terminal asset; isolates execution-mode effect; denominator >0. |
| QF-026 | Edge Curve | LOCKED OBJECT | `E:q↦E(q)` by exact repeated simulation at valid sizes | Piecewise/discontinuous after depth/minimum/rounding; no imposed interpolation or monotonicity. |
| QF-027 | Maximum Profitable Size | LOCKED DEFINITION | `Q_profitable=sup{q:E(q)≥E_min}` | Valid discrete sizes only; calibrated `E_min`; empty feasible set returns no profitable size, not zero by invention. |

## 15. Microstructure / OFI / Microprice — QF-028–035

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-028 | Queue Imbalance | LOCKED | `QI=(Q_bid-Q_ask)/(Q_bid+Q_ask)` | Dimensionless `[-1,1]`; denominator >0. |
| QF-029 | Multi-Level Imbalance | LOCKED | `QI_K=(Σ_kw_kQ^b_k-Σ_kw_kQ^a_k)/(Σ_kw_kQ^b_k+Σ_kw_kQ^a_k)` | Dimensionless; common levels/nonnegative weights, positive denominator; weights calibrated although source headline says LOCKED. |
| QF-030 | Event-Level Bid OFI Contribution | LOCKED DEFINITION | `e^b_n=1[P^b_n≥P^b_{n-1}]Q^b_n-1[P^b_n≤P^b_{n-1}]Q^b_{n-1}` | Base units; both terms apply when prices equal. Ordered events required. |
| QF-031 | Event-Level Ask OFI Contribution | LOCKED | `e^a_n=1[P^a_n≤P^a_{n-1}]Q^a_n-1[P^a_n≥P^a_{n-1}]Q^a_{n-1}` | Base units; both terms apply when prices equal. Ordered events required. |
| QF-032 | OFI | LOCKED | `OFI_n=e^b_n-e^a_n`; `OFI_W=Σ_{n∈W}OFI_n` | Base units; positive is bid-side pressure under this definition. Snapshot-only value must be labelled proxy. |
| QF-033 | Multi-Level OFI | LOCKED STRUCTURE / CALIBRATED WEIGHTS | `MLOFI=Σ_{k=1}^K w_kOFI^{(k)}` | Weighted base/proxy unit; weights/window versioned. |
| QF-034 | Microprice | LOCKED | `MicroPrice=(Ask·Q_bid+Bid·Q_ask)/(Q_bid+Q_ask)` | Price; positive denominator/coherent BBO. |
| QF-035 | Microprice Dislocation | LOCKED | `MicroDislocation=(MicroPrice-Mid)/Mid`; bps `=10^4MicroDislocation` | Dimensionless/bps; `Mid>0`; positive is above mid. |

## 16. Volatility / jumps — QF-036–039

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-036 | Log Return | LOCKED | `r_t=ln(P_t/P_{t-1})` | Dimensionless; explicit price series/reference, ordered positive prices. |
| QF-037 | Realized Variance | LOCKED | `RV_W=Σ_{t∈W}r_t^2` | Dimensionless squared; declared nonempty sampling window. |
| QF-038 | Realized Volatility | LOCKED | `σ_W=sqrt(RV_W)` | Dimensionless; nonnegative; not annualized in the hot path unless explicitly transformed elsewhere. |
| QF-039 | Robust Jump Score | LOCKED STRUCTURE / CALIBRATED THRESHOLD | `JumpScore_t=abs(r_t)/(σ_fast,t+ε)` | Dimensionless nonnegative; `ε>0` numerical safeguard and threshold/horizon versioned. |

## 17. Liquidity / participation / resilience — QF-040–043

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-040 | Depth Participation | LOCKED | `DP(q,δ)=Notional(q)/DepthQuote(δ)` | Dimensionless; matching side/band/book; zero depth is conceptual `+∞` and a reject, never emitted as non-finite number. |
| QF-041 | Volume Participation | LOCKED | `VP(q,W)=Notional(q)/ExecutedVolume_W` | Dimensionless; declared window/source; zero-volume behavior is source-unspecified and remains an invalid typed result/open convention. |
| QF-042 | Mechanical Impact | LOCKED | BUY: `(VWAP-Mid_0)/Mid_0`; SELL: `(Mid_0-VWAP)/Mid_0` | Dimensionless; positive is cost; valid `Mid_0>0` and walk. |
| QF-043 | Liquidity Resilience | LOCKED | `Resilience(t)=(D_t-D_s)/(D_0-D_s)` | Dimensionless; raw may exceed 1; reporting may clamp `[0,1]`; `D_0=D_s` is source-unspecified and invalid/open. |

## 18. Survival / capture — QF-044–050

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-044 | Survival Function | LOCKED OBJECT | `S(t∣X)=P(T>t∣X)` | Probability `[0,1]`; T is remaining time until edge death; defined horizon/features. |
| QF-045 | Discrete Hazard | LEARNED | `h_k(X)=P(T∈[t_k,t_{k+1})∣T≥t_k,X)`; baseline `h_k=σ(β_k^TX)` | Probability `[0,1]`; learned coefficients/artifact and at-risk set. |
| QF-046 | Survival from Discrete Hazard | LOCKED | `S_k=Π_{j=1}^k(1-h_j)` | Probability; exact source indexing is `1..k`; all hazards valid. |
| QF-047 | Edge Half-Life | LOCKED | `t_50=inf{t:S(t)≤0.5}` | Time; if never crossed within horizon, return censored `t50>model_horizon`, not invented value. |
| QF-048 | Capture Probability | LOCKED | `P_capture=E_L[S(L)]`; discrete `=Σ_mP(L∈B_m)S(ℓ_m)` | Probability; same units/time origin for latency and survival; distributions valid/normalized. |
| QF-049 | Expected Edge at Arrival | LEARNED DISTRIBUTION | `E_arrival=E[Edge_{t+L}∣X_t]` | Edge unit; learned conditional distribution. No exponential decay assumption. |
| QF-050 | Probability Above Execution Threshold | LEARNED | `P_exec=P(Edge_{t+L}>E_minimum∣X_t)` | Probability; calibrated/canonical economic threshold with same edge units. |

## 19. Maker fill / adverse selection — QF-051–055

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-051 | Maker Fill Survival | LEARNED | `S_f(t∣X)=P(T_f>t∣X)` | Probability; learned conditional time-to-fill artifact. |
| QF-052 | Maker Fill CDF | LOCKED FROM SURVIVAL | `F_f(t∣X)=1-S_f(t∣X)=P(T_f≤t∣X)` | Probability; same event/horizon/model as QF-051. |
| QF-053 | Expected Fill Time | LOCKED DEFINITION | `E[T_f]=∫_0^∞S_f(t)dt`; discrete approximation by survival bins | Time; conditional/truncated variant must be labelled; finite support/censoring explicit. |
| QF-054 | Adverse Selection BUY | LOCKED | `AS_buy(h)=(P_f-Mid_{t_f+h})/P_f` | Dimensionless; positive is adverse; filled BUY, positive fill price, explicit horizon/reference. |
| QF-055 | Adverse Selection SELL | LOCKED | `AS_sell(h)=(Mid_{t_f+h}-P_f)/P_f` | Dimensionless; positive is adverse; filled SELL, positive fill price, explicit horizon/reference. |

## 20. EV / PnL distributions — QF-056–060

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-056 | Expected Value | LOCKED | `EV=Σ_ip_iPnL_i`, `Σ_ip_i=1` | Explicit PnL asset/numeraire; mutually exclusive/exhaustive scenarios and valid probabilities. |
| QF-057 | Execution EV | LOCKED STRUCTURE | `EV_execution=P_FE[PnL∣F]+P_PE[PnL∣P]+P_RE[PnL∣R]+P_XE[PnL∣X]` | Fill, partial, recovery and failure/other terminal scenarios are exclusive/exhaustive; common numeraire. |
| QF-058 | MT EV | LOCKED STRUCTURE / LEARNED COMPONENTS | `EV_MT=∫f_fill(t∣X)EV_leg2(t)dt-C_adverse-C_recovery`; discrete `Σ_kP(T_f∈B_k)EV_leg2(t_k)-C_adverse-C_recovery` | Common numeraire; learned fill distribution; costs included once. |
| QF-059 | Probability of Positive PnL | LOCKED | `P_+=P(PnL>0)`; `P̂_+=N^{-1}Σ_i1[PnL_i>0]` | Probability; strict `>0`; `N>0`, same PnL definition. |
| QF-060 | Loss Variable | LOCKED | `Loss=-PnL` | Same currency/numeraire; profitable outcomes yield negative Loss. |

## 21. VaR / ES / RAEV — QF-061–063

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-061 | VaR | LOCKED | `VaR_α=F_Loss^{-1}(α)` | Loss units; `0<α<1`; source does not fix finite-sample quantile interpolation. |
| QF-062 | Expected Shortfall | LOCKED | continuous: `CVaR_α=E[Loss∣Loss≥VaR_α]`; robust: `ES_α=(1-α)^{-1}∫_α^1VaR_u du` | Loss units; internal name ExpectedShortfall. Finite-sample tie/interpolation estimator is open. |
| QF-063 | Risk-Adjusted EV | CALIBRATED | `RAEV=EV_execution-InventoryPenalty-StrandedPenalty-ModelUncertaintyPenalty` | Common numeraire. Do not re-subtract fees, slippage, partial or recovery outcomes already inside execution EV. |

## 22. Inventory — QF-064–069

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-064 | Normalized Inventory Deviation | LOCKED | `z_a=(I_a-I_a*)/B_a` | Dimensionless; asset-aligned quantities; `B_a>0`, otherwise invalid/open normalization policy. |
| QF-065 | Soft Inventory Penalty | CALIBRATED | `Penalty_a=κ_az_a^2` | Numeraire; `κ_a≥0` calibrated; only soft-band objective, not hard gate. |
| QF-066 | Hard Inventory Gate | LOCKED | reject if `I_a^future<HardMin_a` or `I_a^future>HardMax_a` | Boolean reject; exact future inventory/reservations; no soft-penalty bypass. |
| QF-067 | Inventory Net Flow | LOCKED | `NetFlow_a(W)=Σ_{trades∈W}ΔI_a` | Asset units; signed deltas, declared window and ordered actual events. |
| QF-068 | Exit Cost | LOCKED STRUCTURE | `ExitCost(X)=CurrentValue(X)-BestExecutableExitValue(X)` | Numeraire; best executable QF-016 exit including depth/fees/slippage/rounding, same state. |
| QF-069 | Stranded Capital Penalty | CALIBRATED STRUCTURE | `StrandedPenalty=ExpectedExitCost+ExpectedIdleCost+ExpectedRiskCost` | Common numeraire; components separate and included once. |

## 23. Bridge / relocation — QF-070–072

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-070 | Bridge Cost | LOCKED STRUCTURE | `BridgeCost(P)=V_start-V_end^net+RiskCost(P)` | Common numeraire; end value uses sequential NetConvert; no repeated conversion costs. |
| QF-071 | Bridge Break-Even Cycles | LOCKED | `N_BE=(BridgeCost+ExpectedExitCost)/E[PnL_cycle]` | Cycles; denominator must be positive, otherwise conceptual `+∞`/never break even. |
| QF-072 | Capital Relocation Value | LOCKED STRUCTURE | `Value(move)=EV_destination-EV_stay-BridgeCost-ExpectedExitCost-RelocationRiskCost` | Numeraire; move only above calibrated threshold with hysteresis/cooldown; like-for-like horizon. |

## 24. Balance / book capacity — QF-073–074

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-073 | Available Balance | LOCKED | `AvailableBalance_a=ActualBalance_a-ReservedBalance_a≥0` | Asset units; negative is invariant violation/UNKNOWN lock, never spendable. |
| QF-074 | Available Book Capacity | LOCKED | `AvailableCapacity_j=ObservedCapacity_j-ReservedCapacity_j` | Leg input units; negative is reservation/state inconsistency and rejects new allocation. |

## 25. Sizing / Q_validated — QF-075–077

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-075 | Optimal Sizing Objective | LOCKED OPTIMIZATION PROBLEM | `q*=argmax_q RAEV(q)` subject to balance, book, impact, `ES_α`, `P_+`, confidence and hard-inventory gates | Valid discrete quantities only; infeasible yields no action. |
| QF-076 | Validated Capacity | LOCKED DEFINITION | `Q_validated=sup{q:Gates(q)=TRUE}` | Valid size unit; exact gated scope/evidence tuple; empty set is no validated capacity. |
| QF-077 | Sizing Search | LOCKED ALGORITHM | valid-size grid → best region → local refinement | Deterministic tie-break/order; no gradient/monotonicity assumption; returns only a feasible audited point. |

## 26. Multi-op allocation — QF-078

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-078 | Portfolio Allocation | LOCKED OPTIMIZATION PROBLEM | `max_q Σ_iRAEV_i(q_i)` subject to `Aq≤b` | Common numeraire and shared balance/depth/inventory/risk constraints; deterministic feasible solution. |

## 27. Recovery — QF-079–080

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-079 | Recovery Objective | LOCKED | `argmax_aE[PortfolioValue_after(a)∣CurrentState]`, equivalently `argmin_aExpectedRecoveryLoss(a)` | Starts from actual current exposure; risk-reducing legal actions; sunk losses excluded. |
| QF-080 | Recovery Loss | LOCKED | `RecoveryLoss=PortfolioValue_beforeRecovery-PortfolioValue_afterRecovery` | Common numeraire; measures incremental recovery degradation, excludes pre-recovery sunk loss. |

## 28. Cross-market / competition — QF-081–083

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-081 | Cross-Market Response | LEARNED | `R_{i→j}(h)=P(ΔMarket_j(h)∣Shock_i,X)` | Learned distribution; ordered markets, horizon and shock definition. |
| QF-082 | Correction Velocity | LOCKED | `Correction(h)=(E_0-E_h)/E_0` | Dimensionless; `E_0>0`; 0 none, 1 disappeared, >1 crossed zero. |
| QF-083 | Competition Hazard | LEARNED | `λ_c(t∣X)` | Nonnegative rate per time; learned artifact. Use global edge-death hazard before unidentifiable cause claims. |

## 29. Infrastructure economics — QF-084–094

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-084 | Infrastructure Latency | LOCKED DECOMPOSITION | `L_total=L_feed+L_compute+L_sign+L_send+L_exchange`; `L_compute=L_decode+L_book+L_route+L_simulation+L_risk+L_decision` | Same time unit, nonnegative, mutually exclusive instrumentation boundaries. |
| QF-085 | Opportunity Capture vs Infrastructure | LOCKED | `P_capture,s=E_{L_s}[S(L_s)]` | Probability; server-specific latency distribution and same survival contract. |
| QF-086 | Infrastructure Gross PnL Difference | LOCKED | `ΔGrossPnL=GrossPnL_candidate-GrossPnL_current` | Numeraire; same opportunity universe, strategy, capital and horizon. |
| QF-087 | Incremental Infrastructure Cost | LOCKED | `ΔCost=Cost_candidate-Cost_current` | Same numeraire/horizon/accounting scope; may be ≤0. |
| QF-088 | Net Upgrade Value | LOCKED | `NetUpgradeValue=ΔGrossPnL-ΔCost` | Numeraire; positive favors candidate before uncertainty gate. |
| QF-089 | Infrastructure ROI | LOCKED | `InfraROI=ΔGrossPnL/ΔCost` | Dimensionless only for `ΔCost>0`; otherwise compare NetPnL/NetUpgradeValue. |
| QF-090 | Infrastructure Net PnL | LOCKED | `NetPnL_s=GrossTradingPnL_s-TradingCosts_s-InfrastructureCost_s` | Numeraire; trading costs included exactly once. |
| QF-091 | Infrastructure Upgrade Gate | CALIBRATED SAFETY FACTOR | `LCB_α(ΔGrossPnL)>SF·ΔCost` | Numeraire inequality; calibrated `α`, `SF`; like-for-like evidence. |
| QF-092 | Infrastructure Efficiency | LOCKED | `InfraEfficiency=NetPnL/InfraCost` | Dimensionless diagnostic; positive denominator required; zero/negative is invalid for ratio. |
| QF-093 | Capture Ratio | LOCKED | `CaptureRatio=Σ_iRealizedPnL_i/Σ_iExpectedExecutablePnL_i` | Dimensionless ratio of sums; aligned eligible set; denominator must be positive. |
| QF-094 | Empirical Opportunity Survival | LOCKED | `ObservedSurvival(h)=N_alive(h)/N_eligible` | Probability; censoring handled appropriately; `N_eligible>0`. |

## 30. Calibration / prediction errors — QF-095–100

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-095 | Brier Score | LOCKED | `Brier=N^{-1}Σ_i(p_i-y_i)^2` | Dimensionless `[0,1]`; aligned binary event/label, `p∈[0,1]`, `N>0`; lower better. |
| QF-096 | Log Loss | LOCKED | `LL=-N^{-1}Σ_i[y_i ln p_i+(1-y_i)ln(1-p_i)]` | Dimensionless nonnegative; aligned binary labels; clip `p` to `[ε,1-ε]`; `0<ε<0.5` numerical parameter, `N>0`. |
| QF-097 | PnL Prediction Error | LOCKED | `PnLError=RealizedPnL-PredictedPnL`; `PnLBias=E[PnLError]` | PnL units; positive means underestimated PnL. |
| QF-098 | Slippage Prediction Error | LOCKED | `SlippageError=ActualSlippage-PredictedSlippage` | Same fraction/bps unit; positive means execution cost underestimated. |
| QF-099 | Fill Calibration Error | SOURCE_DERIVED_FROM_CONTEXT | `CalibrationError_B=ObservedFillRate_B-MeanPredictedFill_B` | Probability-point difference by nonempty aligned bucket; positive means more fills than predicted. Section has no formal status label; fixed calibration definition is context-derived LOCKED. |
| QF-100 | Model Economic Lift | LOCKED | `EconomicLift=NetPnL_model-NetPnL_baseline` | Common numeraire; same dataset, opportunity set, capital, fees and risk budget. |

## 31. Model value / OOD / confidence — QF-101–104

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-101 | Quant Model Value after Latency Cost | LOCKED DEFINITION | `ModelValue=PnL_with-PnL_without-PnLLostDueToAddedLatency-OperationalCost` | Common numeraire/horizon; robust OOS value must be positive for promotion. |
| QF-102 | Model Disagreement | LOCKED FEATURE | `p̄=M^{-1}Σ_mp_m`; `Disagreement=sqrt(M^{-1}Σ_m(p_m-p̄)^2)` | Probability spread; `M>0`, aligned probabilistic outputs; penalty coefficient calibrated. |
| QF-103 | OOD Distance | MODEL DEPENDENT | `OODScore≥0`; larger means farther outside validated support | Score unit/model method versioned. NaN/missing support rejects; no universal estimator is invented. |
| QF-104 | Simulation Confidence | PAS DE FAUX SCORE PONDÉRÉ FIGÉ | `DataFidelityGate ∧ FreshnessGate ∧ OODGate ∧ SampleSupportGate ∧ ModelAgreementGate ∧ LatencyUncertaintyGate → {HIGH,MEDIUM,LOW,REJECT}` | Categorical gated contract; no arbitrary fixed weighted scalar. Missing/invalid gate cannot produce HIGH. |

## 32. Idle capital / accounting — QF-105–108

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-105 | Expected Idle Capital Cost | CALIBRATED | `IdleCost=C×OpportunityRate×T` | Numeraire; nonnegative capital/time; empirically calibrated foregone-opportunity rate, not arbitrary interest. |
| QF-106 | Global Economic PnL | SOURCE_DERIVED_FROM_CONTEXT | `EconomicPnL=ExecutionPnL+InventoryMTM+RebalancePnL+BridgePnL-InfrastructureCost` | Common numeraire/period; components disjoint and reconciled. Formal status line absent; fixed accounting identity is context-derived LOCKED. |
| QF-107 | Inventory Mark-to-Market | SOURCE_DERIVED_FROM_CONTEXT | `MTM_a=I_aP_a^numeraire`; `ΔMTM_a=MTM_{a,t}-MTM_{a,t-1}-ExternalFlow_a` | Numeraire; point-in-time price policy and external flows explicit. Formal status line absent; identity context-derived LOCKED. |
| QF-108 | Total Strategy PnL | SOURCE_DERIVED_FROM_CONTEXT | `StrategyPnL=ΣRoutePnL+ΣRecoveryPnL+ΣRebalancePnL+InventoryPnL`; `EconomicPnL=StrategyPnL-InfraCost` | Common numeraire/period; disjoint ownership. Formal status line absent; identity context-derived LOCKED. |

## 33. Drawdown / MDD — QF-109–110

| ID | Canonical name | Source status | Exact canonical equation | Essential semantics / invalid case |
|---|---|---|---|---|
| QF-109 | Drawdown | SOURCE_DERIVED_FROM_CONTEXT | `Peak_t=max_{u≤t}E_u`; `DD_t=Peak_t-E_t`; `DD_t^rel=(Peak_t-E_t)/Peak_t` | Absolute equity units, relative dimensionless; ordered nonempty equity series; relative requires `Peak_t>0`. Formal status line absent. |
| QF-110 | Maximum Drawdown | SOURCE_DERIVED_FROM_CONTEXT | `MDD=max_tDD_t` | Absolute equity units; nonempty audited interval. Formal status line absent; fixed definition context-derived LOCKED. |

## 34. Dependency graph

The critical composition spine is `QF-007/008/009/010/014/015 → QF-016 → QF-017/018/021 → QF-019/020/022/023/024/025/026/027`, `QF-045 → QF-046 → QF-044/047/048/049/050`, `QF-051 → QF-052/053 → QF-058`, `QF-056/057/058/060/061/062 → QF-063 → QF-075/078`, and `QF-086/087 → QF-088/089/091`, with accounting closing through QF-090 and QF-106–110. The full edge list is in [Formula Dependency Graph](./_analysis/pass11_formula_book/FORMULA_DEPENDENCY_GRAPH.md).

## 35. Consumer map

Feature Engine owns deterministic market measures; Fee/Precision and Conversion engines own exchange arithmetic; Graph/Route owns route composition; Participant/Model owns learned distributions; Simulator owns counterfactual outcome distributions; Risk/Sizing consumes, gates and optimizes; Inventory/Bridge/Recovery owns actual exposure decisions; Accounting owns disjoint PnL; Infrastructure and Validation consume metrics/evidence. The per-QF mapping is in [Formula Consumer Matrix](./_analysis/pass11_formula_book/FORMULA_CONSUMER_MATRIX.md).

## 36. Golden tests / parity

Every locked or locked-structure formula has deterministic normal, boundary and invalid vectors. Mandatory families cover BBO/spread, both book walks, zero fill, fee asset/rebate, NetConvert composition, OWA/Triangle, OFI equality branches, survival indexing/censoring, EV scenario partition, Loss/VaR/ES, inventory/hard gates, sizing discreteness, recovery sunk-cost exclusion, infrastructure denominators, calibration errors, PnL accounting and drawdown. QF-001–003 source vector: Bid 99, Ask 101 → Mid 100, Spread 2, Spread 200 bps. QF-010–012 source vector: asks 100×2 and 101×3, buy 4 base → cost 402 quote, VWAP 100.5, BUY slippage 50 bps. See [golden catalog](./_analysis/pass11_formula_book/GOLDEN_VECTOR_REQUIREMENT_CATALOG.md).

## 37. Formula change control

A change proposal states affected QFs/symbols/units/statuses, before/after vectors, consumers, model/Risk/Replay/evidence impact and migration. Semantic changes increment FormulaVersion and invalidate dependent golden/parity and capability evidence until rerun. Parameter-only changes retain the formula identity but change the parameter/config/artifact version and rerun the declared dependent scope. No silent edit is permitted.

## 38. External revalidation

Exchange price validity, size quantum, market minimums, fee schedules/tiers/rebates and debit-asset behavior remain `EXTERNAL_RULE_REQUIRES_REVALIDATION`. The [external formula register](./_analysis/pass11_formula_book/EXTERNAL_FORMULA_RULE_REGISTER.md) and global external register hold the evidence requirements; PASS11 deliberately performs no Internet lookup.

## 39. Deep-spec links

- [Formula deep-spec index](./deep-specs/formulas/README.md)
- [Global notation, units, signs and numerical policy](./deep-specs/formulas/01_GLOBAL_NOTATION_UNITS_SIGNS_AND_NUMERICAL_POLICY.md)
- [QF-001–016](./deep-specs/formulas/02_QF001_QF016_PRICING_DEPTH_PRECISION_FEES_NETCONVERT.md)
- [QF-017–027](./deep-specs/formulas/03_QF017_QF027_ROUTES_OWA_TRIANGLE_AND_ALPHA.md)
- [QF-028–043](./deep-specs/formulas/04_QF028_QF043_MICROSTRUCTURE_VOLATILITY_AND_LIQUIDITY.md)
- [QF-044–055](./deep-specs/formulas/05_QF044_QF055_SURVIVAL_CAPTURE_MAKER_AND_ADVERSE_SELECTION.md)
- [QF-056–063](./deep-specs/formulas/06_QF056_QF063_EV_VAR_ES_AND_RISK_ADJUSTED_VALUE.md)
- [QF-064–080](./deep-specs/formulas/07_QF064_QF080_INVENTORY_BRIDGE_SIZING_ALLOCATION_AND_RECOVERY.md)
- [QF-081–094](./deep-specs/formulas/08_QF081_QF094_CROSS_MARKET_COMPETITION_AND_INFRASTRUCTURE.md)
- [QF-095–104](./deep-specs/formulas/09_QF095_QF104_CALIBRATION_MODEL_VALUE_OOD_AND_CONFIDENCE.md)
- [QF-105–110](./deep-specs/formulas/10_QF105_QF110_CAPITAL_ACCOUNTING_AND_DRAWDOWN.md)
- [Dependencies and double counting](./deep-specs/formulas/11_FORMULA_DEPENDENCIES_AND_DOUBLE_COUNTING.md)
- [Golden vectors, parity and change control](./deep-specs/formulas/12_GOLDEN_VECTORS_PARITY_AND_CHANGE_CONTROL.md)

## Source

SRC-004 lines 3350–9520, with QF-001–QF-110 at lines 3519–9224 and post-formula governance/golden requirements thereafter. Source statuses and exceptional omissions are recorded without invention.

## 40. CORR-05 — Composition audit

All QF-001–QF-110 were reviewed as one economic composition; equation and semantic changes are zero. QF-056/QF-057 consume one F/P/R/X execution PnL distribution. QF-063 subtracts InventoryPenalty, StrandedPenalty and ModelUncertaintyPenalty only as external, non-overlapping terms; it never repeats scenario fees, slippage, partial-path or Recovery economics.

QF-048/QF-085 arrival survival is not `p_full`; QF-059 positive-PnL probability is derived from the same distribution; QF-093 is a diagnostic/accounting ratio rather than an event probability. QF-027 profitable size and QF-076 validated capacity remain distinct. The QF namespace remains exactly QF-001–QF-110 and no human-derived formula is required. See [QF Composition Audit](_analysis/corr05_economic_integration/QF_COMPOSITION_AUDIT.md) and [Term Owner Registry](_analysis/corr05_economic_integration/ECONOMIC_TERM_OWNER_REGISTRY.md).
