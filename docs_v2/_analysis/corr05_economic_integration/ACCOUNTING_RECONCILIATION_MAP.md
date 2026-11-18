# Accounting Reconciliation Map

Every unique fill, fee, capital flow and valuation delta maps to one action owner. Account owns
observed exchange balances and transfers; Inventory owns actual held quantities/exposure;
Accounting owns attributed records and reporting buckets. None may rewrite another owner's state.

| Bucket | Contents | Excludes |
|---|---|---|
| `STRATEGY` | original route fills/fees and route-owned cashflows | Recovery, Rebalance, Bridge, infra cost |
| `RECOVERY` | exposure-exit actions after Recovery entry | original route and capital relocation |
| `REBALANCE` | deliberate inventory rebalance | Recovery and Bridge |
| `BRIDGE/RELOCATION` | transfer/conversion/relocation actions | OWA strategy execution |
| `INFRA_COST` | recurring/period infrastructure expense | per-order execution charges |
| `INVENTORY_MTM` | valuation movement of held inventory | duplicate realized fill cashflows |

## Non-trade balance-change handling

| Observation | Account | Inventory | Accounting |
|---|---|---|---|
| unique actual fill and fee | records observed order/fill/balance truth | applies actual asset deltas once | attributes fill/fee once to the owning action bucket |
| deposit or withdrawal | applies the proven external balance event | reflects the proven held-quantity change without calling it a fill | records a provenance-linked capital flow outside trading PnL; no new canonical bucket name is declared here |
| external transfer/relocation | applies the proven transfer endpoints when observed | reflects the proven location/quantity state | records capital movement or `BRIDGE/RELOCATION` attribution, never strategy profit |
| mark-to-market price change | does not fabricate a balance event | does not change held quantity | updates `INVENTORY_MTM` under the declared valuation convention |

Every path requires stable source identity, provenance, deduplication and reconciliation against
observed account truth. Unknown or conflicting balance changes remain unresolved; they are not
backfilled as trades or PnL.

QF-106 and QF-108 must reconcile through this one-disjoint-total map. Any broad `StrategyPnL`
presentation is an aggregation of named buckets, not a second ledger. `EconomicPnL` subtracts
InfraCost once. Fill identity and accounting-entry identity enforce exact-once attribution. The
precise serialized Accounting-record schema remains Data-owned and is not invented here.
