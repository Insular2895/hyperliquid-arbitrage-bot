# CORR-01 — Current Documentation Gap Analysis

DOCUMENTATION STATUS: POST-RECONSTRUCTION ANALYSIS

Classification vocabulary: `PRESENT_AND_CLEAR`, `PRESENT_BUT_AMBIGUOUS`, `PARTIALLY_PRESENT`, `MISSING_EXPLICIT_DEFINITION`, `COLLISION_RISK`.

| Topic | Baseline evidence | Classification | Gap closed by CORR-01 |
|---|---|---|---|
| BBO rejection | Market Graph cheap BBO screen and comparator are defined | `PRESENT_AND_CLEAR` | assign a stable funnel boundary and rejection reason population |
| Exact L2 evaluation | directed L2 walk and exact economics are defined | `PRESENT_AND_CLEAR` | distinguish exact evaluation from exact-valid Opportunity |
| Opportunity identity | Opportunity and route correlation exist | `PARTIALLY_PRESENT` | freeze event-level identity and separate continuous episode identity |
| Route execution identity | Execution chain is explicit | `PRESENT_AND_CLEAR` | connect it to funnel attempt/outcome projection |
| `DecisionTrace` | deterministic decision/intents/transitions/risk trace is defined | `PRESENT_AND_CLEAR` | require funnel/timing lineage without making the trace a metric backend |
| `p_full`, `p_partial`, `p_recovery`, `p_failure` | forecast fields exist | `PRESENT_BUT_AMBIGUOUS` | freeze forecast-time semantics, horizon and actual-label join |
| Actual fills | actual `FillEvent` truth and idempotency exist | `PRESENT_AND_CLEAR` | define any-fill/full-fill/conditional-leg populations |
| Partial exposure | actual fill creates exposure; Recovery rules exist | `PRESENT_AND_CLEAR` | distinguish order partial fill, route partial exposure and intermediate exposure |
| `UNKNOWN` | fail-conservative state is explicit | `PRESENT_AND_CLEAR` | keep attempts in cohort and defer outcome until resolved |
| Recovery | canonical machine and PnL separation exist | `PRESENT_AND_CLEAR` | label entry/success/failure without treating recovery as original-route completion |
| Route completion | `RouteExecutionState.COMPLETED` exists | `PRESENT_BUT_AMBIGUOUS` | define empirical full-route completion and direct-vs-recovery closure |
| Reconciliation | terminal truth requirements exist | `PRESENT_AND_CLEAR` | make reconciliation a necessary final funnel boundary |
| Economic PnL | Strategy, Execution, Recovery and fees are separated | `PARTIALLY_PRESENT` | define attempt-level actual PnL completeness and positive outcome |
| Stage latency | QF-084 decomposition and generic `LatencyTrace` exist | `PARTIALLY_PRESENT` | name non-overlapping timing points and derived intervals |
| Infrastructure latency | QF-084/QF-085 and infra benchmark contracts exist | `PRESENT_AND_CLEAR` | map fine stages to formula components without semantic change |
| Operational percentiles | P50/P95/P99/P99.9/MAX convention exists | `PRESENT_BUT_AMBIGUOUS` | attach metric population, clock, missingness and estimator validity |
| Predicted vs actual | validation requires immutable pairs | `PARTIALLY_PRESENT` | exact freeze/join/label/completeness/calibration contract |
| Optimization gates | profiling and robust economic gates exist | `PARTIALLY_PRESENT` | explicit measure→attribute→change→remeasure→capture→economic chain |
| “Capture” vocabulary | QF-048, QF-085, QF-093 and prose reuse the word | `COLLISION_RISK` | prohibit bare capture in metrics and define qualified terms |
| Evaluation/opportunity/episode/attempt counts | individual concepts occur in different domains | `MISSING_EXPLICIT_DEFINITION` | canonical denominator and population constitution |

## Collision families resolved

1. QF-048/QF-085 survival-at-arrival probability versus end-to-end execution success.
2. forecast `p_full` versus actual `RouteExecutionState.COMPLETED`.
3. QF-093 realized-to-expected economic ratio versus empirical count rates.
4. per-update evaluation, exact-valid opportunity, continuous episode and transmitted attempt.

No collision is resolved by renaming or modifying QF-001..110. CORR-01 adds qualified operational terms around the frozen formulas.
