# Order vs Route Terminality

| Order outcome | Order terminal? | Route implication |
|---|---:|---|
| IOC partial, inactive and reconciled | yes | continue actual quantity, Recovery or abort safely |
| leg full and reconciled | yes | later legs may remain |
| Recovery order terminal | yes | residual exposure may remain |
| `UNKNOWN` | no | route cannot close or release affected capital |

`FILLED != route COMPLETED`; `CANCELED != route ABORTED`; `TERMINAL_RECONCILED` is per order and does not waive exposure evaluation.
