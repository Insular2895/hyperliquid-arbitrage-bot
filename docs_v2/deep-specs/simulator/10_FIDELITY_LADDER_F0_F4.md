# 10 — Fidelity Ladder F0–F4

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

The ladder activates evidence-supported capabilities in one architecture. It is neither `RunMode`, `SimulationMode`, Participant P-level, validation maturity M-level, nor a sequence of disposable bot versions.

| Field | F0 — Historical | F1 — Latency + Mechanical | F2 — Queue | F3 — Responsive | F4 — Interactive Research |
|---|---|---|---|---|---|
| Inputs | Historical book, fees, rules | F0 + measured latency/arrival state | F1 + trades/cancels, queue observability, maker forecast | F2 + response/liquidity/cross-market forecasts | F3 + event/agent model inputs |
| Mechanics | Historical L2/simple fills, rounding | Arrival book, Shadow Book, protected walk, partial, Mechanical Impact | F1 + price-time insertion and queue modes | F2 + branch response/resilience | F3 + synthetic interactive flows/worlds |
| Models | None/rules | Empirical latency only | Pessimistic/Optimistic/Probabilistic queue | Conditional Empirical local/sparse cross-market response | Queue-Reactive, Hawkes, advanced ML/agents |
| Outputs | Historical baseline PnL/decisions | Taker fills/slippage/impact at arrival | Fill/time/partial/adverse distributions | Response and multi-market PnL distributions | Research stress/sensitivity distributions |
| Taker | Baseline simple | Yes | Yes | Yes | Yes |
| Maker | No credible queue | No | Yes, distributional | Yes | Yes |
| Market response | No | No | Queue-only | Calibrated aggregate | Advanced interactive |
| Cross-market | Historical observation only | Mechanical locality only | Same | Sparse conditional response | Rich research interaction |
| Explicit agents | No | No | No | No | Yes |
| SimulationMode fit | Exogenous | Exogenous; mechanics inside Interactive too | Either with declared feedback limit | Interactive for response claim | Interactive only |
| Calibration | Golden/historical | Latency + Predicted/Actual fill | Fill/time/adverse Micro-live | Response/distribution/cross-market | Separate experimental validation |
| Intended use | Reproduction and baseline | Taker/mechanics and arrival studies | Maker/queue evaluation | Supported response-aware decisions | Stress/what-if research |
| Capital authority | None by fidelity alone | Only after Risk and M2–M4 evidence | None for maker until calibrated | Inside validated support only | None by default |
| Known limit | No realistic arrival/feedback | No maker queue/response | L2 queue uncertainty; no participant response | Model/OOD/branch uncertainty | Identifiability and synthetic-world risk |
| Promotion gate | F0 DoD and determinism | Arrival/mechanical vs actual | Fill distribution calibrated; recovery tested | Temporal OOS, coverage, economic lift, Shadow/Micro-live | Must beat Champion and remain explicitly governed |

## Closure alignment

SRC-008 labels: `F0 — Historical`, `F1 — Latency + Mechanical`, `F2 — Queue`, `F3 — Responsive`, `F4 — Interactive Research`. SRC-005 serialized names are `F0Historical`, `F1LatencyMechanical`, `F2Queue`, `F3Responsive`, `F4Interactive`. SRC-006 validates F0 simple mechanics, F1 arrival/impact/partial, F2 distributional queue, F3 calibrated participant response, and keeps F4 Research.

## Result invariants

Every `ExecutionForecast` records exact fidelity and excluded capabilities. F0 cannot claim maker probability; F1 cannot claim participant feedback; F2 cannot imply exact L2 queue; F3 cannot exceed model support; F4 cannot become production truth by label. Higher fidelity is enabled only after lower deterministic contracts and required data/evidence exist.
