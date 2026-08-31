# 03 — Benchmark Protocol

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Objective

`hl-infra-benchmark` is the conceptual common workload used to compare infrastructure candidates. PASS 01 defines the evidence contract; it does not implement the tool.

The protocol answers three ordered questions:

1. Is the run valid and comparable?
2. Is the candidate technically better for the real Hyperliquid workload?
3. Does the improvement produce robust positive net economic value?

## Run manifest and comparability

Every run records:

- run ID, `InfraInstanceId`, provider, region, offer and resource allocation;
- start/end, observation intervals and excluded intervals with reason;
- bot build, Git revision, feature flags and config version;
- market universe, subscriptions, feed mode and workload version;
- OS, kernel, CPU model/allocation, runtime and networking mode;
- instrumentation and schema versions;
- chrony/clock status, offset, uncertainty and root dispersion;
- Recorder/compression/storage mode;
- strategy and capital assumptions when economics are compared.

The same bot build, config, market universe, subscriptions, feed mode, workload and observation protocol are required. A difference must be the intended treatment or explicitly modeled. Runs with invalid clocks, nonmatching event identity, changing workload or unrecorded tuning are not pooled as comparable evidence.

## Benchmark phases

### Phase A — screening

Initial duration: approximately 72 hours. Status: `INITIAL_PROTOCOL / CALIBRATABLE`. Purpose: remove clearly inferior/invalid candidates, expose clock/route/reliability problems and collect enough data to choose finalists.

### Phase B — finalists

Initial duration: approximately 7 days if needed. It covers P99.9 tails, time-of-day, route changes, market regimes, contention and stability. Duration may extend when sample count or regime coverage is inadequate.

The one-time Wave 1 research budget is approximately EUR 50–100. It is not a constitutional spending cap.

## Common statistical contract

Unless a benchmark defines otherwise, report count, valid/invalid count, P50, P90 when useful, P95, P99, P99.9 and maximum, plus time buckets and confidence/uncertainty. Percentiles without sample count and observation regime are incomplete. Average alone cannot drive selection.

Internal durations use monotonic time. Cross-machine arrival comparisons use synchronized wall time plus uncertainty. See [Clock and Measurement Contract](04_CLOCK_AND_MEASUREMENT_CONTRACT.md).

## B01 — First Market Data Arrival

- **Purpose:** identify which instance receives the same market event first and quantify lead/lag tails.
- **Inputs:** stable common event identity, market, exchange timestamp if usable, receive wall/monotonic timestamps, instance and clock quality.
- **Instrumentation:** record the earliest accepted receive timestamp before downstream processing on every candidate.
- **Measurement:** `Lead_i,j(e) = Recv_i(e) - Recv_j(e)`; negative means `i` received before `j`.
- **Statistics:** first-arrival win/loss/inconclusive rate; median lead/lag; P50/P90/P95/P99/P99.9 and worst tails by market/time/regime.
- **Confounders:** mismatched event identity, dropped events, reconnect state, different subscription timing, wall-clock steps, route changes.
- **Clock dependency:** strict; a lead not greater than combined uncertainty is inconclusive.
- **Validity:** same event and comparable healthy-feed state; clocks within policy; duplicate/reordered events handled consistently.
- **Artifact:** paired-event dataset, uncertainty flag and provider-pair summary.
- **Decision impact:** primary screening evidence for feed arrival, later translated through survival/economics.
- **Requirements:** `REQ-BENCH-0011`, `REQ-CLOCK-0015`, `REQ-INFRA-0075`.

## B02 — Feed Age

- **Purpose:** measure apparent age of received feed events.
- **Inputs:** receive time, exchange event time and documented exchange timestamp semantics.
- **Instrumentation:** capture raw exchange timestamp and local receive wall time without replacing either.
- **Measurement:** `FeedAge = RecvTime - ExchangeTime`.
- **Statistics:** P50/P95/P99/P99.9, invalid/negative observations and drift over time.
- **Confounders:** exchange batching/serialization, unknown timestamp origin, clock error, replay/snapshot events.
- **Clock dependency:** strict for absolute age.
- **Validity:** exchange timestamp meaning is externally verified and local uncertainty is acceptable.
- **Artifact:** distribution with timestamp-semantic version and uncertainty.
- **Decision impact:** feed-quality diagnostic; never overrules first-arrival when semantics are uncertain.
- **Requirements:** `REQ-BENCH-0012`, relevant clock/data-contract requirements.

## B03 — API / WebSocket RTT

- **Purpose:** measure realistic persistent-connection request/application response behaviour.
- **Inputs:** request start, first byte, response complete; WebSocket ping/pong identifiers/times where supported.
- **Instrumentation:** production-equivalent persistent TCP/TLS/WebSocket connections.
- **Measurement:** start-to-first-byte, start-to-complete and application ping/pong RTT separately.
- **Statistics:** P50/P95/P99/P99.9, jitter, timeout and error rates.
- **Confounders:** reconnect/TLS per request, server-side work, rate limits, mixed endpoints, client queueing.
- **Clock dependency:** monotonic local duration; no cross-host wall clock required.
- **Validity:** workload matches production connection reuse and endpoint semantics.
- **Artifact:** endpoint/connection-state RTT series and distribution report.
- **Decision impact:** network/order-path screening and degradation monitoring baseline.
- **Requirements:** `REQ-BENCH-0013` and API/WS external-register dependencies.

## B04 — Full Reconnect

- **Purpose:** measure recovery from lost connectivity to usable feed.
- **Inputs:** DNS, TCP, TLS, WS handshake, subscription and first-valid-event milestones.
- **Instrumentation:** monotonic timestamps at each transition and explicit health criteria.
- **Measurement:** `TimeToHealthyFeed` from reconnect start to first valid, subscribed, reconciled feed state; retain stage breakdown.
- **Statistics:** P50/P95/P99/P99.9, max, failure rate and failure stage.
- **Confounders:** cached DNS/session resumption, exchange outage, incomplete resubscription, stale first event.
- **Clock dependency:** local monotonic.
- **Validity:** health means operationally usable, not merely socket-open.
- **Artifact:** reconnect trace and stage/failure distribution.
- **Decision impact:** resilience and risk recovery evidence.
- **Requirements:** `REQ-BENCH-0014` plus feed/recovery requirements.

## B05 — Network Stability

- **Purpose:** characterize route and connection stability beyond median latency.
- **Inputs:** route/hops when observable, RTT series, packet loss, resets, reconnects and time buckets.
- **Instrumentation:** continuous low-impact probes plus application connection events.
- **Measurement:** route-change frequency, loss, RTT tails, reset/outage duration and time-of-day degradation.
- **Statistics:** P50/P95/P99/P99.9, loss/error rates, longest outage and regime/time buckets.
- **Confounders:** probe traffic differs from application traffic, ICMP policy, exchange incidents, maintenance.
- **Clock dependency:** local monotonic for durations; wall time for correlation.
- **Validity:** interpret probes with application evidence; do not rank from average ping.
- **Artifact:** route/network timeline and stability summary.
- **Decision impact:** technical screening, reliability and Risk baseline.
- **Requirements:** `REQ-BENCH-0015` and monitoring dependencies.

## B06 — Real Hot-Path CPU

- **Purpose:** measure actual decision workload, not a generic synthetic loop.
- **Inputs:** representative events/books/routes/config and stage timestamps.
- **Instrumentation:** `decode_ns`, `book_ns`, `route_lookup_ns`, `bbo_ns`, `l2_ns`, `risk_ns`, `decision_ns`, `total_ns`; Formula Book QF-084 decomposition remains authoritative.
- **Measurement:** receipt → decode → book → affected-route lookup → BBO → exact L2 walk → fees → risk → decision.
- **Statistics:** P50/P95/P99/P99.9/MAX per stage and total; throughput and queueing context.
- **Confounders:** different compiler/build, universe, market regime, logging, warmup, CPU frequency or tuning.
- **Clock dependency:** monotonic high-resolution local time.
- **Validity:** identical build/workload and representative warm steady state; instrumentation overhead measured.
- **Artifact:** versioned `LatencyTrace` dataset and stage distribution report.
- **Decision impact:** identifies actual compute limits and candidate CPU value.
- **Requirements:** `REQ-INFRA-0071`, QF-084 requirements and LatencyTrace contracts.

## B07 — Scheduler Jitter

- **Purpose:** quantify delayed scheduling/wakeup tails.
- **Inputs:** expected wake and actual wake monotonic times, CPU/run-state context.
- **Instrumentation:** periodic and workload-correlated wake probes.
- **Measurement:** `SchedulerDelay = ActualWake - ExpectedWake`.
- **Statistics:** P50/P99/P99.9/MAX, time-of-day and load buckets.
- **Confounders:** timer resolution, probe frequency, power states, instrumentation process placement.
- **Clock dependency:** local monotonic.
- **Validity:** comparable timer/probe configuration and recorded host load.
- **Artifact:** scheduler-delay time series and tail-event log.
- **Decision impact:** can reject a nominally faster CPU with unsafe tails.
- **Requirements:** `REQ-INFRA-0072`.

## B08 — CPU Contention

- **Purpose:** expose noisy neighbours and unstable CPU allocation.
- **Inputs:** utilization, effective frequency, steal time, context switches, run queue and time buckets.
- **Instrumentation:** host/container metrics correlated with latency traces.
- **Measurement:** contention indicators and their association with hot-path/jitter tails.
- **Statistics:** distributions, maxima, tail-event correlation and time-of-day patterns.
- **Confounders:** container visibility, provider metric semantics, power management and planned local workloads.
- **Clock dependency:** wall time for correlation; monotonic within samples where applicable.
- **Validity:** metrics correspond to the tested CPU scope and identical application load.
- **Artifact:** contention timeline/correlation report.
- **Decision impact:** distinguishes advertised CPU from stable usable compute.
- **Requirements:** `REQ-INFRA-0073`.

## B09 — Recorder Stress

- **Purpose:** quantify Recorder/compression/write interference.
- **Inputs:** engine-only baseline and engine + Recorder + compression + disk-write treatment.
- **Instrumentation:** identical trading workload; hot-path traces, recorder queue/backlog, CPU and disk metrics.
- **Measurement:** `RecorderPenalty = Latency_with_recorder - Latency_without_recorder`, evaluated distributionally and per stage.
- **Statistics:** P50/P95/P99/P99.9/MAX delta, backlog, loss/drop and throughput.
- **Confounders:** unequal events, cache state, compression settings, rotation/fsync schedule and disk throttling.
- **Clock dependency:** local monotonic.
- **Validity:** paired/comparable workloads and complete recorder accounting.
- **Artifact:** before/after trace distributions and RecorderPenalty report.
- **Decision impact:** approves co-location, demands isolation/tuning or rejects the profile.
- **Requirements:** `REQ-EXEC-0329` and Recorder/Data cross-domain requirements.

## B10 — Storage

- **Purpose:** ensure working storage sustains Recorder/recovery needs without hot-path disturbance.
- **Inputs:** representative record sizes/rates, compression, rotation and durability policy.
- **Instrumentation:** sequential write throughput, write/fsync latency, compression throughput and recorder backlog.
- **Measurement:** steady and burst behaviour with correlated hot-path traces.
- **Statistics:** throughput, write/fsync P50/P95/P99/P99.9, backlog peak/drain and penalty tails.
- **Confounders:** page cache, filesystem/mount, disk tier throttling, rotation and free-space state.
- **Clock dependency:** local monotonic.
- **Validity:** production-representative durability/settings; cache effects disclosed.
- **Artifact:** storage/backlog/latency report.
- **Decision impact:** validates working disk and interference, not maximum disk score.
- **Requirements:** `REQ-BENCH-0016` and storage/Recorder dependencies.

## B11 — RAM

- **Purpose:** validate memory capacity and safety margin for the real working set.
- **Inputs:** books, graph, routes, HOT/WARM/COLD, inventory, buffers, Recorder and metrics.
- **Instrumentation:** RSS, peak RSS, page faults, swap and memory-pressure events.
- **Measurement:** steady state, market/subscription peaks, recovery/reconnect and Recorder bursts.
- **Statistics:** RSS distributions/peak, fault rates, swap and pressure duration/count.
- **Confounders:** different allocator/build, lazy allocation, caches, universe and kernel/container accounting.
- **Clock dependency:** wall time for correlation; no cross-host timing dependency.
- **Validity:** realistic maximum supported workload and enough duration to reach stable/peak states.
- **Artifact:** memory profile and headroom decision.
- **Decision impact:** validates ~4 GB or justifies 8 GB+.
- **Requirements:** `REQ-INFRA-0074`.

## B12 — Docker Overhead

- **Purpose:** measure runtime/network isolation cost for the same engine/workload.
- **Inputs:** native and Docker treatments; bridge and host modes when approved for experiment.
- **Instrumentation:** HotPath, RTT, jitter and RecorderPenalty under identical build/config/resources.
- **Measurement:** native-versus-container deltas at P50/P99/P99.9 plus network/scheduler/storage effects.
- **Statistics:** paired distribution differences, confidence intervals and tail event counts.
- **Confounders:** unequal CPU/memory limits, filesystem, network mode, privileges, kernel or host load.
- **Clock dependency:** benchmark-specific rules above.
- **Validity:** only runtime mode changes; security implications recorded separately.
- **Artifact:** Docker overhead report and `OPEN-003` evidence.
- **Decision impact:** confirms Docker profile and informs bridge/host choice; no historical threshold is canonical.
- **Requirements:** `REQ-BENCH-0017`, `REQ-DEPLOY-0217` and Deployment dependencies.

## Technical screening heuristic

Historical weights are: feed arrival 25%, API/order network 20%, jitter/stability 10%, compute 15%, scheduler/contention 10%, operations 8%, cost 7%, storage 3%, reconnect/reliability 2%.

Status: `RESEARCH_HEURISTIC`. It may rank finalists but cannot become a Formula Book rule or replace NetPnL/uncertainty. Inputs must be normalized and missing/invalid metrics cannot silently score as zero or good.

## Infrastructure A/B methodology

Technical shadow comparison can observe the same market events. Live economic comparison must avoid simultaneous execution of the same opportunity from both machines when it would create self-competition or invalidate the counterfactual. Use a later validated assignment scheme such as alternating or randomized opportunities, while keeping opportunity universe, strategy and capital assumptions comparable.

## Tuning order

Run an untuned baseline first. Record every later tuning treatment and change only controlled variables. A provider that needs undocumented tuning is not comparable with its baseline. Lock-free structures, affinity, kernel/runtime/network changes and specialized NIC features are optimization candidates only after a measured bottleneck.

## Transition to economics

Phase A/B can identify technical finalists. Production change additionally requires shadow/counterfactual InfraLostPnL evidence, QF-084–QF-093 economic evaluation, uncertainty/LCB, and appropriate micro-live validation. Technical benchmark improvement alone never mandates upgrade.
