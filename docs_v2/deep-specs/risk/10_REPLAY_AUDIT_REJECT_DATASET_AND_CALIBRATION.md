# Replay, Audit, Reject Dataset and Calibration

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Observable deterministic decisions

Every gate emits metric, decision and machine-readable reason. Every real trade is attributable to immutable snapshot IDs, risk-config version, model/config/schema versions, formulas and ordered inputs. Given identical `RiskSnapshot`, config and models, Risk produces the same `RiskDecision`.

`DecisionTrace` contains ordered decisions, order intents, state transitions and risk decisions. `RunManifest` binds mode, code/build/config, data, models, schemas/formulas and seed where stochastic work applies. Risk itself remains deterministic.

## Risk replay

Replay reconstructs why an action was allowed, reduced, rejected or halted. It can apply a different versioned risk config to the same point-in-time market/account stream, while preserving causal ordering and no-lookahead, to compare policies such as lower impact or higher probability thresholds.

## Reject dataset

Each rejected opportunity retains references to Opportunity, RiskSnapshot, versioned RejectReasons and later counterfactual outcome. Both accepted and rejected candidates are required to estimate false positives, false negatives, opportunity cost, constraint binding and selection bias. Economic rejects remain distinct from risk rejects.

## Calibration and promotion

Threshold research considers NetPnL, drawdown, Expected Shortfall, recovery frequency, execution quality and opportunity cost. Exploratory objectives do not replace Formula Book authority. Results are segmented by market, regime, size, strategy/mode and support; uncertainty and sample size are explicit.

Backtest cannot overrule persistent micro-live/live contradiction. Conversely, a few adverse trades do not prove drift. Policy/model promotion requires temporal OOS evidence, calibration, runtime, failure/fallback testing, shadow and appropriately bounded micro-live evidence. Champion failure rolls back atomically or disables dependent capability.

Source: SRC-005 lines 3330–3398, 3970–4089 and 4459–4734; Data contracts SRC-005 Dossier 4 sections 86, 93 and 98.
