# IOC Partial Terminality Audit

| Event | Filled | Residual may fill? | Prior | Source-backed next | Reservation |
|---|---:|---:|---|---|---|
| IOC zero + terminal proof | 0 | no | `PENDING_RESOLUTION` | `REJECTED` or `CANCELED` per observed status → `TERMINAL_RECONCILED` | release only after reconciliation |
| IOC partial + inactive proof | between 0/requested | no | `PARTIALLY_FILLED` | `CANCELED -> TERMINAL_RECONCILED` | consume fill; release proven remainder after reconciliation |
| IOC partial + unknown status | between 0/requested | unknown | `PARTIALLY_FILLED` | `UNKNOWN`/resolution | lock |
| IOC full | requested | no | pending/partial | `FILLED -> TERMINAL_RECONCILED` | consume fill; reconcile remainder |

Authority: SRC-004 lines 600–1010 and 1048–1230. Exchange evidence, never a timeout or local IOC assumption, proves terminality. Order terminality does not imply route terminality.
