# QF-106 / QF-108 Accounting Scope Audit

## Source reopened

SRC-004 lines 8891–8984 state QF-106 with `ExecutionPnL + InventoryMTM + RebalancePnL + BridgePnL - InfrastructureCost`. Lines 9049–9147 state QF-108 `StrategyPnL = ΣRoutePnL + ΣRecoveryPnL + ΣRebalancePnL + InventoryPnL`, then `EconomicPnL = StrategyPnL - InfraCost`. Neither source equation is changed.

## Closure

| Question | Answer |
|---|---|
| What does QF-106 close? | the general global EconomicPnL period, including every applicable disjoint bucket |
| What does QF-108 StrategyPnL represent? | the source-defined strategy/accounting subtotal: Route + Recovery + Rebalance + Inventory |
| Where does Bridge/Relocation belong? | a separate disjoint `BRIDGE/RELOCATION` bucket |
| Which view owns global close? | QF-106 |
| When is QF-108's compact economic equality usable? | bridge-free scope (`BridgePnL=0`) |
| Can Bridge disappear? | NO |
| Can Bridge appear twice? | NO |

For nonzero Bridge periods, QF-108's compact equality is not used as the general close; QF-106 is mandatory. Mapping `ExecutionPnL` to the disjoint Strategy/Recovery execution-owned cashflows remains an accounting attribution contract, not a new formula. Any missing, overlapping or currency/period-mismatched bucket is invalid, not silently zero.

Result: `RESOLVED BY EXPLICIT CONSERVATIVE SCOPE`; equation changes `0`; new QF `0`.
