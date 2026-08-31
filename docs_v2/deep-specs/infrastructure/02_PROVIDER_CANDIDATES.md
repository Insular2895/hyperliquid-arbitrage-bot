# 02 — Provider Candidates

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Evidence status

Every commercial value below is a historical `SOURCE_SNAPSHOT` from SRC-008. PASS 01 deliberately performed no live provider research. Plan names, prices, resource allocations, OS availability, Tokyo availability, dedicated/shared semantics, network claims, billing and trials require external revalidation before purchase or deployment.

The table explains why a candidate entered the protocol. It does not rank current providers.

## Historical candidate table

| Provider | Offer | Role | Wave | CPU | RAM | Storage | OS | Network claims | Dedicated/shared context | Historical price snapshot | Advantages | Risks | Benchmark question | Current status | External revalidation | Source requirement IDs |
|---|---|---|---:|---|---|---|---|---|---|---|---|---|---|---|---|---|
| TradingFXVPS | Advanced / standard trading VPS | Cheap trading-oriented challenger | 1 | 2 cores, AMD Ryzen 9, ~4.3 GHz | 4 GB DDR5 | 40 GB NVMe | Hyper-V/Windows context; Linux support open | 10 Gbps, IPv4 | Exact allocation/noise context unknown | ~$33.75/month annual-equivalent | Low price; advertised high-frequency CPU; trading-oriented operations | Windows/runtime mismatch; shared-host jitter; marketing not Hyperliquid evidence | Can the cheapest trading-branded offer meet Linux, arrival, hot-path and stability needs? | `SOURCE_SNAPSHOT`; candidate | YES: all commercial fields and Ubuntu/Linux support in Tokyo | `REQ-INFRA-0061`, `REQ-INFRA-0070` |
| TradingFXVPS | Standard HFT | Higher trading-oriented Wave 1 challenger | 1 | 4 cores, ~4.3 GHz+ | 8 GB DDR5 | 50 GB NVMe | Windows snapshot | Fibre Cross Connect; 10GbE SolarFlare | Exact allocation/noise context unknown | ~$63.75/month annual-equivalent | More CPU/RAM; premium network stack claims | Forex-specific ~0.3 ms marketing is not Hyperliquid evidence; OS and marginal value unknown | What measurable Hyperliquid value does the incremental price buy versus Advanced? | `SOURCE_SNAPSHOT`; candidate | YES: plan, price, region, OS, SolarFlare and network claims | `REQ-INFRA-0062`, `REQ-INFRA-0070`, `REQ-EXEC-0333` |
| TradingFXVPS | Semi-Dedicated | Future capacity/performance challenger | Much later | ~10 Ryzen cores, ~4.3 GHz | 32 GB DDR5 | 2 × ~200 GB NVMe RAID1 | Historical provider context | 10 Gbps | Semi-dedicated claim | ~$165.84/month annual-equivalent | More isolation, memory and storage | Premature cost/complexity; unclear incremental capture value | Is cheaper infrastructure proven CPU/jitter/resource-limited enough to justify it? | `FUTURE_GATE`; not initial | YES: entire plan and availability | `REQ-INFRA-0063` |
| TradingFXVPS | HFT Dedicated | Premium/node/research challenger | Much later | Ryzen 9950X class, ~5.5 GHz+ | 192–256 GB DDR5 | 2 × 2 TB NVMe RAID1 | Historical provider context | 2 × 10 Gbps | Dedicated claim | ~$525+/month | Large compute/memory/storage; possible node/research host | Large fixed cost; overprovisioning; operational concentration | Can it recover enough robust incremental PnL or support a justified node/research role? | `FUTURE_GATE`; not initial | YES: plan, price, hardware, region and network | `REQ-INFRA-0064` |
| Akamai / Linode | G7 Dedicated CPU | Conventional Linux dedicated-CPU comparator | 1 | 2 vCPU | 4 GB | 80 GB | Linux | 4 TB transfer | Dedicated CPU label | ~$43/month; ~$0.06/hour | Mature cloud, hourly billing, Linux and claimed dedicated CPU | Current Tokyo stock/specs/routes unknown | Does a conventional dedicated Linux CPU provide better stability/value than trading-branded VPS? | `SOURCE_SNAPSHOT`; candidate | YES: offer, region, billing, resource and allocation claims | `REQ-INFRA-0065` |
| Kamatera | Type B | Economic reserved-resource comparator | 1 | 2 vCPU | 4 GB | 20 GB NVMe | Ubuntu 24.04 snapshot | Not relied upon | Source says dedicated thread/reserved resources; must verify | ~$39/month | Linux baseline; economic; claimed stability | Small disk; exact CPU reservation and Tokyo offer uncertain | Is the reservation claim real/current and does it reduce jitter enough at low cost? | `SOURCE_SNAPSHOT`; candidate | YES: dedicated/reserved semantics, OS, price and availability | `REQ-INFRA-0066` |
| AWS | Lightsail Compute Optimized | Mainstream-cloud route/stability comparator | 1 | 2 vCPU | 4 GB | 160 GB SSD | Linux context | 5 TB transfer | Current compute allocation semantics unknown | ~$42/month | Mature operations, large disk, Tokyo cloud presence | Weak inference from unrelated node placement; no evidence of API colocation | Does the measured Hyperliquid path outperform without assuming platform colocation? | `SOURCE_SNAPSHOT`; candidate | YES: plan, price, AZ/region, allocation and any Hyperliquid relationship | `REQ-INFRA-0067` |
| Sakura | VPS Tokyo | Local Japanese economic challenger | 1 | 4 virtual vCPU | 4 GB | 200 GB SSD | Current support not asserted | Not relied upon | Shared CPU concern | ~¥3,630/month annual-equivalent; ~¥3,960 monthly | Low local price; large disk; local provider | Scheduler jitter, contention and trial/current terms unknown | Does low-cost local hosting retain stable CPU and network tails across time of day? | `SOURCE_SNAPSHOT`; candidate | YES: price, trial, resources, shared context and availability | `REQ-INFRA-0068` |
| Cherry Servers | Performance VDS | Performance Linux challenger | 2 if required | Ryzen 7950X; 4 vCores; roughly 2 physical-core allocation context | 16 GB | 200 GB NVMe | Ubuntu 24.04 snapshot | 3 Gbps | Dedicated-resources claim | ~$104.13/month; ~$88.51 annual-equivalent | Strong Linux CPU/RAM reference without immediate bare metal | Higher price; allocation/current Tokyo stock uncertain | Do measured CPU/jitter gains recover more value than incremental cost? | `SOURCE_SNAPSHOT`; not baseline | YES: all plan, allocation, price, OS and Tokyo facts | `REQ-INFRA-0069` |
| Vultr | Unspecified Tokyo dedicated candidate | Additional market comparator | 2 if required | Not specified in source | Not specified | Not specified | Not specified | Not specified | Not specified | Not specified | Broadens comparison if Wave 1 inconclusive | No source-backed commercial details | Is there a current comparable Tokyo offer worth a controlled run? | `OPEN`; no invented specification | YES: discover and record a dated snapshot before inclusion | `REQ-INFRA-0101` |
| GCP | Unspecified Tokyo candidate | Hyperscaler comparator | 2 if required | Not specified in source | Not specified | Not specified | Not specified | Not specified | Not specified | Not specified | Alternative routing/operations baseline | No source-backed offer or placement evidence | Does a current Tokyo configuration merit benchmark on measured path/stability? | `OPEN`; no invented specification | YES: select a current comparable offer before inclusion | `REQ-INFRA-0101` |
| OCI | Unspecified Tokyo candidate | Hyperscaler comparator | 2 if required | Not specified in source | Not specified | Not specified | Not specified | Not specified | Not specified | Not specified | Alternative pricing/routing baseline | No source-backed offer details | Does a current Tokyo configuration merit benchmark? | `OPEN`; no invented specification | YES: select and snapshot before inclusion | `REQ-INFRA-0101` |

## Wave rules

### Wave 1

TradingFX Advanced, TradingFX Standard HFT, Akamai/Linode G7, Kamatera Type B, AWS Lightsail Compute Optimized and Sakura VPS are the initial screening set, subject to current availability and comparability. Revalidation may remove or replace an unavailable offer without changing the benchmark purpose.

### Wave 2 if required

Cherry, Vultr, GCP, OCI and other current Tokyo dedicated candidates enter only if Wave 1 is inconclusive or demonstrates a specific limitation needing a stronger comparator. No unspecified Wave 2 machine receives invented specs.

### Much later

Semi-Dedicated, HFT Dedicated, bare metal, node infrastructure and colocation-style options require demonstrated resource limitation and robust positive incremental economics.

## Why compare TradingFX Advanced and Standard HFT

They form a direct marginal-value experiment inside one provider family. The decision is not whether HFT marketing sounds stronger, but whether the higher price produces reproducible Hyperliquid improvements in arrival, CPU/scheduler tails, RecorderPenalty, stability and finally net economics.

A small technical gain can be uneconomic. A meaningful tail/reliability gain can be valuable even when median improvement is small. Both require the same workload and clock-valid comparison.

## Selection and rejection

Technical screening can eliminate invalid candidates. It cannot alone select production. Final selection applies the QF-084–QF-093 economic framework, uncertainty and validation evidence.

Reject or suspend a candidate when:

- current facts cannot be confirmed;
- Linux/runtime/deployment requirements cannot be met;
- clocks or measurements are invalid;
- persistent feed/order connectivity is unreliable;
- CPU, memory, disk or Recorder interference is unsafe;
- it is technically inferior on comparable evidence;
- incremental value cannot robustly cover incremental cost.

## External verification boundary

External verification must happen immediately before benchmark rental and again before a purchase/renewal decision if facts could have changed. Evidence should record retrieval date, official URL/document, currency/tax/billing basis and exact offer identifier. Until then the historical facts remain useful only as candidate provenance.
