# Economic Term Owner Registry

| Term | Unit/type | Single owner | Placement |
|---|---|---|---|
| QF-016 fees/book walk | asset/value cashflow | NetConvert / scenario path | `Π_exec` |
| QF-042 mechanical impact | price/diagnostic or modeled state effect | Microstructure/Shadow Book | no second cash deduction |
| adverse selection | conditional price/PnL effect | Participant/Simulator | scenario PnL when validated |
| QF-080 Recovery loss | positive value loss | Recovery scenario | R cashflow once |
| QF-065 InventoryPenalty | value penalty | Inventory | QF-063 external term |
| QF-068 ExpectedExitCost | value/component | executable exit model | within QF-069 when composed |
| QF-069 StrandedPenalty | value penalty | Capital | QF-063 external term |
| ModelUncertaintyPenalty | value penalty | model governance | QF-063 external term |
| QF-070 BridgeCost | value | Bridge engine | Bridge action |
| QF-087 infra cost | value | Infrastructure/accounting | profile comparison / global close once |
| future priority charge | value | affected execution action | scenario cashflow once |
| QF-093 CaptureRatio | dimensionless diagnostic | Infrastructure/accounting | monitoring only |

The registry is normative for consumers; source formulas remain unchanged.
