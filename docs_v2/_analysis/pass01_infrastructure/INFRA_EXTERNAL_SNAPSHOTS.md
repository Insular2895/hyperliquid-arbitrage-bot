# PASS 01 — Infrastructure External Snapshots

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

No live external validation was performed during PASS 01. Values are preserved exactly enough to explain historical candidate selection. `YES` in the revalidation column means the value must not be treated as current.

## Provider and commercial facts

| Fact | Source | Historical value | Why it matters | External revalidation required | When to revalidate | Blocks current documentation? |
|---|---|---|---|---|---|---|
| TradingFXVPS Advanced resources | SRC-008 / `REQ-INFRA-0061` | 2 Ryzen 9 cores ~4.3 GHz; 4 GB DDR5; 40 GB NVMe; 10 Gbps; IPv4 | Defines cheap trading-oriented challenger | YES | Before Wave 1 rental/purchase | NO |
| TradingFXVPS Advanced OS/virtualization | SRC-008 / `REQ-INFRA-0061` | Hyper-V/Windows context; Ubuntu/Linux support open | Can determine deployability | YES | Before candidate admission | NO |
| TradingFXVPS Advanced price | SRC-008 / `REQ-INFRA-0061` | ~$33.75/month annual-equivalent | Sets historical cost comparator | YES | Before economic comparison | NO |
| TradingFXVPS Standard HFT resources/network | SRC-008 / `REQ-INFRA-0062` | 4 cores ~4.3 GHz+; 8 GB DDR5; 50 GB NVMe; Fibre Cross Connect; 10GbE SolarFlare; Windows | Defines marginal challenger | YES | Before Wave 1 rental | NO |
| TradingFXVPS Standard HFT price | SRC-008 / `REQ-INFRA-0062` | ~$63.75/month annual-equivalent | Required for `ΔCost` | YES | Before economic comparison | NO |
| TradingFX latency marketing | SRC-008 | ~0.3 ms toward some Forex counterparties | Must not be mistaken for Hyperliquid evidence | YES | Only if used in candidate rationale; never substitute benchmark | NO |
| TradingFX Semi-Dedicated | SRC-008 / `REQ-INFRA-0063` | ~10 Ryzen cores; 32 GB DDR5; 2 × ~200 GB NVMe RAID1; 10 Gbps; ~$165.84/month annual-equivalent | Future capacity challenger | YES | If future gate opens | NO |
| TradingFX HFT Dedicated | SRC-008 / `REQ-INFRA-0064` | Ryzen 9950X class ~5.5 GHz+; 192–256 GB DDR5; 2 × 2 TB NVMe RAID1; 2 × 10 Gbps; ~$525+/month | Future premium/node/research candidate | YES | If future gate opens | NO |
| Akamai/Linode G7 Dedicated | SRC-008 / `REQ-INFRA-0065` | 2 vCPU; 4 GB; 80 GB; 4 TB; ~$43/month / ~$0.06/hour; Tokyo/APAC claim | Conventional Linux dedicated comparator | YES | Before Wave 1 rental | NO |
| Kamatera Type B | SRC-008 / `REQ-INFRA-0066` | 2 vCPU; 4 GB; 20 GB NVMe; Ubuntu 24.04; ~$39/month | Economic Linux comparator | YES | Before candidate admission/rental | NO |
| Kamatera CPU reservation | SRC-008 / `REQ-INFRA-0066` | Dedicated thread/reserved resource claim | Central to expected jitter stability | YES | Before candidate admission | NO |
| AWS Lightsail Compute Optimized | SRC-008 / `REQ-INFRA-0067` | 2 vCPU; 4 GB; 160 GB SSD; 5 TB; ~$42/month | Mainstream-cloud comparator | YES | Before Wave 1 rental | NO |
| AWS/Hyperliquid placement inference | SRC-008 / `REQ-INFRA-0067` | Foundation non-validating node reportedly in `apne1-az1`; no API-colocation conclusion | Explains weak benchmark rationale only | YES | Before repeating any placement claim | NO |
| Sakura VPS Tokyo | SRC-008 / `REQ-INFRA-0068` | 4 virtual vCPU; 4 GB; 200 GB SSD; ~¥3,630 annual-equivalent / ~¥3,960 monthly | Local Japanese economic challenger | YES | Before Wave 1 rental | NO |
| Sakura trial | SRC-008 | Historical trial information | May reduce screening cost | YES | Before budgeting/rental | NO |
| Cherry Performance VDS | SRC-008 / `REQ-INFRA-0069` | Ryzen 7950X; 4 vCores/~2 physical-core context; 16 GB; 200 GB NVMe; 3 Gbps; Ubuntu 24.04; ~$104.13 / ~$88.51 annual-equivalent | Wave 2 performance comparator | YES | If Wave 2 opens | NO |
| Vultr/GCP/OCI Tokyo offers | SRC-008 / `REQ-INFRA-0101` | Candidate names only; no canonical specs | Prevents invented Wave 2 configurations | YES | Before selecting an offer for Wave 2 | NO |
| Currency/tax/billing basis | All provider snapshots | Historical source presentation | Needed for comparable `ΔCost` | YES | At every economic study | NO |

## Hyperliquid and software facts

| Fact | Source | Historical value | Why it matters | External revalidation required | When to revalidate | Blocks current documentation? |
|---|---|---|---|---|---|---|
| Public feed endpoints/subscriptions | SRC-002/006/008; `EXT-002`, `EXT-005` | Historical API/WS behaviour | Feed adapter and reconnect implementation | YES | Before implementation/integration test/deployment | NO |
| Public feed cadence/fields/event identity | SRC-002/007/008; `EXT-005` | Historical semantics | First-arrival pairing and book validity | YES | Before benchmark implementation | NO |
| Exchange timestamp semantics | SRC-002/007/008 | Historical/uncertain | Feed Age validity | YES | Before using absolute Feed Age | NO |
| Node requirements/flags/outputs | SRC-002/007/008; `EXT-006` | Historical studied node profile | Node feasibility and operations | YES | If node study opens | NO |
| Node region recommendation | SRC-002/007/008; `EXT-006` | Historical recommendation context | Node placement | YES | Before node benchmark/design | NO |
| `order_book_server` L2/L4/spot support | SRC-002/007/008; `EXT-007` | Historical repository capability claims | Feed capability and strategy coverage | YES | Before depending on any capability | NO |
| Rate limits / scheduleCancel | SRC-004/006/008; `EXT-008` | Historical exchange rules | Benchmark safety and execution operations | YES | Before integration/live validation | NO |
| SDK/library versions/support | SRC-002/006; `EXT-015` | Historical versions/status | Build and deployment compatibility | YES | During implementation planning | NO |
| Ubuntu/runtime supported releases | Provider sources/SRC-006 | Historical versions | Deployment/security baseline | YES | Before client image support commitment | NO |

## Revalidation evidence contract

Future verification should prefer official provider/platform documents and record retrieval date, URL/document identifier, exact offer, region, currency, tax and billing commitment. A verified fact may enter canonical deployment evidence only after reviewer validation; until then it remains a dated external record.

None of these facts blocks reconstructing architecture, benchmark method or decision gates. They can block admitting a candidate, implementing timestamp-dependent metrics, purchasing infrastructure or enabling a node.
