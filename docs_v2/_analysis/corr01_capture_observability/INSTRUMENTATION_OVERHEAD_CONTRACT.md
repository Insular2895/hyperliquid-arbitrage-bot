# CORR-01 — Instrumentation Overhead Contract

DOCUMENTATION STATUS: DESIGN CONTRACT — IMPLEMENTATION NOT AUTHORIZED

## Invariant

Measurement must not silently create the latency, drops or stalls it claims to diagnose. The synchronous Core records bounded timestamps/IDs through a non-blocking interface; formatting, joins, export, compression and aggregation occur off the hot path.

## Required comparison

Any instrumentation implementation is evaluated with an A/B or paired design over comparable workload/configuration:

- disabled/minimal baseline versus proposed instrumentation level;
- CPU time, wall/monotonic stage distributions, scheduler tails, allocations and cache/queue effects;
- recorder/telemetry enqueue failures, drops, backlog and storage/export pressure;
- decision throughput and funnel-stage completeness;
- warm-up, sample count, host/instance/build/config and uncertainty;
- both normal load and declared stress/failure cases.

Acceptance limits are `CALIBRATED`, versioned and owned by Validation/Operations. No numeric overhead budget is frozen by CORR-01.

## Degradation order

When pressure rises, degrade observability safely in this order:

1. remove high-cardinality exemplars according to the versioned sampling policy;
2. reduce optional analytical timing detail;
3. aggregate/drop low-priority metrics with explicit loss counters;
4. preserve execution journal, order/fill/reconciliation/Risk evidence and safety health;
5. if critical evidence cannot be preserved, capability degrades/fails closed according to existing Risk/Operations contracts.

No metrics exporter, trace backend, episode projector or dashboard may block cancels, Recovery, Reconciliation or safe shutdown.

## Self-observation

Required health evidence includes timestamp-write cost, observation queue depth, enqueue failures, dropped records by priority/reason, export age/failures, projection lag, join completeness and clock validity. Missing self-observation invalidates optimization claims that rely on the affected instrumentation.
