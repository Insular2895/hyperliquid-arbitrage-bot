# Stale Result and Versioning Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

## Worker identity

A `C2` request/result family must represent, directly or by typed references:

```text
WorkerJobIdentity {
  job_id, family, generation, created_at_monotonic,
  deadline_monotonic, input_fingerprint,
  ordered_event_cursor, book_versions[], account_version?,
  inventory_version?, reservation_version?, risk_version?,
  graph_index_generation?, metadata_version?, fee_version?,
  feature_schema_version?, feature_snapshot_version?,
  model_artifact_id?, simulator_version?, formula_version,
  config_hash, capability_scope
}

WorkerResultIdentity {
  job_id, family, generation, input_fingerprint,
  started_at_monotonic, completed_at_monotonic,
  output_hash, validity_envelope, support, ood_status,
  disposition_reason?
}
```

Fields are conceptual schema requirements, not authorization to mutate frozen structs without compatibility review.

## Acceptance algorithm

1. Match job, family, generation and complete input fingerprint.
2. Reject duplicate, unknown or canceled job identity.
3. Check deadline and capability/model/config validity.
4. Compare every material version with current C0 state.
5. If the declared operation supports exact bounded revalidation, revalidate; otherwise discard stale output.
6. Apply deterministic policy ordering independent of completion time.
7. Run current final Risk and atomic Reservation before any risk-increasing intent.
8. Record `committed`, `discarded_stale`, `discarded_late`, `discarded_duplicate`, `fallback_used` or another typed disposition.

No stale worker `ALLOW`, forecast, size, route or Recovery proposal can authorize commit. Stale explanations may remain evidence but carry no permission.

## Supersession and cancellation

- A newer generation may supersede older derived work only by explicit identity/policy.
- Cancellation is cooperative performance control. Correctness never assumes that canceled CPU work stopped.
- A late result is safely discardable and cannot resurrect a closed generation.
- Completion order is recorded for scheduler analysis but is not economic priority.

## Memory retention

Active-job metadata and result caches are bounded. Terminal entries are removed by a deterministic lifecycle after required disposition evidence is handed to Recorder. No orphan result may retain an immutable Book/model snapshot indefinitely. Cache eviction changes performance only; required decision/outcome evidence follows Recorder retention.

## Metrics

Per bounded family/profile: jobs requested/started/completed/canceled, queue wait, compute time, handoff time, current/stale/late/duplicate/revalidated/committed/discarded, deadline miss, fallback, backlog and retained bytes. Raw job/route IDs live in traces, not metric labels.
