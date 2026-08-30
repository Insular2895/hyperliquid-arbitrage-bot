# Source Inventory

## Périmètre

Inventaire établi le 2026-08-30 avant consolidation. Le workspace
`/Users/insular/Hyperliquid Arbitrage` ne contenait aucun document, PDF, TXT ou
DOCX au démarrage. Les huit fichiers Markdown explicitement fournis par le
propriétaire constituent donc le corpus projet complet disponible.

Le fichier `pasted-text.txt` est la mission de travail : il est traité comme une
instruction, pas comme une source de conception. Les fichiers du vault Graphipy
lus pour la gouvernance sont des règles de méthode, pas des sources du bot.

Les dates de modification filesystem sont quasi simultanées et ne constituent
pas une chronologie intellectuelle fiable. La chronologie ci-dessous est donc
inférée uniquement par le contenu : explorations et corrections d'abord, puis
les six dossiers explicitement présentés comme dossiers de fermeture.

## Corpus

| ID | Fichier | Type | Taille / longueur | Thèmes principaux | Importance | Chronologie approximative | Statut apparent |
|---|---|---:|---:|---|---|---|---|
| SRC-001 | `23. Lock-free  ring buffers  zero-copy.md` | Markdown | 82 593 octets; 5 255 lignes; 12 519 mots | pratiques production, performance, non-blocking hot path, exécution protégée, partial fills, observabilité, méthodologie de validation, HOT/WARM/COLD, Market Atlas, roadmap de collecte | Haute comme consolidation exploratoire; subordonnée aux dossiers 1–6 sur leurs domaines | Tardive dans l'exploration; contient explicitement des corrections d'anciennes idées | correction, méthodologie, spécification partielle |
| SRC-002 | `Bot hyperliquid .md` | Markdown | 149 383 octets; 6 077 lignes; 21 580 mots | vision produit, OWA/triangles, graphe, maker/taker, inventaire, bridge, risque hiérarchique, feeds, Rust/Python, performance | Très haute pour la vision et l'architecture initiale; subordonnée aux dossiers de fermeture | Source fondatrice puis enrichie par plusieurs vagues de réflexion | brainstorming, recherche, décisions intermédiaires, corrections |
| SRC-003 | `Concrètement, en production on doit garder au moins .md` | Markdown | 83 148 octets; 4 272 lignes; 12 198 mots | Recorder, rétention, replay, OWA exact, inventory, terminal viability, recovery, sizing, shared capacity, cross-exchange futur | Haute pour recorder/storage et économie OWA; subordonnée aux dossiers de fermeture | Raffinement après la vision initiale | correction, spécification, recherche |
| SRC-004 | `DOSSIER 16 — EXECUTION STATE MACHINE.md` | Markdown | 101 614 octets; 9 953 lignes; 16 423 mots | Dossier 1/6 Execution State Machine; Dossier 2/6 Formula Book V1 (QF-001 à QF-110) | Autorité maximale pour exécution, fills, recovery, reconciliation et formules | Fermeture 1/6 et 2/6 | final, spécification normative |
| SRC-005 | `DOSSIER 36 — RISK CONSTITUTION V1.md` | Markdown | 115 692 octets; 9 877 lignes; 16 437 mots | Dossier 3/6 Risk Constitution; Dossier 4/6 Schemas, Data Contracts, déterminisme Replay/Live | Autorité maximale pour risque, invariants, types, schémas, événements et parité Replay/Live | Fermeture 3/6 et 4/6 | final, spécification normative |
| SRC-006 | `DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT.md` | Markdown | 98 438 octets; 6 903 lignes; 13 776 mots | Dossier 5/6 Docker/déploiement/sécurité; Dossier 6/6 Definition of Done & Validation Matrix | Autorité maximale pour déploiement, client VPS, sécurité, mises à jour, maturité et validation | Fermeture 5/6 et 6/6 | final, spécification normative |
| SRC-007 | `Oui, dans le modèle qu’on vient de définir, le plus propre est que….md` | Markdown | 136 143 octets; 12 371 lignes; 21 967 mots | modèle client, Market Participants, edge survival, liquidity/cross-market response, couche quantitative et formules pré-clôture | Très haute pour la justification et le détail des modèles; Formula Book final prévaut en cas de conflit | Raffinement avancé antérieur au Formula Book final | recherche, correction, spécification avancée |
| SRC-008 | `Oui. Et en creusant le sujet, je corrigerais une chose fondamentale….md` | Markdown | 100 994 octets; 6 937 lignes; 15 334 mots | simulateur contrefactuel, impact mécanique vs réponse marché, fidélités F0–F4, maker/queue, infrastructure Tokyo, benchmarks et ROI | Très haute pour simulateur et infrastructure; dossiers 2/6, 4/6, 5/6 et 6/6 prévalent sur leurs contrats | Correction avancée explicite de la simulation initiale | correction, recherche, spécification avancée |

## Empreintes SHA-256

| ID | SHA-256 |
|---|---|
| SRC-001 | `061043598486f7e4fa357e681dfb67e909989945be0b8c82e1070cb7ff559921` |
| SRC-002 | `d99b2b9354ba39e74dd616206b63bd0a5442be558f78c47c88dea733f056d4a1` |
| SRC-003 | `7065fc0dcacbcf87212c3ca0dd9cb204aee347a1984bb85757033aeeade6270a` |
| SRC-004 | `df5b1720a26889fce2a74fbc380bad4bda2e2aacdb4f02054c7270e5eb04b5b9` |
| SRC-005 | `798a0f60a14397926505b470aeee5ded11507c04c6bb489a4b1f5fe950ecd66f` |
| SRC-006 | `a535a5fa04feaaf4056ab7b3880f8cbcb803a6b1300d25ed02c96aa14558115d` |
| SRC-007 | `df2e94843df1e4a28bec4699bf89c9d2f2b8faa91763b3d3e78bff05e8369490` |
| SRC-008 | `8b7924d664bd718e324bc3d7f50f0a461244b2638a69d7601caf132d8a849f50` |

## Hiérarchie d'autorité appliquée

1. Dossier 3/6 Risk Constitution pour le risque.
2. Dossier 2/6 Formula Book pour les équations et conventions.
3. Dossier 1/6 Execution State Machine pour ordres, fills, partials, recovery et reconciliation.
4. Dossier 4/6 Data Contracts pour types, événements et déterminisme Replay/Live.
5. Dossier 5/6 Deployment pour installation, Docker, update, rollback et sécurité client.
6. Dossier 6/6 Validation Matrix pour maturité, tests, activation et passage live.
7. Les sources exploratoires pour la vision, les raisons, les hypothèses et les détails non contredits.

Cette hiérarchie résout la version canonique, mais n'efface pas les contradictions :
elles sont consignées dans `CONTRADICTIONS.md` et les directions abandonnées dans
`../decisions/SUPERSEDED_DECISIONS.md`.

## Sources non incorporées

Aucun fichier du corpus n'est ignoré. Il n'existait aucune autre source pertinente
dans le workspace. Les URLs et affirmations externes citées à l'intérieur des notes
ne sont pas revalidées pendant cette mission; elles sont signalées
`EXTERNAL_RULE_REQUIRES_REVALIDATION` lorsqu'elles conditionnent une règle actuelle.
