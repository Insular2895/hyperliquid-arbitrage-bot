# 11 — Capture Funnel and Latency Attribution

DOCUMENTATION STATUS:
POST-RECONSTRUCTION CORRECTION — AWAITING HUMAN REVIEW

## Purpose and authority

This canonical deep specification makes the system’s decision-to-outcome evidence measurable without adding runtime authority. Market Graph owns evaluations and Opportunities; Simulator owns forecasts; Sizing and Risk own size/permission; Execution, Recovery and Reconciliation own actual state; Accounting owns actual PnL; Data/Recorder own identity and evidence; Operations projects and reports.

```text
DETECTED != EXECUTABLE != ELIGIBLE != ATTEMPTED
         != FILLED != COMPLETED != RECONCILED
         != ECONOMICALLY_POSITIVE
```

No dashboard, trace backend or projector can mutate those owners. Formula QF-001..110 and all existing execution transitions remain unchanged.

## Canonical funnel

The pre-execution stages are:

| ID | Stage | Evidence boundary |
|---|---|---|
| `CF-00` | market observation published | ordered event produced a `BookVersion` |
| `CF-01` | route reevaluation triggered | affected `RouteId` selected |
| `CF-02` | cheap evaluation completed | versioned BBO/comparator result exists |
| `CF-03` | cheap screen passed | declared dispatch criterion passed |
| `CF-04` | exact evaluation completed | directed L2/economic trace completed |
| `CF-05` | exact candidate valid | result finite/fresh/rule-valid and meets candidate predicate |
| `CF-06` | opportunity detected | immutable `OpportunityId` emitted |
| `CF-07` | forecast bundle valid | required supported version-compatible forecasts frozen |
| `CF-08` | execution candidate valid | strategy/capital/mode prerequisites satisfied |
| `CF-09` | Risk eligible | current immutable Risk allow exists |
| `CF-10` | positive size selected | strictly positive quantized size exists |
| `CF-11` | reservation committed | complete atomic reservation set exists |
| `CF-12` | plan committed | immutable `ExecutionPlan` exists |
| `CF-13` | execution attempted | first risk-increasing intent may have transmitted |

A failure proven before possible transmission is not attempted. Any exception/timeout after possible transmission is attempted and may be `UNKNOWN`; it remains in the denominator.

## Outcome DAG

After `CF-13`, evidence can branch through leg reached/attempted, known reject, zero fill, any actual fill, order partial fill, full leg fill, intermediate exposure, `UNKNOWN`, original full-route completion, Recovery, route terminal, terminal reconciliation and complete economic outcome.

`CF-27 FULL_ROUTE_COMPLETED` requires actual fills satisfying the original revalidated route objectives, canonical route `COMPLETED`, and no Recovery entry. Existing Execution may reach `COMPLETED` after safe Recovery; that remains a valid state closure but is reported through Recovery and is not renamed original-route full completion. `TERMINAL_RECONCILED` separately requires order/fill/balance/inventory/fee/reservation agreement. `ECONOMICALLY_POSITIVE` additionally requires complete attempt-level PnL strictly above zero at a declared horizon/numeraire.

## Identity and episode grouping

The canonical lineage is:

```text
MarketEventId -> BookVersion -> ReevaluationId -> RouteEvaluationId
-> OpportunityId -> [OpportunityEpisodeId]
-> ForecastBundleId -> ExecutionPlanCandidateId -> SizingDecisionId
-> RiskDecisionId -> ReservationSetId -> ExecutionId -> ExecutionPlanId
-> LegId -> IntentId -> CLOID -> [OID] -> FillIds
-> [RecoveryId] -> ReconciliationId -> AccountingOutcomeId
```

`OpportunityId` is one immutable exact-valid observation. `OpportunityEpisodeId` is a deterministic offline/near-line grouping of contiguous observations for one venue/directed route/strategy/mode/predicate and `EpisodeSegmentationVersion`. It is not exchange truth or a hot-path gate. Gap, hysteresis and censoring policies are calibrated/versioned; reports never pool versions silently.

## Timing points and latency

Local points use one monotonic clock domain: `T_RX`, `T_NORMALIZED`, `T_ORDERED_ADMISSION`, `T_BOOK_PUBLISHED`, `T_ROUTE_LOOKUP_DONE`, `T_BBO_DONE`, `T_EXACT_ECON_DONE`, optional feature/participant/simulator completion, `T_SIZING_DONE`, `T_RISK_DONE`, `T_RESERVATION_DONE`, `T_PLAN_COMMITTED`, `T_INTENT_FROZEN`, `T_SIGNED`, `T_SEND_HANDOFF`, `T_LOCAL_SEND_COMPLETE`, `T_ACK_RX`, `T_FIRST_FILL_RX`, `T_LAST_FILL_RX`, `T_ROUTE_TERMINAL`, `T_RECONCILED`.

Every duration names its exact endpoints, population, clock, mode, source, window, validity and missing-point policy. Exchange timestamps stay separate; one-way latency is unavailable unless source clock semantics and uncertainty permit it. `send→ACK` combines network/exchange effects unless better evidence supports a split. Percentiles are computed from joined per-trace intervals; stage percentiles are never added. “Tick-to-trade” is prohibited unless explicitly aliased to endpoints/population.

QF-084 remains authoritative. Fine timing points map to its non-overlapping compute subcomponents; unavailable external feed/send/exchange components remain unavailable rather than inferred as a residual.

## Metric constitution

Every metric declares purpose, numerator, denominator, unique-ID population, exclusions, unit, event/cohort time, window/maturity/`AS_OF`, dimensions, source records, missing-data behavior, minimum sample, consumer, maturity status and known bias.

Business-negative outcomes are never data-quality exclusions. Denominator zero produces `UNAVAILABLE`, not 0%. `UNKNOWN`, missing joins and censored outcomes remain visible. Conditional leg-N rates use executions that actually reached and attempted leg N; per-attempt variants are named separately. Shadow `would_*` populations never pool with actual MicroLive/Live results.

Required decision-grade outputs include stage counts/conversions, episodes and duration/censoring, attempt selection, any/conditional fill, intermediate exposure, unknown/resolution, full-route completion, Recovery, reconciliation, economic completeness/positivity, trace/join completeness and all named latency distributions.

## Capture terminology

- QF-048 is `EdgeSurvivalAtArrivalProbability`, not route completion.
- QF-085 applies the same survival-at-arrival object to infrastructure candidate latency.
- `ExecutionForecast.p_full` is a frozen forecast under a versioned label/horizon.
- `FullRouteCompletionRate` is an empirical attempt-cohort count rate.
- QF-093 is a ratio of realized PnL sums to expected executable PnL sums, not a count rate.

Bare `capture rate` or `success rate` is invalid in alerts/reports.

## Predicted versus actual

The forecast used for the committed plan is immutable and joins by explicit candidate/execution/label IDs to the later actual multi-axis outcome. `p_full`, `p_partial`, `p_recovery` and `p_failure` are assessed only against their exact `ForecastLabelVersion`; if labels are not mutually exclusive/exhaustive, assess separate binary forecasts and do not renormalize. Post-outcome model recomputation is `COUNTERFACTUAL_MODEL`, never the original prediction.

## Storage and overhead

Low-cardinality counters/histograms, high-cardinality analytical traces and the safety-critical journal are distinct planes. Raw Opportunity/execution/order/fill/client IDs are forbidden metric labels. The critical journal is not sampled for dashboard convenience. Timestamp capture is bounded/non-blocking; formatting, joining and exporting are off-path. Drops, backlog, projection lag, join completeness and measurement overhead are themselves measured. Critical evidence loss invokes existing degradation/fail-closed policy.

## Optimization gate

Promotion evidence follows `measure -> attribute -> change -> remeasure -> funnel effect -> actual economic effect -> cost/uncertainty`. A lower mean, minimum or microbenchmark alone cannot justify deployment. Comparisons bind one trial identity and aligned population/build/config/infra/workload/mode/metric versions, show tails and overhead, preserve negative results and use QF-084..093 where applicable. No `p_full` Risk threshold is introduced here.

## Validation requirements

- deterministic stage projection and episode identity under identical replay/version;
- denominator fixtures for reject, zero-size, pre-send failure, ambiguous send, zero/partial/full fill, Recovery, `UNKNOWN`, late resolution and negative PnL;
- correlation fan-out/fan-in, missing-link and inferred-join tests;
- timing endpoint, clock-domain, overlap/double-count and missing-point tests;
- predicted/actual label version, censoring, calibration and join-completeness tests;
- instrumentation-off/on overhead, stress/backpressure and exporter-failure tests;
- like-for-like optimization comparison and rollback evidence.

## Detailed normative artifacts

- [Funnel contract](../../_analysis/corr01_capture_observability/CAPTURE_FUNNEL_CONTRACT.md)
- [Terminology constitution](../../_analysis/corr01_capture_observability/CAPTURE_TERMINOLOGY_CONSTITUTION.md)
- [Episode identity](../../_analysis/corr01_capture_observability/MARKET_EPISODE_IDENTITY_CONTRACT.md)
- [Correlation/lineage](../../_analysis/corr01_capture_observability/CORRELATION_AND_LINEAGE_CONTRACT.md)
- [Denominator rules](../../_analysis/corr01_capture_observability/FUNNEL_DENOMINATOR_AND_POPULATION_RULES.md)
- [Timing points](../../_analysis/corr01_capture_observability/TIMING_POINT_CONTRACT.md) and [latency taxonomy](../../_analysis/corr01_capture_observability/LATENCY_STAGE_TAXONOMY.md)
- [Metric catalog](../../_analysis/corr01_capture_observability/CAPTURE_METRIC_CATALOG.md)
- [Outcome labels](../../_analysis/corr01_capture_observability/OUTCOME_LABEL_CONTRACT.md) and [predicted/actual calibration](../../_analysis/corr01_capture_observability/PREDICTED_ACTUAL_CAPTURE_CALIBRATION.md)
- [Storage/cardinality](../../_analysis/corr01_capture_observability/OBSERVABILITY_STORAGE_AND_CARDINALITY_POLICY.md), [overhead](../../_analysis/corr01_capture_observability/INSTRUMENTATION_OVERHEAD_CONTRACT.md), and [optimization economics](../../_analysis/corr01_capture_observability/OPTIMIZATION_ECONOMIC_VALUE_CONTRACT.md)
