# PASS 01 — Infrastructure Source Cross-check

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 01 SOURCE REVIEW COMPLETE`

## Method

The eight original files were reopened directly. Numeric locators from the Infrastructure domain index and the master ledger were merged only to avoid rereading overlapping line ranges; semantic interpretation was then performed from the original text, not from PASS 00 prose.

## Coverage by original source

| Source | Requirements reviewed | File | Authority use in PASS 01 |
|---|---:|---|---|
| SRC-001 | 34 | `/Users/insular/Downloads/23. Lock-free  ring buffers  zero-copy/23. Lock-free  ring buffers  zero-copy.md` | Historical performance, benchmark and calibration context; later closures override conflicts. |
| SRC-002 | 58 | `/Users/insular/Downloads/Bot hyperliquid/Bot hyperliquid .md` | Public-feed/node-compatible architecture, WebSocket/book/hot-path context. |
| SRC-003 | 41 | `/Users/insular/Downloads/Concrètement, en production on doit garder au moins/Concrètement, en production on doit garder au moins .md` | Recorder, replay and storage working-set rationale. |
| SRC-004 | 41 | `/Users/insular/Downloads/DOSSIER 16 — EXECUTION STATE MACHINE/DOSSIER 16 — EXECUTION STATE MACHINE.md` | Canonical execution and formula closure, including QF-084–QF-093. |
| SRC-005 | 55 | `/Users/insular/Downloads/DOSSIER 36 — RISK CONSTITUTION V1/DOSSIER 36 — RISK CONSTITUTION V1.md` | Risk, clock-health, infrastructure-state and data-contract closure. |
| SRC-006 | 127 | `/Users/insular/Downloads/DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT/DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT.md` | Deployment, security, client operation and validation authority. |
| SRC-007 | 50 | `/Users/insular/Downloads/Oui, dans le modèle qu’on vient de définir, le plus propre est que…/Oui, dans le modèle qu’on vient de définir, le plus propre est que….md` | Analytical context for latency distributions, participants and confidence gates. |
| SRC-008 | 108 | `/Users/insular/Downloads/Oui. Et en creusant le sujet, je corrigerais une chose fondamentale…/Oui. Et en creusant le sujet, je corrigerais une chose fondamentale….md` | Latest infrastructure synthesis: baseline, providers, benchmarks, economics, node and operations. |

## Direct-source union control

- All 512 PASS 00 Infrastructure entries had at least one numeric original-source locator.
- The merged locator set contained 300 non-overlapping intervals and 17,339 unique original-source lines.
- QF-088 and QF-093 were additionally reopened in the QF-084–QF-093 closure block of SRC-004.
- No live web lookup was used; provider and platform claims remain dated source snapshots.

## Authority resolutions applied

| Topic | Earlier material | Closure applied | Result |
|---|---|---|---|
| Node at launch | Node-focused options in SRC-002/SRC-007 | SRC-006 + latest SRC-008 direction | Node-compatible from day one; public feed first; node activation gated. |
| Storage capacity | Comfortable historical/archive examples in SRC-003 | SRC-008 light baseline plus measured recorder working set | 40–100 GB is only an initial working hypothesis; retention/archive sizing remains measured and separate. |
| Fixed latency numbers | Point examples in earlier sources | SRC-004/005 no-magic-number and calibrated-distribution rules | Mechanisms are invariant; thresholds are calibrated and versioned. |
| Infrastructure upgrade | Capital/profile heuristics | SRC-004 QF-084–QF-093 + SRC-008 explicit correction | Incremental recoverable PnL and lower-confidence evidence govern; capital alone never triggers. |
| Client deployment | Mixed centralized/product language | SRC-006 and explicit client overlay | Per-client isolated deployment; no implicit multi-tenant SaaS control plane. |

## Source-use limitation

Original sources establish project intent and closure authority, but they do not make commercial provider facts current. All provider prices, plan names, regions, node features and exchange/API capabilities are routed to the external revalidation register.
