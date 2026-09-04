# 07 — Counterfactual Simulator

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## 1. Purpose

The Counterfactual Simulator estimates the execution and economic outcome of a candidate plan at one or more sizes. It combines recorded market reality, exchange mechanics, realistic arrival latency, our hypothetical action, calibrated response uncertainty, recovery, and risk distributions. Its output is an `ExecutionForecast`; Risk decides whether execution is allowed.

Its scientific claim is deliberately narrow: **a calibrated distribution of plausible outcomes for interventions inside validated support**, never the exact alternate future.

## 2. Scope

The Simulator owns counterfactual branching, simulated exchange execution, arrival-book walking, `Shadow Book` mutation, maker queue scenarios, response sampling, multi-market propagation, recovery outcomes, Monte Carlo aggregation, `SimulationConfidence`, and result provenance. It consumes the same formulas and state-machine semantics as Live; it does not create parallel financial math.

## 3. Non-goals

This pass does not implement the emulator, queue models, or trading code. It does not choose final sizing/slicing, Risk thresholds, exact recovery transitions, Data field layouts, graph construction, or deployment policy. It does not identify real competitors from synthetic agents, promise exact L4 queue truth from L2, or promote F4 research to production authority.

## 4. Fundamental epistemic limit

**WE CANNOT RECONSTRUCT THE EXACT ALTERNATE WORLD.** Once our hypothetical order changes a book, later historical trades, cancels, and updates may describe a world in which that intervention never occurred. Even perfect pre-intervention state cannot reveal with certainty how every participant would have reacted.

Therefore the simulator must not say “this is exactly what would have happened.” Earlier exact-alternate-world implications are `SUPERSEDED / REJECTED`. The target is a reproducible, calibrated distribution of plausible outcomes, with unsupported regions marked `LOW`, `OOD`, or rejected.

Three problems remain separate:

1. **Exchange Mechanics** — what the order and the exchange do mechanically.
2. **Historical Compatibility** — which future historical events remain applicable after intervention.
3. **Market Response** — how liquidity, participants, and linked markets may respond probabilistically.

No single “impact model” may collapse these layers.

## 5. Replay / Shadow / Counterfactual distinctions

| Concept | Market source | Order/effect boundary | Claim |
|---|---|---|---|
| Historical Replay | Recorded events | `ReplayTransport`; simulated fills | Reproduce what the bot knew and decided under declared assumptions. |
| Shadow Live | Current live feed | `NullShadowTransport`; `WouldSubmitEvent` | Observe decisions and market continuation without our real impact. |
| Counterfactual Replay | Recorded/live-derived baseline | Simulated intervention and, by mode, modeled response | Estimate plausible consequences of our action. |
| Micro-live | Live feed | Real transport, fills, and account under small calibrated limits | Produce intervention evidence for calibration, not a separate strategy. |

`RunMode`, `SimulationMode`, and Replay fidelity are independent provenance axes. “Paper” must not ambiguously cover all four cases.

## 6. Simulator architecture

The logical pipeline is:

```text
Recorded/live-derived state → ReplayClock → decision engine
→ latency/arrival state → HyperliquidExchangeEmulator
→ Δour / maker queue → counterfactual branch
→ conditional local + sparse cross-market Δresponse
→ scenario/recovery paths → PnL distribution
→ SimulationConfidence → RiskDecision
```

The deterministic exchange/mechanical layer precedes stochastic response. Rust is the intended runtime engine boundary; Python may fit, calibrate, diagnose, and compare models offline. This language direction is architectural, not implementation approval.

## 7. Exchange mechanics

`HyperliquidExchangeEmulator` consumes an `OrderIntent` through `ReplayTransport` and emits the same `OrderEvents` and `FillEvents` schemas used by Live. It must use closure-authoritative order state transitions, precision, rounding, price protection, fees, partial fills, cancels, and recovery boundaries.

The architecture supports IOC, ALO/Post Only, GTC, and price-time priority, but the current Hyperliquid definitions and ordering behaviour are `EXTERNAL_REVALIDATION`. F0/F1 validation must not depend on a stale external claim. Blind `fill_at_best_price()` and generic percentage slippage are forbidden substitutes.

## 8. Exact decision timeline

The decision starts at observation time `t0`, then includes decode, book update, route evaluation, simulation, Risk, decision, signing, outbound transport, exchange ingress, exchange ordering, and matching. Conceptually:

```text
t_arrival = t0 + L_compute + L_sign + L_network + L_exchange
```

QF-084 is authoritative and refines this as `L_total = L_feed + L_compute + L_sign + L_send + L_exchange`, with compute decomposed into decode/book/route/simulation/risk/decision. Components are measured or sampled from empirical distributions; a hidden fixed `20 ms` constant is not canonical.

## 9. Arrival state

A protected taker executes against the **arrival book at `t_arrival`**, not the book observed at `t0`, except in an explicit zero-latency test. `recv_ts` defines what the bot knew; `exchange_ts` supports market chronology. Counterfactual latency changes our execution path without granting look-ahead.

## 10. Mechanical impact

Given a chosen arrival state and order, Mechanical Impact is the direct, book-mechanical effect of our order. A protected taker walks the arrival book with QF-009/QF-010, derives QF-011 VWAP, QF-012/QF-013 slippage, QF-014/QF-015 fees, QF-016 `NetConvert`, and QF-042 impact. It produces executed quantity, level consumption, residual quantity, partial fill, and IOC residual cancellation as applicable.

Depth and volume participation use QF-040/QF-041. They condition model support; they do not replace the actual book walk.

## 11. Shadow Book

For each affected market, `Shadow Book` / `Shadow State` is the baseline plus our residual mechanical delta. It preserves consumed levels, our resting maker quantity, estimated queue state, fills, partial fills, cancellations, and account/inventory consequences. `ActualAccountState` and `ShadowCounterfactualState` remain distinct.

`Δour` may contain volume consumed, queue insertion, resting size, price-level mutation, fills/partials, order removal, and the consequent simulated inventory. Only the market directly traded is mechanically mutated.

## 12. Historical incompatibility

If history later cancels 400 units from a level where our branch leaves only 200, applying `200 - 400` is invalid. Similar incompatibilities arise when a historical trade consumes liquidity already removed or assumes a different queue/order identity. Each event application must either remain compatible, be reconciled under an explicit versioned rule, or make the branch diverge. It must never silently create negative depth or fictitious queue certainty.

Invalid dataset regions, gaps, and corrupt state are not evidence; PASS 06 owns their complete policy.

## 13. Exogenous Replay

`SimulationMode::ExogenousReplay` keeps future historical market data externally given. Our action changes our simulated fills, inventory, fees, and PnL but does not claim to alter the historical market path. It is useful for small-impact analysis, latency/mechanical studies, reproducible baselines, and comparisons.

Its limitation is explicit: counterfactual feedback is absent. Low participation can support the approximation; it never proves zero causal response.

## 14. Interactive Counterfactual

`SimulationMode::InteractiveCounterfactual` creates a branch in which our intervention can change future state through mechanical impact, queue evolution, calibrated participant response, stochastic flow, and cross-market response. It returns scenario distributions—not exact reality—and must carry `BranchId`, path identity, models, support, confidence, and rejoin provenance.

The two `SimulationMode` values may be compared, but never silently mixed inside one result.

## 15. Multi-market branches

Each route market has a logically separate baseline and delta. If Leg 1 trades `A/X`, only the `A/X` book receives direct Mechanical Impact. `X/B` or `B/A` may change only through their own later orders or modeled Cross-Market Response.

Interactive propagation uses a sparse `pair_to_response_neighborhood`-like set of economically connected markets, not a dense `N×N×horizons` live matrix. PASS 08 later owns the graph. Each leg re-evaluates its arrival state, remaining edge, Dominant Decay Leg evidence, and response uncertainty.

## 16. Participant / response integration

The Simulator consumes PASS 02 `EdgeSurvivalForecast`, `LiquidityForecast`, `MakerForecast`, and `CrossMarketForecast`; it does not rebuild a second Participant Engine. Participant models emit calibrated distributions or bounded scenario inputs, confidence, OOD, versions, horizons, and lineage.

The initial `Δresponse` direction is a **Conditional Empirical Model**: select historical states/shocks comparable in market, side, size/depth, spread, depth, imbalance, OFI, microprice, volatility, intensity, regime, time, and route context; estimate distributions of price, spread, depth, replenishment, cancellations, new flow, and linked-market response. Exact binning/kernel method and coefficients are `LEARNED / CALIBRATED`.

Queue-Reactive, Hawkes, point-process, ML, and explicit agents are Challengers/Research. Sophistication alone is not promotion evidence. Other participants are initially represented by aggregate conditional flow, not fictional identities.

Conceptually:

```text
World_cf = HistoricalBaseline + Δour + Δresponse
```

This is a decomposition, not a new QF identifier. `Δresponse` is conditional, stochastic, validated, and kept separate from known mechanical consumption.

## 17. Maker queue uncertainty

Maker simulation is not “taker with zero fee.” At arrival, existing same-price quantity precedes our order under the declared price-time model. With L2, aggregate size changes cannot reveal whether volume traded or cancelled ahead/behind us. Exact queue reconstruction is therefore forbidden.

Three L2 queue modes expose the uncertainty:

- `PESSIMISTIC`: cancellations never reduce `queue_ahead`; only observed trades advance it. Lower-bound fill scenario.
- `OPTIMISTIC`: all cancellations at the level are treated as favourable/ahead. Upper-bound sensitivity scenario, never production truth.
- `PROBABILISTIC`: calibrated `P(cancel ahead | state)` and flow/fill distributions advance the queue stochastically.

Outputs include `P(fill by t)`, time-to-first/full-fill, expected filled quantity, partial-fill probability, survival while resting, cancellation outcome, and adverse selection by supported horizon. QF-051–QF-055 and QF-058 govern semantics. L4 compatibility is retained, but current spot L4 availability is not assumed.

Canonical search terms: **Maker Fill Survival** is QF-051 and **Expected Fill Time** is QF-053. The sparse cross-market set is also known by the source spelling **response neighborhood**.

## 18. Scenario generation

The future is a set of scenarios, not one path. Every random variable must map to a calibrated input distribution: latency, queue advancement/fill, partial fill, local response, cross-market response, recovery, or supported dependence. Arbitrary noise is forbidden. Dependence is preserved where learned evidence supports it; otherwise the limitation is declared rather than hidden behind independence.

Slicing scenarios may compare one immediate order, same-time children, time-spaced children, and adaptive fragmentation. Same-time children on the same book should reproduce approximately the same immediate depth consumption as their aggregate. Temporal fragments differ because of replenishment, response, volatility, edge survival, competition, queue evolution, and inventory exposure. PASS 07 owns any live slicing choice.

## 19. Monte Carlo

Monte Carlo belongs in the Simulator, outside Participant hot-path inference. Each path is linked to `run_id`, seed, `BranchId`, and `MonteCarloPathId`. It samples only model-supported uncertainties, applies the same execution/recovery mechanics, and emits a distribution over mutually exclusive terminal outcomes.

Reproducibility requires identical ordered inputs, resolved config, model artifacts, formula version, and RNG seed to reproduce the same sampled paths and aggregates under the declared numeric/runtime contract.

## 20. Recovery simulation

Full completion is not the only path. A route can partially fill, lose a later leg, become invalid, enter recovery, or terminate with residual inventory. The Simulator evaluates candidate Recovery outcomes with the same policy interface/state semantics as Live; it does not assume magical full recovery.

QF-079 selects recovery by expected post-action portfolio value / minimum expected recovery loss. QF-080 measures loss from the state at recovery start; earlier losses are sunk costs. PASS 04 owns exact states and permitted actions.

## 21. Risk distributions

`ExecutionForecast` includes `p_full`, `p_partial`, `p_recovery`, `p_failure`, expected PnL, PnL quantiles, QF-059 `P(PnL>0)`, expected fees/slippage, and QF-060–QF-062 loss/VaR/ExpectedShortfall. QF-056/QF-057 aggregate mutually exclusive outcomes; QF-063 adds only non-duplicated penalties.

Mean and median alone are insufficient: a rare catastrophic failure can dominate route choice. CVaR/ExpectedShortfall is consumed by Risk under PASS 05 thresholds; the Simulator reports it and does not choose the limit.

Multi-size runs evaluate QF-026 `E(q)`, QF-027 profitable size, completion/recovery distributions, impact, and confidence without assuming linear scaling. They feed QF-076 `Q_validated`; PASS 07 owns final sizing.

QF-059 is the canonical **Probability Positive PnL** reference. QF-076 is the canonical **Validated Capacity** reference.

## 22. SimulationConfidence

QF-104 forbids a decorative fixed weighted score. Explicit gates cover data fidelity, freshness, sample support, OOD, model agreement, and latency uncertainty; source-supported reporting also explains impact participation, queue observability, response dispersion, calibration health, and cross-market complexity. Output is auditable (`HIGH`, `MEDIUM`, `LOW`, `REJECT`) with causes, not just `0.78`.

Confidence cannot create evidence. Higher nominal fidelity with uncalibrated models may deserve lower confidence than a supported F1 baseline. Low confidence reduces size, requests fallback, or rejects through Risk; it never upgrades capital authority.

## 23. Branch-and-rejoin

An interactive intervention creates a bounded branch. As QF-043 liquidity resilience and modeled response residuals decay, an explicit `CounterfactualRejoinEvent` may rejoin the historical baseline when a calibrated compatibility rule is satisfied. The event records the fact and reason through Data Contracts; no silent snap-back is permitted.

The canonical **Rejoin event** is therefore an auditable state/event transition, not an implicit horizon expiry.

The horizon depends on market, size, participation, volatility, depth, replenishment, response support, and multi-market divergence. There is no fixed universal `100 ms`. If the branch remains materially incompatible, do not force rejoin: terminate conservatively, expose residual uncertainty, label `LONG_HORIZON_COUNTERFACTUAL_UNRELIABLE`/OOD as applicable, and reduce authority.

## 24. Fidelity F0–F4

| Fidelity | Added capability | Taker | Maker queue | Response | Cross-market | Explicit agents | Authority |
|---|---|---:|---:|---:|---:|---:|---|
| `F0Historical` | Historical book, fees, rounding, simple L2 fills | Baseline | No | No | Historical only | No | Research/replay baseline |
| `F1LatencyMechanical` | Realistic arrival, arrival book, Shadow Book, book walk, partial fill, Mechanical Impact | Yes | No | No | Mechanical locality only | No | Production-capable after M2–M4 evidence |
| `F2Queue` | F1 + price-time maker queue and L2 uncertainty/fill distribution | Yes | Yes | Queue only | Mechanical locality | No | Maker-dependent use only after calibration |
| `F3Responsive` | F2 + OFI, resilience, empirical local and sparse Cross-Market Response | Yes | Yes | Calibrated aggregate | Yes | No | Decision use only inside validated support |
| `F4Interactive` | F3 + advanced point processes, synthetic order flow, agent worlds | Yes | Yes | Advanced research | Yes | Yes | `RESEARCH ONLY` until separately validated |

Fidelity describes modeled capability, not bot release version, `RunMode`, Participant P-level, maturity M-level, or confidence. Every result declares its fidelity and unmodeled claims.

## 25. Determinism / RNG

The deterministic core obeys:

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig,
                  ModelArtifacts, FormulaVersion, Seed)
```

Events are applied in an explicit stable order; receive-time replay enforces no look-ahead. `ReplayClock` replaces hidden wall-clock calls. Strategic timeouts are recorded `TimerEvent`s. `RngProvider` uses the `RunManifest` seed. Fixed-point/tick/lot rules and the single Formula/Fee/Precision/Route/Risk/Execution/Recovery/Inventory/Reservation engines prevent Replay/Live drift.

Parallel workers may calculate immutable-snapshot results, but a result carries `input_state_version`; stale results are discarded or revalidated and decisions commit through an ordered coordinator.

## 26. Data Contracts

PASS 06 owns exact field schemas. PASS 03 consumes the established semantics of `RunMode`, `SimulationMode`, `ReplayFidelity`, `BranchId`, `MonteCarloPathId`, `CounterfactualRejoinEvent`, `ConfidenceState`, `ExecutionForecast`, `EdgeSurvivalForecast`, `LiquidityForecast`, `MakerForecast`, `CrossMarketForecast`, `LatencyTrace`, `TimerEvent`, `GoldenDataset`, `DecisionTrace`, `RunManifest`, `ModelArtifact`/`ModelVersion`, RNG seed, and state hashes.

Every result records mode, fidelity, models, dataset, config, formulas, schemas, build/commit, seed, and state lineage. `RunMode` may change source, transport, explicit flags, Risk profile, or capital; it may not silently change strategy logic or financial math.

## 27. Calibration

Calibration compares Predicted versus Actual by market, side, size/depth, spread, volatility, regime, fidelity, queue visibility, and horizon. Required targets include arrival state/latency, fill/partial rates, time-to-fill, slippage error (`ActualSlippage - PredictedSlippage`), adverse selection, response/replenishment, recovery loss, PnL quantiles, and interval coverage.

A claimed 95% interval should contain approximately 95% of comparable outcomes when assumptions hold. Exact construction, sample minima, and tolerance thresholds remain calibrated. Champion/Challenger promotion requires temporal OOS quality, distribution calibration, economic lift, runtime safety, Shadow, and Micro-live evidence as relevant—not complexity.

## 28. Shadow / Micro-live validation

Shadow validates opportunity evolution, edge survival, arrival-state prediction, would-execute decisions, latency, and observed response without revealing our own causal impact. Micro-live uses real small orders to observe send/ack/fill latency, fills/partials, slippage, cancellations, recovery, post-trade book, and PnL. Historical `€40–50` examples are calibration probes, never universal sizing rules.

Maturity follows M0 Specified → M1 Unit → M2 Replay → M3 Shadow → M4 Micro-live → M5 Live, bounded by critical dependencies. `Backtest Cannot Override Live Evidence`: persistent supported live contradiction removes simulator authority. Risk owns the `Simulator Calibration Kill Switch`, which may reduce size or disable model-dependent strategies.

## 29. OOD / drift

Unseen size/participation, market, regime, volatility, route structure, queue state, shock magnitude, response neighbourhood, or unsupported horizon triggers explicit OOD handling. Drift or model disagreement degrades `ConfidenceState`; fallback must be more conservative. Invalid data, stale forecasts, schema mismatch, non-finite output, and calibration failure cannot yield a confident forecast.

## 30. Research layers

Queue-Reactive, Hawkes, advanced ML, synthetic order flow, explicit `MarketMakerAgent`/`ArbitrageAgent` worlds, and long-horizon non-rejoining universes are Research/Challenger layers. They support stress, what-if, sensitivity, and interaction studies. They do not represent actual competitor identities or production truth by construction.

## 31. External revalidation

Before implementation or production reliance, revalidate current Hyperliquid price-time priority, IOC/ALO/GTC semantics, batching/ordering, public feed timing and L2 granularity, L4 availability, `order_book_server` spot support, exchange timestamps, precision/metadata, fees, and affected API schemas. PASS 03 performed no web revalidation; source statements remain snapshots.

## 32. Deep-spec links

- [Purpose, modes, and epistemic limits](deep-specs/simulator/01_PURPOSE_MODES_AND_EPISTEMIC_LIMITS.md)
- [Exchange Emulator and arrival timeline](deep-specs/simulator/02_EXCHANGE_EMULATOR_AND_ARRIVAL_TIMELINE.md)
- [Shadow Book and Mechanical Impact](deep-specs/simulator/03_SHADOW_BOOK_AND_MECHANICAL_IMPACT.md)
- [Exogenous Replay and historical compatibility](deep-specs/simulator/04_EXOGENOUS_REPLAY_AND_HISTORICAL_COMPATIBILITY.md)
- [Interactive Counterfactual and market response](deep-specs/simulator/05_INTERACTIVE_COUNTERFACTUAL_AND_MARKET_RESPONSE.md)
- [Maker queue and fill simulation](deep-specs/simulator/06_MAKER_QUEUE_AND_FILL_SIMULATION.md)
- [Cross-market and multi-market branches](deep-specs/simulator/07_CROSS_MARKET_AND_MULTI_MARKET_BRANCHES.md)
- [Scenarios, Monte Carlo, and risk distributions](deep-specs/simulator/08_SCENARIOS_MONTE_CARLO_AND_RISK_DISTRIBUTIONS.md)
- [Branch/rejoin, confidence, and OOD](deep-specs/simulator/09_BRANCH_REJOIN_CONFIDENCE_AND_OOD.md)
- [Fidelity ladder F0–F4](deep-specs/simulator/10_FIDELITY_LADDER_F0_F4.md)
- [Validation, calibration, and Micro-live](deep-specs/simulator/11_VALIDATION_CALIBRATION_AND_MICRO_LIVE.md)
- [Runtime Data Contracts and determinism](deep-specs/simulator/12_RUNTIME_DATA_CONTRACTS_AND_DETERMINISM.md)

## Sources and authority

Primary detailed source: SRC-008. Closure authority: SRC-004 for formulas/execution definitions, SRC-005 for Risk/Data/Replay contracts, SRC-006 for validation, and PASS 02/SRC-007 for participant forecast semantics. SRC-001–003 provide uncontradicted historical architecture and workflow requirements. PASS 00 and legacy `/docs` are locators/comparison material, not design authority.
