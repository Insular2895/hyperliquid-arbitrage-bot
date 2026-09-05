# 03 — Exit Cost, Stranded Capital and Inventory Economics

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Expected Exit Cost

QF-068 is the locked source structure for `ExpectedExitCost`: current value less best executable exit value. The exit uses authoritative NetConvert/route outputs and includes fees, depth, slippage and rounding without a second manual deduction. It depends on asset, location, quantity, book state, execution mode, route availability and horizon.

## Stranded capital

Capital is stranded when it exists but is inefficient to exit or redeploy. QF-069 combines three separately stored expected components:

- `ExpectedExitCost`;
- `ExpectedIdleCost`;
- `ExpectedRiskCost`.

The structure is calibrated; no permanent arbitrary coefficient is assumed. A terminal with excessive exit cost or idle time can be rejected despite positive route economics.

## Opportunity cost and utility

Opportunity Cost represents supported alternatives forgone while capital is reserved, resting, in Bridge, in Transit, or otherwise unavailable. QF-105 Expected Idle Capital Cost uses the immobilized capital, duration and an empirical OpportunityRate inferred from opportunities the capital could actually have taken. It is not a risk-free rate and never overrides safety.

Capital Utility should use validated opportunity density/capacity, capture probability, future exitability, competition, inventory fit and Risk—not raw route count or a single edge.

## Decision economics versus accounting

| Concept | Decision-time role | Realized-accounting treatment |
|---|---|---|
| Soft Inventory Penalty | Compare safe alternatives | Not cash PnL |
| Stranded Capital Penalty | Price expected exit/idle/risk burden | Record later actual exit, MTM and idle outcome separately |
| Rebalance Value | Future-state preference | Real Rebalance fills create separate PnL |
| Expected Exit Cost | Candidate terminal/relocation cost | Replace with actual exit fills/costs when executed |
| Inventory MTM | Current valuation change | QF-107, excluding external flows |

Fees/slippage already present in actual route results or NetConvert are not deducted again. Expected and realized values carry lineage to route/action, fills, marks, models and versions.

## Calibration

Compare predicted exit cost with executed exits, predicted idle duration with realized capital unavailability, and stranded penalty with later exit/utility outcomes. Persistent error reduces confidence and may shrink Q_validated or terminal eligibility.

Sources: SRC-003 §§18–31/56–63; SRC-004 QF-063/QF-068–069/QF-105–108; SRC-005 §§70–74/Data §§148–155; SRC-007 §§61–68/91–93.
