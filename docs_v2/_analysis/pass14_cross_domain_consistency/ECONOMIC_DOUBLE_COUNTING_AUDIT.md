# Economic Double-Counting Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Economic item | First-entry owner | Forbidden repeat | Resolution state |
|---|---|---|---|
| spread/depth | QF-009/010 walk | subtract same slippage after QF-016 | CLOSED |
| fee/rebate | QF-014/015 through QF-016/account delta | route-level second fee | CLOSED; debit asset external-gated |
| rounding/minimum | each exact leg | synthetic route-end adjustment | CLOSED |
| partial/failure/recovery scenario | QF-057 scenario PnL | generic deduction after execution EV | CLOSED |
| MT adverse/recovery cost | QF-058 declared component | inside `EV_leg2` and again outside | INCLUSION FLAG REQUIRED |
| soft inventory penalty | QF-065/QF-063 decision objective | realized Inventory PnL | CLOSED |
| hard inventory breach | QF-066 gate | finite soft penalty | CLOSED |
| executable exit | QF-068 | repeat depth/fee/slippage | CLOSED |
| idle capital | QF-105, optionally QF-069 | repeat for same capital/time | CLOSED |
| Bridge conversion | QF-070 net end value | per-leg costs again | CLOSED |
| ExpectedExitCost relocation | explicit QF-072 term | embedded in BridgeCost plus explicit | INCLUSION FLAG REQUIRED |
| Recovery loss | QF-080 from recovery-start state | pre-recovery sunk loss | CLOSED |
| trading costs | QF-090 accounting | net gross plus second subtraction | CLOSED |
| infrastructure cost | QF-090/106/108 close | embed per route and subtract globally | CLOSED |
| model latency loss | QF-101 experiment attribution | already in with/without delta plus explicit | ATTRIBUTION REQUIRED |
| operational model cost | QF-101 | duplicate infrastructure cost center | COST-CENTER LINK REQUIRED |
| external deposits/withdrawals | QF-107 `ExternalFlow` exclusion | Inventory/Strategy PnL | CLOSED |
| Inventory MTM/PnL | QF-107→108 mapping | both labels for identical change | RECONCILIATION MAPPING REQUIRED |

Conditional rows are not unresolved ownership: their serialized record must declare `cost_component_id`, scope, period, numeraire, predicted/counterfactual/realized class and `included_in`. Unowned economic components: **0**. Duplicate-authorized components: **0**.
