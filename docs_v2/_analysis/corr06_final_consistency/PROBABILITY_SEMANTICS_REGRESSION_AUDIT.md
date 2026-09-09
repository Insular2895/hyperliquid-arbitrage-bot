# Probability Semantics Regression Audit

| Object | Meaning | Not equal to |
|---|---|---|
| QF-048 | edge survival at arrival for a latency distribution | `p_full` |
| QF-085 | infrastructure-specific survival/capture object | `p_full` |
| `p_full` | attempt-conditional original-route completion | QF-059 positive PnL |
| `p_partial` | resolved noncompletion with strategy fill/no Recovery | generic failure |
| `p_recovery` | noncompletion with Recovery entry | Recovery success/loss |
| `p_failure` | resolved zero-fill/no-Recovery residual | UNKNOWN/unresolved |
| FullRouteCompletionRate | empirical attempt cohort evidence | probability forecast |
| QF-093 | ratio of realized-PnL sums to expected-executable-PnL sums | completion probability |

Search/audit result: unauthorized blind probability multiplication `0`. Priority and InfraProfile modify/calibrate one supported `Π_exec(q,state)` distribution; they add no external multiplier.
