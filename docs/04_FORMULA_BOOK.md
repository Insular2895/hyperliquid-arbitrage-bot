# 04 — Formula Book

## Règles de gouvernance

Ce registre est l'unique catalogue mathématique. Une formule porte un ID, une
version et des unités; Rust/Python doivent partager golden vectors et tolérances
explicites. Les règles exchange utilisent ticks/lots/fixed point; un modèle peut
calculer en flottant puis repasse par PrecisionEngine. `PnL>0` est un gain,
`Loss=-PnL`; `1 bp=10^-4`. Aucun coût déjà inclus dans `NetConvert` ou
`EV_execution` n'est soustrait deux fois.

Statuts abrégés : `L` LOCKED, `C` CALIBRATED, `D` valeur dynamique, `A`
architecture/structure locked, `M` LEARNED/model-dependent. QF-099 ne porte pas
de label explicite dans la source; sa définition est conservée et son statut
formel reste à confirmer en revue.

## Pricing, depth, precision

| ID | S | Définition canonique |
|---|---:|---|
| QF-001 Mid | L | `Mid_t=(Bid_t+Ask_t)/2` |
| QF-002 Spread | L | `Spread_t=Ask_t-Bid_t` |
| QF-003 Relative spread | L | `RelSpread=Spread/Mid`; `Spread_bps=10^4 RelSpread` |
| QF-004 Base depth | L | `D_base(K)=Σ_{k=1..K} q_k` |
| QF-005 Quote depth | L | `D_quote(K)=Σ_{k=1..K} p_k q_k` |
| QF-006 Band depth | L | ask `Σ_{p_i≤Ask_1(1+δ)}p_iq_i`; bid `Σ_{p_i≥Bid_1(1-δ)}p_iq_i`; bandes δ calibrées |
| QF-007 Size quantization | L | `q_valid=floor(q/lot)·lot` |
| QF-008 Price validity | L+external | règle source : spot max 5 chiffres significatifs et max décimales `8-szDecimals`, entiers permis; passer par PriceQuantizer, jamais `round(price,5)`; `EXTERNAL_RULE_REQUIRES_REVALIDATION` |
| QF-009 Base→Quote walk | L | consommer bids: `Q_out^gross(q)=Σ p_k·min(q_remaining,q_k)`; invalide si profondeur insuffisante |
| QF-010 Quote→Base walk | L | consommer asks: `B_out^gross(v)=Σ min(v_remaining,p_kq_k)/p_k` |
| QF-011 VWAP | L | `VWAP=Σ p_k q_k^fill / Σ q_k^fill` |
| QF-012 BUY slippage | L | `(VWAP_buy-Ask_1)/Ask_1` |
| QF-013 SELL slippage | L | `(Bid_1-VWAP_sell)/Bid_1` |
| QF-014 Fee rate | L+D | `f_{market,mode}` issu de l'état `userFees`, historisé; rebate possible `f<0` |
| QF-015 Fee value | L | `FeeEconomicValue=Notional·f`; `FeeAssetDelta` séparé pour reconciliation |
| QF-016 NetConvert | A | `NetConvert(A,B,q_A,S)=q_B^net`; si frais débités en B, `q_B^net=Quantize_B(GrossConvert(A,B,q_A)-FeeDebit_B)`; sinon FeeEngine expose les asset deltas et `EconomicOutput=GrossOutput-FeeValueConverted`. Ne jamais supposer universellement `output·(1-fee)` |

## Routes, alpha and edge curves

| ID | S | Définition canonique |
|---|---:|---|
| QF-017 Direct output | L | `D(q_A)=NetConvert(A,B,q_A)` |
| QF-018 Indirect output | L | `q_X=NetConvert(A,X,q_A)`; `I(q_A)=NetConvert(X,B,q_X)` |
| QF-019 OWA edge | L | `E_OWA(q)=I(q)/D(q)-1` |
| QF-020 OWA gain | L | `Gain_B(q)=I(q)-D(q)` |
| QF-021 Triangle output | L | `T(q_A)=NC(B,A,NC(X,B,NC(A,X,q_A)))` |
| QF-022 Triangle return | L | `R_triangle(q)=T(q)/q-1` |
| QF-023 Triangle PnL | L | `PnL_triangle(q)=T(q)-q` |
| QF-024 ConversionAlpha | L | `I_TT(q)/D_T(q)-1` (ou outputs absolus associés): structure de route à intention immédiate équitable |
| QF-025 ExecutionAlpha | L | `I_MT(q)/I_TT(q)-1`: avantage/coût du mode, jamais attribué à OWA |
| QF-026 Edge curve | L | `E:q↦E(q)` calculée après chaque niveau/rounding; peut être discontinue |
| QF-027 Maximum profitable size | L | `Q_max= sup{q:E(q)≥E_min}` sur quantités valides; `E_min` est C |

## Microstructure and liquidity

| ID | S | Définition canonique |
|---|---:|---|
| QF-028 Queue imbalance | L | `QI=(Q_bid-Q_ask)/(Q_bid+Q_ask)` si dénominateur >0 |
| QF-029 Multi-level imbalance | L/C | `QI_K=(Σw_kQ^b_k-Σw_kQ^a_k)/(Σw_kQ^b_k+Σw_kQ^a_k)`; structure locked, `w_k` calibrés |
| QF-030 Bid OFI event | L | `e^b_n=1[P^b_n≥P^b_{n-1}]q^b_n-1[P^b_n≤P^b_{n-1}]q^b_{n-1}` |
| QF-031 Ask OFI event | L | `e^a_n=1[P^a_n≤P^a_{n-1}]q^a_n-1[P^a_n≥P^a_{n-1}]q^a_{n-1}` |
| QF-032 OFI | L | `OFI_W=Σ_{n∈W}(e^b_n-e^a_n)` |
| QF-033 MLOFI | A/C | `MLOFI_W=Σ_k w_k OFI_{k,W}`; structure locked, weights calibrés |
| QF-034 Microprice | L | `Micro=(Ask·Q_bid+Bid·Q_ask)/(Q_bid+Q_ask)` |
| QF-035 Microprice dislocation | L | `δ_micro=(Micro-Mid)/Mid` (bps `×10^4`) |
| QF-036 Log return | L | `r_t=ln(Mid_t/Mid_{t-1})` |
| QF-037 Realized variance | L | `RV_W=Σ_{t∈W} r_t²` |
| QF-038 Realized volatility | L | `σ_W=sqrt(RV_W)` |
| QF-039 Jump score | A/C | `JumpScore=|r_t|/(σ_fast+ε)`; structure locked, horizon/threshold calibrés |
| QF-040 Depth participation | L | `DP(q,δ)=Notional(q)/DepthQuote(δ)`; profondeur nulle implique conceptuellement `+∞` et reject |
| QF-041 Volume participation | L | `VP(q,W)=Notional(q)/MarketVolume(W)` |
| QF-042 Mechanical impact | L | buy `(VWAP-Mid_0)/Mid_0`; sell `(Mid_0-VWAP)/Mid_0` |
| QF-043 Resilience | L | `Resilience(t)=(D_t-D_s)/(D_0-D_s)`; reporting clamped `[0,1]`, valeur brute conservable si sur-replenishment |

## Survival, maker and execution distribution

| ID | S | Définition canonique |
|---|---:|---|
| QF-044 Survival | L target | `S(t|X)=P(T>t|X)` |
| QF-045 Discrete hazard | M | `h_k(X)=P(T∈[t_k,t_{k+1}) | T≥t_k,X)` |
| QF-046 Survival from hazard | L | `S(t_k|X)=Π_{j<k}(1-h_j(X))` |
| QF-047 Half-life | L | `t_1/2=inf{t:S(t|X)≤0.5}` |
| QF-048 Capture probability | L | `P_capture=E_L[S(L|X)]` |
| QF-049 Expected edge at arrival | M | `E_arrival=E[Edge_{t+L}|X_t]`; aucune décroissance exponentielle imposée |
| QF-050 Above threshold | M | `P_exec=P(Edge_{t+L}>E_minimum|X_t)` |
| QF-051 Maker fill survival | M | `S_fill(t|X)=P(T_fill>t|X)` |
| QF-052 Maker fill CDF | L | `F_fill(t|X)=1-S_fill(t|X)` |
| QF-053 Expected fill time | L/M | `E[T_fill|X]=∫_0^∞ S_fill(t|X)dt` (ou somme discrète) |
| QF-054 Adverse BUY | L | `AS_buy(h)=(P_f-Mid_{t_f+h})/P_f`; positif = adverse |
| QF-055 Adverse SELL | L | `AS_sell(h)=(Mid_{t_f+h}-P_f)/P_f`; positif = adverse |
| QF-056 Expected Value | L | `EV=Σ_i p_i PnL_i`, scénarios exclusifs, `Σp_i=1` |
| QF-057 Execution EV | A | `EV_exec=P_F E[PnL|F]+P_P E[PnL|P]+P_R E[PnL|R]+P_X E[PnL|X]` |
| QF-058 MT EV | A+M | `EV_MT=∫ f_fill(t|X)·EV_leg2(t)dt-C_adverse-C_recovery`; discret : `Σ_k P(T_f∈B_k)EV_leg2(t_k)-C_adverse-C_recovery` |
| QF-059 Positive PnL | L | `P_+=P(PnL>0)`; MC `N^-1Σ1[PnL_i>0]` |
| QF-060 Loss | L | `Loss=-PnL` |
| QF-061 VaR | L | `VaR_α=inf{l:P(Loss≤l)≥α}` |
| QF-062 Expected Shortfall | L | `ES_α=E[Loss | Loss≥VaR_α]` avec estimateur tail documenté |
| QF-063 Risk-adjusted EV | C | `RAEV=EV_exec-InventoryPenalty-StrandedPenalty-ModelUncertaintyPenalty` sans double décompte |

## Inventory, capital, sizing and recovery

| ID | S | Définition canonique |
|---|---:|---|
| QF-064 Inventory deviation | L | `z_a=(I_a-I*_a)/B_a` |
| QF-065 Soft penalty | C | baseline `Penalty_a=κ_a z_a²` dans les soft bands |
| QF-066 Hard gate | L | rejeter si `I^future_a<HardMin_a` ou `>HardMax_a`; exception seulement recovery/reconciliation explicitement gouvernée |
| QF-067 Net flow | L | `NetFlow_a(W)=Σ_{trades∈W} ΔI_a` |
| QF-068 Exit cost | A | `ExitCost(X)=CurrentValue(X)-BestExecutableExitValue(X)` via NetConvert |
| QF-069 Stranded penalty | C | `ExpectedExitCost+ExpectedIdleCost+ExpectedRiskCost`, composantes séparées |
| QF-070 Bridge cost | A | `BridgeCost(P)=V_start-V_end^net+RiskCost(P)` |
| QF-071 Break-even cycles | L | `(BridgeCost+ExpectedExitCost)/E[PnL_cycle]` si dénominateur >0, sinon `∞` |
| QF-072 Relocation value | A | `EV_destination-EV_stay-BridgeCost-ExpectedExitCost-RelocationRiskCost`; move si supérieur à threshold/hystérésis C |
| QF-073 Available balance | L | `ActualBalance_a-ReservedBalance_a≥0` |
| QF-074 Available book capacity | L | `ObservedCapacity_j-ReservedCapacity_j` |
| QF-075 Sizing objective | L | `q*=argmax_q RAEV(q)` sous balance, book, impact, `ES_α`, `P_+`, confidence et hard inventory gates |
| QF-076 Validated capacity | L | `Q_validated=sup{q:Gates(q)=TRUE}` |
| QF-077 Sizing search | L | grille de quantités valides → meilleure région → raffinement local; aucun gradient supposé |
| QF-078 Portfolio allocation | L | `max_q Σ_i RAEV_i(q_i)` sous `Aq≤b` (capital, profondeur, inventaire, risque) |
| QF-079 Recovery objective | L | `argmax_a E[PortfolioValue_after(a)|CurrentState]`, équiv. `argmin ExpectedRecoveryLoss(a)` |
| QF-080 Recovery loss | L | `PortfolioValue_beforeRecovery-PortfolioValue_afterRecovery`; sunk costs antérieurs exclus |

## Participant response and infrastructure

| ID | S | Définition canonique |
|---|---:|---|
| QF-081 Cross-market response | M | `R_{i→j}(h)=P(ΔMarket_j(h)|Shock_i,X)`, distribution cible |
| QF-082 Correction velocity | L | `(E_0-E_h)/E_0`, `E_0>0`; 1 = disparition, >1 = inversion |
| QF-083 Competition hazard | M | `λ_c(t|X)`; commencer par hazard edge global si causes non identifiables |
| QF-084 Infra latency | L | `L_total=L_feed+L_compute+L_sign+L_send+L_exchange`; `L_compute=L_decode+L_book+L_route+L_sim+L_risk+L_decision` |
| QF-085 Capture by server | L | `P_capture,s=E_{L_s}[S(L_s)]` |
| QF-086 Gross PnL difference | L | `ΔGrossPnL=GrossPnL_candidate-GrossPnL_current`, univers/stratégie/capital identiques |
| QF-087 Incremental cost | L | `ΔCost=Cost_candidate-Cost_current` |
| QF-088 Net upgrade value | L | `ΔGrossPnL-ΔCost` |
| QF-089 Infra ROI | L | `ΔGrossPnL/ΔCost` si `ΔCost>0`; sinon comparer NetPnL |
| QF-090 Infra net PnL | L | `GrossTradingPnL-TradingCosts-InfrastructureCost`, sans double compter les trading costs |
| QF-091 Upgrade gate | C | `LCB_α(ΔGrossPnL)>SF·ΔCost`; `SF` calibré |
| QF-092 Infra efficiency | L | `NetPnL/InfraCost`; diagnostic, objectif principal `max NetPnL` |
| QF-093 Capture ratio | L | `ΣRealizedPnL_i/ΣExpectedExecutablePnL_i`, pas moyenne naïve des ratios |
| QF-094 Observed survival | L | `N_alive(h)/N_eligible`, censure traitée en survival analysis |

## Calibration, model value and accounting

| ID | S | Définition canonique |
|---|---:|---|
| QF-095 Brier | L | `N^-1Σ(p_i-y_i)²` |
| QF-096 Log loss | L | `-N^-1Σ[y_i ln p_i+(1-y_i)ln(1-p_i)]`, `p` clippé à `[ε,1-ε]` |
| QF-097 PnL error | L | `RealizedPnL-PredictedPnL`; bias `E[PnLError]` |
| QF-098 Slippage error | L | `ActualSlippage-PredictedSlippage`; positif = coût sous-estimé |
| QF-099 Fill calibration | review | par bucket `ObservedFillRate_B-MeanPredictedFill_B` |
| QF-100 Economic lift | L | `NetPnL_model-NetPnL_baseline`, mêmes dataset/capital/frais/risk budget |
| QF-101 Model value | L | `PnL_with-PnL_without-PnLLostDueToAddedLatency-OperationalCost`; promotion si robustement >0 OOS |
| QF-102 Disagreement | L feature | `sqrt(M^-1Σ_m(p_m-p̄)²)`, `p̄=M^-1Σp_m` |
| QF-103 OOD | M | `OODScore≥0`, plus grand = hors support; méthode liée au modèle, aucune formule universelle |
| QF-104 Confidence | gates | DataFidelity, Freshness, OOD, SampleSupport, ModelAgreement, LatencyUncertainty → HIGH/MEDIUM/LOW/REJECT; aucun faux score pondéré |
| QF-105 Idle cost | C | `Capital·OpportunityRate·T`, rate empirique des opportunités abandonnées |
| QF-106 Economic PnL | L definition | `ExecutionPnL+InventoryMTM+RebalancePnL+BridgePnL-InfrastructureCost`, composantes séparées |
| QF-107 Inventory MTM | L definition | `MTM_a=I_a·P_a^numeraire`; `ΔMTM=MTM_t-MTM_{t-1}-ExternalFlow_a` |
| QF-108 Strategy PnL | L definition | `ΣRoutePnL+ΣRecoveryPnL+ΣRebalancePnL+InventoryPnL`; economic PnL retire l'infra |
| QF-109 Drawdown | L definition | `Peak_t=max_{u≤t}E_u`; `DD_t=Peak_t-E_t`; relatif `DD_t/Peak_t` |
| QF-110 Maximum drawdown | L definition | `MDD=max_t DD_t` |

## Formules exclues du core V1

Black-Scholes, Greeks, Heston, SABR, CAPM, Markowitz classique et surfaces de
volatilité options : `REJECTED FOR CORE / FUTURE DOMAIN`. Elles ne répondent pas
au routing spot actuel.

## Paramètres non inventés

`E_min`, horizons/fenêtres, OFI weights, jump threshold, hazard/queue/maker et
cross-market parameters, inventory/stranded/uncertainty penalties, `P_min`,
`ES/CVaR` limits, confidence gates, relocation thresholds, maker max age, ACK
timeout et infra `SF` restent `CALIBRATED/LEARNED`.

## Source

SRC-004, Dossier 2/6. QF-008 et toute mécanique exchange doivent être
revalidées officiellement avant codage.
