# 02 — Market Data, Decision and Execution Metrics

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Market/data

Expose feed state/freshness, BookAge, gaps/reordering/corruption/crossing, source/snapshot/book version, exchange/receive times and clock validity, recorder sequence/backlog/loss/quality regions. A freshness value without market/source/unit/time/validity is unusable.

## Decision

Expose candidates/opportunities, accepted/reduced/rejected, reason family, predicted/actual/would status, q candidates and Q_validated, stage latency, stale-worker/result rejection, formula/model/config/capability versions and DecisionTrace completeness.

## Execution

Expose active executions/orders, zero/partial/full outcomes, send→ACK/first/last fill/cancel latency, cancel races, unknown orders/resolution, reconciliation state/time, Recovery attempts/path/loss, dust/buffer, duplicate/late/incompatible events and exchange/local rejects.

Distributions include count, valid/invalid, P50/P95/P99/P99.9/MAX where meaningful and slice by bounded market family/mode/reason/version/instance. High-cardinality IDs are trace exemplars, not metric labels. Metric export never blocks Core.
