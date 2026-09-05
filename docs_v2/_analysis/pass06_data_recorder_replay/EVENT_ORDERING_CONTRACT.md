# Event Ordering Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Canonical rule

For one Recorder/capture context, the total-order key for actual-knowledge processing is:

```text
(recv_monotonic_ns, source_priority, recorder_seq)
```

`recorder_seq` is strictly increasing per Recorder and is the definitive unique local observation order. `recv_monotonic_ns` establishes the receive timeline; `source_priority` resolves declared equal-time concurrency; `recorder_seq` is the final tie-break. The stored sequence may never be rewritten from `exchange_ts`.

## Semantics

| Case | Required handling |
|---|---|
| Older exchange timestamp arrives late | Apply at its receive position; retain exchange time for chronology research |
| Equal receive timestamp | Apply configured source priority, then recorder sequence |
| Concurrent adapters | Ingest through central ordered coordinator |
| Priority/backpressure class differs | Does not alter Core economic order |
| Missing source sequence | Preserve optional absence; local order still exists |
| Cross-recorder merge | Require a versioned merge rule and clock uncertainty; otherwise lower fidelity |
| Replay batching | Preserve the same canonical order inside the batch |
| Worker completion race | Coordinator orders commit; stale versions discard/revalidate |

## No-lookahead consequence

At ReplayClock T, no input whose local receive time/order lies after T can be observed by Core, directly or through precomputed features, models, timers, checkpoints or buffers.

## Open boundary

The exact numeric `source_priority` table and cross-recorder merge algorithm are implementation decisions requiring a deterministic spec and tests. They may not reorder already established dependency/receive order.
