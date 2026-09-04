# Risk Gate Pipeline

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Authority: SRC-005 sections 38–61, 111–148 and 201–204. Gate ordering is constitutional; individual values remain calibrated/learned/exchange-defined.

## Canonical order

| # | Stage | Checks | Failure direction | Cost class |
|---:|---|---|---|---|
| 1 | `SYSTEM HEALTH` | Engine mode, kills, clock, feeds, infra, critical dependencies. | Scope reject/halt; no new risk. | Cheap |
| 2 | `DATA VALIDITY` | Market-state validity, sequence, book freshness, metadata, fees, precision, cross-market anomaly. | Invalidate + resync; reject affected route. | Cheap |
| 3 | `ACCOUNT CONSISTENCY` | Orders, fills, balances, account/reconciliation versions. | Lock affected capital; reconcile. | Cheap |
| 4 | `RESOURCE AVAILABILITY` | Available/reserved balance, shared depth, API/action/connection capacity, concurrency. | Reject/resize; reserve safety capacity first. | Cheap |
| 5 | `HARD INVENTORY` | Future hard bands, hard capital/market/asset/strategy/mode limits. | Hard reject except strict known-exposure reduction. | Cheap |
| 6 | `MARKET / IMPACT` | Spread, liquidity, depth/volume participation, impact, volatility, jump, outlier. | Reject or evidence-bounded smaller size. | Bounded |
| 7 | `MODEL SUPPORT / OOD` | Survival/arrival support, confidence, hard/soft OOD, disagreement, fallback. | Conservative fallback, resize or dependent kill/reject. | Bounded |
| 8 | `EXECUTION FORECAST` | Full/partial/failure/recovery distribution, maker/taker/continuation support. | Reject/mode kill/resize. | Moderate |
| 9 | `TAIL RISK` | P positive, loss, VaR diagnostic, ES/CVaR, route/recovery loss. | Hard reject/resize inside support. | Moderate/high |
| 10 | `SOFT INVENTORY / PORTFOLIO` | Soft bands, net flow, concentration, terminal/stranded, dependency/shared-resource constraints. | Penalize, resize, rebalance preference or reject. | Moderate |
| 11 | `EV` | Expected PnL after real costs and minimum economic significance. | Economic reject, distinct reason family. | Moderate |
| 12 | `FINAL SIZE` | Intersection of all capacity bounds and `Q_validated`; optimizer over safe candidates only. | `q*=0` or `ALLOW_REDUCED_SIZE`. | Bounded optimization |
| 13 | `PRE-SEND REVALIDATION` | Fresh snapshot/TTL, decision-plan match, size/price/action/config bounds. | Refuse transport and reevaluate. | Cheap |

## Named gate families

- Eligibility: `SystemHealthGate`, `DataValidityGate`, `FreshnessGate`, `AccountConsistencyGate`, `ResourceAvailabilityGate`, `HardInventoryGate`.
- Market: `SpreadGate`, `LiquidityGate`, `DepthParticipationGate`, `VolumeParticipationGate`, `ImpactGate`, `VolatilityGate`, `JumpGate`, `OpportunityOutlierGate`, `CrossMarketConsistencyGate`.
- Model: `SurvivalGate`, `ExpectedArrivalEdgeGate`, `ModelConfidenceGate`, `OODGate` (hard/soft), `ModelDisagreementGate`, `SimulationGate`.
- Outcomes: `PositivePnLGate`, `ExpectedPnLGate`, `TailRiskGate`, `MaxSingleRouteLossGate`, `RecoveryTailRiskGate`.
- Portfolio/size: soft inventory, net flow, concentration, terminal viability, stranded/bridge, capital-at-risk, concurrency/dependency, expected-loss budget, portfolio tail, validated capacity and final sizing.

## Fast reject

Stages 1–5 run before expensive Simulator/model/optimizer work. Obvious stale, corrupt, unknown, unreconciled, unreserved or hard-limit failures return immediately with metric and reason. Stage 13 repeats cheap critical checks to close time-of-check/time-of-use drift.

## Runtime contract

Evaluation is deterministic, I/O-free, allocation-light and based on one immutable RiskSnapshot. It emits one canonical action plus size/price constraints, hard rejects and warnings. Each stage records latency and result for audit; acceptable P50/P95/P99/P99.9 values remain calibrated.

Source: SRC-005 lines 1033–1756, 2937–3530 and 4356–4458.
