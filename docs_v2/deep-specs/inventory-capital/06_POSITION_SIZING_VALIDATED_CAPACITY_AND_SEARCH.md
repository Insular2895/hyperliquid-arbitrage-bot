# 06 — Position Sizing, Validated Capacity and Search

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Definitions

Position Sizing chooses total exposure for an already viable, Risk-eligible opportunity. QF-075 maximizes Risk-Adjusted EV over a constrained quantity region. It is nonlinear: NetConvert/book levels, edge, impact, completion, P+, CVaR, confidence, inventory and Recovery all vary with quantity.

QF-027 Maximum Profitable Size is an edge/profitability boundary. QF-076 Validated Capacity, `Q_validated`, is the largest quantity for which every required gate is true. They are not interchangeable.

## Feasible region

The selected quantity must not exceed available/reservable balance (QF-073), available book capacity (QF-074), `Q_validated` (QF-076), Risk maximum, future inventory capacity or supported strategy/execution capability. It must also satisfy impact/participation, completion, P+, CVaR/ES, SimulationConfidence, OOD and minimum economic requirements. Risk's max is a ceiling, never the requested size.

`Q_validated` is bound to route, state, TT/MT/TTT/MTT mode, regime, liquidity, model support, inventory and Risk. Maker and taker capacities differ. It can increase or decrease. Available capital growth or profit compounding alone never changes it.

## Search

QF-077 locks:

1. evaluate a candidate grid;
2. identify the best feasible region;
3. refine locally between neighboring sizes.

This avoids assuming differentiability or monotonic PnL across discrete book/rounding boundaries. Grid/refinement choices are calibrated. Validate small cases against exhaustive search. If no candidate is valid, return `q*=0`.

## Scaling

The 40–50 EUR example is `MICRO_LIVE_PROBE`, not normal size. Promotion uses bounded steps with enough observations, next-band Simulator support, impact/tail/inventory stability and no critical incident. Poor fill/slippage/tail/confidence evidence demotes capacity. Horizontal use of independent opportunities generally precedes forced vertical size, but shared resources must prove independence.

## Evidence records

Persist the entire candidate curve, not only the winner: quantity, executable conversion, edge/EV/RAEV, fill/completion, impact/participation, P+, CVaR, confidence/OOD, future inventory, resource demand, gate results and structured rejection reason.

Sources: SRC-003 §§39–47; SRC-004 QF-026–027/QF-040–042/QF-056–063/QF-073–077; SRC-005 §§59–61/145–152; SRC-006 §§78–82/138–147/272–277; SRC-007 §§53–60; SRC-008 §§44–48/75.
