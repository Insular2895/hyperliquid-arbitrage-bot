# CORR-03 — ExecutionForecast Probability Audit

DOCUMENTATION STATUS: CANONICAL LABEL PROFILE SPECIFIED — AWAITING HUMAN REVIEW

## Authority finding

`SRC-005` locks the four fields but does not define their label events. QF-057 locks an exclusive/exhaustive F/P/R/X scenario structure. CORR-01 correctly requires `ForecastLabelVersion` and forbids silent normalization. CORR-03 therefore specifies the comparable resolved-route profile below without changing the schema or Formula Book.

## `ROUTE_OUTCOME_RESOLVED_V1`

All four values are decision-time probabilities conditional on one real-attempt candidate and its frozen route objective, mode, q and features. They are not conditional on success of an earlier leg. Across the four eventual terminal classes they are unconditional and exhaustive for this profile. At an analysis cutoff, unresolved/censored status means the eventual class is not yet observable; it is reported separately and is never put into `p_failure`.

| Field | Semantic event | Conditional / unconditional | Denominator / population | Mutually exclusive? | Terminal? | Actual label mapping | Sum-to-one role | Open ambiguity |
|---|---|---|---|---|---|---|---|---|
| `p_full` | original intended strategy route reaches canonical `RouteExecutionState::COMPLETED`, objectives proved by actual fills, and Recovery never entered | conditional on frozen real-attempt candidate; unconditional on leg outcome | one supported real attempt under label/scope | yes | yes | `Y_full_route=1`; `STRATEGY_ROUTE_COMPLETED` | F | none in V1; other versions audited |
| `p_partial` | eventual original-route non-completion with one or more actual strategy fills and no Recovery entry | same; not conditional on prior-leg success | same | yes | yes | `Y_full_route=0`, `AnyFillOccurred=true`, `RecoveryEntered=false`; terminal subclass retained | P | partial path flag remains separate |
| `p_recovery` | eventual original-route non-completion in which Recovery was entered, regardless of `RECOVERED` versus `RECOVERY_FAILED` and regardless of Recovery PnL | same | same | yes | yes | `Y_full_route=0`; either Recovery terminal class | R | does not predict Recovery success |
| `p_failure` | residual eventual original-route non-completion without strategy fill and without Recovery entry, including known zero-fill/reject/safe terminal failure | same | same | yes | yes | `Y_full_route=0`; safe no-exposure/failure terminal class | X | unresolved is excluded, not failure |

For this profile `p_full+p_partial+p_recovery+p_failure=1` over eventual terminal outcomes in its declared attempt population. Binary scoring at a cutoff uses resolved labels and discloses unresolved/censored/invalid coverage. If a Simulator artifact uses another label version, each field is evaluated as its declared binary event unless that version independently proves an exclusive/exhaustive partition. Consumers never infer a partition from field names.

For initial TT/TTT, `forecast_horizon` binds a versioned canonical-terminal resolution policy, not an invented fixed millisecond cutoff. A finite-time profile that permits an order/route still unresolved at its horizon cannot use these four terminal fields as an exhaustive partition unless its label schema separately represents that mass; otherwise the four fields are evaluated as separate binary forecasts. Maker time-to-event profiles are separate.

## Non-collisions

- `p_full` is not QF-048/QF-085 arrival survival, QF-059 positive-PnL probability or an empirical completion rate.
- `p_partial` is a terminal route-outcome class for this profile; `PartialFillOccurred` remains a path flag and may coexist with `p_full`.
- `p_recovery` means the Recovery-entry route class, not probability Recovery succeeds.
- `p_failure` is not `UNKNOWN`, negative PnL or every non-completion.
- `Y_full_route` is derived from actual Execution/Reconciliation evidence; Simulator/Shadow cannot create it.

## Open/calibrated boundary

The exact resolution policy, forecast horizon, tolerated original-route objective and operational mechanism for representing conditional resolution coverage remain versioned/calibrated. If implementation cannot preserve the stated conditioning and coverage disclosure, the four values must remain separate binary forecasts and cannot feed QF-057 as a partition. CORR-05 must audit whether this distribution is already economically composed in QF-056/057 before any RAEV, sizing or `Q_validated` integration.
