# 08 — Scenarios, Monte Carlo, and Risk Distributions

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Scenario object

A scenario is one traceable combination of arrival latency, arrival state, exchange mechanics, queue evolution, fill/partial outcome, local/cross-market response, leg evolution, recovery, and terminal portfolio state. Futures are distributions over scenarios, not one forecast path.

Random variables may include empirically supported latency, queue advancement, time/quantity of fill, response vector, liquidity resilience, cross-market delay/magnitude, and recovery outcome. No arbitrary Gaussian/noise assumption is introduced. Correlation/dependence is preserved only where source/data/model support it.

## Monte Carlo provenance

Monte Carlo runs outside Participant hot-path inference. Each path carries `run_id`, `BranchId`, `MonteCarloPathId`, seed/stream identity, `SimulationMode`, fidelity, ordered input/state hashes, resolved config, dataset, model artifacts, formula/schema/build versions, and result confidence. Same contract inputs and RNG seed reproduce the same sample paths.

## Terminal partition

QF-057 uses mutually exclusive classes:

- `F`: full completion;
- `P`: partial completion/residual exposure;
- `R`: recovery path;
- `X`: failure/other terminal path.

Paths include later-leg invalidation, cancel/fill race, residual inventory, and Recovery candidate results. Recovery applies QF-079/QF-080 from the current state; sunk costs are not optimized away.

## Outputs

The distribution reports mean/median, PnL quantiles, variance where used, QF-059 probability positive, probabilities full/partial/recovery/failure, expected fees/slippage, expected/worst supported recovery loss, QF-060 loss, QF-061 VaR, QF-062 ExpectedShortfall/CVaR, QF-063 Risk-Adjusted EV inputs, and `SimulationConfidence`.

Risk owns tail limits and acceptance. Mean EV cannot conceal tail failure. QF-056/QF-057 define aggregation; no fee/slippage/recovery double subtraction is allowed.

## Multi-size and slicing

Evaluate a size curve `q1…qn` because depth, edge, fill, response, recovery, and confidence are nonlinear/discontinuous. Feed QF-026, QF-027, and QF-076 `Q_validated`; PASS 07 owns the final optimizer.

Candidate slicing scenarios are single immediate, same-time fragments, time-spaced fragments, and adaptive fragmentation. Temporal slicing changes replenishment, response, edge survival, competition, volatility, queue, and inventory exposure. The Simulator compares paths; it does not authorize a live policy.

## Failure behaviour

Non-finite samples, impossible state, invalid dataset region, unsupported distribution, or unreproducible paths invalidate the affected run. OOD tails reduce authority; they are not clipped into favourable outcomes.
