# Inventory, Capital, Portfolio and Sizing Gates

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Inventory regions

Inventory targets, soft and hard bands are asset/scoped and versioned. Inside soft bands, no additional restriction is required. Outside soft bands, Risk penalizes or reduces routes that worsen the deviation and favors improvement. A proposed new-risk state outside `[HardMin, HardMax]` is a hard reject.

The only hard-band exception is an explicitly `RISK_REDUCING` action that strictly improves a known pre-existing violation and passes RecoveryRiskPolicy. Net flow over multiple horizons acts before hard breach. Concentration, transit-asset maximum age/value, stranded-asset cost/idle time and terminal viability are first-class gates.

## Capital and reservations

`CapitalAtRisk` includes open orders, unresolved orders, intermediate exposure and recovery commitments. Available capital is actual balance minus all reservations and unresolved claims; unknown capital remains reserved. Every ExecutionPlan reserves capital, book and relevant risk/API budgets before send. No release occurs merely because a network result is uncertain.

Per-market, per-asset, per-strategy and maker/taker/execution-mode limits are independent. Concurrent execution and correlated/shared-resource routes consume aggregated budgets. This prevents leverage-like exposure through duplicate commitments.

## Portfolio subordination

The Portfolio Optimizer receives only risk-eligible routes. Shared depth/balance and route-dependency constraints are applied once. It may choose among safe actions but cannot buy permission with portfolio EV. Expected-loss contributions and portfolio tail constraints remain inputs; exact allocation belongs to PASS 07.

## Sizing

For each candidate size, evaluate EV, Expected Shortfall, probability positive, confidence, impact, execution distribution and inventory/capital effects. The chosen size is bounded by the intersection of capital, executable liquidity, participation, impact, model support, tail loss, inventory, execution and `Q_validated`. If no positive size satisfies all gates, `q* = 0`.

More capital or realized profit cannot raise validated capacity automatically. Scaling requires data volume, Simulator calibration/confidence, micro-live evidence, tails, recovery quality, market capacity and infrastructure stability. Operational bands are evidence-derived, not fixed currency ladders.

Formula references: `QF-064`–`QF-069`, `QF-073`–`QF-078`, `QF-109`–`QF-110`. Source: SRC-005 lines 1757–2171, 2513–2800, 3071–3179 and 3475–3643.
