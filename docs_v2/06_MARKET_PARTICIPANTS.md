# 06 — Market Participants and Competition

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## 1. Purpose

The Market Participants domain predicts execution-relevant collective market response. Its central question is not who a competitor is, but the probability distribution of what the market will do before, during and immediately after our execution.

The three fundamental model interfaces are:

1. `EdgeSurvivalEngine`: will an economically executable opportunity remain when we arrive?
2. `LiquidityResponseEngine`: what book distribution are we likely to encounter after observed flow or our intervention?
3. `CrossMarketResponseEngine`: how may relevant neighbouring markets respond to a shock on one market?

These forecasts improve expected net PnL, sizing, execution and risk. They are not present merely to make a simulator look realistic.

## 2. Scope

PASS 02 specifies:

- collective-response and competition semantics;
- the P0–P5 participant-fidelity ladder;
- opportunity lifetime, survival, hazard, capture and arrival-edge forecasts;
- participant-facing microstructure features;
- liquidity, cancellation, replenishment and future-depth forecasts;
- maker fill-time and adverse-selection forecasts;
- sparse cross-market response and correction;
- optional pseudonymous behaviour signatures;
- Champion/Challenger governance, temporal validation, OOD, disagreement, drift and fallback;
- bounded runtime inference and interfaces to Data, Risk, Execution, Simulator, Sizing, Infrastructure and Market Atlas.

Formula definitions remain owned by SRC-004 and the future Formula Book pass. Data schemas remain owned by the Data Contracts pass. Risk and execution permissions remain owned by their respective closure domains.

## 3. Non-goals

This domain does not:

- reconstruct the psychology, strategy or real-world identity of each trader;
- treat invented market-maker, arbitrageur or retail agents as production truth;
- claim exact counterfactual futures;
- infer causality from correlation or lead/lag alone;
- redefine mechanical book impact, exchange matching or queue mechanics;
- put large Monte Carlo, Hawkes calibration or neural training in the live participant hot path;
- self-modify production model weights from live observations;
- turn a forecast or monitoring score into permission to override Risk.

## 4. Core philosophy — behaviour, not identity

Canonical search phrase: **behaviour not identity**.

Canonical terminology used throughout this domain includes **Survival Function**, **Expected Edge at Arrival**, **Probability Above Execution Threshold**, **Competition Hazard**, **Maker Fill CDF**, **CrossMarketResponseMatrix**, **lead-lag**, **event study**, **Address Behaviour Signature**, **Model Disagreement** and **Model Drift**. The sparse response engine replaces a dense CrossMarketResponseMatrix; retaining the term here makes the rejected design searchable.

Historical market data already contains actions by real participants. Production begins by measuring their aggregate effects:

- opportunity decay and survival;
- adds, cancellations, aggressive flow and replenishment;
- future depth and spread;
- maker fills and post-fill adverse moves;
- cross-market correction distributions.

Latent behaviour labels can describe observable patterns, but they are not identity claims. `ParticipantAddress`, `BehaviourSignature` and `BehaviourCluster` are the permitted terms. Address-level features remain optional until they demonstrate stable incremental predictive and economic lift.

## 5. Participant Engine architecture

```text
Point-in-time Market / Route / Opportunity state
        + measured latency distribution
        + optional intervention description
                         |
                         v
                 ParticipantEngine
        +----------------+----------------+
        |                |                |
        v                v                v
 EdgeSurvival      LiquidityResponse   CrossMarketResponse
        |                |                |
        +----------------+----------------+
                         |
                         v
    compact forecasts + confidence + provenance
                         |
       +---------+-------+---------+----------+
       v         v                 v          v
   Simulator   Risk/Execution    Sizing   Infrastructure/Atlas
```

The architecture can support higher fidelity from the start, but only validated components are active. An interface being `LOCKED` does not mean its parameters are known.

## 6. P0–P5 fidelity ladder

| Level | Meaning | Initial role |
|---|---|---|
| `P0` | Historical participants: recorded tape already contains real activity. | Required data foundation. |
| `P1` | Edge Survival: empirical lifetime, survival/hazard and arrival capture. | First production-capable model dependency after sufficient data. |
| `P2` | Aggregate Response: OFI, liquidity, replenishment and cancel pressure. | Progressive production interface; activate per validated capability. |
| `P3` | Cross Market: sparse lead/lag candidates and response distributions. | Later activation after temporal OOS lift and ablation. |
| `P4` | Participant Signatures: pseudonymous address/behaviour features. | Optional; never an initial production dependency. |
| `P5` | Interactive Research: Queue-Reactive, Hawkes and ABIDES-like agents. | Research/stress layer, not production truth. |

One architecture supports all levels. Runs must declare active participant fidelity separately from Simulator fidelity. Initial production must not depend on P4 or P5.

## 7. Edge Survival

For route `r`, size `q` and time `t`, `E_r(t,q)` is the net executable edge under the authoritative route, cost and execution definitions. An opportunity is born when the applicable entry rule and data/risk preconditions hold. It dies when it no longer clears the applicable execution threshold, validated capacity falls below `q`, or another authoritative condition makes execution economically non-viable. `E_enter > E_exit` may provide calibrated hysteresis.

With `T` the remaining lifetime conditional on point-in-time state `X`:

```text
S(t | X) = P(T > t | X)                       QF-044, LOCKED object
h_k(X) = P(T in [t_k,t_{k+1}) | T >= t_k, X) QF-045, LEARNED
S_k = product_{j=1..k}(1 - h_j)               QF-046, LOCKED
t50 = inf{t : S(t) <= 0.5}                    QF-047, LOCKED
```

If the curve never reaches 0.5 inside its supported horizon, report `t50 > model_horizon`; do not fabricate a value. Cause-specific hazard is a future refinement. The initial reliable target is total observable edge-death hazard.

## 8. Capture versus latency

Infrastructure supplies a latency distribution `L`, not one constant. Capture therefore integrates the entire distribution:

```text
P_capture = E_L[S(L)]
```

The histogram estimator in QF-048 sums latency-bucket probability times survival at the bucket representative. QF-085 applies the same object to infrastructure candidate `s`. `S(E[L])` is not equivalent because survival is nonlinear and latency tails can dominate missed opportunities.

The engine also returns the learned arrival-edge distribution, including:

- `E_arrival = E[Edge_{t+L} | X_t]` (QF-049);
- `P_exec = P(Edge_{t+L} > E_minimum | X_t)` (QF-050);
- edge quantiles and model confidence.

`E_minimum` is not defined here. A positive edge may still be below the authoritative execution threshold.

## 9. Microstructure feature families

Survival and response models may consume point-in-time, provenance-bearing features for the route, each leg and the wider regime:

- current edge, age, derivative/decay, size and executable capacity;
- spread, depth, depth slope and levels required;
- Queue Imbalance and Multi-Level Imbalance;
- true event-level OFI, MLOFI and signed trade flow;
- snapshot-difference OFI proxy when the feed cannot expose events;
- microprice and microprice dislocation;
- trade intensity, cancellation/replenishment proxies;
- volatility, jumps, time of day, regime, activity and cross-market state.

QI, OFI or microprice is never a standalone permission to trade. The exact QF-028..035 definitions are summarized in the microstructure deep spec. Windows, levels, weights, normalizations and activation are `CALIBRATED` or `LEARNED`.

Feed capability is explicit. Event-level OFI requires ordered event-level book updates. A public L2 snapshot stream can only support a labelled snapshot proxy; the two must never share provenance or calibration silently.

## 10. Liquidity Response

`LiquidityResponseEngine` predicts a conditional distribution such as:

```text
P(Book_{t+h} | Book_t, observed flow, OurShock)
```

Targets can include future depth, spread, best prices, microprice, additions, cancellations, aggressive orders and replenishment. QF-043 defines normalized liquidity resilience after a shock:

```text
Resilience(t) = (D_t - D_s) / (D_0 - D_s)
```

Display values may be clamped to `[0,1]`; raw values may preserve over-replenishment. Invalid denominators must be rejected. Future depth is a distribution, not the currently visible L2 copied forward.

Mechanical consumption by our order belongs to Exchange/Simulator mechanics. Subsequent participant response is probabilistic. The learned target must exclude double-counting of mechanical impact.

## 11. Maker forecasts

The maker model predicts more than eventual fill:

- fill probability at supported horizons;
- maker fill survival and CDF;
- time to first and full fill, expected filled quantity and partial-fill probability;
- expected fill time, with horizon conditioning stated where used;
- edge survival while the order rests;
- post-fill adverse selection by side and horizon;
- expected cleanup/recovery costs and confidence.

For fill time `T_f`, QF-051 defines `S_f(t|X)=P(T_f>t|X)` and QF-052 defines `F_f=1-S_f`. QF-053 integrates fill survival for expected fill time. QF-054/055 define positive adverse selection as a movement against the filled maker position.

Maker fee advantage alone is insufficient: fill can arrive precisely when the quote becomes toxic, the second leg can deteriorate, and recovery may be required. QF-058 MT EV is referenced but owned by Formula/Execution.

Exact cancellation allocation and queue evolution under L2 remain Simulator/Exchange concerns for PASS 03. Participant models forecast distributions under declared queue observability; they do not pretend to reconstruct an exact queue from snapshots.

## 12. Cross-Market Response

For a source-market shock `i`, QF-081 defines the learned target; QF-082 defines correction and QF-083 defines the learned Competition Hazard boundary:

```text
R_{i->j}(h) = P(Delta Market_j(h) | Shock_i, X)
```

The response graph is sparse: same-asset markets, route neighbours, triangle neighbours and empirically supported lead/lag candidates. A dense `N × N × horizons` model is rejected because it inflates compute, memory, false correlation and overfit.

Event studies observe target mid, spread, depth and OFI at supported horizons, conditioned on state, volatility, shock size, direction and liquidity. Cross-correlation, lagged regression or Granger-like discovery may propose candidates, but correlation does not prove direct causal impact. Production entry requires temporal OOS predictive lift and with/without ablation.

QF-082 correction velocity captures gradual as well as binary decay. `DominantDecayLeg` may summarize which route leg most often drives economic death. `RouteCompetitionScore` is monitoring-only; Risk consumes direct distributions, tails and confidence.

## 13. Optional participant signatures

When a passive public trade record provides pseudonymous counterparties and that fact is externally revalidated, the research pipeline may derive:

- markets and time-of-day activity;
- size/frequency distributions, burstiness and buy/sell symmetry;
- market-transition graphs;
- `ReactionDelay` to a defined event;
- `FastCorrectionSignature` and its conditional activity probability.

One address can represent multiple strategies and one entity can use multiple accounts, subaccounts, vaults or API wallets. Clusters indicate behavioural similarity, never proven common ownership. No mass per-address account queries or unsupported deanonymization are allowed. Exact addresses should be minimized or hashed when identity is unnecessary.

## 14. Model governance

The source-derived progression is:

| Class | Role |
|---|---|
| Empirical survival / Kaplan–Meier-style stratification | Initial simple, interpretable Champion/fallback after validation. |
| Discrete hazard | Production-capable learned model; interpretable challenger or Champion candidate. |
| Survival GBDT | Challenger for nonlinearities and interactions. |
| Deep survival | Research/Future; only if calibration, replay economics, runtime and robustness improve. |
| Queue-Reactive | Challenger/P5 research for state-dependent event intensities. |
| Hawkes | Challenger/P5 research for self-/cross-excitation. |
| Explicit agents | P5 research and stress scenarios, not forecasts unless empirically calibrated and separately promoted. |

The Champion controls decisions. Challengers receive the same point-in-time features and log predictions without affecting orders. Training and calibration occur offline in Python; approved compact artifacts are inferred in Rust. Production does not update its own weights online.

Each artifact records model ID, training dataset/window, feature schema, Git revision, hyperparameters, validation metrics and supported markets, regimes and sizes.

## 15. OOD, disagreement and drift

Confidence depends on data fidelity, sample support, regime/route/size support, feed age, model dispersion and available L2/L4 capability. QF-103 requires a non-negative OOD score whose model-specific method is versioned; larger means farther outside validated support.

QF-102 measures dispersion across probabilistic models. Significant disagreement is uncertainty, not a voting mechanism that can bypass Risk. Drift monitoring compares calibration and feature distributions across recent and longer windows.

For OOD, stale/incompatible features, unavailable/corrupt artifacts, NaN output, excessive drift or unsupported disagreement:

- mark confidence low/OOD;
- use a conservative empirical fallback when valid;
- add risk buffer and reduce size where Risk permits;
- reject model-dependent routes or disable the affected strategy when no safe fallback exists.

Failure must reduce capability.

## 16. Hot-path constraints

The live path performs incremental feature updates plus small bounded inference. It may use precomputed quantiles, lookup tables, expected values and tail values. It does not run large Monte Carlo, Hawkes simulation, neural training or explicit agent worlds on every update.

Every forecast carries model/version, feature-schema version, as-of/event time, input lineage, fidelity, supported horizon and confidence. Stale or schema-incompatible results are rejected. Monte Carlo draws participant-response scenarios inside the Simulator, not inside participant inference.

## 17. Risk interfaces

Risk may consume direct `p_survive_arrival`, `p_above_threshold_arrival`, arrival-edge quantiles, liquidity loss/tails, maker fill/adverse-selection estimates, cross-market response and confidence. It must not blindly consume a composite competition score.

Survival, maker toxicity, cross-market consistency, OOD, drift and model availability can only tighten or block decisions according to the Risk Constitution. Participant output never relaxes a hard risk limit.

## 18. Simulator interfaces

The Simulator consumes calibrated distributions or compact scenario inputs. It owns the counterfactual branch, mechanical impact, exchange mechanics, queue counterfactuals, partial-fill paths, recovery and PnL distribution. Participant models supply stochastic response, not a single certain future.

Historical `EXOGENOUS_REPLAY` and `INTERACTIVE_COUNTERFACTUAL` remain distinct. P0–P5 participant fidelity is separate from F0–F4 Simulator fidelity.

## 19. Sizing, Infrastructure and Market Atlas interfaces

- Sizing uses future-depth distributions, survival, impact and recovery risk; unsupported sizes become OOD and are reduced or rejected.
- Slicing compares replenishment against edge decay, competition and inventory risk; replenishment alone never justifies waiting.
- Infrastructure combines measured latency distributions with survival through QF-048/QF-085 and evaluates economic benefit after cost.
- Market Atlas records time-windowed, versioned survival, correction, replenishment, toxicity and response statistics; it may inform HOT/WARM/COLD selection but cannot create trading permission.
- Recovery may consume Liquidity and Cross-Market forecasts after partial fills.

## 20. Validation

Random row splits are forbidden for time-dependent market models. Validation uses past-to-future splits, walk-forward evaluation, new-regime/asset/liquidity slices, right-censor handling and point-in-time feature reconstruction.

Required evidence includes:

- probability calibration by horizon and support slice;
- Brier score (QF-095), Log Loss (QF-096), integrated Brier and survival calibration where applicable;
- fill calibration error (QF-099) for maker forecasts;
- EconomicLift (QF-100) on the same dataset, capital, fees and risk budget;
- ModelValue after added latency and operational cost (QF-101);
- feature/model ablations, OOD tests, fallback/fault injection and runtime bounds;
- replay, shadow and micro-live predicted-versus-realized calibration before model-dependent scaling.

The initial participant Champion must beat a naive constant-survival baseline out of sample. Cross-market requires predictive improvement and ablation. Maker strategy activation requires calibrated fill and adverse-selection models plus tested second-leg recovery. No universal numerical promotion threshold is invented in this pass.

## 21. Calibrated and learned parameters

The following remain data-derived and versioned: opportunity thresholds owned elsewhere; survival/fill horizons; strata and censor policy details; hazard coefficients; feature windows; MLOFI weights; shock and response representations; sparse neighbours; response delays; fill and adverse-selection horizons; confidence/OOD methods; drift thresholds; fallback support; promotion gates and runtime budgets.

## 22. Research and future capabilities

Cause-specific hazards, event-level L4 models, address clusters, survival GBDT, deep survival, Queue-Reactive, Hawkes and explicit agent worlds are retained as governed capabilities. None is required for initial production. A higher-complexity model is promoted only when it produces robust temporal OOS statistical improvement, calibration improvement, positive economic lift after latency/operations, acceptable runtime, stable behaviour and safe OOD/fallback results.

## 23. External revalidation

This pass does not browse or revalidate live facts. Before depending on them, revalidate the current public feed cadence/semantics and counterparty fields; node raw-book-diff/order lifecycle capabilities; spot L4 support; and the applicability of cited academic findings to Hyperliquid data. Until then, such facts are source snapshots or external-dependent assumptions, not current guarantees.

## 24. Deep specifications

- [Objective, Scope and Fidelity Ladder](deep-specs/participants/01_OBJECTIVE_SCOPE_AND_FIDELITY_LADDER.md)
- [Edge Survival, Hazard and Capture](deep-specs/participants/02_EDGE_SURVIVAL_HAZARD_AND_CAPTURE.md)
- [Microstructure Features, OFI and Microprice](deep-specs/participants/03_MICROSTRUCTURE_FEATURES_OFI_AND_MICROPRICE.md)
- [Liquidity Response, Replenishment and Resilience](deep-specs/participants/04_LIQUIDITY_RESPONSE_REPLENISHMENT_AND_RESILIENCE.md)
- [Maker Fill, Queue and Adverse Selection](deep-specs/participants/05_MAKER_FILL_QUEUE_AND_ADVERSE_SELECTION.md)
- [Cross-Market Response and Correction](deep-specs/participants/06_CROSS_MARKET_RESPONSE_AND_CORRECTION.md)
- [Participant Signatures and Address Behaviour](deep-specs/participants/07_PARTICIPANT_SIGNATURES_AND_ADDRESS_BEHAVIOUR.md)
- [Model Governance, Validation, OOD and Fallback](deep-specs/participants/08_MODEL_GOVERNANCE_VALIDATION_OOD_AND_FALLBACK.md)
- [Runtime Inference and Cross-Domain Contracts](deep-specs/participants/09_RUNTIME_INFERENCE_AND_CROSS_DOMAIN_CONTRACTS.md)

## Sources

Original sources SRC-001..008, with SRC-004 authoritative for formulas, SRC-005 for Risk/Data contracts, SRC-006 for validation/activation and SRC-008 for Simulator interaction. SRC-007 is the principal detailed participant-model source. PASS 00 is a locator, not design authority.
