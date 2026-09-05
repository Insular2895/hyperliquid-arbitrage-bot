# Time, Clock, Ordering and Source Quality

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Three time meanings

| Field | Meaning | Valid use | Invalid use |
|---|---|---|---|
| `exchange_ts?` | Time asserted by source | Market chronology/research | Bot knowledge time; invented fallback |
| `recv_wallclock_ts` | Local synchronized wall time | History/cross-host comparison with uncertainty | Local elapsed duration without clock-quality check |
| `recv_monotonic_ns` | Local monotonic receive instant | Ordering, latency deltas, timers | Cross-host absolute comparison |

`ClockQualityRecord { offset, uncertainty, source_count, timestamp }` qualifies wall-clock comparisons. A cross-machine timing claim is valid only when its separation exceeds the combined uncertainty or a versioned statistical rule says so.

## Canonical total order

Within a Recorder/capture context, actual-knowledge replay orders by `(recv_monotonic_ns, source_priority, recorder_seq)`, with `recorder_seq` the definitive unique local observation order. Source priority handles true equal-time concurrency but cannot move a dependent event across an already established receive order. Exchange time never replaces this rule.

Multi-recorder merge is not silently defined: it requires a versioned merge policy, clock-quality record and deterministic tie-break. If the evidence cannot support a total order, mark the region `LOW_FIDELITY` or `INVALID_FOR_REPLAY` for the claimed use.

## Clock and quality interfaces

Core uses `Clock`, implemented by `LiveClock`, `ReplayClock`, `TestClock`. Timers are events. Normalized inputs may carry `SourceQuality { fidelity, age, sequence_integrity, clock_quality }`. Missing/unknown quality is explicit. Replay at T exposes only received events at or before T.

## Tests

Test identical timestamps, late exchange timestamps, wall-clock jump, monotonic order, source reconnect, missing source sequence, clock uncertainty, acceleration and future-event isolation. Expected result is identical ordered input and DecisionTrace across runs.
