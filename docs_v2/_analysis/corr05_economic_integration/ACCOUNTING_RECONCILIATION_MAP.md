# Accounting Reconciliation Map

Every unique fill, fee, transfer and valuation delta maps to one action owner:

| Bucket | Contents | Excludes |
|---|---|---|
| `STRATEGY` | original route fills/fees and route-owned cashflows | Recovery, Rebalance, Bridge, infra cost |
| `RECOVERY` | exposure-exit actions after Recovery entry | original route and capital relocation |
| `REBALANCE` | deliberate inventory rebalance | Recovery and Bridge |
| `BRIDGE/RELOCATION` | transfer/conversion/relocation actions | OWA strategy execution |
| `INFRA_COST` | recurring/period infrastructure expense | per-order execution charges |
| `INVENTORY_MTM` | valuation movement of held inventory | duplicate realized fill cashflows |

QF-106 and QF-108 must reconcile through this one-disjoint-total map. Any broad `StrategyPnL` presentation is an aggregation of named buckets, not a second ledger. `EconomicPnL` subtracts InfraCost once. Fill identity and accounting-entry identity enforce exact-once attribution.
