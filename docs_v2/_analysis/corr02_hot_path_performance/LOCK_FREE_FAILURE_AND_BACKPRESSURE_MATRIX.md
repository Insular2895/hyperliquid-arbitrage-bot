# Lock-Free Failure and Backpressure Matrix

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Boundary | Priority/content | Full behavior | Never allowed | Recovery/evidence |
|---|---|---|---|---|
| market ingress | book deltas/snapshots | explicit invalidation and resync if required evidence cannot be preserved | silent drop followed by valid-book claim | gap counter, Book invalid, resync |
| ordered-core handoff | canonical events/commands | fail closed or bounded upstream pressure under specified protocol | reorder/duplicate/overwrite | sequence audit and health event |
| worker request/result | immutable proposals | cancel/drop stale low-value computation, never current truth | stale commit or loss of required unique input tuple | stale/cancel counters, fallback |
| Recorder P0/P1 | orders/fills/account/journal critical evidence | preserve or declare critical health and block new risk as owned policy requires | silent loss | durable reconciliation path, incident |
| Recorder P2/P3 | lower-priority analytics | versioned sampling/drop/degrade | relabel incomplete as complete | loss counters and missingness |
| metrics | aggregate telemetry | drop/coarsen low-priority observations under declared policy | block safety commit or hide missingness | health/cardinality counters |

Every later queue specification includes capacity source, producer/consumer cardinality, progress guarantee actually claimed, ordering, overflow, retry/spin/park behavior, memory-order proof, cache-line layout, shutdown/drain, priority inversion and failure injection. Account/fill/critical execution evidence is never sacrificed to keep market telemetry flowing.
