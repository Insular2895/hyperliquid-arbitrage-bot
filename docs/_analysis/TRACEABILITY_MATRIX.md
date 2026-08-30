# Traceability matrix

## Sources vers documents normatifs

| Source | Exigences incorporées | Documents principaux |
|---|---|---|
| SRC-001 | guards historiques, recorder/replay, hot path, validation scientifique | 00, 12, 15–18, Superseded |
| SRC-002 | graphe 2/3 legs, affected routes, microstructure, Rust/Python, HOT/WARM/COLD | 00–06, 13, 17 |
| SRC-003 | stockage, OWA, sizing/shared capacity, inventaire/relocation, venue-aware | 03, 08, 11–13, 18 |
| SRC-004 D1 | machines d'état, orders/fills/cancel/recovery/reconciliation | 10, specs exécution |
| SRC-004 D2 | QF-001..110, statuts, conventions | 04 et specs quant |
| SRC-005 D3 | hiérarchie, invariants, gates, kill switches | 09, 16 |
| SRC-005 D4 | IDs/types/events/snapshots/clock/RNG/manifests/no-lookahead | 02, 11, 12 |
| SRC-006 D5 | VPS/client, Docker, secrets, licence, update/rollback/botctl | 14, 15, 18 |
| SRC-006 D6 | M0–M5, DoD, failure injection, phases | 16, 17 |
| SRC-007 | réponse agrégée, survie, maker, adresses, champion/challenger | 05–07 |
| SRC-008 | simulateur F0–F4, mécanique/réponse, infra benchmark/ROI | 07, 13, 16 |

## Exigences critiques vers preuves documentaires

| ID | Exigence | Décision/contrat | Validation |
|---|---|---|---|
| REQ-001 | OWA exige un direct | 03 §Routes | 16 M1 |
| REQ-002 | `NetConvert` unique, L2/frais/précision | 04 QF-016 | golden parity |
| REQ-003 | `Edge(q)`, `Q_validated` | 04 QF-026/076 | replay multi-size |
| REQ-004 | pas de double dépense/capacité | 08/09 | property + concurrency tests |
| REQ-005 | hard gates non compensables | 09 | invariant tests |
| REQ-006 | fill réel uniquement | 10 | partial/cancel-race tests |
| REQ-007 | no blind retry | 10 | timeout/duplicate tests |
| REQ-008 | reconcile avant nouveau risque | 09/10 | restart/failure injection |
| REQ-009 | replay/live même core | 11/12 | parity golden run |
| REQ-010 | clock/RNG injectés, no lookahead | 11/12 | determinism/audit tests |
| REQ-011 | contrefactuel distributionnel | 07 | calibration micro-live |
| REQ-012 | modèle participants agrégé avant agents | 06/ADR | OOS lift |
| REQ-013 | un VPS/client, aucun SaaS hot-path | 14/ADR | deployment acceptance |
| REQ-014 | license n'empêche pas recovery | 14/15 | outage test |
| REQ-015 | phases M0–M5 et activation progressive | 16/17 | gates signés |

La traçabilité détaillée au niveau module est portée par les sections `Sources`
des ADR et les dépendances/tests de `docs/specs/`.
