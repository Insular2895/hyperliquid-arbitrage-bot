# Bridge vs OWA vs Rebalance vs Recovery

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Test | OWA | Bridge/Relocation | Rebalance | Recovery |
|---|---|---|---|---|
| Initiating state | Safe new opportunity | Safe intentional move decision | Inventory drift/capacity imbalance | Existing unwanted/unsafe exposure |
| Purpose | Beat valid direct comparator now | Improve future capital utility | Restore target/band capacity | Minimize loss/risk from exposure |
| Direct A->B comparator required | Yes | No | No | No |
| STAY comparator | Not defining test | Mandatory | Wait/natural reversal mandatory | Only if safe; exposure priority controls |
| Immediate EV may be negative | No normal exemption | Yes, if future relocation value passes | Yes, for supported restoration | Yes, safety can dominate |
| Risk priority | New opportunity | Below Recovery/Rebalance priority | Above new opportunity | Above all ordinary optimization |
| Accounting | Route/Strategy PnL | Bridge/Relocation PnL | Rebalance PnL | Recovery PnL/Loss |
| Partial failure | Recovery if unwanted exposure | Recovery if unwanted exposure | Recovery if unsafe/unresolved | Continue Recovery state machine |

Classification tests must cover `A -> X -> B` with and without a direct comparator, inventory-normalization trades, and trades caused by partial/failed execution.
