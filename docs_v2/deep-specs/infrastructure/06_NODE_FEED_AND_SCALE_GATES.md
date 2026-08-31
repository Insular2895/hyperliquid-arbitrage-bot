# 06 — Node, Feed and Scale Gates

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Canonical initial decision

The initial trading deployment uses the public Hyperliquid feed through a provider-neutral feed abstraction. The architecture is compatible with a future node feed, but no Hyperliquid node is required at launch.

This resolves `CONFLICT-002`: earlier node-oriented research remains useful as future design context, while SRC-006 deployment direction and latest SRC-008 infrastructure synthesis govern the initial topology.

## Feed abstraction

Downstream book, route, simulation, Risk and decision components consume a normalized feed contract rather than public-feed- or node-specific code. A feed adapter is responsible for:

- connection/subscription lifecycle;
- snapshot/incremental reconciliation;
- event identity, ordering and duplicate semantics;
- receive wall/monotonic timestamps and clock quality;
- raw source metadata and adapter version;
- health, gap, stale and reconnect state;
- normalized events without erasing raw provenance.

The abstraction must not pretend feeds are semantically identical. Capability/semantic differences remain explicit and validated before a new adapter can drive Live.

## Why public feed first

- It supports the lightweight one-VPS baseline.
- It avoids node resource, reliability, upgrade and operations burden before evidence of need.
- It allows strategy/Recorder/validation evidence to develop without conflating node complexity.
- It enables measurement of actual public-feed limitation rather than assuming it.
- It preserves a low-cost client model.

Public feed first is not a claim that the public feed is always optimal. It is the correct evidence-generating initial condition.

## What is externally unstable

Before implementation/deployment, revalidate:

- current public API/WS endpoints, subscriptions, snapshots and reconnect rules;
- cadence, event fields, identities, ordering and timestamp semantics;
- current node installation/resource/region recommendations;
- node flags, outputs, reliability and supported markets;
- `order_book_server` or equivalent L2/L4/spot capabilities;
- SDK/library support, versions and rate limits.

PASS 01 does not use current internet claims to close these facts.

## Evidence of public-feed limitation

A node study begins only when valid evidence links public-feed quality to material capture loss. Evidence can include:

- relative first-arrival disadvantage against a credible alternative;
- stale/gapped feed intervals and reconnect impact;
- model-derived opportunity survival loss attributable to feed arrival;
- `InfraLostPnLRecord` evidence with controlled attribution;
- counterfactual/replay/shadow estimates with uncertainty;
- inability to meet safety/reliability objectives after simpler fixes.

High capital, competitor anecdotes, node availability or marketing latency are not sufficient.

## Node escalation gate

```text
measure public-feed limitation
  -> validate attributable InfraLostPnL
  -> identify a current node/feed candidate
  -> revalidate capabilities and operational burden
  -> benchmark node feed under comparable event/clock contract
  -> estimate candidate RecoverablePnL
  -> compare incremental cost and uncertainty
  -> validate reliability, Risk and recovery
  -> activate only after robust positive economics and approval
```

No material limitation or no economic case means `NO NODE`.

## Node benchmark

The node candidate is compared with the public feed on:

- common-event first arrival with clock uncertainty;
- event completeness, ordering, duplicates and gap/recovery behaviour;
- Feed Age only where timestamp semantics allow;
- downstream book consistency and usable-event latency;
- outage/restart/catch-up behaviour;
- CPU, memory, disk and network resource consumption;
- operational incidents and maintenance burden;
- incremental capturable/realized PnL and uncertainty.

Raw first byte is not sufficient if the event cannot safely update the book or if completeness/recovery is worse.

## Future topology

If justified, preserve the studied separation:

```text
SERVER A — TRADING
  fast/stable compute
  trading engine and signer boundary

       authenticated low-latency feed link

SERVER B — NODE
  larger CPU/RAM/storage/network profile
  node lifecycle and feed adapter
```

The lightweight trading VPS is not silently expanded into a heavy combined host. Combined versus separated topology would itself require benchmark, failure and security analysis.

The link becomes a new dependency: it needs clock/latency measurement, authentication, backpressure, health, reconnection and failure semantics. A node that adds an unreliable network hop may not improve usable capture.

## Client distribution boundary

The commercial model is one isolated client deployment per client/account. It does not imply one node per client. Any future shared node/feed service changes trust, availability, network, security, licensing, tenancy and product architecture and therefore requires explicit later design and validation.

No shared central execution or custody follows from node compatibility.

## Premium and bare-metal escalation

Premium VPS, dedicated server, bare metal or colocation-style infrastructure follows the same gate as any upgrade:

- prove a measured resource/network limitation;
- select a current comparable candidate;
- establish technical improvement on real workload;
- translate it to RecoverablePnL/risk benefit;
- clear cost, uncertainty and validation.

“HFT”, specialized NIC, many cores, 10 Gbps or proximity claims do not bypass the gate. SolarFlare, kernel bypass, lock-free queues, CPU isolation and similar techniques remain research/tuning candidates until a measured bottleneck and safe benefit exist.

## Node health and Risk

A future node feed must expose the same minimum health contract as public feed plus node-specific sync/catch-up/version/resource state. Unsafe or unverified node output cannot drive new risk. Fallback to public feed is not automatic unless feed consistency, book resynchronization and execution-state transition are explicitly validated.

## Rollback

Node activation must preserve a validated rollback path to the prior feed/topology. Rollback evidence includes configuration/version, book resynchronization, duplicate/gap handling, risk state and `InfraInstanceId`/feed identity change. Economic downgrade rules also apply if the node advantage does not persist.

## Open items

- `OPEN-006`: future node activation;
- current node and order-book-server capabilities: external revalidation;
- exact public/node live experimental design;
- combined versus separated topology only if a node gate is reached;
- product model for any shared node service.

## Requirement anchors

`REQ-NODE-0001`–`REQ-NODE-0003`, `REQ-INFRA-0057`, `REQ-INFRA-0058`, `REQ-INFRA-0088`, `CONFLICT-002`, `EXT-005`–`EXT-007`, and public-feed/node dependencies mapped in the PASS 01 ledger.
