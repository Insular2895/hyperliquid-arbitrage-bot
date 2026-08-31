# 04 — Clock and Measurement Contract

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Authority and purpose

The SRC-005 Data Contracts are authoritative over Infrastructure prose. This deep spec defines how infrastructure benchmarks consume those timing contracts. It does not redefine exchange timestamp semantics or the canonical data schemas.

Clock quality is part of measurement validity and risk health. A precise-looking timestamp from an unhealthy clock is not valid evidence.

## Clock domains

### Monotonic clock

Use monotonic nanoseconds for elapsed durations on one host/process:

- decode, book, route, simulation, risk and decision stages;
- request RTT and WebSocket ping/pong;
- reconnect stages and `TimeToHealthyFeed`;
- scheduler delay;
- RecorderPenalty experiments;
- local timeout/deadline observation.

Monotonic time is not converted to UTC to create cross-machine ordering. It may reset across reboot/process lifetime depending on the platform contract and therefore carries boot/run context.

### Synchronized wall clock

Use wall time for:

- cross-machine first-arrival comparison;
- apparent Feed Age against an exchange timestamp;
- correlation across machines/services;
- operational incident and RunManifest chronology.

Every wall-clock measurement used comparatively carries contemporaneous clock quality/uncertainty.

### Exchange time

Exchange timestamps are preserved raw with a documented field/semantic version. They may represent event creation, batching, matching, publication or another stage. Until externally verified, their semantic ambiguity is explicit. Infrastructure must not silently reinterpret them as packet-send time.

## Initial synchronization direction

`chrony` is the initial host synchronization direction. The exact configuration and source policy belong to Deployment/Operations validation. At minimum, expose or record:

- `clock_offset`;
- `clock_uncertainty`;
- `root_dispersion`;
- synchronization/health state;
- measurement wall timestamp;
- host/`InfraInstanceId` and run ID;
- clock source/configuration version where available.

Clock offset is an estimate, not truth. Root dispersion is an input to quality assessment, not automatically the full error bound. The canonical uncertainty derivation remains calibrated and versioned.

## Cross-machine comparison

For common event `e`:

```text
Lead_i,j(e) = Recv_i(e) - Recv_j(e)
```

Negative means instance `i` received the event before `j` under the corrected wall-time estimates.

Each receive record retains:

- stable event identity and market;
- raw exchange timestamp if present;
- raw receive wall time;
- receive monotonic time;
- provider/instance/run identity;
- clock offset, uncertainty and health near the observation;
- connection/subscription/sequence context.

## Uncertainty and inconclusive results

For two independent host estimates, the combined uncertainty must be conservatively derived by the approved Data/Validation policy. PASS 01 does not lock a single combination formula.

A paired result is `INCONCLUSIVE_CLOCK` when the observed lead magnitude does not exceed the approved combined uncertainty or either clock is unhealthy. Such events remain countable as inconclusive and are not converted to wins by sign alone.

An aggregate provider comparison reports wins, losses and inconclusive events separately. Dropping inconclusive observations without disclosure is invalid because clock quality may correlate with host/provider conditions.

## Event identity contract

Cross-machine arrival comparison is valid only for the same semantic event. Identity may require market, channel/type, exchange sequence/event ID, payload keys and/or a stable content hash approved by the feed/Data contract.

The protocol must distinguish:

- exact common event;
- duplicate delivery of one event;
- snapshot versus incremental update;
- reordered event;
- semantically similar but nonidentical market state;
- event missing from one instance.

No common identity means no pairwise lead measurement.

## Feed Age contract

When exchange timestamp semantics are usable:

```text
FeedAge = RecvTime - ExchangeTime
```

The record includes local clock uncertainty and exchange timestamp semantic/version. Negative or implausible age is retained and flagged; it is not clamped silently.

Feed Age is invalid or diagnostic-only when:

- the exchange field meaning is unknown;
- timestamp units/epoch are uncertain;
- local clock health is outside policy;
- the event is a replay/snapshot with different semantics;
- the timestamp can be reused across a batch in a way not accounted for.

Relative first-arrival can still be useful when absolute Feed Age is uncertain, provided the cross-host clock contract holds.

## Local latency trace

The source-backed `LatencyTrace` measures ordered local stages. Formula Book QF-084 is the canonical decomposition:

```text
L_total = L_feed + L_compute + L_sign + L_send + L_exchange

L_compute =
  L_decode + L_book + L_route + L_simulation + L_risk + L_decision
```

Instrumentation may expose compatible finer fields such as `route_lookup_ns`, `bbo_ns` and `l2_ns`, but must map them explicitly to the canonical decomposition and avoid double counting.

Stage timestamps/durations carry run/build/config identity and a trace/opportunity/event linkage. Missing stages are `missing/not_applicable`, never silently zero.

## RunManifest

A timing dataset is interpretable only with a `RunManifest` containing at least:

- run ID and observation interval;
- `InfraInstanceId`;
- provider, region, offer/resource profile;
- bot Git revision/build and config;
- OS/kernel/runtime/network mode;
- market universe, subscriptions and feed mode;
- instrumentation/schema version;
- clock synchronization/config and health summary;
- Recorder/tuning mode;
- exclusions and known incidents.

## InfraInstanceId

`InfraInstanceId` binds evidence to the material infrastructure configuration. It changes or is versioned when provider, region, offer/allocation, machine, OS/kernel, Docker network mode or other performance-relevant attributes change materially.

Evidence does not transfer automatically across identities. The Validation Matrix decides the required revalidation depth before Live.

## Clock health and Risk

Clock health contributes to `InfraState`. A clock that prevents trustworthy order deadlines, feed age, incident correlation or cross-machine measurement can move the system to `DEGRADED` or `UNSAFE` according to the Risk Constitution. `UNSAFE` forbids new risk; recovery actions remain governed by the execution state machine.

Exact thresholds, hold periods and recovery hysteresis are `CALIBRATED` under `OPEN-004`.

## Invalidity taxonomy

| Code/concept | Meaning | Treatment |
|---|---|---|
| `INCONCLUSIVE_CLOCK` | Difference is within uncertainty or quality is insufficient | Neither win nor loss; retain evidence |
| `INVALID_EVENT_IDENTITY` | Records cannot be proven to represent the same event | Exclude pair and report count |
| `INVALID_EXCHANGE_TIME` | Timestamp semantics/units are not usable | Exclude Feed Age; preserve raw value |
| `CLOCK_STEP_OR_GAP` | Wall clock discontinuity or observation gap | Mark affected interval invalid |
| `UNHEALTHY_FEED_STATE` | Candidate not subscribed/reconciled/healthy | Exclude arrival comparison; count availability failure |
| `RUN_NOT_COMPARABLE` | Build/config/workload/treatment differs unexpectedly | Do not pool |

Names are documentary concepts unless Data/Validation closure defines an exact enum.

## Reporting rules

- Report sample and invalid/inconclusive counts with every percentile table.
- Preserve raw times and corrections; do not overwrite the observation with a corrected value only.
- Report clock quality over time, not one run-start sample.
- Partition known reconnect/unhealthy intervals rather than hiding them.
- Do not claim cross-server leads smaller than uncertainty.
- Do not infer API colocation from clock-corrected low latency alone.

## Open and external items

- exact uncertainty derivation and health thresholds: `OPEN-004`;
- exchange timestamp semantics and feed field contracts: external revalidation;
- chrony production configuration/alert policy: Deployment and Operations validation;
- schema/enumeration finalization: Data Contracts pass, if not already closed.

## Requirement anchors

Primary anchors include `REQ-CLOCK-0015`, `REQ-INFRA-0090`, `REQ-INFRA-0091`, QF-084, SRC-005 timing/data requirements, and all benchmark requirements marked clock-dependent in the PASS 01 ledger.
