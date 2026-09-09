# Sequencing and Priority Fact Audit

`CURRENT FACT ADDENDUM: 2026-09-09 — SUPERSEDES THE 2026-09-08 ABSENCE CLAIM`

| Mechanism | Current official fact | Boundary |
|---|---|---|
| gossip/read priority | recurring independent on-chain slot auction; configured peers may prioritize normal and split client-block data | each hop may ignore it; peer topology creates variance; not order matching |
| `split_client_blocks` | uncommitted mempool transactions, no responses, eagerly propagated; all path peers must enable | `NON-CANONICAL`; random order by default unless configured for auction ordering |
| IOC write priority | eligible all-IOC non-outcome group; 0–8 bps changes effective temporal preference, higher rates supply similar-time tie-break behavior | cancels remain ahead of executable orders; no fill guarantee |
| ALO write priority | eligible all non-reduce-only ALO non-outcome group; sorts within a documented 400 ms recent price-level tail | no IOC-style mempool priority; charge at placement whether filled or not |
| cancel / ALO / IOC | latency guide says cancel and ALO sent at comparable time almost always execute before IOC/GTC; cancels are explicit first class in IOC ordering | empirical/documented scope, not universal deterministic route completion |
| matching | price/queue mechanics still apply | priority cannot cross price or bypass Risk/protection |
| rate-limit reservation | purchases request capacity | not sequencing priority |
| HyperEVM gas | EVM transaction mechanism | not HyperCore spot order priority |

Read and write priority are distinct typed treatments. `RX→SEND` alone does not determine effective liquidity survival. Experiments record policy, eligibility, source version, actual ordering/ACK/fill evidence, costs, uncertainty and outcome provenance. See [CORR-06 current fact audit](../corr06_final_consistency/CURRENT_HYPERLIQUID_PRIORITY_AND_SEQUENCING_AUDIT.md).
