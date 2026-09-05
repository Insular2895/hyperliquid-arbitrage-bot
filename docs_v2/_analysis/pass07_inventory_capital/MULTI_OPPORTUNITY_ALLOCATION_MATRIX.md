# Multi-Opportunity Allocation Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Scenario | Required allocation constraint | Expected behavior |
|---|---|---|
| Independent opportunities | prove distinct balances/books/inventory/Risk interactions | QF-078 may allocate independently |
| Same input balance | sum reserved capital <= QF-073 | no double spend |
| Same market depth | joint side/band consumption <= QF-074 | no double-counted L2 |
| Same intermediate asset | aggregate partial/Recovery and inventory risk | joint cap/risk |
| Same inventory band | future deltas aggregate | QF-066 and soft penalty on portfolio state |
| Same Risk budget | total contribution within Risk limit | optimizer cannot relax bound |
| Bridge + opportunity | common balance/book/Risk reservation | choose within utility/action priority |
| Rebalance + opportunity | include restoration need and common resources | Risk priority before new opportunity |
| Recovery + opportunity | existing exposure priority | Recovery resources protected; new risk may be zero |

Pipeline: individual viability -> Risk eligibility -> size curves -> QF-078 allocation -> reservation -> final revalidation. Absolute RAEV/capacity matters; relative edge alone does not.
