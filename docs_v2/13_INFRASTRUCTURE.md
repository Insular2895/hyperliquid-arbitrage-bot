# 13 — Infrastructure

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Purpose

This document is the canonical domain master for the bot's infrastructure. It defines the initial deployment direction, the evidence required to select or change infrastructure, the interaction with risk, and the boundaries delegated to the Infrastructure deep specs and later domain passes.

The domain goal is not maximum advertised hardware performance. It is maximum robust net trading value under measured latency, reliability, risk and cost.

## Scope

PASS 01 covers:

- initial host and deployment profile;
- Tokyo-first validation without region hard-coding;
- historical provider candidates and benchmark waves;
- CPU, memory, network, storage and Docker measurement;
- clock and cross-machine measurement contracts;
- infrastructure economics, upgrade and downgrade;
- public-feed-first and future node escalation;
- infrastructure health outputs for Risk;
- resilience, recovery and client diagnostics.

This pass does not redefine the Formula Book, Risk Constitution, Data Contracts, Recorder policy, Deployment policy, Validation Matrix, execution state machine or Market Participants model. Their closure sources remain authoritative.

## Status vocabulary

| Status | Meaning in this domain |
|---|---|
| `LOCKED` | Project invariant supported by closure or latest uncontradicted source. |
| `CALIBRATED` | Mechanism is required; values, windows or thresholds must be measured and versioned. |
| `OPEN` | A decision cannot be made from the current evidence. |
| `SOURCE_SNAPSHOT` | Historical provider/platform claim preserved for provenance, not asserted as current. |
| `FUTURE_GATE` | Architecture remains compatible, but activation requires explicit evidence and validation. |

## Locked principles

1. Infrastructure code is provider-agnostic and region-agnostic.
2. Tokyo is the first region to validate, not a permanent claim of optimality.
3. Select infrastructure from comparable measurement of the real workload, not advertised vCPU count, GHz, bandwidth or trading branding.
4. Use monotonic time for elapsed durations. Cross-machine comparisons require synchronized wall time plus clock quality and uncertainty.
5. Public Hyperliquid feed is the initial source; the feed interface remains compatible with future alternatives.
6. A Hyperliquid node is not required at launch.
7. Technical improvement alone does not mandate an upgrade. Incremental net economic value and uncertainty govern.
8. Upgrade and downgrade are symmetric decisions. Sunk cost is irrelevant.
9. Capital alone never selects an infrastructure tier.
10. Infrastructure health is a Risk input. An unsafe state forbids new risk according to the Risk Constitution.
11. Recorder, compression, metrics and disk work must not materially disturb the trading hot path.
12. Client execution is isolated per client; no central multi-tenant execution SaaS is assumed.
13. The product may diagnose and recommend infrastructure actions, but it must not automatically buy, migrate or upgrade infrastructure.
14. Reproducible cold recovery precedes hot standby unless downtime economics justify the latter.
15. No historical example or target becomes a universal threshold without calibration evidence.

## Initial baseline

The source-derived starting hypothesis is:

| Component | Initial direction | Status |
|---|---|---|
| Topology | One VPS, no cluster and no mandatory second server | `LOCKED` initial scope |
| Region | Tokyo first | `CALIBRATED`; benchmark against alternatives when needed |
| Cost | Roughly EUR 30–50/month | Initial research target, not a cap |
| OS | Linux, Ubuntu preferred | Initial direction; exact supported release validated by Deployment |
| Architecture | x86-64 preferred | Initial direction |
| Runtime | Docker | Deployment authority applies |
| CPU | Approximately two stable, fast vCPU; dedicated/reserved preferred when economical | `CALIBRATED` |
| RAM | Approximately 4 GB | `CALIBRATED` against realistic working set |
| Local disk | Approximately 40–100 GB NVMe | Lightweight working-storage hypothesis |
| Feed | Public Hyperliquid feed through an abstraction | `LOCKED` initial direction |
| Engine | Rust trading engine | Architecture direction |
| Recorder | Lightweight local recorder if interference benchmark is acceptable | `CALIBRATED` |
| Node | None required initially | `LOCKED` |
| Bare metal | None required initially | `LOCKED` |

The numbers are not customer guarantees. A machine becomes valid only after the applicable deployment, benchmark and validation gates.

## Deployment storage versus research storage

The project has two legitimate storage roles:

- **production working storage**: local short-horizon event buffer, recorder queue, logs, state and operational artifacts; the 40–100 GB baseline is a starting hypothesis;
- **research/archive storage**: longer raw-data retention, replay corpora and derived datasets; hundreds of GB or approximately 1 TB may be reasonable outside the trading VPS.

The roles must not be collapsed. Production disk size is derived from measured recorder throughput, retention and recovery objectives. Research/archive sizing belongs to the Recorder/Data pass. This resolves `CONFLICT-003` without deleting either source context.

## Tokyo first, not Tokyo forever

Tokyo is the first deployment and benchmark direction because the source research selected it as the initial hypothesis. It is not encoded into trading logic, feed interfaces, persistence schemas or decision rules. Provider, region and route are RunManifest/InfraInstance metadata.

A different region may replace Tokyo if current platform availability or comparable measurements show better arrival quality, tails, reliability or net economics. `OPEN-002` remains open until current facts and benchmark evidence exist.

## CPU philosophy

Two stable fast cores can outperform eight noisy shared vCPU for this workload. Selection must evaluate:

- real single-thread hot-path distributions;
- cache and working-set behaviour;
- effective frequency stability;
- scheduler delay and tail latency;
- steal time, context switches and run queue;
- noisy-neighbour and time-of-day contention;
- Recorder and compression interference.

Advertised GHz, core count or “HFT” branding is not selection evidence.

## Network philosophy

Advertised 10 Gbps is not the primary performance KPI. The relevant evidence is event arrival quality, persistent connection behaviour, RTT tails, jitter, packet loss, route stability, reconnect time and first valid event after recovery.

Average ping alone is insufficient. The benchmark reports P50, P95, P99 and P99.9 where sample volume supports them, plus maxima/tail events and time-of-day/regime context.

## Provider benchmark waves

Wave 1 screens the source-backed initial candidates:

- TradingFXVPS Advanced;
- TradingFXVPS Standard HFT;
- Akamai/Linode G7 Dedicated;
- Kamatera Type B;
- AWS Lightsail Compute Optimized;
- Sakura VPS Tokyo.

Wave 2 is opened only if Wave 1 cannot answer the decision or a performance bottleneck requires stronger challengers:

- Cherry Performance VDS;
- Vultr;
- GCP;
- OCI;
- other current Tokyo dedicated candidates.

Much later, and only behind economics and validation gates: TradingFX Semi-Dedicated, TradingFX HFT Dedicated, bare metal, node infrastructure or colocation-style infrastructure.

All prices, plan names, resource claims, regions and trials are historical `SOURCE_SNAPSHOT` facts requiring external revalidation before spending or deployment. See [Provider Candidates](deep-specs/infrastructure/02_PROVIDER_CANDIDATES.md).

## Benchmark phases

The conceptual benchmark tool is `hl-infra-benchmark`: the same workload and build run across candidates. PASS 01 specifies it but does not implement it.

### Phase A — screening

Approximately 72 hours per candidate is the initial protocol. It eliminates clearly inferior candidates and catches obvious route, clock, CPU, feed or reliability problems. The duration is calibratable, not constitutional.

### Phase B — finalists

Approximately 7 days when needed. It observes P99.9 tails, jitter, route changes, time-of-day effects, market regimes and operational stability. A short ping test cannot select the production provider.

The approximate one-time screening budget of EUR 50–100 is a research plan, not a permanent cap.

## Run comparability

Comparative runs require the same:

- bot build and Git revision;
- configuration and market universe;
- subscriptions and feed mode;
- workload and instrumentation;
- observation protocol;
- strategy and capital assumptions for economic comparison.

Every run is attributable to a `RunManifest` and `InfraInstanceId`, including provider, region, instance profile, OS/kernel, runtime/network mode, CPU characteristics and clock health. Invalid or materially different runs are not pooled without an explicit normalization decision.

## Twelve required benchmarks

| # | Benchmark | Primary decision evidence |
|---:|---|---|
| 1 | First Market Data Arrival | Relative event arrival wins and lead/lag distributions with clock uncertainty. |
| 2 | Feed Age | Receive time minus exchange time when timestamp semantics and clock quality permit. |
| 3 | API / WebSocket RTT | Persistent-connection request and application ping/pong distributions. |
| 4 | Full Reconnect | DNS through subscriptions to first valid event; `TimeToHealthyFeed`. |
| 5 | Network Stability | Route change, packet loss, RTT tails, resets and time-of-day degradation. |
| 6 | Real Hot-Path CPU | Receipt through decode, book, route, L2, fees, risk and decision. |
| 7 | Scheduler Jitter | Actual wake minus expected wake distributions and maxima. |
| 8 | CPU Contention | Utilization, effective frequency, steal, context switches and run queue. |
| 9 | Recorder Stress | Engine-only versus engine + recorder/compression/writes; `RecorderPenalty`. |
| 10 | Storage | Write/fsync/compression/backlog behaviour and hot-path isolation. |
| 11 | RAM | Real working set, RSS/peak, faults, swap and memory pressure. |
| 12 | Docker Overhead | Native versus Docker; bridge versus host remains empirical/open. |

The full validity and artifact contract is in [Benchmark Protocol](deep-specs/infrastructure/03_BENCHMARK_PROTOCOL.md).

## Clock contract summary

`chrony` is the initial synchronization direction. Hosts expose or record `clock_offset`, `clock_uncertainty`, `root_dispersion` and the observation timestamp.

- internal elapsed time: monotonic nanoseconds;
- comparable wall event time: synchronized wall clock plus uncertainty;
- cross-machine result whose magnitude does not exceed combined uncertainty: inconclusive;
- first-arrival result without stable event identity: invalid;
- Feed Age without known exchange timestamp semantics: diagnostic or invalid, never overclaimed.

The Data Contracts closure is authoritative. See [Clock and Measurement Contract](deep-specs/infrastructure/04_CLOCK_AND_MEASUREMENT_CONTRACT.md).

## Technical screening versus final selection

The historical screening heuristic weights feed arrival 25%, API/order network 20%, jitter/stability 10%, compute 15%, scheduler/contention 10%, operations 8%, cost 7%, storage 3% and reconnect/reliability 2%. It is a `RESEARCH_HEURISTIC` for finalist screening, not a Formula Book rule or the final production objective.

Technically faster does not imply economically better. Final selection uses comparable trading PnL, trading costs, infrastructure cost, stability, risk and uncertainty.

## Latency, survival and economics

Infrastructure latency matters because an edge can disappear before execution:

```text
Latency distribution
  + Edge Survival S(t)
  -> P_capture
  -> capturable opportunity set
  -> realized PnL
  -> infrastructure economics
```

PASS 01 owns measured infrastructure latency and the required interface, including the `OpportunitySurvival` dependency. PASS 02 owns the detailed competition and survival model.

## Canonical formulas

Infrastructure uses the Formula Book closure `QF-084` through `QF-093`:

- `QF-084`: latency decomposition;
- `QF-085`: `P_capture,s = E_{L_s}[S(L_s)]`;
- `QF-086`: incremental gross PnL on the same opportunity universe/assumptions;
- `QF-087`: incremental infrastructure cost;
- `QF-088`: `NetUpgradeValue = ΔGrossPnL - ΔCost`;
- `QF-089`: `InfraROI = ΔGrossPnL / ΔCost` only when `ΔCost > 0`;
- `QF-090`: net PnL after trading and infrastructure costs, without double-counting;
- `QF-091`: lower-confidence-bound upgrade gate with calibrated `alpha` and safety factor;
- `QF-092`: `InfraEfficiency = NetPnL / InfraCost`, diagnostic only;
- `QF-093`: aggregate CaptureRatio from sums, never a naïve mean of per-opportunity ratios.

The precise transcriptions and interpretation boundaries are in [Infrastructure Economics and ROI](deep-specs/infrastructure/05_INFRA_ECONOMICS_AND_ROI.md). Formula changes belong to PASS 11.

## InfraLostPnL and RecoverablePnL

`InfraLostPnL` is first-class evidence of opportunities lost to late data, network/compute delay, scheduler jitter, feed degradation, reconnect or outage. It is recorded through `InfraLostPnLRecord` where the Data Contract defines it.

Attribution must avoid double counting. Sequential marginal attribution is preferred when multiple causes coexist. Estimation remains calibrated/model-derived; it must retain model version, uncertainty and evidence provenance.

`RecoverablePnL` is the defensible portion expected to be recovered by a candidate, not total modeled loss and never an automatic promise.

## Upgrade pipeline

```text
Current infrastructure
  -> measure limitation / InfraLostPnL
  -> prove infrastructure is limiting
  -> rent candidate
  -> comparable technical benchmark
  -> shadow/counterfactual estimate
  -> estimate ΔGrossPnL and uncertainty
  -> compare ΔCost through LCB/ROI gate
  -> micro-live validation
  -> upgrade only if robust net economic value is positive
```

Live A/B evaluation must not execute the same opportunity simultaneously from two servers when that creates self-competition. Assignment may alternate or randomize under a later validated experiment design.

## Downgrade pipeline

The same comparison runs in reverse. If the robust incremental advantage of a premium machine is below its incremental cost, the cheaper validated machine is preferred. Previous rent, setup effort and other sunk costs do not alter the forward decision.

## Capital is not an infrastructure trigger

More capital does not imply an automatic upgrade. Drivers may include validated capacity, opportunity density, capture loss, InfraLostPnL, recoverable PnL, risk/stability and economic ROI. Large idle capital alone justifies nothing. No universal capital-to-server bands are canonical. This resolves `CONFLICT-008`.

## Public feed and node gate

The initial system consumes the public feed through a feed abstraction. It is node-compatible, not node-dependent. This resolves `CONFLICT-002`.

A node is evaluated only when evidence shows public-feed quality materially limits capturable PnL and a node candidate may recover enough value after cost, uncertainty, reliability and operational burden. No economic case means no node.

If justified later, the studied topology separates a fast/stable trading engine machine from a larger node machine. One client deployment does not imply one expensive node per client. Node features, resource requirements, output semantics and region recommendations all require external revalidation. See [Node, Feed and Scale Gates](deep-specs/infrastructure/06_NODE_FEED_AND_SCALE_GATES.md).

## Infrastructure health and Risk

`InfrastructureMonitor` produces an `InfraState` consistent with the Risk Constitution: `HEALTHY`, `DEGRADED` or `UNSAFE`. Inputs include feed age, API RTT, jitter, loss, CPU/scheduler state, recorder health, clock health and WebSocket connectivity.

- `HEALTHY`: infrastructure does not independently restrict permissions;
- `DEGRADED`: permissions reduce according to Risk policy;
- `UNSAFE`: no new risk; recovery/reconciliation actions only as allowed by the execution state machine.

Exact thresholds and windows are calibrated, versioned and provenance-bearing. Conceptual alerts include `FEED_STALE`, `CLOCK_UNSYNCED`, `CPU_JITTER_HIGH`, `RECORDER_BACKLOG_HIGH`, `DISK_LOW`, `NETWORK_P99_DEGRADED`, `WS_RECONNECT_LOOP` and `INFRA_UNSAFE`; final names belong to the Operations/contract authority.

## Rolling model and monitoring outputs

Short horizons govern immediate safety; long horizons support economics. Source examples such as 5m, 15m, 1h, 6h, 24h, 7d and 30d are calibrated examples, not locked windows.

Infrastructure exposes feed age, relative arrival, compute/sign/API/send/ack/fill distributions, scheduler jitter, steal/frequency, loss/reconnects, clock quality, memory, disk and recorder backlog. PASS 10 owns the complete observability and alert operations design.

## Client model and diagnostics

Commercial direction:

```text
one client -> one isolated VPS/server -> Docker -> one bot
           -> one signer/API wallet -> client-owned account/capital
```

Conceptual profiles are `LOCAL/RESEARCH`, `TOKYO STANDARD` and `TOKYO PERFORMANCE`. Indicative resource shapes are approximately 2 vCPU/4 GB for Standard, 2 stable fast vCPU/4–8 GB for Recommended, and 4 high-frequency/dedicated vCPU/8–16 GB for Performance. Only benchmark and validation evidence turns a profile into a supported requirement.

`botctl benchmark` or the approved equivalent evaluates CPU, scheduler, memory, disk, clock, feed, API RTT, network and Docker behaviour. It may return validated/degraded/rejected semantics aligned with Deployment, Risk and Validation. It may recommend `KEEP CURRENT INFRA`, `BENCHMARK UPGRADE` or `DOWNGRADE CANDIDATE`; it never purchases a VPS or migrates funds.

A material `InfraInstanceId` change requires appropriate revalidation before Live capability.

## Resilience and backup economics

Initial resilience prioritizes reproducible images, provisioning, configuration backup, automated redeployment, restart reconciliation and single-writer safety. A second VPS is not automatic.

Hot standby is future-gated by expected downtime loss versus incremental backup cost and operational risk. If activated, it must prevent split brain and dual active trading with the same account/signer. Deployment and Execution authorities define ownership and failover permissions.

## Calibrated aspects

- final provider and region;
- exact CPU/RAM/storage profiles;
- Phase A/B duration when evidence requires adjustment;
- clock-health limits;
- infrastructure-health thresholds and rolling windows;
- Docker bridge versus host networking;
- acceptable RecorderPenalty;
- internal compute KPI targets;
- `alpha`, safety factor and exact LCB method;
- InfraLostPnL and RecoverablePnL estimators;
- node and standby activation economics.

Historical P50 200–300 microseconds and P95 below approximately 500 microseconds are design hypotheses only, not guarantees.

## Open decisions

| Open item | Decision evidence required |
|---|---|
| `OPEN-001` | Controlled ranking of current providers. |
| `OPEN-002` | Current platform facts and region benchmark. |
| `OPEN-003` | Native/bridge/host Docker experiment plus security review. |
| `OPEN-004` | Valid distributions and Risk calibration for health limits. |
| `OPEN-005` | Formula/validation choice for `alpha`, safety factor and LCB. |
| `OPEN-006` | Public-feed limitation, node capability, reliability and ROI evidence. |
| `OPEN-011` | Measured Recorder throughput and retention objectives. |
| `OPEN-015` | Operations pass choice of telemetry/export backend. |

## External revalidation

Before any provider purchase or deployment decision, revalidate plan availability, price, billing, resources, dedicated/shared semantics, OS, region and network claims. Before node or platform integration, revalidate Hyperliquid feed/API/node capabilities, timestamp semantics, rate limits and software requirements.

These checks do not block documentary reconstruction; they block treating historical snapshots as current deployment facts.

## Deep specs

- [Infrastructure deep-spec index](deep-specs/infrastructure/README.md)
- [Baseline and Deployment Profiles](deep-specs/infrastructure/01_BASELINE_AND_DEPLOYMENT_PROFILES.md)
- [Provider Candidates](deep-specs/infrastructure/02_PROVIDER_CANDIDATES.md)
- [Benchmark Protocol](deep-specs/infrastructure/03_BENCHMARK_PROTOCOL.md)
- [Clock and Measurement Contract](deep-specs/infrastructure/04_CLOCK_AND_MEASUREMENT_CONTRACT.md)
- [Infrastructure Economics and ROI](deep-specs/infrastructure/05_INFRA_ECONOMICS_AND_ROI.md)
- [Node, Feed and Scale Gates](deep-specs/infrastructure/06_NODE_FEED_AND_SCALE_GATES.md)
- [Operations, Resilience and Client Diagnostics](deep-specs/infrastructure/07_OPERATIONS_RESILIENCE_AND_CLIENT_DIAGNOSTICS.md)

## Traceability

PASS 01 reviewed 514 Infrastructure-relevant requirements against original source locators. The evidence is in [Infrastructure Requirement Ledger](_analysis/pass01_infrastructure/INFRA_REQUIREMENT_LEDGER.md), including cross-domain requirements deliberately routed to future passes.
