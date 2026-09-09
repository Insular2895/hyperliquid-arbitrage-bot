# 04 — Parameter Search

STATUS: FUTURE SPECIFIED / NOT ACTIVE

Parameter search compares bounded versions of a declared `StrategySpec`; it cannot search away constitutional constraints.

## Search contract

Before execution freeze: hypothesis; parameter names/types/units; defensible domains; locked Risk and safety values; objective vector; guardrails; Dataset and temporal splits; evaluation budget; seed policy; stopping rule; multiplicity family; invalid-run handling; and final holdout policy.

Permitted methods progress only as justified: manual baselines, grid, random, Latin hypercube, Bayesian optimization, then evolutionary methods. Added sophistication requires evidence that the prior method cannot efficiently characterize the declared space. Search compute is bounded and auditable.

Risk limits, kill-switch conditions, reconciliation rules, freshness requirements, authorization states, capital ceilings and protected execution constraints are not search parameters. Objective functions cannot reward bypassing abstention, missing-data or failure semantics.

Candidate dimensions can include edge/age thresholds, q inside already permitted evidence bounds, depth participation, volatility/regime filters, route/market inclusion, priority policy only where supported, and execution mode only after its separate capability gate. Search never raises `Q_validated`; inventory settings remain inside higher-level Risk permission.

The search ranks robust regions, not the single highest historical PnL. Outputs include candidate set, all attempted points, failures/censoring, score components, uncertainty, sensitivity/stability surfaces, boundary behavior, compute cost and selection rationale. Duplicate trials and adaptive choices remain visible.

Objectives consume canonical net economics—fees, executable book walk/slippage, priority, Recovery, infrastructure, inventory/capital opportunity effects where owned—exactly once. Gross edge and a new research accounting formula are insufficient.

Search, Monte Carlo and Simulator are distinct:

- search selects candidate configurations;
- the canonical Simulator evaluates economic/execution scenarios;
- Monte Carlo repeats coherent Simulator scenarios to characterize uncertainty.

No search result is promoted directly. It proceeds through untouched temporal OOS, walk-forward, robustness, Shadow and separately authorized Micro-live evidence.
