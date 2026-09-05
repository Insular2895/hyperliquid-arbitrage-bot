# Inventory State and Flow Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| State | Producer | Consumer | Source truth | Formula/ref | Time/version |
|---|---|---|---|---|---|
| Actual balance | Account reducer + reconciliation | QF-073, Risk, Inventory | Exchange-observed fills/balance truth | Account contract | account version / event time |
| Reserved balance | Execution reservation reducer | QF-073, allocator | Unresolved canonical reservations | ReservationState | reservation + account version |
| Available balance | Derived state | Sizer/allocator/Risk | Actual minus reserved | QF-073 | same coherent snapshot |
| Current inventory | Inventory reducer | Terminal/Sizer/Risk/accounting | Actual fill asset deltas | Fill transition | inventory version |
| Target | Config/classification policy | penalty/terminal | Versioned calibrated policy | QF-064 input | config version/effective time |
| Soft deviation | Inventory economics | Sizer/allocator | current/target/band | QF-064/065 | snapshot + formula version |
| Hard deviation | Risk | permission | future inventory + hard bounds | QF-066 | RiskSnapshot/config version |
| NetFlow | Rolling fill-derived reducer | Risk/Sizer | actual fill deltas | QF-067 | window + cutoff + version |
| Pending transit | Execution/Inventory | Recovery/Risk | actual partial fills | Execution state | order/route/inventory version |
| Dust | Inventory/Execution | Recovery/Rebalance | residual actual quantity | calibrated tolerance | precision/config version |
| Recovery exposure | Recovery state machine | Risk/Execution/accounting | actual unwanted exposure | QF-079/080 interface | recovery/inventory version |
| MTM | Accounting | reporting/Risk | inventory + point-in-time numeraire marks | QF-107 | valuation timestamp/version |
| Exit capacity | Market/route interface | Terminal/Bridge/Sizer | executable current path state | QF-016/068 | book/route/Atlas version |

All consumers use one coherent immutable snapshot. Plans and forecasts do not overwrite actual state.
