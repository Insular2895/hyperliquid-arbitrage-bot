# Simulator Validation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Fidelity | Meaning | Minimum validation | Prohibited claim |
|---|---|---|---|
| F0 | historical/exogenous replay | ordering, no lookahead, historical rules, trace determinism | causal effect of our order |
| F1 | latency + mechanical execution | arrival reconstruction, L2 walk, fees/precision/partial fixtures | participant response realism |
| F2 | ShadowBook/local intervention | conservation, our-order mutation and branch provenance | calibrated external response |
| F3 | stochastic learned response | temporal OOS, distribution calibration, OOD, Micro-live comparison | exact alternate universe |
| F4 | explicit participant/agent research | stylized facts, sensitivity, challenger comparison | production truth or permission |

Validation spans full/partial/zero/reject/cancel/Recovery paths, seeded Monte Carlo repeatability, branch/rejoin rules, queue bounds, cross-market response and outcome distributions. Compare predicted and actual fill, time, slippage, response, Recovery and PnL by support slice.

Fidelity availability does not imply validated maturity. Backtest contradiction by persistent live evidence triggers lower confidence/Q_validated, fallback or dependent capability suspension. F4 remains research even if computationally elaborate.
