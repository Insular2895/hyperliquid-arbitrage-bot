# PASS 02 — Participant Model Boundaries

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 02 REVIEW COMPLETE`

| Capability | Classification | What is fixed | What is not fixed / activation boundary |
|---|---|---|---|
| Edge Survival | `PRODUCTION INTERFACE`; initial baseline direction | Economic lifetime object, survival outputs, latency integration and safe fallback. | Horizons/strata/support calibrated; no model-dependent production use before data/validation. |
| Empirical survival | `PRODUCTION BASELINE` / fallback | Simple, interpretable first Champion direction. | Must beat naive constant-survival baseline OOS and be censor-aware/calibrated. |
| Discrete Hazard | `PRODUCTION-CAPABLE CHALLENGER` | QF-045 target and QF-046 mapping. | Coefficients learned; promotion evidence required. |
| Liquidity Response | `PRODUCTION INTERFACE / NOT YET CALIBRATED` | Conditional distribution, mechanical separation, forecast semantics. | Estimator, horizons and response parameters learned; F3 activation after calibration. |
| Cross-Market Response | `PRODUCTION INTERFACE / NOT YET CALIBRATED` | QF-081 object, sparse graph, no causal overclaim. | Neighbours/horizons/model learned; OOS lift and ablation required. |
| Maker Fill | `PRODUCTION INTERFACE / NOT YET CALIBRATED` | Fill survival/CDF/time targets and queue-fidelity disclosure. | Fill model/horizons learned; maker activation requires live calibration. |
| Adverse Selection | `PRODUCTION INTERFACE / NOT YET CALIBRATED` | QF-054/055 sign and conditioning semantics. | Expected values/horizons learned; activation tied to maker validation. |
| Address Behaviour | `RESEARCH/FUTURE`, `EXTERNAL-DEPENDENT` | Address is not identity; passive/signature-only boundary. | Feed fields, privacy, lift, clusters and production need revalidation. |
| Survival GBDT | `CHALLENGER` | May capture nonlinearities/interactions. | Promoted only with robust calibration/economic/runtime improvement. |
| Deep Survival | `RESEARCH/FUTURE` | Allowed only as governed challenger. | Not justified absent additional value, robustness and acceptable runtime. |
| Queue-Reactive | `CHALLENGER / P5 RESEARCH` | State-dependent event-intensity research role. | Requires event fidelity and gain over simpler models; not initial hot-path baseline. |
| Hawkes | `CHALLENGER / P5 RESEARCH` | Self-/cross-excitation research role. | Complex calibration and runtime; use only if simple hazard is insufficient. |
| Explicit Agent Simulation | `P5 RESEARCH/STRESS` | Scenario/what-if laboratory. | Never production truth by construction; calibration/identifiability unresolved. |

## Cross-domain ownership

| Boundary | Participant owns | Other owner |
|---|---|---|
| Opportunity death | Remaining-lifetime labels/forecast conditional on the supplied economic rule. | Formula/Execution/Risk owns edge/cost/threshold semantics. |
| Mechanical impact | Participant owns subsequent learned collective response. | Exchange Emulator/Simulator owns deterministic book mutation and queue mechanics. |
| Forecast schemas | Participant defines semantic needs. | Data Contracts owns fields, types, units and serialization. |
| Trading decision | Participant emits distributions/confidence. | Risk/Execution owns permission and action. |
| Monte Carlo | Participant provides calibrated distributions/quantiles. | Simulator owns branching and PnL outcomes. |
| Latency | Participant integrates a supplied distribution with survival. | Infrastructure owns measurement and profile comparability. |
| Sizing/slicing | Participant provides survival/future-depth/response inputs. | Sizing/Simulator/Risk owns optimization and constraints. |

## Locked architecture versus learned model

The key PASS 02 correction is that a model interface can be final-capable and `LOCKED` while its estimator and parameters remain unknown. Survival, capture, maker fill, cross-market response, Risk gates and Data-contract semantics are not “mere research ideas”; using a particular GBDT, Hawkes process, cluster method or coefficient set still is.
