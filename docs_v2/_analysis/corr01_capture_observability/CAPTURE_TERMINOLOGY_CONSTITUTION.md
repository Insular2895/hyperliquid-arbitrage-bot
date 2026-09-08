# CORR-01 — Capture Terminology Constitution

DOCUMENTATION STATUS: CANONICAL TERMINOLOGY STRENGTHENING — AWAITING HUMAN REVIEW

## Prohibited shorthand

No metric, alert, gate or report may use bare `capture`, `capture rate` or `success rate`. It must name the event, population and scope.

## Canonical qualified terms

| Term | Exact semantic object | Population / denominator | Must not be called |
|---|---|---|---|
| `EdgeSurvivalAtArrivalProbability` | QF-048 `E_L[S(L)]` | model distribution, not an empirical count cohort | full-route capture probability |
| `InfrastructureEdgeSurvivalAtArrivalProbability` | QF-085 `E_{L_s}[S(L_s)]` for infrastructure candidate `s` | aligned model and infrastructure latency distribution | execution success rate |
| `ExecutionForecast.p_full` | under `ROUTE_OUTCOME_RESOLVED_V1`, frozen probability of eventual original-route completion proved by actual fills with no Recovery entry | one real-attempt candidate and frozen features | actual full-route completion |
| `ExecutionForecast.p_partial` | under that profile, frozen probability of eventual non-completion with strategy fill and no Recovery entry | same attempt population; not conditional on prior-leg success | observed partial-fill incidence |
| `ExecutionForecast.p_recovery` | under that profile, frozen probability of eventual non-completion that enters Recovery, irrespective of Recovery success/PnL | same attempt population | probability Recovery succeeds |
| `ExecutionForecast.p_failure` | under that profile, frozen residual eventual zero-fill/no-Recovery non-completion probability | same attempt population | `UNKNOWN`, any reject, or negative PnL |
| `FullRouteCompletionRate` | attempts meeting `CF-27` | `ExecutionAttemptCount` in identical mode/scope/window, with unresolved shown separately | QF-048/QF-085 capture |
| `FirstLegAnyFillRate` | attempts with at least one actual fill on first intended leg | attempts that reached/attempted first leg, as explicitly selected | full-route completion |
| `ConditionalLegNFullFillRate` | leg-N full fills | executions that actually reached and attempted leg N | unconditional attempt success |
| `RecoveryEntryRate` | attempts entering Recovery | attempts | failure rate or route completion |
| `TerminalReconciliationRate` | attempts reconciled within the declared window/horizon | attempts mature enough for that horizon; unresolved disclosed | economic success |
| `EconomicallyPositiveAttemptRate` | complete actual PnL > 0 | economically complete, terminal-reconciled attempts | gross opportunity rate |
| `CaptureRatioQF093` | QF-093 `sum(RealizedPnL)/sum(ExpectedExecutablePnL)` | same eligible economic set and positive denominator | count-based success/capture rate |
| `OpportunityEpisode` | offline/near-line grouping of contiguous exact-valid `Opportunity` observations under a versioned rule | episode records | one BBO tick, one `OpportunityId`, or one attempt |

## Forecast label version

`ExecutionForecast` must bind `ForecastLabelVersion`, forecast horizon, route objective, execution mode, candidate size, market/config/model/formula/schema versions and issue time. `p_full + p_partial + p_recovery + p_failure = 1` only when that exact label version declares a mutually exclusive exhaustive partition. Missing/invalid labels invalidate the probability vector; consumers may not silently renormalize it.

CORR-03 closes `ROUTE_OUTCOME_RESOLVED_V1` as an eventual-terminal partition. Unresolved/censored/invalid at the analysis cutoff is observation coverage, not `p_failure`; scoring discloses it separately. Other versions retain the general rule above.

For CORR-01, the comparable actual `full` label is `CF-27 FULL_ROUTE_COMPLETED`. Recovery entry is separately observable. A safe route closure reached after Recovery remains canonical Execution `COMPLETED` where the existing state machine says so, but it does not retroactively satisfy the original full-route label.

## Rate suffixes

Empirical metrics use names ending in `Count`, `Rate`, `Duration` or `PnL` and declare a population. Forecasts use `Probability` or the frozen `p_*` schema fields. Formula references retain `QF-xxx`. Economic ratios name the numerator and denominator or retain `QF093` in the metric name.
