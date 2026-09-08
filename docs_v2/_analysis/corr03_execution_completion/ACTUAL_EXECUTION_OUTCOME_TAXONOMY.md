# CORR-03 — Actual Execution Outcome Taxonomy

DOCUMENTATION STATUS: DERIVED EVIDENCE TAXONOMY — NOT A RUNTIME STATE MACHINE

Labels are projections from deduplicated actual `FillEvent`s, canonical Execution/Recovery states and terminal Reconciliation evidence. Planned, predicted, Replay-counterfactual and Shadow fills cannot produce Live actual labels.

| Terminal analytical class | Required authoritative predicate | `Y_full_route` | Economic meaning |
|---|---|---:|---|
| `STRATEGY_ROUTE_COMPLETED` | original route objectives proved; route `COMPLETED`; no Recovery entry; terminal/reconciliation evidence not contradictory | 1 | may still have negative PnL |
| `SAFE_TERMINAL_NO_STRATEGY_EXPOSURE` | resolved attempt; no actual strategy fill/exposure; all orders/reservations terminal/reconciled | 0 | may have small costs; not automatically loss-free |
| `RECOVERED_AFTER_STRATEGY_FAILURE` | original route not completed; Recovery entered and reached `RECOVERED`; final evidence consistent | 0 | operational recovery, not strategy success or positive PnL |
| `RECOVERY_FAILED_OR_RESIDUAL_EXPOSURE` | Recovery reached `RECOVERY_FAILED`, or terminal manual/escalated state retains material actual exposure | 0 | exposure/loss remains explicitly accounted |
| `TERMINAL_FAILED_SAFE` | original route not completed; terminal-reconciled safe closure not covered above, including a partial-fill/buffer outcome permitted by policy | 0 | economic result is separate |
| `UNRESOLVED` | canonical terminal/reconciliation evidence insufficient or still `UNKNOWN` | unavailable | non-terminal analytical status; never silently 0 |

`INVALID_EVIDENCE` is a dataset-validity status, not a terminal market outcome. A later authoritative correction appends a versioned superseding label; history and path flags remain retained.

## Label authority

`Y_full_route=1` only after actual fills and canonical state prove the original route predicate. It becomes 0 only after authoritative resolution proves one of the non-completion terminal classes. Recovery success, one full order, one full leg, ACK, economic profit or a simulated result are insufficient.
