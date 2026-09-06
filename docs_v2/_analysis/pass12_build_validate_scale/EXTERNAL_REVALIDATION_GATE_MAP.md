# PASS 12 — External Revalidation Gate Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

No external fact was revalidated during PASS 12. This map routes current-fact checks to the existing external register and the future implementation/activation owner.

| External fact family | Technical phases affected | Shadow blocked if stale? | Micro-live blocked? | Live blocked? | Revalidation owner |
|---|---|---|---|---|---|
| Hyperliquid market/asset metadata and status | 2, 5, 6, 16 | Affected semantic claim yes | Yes | Yes | Adapter + Metadata owner |
| Price validity, tick/significant-figure rules | 5, 7, 9, 13 | Conformance Shadow yes | Yes | Yes | Precision/Formula owner |
| Size, lot, minimum quantity/notional rules | 5, 7, 9, 17 | Conformance Shadow yes | Yes | Yes | Precision/Sizing owner |
| Fee schedule, tier, debit asset and maker/taker treatment | 5, 7, 18, 20, 23–26 | Economic Shadow yes | Yes | Yes | Fee/Accounting owner |
| Order types and IOC/GTC/ALO/Post-Only semantics | 12–14, 18, 20, 22–23 | Transport Shadow yes | Yes | Yes | Execution owner |
| Price protection/marketability/cancel semantics | 12–14, 18, 20, 23 | Yes | Yes | Yes | Execution/Risk owner |
| API wallet, signing/auth and permission scope | 13, 20, 23 | Signer integration yes | Yes | Yes | Security/Execution owner |
| Nonce, CLOID/OID lookup, idempotence and batching/order | 12–14, 20, 23 | Yes | Yes | Yes | Execution/Reconciliation owner |
| WebSocket/account events, sequence/timestamp/snapshot/diff behavior | 2–5, 8, 13–14 | Yes | Yes | Yes | Data/Adapter owner |
| Public/node feed behavior, L2/L4/order-book-server support | 2–4, 18, 21–23, 26 | Feature-dependent | Maker/node modes yes | Maker/node modes yes | Data/Infra owner |
| Supported Linux/Docker/runtime/security baseline | 19–20, 26 | Host readiness yes | Yes | Yes | Deployment/Security owner |
| Provider/network/node commercial/current capability facts | 19–20, 26 | Benchmark admission | Only affected profile | Yes for affected profile | Infrastructure owner |

An unverified fact blocks only capabilities that require it. For example, stale node behavior does not block public-feed TT when current public-feed contracts are separately verified.
