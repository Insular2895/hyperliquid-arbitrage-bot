# PASS 03 — Simulator Mode and Fidelity Matrix

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Orthogonal dimensions

| Dimension | Canonical values | Governs | Does not govern |
|---|---|---|---|
| `RunMode` | `Replay`, `Paper`, `Shadow`, `MicroLive`, `Live` | source/transport, explicit Risk config, capital/environment provenance | strategy/formula logic or automatically selected fidelity |
| `SimulationMode` | `ExogenousReplay`, `InteractiveCounterfactual` | treatment of future market feedback | live transport or evidence maturity |
| `ReplayFidelity` | `F0Historical`, `F1LatencyMechanical`, `F2Queue`, `F3Responsive`, `F4Interactive` | enabled Simulator mechanics/models | confidence, Participant P-level, or M0–M5 maturity |

## Supported/meaningful combinations

| Run context | SimulationMode | Fidelity | Purpose / mechanics/models | Excluded | Capital | Determinism | Outputs / limitation / maturity |
|---|---|---|---|---|---|---|---|
| Replay | Exogenous | F0 | Historical reproduction, fees, rounding, simple fills | realistic arrival, queue, feedback | None by result alone | Deterministic | Baseline trace/PnL; M2 target. |
| Replay | Exogenous | F1 | Counterfactual latency, arrival book, book walk, partial, `Δour` | response feedback, maker queue | None by result alone | Deterministic if latency trace fixed; seeded if sampled | Mechanical distribution/baseline; M2 then compare Micro-live. |
| Replay | Exogenous | F2 | F1 + maker queue sensitivity/distribution while market future remains external | participant response | None for maker until calibrated | Deterministic bounds; seeded probabilistic queue | Queue envelope; explicit feedback omission. |
| Replay | Interactive | F1 | Branch carries deterministic `Δour`; useful mechanics control | `Δresponse` | None | Deterministic | Control branch, not responsive claim. |
| Replay | Interactive | F2 | F1 + queue branch | local/cross-market participant response | None until calibration | Bounds/seeded queue | Maker counterfactual limited by exogenous response. |
| Replay | Interactive | F3 | F2 + empirical local/liquidity/sparse cross-market `Δresponse`, branch/rejoin | explicit agents/uncalibrated advanced flow | Inside validated support only after Risk/M4 evidence | Seeded stochastic, reproducible | Full forecast distribution; M2–M4 required. |
| Replay | Interactive | F4 | F3 + Queue-Reactive/Hawkes/synthetic/agent worlds | production-truth claim | No default authority | Seeded experimental | Stress/what-if; Research only. |
| Shadow | N/A in base RunMode | N/A in base run; companion Replay forecast declares its F-level | Live-feed observation and would-submit through null transport | own actual causal impact/fill | Zero orders | Decision trace deterministic given recorded inputs | M3 observation. SRC-005 does not declare a direct SimulationMode/Fidelity combination for Shadow. |
| Paper | N/A in base RunMode | N/A unless a separately manifested Simulator run is attached | Real market plus simulated execution/account | real fills/account effects | Simulated only | Inputs/events recorded | Intermediate diagnostic. Do not infer Interactive semantics from `Paper`. |
| MicroLive | N/A for real execution; compare against separately identified forecasts | Forecasts may be F1–F3 | Same Live core, real small orders; compare prior forecast to actual | F4 as decision authority | Strict calibrated real caps | Actual events recorded; replay reproduces decision | M4 calibration, not profit-seeking. |
| Live | N/A for the real transport; consumes approved separately versioned forecast outputs | Approved forecast capability may be F1–F3 | Real source/transport; same core/formulas; deterministic expected/quantile inputs preferred | F4/unpromoted models | Only Risk-approved validated capacity | All important events/outputs recorded for replay | M5 does not mean permanent validity. |

Direct Shadow/Paper/MicroLive/Live combinations with `SimulationMode` are not enumerated by SRC-005 and are therefore not invented here. A companion counterfactual forecast is a separately manifested Simulator run. “Interactive Live” is not a separate `RunMode`; a promoted Interactive forecast may be consumed alongside Live only under Risk bounds. A random Monte Carlo path must never become “the future” selected by Live.

## Provenance invariant

Every result records all three axes plus Participant fidelity, maturity/evidence references, data/model/config/formula/schema/build versions, RNG seed, branch/path IDs, state hashes, and excluded capabilities. Comparisons across modes/fidelities must be labelled.
