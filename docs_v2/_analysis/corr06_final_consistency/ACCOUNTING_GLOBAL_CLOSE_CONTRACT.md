# Accounting Global-Close Contract

Every actual fill, fee, priority charge, transfer and valuation delta has one stable accounting-entry identity and one owner before aggregation.

| Bucket | Includes | Never includes |
|---|---|---|
| Strategy/Execution | original-route cashflows and normal exchange fees | Recovery, Bridge, InfraCost |
| Recovery | post-entry exposure resolution | original route or a second QF-080 charge |
| Rebalance | intentional inventory rebalancing | Bridge/Recovery |
| Bridge/Relocation | intentional capital-location move | OWA route alpha or Strategy subtotal |
| InventoryMTM | external-flow-adjusted valuation | duplicate fill cashflow |
| InfraCost | recurring/profile/feed cost, including owned read-auction spend | write-priority execution charges |

QF-106 closes globally. QF-108 is a bridge-free subtotal view. Write-priority charges are scenario action costs once; gossip/read auction cost is infrastructure once. Forecast penalties never enter realized ledgers. Tests use zero-Bridge and nonzero-Bridge periods and fail on omission or duplication.
