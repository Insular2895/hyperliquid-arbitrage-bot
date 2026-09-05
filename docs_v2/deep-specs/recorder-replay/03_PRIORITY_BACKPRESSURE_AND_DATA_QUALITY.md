# Priority, Backpressure and Data Quality

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The closure hierarchy is P0 fills/account/execution, P1 market windows around executions/incidents, P2 general market events, P3 derived diagnostics. The older SRC-003 inversion of P2/P3 is superseded. Priorities govern capture/retention pressure, never economic event application order.

| Pressure | Required response |
|---|---|
| Healthy | Capture all enabled classes; publish metrics |
| Elevated | Alert, accelerate close/archive, suppress optional P3 work |
| Saturated | Explicitly drop/sample/degrade P3, then P2 under versioned policy; preserve P0/P1 |
| Critical P0 risk | Emit critical health; protect journal; invoke Risk/Operations response |

No drop is silent. Minimum counters are `events_received`, `events_written`, `events_dropped`, `sequence_gaps`; metrics also split by priority/source/type and include queue age/depth. A gap produces a quality region with scope/reason.

`INVALID_FOR_REPLAY` means the evidence cannot sustain the requested semantics, such as missing canonical order/book continuity. `LOW_FIDELITY` permits an explicitly limited use with the limitation carried into RunManifest/results. Unknown quality is not treated as valid.

Tests exceed input/write capacity, starve disk, corrupt chunks and drop each class. They assert P0/P1 preservation order, bounded enqueue, accurate counters, quality marking and no false completeness claim.
