# Capital Action Taxonomy

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

These are economic classifications, not a new runtime enum.

`NEW_STRATEGY` is the generic economic family for a new Risk-eligible alpha action; OWA and Triangle are concrete members. The label is documentary and does not invent a final code enum.

| Action | Purpose | Comparator | Return structure | Risk priority | Accounting | Negative immediate EV? | Reservation | Terminal objective | Formula refs |
|---|---|---|---|---|---|---:|---|---|---|
| NEW_STRATEGY family | Open new normal strategy exposure | strategy-specific baseline | positive eligible RAEV | Lowest ordinary action | Strategy/Route | No normal exemption | balance/book/Risk | strategy-valid terminal | QF-057/QF-063 |
| OWA | Better current A-to-B conversion | Direct A->B vs A->X->B | Conversion/Execution EV | New opportunity | Route/Strategy | No normal exemption | balance/book/Risk | Valid B | QF-016–020, 057, 063 |
| Triangle | Return to starting asset | start vs final same asset | cycle PnL | New opportunity | Route/Strategy | No | balance/book/Risk | Starting asset | QF-021–023 |
| Bridge | Move capital toward future-useful destination | candidate path and STAY | immediate cost + future utility | Below safety/Recovery | Bridge | Yes if QF-072 positive | balance/book/Risk | useful, exit-capable destination | QF-068, 070–072 |
| Capital Relocation | Decision layer selecting move or stay | `EV_destination` vs `EV_stay` | net future value | Below safety/Recovery | Bridge/Relocation | Yes | same canonical system | higher supported utility | QF-072 |
| Rebalance | Restore bands/capacity | wait/natural reversal vs act now | risk/capacity restoration | Above new opportunity | Rebalance | Yes | shared, Risk-prioritized | closer/safer inventory | QF-064–069 interface |
| Recovery | Reduce existing unwanted exposure | allowed recovery exits | minimize expected Recovery loss | Constitutional high priority | Recovery | Yes | priority resources | safest supported exposure state | QF-079–080 |
| Hold/Stay | Preserve current capital location | all moves | no transaction; continued utility/cost | Default comparator | none until state changes | N/A | existing reservations only | current state | QF-072/QF-105 |

Bridge vs Rebalance vs Recovery is determined by purpose and initiating state, not by the physical conversion path.
