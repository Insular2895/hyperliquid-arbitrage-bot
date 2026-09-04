# Model, Execution and Tail Risk

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Model gate sequence

Risk consumes validated forecasts only after hard market/account/resource eligibility. It then checks:

1. survival/competition and probability the edge remains at arrival;
2. expected arrival edge against the executable threshold;
3. artifact, feature-schema, market/regime/horizon/size support;
4. confidence, OOD distance and model disagreement;
5. Simulator confidence and calibration health;
6. execution forecast distributions;
7. probability of positive PnL, worst loss and Expected Shortfall/CVaR.

Hard OOD or invalid mandatory input rejects the dependent action. Soft OOD may reduce size only into validated support. A failed advanced model uses a validated conservative fallback or disables its dependent capability. Missing output cannot be ignored while retaining the same aggression.

## Execution-specific risk

- Maker: ALO/Post Only, maximum exposure/age, edge-death and toxicity checks, continuous T5 monitoring, immediate T3 reassessment after every fill.
- Taker: protected marketable limit, maximum slippage/impact and current capacity.
- Multi-leg: T4 before every next leg; quantity derives from actual previous fills, fees and rounding; compare current safe continuation against bounded recovery.
- Order ambiguity: no blind retry; preserve reservation and reconcile.

The current RiskDecision is necessary but not sufficient. ExecutionTransport also verifies action, size/price bounds, snapshot freshness, plan identity/config version and critical transport invariants immediately before send.

## Tail boundary

Risk evaluates outcome distributions from Simulator/Execution, including full, partial, failure and recovery branches. It consumes Formula Book objects `QF-059` probability positive, `QF-060` loss, `QF-061` VaR, `QF-062` Expected Shortfall, `QF-063` risk-adjusted EV and route/recovery loss bounds.

VaR alone is insufficient because it does not characterize the tail beyond the quantile. Positive mean EV or high `P(PnL > 0)` cannot override CVaR, worst-route-loss, hard inventory or recovery-tail limits. Mechanical impact and probabilistic market response remain separate to avoid double counting.

## Quality monitoring

Persistent actual-versus-predicted slippage, fill, PnL or recovery error can reduce size or trigger an execution-mode/strategy/market kill. Persistent Simulator or Participant miscalibration disables only dependent capabilities where safe. Backtest evidence never overrules persistent live contradiction, while isolated live samples are not sufficient proof of drift.

Source: SRC-005 lines 1273–1756, 2172–2512, 2812–2899 and 4021–4089.
