# CORR-01 — Latency Stage Taxonomy

DOCUMENTATION STATUS: CANONICAL ATTRIBUTION DESIGN — AWAITING HUMAN REVIEW

## Derived local stages

Each duration is `end - start` in one valid monotonic clock domain. It is recorded only for the named population.

| Metric stem | Start | End | Population |
|---|---|---|---|
| `NormalizeDuration` | `T_RX` | `T_NORMALIZED` | normalized observations |
| `OrderedAdmissionDuration` | `T_NORMALIZED` | `T_ORDERED_ADMISSION` | admitted observations |
| `BookPublishDuration` | `T_ORDERED_ADMISSION` | `T_BOOK_PUBLISHED` | book-affecting admitted observations |
| `AffectedRouteLookupDuration` | `T_BOOK_PUBLISHED` | `T_ROUTE_LOOKUP_DONE` | triggered reevaluations |
| `CheapBboEvaluationDuration` | `T_ROUTE_LOOKUP_DONE` | `T_BBO_DONE` | cheap evaluations |
| `ExactEconomicEvaluationDuration` | `T_BBO_DONE` | `T_EXACT_ECON_DONE` | exact-dispatched evaluations |
| `FeatureDuration` | `T_EXACT_ECON_DONE` | `T_FEATURES_DONE` | feature-required candidates |
| `ParticipantForecastDuration` | `T_FEATURES_DONE` | `T_PARTICIPANT_DONE` | participant-required candidates |
| `SimulationDuration` | latest required predecessor | `T_SIMULATION_DONE` | Simulator-required candidates; predecessor named in record |
| `SizingDuration` | latest required forecast/economics point | `T_SIZING_DONE` | sized candidates; predecessor named |
| `RiskDecisionDuration` | `T_SIZING_DONE` | `T_RISK_DONE` | Risk-evaluated candidates |
| `ReservationDuration` | `T_RISK_DONE` | `T_RESERVATION_DONE` | reservation attempts |
| `PlanCommitDuration` | `T_RESERVATION_DONE` | `T_PLAN_COMMITTED` | committed or failed plan paths |
| `IntentFreezeDuration` | `T_PLAN_COMMITTED` | `T_INTENT_FROZEN` | intent-producing plans |
| `SignDuration` | `T_INTENT_FROZEN` | `T_SIGNED` | signed intents |
| `SendHandoffDuration` | `T_SIGNED` | `T_SEND_HANDOFF` | transport handoffs |
| `LocalSendDuration` | `T_SEND_HANDOFF` | `T_LOCAL_SEND_COMPLETE` | locally completed sends |
| `SendToAckDuration` | `T_SEND_HANDOFF` | `T_ACK_RX` | attempts with ACK evidence; unresolved separately |
| `SendToFirstFillDuration` | `T_SEND_HANDOFF` | `T_FIRST_FILL_RX` | attempts with fill evidence; zero-fill is not excluded from count reports |
| `FirstToLastFillDuration` | `T_FIRST_FILL_RX` | `T_LAST_FILL_RX` | executions with terminally known fill set |
| `AttemptToRouteTerminalDuration` | `T_SEND_HANDOFF` | `T_ROUTE_TERMINAL` | resolved terminal attempts |
| `RouteTerminalToReconciledDuration` | `T_ROUTE_TERMINAL` | `T_RECONCILED` | terminal routes that reconcile |
| `AttemptToReconciledDuration` | `T_SEND_HANDOFF` | `T_RECONCILED` | reconciled attempts |

## End-to-end qualified names

- `ObservationToExactCandidateDuration = T_EXACT_ECON_DONE - T_RX` for exact-dispatched evaluations.
- `ObservationToPlanCommitDuration = T_PLAN_COMMITTED - T_RX` for committed plans.
- `ObservationToSendHandoffDuration = T_SEND_HANDOFF - T_RX` for attempts.
- `ObservationToFirstFillDuration = T_FIRST_FILL_RX - T_RX` for any-fill attempts.
- `ObservationToReconciledDuration = T_RECONCILED - T_RX` for reconciled attempts.

The term `tick-to-trade` is prohibited unless the report aliases it to one exact start/end pair and population. Mean-only reporting is insufficient.

## QF-084 compatibility map

CORR-01 does not change QF-084. Fine local points support this non-overlapping interpretation when present:

```text
L_decode    = T_NORMALIZED - T_RX
L_book      = T_BOOK_PUBLISHED - T_NORMALIZED
L_route     = route lookup + cheap/exact/feature/participant work assigned by trace
L_simulation= simulator-owned interval
L_risk      = T_RISK_DONE - T_SIZING_DONE
L_decision  = non-overlapping sizing/reservation/plan/intent decision intervals
L_compute   = sum of the declared fine components
L_sign      = T_SIGNED - T_INTENT_FROZEN
```

`L_feed`, network portion of `L_send`, and `L_exchange` are not automatically observable from local points. `T_LOCAL_SEND_COMPLETE - T_SEND_HANDOFF` is named `LocalSendDuration`; `T_ACK_RX - T_SEND_HANDOFF` is an observed round trip that combines transport/exchange/response effects. Splitting it requires valid external timestamps or controlled measurement and uncertainty. No residual is silently assigned to the exchange.

## Distribution contract

For every duration, publish total population, endpoint-complete count, invalid-clock count, censored/unresolved count, P50/P95/P99/P99.9/MAX where sample/evidence rules permit, estimator/version and measurement window. Tail percentiles are `UNAVAILABLE` below calibrated sample sufficiency. Histograms use versioned stable buckets; raw high-cardinality trace exemplars remain outside metric labels.

### Normative metric-entry completion

The endpoint/population table above and this table form one normative catalog entry per metric. Numerator is the count of valid endpoint-complete durations in a histogram bucket/quantile sample; denominator for completeness is the full named population. Unit is monotonic nanoseconds internally and an explicitly named display unit. Cohort time is the start point, with observation window, maturity horizon and `AS_OF`. Common dimensions are bounded mode, market/route family, stage validity, build/config major version and infrastructure instance class. Source records are the two typed timing points plus lineage. Data-quality exclusions follow the denominator contract; negative business outcomes are not exclusions. Minimum count, histogram buckets and estimator are `CALIBRATED`. Consumers are Operations, Validation and the owning stage domain; status is `SPECIFIED_NOT_IMPLEMENTED`.

| Metric family | Purpose | Missing/censor behavior | Principal known bias |
|---|---|---|---|
| normalize/admission/book | local market-data processing attribution | missing endpoint stays in population and invalidates only that duration | message size, source and burst mix |
| route lookup/BBO/exact | Graph compute attribution and amplification | dispatched-but-incomplete work counted separately | route density, size grid and early rejection |
| feature/participant/simulation | optional model path attribution | not-required differs from required-but-missing | support/OOD and asynchronous scheduling selection |
| sizing/Risk/reservation/plan/intent | decision/admission attribution | zero/reject remains valid timing if both endpoints exist | only candidates reaching each conditional stage |
| sign/handoff/local send | controlled local execution path | possible-send ambiguity remains attempt; missing completion censored | signer cache, transport buffering and batching |
| send→ACK/fill | observed response/fill timing | no-ACK/no-fill/UNKNOWN is censored/outcome count, not silently excluded | exchange/network conditions and fill selection |
| fill span/route terminal/reconciliation | actual outcome/finality duration | provisional last fill and unresolved routes stay censored | route length, Recovery and late reconciliation |
| qualified end-to-end | actual per-trace critical-path latency | any required endpoint missing invalidates that sample and is counted | only paths reaching the named end stage |

Optimization comparisons must also report stage-reach/conversion rates so conditional-latency improvement cannot hide selective dropping of slower items.

## Non-additivity warning

Percentiles do not add: the sum of stage P99 values is not end-to-end P99. End-to-end distributions are computed per joined trace, then aggregated. Parallel branches name their critical path; overlapping intervals are never summed as sequential work.
