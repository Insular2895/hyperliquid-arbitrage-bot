# 02 — Market Data, Decision and Execution Metrics

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Market/data

Expose feed state/freshness, BookAge, gaps/reordering/corruption/crossing, source/snapshot/book version, exchange/receive times and clock validity, recorder sequence/backlog/loss/quality regions. A freshness value without market/source/unit/time/validity is unusable.

## Decision

Expose candidates/opportunities, accepted/reduced/rejected, reason family, predicted/actual/would status, q candidates and Q_validated, stage latency, stale-worker/result rejection, formula/model/config/capability versions and DecisionTrace completeness.

## Execution

Expose active executions/orders, zero/partial/full outcomes, send→ACK/first/last fill/cancel latency, cancel races, unknown orders/resolution, reconciliation state/time, Recovery attempts/path/loss, dust/buffer, duplicate/late/incompatible events and exchange/local rejects.

Distributions include count, valid/invalid, P50/P95/P99/P99.9/MAX where meaningful and slice by bounded market family/mode/reason/version/instance. High-cardinality IDs are trace exemplars, not metric labels. Metric export never blocks Core.

## CORR-01 qualification

The words `opportunity`, `capture`, `fill`, `completion` and `success` cannot stand alone in a metric name. Use the stage/count/rate definitions and exact populations from [Capture Funnel and Latency Attribution](11_CAPTURE_FUNNEL_AND_LATENCY_ATTRIBUTION.md). Conditional leg rates, attempt-cohort rates, episode rates and QF-048/QF-085/QF-093 are different objects. Every distribution includes endpoint-complete, invalid-clock, censored/unresolved and total population counts.
