# PASS 03 — Simulator Validation Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

No numerical acceptance threshold is invented. Targets marked “calibrated” require a versioned Validation/Risk decision and support analysis.

| Capability | Evidence source | Replay validation | Shadow validation | Micro-live validation | Metric / calibration target | OOD / failure behaviour | Maturity / authority |
|---|---|---|---|---|---|---|---|
| Latency arrival | `LatencyTrace`, recorded events, infra benchmarks | receive-time/no-look-ahead; QF-084 decomposition; seeded distribution | predicted arrival/book versus observed continuation | send/ack/fill trace and arrival-state reconstruction | latency quantiles and arrival-state error by infra/regime | stale/missing trace → lower fidelity/reject | F1; M2 then M3/M4; SRC-004/005/006 |
| Taker mechanics | books, rules, intents, actual fills | Golden QF-009–016 walk, fees, rounding, protection | would-fill only; no causal fill proof | per-level/qty/VWAP/slippage versus actual | exact fixture invariants; fill/price error | invalid rules/state → no fill/result invalid | F0/F1; SRC-004/006 |
| Partial fills | protected depth, order/fill events | insufficient-depth, residual, IOC and later-leg paths | estimate only | actual partial/residual/cancel | predicted partial rate/quantity and state reconciliation | impossible residual or mismatch → fail | F1; Execution closure + SRC-006 |
| Queue mechanics | L2 trades/cancels; L4 if revalidated | Pessimistic/Optimistic bounds; seeded probabilistic repeat | would-rest evolution | real maker order queue/fill | bound coherence, queue advancement support | L2 ambiguity explicit; unsupported → pessimistic/reject | F2; SRC-008/005/006 |
| Maker fill | `MakerForecast`, own events | QF-051–053/QF-099 survival/CDF/timing/quantity | probability vs observed market opportunity only | calibration by probability bucket/horizon | fill calibration, timing/partial error | queue visibility/support OOD → conservative | F2, M4 before dependent activation; SRC-004/006/PASS02 |
| Adverse selection | maker fills + later mids | signed QF-054/055 by horizon | no own-fill validation | actual post-fill move and second-leg economics | prediction/quantile error and MT lift | unsupported horizon/state → adverse buffer/reject | F2+, M4; SRC-004/006 |
| Liquidity response | shock-labelled book/trade paths | separate mechanical delta; temporal OOS | predicted depth/spread/replenishment vs observed exogenous shocks | post-intervention response | distribution coverage, depth/spread/resilience error | unsupported shock/regime → omit with lower fidelity/reject | F3 only after calibration; PASS02/SRC-008 |
| Cross-market response | aligned source/target events | sparse event study, common-factor/clock tests, ablation | neighbour continuation forecast | real intervention target response | per-target/horizon coverage/error, QF-081/082, economic lift | unsupported neighbour ≠ zero; low confidence | F3; PASS02/SRC-004/006 |
| Recovery | partial/failure fixtures and real events | same Recovery Engine, QF-079/080, sunk-cost tests | candidate outcome only | actual action/loss/time/state | recovery rate/loss quantiles and state reconciliation | missing valid recovery → conservative terminal failure | F1+, exact states PASS04; SRC-004/005/006 |
| PnL distribution | all terminal paths | seeded QF-056–060 aggregation/hash | observed market outcome without causal fill caveat | actual PnL versus predicted distribution | mean/median/quantiles/P+/full/partial/recovery/failure coverage | non-finite/impossible/probability sum error → invalid | F1–F3; SRC-004/006 |
| VaR/CVaR | loss paths | QF-060–063 fixtures and seeded tails | diagnostic only | tail exceedance/coverage when support sufficient | VaR quantile and ExpectedShortfall calibration | insufficient tail support → LOW/reject size | Risk gate PASS05; SRC-004 |
| `SimulationConfidence` | support/fidelity/freshness/OOD/agreement/calibration | each QF-104 gate and cause tested | cause/level versus observed errors | confidence-stratified calibration | monotone fail-conservative outcomes; no fake score | any hard gate/OOD/drift → LOW/REJECT | all fidelities; SRC-004/005/006 |
| Branch-and-rejoin | branch events, residuals, baseline | compatibility/conflict fixtures; variable horizons | response-decay diagnostics | post-trade residual/book compatibility | false-rejoin, non-rejoin, horizon/support, explicit event | never force rejoin; terminal unreliable/OOD | F3; threshold calibrated; SRC-005/008 |

## Common validation invariants

1. Same ordered events/config/models/formulas/seed reproduce `DecisionTrace` and sampled paths under the declared contract.
2. Random row split is insufficient; learned models use point-in-time temporal/walk-forward OOS.
3. Distribution calibration is evaluated by market/side/size/regime/horizon/fidelity/support, not only globally.
4. Statistical accuracy alone is insufficient: economic lift, tail risk, runtime, operations, and fallback matter.
5. Shadow cannot prove causal impact without a sent order; Micro-live supplies that evidence.
6. A capability cannot exceed the maturity of a critical dependency.
7. Persistent supported live contradiction overrides Replay and activates Risk's calibration response.
8. F4 remains Research regardless of apparent backtest quality until separately promoted; no automatic production path is defined.
