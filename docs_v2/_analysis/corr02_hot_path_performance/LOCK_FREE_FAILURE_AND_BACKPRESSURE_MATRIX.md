# Lock-Free Failure and Backpressure Matrix

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Boundary | Priority/content | Full behavior | Never allowed | Recovery/evidence |
|---|---|---|---|---|
| market ingress | book deltas/snapshots | explicit invalidation and resync if required evidence cannot be preserved | silent drop followed by valid-book claim | gap counter, Book invalid, resync |
| ordered-core handoff | canonical events/commands | fail closed or bounded upstream pressure under specified protocol | reorder/duplicate/overwrite | sequence audit and health event |
| worker request/result | immutable proposals | cancel/drop stale low-value computation, never current truth | stale commit or loss of required unique input tuple | stale/cancel counters, fallback |
| Recorder P0 | orders/fills/account/fees/Risk/Reservations/Execution/Recovery/Reconciliation/journal | preserve or declare critical health and block new risk as owned policy requires | silent loss or indefinite Core disk wait | durability outcome, UNKNOWN and reconciliation evidence |
| Recorder P1 | protected market/infra windows around executions or incidents | preserve while pinned; invalidate/lower affected evidence if incomplete | treat missing protected context as complete | protected-window manifest, gap and incident evidence |
| Recorder P2 | general market RAW/normalized capture | versioned sample/drop/degrade with scoped quality invalidation | relabel incomplete market data as complete | loss counters, gaps and dataset missingness |
| Recorder P3 | derived analytics/diagnostics | shed/delay/recompute first under declared policy | hide missingness or fabricate recomputation | loss counters and lineage/recompute evidence |
| metrics | aggregate telemetry | drop/coarsen low-priority observations under declared policy | block safety commit or hide missingness | health/cardinality counters |

Every later queue specification includes capacity source, producer/consumer cardinality, progress guarantee actually claimed, ordering, overflow, retry/spin/park behavior, memory-order proof, cache-line layout, shutdown/drain, priority inversion and failure injection. Account/fill/critical execution evidence is never sacrificed to keep market telemetry flowing.
