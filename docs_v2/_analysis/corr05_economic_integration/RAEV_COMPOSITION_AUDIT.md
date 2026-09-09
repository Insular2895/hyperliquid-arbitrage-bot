# RAEV Composition Audit

QF-063 remains:

`RAEV = EV_execution - InventoryPenalty - StrandedPenalty - ModelUncertaintyPenalty`

The three deductions are external, non-overlapping state/evidence penalties:

- `InventoryPenalty` prices undesirable post-decision inventory deviation;
- `StrandedPenalty` prices expected exit, idle and risk cost of stranded capital;
- `ModelUncertaintyPenalty` prices validated evidence uncertainty under its canonical contract.

Fees, executable slippage/book walk, partial fills, participant response and Recovery execution outcomes already belong inside `Π_exec` and are not subtracted again. ExpectedExitCost is a component of StrandedPenalty when QF-069 is used, so QF-068 is not an additional parallel deduction. QF-105 idle cost likewise remains inside that composition.

Risk hard gates stay gates. Positive RAEV cannot override a Risk rejection, stale/UNKNOWN state, unsupported q or unavailable evidence.
