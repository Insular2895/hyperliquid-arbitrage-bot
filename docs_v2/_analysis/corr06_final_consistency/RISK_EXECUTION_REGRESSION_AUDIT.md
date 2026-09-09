# Risk / Execution Regression Audit

| Invariant | Result |
|---|---|
| No Blind Retry | PASS |
| `SENT` potentially executed | PASS |
| `UNKNOWN` locks affected resources | PASS |
| cancel requested is not canceled | PASS |
| only unique actual fills update Inventory/economics | PASS |
| Recovery starts from current exposure and remains first-class | PASS |
| Reconciliation precedes READY/new risk after uncertainty | PASS |
| positive RAEV or paid priority cannot override hard Risk | PASS |
| prediction/Shadow cannot mutate actual Inventory | PASS |
| speculative node data cannot authorize real risk | PASS |

Priority policy adds request/evidence/cost fields only. Fast-cancel ambiguity creates no assumed transport advantage. State machines, transitions, scheduler safety priority, reservations and actual-truth authority are unchanged. Regression count: `0`.
