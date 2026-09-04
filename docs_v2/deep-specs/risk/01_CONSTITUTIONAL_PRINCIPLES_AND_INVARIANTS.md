# Constitutional Principles and Invariants

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Governing order

`Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity` is an ordering constraint for scheduling and authorization. The optimizer solves `max EV(a)` only for `a ∈ A_safe`; hard failures remove actions from the set.

System work is scheduled in this exact order: protect existing exposure; cancel unsafe resting orders; reconcile unknown state; recover unwanted inventory; complete a safe existing route; rebalance; take a new opportunity.

Risk layers are `GLOBAL RISK → CAPITAL / INVENTORY RISK → ROUTE RISK → LEG RISK → ORDER RISK`. Upstream limits may tighten or block; no layer grants a bypass to a downstream hard rule. Global PnL cannot relax leg or order safety.

## Rule classes

A hard invariant cannot be bypassed by edge, realized PnL, client profile, operator preference, strategy or optimizer. A calibrated policy fixes the rule structure but learns/version-controls its value. For example, `No Trade On Stale Book` is hard while `stale_age_max` is calibrated.

## Thirty canonical invariants

The exact names are:

1. `INV-001 — No Trade Without Valid Market State`
2. `INV-002 — No Trade On Stale Book`
3. `INV-003 — Route Freshness = Worst Leg Freshness`
4. `INV-004 — No Unknown Metadata`
5. `INV-005 — Fees Must Be Known`
6. `INV-006 — Exchange Precision Is Mandatory`
7. `INV-007 — No Negative Available Balance`
8. `INV-008 — Unknown Capital Is Reserved Capital`
9. `INV-009 — No Double Spending`
10. `INV-010 — Reservations Before Orders`
11. `INV-011 — Shared Depth Cannot Be Double Counted`
12. `INV-012 — Actual Fill Beats Expected Fill`
13. `INV-013 — Next Leg Uses Actual Previous Fill`
14. `INV-014 — No Blind Retry`
15. `INV-015 — Cancel Sent ≠ Canceled`
16. `INV-016 — Partial Fill Creates Real Exposure`
17. `INV-017 — Existing Exposure Has Priority`
18. `INV-018 — Recovery May Be Negative EV`
19. `INV-019 — Recovery Is Not Unlimited`
20. `INV-020 — Sunk Costs Are Sunk`
21. `INV-021 — No Averaging Down By Default`
22. `INV-022 — No Martingale`
23. `INV-023 — No New Risk In RECOVERY_ONLY`
24. `INV-024 — No New Risk In HALTED`
25. `INV-025 — No Trading While Account State Is Unreconciled`
26. `INV-026 — Clock Must Be Healthy`
27. `INV-027 — Required Feeds Must Be Healthy`
28. `INV-028 — Trading Requires InfraHealth == ACCEPTABLE`
29. `INV-029 — Slow Compute Can Become a Risk Event`
30. `INV-030 — Recorder Must Never Block Execution`

No item is superseded or destinationless. Exact inputs, actions, reason families, tests, source ranges and cross-domain owners are in the analysis catalog.

## Core consequences

- Exchange truth beats planned/model truth; unique actual fills determine exposure.
- Existing exposure beats new alpha; uncertain capacity stays locked.
- Hard rules beat EV; no optimizer resurrects a rejected route.
- Uncertainty is risk; increased uncertainty reduces capability.
- Every risk increase is explicit and observable.
- Failure moves toward risk reduction.

Source: SRC-005 lines 91–1032 and 4686–5241.
