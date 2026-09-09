# Inventory, Exit and Stranded-Capital Double-Count Audit

| Term | Canonical object | Ownership |
|---|---|---|
| QF-065 InventoryPenalty | preference/risk cost of inventory deviation | external QF-063 state penalty |
| QF-066 hard inventory limit | permission | Risk gate, never a penalty |
| QF-068 ExpectedExitCost | `CurrentValue - BestExecutableExitValue` | component/diagnostic using QF-016 exit costs |
| QF-069 StrandedPenalty | `ExpectedExitCost + ExpectedIdleCost + ExpectedRiskCost` | external QF-063 stranded penalty |
| QF-105 IdleCapitalCost | idle component | part of QF-069 where that composition is used |

QF-068 is not subtracted beside the complete QF-069. QF-105 is not deducted again. InventoryPenalty and StrandedPenalty may coexist because they price different objects, but their calibration must not both price the same future liquidation/risk cost.
