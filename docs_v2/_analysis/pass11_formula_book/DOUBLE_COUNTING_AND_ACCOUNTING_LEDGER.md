# Double-Counting and Accounting Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| ID | Economic item | First entry / owner | May flow into | Forbidden second entry | Audit disposition |
|---|---|---|---|---|---|
| DC-01 | spread/depth execution effect | QF-009/010 walk | QF-016, routes, EV | separate slippage deduction for same walk | resolved by ownership rule |
| DC-02 | fee/rebate | QF-014/015 applied by QF-016 | net route outputs/account deltas | multiply every route output by `(1-f)` or subtract fee again | resolved |
| DC-03 | rounding/minimum loss | QF-007/008/016 at each leg | subsequent exact leg input | synthetic end-of-route rounding adjustment | resolved |
| DC-04 | partial/failure/recovery outcome | QF-057 scenario PnL | QF-063 EV term | generic partial/recovery deduction after EV | resolved |
| DC-05 | MT adverse/recovery cost | QF-058 | execution-mode comparison | cost inside `EV_leg2` and after integral | conditional: evidence field declares inclusion |
| DC-06 | soft inventory penalty | QF-065 → QF-063 | sizing objective | realized InventoryPnL/MTM ledger | resolved separation |
| DC-07 | hard inventory breach | QF-066 gate | QF-075/076 allow/reject | convert into a finite soft penalty | resolved |
| DC-08 | executable exit cost | QF-068 | QF-069/071/072 as declared | separate depth/fee/slippage deductions from same exit | resolved |
| DC-09 | idle capital cost | QF-105, consumed by QF-069 when used | stranded/relocation analysis | QF-069 plus separate QF-105 for same capital/time | resolved |
| DC-10 | bridge conversion cost | net end value in QF-070 | QF-071/072 | per-leg fee/slippage again | resolved |
| DC-11 | ExpectedExitCost in relocation | explicit QF-072 term | relocation value | also embedded in the evaluated BridgeCost | conditional; inclusion flag mandatory |
| DC-12 | recovery loss | QF-080 | recovery attribution/QF-108 | charge loss incurred before Recovery started | resolved sunk-cost exclusion |
| DC-13 | trading costs | QF-090 | NetPnL/QF-100 | already-net GrossTradingPnL or QF-106 component plus second subtraction | resolved ledger definitions |
| DC-14 | infrastructure cost | QF-090/QF-106/QF-108 global close | EconomicPnL/model comparison | embedded in each RoutePnL and subtracted globally | resolved |
| DC-15 | added model latency loss | QF-101 | ModelValue | included in `PnL_with-PnL_without` and subtracted again | conditional experiment attribution |
| DC-16 | operational model cost | QF-101 | ModelValue | same amount inside InfrastructureCost and OperationalCost without allocation | conditional cost center required |
| DC-17 | external deposits/withdrawals | removed by QF-107 | equity/account reconciliation | treat as InventoryPnL or StrategyPnL | resolved |
| DC-18 | InventoryPnL/MTM | QF-107 attribution into QF-108 | QF-106 global PnL | both InventoryMTM and InventoryPnL for identical change | reconciliation mapping required |

Every economic record carries `cost_component_id`, scope, period, asset/numeraire, predicted/counterfactual/realized class and `included_in` owner. QF-063 is a decision objective; QF-106–108 are accounting identities. These layers may reconcile but cannot reuse unlabeled components.
