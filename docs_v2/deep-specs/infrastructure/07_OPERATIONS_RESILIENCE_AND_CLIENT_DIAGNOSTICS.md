# 07 — Operations, Resilience and Client Diagnostics

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Boundary

This spec defines Infrastructure outputs and failure behaviour. PASS 10 owns the complete Operations/Monitoring implementation and alert-routing policy. SRC-005 Risk/Data closure and SRC-006 Deployment/Validation closure remain authoritative.

## InfrastructureMonitor contract

`InfrastructureMonitor` consumes versioned observations and produces an `InfraSnapshot`/`InfraState` suitable for Risk, Operations, benchmark and economics consumers.

Minimum input families:

- feed freshness, gaps, arrival quality and connection state;
- API/WebSocket RTT and errors;
- reconnect stages and `TimeToHealthyFeed`;
- hot-path, sign, send→ack and send→fill distributions where available;
- scheduler jitter, CPU utilization/frequency/steal/context switches/run queue;
- packet loss, route changes and network tails;
- clock offset, uncertainty, root dispersion and sync health;
- memory, pressure, faults and swap;
- write/fsync latency, free disk and Recorder queue/backlog;
- runtime/container and `InfraInstanceId` identity.

Observations retain event/run/config/model provenance and validity state. Missing is not healthy and is not silently converted to zero.

## InfraState and Risk

The Risk Constitution supplies the canonical state meanings:

| State | Infrastructure meaning | Permission consequence |
|---|---|---|
| `HEALTHY` | Required infrastructure signals are valid and within calibrated policy | No additional infrastructure restriction |
| `DEGRADED` | Quality/reliability is impaired but controlled operation may remain possible | Risk policy reduces or restricts permissions |
| `UNSAFE` | Infrastructure cannot support safe new risk | No new risk; recovery/reconciliation only as allowed |

Infrastructure does not independently invent a trading permission. It supplies evidence/state; Risk and the execution state machine decide permitted actions.

Examples that may lead to degradation/unsafe state: stale/gapped feed, unhealthy clock, extreme network/scheduler tails, reconnect loop, recorder failure/backpressure threatening the engine, resource exhaustion or loss of exchange connectivity.

## Thresholds and hysteresis

Exact thresholds, windows, hold times, hysteresis and recovery evidence are `CALIBRATED` (`OPEN-004`). They are versioned parameters with provenance, not magic numbers embedded in code/docs.

Recovery to healthier state should require sustained valid evidence and any necessary book/account reconciliation; one good sample does not erase an unsafe interval.

## Rolling horizons

Use multiple horizons with distinct purposes:

- fast/minutes: immediate safety and incident detection;
- recent/hours: persistent degradation and local trend;
- medium/day-week: provider stability, regime and operations review;
- long/weeks-month: infrastructure economics and upgrade/downgrade evidence.

Source examples 5m, 15m, 1h, 6h, 24h, 7d and 30d are calibratable examples. The Operations/Risk calibration selects actual windows.

## Alert concepts

| Conceptual alert | Evidence | Immediate consumer |
|---|---|---|
| `FEED_STALE` | Feed freshness/gap outside policy | Risk, feed recovery, Operations |
| `CLOCK_UNSYNCED` | Clock unhealthy/uncertainty too high | Risk, benchmark invalidation, Operations |
| `CPU_JITTER_HIGH` | Scheduler/hot-path tail degradation | Risk/Operations |
| `RECORDER_BACKLOG_HIGH` | Queue/backlog threatens loss or interference | Recorder/Operations; Risk if material |
| `DISK_LOW` | Free space/retention safety margin insufficient | Operations/Recorder |
| `NETWORK_P99_DEGRADED` | Sustained tail/route/loss deterioration | Risk/Operations/economics |
| `WS_RECONNECT_LOOP` | Repeated failure to reach healthy feed | Risk/recovery/Operations |
| `INFRA_UNSAFE` | Aggregated state forbids new risk | Risk/execution/Operations |

Names are conceptual unless closure contracts define exact enums. Alert payloads include state, evidence window, threshold/config version, instance/run, first/last seen and recommended operator action.

## Client diagnostic

`botctl benchmark` or an approved equivalent runs before Live on a new/materially changed host and on operator request. It tests:

- CPU hot-path and scheduler consistency;
- memory working set and pressure;
- storage/Recorder throughput/interference;
- clock synchronization and uncertainty;
- feed connectivity, freshness and reconnect;
- persistent API/WS RTT and network stability;
- Docker/runtime overhead/configuration;
- required Deployment/security prerequisites.

The result is an `INFRA_PROFILE`-like artifact aligned with Deployment/Validation, including:

- `InfraInstanceId`, build/config and observation interval;
- test versions and raw artifact links;
- pass/degraded/rejected findings per capability;
- invalid/unmeasured items;
- supported operational mode/profile;
- revalidation expiry/trigger;
- operator-facing remediation.

Final status names must match the closure contracts rather than this conceptual wording.

## Recommendations and authority

Based on validated evidence, the product may report:

- `KEEP CURRENT INFRA`;
- `BENCHMARK UPGRADE`;
- `DOWNGRADE CANDIDATE`;
- collect more evidence / infrastructure unsafe.

It must not automatically purchase or cancel hosting, migrate funds/accounts/signers, change region/provider, or authorize Live. Client/operator retains infrastructure choice; Deployment/Validation and economic gates still apply.

## Material change and revalidation

Material `InfraInstanceId` changes include provider/region/offer/machine, CPU allocation, OS/kernel, runtime/network mode and other performance-relevant changes. The diagnostic and appropriate benchmark/validation run before Live capability.

Routine reboot on unchanged identity can still require clock/feed/book/account health and reconciliation before Live, even if it does not create a new identity.

## Recorder and disk operations

The Recorder must remain non-blocking relative to the hot path under its closure policy. Infrastructure observes queue/backlog, write/fsync/compression, disk free and `RecorderPenalty`.

When pressure rises, behaviour follows Recorder/Risk/Operations authority; Infrastructure does not invent data dropping or trading continuation policy. Local NVMe is working storage/short-term buffer, not automatically the permanent research archive.

## Cold recovery baseline

Before requiring a second VPS, maintain:

- reproducible, versioned Docker image;
- reproducible provisioning/configuration with secrets kept outside images;
- backups of persistent configuration/state under Deployment policy;
- automated redeployment procedure;
- clock/feed/account/book reconciliation before new risk;
- explicit owner/signer/single-writer verification;
- recovery drill evidence and measured recovery time.

Cold recovery is “cheap first,” not “uncontrolled.” Recovery that can start a stale or duplicate writer is invalid.

## Backup economics

A backup host is justified when the robust expected loss avoided by improved recovery/availability exceeds incremental backup and operational risk/cost. The source discusses `ExpectedDowntimeLoss` conceptually; PASS 01 does not promote an exploratory formula into the Formula Book.

The comparison includes outage frequency/duration, recoverable opportunity loss, restart/reconciliation time, backup rent, maintenance/testing burden and split-brain/security risk.

## Future hot standby

Hot standby is a `FUTURE_GATE`. Before activation it requires:

- explicit leader/ownership and single-active-writer mechanism;
- signer/account safety and no dual active trading;
- fencing/lease/failover semantics robust to partition;
- state/feed/book/account synchronization and reconciliation;
- tested failover and failback;
- monitoring/alerting and operator override;
- positive economic case under uncertainty.

No “start both and hope one wins” design is allowed. Deployment and Execution authority owns final mechanics.

## Failure tests

At minimum validate scenarios applicable to the chosen profile:

- feed stale/gap and malformed/reordered recovery;
- WebSocket/API disconnect and reconnect loop;
- clock loss/offset/uncertainty deterioration;
- CPU contention and scheduler tail injection;
- recorder queue growth, disk latency and disk-low;
- process/container/host restart;
- network loss/route degradation;
- incomplete state/account reconciliation;
- standby partition/fencing failures if standby exists.

Each test records expected state/permission, observed state, recovery criteria, artifacts and unresolved deviations.

## Periodic report

The source-backed monthly/periodic infrastructure report concept includes:

- health/degradation/unsafe time by cause;
- feed/RTT/reconnect/hot-path/scheduler/clock/Recorder distributions and trend;
- significant incidents and recovery evidence;
- current provider cost and reliability;
- CaptureRatio/InfraLostPnL/RecoverablePnL model/version summaries;
- current-versus-candidate or downgrade evidence;
- recommendation with confidence and open actions.

Exact cadence, backend and alert routing belong to PASS 10 (`OPEN-015`).

## Split-brain prevention

Any backup/failover topology must preserve one active owner/writer for the same account/signer. On ambiguous ownership or partition, safety wins: no new risk until ownership and account state are reconciled under closure policy.

## Open items

- `OPEN-004`: health thresholds/windows/hysteresis;
- `OPEN-011`: retention/storage capacities;
- `OPEN-015`: telemetry/export backend;
- backup/hot-standby economics and mechanism;
- final diagnostic status schema and revalidation depth.

## Requirement anchors

`REQ-INFRA-0091`, `REQ-INFRA-0095`, `REQ-INFRA-0096`, `REQ-INFRA-0099`, `REQ-OPS-0019`–`REQ-OPS-0023`, `REQ-RISK-0329`, `REQ-CLIENT-0025`–`REQ-CLIENT-0028`, `REQ-CLIENT-9001`, SRC-005 risk/data contracts and SRC-006 deployment/validation requirements mapped in the PASS 01 ledger.
