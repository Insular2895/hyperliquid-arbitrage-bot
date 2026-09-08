# Sequencing and Priority Fact Audit

`EXTERNAL SNAPSHOT: 2026-09-08`

## Separate mechanisms

| Mechanism | Verified fact | Not established |
|---|---|---|
| network/gossip priority | node operators can enable gossip-auction priority ordering; default mempool stream order is random | client-selected per-order paid priority or guaranteed propagation lead |
| validator processing | official nonce docs say ALO-only batches receive validator priority | deterministic order versus IOC/GTC/cancel, spot fill advantage or exact cost |
| inclusion/block position | committed blocks have order, and mempool data is pre-commit | user control or deterministic inclusion guarantee |
| book matching | official HyperCore book uses price-time priority | gossip/inclusion priority jumping worse price or earlier same-price book priority |
| rate-limit reservation | buys API request capacity | exchange sequencing/matching priority |
| HyperEVM priority fee | applies to EVM transactions | V1 HyperCore spot order entry |

## Timing interpretation

Local send latency measures the client boundary. Response/ACK latency combines delivery and server processing; it is not fill or pure sequencing. Fill latency includes market/matching conditions. QF-084 retains an exchange component but CORR-04 adds no new decomposition formula.

No current official user-facing numeric/paid per-order priority field for the V1 spot API-wallet path was verified. No deterministic cancel-before-IOC, ALO-before-IOC, order inclusion or matching improvement is claimed. Any future experiment must revalidate scope and compare identical conditions while recording request, block/order position if authoritative, ACK/status/fill, completion, cost and uncertainty.
