# ExecutionForecast Economic Mapping

Under `ROUTE_OUTCOME_RESOLVED_V1`, the Simulator owns one attempt-conditional terminal partition:

| Forecast field | Scenario | Scenario cashflow requirement |
|---|---|---|
| `p_full` | `F` | all actual/simulated route conversions, fees, book walk and path effects once; no Recovery |
| `p_partial` | `P` | filled and residual-position economics, terminal exit/holding treatment once; no Recovery entry |
| `p_recovery` | `R` | strategy path plus Recovery execution fees/slippage and QF-080 incremental loss once |
| `p_failure` | `X` | resolved zero-fill/no-Recovery costs, if any |

The canonical conceptual random variable is `Π_exec(q, state)`. This is a specification name, not a new QF. QF-056 computes its expectation and QF-057 supplies the F/P/R/X partition. QF-059, VaR and CVaR are derived from this same distribution.

Survival, participant, completion and infrastructure models are inputs/features used to calibrate or generate this distribution. Consumers do not multiply their headline outputs onto `ExecutionEV` after the distribution has already represented them.
