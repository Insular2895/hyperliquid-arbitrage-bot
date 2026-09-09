# Probability Conditioning Matrix

| Quantity | Canonical event | Conditioning / population | Not equivalent to |
|---|---|---|---|
| QF-048 `P_capture` | E1 | expectation of edge-survival function over decision-time latency | attempt, fill, completion, profit |
| QF-085 `P_capture(s)` | E1 under infra profile `s` | same event under the declared profile | infra ROI or completion |
| `p_full` | F / E4 | `P(F | E2, frozen q/state, label version, supported scope)` | QF-048, positive PnL |
| `p_partial` | P | same resolved-attempt conditioning | any path partial that later completes |
| `p_recovery` | R / E5 | same; entry regardless of E6 or PnL | Recovery success |
| `p_failure` | X | same; resolved zero-fill/no-Recovery residual | UNKNOWN, negative PnL |
| QF-059 | E9 | probability mass with `Π_exec > 0` in the same distribution | completion or Recovery success |
| FullRouteCompletionRate | empirical E4 rate | declared attempt/resolved cohort and maturity policy | a formula or penalty |
| RecoverySuccessRate | E6 | `P(E6 | E5)` with resolved Recovery coverage | route completion or profit |
| QF-093 | realized/expected PnL ratio | ratio-of-sums in its declared infra/accounting scope | any event probability |

Blind multiplication is forbidden. A future factored model must prove coherent denominators, conditional events, disjoint information and joint calibration.
