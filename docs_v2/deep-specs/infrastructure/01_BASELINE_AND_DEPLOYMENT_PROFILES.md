# 01 — Baseline and Deployment Profiles

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Decision frame

The baseline is the smallest architecture capable of producing valid production evidence without prematurely buying node, cluster, bare-metal or standby complexity. It is a starting hypothesis, not a promise that every machine with the advertised shape is valid.

## Initial topology

```text
Hyperliquid public feed
        |
        v
one Tokyo VPS
  - Rust trading engine
  - in-memory books/routes/risk state
  - Docker deployment
  - lightweight local Recorder when validated
  - local operational state/metrics
        |
        v
client-owned Hyperliquid account
```

There is no mandatory node, second server, cluster, bare metal, colocated service or external critical control plane. The bot must continue to enforce single-writer/account ownership rules defined by Deployment and Execution.

## Initial resource hypothesis

| Resource | Starting direction | What validates it | Failure signal |
|---|---|---|---|
| Region | Tokyo | First-arrival, RTT/tails, reconnect and economic comparison | Another region is materially better/current platform unavailable |
| CPU | ~2 stable fast vCPU | Real Hot-Path, Jitter, Contention and Recorder Stress | Tail growth, steal/run queue or throughput limit |
| RAM | ~4 GB | Real working-set benchmark | Swap, pressure, page-fault or peak-RSS risk |
| Disk | ~40–100 GB local NVMe | Recorder throughput, backlog, retention and recovery needs | Interference, low space or insufficient working horizon |
| OS | Linux/Ubuntu preferred, x86-64 | Deployment compatibility/security validation | Unsupported dependencies or invalid operations baseline |
| Runtime | Docker | Native/Docker overhead and deployment validation | Material performance or isolation failure |
| Cost | ~EUR 30–50/month | Candidate availability and NetPnL comparison | No valid candidate at that cost |

All approximate resource numbers are `CALIBRATED`.

## Tokyo-first contract

`TOKYO_FIRST` means:

- begin current infrastructure validation in Tokyo;
- preserve Tokyo candidate coverage in Wave 1;
- attach region to `InfraInstanceId` and `RunManifest`;
- test rather than assume route/arrival advantage.

It does not mean:

- hardcode Tokyo into trading logic or schemas;
- claim Tokyo is always closest to every relevant platform component;
- skip external availability verification;
- prevent later region benchmarks or migration.

## Provider and region abstraction

No trading, risk or accounting decision may depend on a provider-specific code branch. Provisioning adapters may contain provider details, while runtime contracts expose generic host, region, network, clock and resource measurements.

At minimum, `InfraInstanceId` identifies a materially distinct provider/region/offer/resource/runtime profile. A material change creates a new identity and invalidates transferred performance assumptions until revalidated.

## CPU contract

The hot path is latency-sensitive and primarily constrained by consistent real work, not aggregate synthetic throughput. Evaluation includes single-thread work, cache, effective frequency, scheduler tails, steal, context switches, run queue and contention.

No selection rule may treat advertised vCPU, GHz, dedicated labels, “HFT” names or peak synthetic scores as sufficient evidence. Two stable cores may beat eight noisy shared vCPU.

CPU affinity, isolation, priority and kernel tuning are hypotheses to benchmark and validate; they are not silently required by this pass.

## Memory contract

The realistic working set includes books, global graph, precomputed routes, HOT/WARM/COLD state, inventory, buffers, Recorder queues and metrics. The RAM benchmark records RSS, peak RSS, page faults, swap and pressure under realistic subscription and market load.

4 GB is acceptable only if the measured safety margin is adequate. 8 GB or more becomes justified when validated working-set, reliability or economics require it.

## Storage roles

### Production working storage

Local storage supports short-term Recorder output, write buffers, operational logs/state and restart/recovery artifacts. The lightweight 40–100 GB range is an initial hypothesis. Storage must not disturb the hot path.

### Research/archive storage

Raw-data archives, long replay corpora and derived datasets may require hundreds of GB or around 1 TB. They can live on a research machine or later archive tier. Their existence does not force the initial trading VPS to carry the same capacity.

Retention policy and permanent archive architecture belong to PASS 06. This spec only requires measurable throughput, backlog, free space and safe transfer/rotation boundaries.

## Network contract

Persistent production connections are the reference workload. Selection evidence includes event arrival, application RTT distributions, P99/P99.9, jitter, loss, route stability, resets and reconnect-to-healthy time. Average ICMP ping and advertised bandwidth are insufficient.

## Feed and Recorder

The initial feed is public Hyperliquid data through an abstraction that can later support a node or other valid feed. Books and routing state remain in memory. No disk access is permitted in the decision hot path.

The lightweight Recorder may share the initial host only when Recorder Stress shows acceptable tail interference and backlog. Otherwise it must be reduced, isolated or moved according to later Recorder/Deployment design.

## Docker role

Docker is the deployment direction because the client model needs reproducibility and isolation. It does not receive a performance exemption. The same build/workload is compared native versus Docker, and bridge versus host networking stays `OPEN-003` until measured and security-reviewed.

## Client isolation model

```text
one client
  -> one isolated VPS or server
  -> one bot/container deployment
  -> one signer/API wallet
  -> one client-owned account and capital base
```

No central multi-tenant execution engine or shared custody is implied. Provider independence allows the same approved image/profile to run on different supported hosts after validation.

## Conceptual deployment profiles

| Profile | Purpose | Indicative shape | Live status |
|---|---|---|---|
| `LOCAL / RESEARCH` | Development, replay, investigation | Developer-controlled; not standardized here | Not production by profile name |
| `TOKYO STANDARD` | Low-cost candidate baseline | ~2 vCPU, ~4 GB, light NVMe | Requires benchmark and Deployment validation |
| `TOKYO RECOMMENDED` | Stable production candidate | ~2 stable/dedicated fast vCPU, ~4–8 GB | Requires benchmark and Validation |
| `TOKYO PERFORMANCE` | Challenger when measured limitations exist | ~4 high-frequency/dedicated vCPU, ~8–16 GB | Requires positive incremental economics |

These profiles are not capital bands. Promotion depends on observed limits and economics.

## Machine change and validation

A provider, region, offer, CPU allocation, runtime network mode or other material profile change creates a new/changed `InfraInstanceId`. Before Live capability, run the appropriate diagnostic, clock check, feed/network tests, workload benchmark and validation matrix. The exact depth depends on the materiality policy owned by Validation.

## Locked, calibrated and open

### Locked

- one lightweight host is enough to start validation;
- public feed first and node not required initially;
- provider/region agnosticism at code level;
- Docker deployment direction;
- per-client isolation;
- no disk in the hot decision path;
- material host change requires revalidation;
- no automatic purchase or migration.

### Calibrated

- provider, region winner and cost;
- CPU/RAM/disk capacity;
- acceptable Recorder co-location;
- Docker overhead;
- profile validation limits;
- internal compute KPI targets.

### Open

- `OPEN-001` final provider ranking;
- `OPEN-002` final region;
- `OPEN-003` Docker bridge versus host;
- `OPEN-011` final storage/retention capacity.

## Requirement anchors

Primary anchors include `REQ-INFRA-9001`, `REQ-CLIENT-9001`, `REQ-INFRA-0056`–`REQ-INFRA-0060`, `REQ-INFRA-0088`, `REQ-INFRA-0093`–`REQ-INFRA-0095`, and the deployment/client requirements mapped in the PASS 01 ledger.
