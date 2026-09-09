# Economic Event Ontology

The canonical event sequence is:

| Event | Meaning | Truth owner |
|---|---|---|
| `E0` | opportunity exists at decision time | Market Graph / frozen candidate |
| `E1` | opportunity survives with acceptable edge at arrival | Simulator survival model |
| `E2` | execution attempt begins | Execution transport truth |
| `E3` | any actual fill occurs | deduplicated exchange/account fills |
| `E4` | intended full route completes | Execution + Reconciliation derived label |
| `E5` | Recovery is entered | Recovery state machine |
| `E6` | Recovery succeeds operationally | Recovery + Reconciliation |
| `E7` | terminal state reconciles | Reconciliation |
| `E8` | final economic outcome is known | Accounting after reconciliation |
| `E9` | final PnL is positive | Accounting projection of E8 |

These events are not synonyms and need not imply one another except where a declared label contract proves it. There is no generic `P_success`. Unknown, unresolved, censored and invalid evidence are coverage states, not economic outcomes.
