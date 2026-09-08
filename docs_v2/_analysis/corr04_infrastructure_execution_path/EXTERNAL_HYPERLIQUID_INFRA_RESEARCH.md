# External Hyperliquid Infrastructure Research

`EXTERNAL_REVALIDATION_SNAPSHOT — retrieved 2026-09-08`

## Method and limits

Official Hyperliquid documentation and the official `hyperliquid-dex` GitHub organization are primary. Linux kernel, Docker, IETF, DPDK and F-Stack primary materials cover general transport/host questions. Absence of documented FIX or per-order paid priority is an evidence result, not proof that a private interface cannot exist. Every current fact must be revalidated before implementation or activation.

Local source snapshots used for reproducibility:

- `hyperliquid-dex/node` commit `405cc08b17a727ee51b0f9128918955a84439915` (2026-08-10);
- `hyperliquid-dex/order_book_server` commit `8b4f237904f683aca2dba21a07d87e831ead2a97` (2026-07-15).

## Claim ledger

`Direct quote locator` is the inspected section/line anchor, not a reproduced quotation.

| Fact ID | Claim | Official source / URL | Retrieval date | Software/doc version or commit | Direct quote locator | Interpretation | Current? | Hyperliquid-specific? | V1 relevance | Status | Requires future revalidation? |
|---|---|---|---|---|---|---|---|---|---|---|---|
| `HF-001` | Official node roles are validator and non-validator. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README “System Requirements” | V1 research uses non-validator; validator duties are out of scope. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-002` | Published minimums: validator 32 cores/128 GB/1 TB SSD; non-validator 16 cores/128 GB/500 GB SSD; Ubuntu 24.04 only. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README lines 5–12 | A 4 GB trading VPS cannot be assumed to host a node. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-003` | Gossip ports 4001/4002 must be public or peers may deprioritize the node. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README lines 10–12 | Node deployment expands firewall/attack-surface obligations. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-004` | Default node output can generate roughly 100 GB/day of logs. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README “Outputs”, line 91 | Storage/rotation/Recorder interference are material. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-005` | Nodes expose transaction blocks/state snapshots plus optional trades, fills, statuses, raw book diffs and related streams. | [Node repository](https://github.com/hyperliquid-dex/node), [L1 schemas](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/nodes/l1-data-schemas) | 2026-09-08 | `405cc08…`; live docs | README “Outputs/Flags”; schema headings | Richer coverage does not grant canonical authority. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-006` | Output batching/streaming/immediate-flush flags alter timing/shape; immediate flushing increases disk I/O. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README lines 138–145 | Build/flags belong to feed/interference identity. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-007` | Local `--serve-info` is a subset: no historical queries/WebSockets and no `l2Book`. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README “Local server” | A local node is not a drop-in public API replacement. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-008` | Official latency guidance recommends reliable peer/immediate flushing and at least 32 logical cores plus 500 MB/s disk throughput. | [Optimizing latency](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/optimizing-latency) | 2026-09-08 | live docs | “Optimizing latency” node guidance | Latency guidance is not economic proof. | yes | yes | high | `CURRENT_GUIDANCE` | yes |
| `HF-009` | `order_book_server` is standalone/non-core/as-is, may be insecure/incompatible, lacks spot books and batches by block. | [order_book_server](https://github.com/hyperliquid-dex/order_book_server) | 2026-09-08 | `8b4f237…` | README disclaimer/limitations | It cannot close V1 spot L4 or safety. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-010` | Foundation non-validator access is best effort, unguaranteed and unsuitable as the sole authoritative time-sensitive trading source. | [Foundation node](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/nodes/foundation-non-validating-node) | 2026-09-08 | live docs | warning/terms section | Warning scope is Foundation service; all node sources still require qualification. | yes | yes | high | `CURRENT_WARNING` | yes |
| `HF-011` | Public WebSocket offers `l2Book`, `bbo`, trades and account/order subscriptions with channel-specific snapshots. | [WebSocket subscriptions](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/websocket/subscriptions) | 2026-09-08 | live docs | subscriptions table/types | Public input remains initial canonical adapter contract. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-012` | Orders use HTTP `/exchange` or WebSocket post; response/ACK is not fill or route completion. | [Exchange endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/exchange-endpoint), [WS post](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/websocket/post-requests) | 2026-09-08 | live docs | action/response sections | Existing ESM outcome truth stays authoritative. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-013` | Current TIF values include ALO/IOC/GTC and client order IDs are supported. | [Exchange endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/exchange-endpoint) | 2026-09-08 | live docs | order action fields | No relative action-order guarantee is inferred. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-014` | Nonces are signer-scoped with rolling set/time limits; separate API wallets per process/subaccount are recommended. | [Nonces/API wallets](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/nonces-and-api-wallets) | 2026-09-08 | live docs | nonce rules/recommendations | Reinforces one owner/signer isolation. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-015` | ALO-only batches receive documented validator priority relative to mixing ALO with IOC/GTC. | [Nonces/API wallets](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/nonces-and-api-wallets) | 2026-09-08 | live docs | batching note | Not a user numeric paid priority or deterministic fill guarantee. | yes | yes | medium | `CURRENT_FACT_LIMITED_SCOPE` | yes |
| `HF-016` | HyperCore book matching uses price-time priority. | [Order book](https://hyperliquid.gitbook.io/hyperliquid-docs/hypercore/order-book) | 2026-09-08 | live docs | matching description | Gossip/inclusion priority does not jump price-time priority. | yes | yes | high | `CURRENT_FACT` | yes |
| `HF-017` | `split_client_blocks: true` streams uncommitted mempool transactions without responses; all peers in path must enable it. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README lines 551–555 | Explicitly speculative/non-canonical. | yes | yes | research | `CURRENT_FACT` | yes |
| `HF-018` | Mempool streaming order is random by default; node operators can enable gossip-auction priority ordering. | [Node repository](https://github.com/hyperliquid-dex/node) | 2026-09-08 | `405cc08…` | README line 555 | Gossip configuration is not book priority or client guarantee. | yes | yes | research | `CURRENT_FACT` | yes |
| `HF-019` | Rate-limit reservation purchases request capacity, not documented transaction sequencing priority. | [Rate limits](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/rate-limits-and-user-limits) | 2026-09-08 | live docs | reserve request weight | Do not price it as order priority. | yes | yes | medium | `CURRENT_FACT` | yes |
| `HF-020` | HyperEVM gas priority fees are distinct from HyperCore spot order entry. | [Using HyperEVM](https://hyperliquid.gitbook.io/hyperliquid-docs/onboarding/how-to-use-the-hyperevm) | 2026-09-08 | live docs | transaction fee guidance | No transfer to V1 spot semantics. | yes | yes | high | `NOT_APPLICABLE_TO_V1_SPOT` | yes |
| `HF-021` | No current official FIX order-entry interface was found; documented order transports are HTTP/WebSocket. | Official docs and repositories linked above | 2026-09-08 | live docs + pinned repos | site/repository FIX search | Reject FIX for current V1, without claiming a private interface cannot exist. | no positive support found | yes | high | `NOT_CURRENT / REJECTED_FOR_V1` | yes |
| `HF-022` | No user-facing paid/numeric per-order priority control was found for the V1 spot API-wallet path. | Official docs and node repository linked above | 2026-09-08 | live docs + `405cc08…` | priority/fee/order field search | Keep economic hook future-only; no Formula/Risk use. | not verified | yes | high | `NOT_CURRENTLY_VERIFIED` | yes |

## Node fact questions A–O

| Question | Evidence-backed answer |
|---|---|
| A — variants | Validator and non-validator. CORR-04 studies non-validator only. |
| B — non-validator data | Committed transaction blocks/state-derived outputs plus optional trades, fills, statuses, raw book diffs, misc/system outputs and limited local info requests, according to enabled flags. |
| C — committed/final | Block-indexed `replica_cmds` and resulting block outputs are committed HyperBFT observations; one-block finality applies to committed blocks, not mempool data. Exact field finality remains schema-specific. |
| D — pre-commit | The `mempool_txs` stream from `split_client_blocks` is explicitly uncommitted and has no responses. |
| E — sole execution authority | No. Actual order/fill/account truth remains canonical exchange/account evidence plus Execution/Reconciliation. Foundation access is explicitly unsuitable as a sole time-sensitive source. |
| F — warnings | Heavy resources/log volume, public gossip ports, peer topology, catch-up/lag, software/flag drift, limited local info server, `order_book_server` disclaimer/no spot support, and Foundation best-effort caveat. |
| G — hardware | Published minimum non-validator 16 cores/128 GB/500 GB SSD; latency guidance recommends at least 32 logical cores and 500 MB/s disk throughput. |
| H — bandwidth/storage | No universal bandwidth number is documented in the inspected material; ports and route/peer quality matter. Default logs can approach 100 GB/day. Measure actual ingress/egress and retention. |
| I — software | Ubuntu 24.04 only at the inspected node commit; `hl-visor` manages the current node binary. |
| J — sync | A non-validator connects to configured/root peers and applies streamed blocks; peer/config/build identity is required evidence. |
| K — lag/resync | `applied block` progress, local-vs-L1 timestamps, output gaps and catch-up must be monitored. During lag/resync the source is unhealthy and cannot drive new canonical risk. Exact resync behavior needs implementation-time verification. |
| L — local endpoints/streams | Files under `~/hl/data`, optional local `/info` subset on port 3001, optional EVM RPC, plus `mempool_txs` when explicitly configured. Local `/info` is not WebSocket and lacks `l2Book`. |
| M — overlap | Trades, order/fill/status information and reconstructable book information overlap conceptually with public channels, but encoding/cadence/ordering can differ. |
| N — semantic differences | Node block/stream outputs expose block context/raw diffs and optional uncommitted mempool data; public WebSocket emits channel snapshots/updates. Arrival, grouping, IDs and knowledge time differ. |
| O — one-to-one alignment | Not guaranteed by current public documentation. Use a shared authoritative ID when present; otherwise a strict semantic fingerprint plus ambiguity rejection. Nearest timestamps are never enough. |

## Priority questions A–M

| Dimension | Current disposition |
|---|---|
| validator/node gossip priority | Exists as current node-operator configuration for gossip-auction ordering. |
| user-facing per-order priority | No arbitrary paid/numeric control verified for V1 spot. ALO-only batching priority is documented but narrower. |
| spot availability | Price-time matching applies; no separate user paid-priority spot field verified. |
| inclusion/order/matching effect | Gossip ordering and ALO batch treatment may affect propagation/processing; no deterministic inclusion, relative action order or fill effect is claimed. Matching remains price-time. |
| fee, asset, charge time | Unknown/not applicable because no V1 per-order paid mechanism was verified. |
| client control | Clients control batching/TIF; node operators control the inspected gossip setting. Neither is an arbitrary priority-price request. |
| API-wallet path | No paid priority control verified. |
| deterministic guarantee | None found for the effect CORR-04 would need. |
| measurability | Possible only in a later controlled experiment after semantics and scope are revalidated. |

## Research stop condition

Primary sources answered the material architecture questions. Remaining gaps concern unpublished topology, real measured latency/capture, provider-specific behavior and future software changes; more generic web material would not close them. They therefore remain benchmark/revalidation items rather than inferred facts.
