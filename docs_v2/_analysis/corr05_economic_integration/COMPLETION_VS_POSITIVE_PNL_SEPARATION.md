# Completion versus Positive-PnL Separation

Completion and profitability are orthogonal label axes:

| Route completion | Final PnL | Valid interpretation |
|---|---|---|
| full | positive | operational and economic positive |
| full | zero/negative | operational completion with no profit/loss |
| noncomplete | positive | incomplete route whose exits/market moves produced profit |
| noncomplete | zero/small negative | failure magnitude is not inferred from non-completion |
| Recovery succeeds | any sign | exposure resolved operationally; PnL remains separate |

`p_full` and FullRouteCompletionRate never prove QF-059. QF-059 is derived from the mass of `Π_exec(q,state) > 0`. Dashboards and validation report both axes separately.
