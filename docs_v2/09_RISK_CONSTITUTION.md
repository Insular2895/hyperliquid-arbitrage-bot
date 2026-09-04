# 09 — Risk Constitution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

The Risk Constitution defines which actions the bot may take when market, account, execution, model, infrastructure or configuration state is imperfect. It is an authorization boundary, not a profit predictor. It protects capital, preserves state consistency, bounds recovery, and makes every material restriction observable and replayable.

The engine may optimize only inside the safe action set:

```text
max_a EV(a)
subject to a ∈ A_safe
```

A hard-forbidden action is absent from `A_safe`; it is not rescued by attaching a large negative penalty to it.

## 2. Authority

SRC-005 Dossier 3/6 is the closure authority for constitutional principles, invariants, gates, action permissions, kill semantics and risk policy. SRC-005 Dossier 4/6 is authoritative for frozen data fields. SRC-004 owns formulas and execution mechanics; SRC-006 owns validation and deployment acceptance. Completed V2 Participant, Simulator, Execution and Infrastructure documents supply their owned outputs without overriding Risk.

If authorities conflict, the narrower closure authority wins. Current exchange/API facts remain external revalidation items. Quantitative limits without evidence remain calibrated or open; this document does not invent them.

## 3. Constitutional priority

```text
Safety
>
StateConsistency
>
ExistingExposure
>
RiskLimits
>
ExpectedPnL
>
Opportunity
```

A profitable new opportunity never delays reconciliation, protection of real exposure, safe cancel, bounded recovery, or a hard limit. Global profit cannot relax leg or order safety.

## 4. Hard invariant vs calibrated policy

| Class | Meaning | Override permitted? | Example |
|---|---|---|---|
| `HARD INVARIANT` | Structural rule defining the safe set. | No edge, PnL, profile, optimizer or operator override. | No new risk on invalid/stale required market state. |
| `CALIBRATED POLICY` | Structure is mandatory; value/window/bound comes from evidence. | Only versioned change inside validated bounds. | Exact stale threshold. |

The stale-book prohibition is hard; `stale_age_max` is calibrated. A client may tighten a calibrated bound but cannot remove the rule.

## 5. System action priority

The exact scheduler priority is:

1. `PROTECT EXISTING EXPOSURE`
2. `CANCEL UNSAFE RESTING ORDERS`
3. `RECONCILE UNKNOWN STATE`
4. `RECOVER UNWANTED INVENTORY`
5. `COMPLETE SAFE EXISTING ROUTE`
6. `REBALANCE`
7. `TAKE NEW OPPORTUNITY`

Expected profit never reorders these classes. Scarce API, capital and compute capacity is reserved for the higher-priority safety actions first.

## 6. Risk layers

```text
GLOBAL RISK
    ↓
CAPITAL / INVENTORY RISK
    ↓
ROUTE RISK
    ↓
LEG RISK
    ↓
ORDER RISK
```

A higher layer may reduce or block a lower layer. It may never authorize the lower layer to violate its own hard rule. The layers own distinct budgets for capital, market/asset/strategy exposure, route loss, leg continuation and order protection.

## 7. Invariant catalog summary

SRC-005 contains exactly `INV-001` through `INV-030`; all 30 are documented without gaps in [RISK_INVARIANT_CATALOG](_analysis/pass05_risk/RISK_INVARIANT_CATALOG.md). They cover market validity and freshness, metadata/fees/precision, balances/reservations/shared depth, exchange truth and partial fills, bounded recovery, state modes, account reconciliation, clock/feed/infrastructure health, compute lag and recorder isolation.

Each invariant is structural and hard. Some compare against calibrated values, but calibration changes only the value, never the invariant's existence or fail-safe direction.

## 8. Risk evaluation pipeline

The canonical order from SRC-005 section 202 is:

```text
1  SYSTEM HEALTH
2  DATA VALIDITY
3  ACCOUNT CONSISTENCY
4  RESOURCE AVAILABILITY
5  HARD INVENTORY
6  MARKET / IMPACT
7  MODEL SUPPORT / OOD
8  EXECUTION FORECAST
9  TAIL RISK
10 SOFT INVENTORY / PORTFOLIO
11 EV
12 FINAL SIZE
13 PRE-SEND REVALIDATION
```

Cheap hard checks form the fast-reject path; stale, corrupt, unknown or unreconciled inputs must not trigger large Monte Carlo or portfolio optimization. `RiskGate` is deterministic, allocation-light, I/O-free and consumes immutable in-memory snapshots only.

## 9. System/market/account eligibility

New risk requires healthy-enough clock, mandatory feeds and infrastructure; valid sequenced books for every route leg; known current metadata, fee and precision rules; reconciled account/order/fill/balance state; and available capital, reservation and API capacity. Unknown capacity remains reserved. A sequence gap invalidates the affected state until snapshot/resync; the live engine never guesses a missing book event.

`Age_book = Now - LastValidUpdate` and `Age_route = max(Age_leg)`. The rule is hard; clock choice, thresholds and windows are calibrated. A route is never fresher than its oldest required leg.

## 10. Market risk gates

The minimum market gate set is `FreshnessGate`, `SpreadGate`, `LiquidityGate`, `ImpactGate`, `VolumeParticipationGate`, `JumpGate` and `VolatilityGate`. The gates consume authoritative Formula Book outputs and versioned thresholds:

- spread must remain inside the supported economic/market bound;
- executable depth must support the proposed quantity without double use;
- depth and recent-volume participation remain within validated limits;
- mechanical impact and protected prices must be acceptable;
- realized volatility and robust jump state must be supported;
- inconsistent cross-market state or an extreme unsupported edge increases suspicion, triggers data/metadata checks, lowers confidence and may reject.

Low liquidity cannot be repaired merely by a faster VPS. Opportunity magnitude is not evidence of correctness.

## 11. Model/OOD risk

Model-dependent action requires supported market, regime, feature schema, horizon and size; current features; a valid artifact; adequate confidence; acceptable OOD distance and disagreement; and a validated conservative fallback when used. Hard OOD rejects the dependent action. Soft OOD may reduce size only if the reduced size itself falls inside support. Size cannot purchase model confidence.

Survival, expected arrival edge, probability above threshold, maker toxicity, participant drift, cross-market consistency and Simulation confidence feed Risk. Forecasts inform eligibility but never override exchange truth or a hard invariant.

## 12. Execution risk

Maker requires ALO/Post Only semantics, bounded resting exposure/age, live edge and toxicity reassessment, and immediate reevaluation after every fill. Taker requires protected price and maximum slippage/impact. Multi-leg continuation is reassessed from actual fills, fees, rounding and current state; the original route has no privilege.

`UNKNOWN`, `CANCEL_REQUESTED`, partial fills and dust are real exposure states. No blind retry is permitted. ExecutionTransport accepts a real `OrderIntent` only when a current RiskDecision authorizes `ALLOW` or `ALLOW_REDUCED_SIZE` and the plan satisfies the decision's bound.

## 13. Tail risk

Risk evaluates the full execution-outcome distribution, not a point estimate: probability of positive PnL, loss variable, VaR as diagnostic, Expected Shortfall/CVaR, worst single-route loss, recovery tail and portfolio aggregation. Expected EV never overrides an exceeded tail bound.

Mechanical impact, participant response, market move and recovery outcomes must not be double counted. A route's `ExpectedLossContribution` is an input to later portfolio allocation; the optimizer only receives already eligible routes.

## 14. Inventory/capital risk

Actual fills update inventory immediately. New risk must respect hard inventory bounds, capital-at-risk, per-market/per-asset/per-strategy/per-mode limits, shared balance/depth reservations, concentration, net-flow, concurrency, transit-asset age/value, terminal viability and stranded-asset risk.

Soft bands apply penalties or reduce production. Hard bands reject new risk. A known exposure already outside a band may take an explicitly risk-reducing action only when it strictly improves the violation and passes RecoveryRiskPolicy. Route, rebalance and bridge PnL remain separate.

## 15. Economic gate

Economic significance is evaluated only after hard eligibility, execution/tail support and soft portfolio constraints. An economically negative candidate is an economic reject, not a risk reject. A risk-eligible action may still be declined because net expected value after all real costs is inadequate.

Optimizer order is fixed:

```text
Candidate → Hard Risk Eligibility → Optimizer/Sizing → Final Pre-Send Risk Check
```

The optimizer cannot resurrect a rejected candidate.

## 16. RiskSnapshot

One evaluation consumes one immutable `RiskSnapshot`. The frozen Dossier 4 fields are:

```text
risk_snapshot_id
market_versions
account_version
inventory_version
reservation_version
feature_snapshot_ids
model_forecasts
infra_state_version
risk_config_version
created_at
```

These references resolve the semantic contents described by Dossier 3: books, inventory, balances, reservations, model forecasts, infrastructure health and configuration. A new material event creates a new snapshot/version; mixed-time reads are forbidden.

## 17. RiskDecision

The frozen Dossier 4 contract is:

```text
decision_id
risk_snapshot_id
allowed
action
max_allowed_size
required_price_limits
hard_rejects[]
warnings[]
created_at
```

The action enum is exactly `ALLOW`, `ALLOW_REDUCED_SIZE`, `ALLOW_RECOVERY_ONLY`, `REJECT`, `HALT_MARKET`, `HALT_STRATEGY`, `HALT_GLOBAL`. Dossier 3 additionally requires semantics for execution mode, risk-config version and model versions; the frozen schema carries these through snapshot/plan/version references rather than inventing extra `RiskDecision` fields. Reject reasons are closed, versioned and machine-readable.

## 18. TTL/revalidation

`TTL_risk` is calibrated by regime, edge survival and feed fidelity; no fixed universal duration is specified. Expiry requires a new RiskSnapshot and decision before send. Risk is evaluated at all exact checkpoints:

| Point | Moment |
|---|---|
| `T0` | opportunity detected |
| `T1` | before reservation |
| `T2` | immediately before order send |
| `T3` | after each fill |
| `T4` | before every next leg |
| `T5` | during resting maker |

Any material market, account, reservation, model, infrastructure or config change invalidates the previous decision even before nominal TTL expiry.

## 19. Action classification

| Class | Meaning | Examples | Permission rule |
|---|---|---|---|
| `RISK_INCREASING` | Can enlarge exposure or commitment. | New route, larger maker order, buy farther above target. | All applicable gates required. |
| `RISK_NEUTRAL` | Does not intentionally add economic exposure. | Query, reconcile, context-dependent cancel request. | Allowed when operationally safe; classification uses actual context. |
| `RISK_REDUCING` | Strictly improves a known existing exposure. | Protected exit, cancel unsafe maker, sell unwanted transit asset. | May use bounded exception under RecoveryRiskPolicy. |

Classification is based on the post-action exposure, not an endpoint name. Every risk increase must be explicit.

## 20. Fail-closed / risk-reducing exception

If the system cannot prove whether an action is safe or risk increasing, the default is `NO NEW RISK`. Failure must make the system less active.

The only limited exception is an action that reduces a known existing exposure. It must still have current executable state, price protection, explicit reservations, bounded loss/time/attempts, and RecoveryRiskPolicy authorization. This is not a general fail-open mechanism.

## 21. Kill switches

The exact minimum scope taxonomy is `GLOBAL_KILL`, `MARKET_KILL`, `ASSET_KILL`, `STRATEGY_KILL`, `EXECUTION_MODE_KILL`, `MODEL_KILL`, `INFRA_KILL`. Scope is dependency-aware and should be the smallest safe one.

Monitored switch families include execution-quality divergence, Simulator calibration failure, Participant model drift, fee change and metadata change. `GLOBAL_KILL` stops new risk everywhere, cancels maker, reconciles and permits recovery only by policy. Market/asset kills disable dependent routes while retaining permitted risk-reducing exits. Reset requires the triggering condition cleared, state reconciled, health revalidated and any required manual acknowledgement; no kill reset directly implies trading readiness.

## 22. Dependency-aware degradation

Every strategy/capability declares mandatory dependencies, optional dependencies and validated fallbacks. Failure of a mandatory model or feed disables only dependent capabilities when narrower safe isolation is possible. Fallback must be at least as conservative as the failed capability.

Infrastructure levels are `HEALTHY`, `DEGRADED`, `UNSAFE`, `CRITICAL`: progressively reduced size/higher economic threshold, then no new risk, then cancel/recover/halt as applicable. Exact transitions are calibrated. Missing support never means “ignore the feature and trade unchanged.”

## 23. Drawdown/loss controls

The state architecture is `NORMAL`, `CAUTION`, `RISK_OFF`, `HALT`; exact thresholds and hysteresis are calibrated. Multiple session/daily and short/long windows, loss velocity, consecutive failures and execution/recovery quality distinguish strategy variance from system degradation.

`CAUTION` tightens or reduces. `RISK_OFF` forbids new risk while allowing safety actions. `HALT` applies the relevant kill and escalation. Profit or drawdown state never relaxes another hard rule, triggers martingale, or authorizes averaging down.

## 24. Recovery Risk policy

PASS 04 owns the Recovery state machine; Risk owns permission. Recovery may have negative EV because protecting existing exposure outranks profit. It is never unlimited: attempt, elapsed-time, loss/tail, price, inventory and capacity bounds are versioned; actual exposure must be known; each new recovery order is reserved and protected.

After each fill/failure/state change, reevaluate. Exhaustion escalates to the appropriate halt/manual path. Sunk cost never widens future permission, and recovery cannot hide leverage or relabel route loss.

## 25. Capital scaling restrictions

More capital does not automatically change impact, depth/volume participation, OOD, tail, inventory, execution or validated-size limits. Auto-compounding can raise available capital but `Q_validated` remains the capacity ceiling.

Scaling requires sufficient observations plus Simulator confidence, micro-live evidence, tail validation, market capacity, recovery quality and infrastructure stability. Operational capital bands derive from evidence rather than fixed euro ladders. A more expensive server is not intrinsically safer; Infrastructure ROI remains PASS 01 authority.

## 26. Config/parameter governance

Constitutional parameters cannot be disabled. Tunables carry name, unit, scope, owner, value/range, provenance, version, effective time, update/rollback process, hot-reload policy, plan-pinning behavior and validation evidence.

Allowed provenance classes are `CALIBRATED`, `LEARNED`, `EXCHANGE_RULE`, `SAFETY_DEFAULT`, `USER_TIGHTENABLE`, plus explicit `OPEN`; constitutional rules remain `CONSTITUTIONAL`. Runtime changes are atomic, logged and versioned. An `ExecutionPlan` pins its risk configuration between legs; emergency hard stops may still interrupt it.

## 27. Client/operator restrictions

A client may tighten limits beneath validated maxima. A client or operator may reduce limits and trigger market, strategy or global kills. Neither can disable freshness, UNKNOWN handling, reconciliation, precision, reservations, hard inventory or any other hard invariant.

Unsupported/inconsistent config prevents `READY`. Examples include negative limits, probabilities outside `[0,1]`, soft bounds outside hard bounds, disabled stale checks or unlimited impact. There is no super-admin bypass of the Constitution.

## 28. Audit / replay / reject dataset

Every decision records snapshot/config/model provenance, calculated metrics, gate results, reason codes and action. Same ordered inputs, formula/config/model versions and deterministic state must reproduce the same decision trace.

Rejected opportunities are retained with Opportunity, RiskSnapshot, RejectReasons and later counterfactual outcome. Calibration uses both accepted and rejected cases to measure false positives, false negatives and opportunity cost. Threshold optimization balances NetPnL, drawdown, Expected Shortfall and recovery frequency; backtest cannot override persistent live evidence, and a handful of live samples cannot establish drift.

## 29. Validation / DoD

Each invariant receives unit, property and fault-injection tests as applicable. Mandatory acceptance includes stale/unknown/hard-inventory/CVaR/OOD/infra-unsafe tests, deterministic identical-input decisions and evaluation latency distributions at P50/P95/P99/P99.9. No universal performance threshold is invented.

Risk activation is capability-gated. Binary support is not live permission. Model/config/schema/dataset/capital/risk evidence, micro-live behavior, kill drills and regression reports are versioned before promotion or scaling.

## 30. Failure philosophy

```text
Failure → RiskReduction
```

The engine handles stopped, lying, late, duplicate, OOD and stale dependencies explicitly. It invalidates and resynchronizes bad state, latches appropriate kills, preserves uncertain reservations, and escalates when truth cannot be reconstructed. Panics, numerical invalidity, division by zero, memory/state corruption, secret/signer failure and recorder/storage pressure never silently produce permission.

Startup is `BOOT → CONFIG VALIDATE → CLOCK → FEEDS → BOOKS → ACCOUNT → OPEN ORDERS → FILLS → RECONCILIATION → RISK HEALTH → READY`. Shutdown is `STOP NEW RISK → HANDLE RESTING ORDERS → RESOLVE ACTIVE EXECUTIONS → PERSIST → STOP`. Automatic process restart is never automatic re-trading.

## 31. Cross-domain contracts

| Producer | Risk consumes | Risk guarantees downstream |
|---|---|---|
| Data/Clock/Account/Inventory | Versioned immutable states, sequence/freshness, balances/reservations | Eligibility and explicit invalidity; no state mutation |
| Participant models | Survival, arrival edge, liquidity, toxicity, OOD/disagreement/drift | Dependency-scoped permission; never blind trust |
| Simulator | Execution outcome distribution, confidence, calibration health | Tail/simulation gate and supported size |
| Execution | Actual fills, order/reconciliation/recovery states | Current RiskDecision and bounded continuation/recovery |
| Infrastructure | InfraState, latency/clock/feed/recorder health | Degrade/kill action; no provider purchase decision |
| Formula Book | QF outputs and units | No formula redefinition |
| Validation | CapabilityManifest/ValidatedCapability and evidence | Enable only validated capability |
| Operations | Incidents, acknowledgement and telemetry | Machine-readable decisions, kills and audit trail |

Exact schema definitions remain Data Contracts authority; exact formula expressions remain Formula Book authority; inventory/portfolio ownership remains their future closure passes.

## 32. Deep-spec links

- [Risk deep-spec index](deep-specs/risk/README.md)
- [Constitutional Principles and Invariants](deep-specs/risk/01_CONSTITUTIONAL_PRINCIPLES_AND_INVARIANTS.md)
- [Market, Data and Account Eligibility](deep-specs/risk/02_MARKET_DATA_AND_ACCOUNT_ELIGIBILITY_GATES.md)
- [Market, Liquidity, Volatility and Impact Risk](deep-specs/risk/03_MARKET_LIQUIDITY_VOLATILITY_AND_IMPACT_RISK.md)
- [Model, Execution and Tail Risk](deep-specs/risk/04_MODEL_EXECUTION_AND_TAIL_RISK.md)
- [Inventory, Capital, Portfolio and Sizing](deep-specs/risk/05_INVENTORY_CAPITAL_PORTFOLIO_AND_SIZING_GATES.md)
- [RiskSnapshot, RiskDecision, TTL and Revalidation](deep-specs/risk/06_RISK_SNAPSHOT_DECISION_TTL_AND_REVALIDATION.md)
- [Kill Switches and Degraded Modes](deep-specs/risk/07_KILL_SWITCHES_DEPENDENCIES_AND_DEGRADED_MODES.md)
- [Recovery Risk and Action Classification](deep-specs/risk/08_RECOVERY_RISK_AND_ACTION_CLASSIFICATION.md)
- [Parameter Governance and Client Bounds](deep-specs/risk/09_CONFIG_PARAMETER_GOVERNANCE_AND_CLIENT_BOUNDS.md)
- [Replay, Audit, Reject Dataset and Calibration](deep-specs/risk/10_REPLAY_AUDIT_REJECT_DATASET_AND_CALIBRATION.md)
- [Failures, Tests and Definition of Done](deep-specs/risk/11_FAILURE_MODES_TESTS_AND_DEFINITION_OF_DONE.md)

Traceability and source locators are in `docs_v2/_analysis/pass05_risk/`.
