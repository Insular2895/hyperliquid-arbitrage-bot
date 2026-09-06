# Global Symbol Table

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Indices: `t,u,n` time/event; `i,j,k,m` level/scenario/bin/model; `a,A,B,X` asset; `s` side/server; `W` window; `h` horizon. Optional values are never represented by a magic numeric sentinel.

| Symbol | Canonical meaning | Unit | Domain | First QF | Other QFs | Indexes | Sign / zero / negative | Optional | Source |
|---|---|---|---|---|---|---|---|---|---|
| `Bid_t`,`Ask_t` | best bid/ask | quote/base | book | 001 | 002,003,006,012,013,034 | time,market | >0; Bid≤Ask | no when evaluated | SRC-004 3519+ |
| `Mid_t` | BBO midpoint | quote/base | feature | 001 | 003,035,036,042,054,055 | time,market | >0 | no | SRC-004 |
| `Spread`,`SpreadRel`,`SpreadBps` | absolute/fraction/bps width | price/ratio/bps | feature | 002 | 003 | time,market | ≥0 valid | no | SRC-004 |
| `p_i`,`q_i` | level price/base size | quote/base; base | book | 004 | 005–013 | level,side,market | p>0,q≥0 | no | SRC-004 |
| `K`,`δ` | depth levels / relative band | count / ratio | feature | 004 | 006,029,033 | — | K≥1,δ≥0 | config | SRC-004 |
| `DepthBase_s`,`DepthQuote_s`,`D_ask`,`D_bid` | depth measures | base / quote | liquidity | 004 | 005,006,040,043 | side,market | ≥0 | no | SRC-004 |
| `d`,`Δq`,`q_valid` | size decimals, quantum, legal size | count;base;base | precision | 007 | 008,016 | asset/market | d≥0, values≥0 | no | SRC-004 |
| `szDecimals` | exchange size precision metadata | count | precision | 008 | — | asset | ≥0 | no | SRC-004 |
| `q_remaining`,`Q_remaining`,`x_i`,`Q_i` | walk residual/fill/spend | base or quote as named | conversion | 009 | 010,011 | leg,level | ≥0 | no | SRC-004 |
| `GrossQuote`,`GrossBase`,`GrossConvert` | pre-fee walk output | output asset | conversion | 009 | 010,016 | leg | ≥0 | no | SRC-004 |
| `VWAP` | fill-weighted price | quote/base | execution | 011 | 012,013,042 | side,book,q | >0 when defined | yes if zero fill | SRC-004 |
| `f_market,mode` | point-in-time fee rate | ratio | fee | 014 | 015,016 | account,market,mode,time | zero/negative rebate allowed | no with evidence | SRC-004 |
| `Notional`,`FeeValue`,`FeeDebit_B`,`FeeAssetDelta` | value and actual fee debit | explicit asset/numeraire | fee | 015 | 016,040 | leg,asset | fee may be negative rebate | debit policy-dependent | SRC-004 |
| `NC`,`S`,`q_A`,`q_B^net` | NetConvert, immutable state, input/output | A/B | conversion | 016 | 017–025,068,070 | assets,state | quantities≥0 | output invalid possible | SRC-004 |
| `D(q_A)`,`I(q_A)` | direct/indirect terminal B outputs | B | route | 017 | 018–020,024 | route,size | ≥0 if valid | yes invalid | SRC-004 |
| `q_X`,`q_B`,`q'_A` | sequential route amounts | named asset | route | 018 | 021–023 | leg | ≥0 | no valid route | SRC-004 |
| `Edge_OWA`,`Gain_B`,`R_triangle`,`PnL_A` | route edge/gain/return/PnL | ratio;B;ratio;A | route | 019 | 020–023 | route,size | signed; zero allowed | yes invalid | SRC-004 |
| `Output_Direct,T`,`Output_Indirect,TT`,`Output_Indirect,MT` | comparable mode outputs | same terminal asset | execution | 024 | 025 | route,mode | ≥0 | yes invalid | SRC-004 |
| `E(q)`,`E_min`,`Q_profitable` | size edge curve/threshold/max profitable size | edge;edge;input asset | sizing | 026 | 027 | route,size | edge signed; q≥0 | empty feasible optional | SRC-004 |
| `Q_bid`,`Q_ask`,`QI`,`QI_K`,`w_k` | BBO/level sizes, imbalance, weights | base;base;ratio;ratio;weight | microstructure | 028 | 029,034 | level/side | sizes/weights≥0; QI signed | no valid | SRC-004 |
| `P^b_n`,`P^a_n`,`Q^b_n`,`Q^a_n` | event BBO prices/sizes | price/base | OFI | 030 | 031–033 | event,side | price>0,size≥0 | no | SRC-004 |
| `e^b_n`,`e^a_n`,`OFI_n`,`OFI_W`,`MLOFI` | flow contributions/aggregates | base or weighted base | OFI | 030 | 031–033 | event,level,window | signed; zero allowed | no valid | SRC-004 |
| `MicroPrice`,`MicroDislocation` | microprice and relative displacement | price / ratio | microstructure | 034 | 035 | market,time | price>0; displacement signed | no valid | SRC-004 |
| `P_t`,`r_t`,`RV_W`,`σ_W`,`σ_fast`,`ε` | reference price, log return, variance, scales/safeguard | price;ratio;ratio²;ratio;ratio | volatility | 036 | 037–039 | time,window | P>0,RV/σ≥0,ε>0 | no valid | SRC-004 |
| `DP`,`VP`,`ExecutedVolume_W` | participation ratios and volume | ratio;ratio;quote | liquidity | 040 | 041 | market,window | ≥0; denominator positive | ratio invalid possible | SRC-004 |
| `D_0`,`D_s`,`D_t`,`Resilience` | before/post/current depth and recovery | same depth / ratio | liquidity | 043 | — | time | depth≥0; raw resilience signed/>1 | invalid if denom zero | SRC-004 |
| `T`,`S(t∣X)`,`X` | time to edge death, survival, feature state | time;probability;feature vector | survival | 044 | 045–050,083,085 | time/context | T≥0,S∈[0,1] | censored T | SRC-004 |
| `h_k`,`β_k`,`σ(z)`,`S_k` | hazard, coefficients, sigmoid, survival product | probability;model;probability;probability | survival | 045 | 046 | bin/model | probabilities [0,1] | no valid | SRC-004 |
| `t_50`,`model_horizon` | half-life/censor horizon | time | survival | 047 | — | model | ≥0 | censored not missing | SRC-004 |
| `L`,`B_m`,`ℓ_m`,`P_capture` | latency RV/bins/representative/capture probability | time;bin;time;probability | capture | 048 | 085 | server/bin | nonnegative/[0,1] | no valid | SRC-004 |
| `Edge_{t+L}`,`E_arrival`,`E_minimum`,`P_exec` | arrival edge expectation/threshold/probability | edge;edge;edge;probability | model | 049 | 050 | horizon | edges signed,P∈[0,1] | unavailable under OOD | SRC-004 |
| `T_f`,`S_f`,`F_f`,`f_fill` | fill time/survival/CDF/density | time;probability;probability;1/time | maker | 051 | 052,053,058 | time/order | valid ranges | censored possible | SRC-004 |
| `P_f`,`t_f`,`AS_buy`,`AS_sell` | fill price/time/adverse-selection ratios | price;time;ratio;ratio | maker | 054 | 055 | side,horizon | AS positive adverse | no valid | SRC-004 |
| `p_i`,`PnL_i`,`EV` | scenario probability/outcome/expected value | probability;numeraire;numeraire | simulator | 056 | 057–063 | scenario | p≥0,PnL/EV signed | no valid | SRC-004 |
| `F,P,R,X`,`P_F...P_X` | full/partial/recovery/failure scenarios/probabilities | category/probability | execution EV | 057 | — | scenario | p∈[0,1] | no | SRC-004 |
| `EV_leg2(t)`,`C_adverse`,`C_recovery`,`EV_MT` | future leg value and MT costs/value | numeraire | MT | 058 | — | time/bin | costs ≥0,EV signed | no valid | SRC-004 |
| `P_+`,`N` | positive-PnL probability/sample count | probability/count | risk | 059 | 094–096 | sample | P∈[0,1],N>0 | no valid | SRC-004 |
| `Loss`,`α`,`VaR_α`,`ES_α` | loss variable/confidence/tail measures | numeraire;ratio;numeraire;numeraire | risk | 060 | 061,062,091 | confidence | Loss signed, α∈(0,1) | no valid | SRC-004 |
| `InventoryPenalty`,`StrandedPenalty`,`ModelUncertaintyPenalty`,`RAEV` | objective penalties/value | common numeraire | risk | 063 | 065,069,075 | candidate | penalties≥0,RAEV signed | no valid | SRC-004 |
| `I_a`,`I_a*`,`B_a`,`z_a`,`κ_a` | inventory/target/band/deviation/coefficient | asset;asset;asset;ratio;numeraire | inventory | 064 | 065–067 | asset | B>0,κ≥0,z signed | no valid | SRC-004 |
| `HardMin_a`,`HardMax_a`,`I_a^future` | hard inventory bounds/projected value | asset | risk | 066 | 075,076 | asset | ordered bounds | no | SRC-004 |
| `ΔI_a`,`NetFlow_a(W)` | signed inventory delta/flow | asset | inventory | 067 | — | asset,time | signed; zero valid | no | SRC-004 |
| `CurrentValue`,`BestExecutableExitValue`,`ExitCost` | current/executable value gap | numeraire | exit | 068 | 069–072 | exposure,state | cost generally ≥0 but source identity governs | unavailable possible | SRC-004 |
| `ExpectedExitCost`,`ExpectedIdleCost`,`ExpectedRiskCost` | stranded components | numeraire | capital | 069 | 071,072 | horizon | costs≥0 | no valid | SRC-004 |
| `V_start`,`V_end^net`,`RiskCost(P)`,`BridgeCost` | bridge values/cost | numeraire | bridge | 070 | 071,072 | path | cost signed by identity; risk cost≥0 | no valid | SRC-004 |
| `E[PnL_cycle]`,`N_BE` | expected cycle PnL/break-even cycles | numeraire/cycle;cycles | bridge | 071 | — | route | denominator must >0 | ∞ semantic possible | SRC-004 |
| `EV_destination`,`EV_stay`,`RelocationRiskCost` | relocation alternatives/cost | numeraire | capital | 072 | — | destination,horizon | EV signed,cost≥0 | no valid | SRC-004 |
| `ActualBalance`,`ReservedBalance`,`AvailableBalance` | account balance terms | asset | inventory | 073 | 075–078 | asset | available≥0 invariant | no | SRC-004 |
| `ObservedCapacity`,`ReservedCapacity`,`AvailableCapacity` | book capacity terms | leg input unit | sizing | 074 | 075–078 | leg/book | available≥0 invariant | no | SRC-004 |
| `q*`,`Q_validated`,`Gates(q)` | optimal/validated size and predicate | asset;asset;boolean | sizing | 075 | 076,077 | opportunity | sizes≥0 | empty set possible | SRC-004 |
| `Aq≤b`,`q_i` | portfolio resource matrix/vector | typed resource units | portfolio | 078 | — | opportunity/resource | feasibility constraint | no solution possible | SRC-004 |
| `PortfolioValue_after/before`,`RecoveryLoss`,`a` | recovery valuations/loss/action | numeraire/category | recovery | 079 | 080 | action,state | higher value good; loss positive bad | no safe action possible | SRC-004 |
| `Shock_i`,`ΔMarket_j(h)`,`R_i→j` | source shock/target change/conditional distribution | defined feature/distribution | participants | 081 | 082 | markets,horizon | distribution-defined | unavailable possible | SRC-004 |
| `E_0`,`E_h`,`Correction` | initial/future edge and correction ratio | edge;edge;ratio | participants | 082 | — | horizon | E0>0; correction signed | invalid if E0≤0 | SRC-004 |
| `λ_c` | competition/edge death hazard | 1/time | participants | 083 | — | time/context | ≥0 | model unavailable possible | SRC-004 |
| `L_total`,`L_feed`,`L_compute`,`L_sign`,`L_send`,`L_exchange` | latency total/stages | time | infra | 084 | 085,101 | server | ≥0 | missing stage invalid | SRC-004 |
| `L_decode`,`L_book`,`L_route`,`L_simulation`,`L_risk`,`L_decision` | compute substages | time | infra | 084 | — | server | ≥0 | missing stage invalid | SRC-004 |
| `GrossPnL_candidate/current`,`ΔGrossPnL` | comparable gross trading result/difference | numeraire | infra | 086 | 088,089,091 | server/config | signed | no valid | SRC-004 |
| `Cost_candidate/current`,`ΔCost` | comparable infra cost/difference | numeraire | infra | 087 | 088,089,091 | server/config | signed | no valid | SRC-004 |
| `NetUpgradeValue`,`InfraROI`,`SF`,`LCB_α` | upgrade value/ratio/safety/evidence bound | numeraire;ratio;ratio;numeraire | infra | 088 | 089,091 | confidence | signed except SF>0 | ROI invalid denom | SRC-004 |
| `GrossTradingPnL`,`TradingCosts`,`InfrastructureCost`,`NetPnL` | infra accounting components | numeraire | accounting | 090 | 092,100 | period/server | PnL signed,costs≥0 | no valid | SRC-004 |
| `InfraEfficiency`,`CaptureRatio` | diagnostic ratios | ratio | infra | 092 | 093 | period | signed/positive denominator | invalid denom possible | SRC-004 |
| `N_alive`,`N_eligible`,`ObservedSurvival` | survival cohort counts/rate | count/count/probability | validation | 094 | — | horizon | counts≥0,eligible>0 | empty cohort invalid | SRC-004 |
| `p_i`,`y_i`,`Brier`,`LL`,`ε` | predicted probability,label,scores,clip | probability;binary;ratio;ratio;ratio | calibration | 095 | 096 | sample | p∈[0,1],ε∈(0,.5),scores≥0 | no valid | SRC-004 |
| `RealizedPnL`,`PredictedPnL`,`PnLError`,`PnLBias` | PnL outcome/forecast/error/bias | numeraire | calibration | 097 | — | event/sample | signed; positive underprediction | outcome optional until matured | SRC-004 |
| `ActualSlippage`,`PredictedSlippage`,`SlippageError` | execution cost outcome/forecast/error | same ratio/bps | calibration | 098 | — | event | positive cost underprediction | outcome optional until matured | SRC-004 |
| `ObservedFillRate_B`,`MeanPredictedFill_B`,`CalibrationError_B` | bucket fill rates/error | probability points | calibration | 099 | — | bucket | signed; positive underprediction of fill | invalid empty bucket | SRC-004 |
| `EconomicLift`,`NetPnL_model/baseline` | comparable model lift/PnLs | numeraire | model value | 100 | 101 | experiment | signed | no valid | SRC-004 |
| `ModelValue`,`PnLLostDueToAddedLatency`,`OperationalCost` | net model contribution and costs | numeraire | model value | 101 | — | experiment | signed/costs≥0 | no valid | SRC-004 |
| `M`,`p_m`,`p̄`,`Disagreement` | model count/predictions/mean/spread | count/probability | uncertainty | 102 | 104 | model | M>0,p∈[0,1],spread≥0 | no valid | SRC-004 |
| `OODScore` | model-specific distance from support | model-defined score | OOD | 103 | 104 | artifact | ≥0,larger worse | unavailable possible | SRC-004 |
| six `*Gate`,`Confidence` | confidence gates/category | boolean/category | simulator | 104 | 075,076 | version/context | ordered category | gate unknown possible | SRC-004 |
| `C`,`OpportunityRate`,`T`,`IdleCost` | idle capital/rate/duration/cost | capital;value/(capital·time);time;numeraire | capital | 105 | 069 | horizon | nonnegative | no valid | SRC-004 |
| `ExecutionPnL`,`InventoryMTM`,`RebalancePnL`,`BridgePnL`,`EconomicPnL` | global PnL components/total | numeraire | accounting | 106 | 108–110 | period | signed | no valid | SRC-004 |
| `MTM_a`,`P_a^numeraire`,`ExternalFlow_a`,`ΔMTM_a` | asset value/valuation/external-flow-adjusted delta | numeraire;numeraire/asset;numeraire;numeraire | accounting | 107 | 106,108 | asset,time | signed | price unavailable possible | SRC-004 |
| `RoutePnL`,`RecoveryPnL`,`RebalancePnL`,`InventoryPnL`,`StrategyPnL` | disjoint strategy attribution | numeraire | accounting | 108 | 106 | period/component | signed | no valid | SRC-004 |
| `E_t`,`Peak_t`,`DD_t`,`DD_t^rel`,`MDD` | equity, running peak, drawdown, max | numeraire;numeraire;numeraire;ratio;numeraire | risk | 109 | 110 | time | DD/MDD≥0 valid | relative/empty invalid possible | SRC-004 |
