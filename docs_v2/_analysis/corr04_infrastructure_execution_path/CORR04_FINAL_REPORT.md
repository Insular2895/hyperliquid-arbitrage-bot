# CORR-04 — INFRASTRUCTURE / FEED / NODE / SEQUENCING COMPLETE

- Baseline commit: `5a8d5244e2a78da1b4698c4a563b1f3e9972b2be`
- CORR-03 prerequisite: `VERIFIED`
- Official Hyperliquid research: `COMPLETE FOR DOCUMENTARY SCOPE`
- inspected: official node/order-book-server commits, node/API/WebSocket/order/nonces/rate-limit/order-book/HyperBFT documentation
- current node variants: validator and non-validator
- node resource requirements: `EXTERNALLY VERIFIED AT PINNED COMMIT; DATE-SENSITIVE`
- public feed baseline: `PRESERVED`
- node required for V1 launch: `NO`
- node challenger architecture/promotion/resource model: `SPECIFIED`
- dual-feed canonical writers: `1`
- feed fusion: `NOT AUTHORIZED`
- event alignment/matched comparison: `SPECIFIED`
- `split_client_blocks`: `CURRENT AT INSPECTED COMMIT`; uncommitted mempool stream, no responses, non-final/random by default
- current semantic status: `SPECULATIVE / UNCOMMITTED / NON-CANONICAL`
- speculative lane: `RESEARCH / NON-CANONICAL`
- speculative canonical mutation/order send: `FORBIDDEN`
- speculative precompute: `ALLOWED ONLY AFTER EXACT CANONICAL PARITY`
- provider/region/AZ/network benchmark: `SPECIFIED`; Tokyo permanent: `NO`
- Docker baseline: `PRESERVED`; bridge/host/native benchmark: `SPECIFIED`
- native deployment promoted: `NO`; security controls disabled: `0`
- CPU affinity/scheduler/IRQ/kernel tuning: `EVIDENCE-GATED`
- AF_XDP/DPDK/F-Stack: `RESEARCH`; kernel bypass baseline: `NO`
- TCP/TLS applicability: `AUDITED — PACKET I/O ALONE DOES NOT SUPPLY TCP/TLS/WS`
- current user-facing paid/numeric per-order priority for V1 spot: `NOT VERIFIED / NOT CURRENTLY DOCUMENTED`
- ALO-only validator priority and node gossip priority: `CURRENT LIMITED FACTS`; deterministic sequencing/fill guarantee: `NO CLAIM`
- priority cost known: `NO`; Priority Formula/Risk gate: `0`
- FIX official current order-entry support: `NOT FOUND`; V1 baseline: `NO`
- Infra Capture Attribution: `SPECIFIED`; FullRouteCompletion integration: `SPECIFIED AS EVIDENCE`
- Formula changes/new QF: `0 / 0`
- Execution/UNKNOWN/Risk hard-gate semantic changes: `0 / 0 / 0`
- roadmap/validation: `UPDATED IN EXISTING PHASES/M0–M5`
- review baseline: `STALE — CORR SERIES IN PROGRESS`
- files outside `docs_v2`: `0`; source code/legacy docs: `0 / 0`
- human approval: `PENDING FINAL REVIEW`
- implementation: `NOT AUTHORIZED`
- CORR-05 started: `NO`

All current facts remain tied to retrieval date/version and future revalidation. The deliverable establishes decision gates; it does not claim that any infrastructure treatment has passed them.

## CORR-05 readiness checks 87–93

| Check | Result | Evidence |
|---|---|---|
| priority-cost ownership deferred | `YES` | Priority hook assigns no economic owner |
| node cost/economic evidence available to QF-086–QF-091 consumers | `YES` | resource/interference, experiment and promotion contracts |
| actual completion metrics available | `YES` | CORR-03 authority retained |
| QF-048 remains distinct from FullRouteCompletion | `YES` | modeled capture versus actual outcome explicitly separated |
| completion accounting in QF-056/057 can be audited | `YES` | CORR-05 deferment recorded |
| survival/completion/infra double counting can be detected | `YES` | attribution contract forbids pre-audit multiplication |
| `Q_validated` can consume completion evidence without changing truth | `YES` | Validation owns evidence scope; Execution truth unchanged |
