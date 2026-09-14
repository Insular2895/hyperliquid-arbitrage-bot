# Bridge Risk Exact-Once Audit

| Phenomenon | Canonical owner | Included in | Forbidden duplicate |
|---|---|---|---|
| L2 impact | NetConvert | QF-016/QF-070 end value | Bridge risk/RAEV cash cost |
| trading fee/rebate | NetConvert/Fee | QF-016 asset deltas | scenario/Bridge/Accounting duplicate |
| execution failure/adverse selection | Simulator scenario | QF-057 | external second execution penalty |
| destination-state risk | OPEN partition | QF-070 or QF-072, once | both RiskCost terms |
| expected exit burden | Exit/Capital | QF-068 and explicit QF-071/072 term | full QF-069 beside it |
| idle capital | Capital | QF-105 / QF-069 where applicable | second RAEV/Bridge term |
| inventory deviation | Inventory | QF-065 external penalty | scenario cashflow duplicate |
| Recovery cashflow | Recovery scenario | QF-057/QF-080 | second RAEV/Bridge penalty |

Because the source does not define the exact `RiskCost(P)`/`RelocationRiskCost` split, proof of disjoint ownership is a precondition; otherwise Bridge fails closed.
