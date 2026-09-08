# CORR-03 — EXECUTION OUTCOMES / COMPLETION CALIBRATION COMPLETE

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW — IMPLEMENTATION NOT AUTHORIZED

| Field | Result |
|---|---|
| Baseline commit | `705bbe781ad4246ed68262ffca84360a93c0c5e2` |
| CORR-02 prerequisite | `VERIFIED` |
| Harjus research | `COMPLETE` |
| Harjus primary sources | repository HEAD `09816b3...`; 2025 write-up; v4.0.0 write-up; 2026 production log |
| HJ scenarios | `10 / 10` |
| Directly Harjus-evidenced | `HJ-001`, `HJ-003` (`2 / 10`) |
| Project-derived failure scenarios | `HJ-002`, `HJ-004..010` (`8 / 10`) |
| Execution State Machine changes | `0` |
| Execution behavior changes | `0` |
| UNKNOWN / No Blind Retry changes | `0 / 0` |
| Recovery / Actual Fill semantic changes | `0 / 0` |
| Recovery behavior changes | `0` |
| Actual outcome taxonomy | `SPECIFIED` |
| Path flags / terminal classes | `SPECIFIED / SPECIFIED` |
| Unresolved/censoring / attempt cohort | `SPECIFIED / SPECIFIED` |
| Decision-time feature snapshot | `SPECIFIED` |
| Zero-fill / partial / UNKNOWN / Recovery-failure retention | `MANDATORY / MANDATORY / MANDATORY / MANDATORY` |
| `p_full` | probability of eventual original strategy-route completion, actual-fill proved, no Recovery |
| `p_partial` | probability of eventual non-completion with strategy fill, no Recovery, under V1 profile |
| `p_recovery` | probability of eventual non-completion that entered Recovery; not Recovery success |
| `p_failure` | probability of residual eventual zero-fill/no-Recovery non-completion; not UNKNOWN or negative PnL |
| Probability partition | `EXCLUSIVE/EXHAUSTIVE ONLY FOR DECLARED ROUTE_OUTCOME_RESOLVED_V1`; otherwise separate binary forecasts |
| Naïve leg probability multiplication | `FORBIDDEN` |
| Empirical completion baseline | `SPECIFIED` |
| Initial complexity / constant baseline | `SIMPLE / RETAINED` |
| Hierarchical fallback | `SPECIFIED; THRESHOLDS/SMOOTHING CALIBRATED` |
| Complex ML initially / GBDT | `NO / CHALLENGER ONLY` |
| Online live self-learning | `NO` |
| Predicted-actual join / temporal OOS | `SPECIFIED / REQUIRED` |
| Brier/LogLoss | `QF-095/096 REUSED` |
| New QF / Formula semantic changes | `0 / 0` |
| Formula changes | `0` |
| New Risk hard gate / p_full threshold | `0 / NONE` |
| Direct sizing / Q_validated integration | `DEFERRED CORR-05` |
| ExecutionEV integration | `QF-056/057 composition exists; double-count audit DEFERRED CORR-05` |
| Validation / roadmap / operations | `UPDATED / UPDATED / UPDATED` |
| Review baseline | `STALE — CORR SERIES IN PROGRESS` |
| Files outside docs_v2 / source code / legacy docs | `0 / 0 / 0` |
| Human approval | `PENDING` |
| Implementation authorized | `NO` |
| CORR-04 started | `NO` |

## Final disposition

Actual exchange/account evidence flows through Execution, Recovery and Reconciliation before labels are derived. Simulator and Shadow cannot create actual labels. Failures and unresolved attempts remain visible. The empirical model begins as a transparent offline comparator and can affect no decision until scoped promotion. CORR-05 must decide economic integration without multiplying an already represented outcome probability.
