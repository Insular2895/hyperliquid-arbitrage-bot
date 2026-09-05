# 09 — Rebalance, Recovery and Capital-Action Boundaries

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Action taxonomy

| Action | Purpose | Normal economic standard | Priority/accounting |
|---|---|---|---|
| OWA | Beat a valid direct A-to-B comparator now | Positive eligible route economics | Strategy/Route PnL |
| Bridge/Relocation | Move capital to higher expected future utility | QF-072 vs STAY, may cost now | Bridge PnL |
| Rebalance | Restore inventory/capacity toward validated bands | Compare waiting vs rebalancing; may cost now | Rebalance PnL |
| Recovery | Reduce existing unwanted/unsafe exposure | QF-079 loss-minimizing/safety objective; may be negative EV | Recovery PnL/Loss |
| Hold/Stay | Preserve current state | Explicit comparator/choice | No transaction PnL |

A triangle returns to its starting asset and remains route-owned; it is not Bridge. Names above are economic categories, not a newly invented runtime enum.

## Rebalance

Rebalance addresses accumulated inventory drift and future capacity exhaustion. Prefer profitable/natural reverse opportunities when safe. A physical or explicitly losing Rebalance is considered only when the expected cost of waiting—missed opportunities, immobilization, directional risk and hard-limit probability—exceeds the supported cost/risk of rebalancing. It never hides inside OWA PnL.

## Recovery

Recovery begins with already-real unwanted exposure caused by partial/failed execution or unsafe state. QF-079 compares allowed exit actions by expected post-action portfolio value / expected Recovery loss in a common numeraire. QF-080 records loss from the Recovery boundary and excludes earlier sunk loss. Execution owns candidate order mechanics and verification; Risk owns permissions.

## Priority and transitions

Existing exposure, cancels, reconciliation and Recovery outrank Rebalance, Bridge and new opportunity. No ordinary Bridge begins during forbidden `UNKNOWN`, unreconciled or dangerous Recovery state. If Bridge partially executes and cannot safely continue, actual exposure is reclassified to Recovery; it is not rolled back conceptually.

Negative immediate EV can be justified for Recovery, risk-reducing Rebalance or future-value Bridge under their own rules. A new Strategy opportunity receives none of these exemptions.

Sources: SRC-003 §§31–36 and rebalancing discussion; SRC-004 QF-079–080; SRC-005 constitutional priority/§§66–74; PASS04 Execution and PASS05 Risk.
