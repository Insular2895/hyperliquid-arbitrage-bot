# CORR-01 — Funnel Denominator and Population Rules

DOCUMENTATION STATUS: CANONICAL METRIC CONTRACT — AWAITING HUMAN REVIEW

## Population identity

Every count/rate declares:

```text
PopulationId = hash(
  metric_definition_version, RunMode, venue, strategy,
  route/market scope, capability/config/model/formula versions,
  observation-time window, maturity horizon, inclusion/exclusion policy
)
```

Hash/encoding is implementation-owned; the included fields are normative. Rates from different `PopulationId`s are not silently combined.

## General denominator rules

1. A stage conversion rate uses the immediately named parent population unless the metric name says otherwise.
2. Counts are of unique canonical IDs, never log lines, retries, packets or samples.
3. An originating item remains in its denominator when later evidence is missing, unknown or negative. Missingness is reported, not erased.
4. Exact invalidity, Risk rejection, zero size, reservation failure and proven pre-send failure have explicit dispositions.
5. `UNKNOWN` attempts remain attempted. Outcome-rate reports either wait for a declared maturity horizon or expose unresolved/censored counts beside resolved rates.
6. Conditional leg-N fill rates use executions that reached and attempted leg N. Unconditional per-attempt leg metrics must say `PerAttempt`.
7. Actual-fill rates are available only in MicroLive/Live or a named simulated-run population; Shadow truth is `would_*` and never pooled with actual.
8. Full-route completion requires `CF-27`; terminal safe closure after Recovery is reported under Recovery/reconciliation outcomes.
9. Economic positivity uses only `CF-31` economically complete records. A second `PerAttemptLowerBound` metric may include unresolved/missing as non-positive, but must be named and never substituted.
10. Episode metrics bind one `EpisodeSegmentationVersion` and disclose left/right censoring and observation gaps.
11. Comparisons use the same market/opportunity universe, capital, mode, strategy/config and maturity policy, or apply a predeclared controlled design with uncertainty.

## Exclusion vocabulary

Allowed metric-specific exclusions are explicit and counted: `DUPLICATE_CANONICAL_ID`, `WRONG_MODE`, `OUTSIDE_TIME_WINDOW`, `OUTSIDE_DECLARED_SCOPE`, `SCHEMA_INCOMPATIBLE`, `INVALID_CLOCK`, `MISSING_REQUIRED_ENDPOINT`, `INFERRED_JOIN_NOT_ALLOWED`, `NOT_MATURE_AT_CUTOFF`, `TEST_TRAFFIC`, `OPERATOR_DECLARED_INVALID_RUN`.

Business-negative outcomes such as BBO reject, exact reject, Risk reject, zero size, exchange reject, zero fill, partial fill, Recovery or negative PnL are not data-quality exclusions.

## Time windows and maturity

Counts are assigned by the observation/attempt start time stated by the metric. Outcomes may arrive after the reporting window and update the cohort until its maturity horizon. Reports state `AS_OF` time, resolved fraction and revisions. Rolling windows do not truncate a route’s later outcome from its originating cohort.

## Empty and small cohorts

- denominator zero: emit count 0 and rate `UNAVAILABLE`, never 0%;
- below `minimum_sample_count`: emit the estimate with `LOW_SAMPLE` only if policy permits, never a promotion-grade claim;
- invalid or systematically missing evidence: emit `INVALID_EVIDENCE`, not an optimistic filtered rate;
- confidence/uncertainty method is calibrated/versioned and may differ by metric, but population and raw counts remain visible.
