# Participant–Simulator Consistency Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Layer | Owns | Does not own | Consumer boundary | Result |
|---|---|---|---|---|
| Participants P0–P5 | collective survival, liquidity, maker and sparse cross-market forecasts | actual identity, execution permission, exact counterfactual | artifact/support/horizon/confidence to Simulator/Risk | PASS |
| Simulator F0 | historical/exogenous outcome reconstruction | causal alternate market | declared baseline | PASS |
| Simulator F1 | latency/arrival/mechanical own-book change | participant response | exact mechanical `Delta_our` | PASS |
| Simulator F2 | L2 queue uncertainty scenarios | exact L4 position | pessimistic/optimistic/probabilistic modes | PASS |
| Simulator F3 | calibrated stochastic response | exact alternate universe | point-in-time learned distributions | PASS |
| Simulator F4 | explicit interactive agents/research | production truth | Research only | PASS |

Mechanical impact is applied once before modeled response. Participant P-level and Simulator F-level are independent declared axes. `ExecutionForecast` partitions full/partial/recovery/failure mass, carries fidelity/support/seed/model versions and never authorizes capital. Backtest cannot override persistent supported live contradiction; demotion/fallback is scoped. Identity fabrication paths: **0**. Fidelity overclaims: **0**.
