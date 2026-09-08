# CORR-03 — Path Flags and Terminal Outcomes

DOCUMENTATION STATUS: DERIVED EVIDENCE CONTRACT

Path/incident flags are sticky historical facts. Terminal class answers where the attempt ended; it never erases how it got there.

Minimum flags: `ZeroFillOccurred`, `PartialFillOccurred`, `LaterLegFailureOccurred`, `UnknownOrderOccurred`, `CancelRaceOccurred`, `RecoveryEntered`, `RecoveryPartialOccurred`, `DuplicateFillObserved`, `RestartReconciliationOccurred`, `ResidualExposureObserved`.

| Example canonical path | Sticky flags | Terminal class | `Y_full_route` |
|---|---|---|---:|
| SENT → known zero fill → reconciled | zero | `SAFE_TERMINAL_NO_STRATEGY_EXPOSURE` | 0 |
| partial fill → more fills/legs → `COMPLETED`, no Recovery | partial | `STRATEGY_ROUTE_COMPLETED` | 1 |
| UNKNOWN → fill discovered → original route safely completes | unknown | `STRATEGY_ROUTE_COMPLETED` | 1 |
| partial/later-leg failure → Recovery → `RECOVERED` | partial/later/recovery | `RECOVERED_AFTER_STRATEGY_FAILURE` | 0 |
| cancel requested → fill arrives → route completes | cancel-race | `STRATEGY_ROUTE_COMPLETED` | 1 |
| Recovery partial → limits exhausted | recovery/recovery-partial/residual | `RECOVERY_FAILED_OR_RESIDUAL_EXPOSURE` | 0 |
| SENT → UNKNOWN, cutoff before proof | unknown | `UNRESOLVED` | unavailable |

This matrix prevents the invalid equivalences `partial=failure`, `UNKNOWN=no fill`, `RECOVERED=COMPLETED` and `completed=profitable`.
