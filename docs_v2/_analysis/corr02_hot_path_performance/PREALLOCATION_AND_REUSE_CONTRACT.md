# Preallocation and Reuse Contract

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

Every preallocated buffer, vector, queue, scratch object or pool records:

- capacity source and expected distribution;
- owning lifetime/thread/generation;
- growth, saturation or fallback behavior;
- reset rules and validity marker;
- maximum measured footprint;
- instrumentation for growth/fallback;
- tests for empty/boundary/burst/topology-change/shutdown reuse.

Exhaustion never causes silent truncation, overwrite, corrupt ordering or fabricated completeness. Permitted responses are a safe bounded growth path, explicit fallback allocation, lower-priority observability degradation under its existing policy, or scoped fail-closed behavior. The response is typed and observable.

Object reuse clears every semantic field, version, ID, length and residual. Poison/reset/property tests prove that data from a previous event, route, client or generation cannot leak. Reuse across concurrent owners requires an explicit ownership protocol; aliasing mutable scratch is forbidden.

Capacity values, pool implementation and whether a candidate is worthwhile remain benchmark/calibration choices.
