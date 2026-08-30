# 17 — Implementation Roadmap

## Règles

Cette roadmap n'autorise pas l'implémentation avant revue. Une phase commence
seulement si ses contrats/invariants sont acceptés, ses dépendances ont le niveau
requis et son DoD est mesurable. Travailler en vertical slices; recorder tôt;
replay avant modèles sophistiqués. Architecture finale-capable, fonctionnalités
progressivement activées.

## Phases normatives

| Phase | Livrable | DoD minimal / maturité de sortie |
|---:|---|---|
| 1 | Domain types and schemas | strong IDs/units/events/snapshots/versions; compile-time misuse tests; M1 |
| 2 | Hyperliquid adapters | transport abstrait, fixtures officielles revalidées, errors typed; M1 |
| 3 | Recorder | RAW append-only, priority/backpressure, chunks/checksums/gaps/crash; M1 then soak |
| 4 | Book Engine | snapshot/update/resync/freshness/single writer; golden reconstruction; M1 |
| 5 | Metadata/Fee/Precision | historical/dynamic state, normalization, invalidation; external rules verified; M1 |
| 6 | Graph/Routes | venue-aware edges, direct/OWA/triangle, dependencies, affected routes; M1 |
| 7 | NetConvert/Formula Core | QF pricing/routes exact, Rust/Python golden parity; M1 |
| 8 | Replay Engine | Clock/RNG/manifest/checkpoints/no-lookahead/determinism; M2 data core |
| 9 | Basic Opportunity Engine | BBO→L2 candidates, decisions/reasons; replay evidence; M2 |
| 10 | Account/Inventory/Reservations | ledgers, bands schema, reserve/release, concurrency invariants; M2 |
| 11 | Risk Core | constitutional gates/limits/kill switches with property/fault tests; M2 |
| 12 | Execution State Machine | five machines, CLOID, fill ledger, unknown/cancel race; emulator M2 |
| 13 | Execution Transport | protected IOC/ALO, signer/nonce, official contract verification; shadow M3 |
| 14 | Recovery/Reconciliation | actual fills, multi-route/split recovery, restart reconciliation; M3 |
| 15 | Quant Microstructure | QF-028..043 observe-only, point-in-time features; M2 |
| 16 | Market Atlas | classification, reachability, HOT/WARM/COLD policy candidates; M2 |
| 17 | Sizing | QF-075..077, shared capacities, grid/refine, tail/confidence gates; M2 |
| 18 | Simulator F0/F1 | historical + latency/mechanical, outcome distributions/calibration; M2 |
| 19 | Shadow | end-to-end live observation/plans/reconcile, no submits; M3 |
| 20 | Micro-live TT | owner-approved tiny capital, protected orders, rollback/recovery; M4 |
| 21 | Survival/Participant Models | empirical champion then challengers, OOS calibration/lift; M2/M3 observe |
| 22 | Advanced Simulator | F2/F3; F4 research; micro-live calibration and confidence; M2/M3 |
| 23 | MT/MTT | maker queue/fill/adverse/expiry validated; M4 capability-specific |
| 24 | Opportunity Portfolio | QF-078 allocation vs validated baseline; M2 then M4 |
| 25 | Bridge/Capital Relocation | terminal/exit/idle/hysteresis, internal bridge only; M2→M4 |
| 26 | Scaling | capability manifest, capital bands, infra ROI, sustained monitoring; M5 |

## Phase 1 — instruction exécutable après validation

Scope strict : définir IDs et valeurs typées, event envelopes, schema versioning,
snapshot ownership, Clock/RNG interfaces et RunManifest minimal; fournir unit,
serialization compatibility, property et misuse tests. Ne pas connecter le
réseau, ne pas calculer d'edge, ne pas signer d'ordre. Arbitrages de design
restants passent par ADR, pas par constante implicite.

## Interdépendances critiques

- Phase 13 dépend de 1–12.
- Phase 20 dépend de recovery/reconciliation, M3 et operations/rollback.
- Phase 23 dépend d'un modèle maker calibré, pas seulement d'ALO supporté.
- Phase 25 ne précède pas terminal viability/sizing/risk.
- Phase 26 est une validation, pas une simple hausse de config.

## Stop conditions

Invariant ambigu, external rule non vérifiée, simulation bias non borné, unknown
exposure, regression risk/security, data gaps non expliqués ou DoD non satisfait
→ phase bloquée/risk-off. Documenter la preuve manquante dans `OPEN_ITEMS`.

## Sources

SRC-006 D6 roadmap et DoD; dépendances issues des cinq autres dossiers.
