# SRC-003 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-003`
- Filename: `Concrètement, en production on doit garder au moins .md`
- SHA-256: `7065fc0dcacbcf87212c3ca0dd9cb204aee347a1984bb85757033aeeade6270a`
- Line count: 4272
- Authority profile: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Main domains: ACCOUNTING, ARCH, EXECUTION, INVENTORY, ROUTING, PRODUCT, INFRA, RISK, CAPITAL, BRIDGE, RECORDER, RESEARCH
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-003-ITEM-0001 — Source preamble

- Source: `SRC-003`
- Location: lines 1–30; heading `Source preamble`
- Domain tags: EXECUTION, RECOVERY, ACCOUNTING, CAPITAL, ROUTING, QUANT, PRODUCT
- Source statement: Source preamble: Concrètement, en production on doit garder au moins : * les ordres envoyés et les fills réels : prix demandé, prix obtenu, quantité, frais, partial fills ;
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Source preamble` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0062`; supporting items: SRC-007-ITEM-0001, SRC-008-ITEM-0001; domain indexes `EXECUTION, RECOVERY, ACCOUNTING, CAPITAL, ROUTING, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0002 — Deuxième raison : comparer simulation et réalité

- Source: `SRC-003`
- Location: lines 31–51; heading `Deuxième raison : comparer simulation et réalité`
- Domain tags: EXECUTION, SIMULATOR, REPLAY
- Source statement: Deuxième raison : comparer simulation et réalité: Notre Replay Engine va estimer par exemple : Expected slippage = 0.021 %
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Deuxième raison : comparer simulation et réalité` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0063`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, SIMULATOR, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0003 — Troisième raison : le marché change

- Source: `SRC-003`
- Location: lines 52–76; heading `Troisième raison : le marché change`
- Domain tags: ACCOUNTING, BRIDGE, ROUTING, MARKET_ATLAS
- Source statement: Troisième raison : le marché change: Même si notre bot est parfaitement calibré en septembre, Hyperliquid peut changer en décembre : * comportement des routes ;
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Troisième raison : le marché change` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ACCT-0031`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, BRIDGE, ROUTING, MARKET_ATLAS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0004 — Mais ça ne signifie PAS qu’on doit garder 20 Go/jour éternellement

- Source: `SRC-003`
- Location: lines 77–118; heading `Mais ça ne signifie PAS qu’on doit garder 20 Go/jour éternellement`
- Domain tags: EXECUTION, INFRA, INVENTORY, PRODUCT
- Source statement: Mais ça ne signifie PAS qu’on doit garder 20 Go/jour éternellement: C'est là que je nuancerais ce que je t'ai dit avant. Une fois en production mature, on pourrait faire :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Mais ça ne signifie PAS qu’on doit garder 20 Go/jour éternellement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0064`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0005 — Donc le stockage prod pourrait être nettement plus petit

- Source: `SRC-003`
- Location: lines 119–153; heading `Donc le stockage prod pourrait être nettement plus petit`
- Domain tags: EXECUTION, RECORDER, DATA, INFRA, OPERATIONS, PRODUCT, ARCH
- Source statement: Donc le stockage prod pourrait être nettement plus petit: 100–300 Go NVMe par exemple Les 500 Go–1 To que je citais étaient une configuration confortable, pas une obligation.
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Donc le stockage prod pourrait être nettement plus petit` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0065`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, DATA, INFRA, OPERATIONS, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0006 — 1. Architecture commune

- Source: `SRC-003`
- Location: lines 154–193; heading `1. Architecture commune`
- Domain tags: ARCH, EXECUTION, RECORDER, INFRA, DEPLOYMENT, ACCOUNTING, MICROSTRUCTURE, QUANT
- Source statement: 1. Architecture commune: Dans les deux environnements : Le Recorder est parallèle au bot.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `1. Architecture commune` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ARCH-0044`; supporting items: none found by conservative heading match; domain indexes `ARCH, EXECUTION, RECORDER, INFRA, DEPLOYMENT, ACCOUNTING, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0007 — 2. TEST / R&D : objectif = construire notre historique propriétaire

- Source: `SRC-003`
- Location: lines 194–201; heading `2. TEST / R&D : objectif = construire notre historique propriétaire`
- Domain tags: ROUTING, ARCH, RESEARCH
- Source statement: 2. TEST / R&D : objectif = construire notre historique propriétaire: Au début, on veut être assez agressifs dans la collecte. Parce qu'on ne sait pas encore :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `2. TEST / R&D : objectif = construire notre historique propriétaire` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-ROUTE-0019`; supporting items: none found by conservative heading match; domain indexes `ROUTING, ARCH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0008 — On enregistre quasiment tout le spot pertinent

- Source: `SRC-003`
- Location: lines 202–218; heading `On enregistre quasiment tout le spot pertinent`
- Domain tags: EXECUTION, RECORDER, CLOCK, HOT_WARM_COLD
- Source statement: On enregistre quasiment tout le spot pertinent: HOT/WARM/COLD sert au calcul live, pas à décider quelles données historiques méritent d'exister.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `On enregistre quasiment tout le spot pertinent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0066`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, CLOCK, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0009 — 3. Donnée RAW de test

- Source: `SRC-003`
- Location: lines 219–245; heading `3. Donnée RAW de test`
- Domain tags: RECORDER, DATA, CLOCK, INFRA, ACCOUNTING, ARCH
- Source statement: 3. Donnée RAW de test: Pour chaque message reçu : Parce que si notre parser Rust contient un bug en septembre, on pourra reparcourir août avec un parser corrigé.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `3. Donnée RAW de test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0001`; supporting items: none found by conservative heading match; domain indexes `RECORDER, DATA, CLOCK, INFRA, ACCOUNTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0010 — 4. Le RAW est découpé en petits chunks

- Source: `SRC-003`
- Location: lines 246–287; heading `4. Le RAW est découpé en petits chunks`
- Domain tags: RECORDER, DATA, CLOCK
- Source statement: 4. Le RAW est découpé en petits chunks: Je ne ferais pas : Donc environ un fichier toutes les 5–15 minutes, selon volume.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `4. Le RAW est découpé en petits chunks` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0002`; supporting items: none found by conservative heading match; domain indexes `RECORDER, DATA, CLOCK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0011 — 5. Ensuite le RAW produit un dataset NORMALIZED

- Source: `SRC-003`
- Location: lines 288–334; heading `5. Ensuite le RAW produit un dataset NORMALIZED`
- Domain tags: DATA, RECORDER, ARCH
- Source statement: 5. Ensuite le RAW produit un dataset NORMALIZED: Ça rend l'analyse extrêmement rapide.
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `5. Ensuite le RAW produit un dataset NORMALIZED` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0005`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0012 — 6. Puis on génère les données DERIVED

- Source: `SRC-003`
- Location: lines 335–388; heading `6. Puis on génère les données DERIVED`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, BRIDGE, ROUTING, GRAPH, MARKET_ATLAS, QUANT, ARCH
- Source statement: 6. Puis on génère les données DERIVED: C'est là que notre Market Atlas apparaît. Ces données sont très légères comparées au RAW.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `6. Puis on génère les données DERIVED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0032`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, BRIDGE, ROUTING, GRAPH, MARKET_ATLAS, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0013 — 7. Comment les données s'accumulent en phase test

- Source: `SRC-003`
- Location: lines 389–405; heading `7. Comment les données s'accumulent en phase test`
- Domain tags: EXECUTION, RECORDER, INFRA
- Source statement: 7. Comment les données s'accumulent en phase test: Imaginons que notre recorder génère après compression : 1 jour | 10 Go
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `7. Comment les données s'accumulent en phase test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0067`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0014 — 8. Ton SSD 1 To en TEST

- Source: `SRC-003`
- Location: lines 406–426; heading `8. Ton SSD 1 To en TEST`
- Domain tags: REPLAY
- Source statement: 8. Ton SSD 1 To en TEST: BOT / IDE / système ├── RAW récent 100–200 Go
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `8. Ton SSD 1 To en TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-REPLAY-0006`; supporting items: none found by conservative heading match; domain indexes `REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0015 — 9. iCloud en phase TEST

- Source: `SRC-003`
- Location: lines 427–450; heading `9. iCloud en phase TEST`
- Domain tags: RECORDER
- Source statement: 9. iCloud en phase TEST: Ton iCloud peut servir d'archive froide temporaire.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `9. iCloud en phase TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0003`; supporting items: none found by conservative heading match; domain indexes `RECORDER`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0016 — SSD

- Source: `SRC-003`
- Location: lines 451–452; heading `SSD`
- Domain tags: ARCH
- Source statement: SSD: 7–14 derniers jours RAW.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `SSD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0045`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0017 — iCloud

- Source: `SRC-003`
- Location: lines 453–454; heading `iCloud`
- Domain tags: ARCH
- Source statement: iCloud: 30–90 jours RAW compressés.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `iCloud` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0046`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0018 — Mac

- Source: `SRC-003`
- Location: lines 455–458; heading `Mac`
- Domain tags: DATA
- Source statement: Mac: Je commencerais effectivement avec 2 To, pas 6 To.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Mac` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0006`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0019 — 10. Mais ne jamais écrire directement vers iCloud

- Source: `SRC-003`
- Location: lines 459–484; heading `10. Mais ne jamais écrire directement vers iCloud`
- Domain tags: EXECUTION, RECORDER, INFRA, ACCOUNTING
- Source statement: 10. Mais ne jamais écrire directement vers iCloud: Donc iCloud ne peut jamais ralentir ou casser notre Recorder.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `10. Mais ne jamais écrire directement vers iCloud` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0068`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0020 — 11. La rétention pendant la recherche

- Source: `SRC-003`
- Location: lines 485–486; heading `11. La rétention pendant la recherche`
- Domain tags: RESEARCH
- Source statement: 11. La rétention pendant la recherche: Au début :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `11. La rétention pendant la recherche` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0010`; supporting items: none found by conservative heading match; domain indexes `RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0021 — RAW

- Source: `SRC-003`
- Location: lines 487–488; heading `RAW`
- Domain tags: ARCH
- Source statement: RAW: 14–60 jours, voire plus si stockage disponible.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `RAW` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0047`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0022 — NORMALIZED

- Source: `SRC-003`
- Location: lines 489–490; heading `NORMALIZED`
- Domain tags: ARCH
- Source statement: NORMALIZED: longue durée.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `NORMALIZED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0048`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0023 — DERIVED

- Source: `SRC-003`
- Location: lines 491–492; heading `DERIVED`
- Domain tags: ARCH
- Source statement: DERIVED: quasi permanent.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `DERIVED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0049`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0024 — GOLDEN DATASETS

- Source: `SRC-003`
- Location: lines 493–519; heading `GOLDEN DATASETS`
- Domain tags: DATA, EXECUTION, ACCOUNTING, BRIDGE, QUANT
- Source statement: GOLDEN DATASETS: Les golden datasets sont des périodes particulièrement importantes : Ces datasets servent ensuite aux tests de régression.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `GOLDEN DATASETS` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0007`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, ACCOUNTING, BRIDGE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0025 — 12. Puis on développe et teste le bot sur ces données

- Source: `SRC-003`
- Location: lines 520–568; heading `12. Puis on développe et teste le bot sur ces données`
- Domain tags: RISK, ACCOUNTING, SIMULATOR, REPLAY, INVENTORY, BRIDGE, TRIANGLE, GRAPH
- Source statement: 12. Puis on développe et teste le bot sur ces données: Notre moteur Rust reçoit : Il pense presque être en live.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `12. Puis on développe et teste le bot sur ces données` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0028`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, SIMULATOR, REPLAY, INVENTORY, BRIDGE, TRIANGLE, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0026 — 13. En TEST, on peut rejouer le même marché 100 fois

- Source: `SRC-003`
- Location: lines 569–572; heading `13. En TEST, on peut rejouer le même marché 100 fois`
- Domain tags: DATA
- Source statement: 13. En TEST, on peut rejouer le même marché 100 fois: C'est tout l'intérêt. Dataset :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `13. En TEST, on peut rejouer le même marché 100 fois` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0008`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0027 — Run A

- Source: `SRC-003`
- Location: lines 573–579; heading `Run A`
- Domain tags: ARCH
- Source statement: Run A: 1000 USDC
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Run A` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0050`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0028 — Run B

- Source: `SRC-003`
- Location: lines 580–586; heading `Run B`
- Domain tags: ARCH
- Source statement: Run B: 1000 BTC-equivalent
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Run B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0051`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0029 — Run C

- Source: `SRC-003`
- Location: lines 587–619; heading `Run C`
- Domain tags: INFRA, BRIDGE, HOT_WARM_COLD
- Source statement: Run C: sans jamais réenregistrer le marché.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Run C` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0031`; supporting items: none found by conservative heading match; domain indexes `INFRA, BRIDGE, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0030 — 14. TEST : le dataset grossit jusqu'à ce qu'on possède assez de régimes

- Source: `SRC-003`
- Location: lines 620–634; heading `14. TEST : le dataset grossit jusqu'à ce qu'on possède assez de régimes`
- Domain tags: DATA, INFRA
- Source statement: 14. TEST : le dataset grossit jusqu'à ce qu'on possède assez de régimes: Je ne raisonnerais pas simplement : On veut observer plusieurs situations :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `14. TEST : le dataset grossit jusqu'à ce qu'on possède assez de régimes` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0009`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0031 — 15. Puis passage en PRODUCTION

- Source: `SRC-003`
- Location: lines 635–640; heading `15. Puis passage en PRODUCTION`
- Domain tags: PRODUCT, INFRA
- Source statement: 15. Puis passage en PRODUCTION: On sait déjà comment le marché fonctionne. Il n'est plus nécessaire de conserver chaque octet du L2 pendant 2 ans.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `15. Puis passage en PRODUCTION` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0003`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0032 — 16. Pourquoi continuer à enregistrer le marché en production

- Source: `SRC-003`
- Location: lines 641–642; heading `16. Pourquoi continuer à enregistrer le marché en production`
- Domain tags: PRODUCT
- Source statement: 16. Pourquoi continuer à enregistrer le marché en production: Principalement pour quatre raisons :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `16. Pourquoi continuer à enregistrer le marché en production` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0004`; supporting items: none found by conservative heading match; domain indexes `PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0037 — 17. Production : beaucoup plus sélectif sur la rétention

- Source: `SRC-003`
- Location: lines 648–672; heading `17. Production : beaucoup plus sélectif sur la rétention`
- Domain tags: PRODUCT, EXECUTION, RECORDER, INFRA, OPERATIONS
- Source statement: 17. Production : beaucoup plus sélectif sur la rétention: Le serveur Tokyo pourrait enregistrer : mais garder le RAW complet localement seulement :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `17. Production : beaucoup plus sélectif sur la rétention` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0005`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, EXECUTION, RECORDER, INFRA, OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0038 — 18. Ce qu'on garde longtemps en production

- Source: `SRC-003`
- Location: lines 673–674; heading `18. Ce qu'on garde longtemps en production`
- Domain tags: PRODUCT
- Source statement: 18. Ce qu'on garde longtemps en production: Ça, je ne supprimerais pratiquement jamais :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `18. Ce qu'on garde longtemps en production` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0006`; supporting items: none found by conservative heading match; domain indexes `PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0039 — Executions

- Source: `SRC-003`
- Location: lines 675–688; heading `Executions`
- Domain tags: EXECUTION, RECOVERY, ACCOUNTING
- Source statement: Executions: order slippage
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Executions` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0069`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0040 — Opportunities

- Source: `SRC-003`
- Location: lines 689–700; heading `Opportunities`
- Domain tags: ROUTING
- Source statement: Opportunities: route decision
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Opportunities` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0020`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0041 — Inventory

- Source: `SRC-003`
- Location: lines 701–711; heading `Inventory`
- Domain tags: INVENTORY, CAPITAL, BRIDGE
- Source statement: Inventory: capital location balances
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Inventory` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0008`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0042 — Latencies

- Source: `SRC-003`
- Location: lines 712–714; heading `Latencies`
- Domain tags: ARCH
- Source statement: Latencies: Très léger.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Latencies` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0052`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0043 — Derived features

- Source: `SRC-003`
- Location: lines 715–717; heading `Derived features`
- Domain tags: ARCH
- Source statement: Derived features: Relativement léger.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Derived features` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0053`; supporting items: SRC-005-ITEM-0267; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0044 — Incidents

- Source: `SRC-003`
- Location: lines 718–720; heading `Incidents`
- Domain tags: OPERATIONS
- Source statement: Incidents: Conservation permanente.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Incidents` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OPS-0002`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0045 — 19. Market windows autour des vrais ordres

- Source: `SRC-003`
- Location: lines 721–752; heading `19. Market windows autour des vrais ordres`
- Domain tags: ARCH
- Source statement: 19. Market windows autour des vrais ordres: Si un ordre réel est exécuté à : je voudrais automatiquement taguer :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `19. Market windows autour des vrais ordres` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0054`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0046 — 20. Exemple production

- Source: `SRC-003`
- Location: lines 753–791; heading `20. Exemple production`
- Domain tags: PRODUCT, EXECUTION, INFRA
- Source statement: 20. Exemple production: Le bot tourne 24 heures. RAW full market 12 GB
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `20. Exemple production` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0007`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, EXECUTION, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0047 — 21. Production : structure physique

- Source: `SRC-003`
- Location: lines 792–810; heading `21. Production : structure physique`
- Domain tags: PRODUCT, RECORDER, INFRA
- Source statement: 21. Production : structure physique: NVMe 250–500 GB minimum confortable Le serveur n'est pas notre archive.
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `21. Production : structure physique` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0008`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, RECORDER, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0048 — 22. Ensuite archive

- Source: `SRC-003`
- Location: lines 811–827; heading `22. Ensuite archive`
- Domain tags: RECORDER, INFRA
- Source statement: 22. Ensuite archive: Pas besoin que le Mac soit allumé.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `22. Ensuite archive` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0004`; supporting items: none found by conservative heading match; domain indexes `RECORDER, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0049 — 23. Object storage production

- Source: `SRC-003`
- Location: lines 828–867; heading `23. Object storage production`
- Domain tags: PRODUCT, INFRA, OPERATIONS, ROUTING, HOT_WARM_COLD
- Source statement: 23. Object storage production: Mais avec des lifecycle policies.
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `23. Object storage production` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0009`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, INFRA, OPERATIONS, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0050 — 24. Donc on automatise la suppression

- Source: `SRC-003`
- Location: lines 868–900; heading `24. Donc on automatise la suppression`
- Domain tags: RECORDER, OPERATIONS
- Source statement: 24. Donc on automatise la suppression: Le bot ne supprime pas au hasard.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `24. Donc on automatise la suppression` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0005`; supporting items: none found by conservative heading match; domain indexes `RECORDER, OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0051 — 25. Production : le Recorder ne doit jamais remplir le disque

- Source: `SRC-003`
- Location: lines 901–928; heading `25. Production : le Recorder ne doit jamais remplir le disque`
- Domain tags: EXECUTION, RECORDER, PRODUCT, INFRA, MICROSTRUCTURE
- Source statement: 25. Production : le Recorder ne doit jamais remplir le disque: Mais surtout on surveille : Si le Recorder n'arrive plus à suivre :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `25. Production : le Recorder ne doit jamais remplir le disque` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0070`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, PRODUCT, INFRA, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0052 — 26. On sépare encore le hot path

- Source: `SRC-003`
- Location: lines 929–957; heading `26. On sépare encore le hot path`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, RISK, RECORDER, DEPLOYMENT, MICROSTRUCTURE
- Source statement: 26. On sépare encore le hot path: Même si le stockage cloud tombe : le bot continue, dans les limites définies.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `26. On sépare encore le hot path` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ROUTE-0021`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, RISK, RECORDER, DEPLOYMENT, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0053 — 27. Account/Execution data a priorité sur Market RAW

- Source: `SRC-003`
- Location: lines 958–972; heading `27. Account/Execution data a priorité sur Market RAW`
- Domain tags: EXECUTION, INFRA, ACCOUNTING, INVENTORY
- Source statement: 27. Account/Execution data a priorité sur Market RAW: Si le disque devient critique, on peut accepter de perdre une partie du marché brut. Je n'accepte pas de perdre :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `27. Account/Execution data a priorité sur Market RAW` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0071`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ACCOUNTING, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0054 — P0

- Source: `SRC-003`
- Location: lines 973–974; heading `P0`
- Domain tags: ARCH
- Source statement: P0: Executions/account.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `P0` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0055`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0055 — P1

- Source: `SRC-003`
- Location: lines 975–976; heading `P1`
- Domain tags: OPERATIONS
- Source statement: P1: Market autour des executions/incidents.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `P1` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OPS-0003`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0056 — P2

- Source: `SRC-003`
- Location: lines 977–978; heading `P2`
- Domain tags: ARCH
- Source statement: P2: Derived/opportunities.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `P2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0056`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0057 — P3

- Source: `SRC-003`
- Location: lines 979–981; heading `P3`
- Domain tags: ARCH
- Source statement: P3: Raw marché général.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `P3` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0057`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0058 — 28. Production sert aussi à améliorer notre simulateur

- Source: `SRC-003`
- Location: lines 982–1027; heading `28. Production sert aussi à améliorer notre simulateur`
- Domain tags: PRODUCT, VALIDATION, REPLAY, ARCH, FUTURE
- Source statement: 28. Production sert aussi à améliorer notre simulateur: Chaque trade réel donne : Puis Python analyse les erreurs.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `28. Production sert aussi à améliorer notre simulateur` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-PRODUCT-0010`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, VALIDATION, REPLAY, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0059 — 29. Production enrichit donc continuellement notre Market Atlas

- Source: `SRC-003`
- Location: lines 1028–1050; heading `29. Production enrichit donc continuellement notre Market Atlas`
- Domain tags: MARKET_ATLAS, PRODUCT, INFRA, ACCOUNTING, MICROSTRUCTURE, BRIDGE, ROUTING, QUANT
- Source statement: 29. Production enrichit donc continuellement notre Market Atlas: Même si on supprime le RAW ancien, les features restent : d'historique économique sans conserver 90 jours de L2 complet.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `29. Production enrichit donc continuellement notre Market Atlas` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ATLAS-0002`; supporting items: SRC-006-ITEM-0330; domain indexes `MARKET_ATLAS, PRODUCT, INFRA, ACCOUNTING, MICROSTRUCTURE, BRIDGE, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0060 — 30. Synchronisation TEST ↔ PROD

- Source: `SRC-003`
- Location: lines 1051–1079; heading `30. Synchronisation TEST ↔ PROD`
- Domain tags: EXECUTION, DATA, INFRA, REPLAY, PRODUCT
- Source statement: 30. Synchronisation TEST ↔ PROD: Notre environnement R&D peut récupérer : les 12 heures autour d'une mauvaise journée
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `30. Synchronisation TEST ↔ PROD` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0072`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DATA, INFRA, REPLAY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0061 — 31. Exemple d'incident

- Source: `SRC-003`
- Location: lines 1080–1125; heading `31. Exemple d'incident`
- Domain tags: OPERATIONS, EXECUTION, RISK, INFRA, ACCOUNTING, REPLAY, INVENTORY, ROUTING
- Source statement: 31. Exemple d'incident: Le serveur a automatiquement conservé : T-10 sec → T+20 sec
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `31. Exemple d'incident` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-OPS-0004`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, EXECUTION, RISK, INFRA, ACCOUNTING, REPLAY, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0062 — 32. Structure globale TEST

- Source: `SRC-003`
- Location: lines 1126–1147; heading `32. Structure globale TEST`
- Domain tags: RECORDER, REPLAY, ARCH, RESEARCH
- Source statement: 32. Structure globale TEST: └── iCloud / archive temporaire
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `32. Structure globale TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0006`; supporting items: none found by conservative heading match; domain indexes `RECORDER, REPLAY, ARCH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0063 — 33. Structure globale PROD

- Source: `SRC-003`
- Location: lines 1148–1176; heading `33. Structure globale PROD`
- Domain tags: EXECUTION, RECORDER, INFRA, OPERATIONS, ARCH, RESEARCH
- Source statement: 33. Structure globale PROD: TOKYO ├── Rust Trading Engine
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `33. Structure globale PROD` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0073`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, OPERATIONS, ARCH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0064 — 34. Rétention que je choisirais comme point de départ

- Source: `SRC-003`
- Location: lines 1177–1194; heading `34. Rétention que je choisirais comme point de départ`
- Domain tags: RECORDER, DATA, INFRA, OPERATIONS, PRODUCT, ARCH
- Source statement: 34. Rétention que je choisirais comme point de départ: Pas gravée dans le marbre, mais une bonne base : Donnée | Test | Production
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `34. Rétention que je choisirais comme point de départ` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REC-0007`; supporting items: none found by conservative heading match; domain indexes `RECORDER, DATA, INFRA, OPERATIONS, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0065 — 35. Avec ton matériel actuellement

- Source: `SRC-003`
- Location: lines 1195–1196; heading `35. Avec ton matériel actuellement`
- Domain tags: ARCH
- Source statement: 35. Avec ton matériel actuellement: Pour la phase R&D :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `35. Avec ton matériel actuellement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ARCH-0058`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0066 — SSD Mac 1 To

- Source: `SRC-003`
- Location: lines 1197–1206; heading `SSD Mac 1 To`
- Domain tags: ARCH
- Source statement: SSD Mac 1 To: Je commencerais sans acheter autre chose. pour ne jamais saturer ton Mac.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `SSD Mac 1 To` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0059`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0067 — iCloud 2 To

- Source: `SRC-003`
- Location: lines 1207–1211; heading `iCloud 2 To`
- Domain tags: ARCH
- Source statement: iCloud 2 To: Je le prendrais uniquement lorsqu'on voit que nos données réellement compressées commencent à consommer suffisamment d'espace. Pas besoin des 6 To aujourd'hui.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `iCloud 2 To` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0060`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0068 — 36. La première métrique qu'on programme

- Source: `SRC-003`
- Location: lines 1212–1245; heading `36. La première métrique qu'on programme`
- Domain tags: INFRA, EXECUTION, RECORDER
- Source statement: 36. La première métrique qu'on programme: Dès le premier jour du Recorder : Après exactement 24 h, on aura par exemple :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `36. La première métrique qu'on programme` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0032`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, RECORDER`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0069 — La règle finale

- Source: `SRC-003`
- Location: lines 1246–1247; heading `La règle finale`
- Domain tags: ARCH
- Source statement: La règle finale: Je résumerais toute notre politique de données comme ça :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `La règle finale` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0061`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0070 — Pendant la recherche

- Source: `SRC-003`
- Location: lines 1248–1250; heading `Pendant la recherche`
- Domain tags: RESEARCH
- Source statement: Pendant la recherche: On privilégie la capacité à rejouer le passé.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Pendant la recherche` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0011`; supporting items: none found by conservative heading match; domain indexes `RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0071 — Pendant la production

- Source: `SRC-003`
- Location: lines 1251–1253; heading `Pendant la production`
- Domain tags: PRODUCT, OPERATIONS
- Source statement: Pendant la production: On privilégie la capacité à expliquer chaque décision réelle. Donc on garde tout autour des trades/incidents, et on réduit progressivement le bruit du marché général.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Pendant la production` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-PRODUCT-0011`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0072 — Et dans les deux cas

- Source: `SRC-003`
- Location: lines 1254–1283; heading `Et dans les deux cas`
- Domain tags: EXECUTION, RECOVERY, RISK, DATA, REPLAY, MICROSTRUCTURE, CAPITAL, BRIDGE
- Source statement: Et dans les deux cas: RAW → NORMALIZED → DERIVED → REPLAY → amélioration du bot. Ainsi les données ne sont jamais juste des “logs”. Elles deviennent le système qui nous permet de cartographier Hyperliquid, tester les routes, calibrer le capital, comprendre les pertes, comparer simulation/live et améliorer continuellement notre moteur sans expérimenter directement avec de gros montants.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Et dans les deux cas` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0074`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, DATA, REPLAY, MICROSTRUCTURE, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0073 — Exemple

- Source: `SRC-003`
- Location: lines 1284–1338; heading `Exemple`
- Domain tags: EXECUTION, INFRA, ACCOUNTING, CAPITAL, BRIDGE, TRIANGLE, GRAPH, HOT_WARM_COLD
- Source statement: Exemple: On prend exactement la même journée Hyperliquid. Capital = 1 000 USDC
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Exemple` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0075`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ACCOUNTING, CAPITAL, BRIDGE, TRIANGLE, GRAPH, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0074 — On pourra même tester ton idée HOT/WARM/COLD proprement

- Source: `SRC-003`
- Location: lines 1339–1340; heading `On pourra même tester ton idée HOT/WARM/COLD proprement`
- Domain tags: HOT_WARM_COLD
- Source statement: On pourra même tester ton idée HOT/WARM/COLD proprement: Même marché enregistré.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `On pourra même tester ton idée HOT/WARM/COLD proprement` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0027`; supporting items: SRC-001-ITEM-0049, SRC-006-ITEM-0332, SRC-007-ITEM-0115; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0075 — Sans optimisation

- Source: `SRC-003`
- Location: lines 1341–1356; heading `Sans optimisation`
- Domain tags: INFRA, ACCOUNTING, ROUTING, HOT_WARM_COLD
- Source statement: Sans optimisation: routes évaluées = 100 % PnL théorique capté = 100 %
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Sans optimisation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0033`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0076 — Notre version

- Source: `SRC-003`
- Location: lines 1357–1385; heading `Notre version`
- Domain tags: EXECUTION, INFRA, ACCOUNTING, INVENTORY, ROUTING, HOT_WARM_COLD, QUANT, ARCH
- Source statement: Notre version: HOT = accessible depuis inventory routes évaluées = 24 %
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Notre version` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0076`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ACCOUNTING, INVENTORY, ROUTING, HOT_WARM_COLD, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0077 — Idem pour les bridges

- Source: `SRC-003`
- Location: lines 1386–1395; heading `Idem pour les bridges`
- Domain tags: BRIDGE, INVENTORY
- Source statement: Idem pour les bridges: On peut rejouer exactement la même période avec :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Idem pour les bridges` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BRIDGE-0007`; supporting items: none found by conservative heading match; domain indexes `BRIDGE, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0078 — Policy A

- Source: `SRC-003`
- Location: lines 1396–1397; heading `Policy A`
- Domain tags: ARCH
- Source statement: Policy A: Ne jamais quitter BTC.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Policy A` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0062`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0079 — Policy B

- Source: `SRC-003`
- Location: lines 1398–1399; heading `Policy B`
- Domain tags: ARCH
- Source statement: Policy B: Passer ETH dès que son EV dépasse BTC.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Policy B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0063`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0080 — Policy C

- Source: `SRC-003`
- Location: lines 1400–1412; heading `Policy C`
- Domain tags: RISK, ACCOUNTING, BRIDGE
- Source statement: Policy C: Passer ETH seulement si :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Policy C` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0029`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0081 — Policy D

- Source: `SRC-003`
- Location: lines 1413–1428; heading `Policy D`
- Domain tags: RISK, ACCOUNTING, INVENTORY, CAPITAL, BRIDGE, QUANT
- Source statement: Policy D: Déplacer seulement 50 % du capital. Ça nous permettra probablement d'améliorer énormément le Capital Engine.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Policy D` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0030`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, INVENTORY, CAPITAL, BRIDGE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0082 — Et on peut tester le temps

- Source: `SRC-003`
- Location: lines 1429–1461; heading `Et on peut tester le temps`
- Domain tags: EXECUTION, DATA, INFRA, ACCOUNTING, REPLAY, ROUTING
- Source statement: Et on peut tester le temps: Par exemple une route existe à : On veut voir ce qu'elle donne si notre ordre agit :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Et on peut tester le temps` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0077`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DATA, INFRA, ACCOUNTING, REPLAY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0083 — Limite importante

- Source: `SRC-003`
- Location: lines 1462–1466; heading `Limite importante`
- Domain tags: RISK, REPLAY
- Source statement: Limite importante: Si notre source n'a fourni qu'un nouvel état toutes les ~500 ms, on ne peut pas inventer le vrai carnet à T+20 ms. la qualité maximale du replay = la qualité maximale de la donnée enregistrée.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Limite importante` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0031`; supporting items: none found by conservative heading match; domain indexes `RISK, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0084 — On pourra également améliorer le simulateur lui-même

- Source: `SRC-003`
- Location: lines 1467–1508; heading `On pourra également améliorer le simulateur lui-même`
- Domain tags: EXECUTION, RISK, REPLAY, PRODUCT, ARCH, FUTURE
- Source statement: On pourra également améliorer le simulateur lui-même: C'est là que les données de production deviendront très importantes. Expected fill = 100 %
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `On pourra également améliorer le simulateur lui-même` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0078`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, REPLAY, PRODUCT, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0085 — On pourra même tester des idées qu'on n'avait pas encore au moment de l'enregistrement

- Source: `SRC-003`
- Location: lines 1509–1534; heading `On pourra même tester des idées qu'on n'avait pas encore au moment de l'enregistrement`
- Domain tags: ARCH, INFRA, REPLAY, BRIDGE, QUANT
- Source statement: On pourra même tester des idées qu'on n'avait pas encore au moment de l'enregistrement: C'est probablement la raison la plus importante de conserver le RAW. Dans trois mois, on invente :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `On pourra même tester des idées qu'on n'avait pas encore au moment de l'enregistrement` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0064`; supporting items: none found by conservative heading match; domain indexes `ARCH, INFRA, REPLAY, BRIDGE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0086 — Ce qu'on ne pourra jamais simuler parfaitement

- Source: `SRC-003`
- Location: lines 1535–1562; heading `Ce qu'on ne pourra jamais simuler parfaitement`
- Domain tags: RISK, VALIDATION, REPLAY
- Source statement: Ce qu'on ne pourra jamais simuler parfaitement: Il faut garder cette limite. Un replay historique ne peut pas reproduire parfaitement :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Ce qu'on ne pourra jamais simuler parfaitement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-RISK-0032`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0087 — Donc notre boucle d'amélioration finale devient très puissante

- Source: `SRC-003`
- Location: lines 1563–1595; heading `Donc notre boucle d'amélioration finale devient très puissante`
- Domain tags: EXECUTION, RECORDER, DATA, VALIDATION, REPLAY
- Source statement: Donc notre boucle d'amélioration finale devient très puissante: nouveaux marchés + vrais fills
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Donc notre boucle d'amélioration finale devient très puissante` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0079`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, DATA, VALIDATION, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0088 — À terme, on pourra quasiment demander au système

- Source: `SRC-003`
- Location: lines 1596–1612; heading `À terme, on pourra quasiment demander au système`
- Domain tags: EXECUTION, RISK, INFRA, ACCOUNTING, CAPITAL, BRIDGE, HOT_WARM_COLD, CROSS_EXCHANGE
- Source statement: À terme, on pourra quasiment demander au système: Pour ces 30 jours de marché, quelle politique aurait produit le meilleur résultat avec 1 000 €, tout en limitant le drawdown à X et le capital immobilisé à Y ? Quelle combinaison HOT/WARM/COLD minimise le CPU tout en gardant au moins 99 % des opportunités rentables ?
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `À terme, on pourra quasiment demander au système` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0080`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, ACCOUNTING, CAPITAL, BRIDGE, HOT_WARM_COLD, CROSS_EXCHANGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0089 — 1. Sur un même exchange : ce n’est pas rare du tout

- Source: `SRC-003`
- Location: lines 1613–1619; heading `1. Sur un même exchange : ce n’est pas rare du tout`
- Domain tags: OWA, TRIANGLE, PRODUCT, RESEARCH
- Source statement: 1. Sur un même exchange : ce n’est pas rare du tout: Le papier de Grimberg, Lauinger et McCoy sur Binance avait déjà trouvé 26,6 millions de conversions indirectes, représentant 2,71 % des trades, contre seulement 0,24 % attribués au triangular arbitrage. Autrement dit, dans leur échantillon, le 2-leg indirect était environ 11 fois plus répandu que le véritable triangle fermé. Ils mesuraient également un av…
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `1. Sur un même exchange : ce n’est pas rare du tout` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-OWA-0001`; supporting items: none found by conservative heading match; domain indexes `OWA, TRIANGLE, PRODUCT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0090 — 2. Mais d’où vient réellement ce profit ?

- Source: `SRC-003`
- Location: lines 1620–1697; heading `2. Mais d’où vient réellement ce profit ?`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, FORMULA, EXECUTION, ROUTING, QUANT
- Source statement: 2. Mais d’où vient réellement ce profit ?: Il faut être extrêmement précis. Ce qu’on cherche n’est pas nécessairement :
- Nature: formula/definition
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `2. Mais d’où vient réellement ce profit ?` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0033`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, FORMULA, EXECUTION, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0091 — 3. Pourquoi peut-il y avoir cette incohérence sur LE MÊME exchange ?

- Source: `SRC-003`
- Location: lines 1698–1728; heading `3. Pourquoi peut-il y avoir cette incohérence sur LE MÊME exchange ?`
- Domain tags: EXECUTION
- Source statement: 3. Pourquoi peut-il y avoir cette incohérence sur LE MÊME exchange ?: « Hyperliquid connaît tous ses marchés, donc BTC/HYPE × HYPE/ETH devrait toujours être égal à BTC/ETH. » * ses propres traders ;
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `3. Pourquoi peut-il y avoir cette incohérence sur LE MÊME exchange ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0081`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0092 — 4. Les études identifient plusieurs causes concrètes

- Source: `SRC-003`
- Location: lines 1729–1758; heading `4. Les études identifient plusieurs causes concrètes`
- Domain tags: RESEARCH, EXECUTION, PRODUCT, ARCH
- Source statement: 4. Les études identifient plusieurs causes concrètes: Le papier 2026 mentionne notamment les gros ordres qui épuisent momentanément un carnet, créant un déséquilibre sur cette paire sans que tous les autres marchés aient encore réagi. Il mentionne aussi la granularité des ticks de prix : certaines paires peuvent ne pas pouvoir refléter précisément la “bonne” valeur parce que les prix ne peuvent bouger que pa…
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `4. Les études identifient plusieurs causes concrètes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RESEARCH-0012`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, EXECUTION, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0093 — 5. Et il y a une autre source importante : la profondeur

- Source: `SRC-003`
- Location: lines 1759–1762; heading `5. Et il y a une autre source importante : la profondeur`
- Domain tags: ARCH
- Source statement: 5. Et il y a une autre source importante : la profondeur: Celle-là est particulièrement importante pour notre bot. Même si les mid-prices sont parfaitement cohérents, les prix exécutables peuvent ne pas l’être.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `5. Et il y a une autre source importante : la profondeur` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ARCH-0065`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0094 — Direct BTC → ETH

- Source: `SRC-003`
- Location: lines 1763–1772; heading `Direct BTC → ETH`
- Domain tags: ARCH
- Source statement: Direct BTC → ETH: Pour convertir 1 000 €, on obtient un mauvais prix moyen.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Direct BTC → ETH` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ARCH-0066`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0095 — BTC → HYPE

- Source: `SRC-003`
- Location: lines 1773–1775; heading `BTC → HYPE`
- Domain tags: ARCH
- Source statement: BTC → HYPE: très liquide. Puis :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `BTC → HYPE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0067`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0096 — HYPE → ETH

- Source: `SRC-003`
- Location: lines 1776–1785; heading `HYPE → ETH`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE, OWA, PRODUCT, RESEARCH
- Source statement: HYPE → ETH: Le détour peut finalement produire plus d’ETH. Donc notre scanner ne doit pas simplement chercher :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `HYPE → ETH` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RISK-0033`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE, OWA, PRODUCT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0097 — 6. Et le phénomène est suffisamment fréquent pour être automatisé à très haute vitesse

- Source: `SRC-003`
- Location: lines 1786–1801; heading `6. Et le phénomène est suffisamment fréquent pour être automatisé à très haute vitesse`
- Domain tags: EXECUTION, INFRA, TRIANGLE, ROUTING, GRAPH, HOT_WARM_COLD, PRODUCT, ARCH
- Source statement: 6. Et le phénomène est suffisamment fréquent pour être automatisé à très haute vitesse: Le papier 2026 montre que sur Binance, pour les séquences taker/taker, environ 80,3 % du volume et 82,6 % des gains détectés se situaient dans les séquences dont les deux opérations étaient espacées de 35 ms ou moins. Avec le temps, une grande partie de l’activité s’est déplacée jusque dans la tranche 0–10 ms, signe d’une compétition de plus en plus forte…
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `6. Et le phénomène est suffisamment fréquent pour être automatisé à très haute vitesse` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0082`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, TRIANGLE, ROUTING, GRAPH, HOT_WARM_COLD, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0098 — 7. Mais attention : les profits individuels ont énormément diminué

- Source: `SRC-003`
- Location: lines 1802–1819; heading `7. Mais attention : les profits individuels ont énormément diminué`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, EXECUTION, PRODUCT, RESEARCH
- Source statement: 7. Mais attention : les profits individuels ont énormément diminué: C’est là où le papier 2026 est beaucoup plus intéressant que l’ancien. Les données plus récentes montrent qu’en Q2 2023, l’écart brut moyen détecté sur Binance n’était plus que d’environ 3,8 bps, contre environ 20,4 bps sur Kraken. Les auteurs interprètent cette compression comme un signe de marché Binance plus mature/compétitif. (arXiv)
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `7. Mais attention : les profits individuels ont énormément diminué` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ACCT-0034`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, EXECUTION, PRODUCT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0099 — 8. Et ça change notre raisonnement sur le PnL

- Source: `SRC-003`
- Location: lines 1820–1860; heading `8. Et ça change notre raisonnement sur le PnL`
- Domain tags: ACCOUNTING, MARKET_ATLAS
- Source statement: 8. Et ça change notre raisonnement sur le PnL: Imaginons que notre bot trouve : Un autre système pourrait trouver :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `8. Et ça change notre raisonnement sur le PnL` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ACCT-0035`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MARKET_ATLAS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0100 — 9. Maintenant : multi-exchange

- Source: `SRC-003`
- Location: lines 1861–1887; heading `9. Maintenant : multi-exchange`
- Domain tags: CROSS_EXCHANGE, OWA, PRODUCT
- Source statement: 9. Maintenant : multi-exchange: Là on parle d’une autre famille. Hyperliquid BTC = 100 000
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `9. Maintenant : multi-exchange` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-XEX-0001`; supporting items: none found by conservative heading match; domain indexes `CROSS_EXCHANGE, OWA, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0101 — 10. Est-ce que les écarts multi-exchange arrivent aussi ?

- Source: `SRC-003`
- Location: lines 1888–1894; heading `10. Est-ce que les écarts multi-exchange arrivent aussi ?`
- Domain tags: CROSS_EXCHANGE, RESEARCH
- Source statement: 10. Est-ce que les écarts multi-exchange arrivent aussi ?: Makarov et Schoar ont documenté des écarts importants et récurrents entre exchanges, et montrent qu’ils sont historiquement beaucoup plus importants entre pays/régions qu’entre marchés d’un même environnement. (SSRN) À l’extrême, pendant le fameux Kimchi Premium de 2017–2018, ils observent notamment des prix coréens supérieurs de plus de 15 % en moyenne sur une période, avec des écarts atteignant environ 40 % plusieurs jours. (ResearchGate)
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `10. Est-ce que les écarts multi-exchange arrivent aussi ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-XEX-0002`; supporting items: none found by conservative heading match; domain indexes `CROSS_EXCHANGE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0102 — 11. Le problème cross-exchange : le capital doit être présent AVANT l'opportunité

- Source: `SRC-003`
- Location: lines 1895–1939; heading `11. Le problème cross-exchange : le capital doit être présent AVANT l'opportunité`
- Domain tags: EXECUTION, CAPITAL, CROSS_EXCHANGE, ACCOUNTING, MICROSTRUCTURE, PRODUCT, RESEARCH
- Source statement: 11. Le problème cross-exchange : le capital doit être présent AVANT l'opportunité: La mauvaise stratégie serait : Makarov et Schoar soulignent précisément que les transferts de crypto/fiat peuvent prendre suffisamment longtemps pour que l’opportunité disparaisse. Pour verrouiller immédiatement l’arbitrage, il faut acheter sur le marché bon marché et vendre simultanément sur le marché cher. (ResearchGate)
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `11. Le problème cross-exchange : le capital doit être présent AVANT l'opportunité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0083`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CAPITAL, CROSS_EXCHANGE, ACCOUNTING, MICROSTRUCTURE, PRODUCT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0103 — 12. Mais le capital se déséquilibre

- Source: `SRC-003`
- Location: lines 1940–1941; heading `12. Mais le capital se déséquilibre`
- Domain tags: CAPITAL
- Source statement: 12. Mais le capital se déséquilibre: Après plusieurs arbitrages :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `12. Mais le capital se déséquilibre` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0015`; supporting items: none found by conservative heading match; domain indexes `CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0104 — Hyperliquid

- Source: `SRC-003`
- Location: lines 1942–1947; heading `Hyperliquid`
- Domain tags: ARCH
- Source statement: Hyperliquid: BTC ↑ USDC ↓
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Hyperliquid` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0068`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0105 — Binance

- Source: `SRC-003`
- Location: lines 1948–1968; heading `Binance`
- Domain tags: RISK, INVENTORY, CAPITAL, BRIDGE, ROUTING, RESEARCH
- Source statement: Binance: Donc tôt ou tard : Binance n'a plus de BTC
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Binance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RISK-0034`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, CAPITAL, BRIDGE, ROUTING, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0106 — 13. Donc quel type produit les plus gros écarts ?

- Source: `SRC-003`
- Location: lines 1969–1988; heading `13. Donc quel type produit les plus gros écarts ?`
- Domain tags: RISK, CAPITAL, OWA, CROSS_EXCHANGE, RESEARCH
- Source statement: 13. Donc quel type produit les plus gros écarts ?: En général, les recherches indiquent : Même exchange OWA | Cross-exchange
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `13. Donc quel type produit les plus gros écarts ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0035`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, OWA, CROSS_EXCHANGE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0107 — 14. Il existe aussi des inefficiences ultra-courtes ENTRE exchanges

- Source: `SRC-003`
- Location: lines 1989–2010; heading `14. Il existe aussi des inefficiences ultra-courtes ENTRE exchanges`
- Domain tags: QUANT, ARCH, FUTURE
- Source statement: 14. Il existe aussi des inefficiences ultra-courtes ENTRE exchanges: Et ça nous intéresse pour plus tard. Albers et al. ont étudié les carnets de plusieurs marchés Bitcoin à une granularité sub-seconde. Ils trouvent une structure leader/lagger entre exchanges et arrivent à expliquer entre 10 % et 37 % des variations de rendement à 500 ms selon le marché cible. Ils montrent également que les frais jouent un rôle important dans la possibilité de monétiser ces d…
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `14. Il existe aussi des inefficiences ultra-courtes ENTRE exchanges` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-QUANT-0005`; supporting items: none found by conservative heading match; domain indexes `QUANT, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0108 — 15. Maintenant la question essentielle : lequel pour NOTRE projet ?

- Source: `SRC-003`
- Location: lines 2011–2045; heading `15. Maintenant la question essentielle : lequel pour NOTRE projet ?`
- Domain tags: SECURITY, INVENTORY, CAPITAL, BRIDGE, TRIANGLE, GRAPH, HOT_WARM_COLD, ARCH
- Source statement: 15. Maintenant la question essentielle : lequel pour NOTRE projet ?: Je pense qu’on a raison de commencer avec l’interne Hyperliquid. Parce que notre architecture actuelle est presque faite sur mesure pour ça :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `15. Maintenant la question essentielle : lequel pour NOTRE projet ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SEC-0002`; supporting items: none found by conservative heading match; domain indexes `SECURITY, INVENTORY, CAPITAL, BRIDGE, TRIANGLE, GRAPH, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0109 — 16. Mais je ferais une modification architecture MAINTENANT

- Source: `SRC-003`
- Location: lines 2046–2047; heading `16. Mais je ferais une modification architecture MAINTENANT`
- Domain tags: ARCH, PRODUCT, FUTURE
- Source statement: 16. Mais je ferais une modification architecture MAINTENANT: Puisqu’on veut une V1 qui ne nécessite pas une refonte plus tard :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `16. Mais je ferais une modification architecture MAINTENANT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ARCH-0069`; supporting items: none found by conservative heading match; domain indexes `ARCH, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0110 — rendre le graphe venue-aware.

- Source: `SRC-003`
- Location: lines 2048–2104; heading `rendre le graphe venue-aware.`
- Domain tags: GRAPH, CROSS_EXCHANGE, RISK, INFRA, ACCOUNTING, INVENTORY, FUTURE
- Source statement: rendre le graphe venue-aware: Au lieu d’avoir uniquement : on peut conceptuellement avoir :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `rendre le graphe venue-aware.` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-GRAPH-0013`; supporting items: none found by conservative heading match; domain indexes `GRAPH, CROSS_EXCHANGE, RISK, INFRA, ACCOUNTING, INVENTORY, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0111 — 17. Et surtout : je veux maintenant distinguer 3 choses dans notre “2-leg”

- Source: `SRC-003`
- Location: lines 2105–2120; heading `17. Et surtout : je veux maintenant distinguer 3 choses dans notre “2-leg”`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, INVENTORY, CAPITAL, BRIDGE, ROUTING, QUANT, PRODUCT
- Source statement: 17. Et surtout : je veux maintenant distinguer 3 choses dans notre “2-leg”: C’est probablement la conclusion la plus importante de cette recherche. Type | Exemple | Ce qu’on gagne
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `17. Et surtout : je veux maintenant distinguer 3 choses dans notre “2-leg”` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ACCT-0036`; supporting items: SRC-008-ITEM-0070; domain indexes `ACCOUNTING, MICROSTRUCTURE, INVENTORY, CAPITAL, BRIDGE, ROUTING, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0112 — 18. Et le papier de 2020 nous donne même une information essentielle sur la concurrence

- Source: `SRC-003`
- Location: lines 2121–2155; heading `18. Et le papier de 2020 nous donne même une information essentielle sur la concurrence`
- Domain tags: RESEARCH, EXECUTION, RECOVERY, RISK, INFRA, ROUTING, QUANT
- Source statement: 18. Et le papier de 2020 nous donne même une information essentielle sur la concurrence: Ils ont observé que 6,08 % des conversions indirectes identifiées étaient défavorables par rapport à la route directe. Leur hypothèse est notamment que plusieurs bots capturaient simultanément la même opportunité : le premier consommait la capacité du carnet, et le retardataire se retrouvait avec l’asset intermédiaire et devait sortir à moins bon prix. (a…
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `18. Et le papier de 2020 nous donne même une information essentielle sur la concurrence` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RESEARCH-0013`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, EXECUTION, RECOVERY, RISK, INFRA, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0113 — 19. Ils ont même observé comment les bots géraient la perte

- Source: `SRC-003`
- Location: lines 2156–2183; heading `19. Ils ont même observé comment les bots géraient la perte`
- Domain tags: EXECUTION, RECOVERY, GRAPH, RESEARCH
- Source statement: 19. Ils ont même observé comment les bots géraient la perte: Le papier identifie deux comportements : full exit : liquider entièrement l’intermédiaire vers la destination, même à perte ;
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `19. Ils ont même observé comment les bots géraient la perte` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0084`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, GRAPH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0114 — Ma conclusion pour notre projet

- Source: `SRC-003`
- Location: lines 2184–2214; heading `Ma conclusion pour notre projet`
- Domain tags: EXECUTION, RECORDER, ACCOUNTING, INVENTORY, CAPITAL, OWA, TRIANGLE, ROUTING
- Source statement: Ma conclusion pour notre projet: La recherche renforce énormément la direction qu’on prend. Le same-exchange 2-leg doit être une stratégie de premier rang, pas une fonctionnalité secondaire. Il existe historiquement à grande échelle, il semble plus fréquent que le triangle fermé, mais ses marges sont devenues minuscules et nécessitent vitesse + frais faibles + très gros volume de décisions. (arXiv)
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Ma conclusion pour notre projet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0085`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, ACCOUNTING, INVENTORY, CAPITAL, OWA, TRIANGLE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0116 — 1. Définition exacte : qu’est-ce qu’un vrai OWA 2-leg ?

- Source: `SRC-003`
- Location: lines 2216–2232; heading `1. Définition exacte : qu’est-ce qu’un vrai OWA 2-leg ?`
- Domain tags: OWA, TRIANGLE, ROUTING
- Source statement: 1. Définition exacte : qu’est-ce qu’un vrai OWA 2-leg ?: Un OWA (*One-Way Arbitrage*) doit avoir : un actif de départ A, un actif intermédiaire X, un actif final B, et une route directe A → B permettant la comparaison.
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `1. Définition exacte : qu’est-ce qu’un vrai OWA 2-leg ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OWA-0002`; supporting items: none found by conservative heading match; domain indexes `OWA, TRIANGLE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0117 — 2. Première correction importante

- Source: `SRC-003`
- Location: lines 2233–2252; heading `2. Première correction importante`
- Domain tags: ACCOUNTING, MICROSTRUCTURE
- Source statement: 2. Première correction importante: On ne doit PAS dire : BTC → HYPE → ETH rapporte +0,10 %.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `2. Première correction importante` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ACCT-0037`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0118 — 3. Fonction fondamentale : NetConvert()

- Source: `SRC-003`
- Location: lines 2253–2282; heading `3. Fonction fondamentale : NetConvert()`
- Domain tags: ROUTING, RISK, ACCOUNTING, ARCH
- Source statement: 3. Fonction fondamentale : NetConvert(): Tout doit reposer sur une seule primitive Rust. Elle doit intégrer simultanément :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `3. Fonction fondamentale : NetConvert()` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ROUTE-0022`; supporting items: none found by conservative heading match; domain indexes `ROUTING, RISK, ACCOUNTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0119 — 4. Exemple SELL

- Source: `SRC-003`
- Location: lines 2283–2319; heading `4. Exemple SELL`
- Domain tags: PRODUCT, ACCOUNTING
- Source statement: 4. Exemple SELL: Si on vend 50 HYPE : On obtient le véritable output_USDC.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `4. Exemple SELL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0012`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0120 — 5. Exemple BUY

- Source: `SRC-003`
- Location: lines 2320–2333; heading `5. Exemple BUY`
- Domain tags: GRAPH, PRODUCT
- Source statement: 5. Exemple BUY: Si nous possédons USDC et voulons HYPE : Chaque marché crée bien deux edges directionnels différents dans notre graphe.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `5. Exemple BUY` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-GRAPH-0014`; supporting items: none found by conservative heading match; domain indexes `GRAPH, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0121 — 6. Calcul du DIRECT

- Source: `SRC-003`
- Location: lines 2334–2354; heading `6. Calcul du DIRECT`
- Domain tags: ROUTING, QUANT
- Source statement: 6. Calcul du DIRECT: Pour une quantité initiale qA :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `6. Calcul du DIRECT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0023`; supporting items: none found by conservative heading match; domain indexes `ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0122 — 7. Calcul de l’INDIRECT

- Source: `SRC-003`
- Location: lines 2355–2388; heading `7. Calcul de l’INDIRECT`
- Domain tags: ROUTING
- Source statement: 7. Calcul de l’INDIRECT: Première jambe : qX =
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `7. Calcul de l’INDIRECT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0024`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0123 — 8. Edge OWA véritable

- Source: `SRC-003`
- Location: lines 2389–2421; heading `8. Edge OWA véritable`
- Domain tags: OWA
- Source statement: 8. Edge OWA véritable: I(qA) / D(qA) - 1 29.025 / 29.000 - 1
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `8. Edge OWA véritable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OWA-0003`; supporting items: none found by conservative heading match; domain indexes `OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0124 — 9. Les fees ne sont jamais ajoutés “à la louche”

- Source: `SRC-003`
- Location: lines 2422–2443; heading `9. Les fees ne sont jamais ajoutés “à la louche”`
- Domain tags: ACCOUNTING, EXECUTION, ROUTING
- Source statement: 9. Les fees ne sont jamais ajoutés “à la louche”: Hyperliquid possède actuellement des frais spot dépendant notamment du tier du compte, maker/taker, du staking, du type de quote asset et de certaines caractéristiques de la paire. Le tier spot de base est actuellement de 0,070 % taker et 0,040 % maker ; les paires entre deux quote assets bénéficient notamment d’une réduction de 80 % sur les frais taker.
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `9. Les fees ne sont jamais ajoutés “à la louche”` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ACCT-0038`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, EXECUTION, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0125 — 10. Le benchmark DIRECT doit être équitable

- Source: `SRC-003`
- Location: lines 2444–2459; heading `10. Le benchmark DIRECT doit être équitable`
- Domain tags: BENCHMARK, EXECUTION, OWA
- Source statement: 10. Le benchmark DIRECT doit être équitable: Correction très importante par rapport à nos explications précédentes. On ne peut pas comparer :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `10. Le benchmark DIRECT doit être équitable` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BENCH-0005`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, EXECUTION, OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0126 — 11. Famille IMMEDIATE_OWA

- Source: `SRC-003`
- Location: lines 2460–2485; heading `11. Famille IMMEDIATE_OWA`
- Domain tags: EXECUTION
- Source statement: 11. Famille IMMEDIATE_OWA: C’est la comparaison la plus propre pour mesurer une anomalie immédiatement exploitable.
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `11. Famille IMMEDIATE_OWA` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0086`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0127 — 12. Famille PASSIVE_OWA

- Source: `SRC-003`
- Location: lines 2486–2510; heading `12. Famille PASSIVE_OWA`
- Domain tags: EXECUTION, MAKER_MODEL
- Source statement: 12. Famille PASSIVE_OWA: on accepte d’attendre un fill maker. Là on peut comparer par exemple :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `12. Famille PASSIVE_OWA` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0087`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0128 — 13. Plans d’exécution 2-leg que l’on GARDE

- Source: `SRC-003`
- Location: lines 2511–2525; heading `13. Plans d’exécution 2-leg que l’on GARDE`
- Domain tags: EXECUTION, PRODUCT
- Source statement: 13. Plans d’exécution 2-leg que l’on GARDE: Pour notre cœur V1 : Ce sont nos deux principaux plans.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `13. Plans d’exécution 2-leg que l’on GARDE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0088`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0129 — 14. Plans que l’on N’UTILISE PAS par défaut

- Source: `SRC-003`
- Location: lines 2526–2561; heading `14. Plans que l’on N’UTILISE PAS par défaut`
- Domain tags: EXECUTION, INFRA, ARCH, RESEARCH
- Source statement: 14. Plans que l’on N’UTILISE PAS par défaut: ne doivent pas faire partie du cœur normal du bot. Après le premier taker :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `14. Plans que l’on N’UTILISE PAS par défaut` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0089`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ARCH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0130 — 15. Un OWA n’existe PAS sans comparateur

- Source: `SRC-003`
- Location: lines 2562–2596; heading `15. Un OWA n’existe PAS sans comparateur`
- Domain tags: OWA, CAPITAL, BRIDGE, ROUTING
- Source statement: 15. Un OWA n’existe PAS sans comparateur: On ne peut pas appeler ça : puisqu’il n’existe aucun taux direct à battre.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `15. Un OWA n’existe PAS sans comparateur` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OWA-0004`; supporting items: none found by conservative heading match; domain indexes `OWA, CAPITAL, BRIDGE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0131 — 16. Deuxième distinction essentielle : OWA vs relocation

- Source: `SRC-003`
- Location: lines 2597–2615; heading `16. Deuxième distinction essentielle : OWA vs relocation`
- Domain tags: BRIDGE, OWA, CAPITAL, FUTURE
- Source statement: 16. Deuxième distinction essentielle : OWA vs relocation: et l’indirect nous donne effectivement davantage d’ETH que BTC → ETH. Il y a bien :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `16. Deuxième distinction essentielle : OWA vs relocation` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-BRIDGE-0008`; supporting items: none found by conservative heading match; domain indexes `BRIDGE, OWA, CAPITAL, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0132 — 17. ConversionAlpha

- Source: `SRC-003`
- Location: lines 2616–2627; heading `17. ConversionAlpha`
- Domain tags: ROUTING
- Source statement: 17. ConversionAlpha: Quelle route convertit A vers B le plus efficacement maintenant ?
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `17. ConversionAlpha` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0025`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0133 — 18. RelocationValue

- Source: `SRC-003`
- Location: lines 2628–2641; heading `18. RelocationValue`
- Domain tags: BRIDGE, CAPITAL, FUTURE
- Source statement: 18. RelocationValue: Est-ce économiquement préférable que mon capital vive maintenant en B plutôt qu’en A ? Il prend en compte :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `18. RelocationValue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-BRIDGE-0009`; supporting items: none found by conservative heading match; domain indexes `BRIDGE, CAPITAL, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0134 — 19. Pourquoi ?

- Source: `SRC-003`
- Location: lines 2642–2660; heading `19. Pourquoi ?`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, ROUTING
- Source statement: 19. Pourquoi ?: Sinon nous pourrions écrire : et considérer le trade excellent.
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `19. Pourquoi ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0039`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0135 — 20. Classification des assets

- Source: `SRC-003`
- Location: lines 2661–2674; heading `20. Classification des assets`
- Domain tags: INVENTORY, MARKET_ATLAS, ARCH
- Source statement: 20. Classification des assets: La littérature récente raisonne avec des *anchor coins* liquides comme BTC, ETH ou stablecoins comme actifs de départ/arrivée et des coins moins liquides comme intermédiaires. Nous reprenons l’idée, mais PAS les classifications Binance.
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `20. Classification des assets` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0009`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, MARKET_ATLAS, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0136 — 21. CORE_INVENTORY

- Source: `SRC-003`
- Location: lines 2675–2689; heading `21. CORE_INVENTORY`
- Domain tags: INVENTORY, ARCH, RISK, CAPITAL, ROUTING, MARKET_ATLAS
- Source statement: 21. CORE_INVENTORY: Asset sur lequel notre capital peut normalement terminer. volatilité compatible avec nos limites
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `21. CORE_INVENTORY` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INV-0010`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, ARCH, RISK, CAPITAL, ROUTING, MARKET_ATLAS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0137 — 22. TRANSIT

- Source: `SRC-003`
- Location: lines 2690–2709; heading `22. TRANSIT`
- Domain tags: RECOVERY
- Source statement: 22. TRANSIT: Asset que nous acceptons comme : mais pas comme destination normale.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `22. TRANSIT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0008`; supporting items: none found by conservative heading match; domain indexes `RECOVERY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0138 — 23. EXCLUDED

- Source: `SRC-003`
- Location: lines 2710–2721; heading `23. EXCLUDED`
- Domain tags: ACCOUNTING
- Source statement: 23. EXCLUDED: Pas utilisé, même comme intermédiaire si le risque économique dépasse l’intérêt.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `23. EXCLUDED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0040`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0139 — 24. Terminal Viability Gate

- Source: `SRC-003`
- Location: lines 2722–2750; heading `24. Terminal Viability Gate`
- Domain tags: BRIDGE, MARKET_ATLAS, OWA, ROUTING
- Source statement: 24. Terminal Viability Gate: Donc un excellent OWA peut être rejeté :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `24. Terminal Viability Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-BRIDGE-0010`; supporting items: SRC-005-ITEM-0075, SRC-006-ITEM-0372; domain indexes `BRIDGE, MARKET_ATLAS, OWA, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0140 — 25. Cela résout notre problème des “40 opportunités”

- Source: `SRC-003`
- Location: lines 2751–2765; heading `25. Cela résout notre problème des “40 opportunités”`
- Domain tags: EXECUTION, ROUTING, ARCH
- Source statement: 25. Cela résout notre problème des “40 opportunités”: Supposons qu’on prenne 40 fois : Au bout d’un moment, le moteur doit pénaliser les routes qui produisent encore plus d’ETH.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `25. Cela résout notre problème des “40 opportunités”` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0090`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0141 — 26. Inventaire avant/après

- Source: `SRC-003`
- Location: lines 2766–2790; heading `26. Inventaire avant/après`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, PORTFOLIO, ROUTING
- Source statement: 26. Inventaire avant/après: On ne demande donc pas seulement :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `26. Inventaire avant/après` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0041`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, PORTFOLIO, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0142 — 27. Inventory bands

- Source: `SRC-003`
- Location: lines 2791–2811; heading `27. Inventory bands`
- Domain tags: INVENTORY, INFRA, REPLAY, ARCH
- Source statement: 27. Inventory bands: Pour chaque CORE asset : ETH target = 25 %
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `27. Inventory bands` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INV-0011`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, INFRA, REPLAY, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0143 — 28. Effet des limites

- Source: `SRC-003`
- Location: lines 2812–2843; heading `28. Effet des limites`
- Domain tags: RISK, RECOVERY, INVENTORY, ROUTING
- Source statement: 28. Effet des limites: Si ETH est à : une route finissant ETH :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `28. Effet des limites` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0036`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0144 — 29. Flow control

- Source: `SRC-003`
- Location: lines 2844–2867; heading `29. Flow control`
- Domain tags: RISK, ARCH
- Source statement: 29. Flow control: On ne regarde pas seulement le stock. On regarde également la vitesse à laquelle il dérive.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `29. Flow control` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0037`; supporting items: none found by conservative heading match; domain indexes `RISK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0145 — 30. Valeur d’une route ajustée à l’inventaire

- Source: `SRC-003`
- Location: lines 2868–2888; heading `30. Valeur d’une route ajustée à l’inventaire`
- Domain tags: ROUTING, INVENTORY, CAPITAL, PORTFOLIO
- Source statement: 30. Valeur d’une route ajustée à l’inventaire: Notre route possède d’abord : Une route légèrement moins rentable mais qui nous rééquilibre peut donc battre une route qui augmente un mauvais déséquilibre.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `30. Valeur d’une route ajustée à l’inventaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0026`; supporting items: none found by conservative heading match; domain indexes `ROUTING, INVENTORY, CAPITAL, PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0146 — 31. Attention : ce n’est PAS une autorisation de perdre

- Source: `SRC-003`
- Location: lines 2889–2905; heading `31. Attention : ce n’est PAS une autorisation de perdre`
- Domain tags: ACCOUNTING, INVENTORY, CAPITAL, OWA, ROUTING
- Source statement: 31. Attention : ce n’est PAS une autorisation de perdre: On ne prend pas automatiquement A. Une stratégie de rebalance perdante est gérée explicitement par :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `31. Attention : ce n’est PAS une autorisation de perdre` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ACCT-0042`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, INVENTORY, CAPITAL, OWA, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0147 — 32. Risque d’exécution entre Leg1 et Leg2

- Source: `SRC-003`
- Location: lines 2906–2925; heading `32. Risque d’exécution entre Leg1 et Leg2`
- Domain tags: RESEARCH
- Source statement: 32. Risque d’exécution entre Leg1 et Leg2: au moment de la détection, nous devons tenir compte du fait que : Le papier de 2020 identifie précisément ce phénomène : plusieurs traders peuvent viser la même deuxième conversion, le premier consomme la meilleure capacité du carnet et le trader retardataire se retrouve avec l’intermédiaire à liquider à un taux moins favorable.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `32. Risque d’exécution entre Leg1 et Leg2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0014`; supporting items: none found by conservative heading match; domain indexes `RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0148 — 33. Donc edge > 0 ne suffit jamais

- Source: `SRC-003`
- Location: lines 2926–2952; heading `33. Donc edge > 0 ne suffit jamais`
- Domain tags: RECOVERY, ACCOUNTING
- Source statement: 33. Donc edge > 0 ne suffit jamais: On définit : P_full_completion
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `33. Donc edge > 0 ne suffit jamais` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0009`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0149 — 34. Version plus complète

- Source: `SRC-003`
- Location: lines 2953–2978; heading `34. Version plus complète`
- Domain tags: EXECUTION, RECOVERY, RISK, INFRA, ROUTING
- Source statement: 34. Version plus complète: Le routeur n’exécute que si : ET tous les Risk Gates passent.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `34. Version plus complète` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0091`; supporting items: SRC-007-ITEM-0184; domain indexes `EXECUTION, RECOVERY, RISK, INFRA, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0150 — 35. Recovery n’est pas forcément X → B coûte que coûte

- Source: `SRC-003`
- Location: lines 2979–2993; heading `35. Recovery n’est pas forcément X → B coûte que coûte`
- Domain tags: RECOVERY, EXECUTION, RESEARCH
- Source statement: 35. Recovery n’est pas forcément X → B coûte que coûte: Le papier de 2020 observe justement deux comportements après une conversion ratée : tout l’intermédiaire vers une destination,
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `35. Recovery n’est pas forcément X → B coûte que coûte` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0010`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, EXECUTION, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0151 — 36. Notre Recovery Engine cherche le minimum de perte

- Source: `SRC-003`
- Location: lines 2994–3019; heading `36. Notre Recovery Engine cherche le minimum de perte`
- Domain tags: RECOVERY, RISK, INFRA, ACCOUNTING, INVENTORY
- Source statement: 36. Notre Recovery Engine cherche le minimum de perte: Si on est bloqué avec X : Il peut donc répartir la sortie.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `36. Notre Recovery Engine cherche le minimum de perte` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0011`; supporting items: SRC-006-ITEM-0397; domain indexes `RECOVERY, RISK, INFRA, ACCOUNTING, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0152 — 37. Latence : ce que les papiers nous apprennent réellement

- Source: `SRC-003`
- Location: lines 3020–3023; heading `37. Latence : ce que les papiers nous apprennent réellement`
- Domain tags: RESEARCH, EXECUTION, DATA, OWA
- Source statement: 37. Latence : ce que les papiers nous apprennent réellement: Le papier de 2020 observe une latence moyenne d’environ 21,43 ms entre les deux opérations d’indirect conversions et 78,94 % sous 30 ms dans son dataset Binance. Le papier de 2026 constate sur Binance que 80,3 % du volume taker/taker et 82,6 % des gains étudiés se concentraient dans les séquences ≤35 ms, tandis que les pertes se concentraient davantage aux latences supérieures.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `37. Latence : ce que les papiers nous apprennent réellement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0015`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, EXECUTION, DATA, OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0153 — 38. Ce qu’on NE fait PAS avec cette information

- Source: `SRC-003`
- Location: lines 3024–3046; heading `38. Ce qu’on NE fait PAS avec cette information`
- Domain tags: EXECUTION, RECORDER, INFRA, SURVIVAL
- Source statement: 38. Ce qu’on NE fait PAS avec cette information: On ne code PAS : Ces chiffres montrent seulement :
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `38. Ce qu’on NE fait PAS avec cette information` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-EXEC-0092`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0154 — 39. Sizing : une route n’a jamais une rentabilité unique

- Source: `SRC-003`
- Location: lines 3047–3070; heading `39. Sizing : une route n’a jamais une rentabilité unique`
- Domain tags: SIZING, ROUTING
- Source statement: 39. Sizing : une route n’a jamais une rentabilité unique: 1 000 € +2 bps 1 500 € -3 bps
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `39. Sizing : une route n’a jamais une rentabilité unique` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIZE-0001`; supporting items: none found by conservative heading match; domain indexes `SIZING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0155 — 40. Fonction de capacité

- Source: `SRC-003`
- Location: lines 3071–3083; heading `40. Fonction de capacité`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE, QUANT
- Source statement: 40. Fonction de capacité: pour toutes les quantités jusqu’à la capacité choisie.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `40. Fonction de capacité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0038`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0156 — 41. Contraintes du sizing

- Source: `SRC-003`
- Location: lines 3084–3100; heading `41. Contraintes du sizing`
- Domain tags: SIZING, RECOVERY, RISK, INVENTORY, CAPITAL
- Source statement: 41. Contraintes du sizing: La taille finale est limitée par :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `41. Contraintes du sizing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-SIZE-0002`; supporting items: SRC-007-ITEM-0236; domain indexes `SIZING, RECOVERY, RISK, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0157 — 42. On ne fixe donc PAS 50 € comme taille économique

- Source: `SRC-003`
- Location: lines 3101–3119; heading `42. On ne fixe donc PAS 50 € comme taille économique`
- Domain tags: RISK, VALIDATION
- Source statement: 42. On ne fixe donc PAS 50 € comme taille économique: Notre commentaire précédent sur 40–50 € est conservé uniquement dans deux cas : n'est pas une règle de stratégie.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `42. On ne fixe donc PAS 50 € comme taille économique` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0039`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0158 — 43. Fragmentation : ce qu’on garde

- Source: `SRC-003`
- Location: lines 3120–3141; heading `43. Fragmentation : ce qu’on garde`
- Domain tags: SLICING, CAPITAL, ROUTING
- Source statement: 43. Fragmentation : ce qu’on garde: c’est-à-dire utiliser notre capital sur plusieurs opportunités indépendantes. sur la seule route A.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `43. Fragmentation : ce qu’on garde` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SLICE-0001`; supporting items: none found by conservative heading match; domain indexes `SLICING, CAPITAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0159 — 44. Ce qu’on ne garde PAS

- Source: `SRC-003`
- Location: lines 3142–3161; heading `44. Ce qu’on ne garde PAS`
- Domain tags: SLICING
- Source statement: 44. Ce qu’on ne garde PAS: 1 × 2 000 € simultanément sur exactement le même carnet ne crée pas magiquement plus de profondeur.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `44. Ce qu’on ne garde PAS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-SLICE-0002`; supporting items: none found by conservative heading match; domain indexes `SLICING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0160 — 45. Shared Capacity

- Source: `SRC-003`
- Location: lines 3162–3187; heading `45. Shared Capacity`
- Domain tags: CAPITAL, PORTFOLIO, EXECUTION, ROUTING
- Source statement: 45. Shared Capacity: Deux routes différentes peuvent utiliser le même carnet. Si le carnet possède seulement :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `45. Shared Capacity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0016`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, PORTFOLIO, EXECUTION, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0161 — 46. Reservation Engine

- Source: `SRC-003`
- Location: lines 3188–3205; heading `46. Reservation Engine`
- Domain tags: INVENTORY, CAPITAL, ROUTING
- Source statement: 46. Reservation Engine: Même principe pour les balances.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `46. Reservation Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INV-0012`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, CAPITAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0162 — 47. Le moteur ne sélectionne donc plus “la meilleure route”

- Source: `SRC-003`
- Location: lines 3206–3236; heading `47. Le moteur ne sélectionne donc plus “la meilleure route”`
- Domain tags: ROUTING, RISK, ACCOUNTING, INVENTORY, CAPITAL, PORTFOLIO
- Source statement: 47. Le moteur ne sélectionne donc plus “la meilleure route”: le meilleur ensemble de routes la meilleure taille pour chacune
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `47. Le moteur ne sélectionne donc plus “la meilleure route”` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ROUTE-0027`; supporting items: none found by conservative heading match; domain indexes `ROUTING, RISK, ACCOUNTING, INVENTORY, CAPITAL, PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0163 — 48. Cross-exchange 2-leg : définition séparée

- Source: `SRC-003`
- Location: lines 3237–3262; heading `48. Cross-exchange 2-leg : définition séparée`
- Domain tags: CROSS_EXCHANGE, OWA, PRODUCT
- Source statement: 48. Cross-exchange 2-leg : définition séparée: Il ne faut pas mélanger ça avec l’OWA. Ce sont bien deux opérations, mais ce n’est pas :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `48. Cross-exchange 2-leg : définition séparée` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XEX-0003`; supporting items: none found by conservative heading match; domain indexes `CROSS_EXCHANGE, OWA, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0164 — 49. Calcul cross-exchange

- Source: `SRC-003`
- Location: lines 3263–3291; heading `49. Calcul cross-exchange`
- Domain tags: CROSS_EXCHANGE, ACCOUNTING, QUANT, PRODUCT
- Source statement: 49. Calcul cross-exchange: Pour une quantité qBTC :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `49. Calcul cross-exchange` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XEX-0004`; supporting items: none found by conservative heading match; domain indexes `CROSS_EXCHANGE, ACCOUNTING, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0165 — 50. Mais il existe un coût caché : le déséquilibre de venue

- Source: `SRC-003`
- Location: lines 3292–3314; heading `50. Mais il existe un coût caché : le déséquilibre de venue`
- Domain tags: ACCOUNTING
- Source statement: 50. Mais il existe un coût caché : le déséquilibre de venue: Le PnL global peut être positif tout en dégradant notre capacité à faire le prochain trade.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `50. Mais il existe un coût caché : le déséquilibre de venue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0043`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0166 — 51. On ne doit PAS affecter naïvement un “frais de rebalance complet” à chaque trade

- Source: `SRC-003`
- Location: lines 3315–3330; heading `51. On ne doit PAS affecter naïvement un “frais de rebalance complet” à chaque trade`
- Domain tags: INVENTORY, ACCOUNTING, FUTURE
- Source statement: 51. On ne doit PAS affecter naïvement un “frais de rebalance complet” à chaque trade: Parce que plusieurs trades peuvent : et une opportunité inverse future peut rééquilibrer gratuitement tout en gagnant de l’argent.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `51. On ne doit PAS affecter naïvement un “frais de rebalance complet” à chaque trade` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INV-0013`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, ACCOUNTING, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0167 — 52. On utilise un InventoryShadowCost

- Source: `SRC-003`
- Location: lines 3331–3345; heading `52. On utilise un InventoryShadowCost`
- Domain tags: VALIDATION, ACCOUNTING, INVENTORY, RISK
- Source statement: 52. On utilise un InventoryShadowCost: combien cette nouvelle opération dégrade ou améliore économiquement notre inventaire par venue.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `52. On utilise un InventoryShadowCost` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0013`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, INVENTORY, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0168 — 53. Exemple

- Source: `SRC-003`
- Location: lines 3346–3372; heading `53. Exemple`
- Domain tags: VALIDATION, ACCOUNTING, INVENTORY, PRODUCT
- Source statement: 53. Exemple: Si Binance manque déjà énormément de BTC : Une petite opportunité peut être rejetée.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `53. Exemple` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-VALID-0014`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0169 — 54. Cross-exchange : règle absolument non négociable

- Source: `SRC-003`
- Location: lines 3373–3393; heading `54. Cross-exchange : règle absolument non négociable`
- Domain tags: CROSS_EXCHANGE, INVENTORY, CAPITAL, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 54. Cross-exchange : règle absolument non négociable: On ne fait pas : La littérature cross-exchange montre précisément que la lenteur des transferts de capital constitue une friction majeure à l’arbitrage. Le capital doit être prépositionné lorsque l’on veut verrouiller rapidement une différence de prix entre venues.
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `54. Cross-exchange : règle absolument non négociable` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-XEX-0005`; supporting items: none found by conservative heading match; domain indexes `CROSS_EXCHANGE, INVENTORY, CAPITAL, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0170 — 55. Activation cross-exchange dans notre projet

- Source: `SRC-003`
- Location: lines 3394–3420; heading `55. Activation cross-exchange dans notre projet`
- Domain tags: CROSS_EXCHANGE, GRAPH, PRODUCT, ARCH, FUTURE
- Source statement: 55. Activation cross-exchange dans notre projet: Notre graphe doit être venue-aware : Mais nous validons d’abord :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `55. Activation cross-exchange dans notre projet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-XEX-0006`; supporting items: none found by conservative heading match; domain indexes `CROSS_EXCHANGE, GRAPH, PRODUCT, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0171 — 56. Accounting : les PnL qu’il faut stocker séparément

- Source: `SRC-003`
- Location: lines 3421–3447; heading `56. Accounting : les PnL qu’il faut stocker séparément`
- Domain tags: ACCOUNTING, RECOVERY, INVENTORY, BRIDGE
- Source statement: 56. Accounting : les PnL qu’il faut stocker séparément: Pour chaque 2-leg : direct_output
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `56. Accounting : les PnL qu’il faut stocker séparément` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0044`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, RECOVERY, INVENTORY, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0172 — 57. Important : ne jamais confondre ConversionAlpha et PortfolioPnL

- Source: `SRC-003`
- Location: lines 3448–3464; heading `57. Important : ne jamais confondre ConversionAlpha et PortfolioPnL`
- Domain tags: ACCOUNTING, PORTFOLIO, INVENTORY, ROUTING, FUTURE
- Source statement: 57. Important : ne jamais confondre ConversionAlpha et PortfolioPnL: -8 € MTM plus tard Le 2-leg était effectivement meilleur que la route directe.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `57. Important : ne jamais confondre ConversionAlpha et PortfolioPnL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ACCT-0045`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, PORTFOLIO, INVENTORY, ROUTING, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0173 — 58. Pipeline exact d’une opportunité same-venue

- Source: `SRC-003`
- Location: lines 3465–3500; heading `58. Pipeline exact d’une opportunité same-venue`
- Domain tags: EXECUTION, RECOVERY, RISK, DEPLOYMENT, ACCOUNTING, INVENTORY, CAPITAL, PORTFOLIO
- Source statement: 58. Pipeline exact d’une opportunité same-venue: BookUpdate affected Route2
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `58. Pipeline exact d’une opportunité same-venue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0093`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, DEPLOYMENT, ACCOUNTING, INVENTORY, CAPITAL, PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0174 — 59. Pseudo-décision

- Source: `SRC-003`
- Location: lines 3501–3543; heading `59. Pseudo-décision`
- Domain tags: EXECUTION, RECOVERY, RISK, INVENTORY, CAPITAL, PORTFOLIO, BRIDGE, OWA
- Source statement: 59. Pseudo-décision: direct = quote_direct(A, B, q) indirect = quote_indirect(A, X, B, q)
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `59. Pseudo-décision` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0094`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, INVENTORY, CAPITAL, PORTFOLIO, BRIDGE, OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0175 — 60. Les choses que nous GARDONS définitivement

- Source: `SRC-003`
- Location: lines 3544–3566; heading `60. Les choses que nous GARDONS définitivement`
- Domain tags: RECOVERY, VALIDATION, ACCOUNTING, INVENTORY, SIZING, SLICING, BRIDGE, OWA
- Source statement: 60. Les choses que nous GARDONS définitivement: OWA A→X→B vs A→B | OUI TM/MM | NON par défaut
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `60. Les choses que nous GARDONS définitivement` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0012`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, VALIDATION, ACCOUNTING, INVENTORY, SIZING, SLICING, BRIDGE, OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0176 — 61. Les choses que nous supprimons/corrigeons définitivement

- Source: `SRC-003`
- Location: lines 3567–3623; heading `61. Les choses que nous supprimons/corrigeons définitivement`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE, OWA, ROUTING, QUANT, RESEARCH
- Source statement: 61. Les choses que nous supprimons/corrigeons définitivement: On ne considère plus comme correct : On ne considère plus :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `61. Les choses que nous supprimons/corrigeons définitivement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-RISK-0040`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE, OWA, ROUTING, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0177 — 62. La métrique centrale finale du 2-leg

- Source: `SRC-003`
- Location: lines 3624–3656; heading `62. La métrique centrale finale du 2-leg`
- Domain tags: RECOVERY, RISK, ACCOUNTING, INVENTORY, CAPITAL
- Source statement: 62. La métrique centrale finale du 2-leg: Je ne veux donc pas que notre bot classe les opportunités uniquement sur : Il doit arriver à :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `62. La métrique centrale finale du 2-leg` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0013`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, RISK, ACCOUNTING, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0178 — 63. Mais les composantes restent enregistrées séparément

- Source: `SRC-003`
- Location: lines 3657–3691; heading `63. Mais les composantes restent enregistrées séparément`
- Domain tags: RECOVERY, RISK, ACCOUNTING, INVENTORY, RESEARCH
- Source statement: 63. Mais les composantes restent enregistrées séparément: Très important pour la recherche. Le bot ne doit pas uniquement enregistrer :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `63. Mais les composantes restent enregistrées séparément` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0014`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, RISK, ACCOUNTING, INVENTORY, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0179 — 64. Conclusion de l’interrogation n°2

- Source: `SRC-003`
- Location: lines 3692–3759; heading `64. Conclusion de l’interrogation n°2`
- Domain tags: EXECUTION, RISK, ACCOUNTING, INVENTORY, CAPITAL, PORTFOLIO, ROUTING, QUANT
- Source statement: 64. Conclusion de l’interrogation n°2: Le cœur économique de notre 2-leg devient donc : La découverte scientifique importante est que ce type de conversion existe réellement à grande échelle : l'étude de 2020 en identifiait 26,6 millions sur Binance, avec 95 % des séquences détectées donnant un meilleur ratio que la route directe selon leur méthodologie ; l'étude 2026 en identifie plus de 402 millions sur cinq ans de Binance et montre que le…
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `64. Conclusion de l’interrogation n°2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0095`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, ACCOUNTING, INVENTORY, CAPITAL, PORTFOLIO, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0180 — Comment éviter d’être épuisé

- Source: `SRC-003`
- Location: lines 3760–3761; heading `Comment éviter d’être épuisé`
- Domain tags: ARCH
- Source statement: Comment éviter d’être épuisé: Je mettrais 4 niveaux.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Comment éviter d’être épuisé` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0070`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0181 — 1. Des inventaires cibles par exchange

- Source: `SRC-003`
- Location: lines 3762–3797; heading `1. Des inventaires cibles par exchange`
- Domain tags: EXECUTION, RISK, RECORDER, PRODUCT
- Source statement: 1. Des inventaires cibles par exchange: On ne laisse jamais une venue aller jusqu’à zéro. Les pourcentages sont illustratifs : le Recorder devra déterminer les bons niveaux.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `1. Des inventaires cibles par exchange` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0096`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, RECORDER, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0182 — 2. Donner une valeur au rééquilibrage

- Source: `SRC-003`
- Location: lines 3798–3852; heading `2. Donner une valeur au rééquilibrage`
- Domain tags: RISK, VALIDATION, ACCOUNTING, INVENTORY, PRODUCT
- Source statement: 2. Donner une valeur au rééquilibrage: Hyperliquid = trop de BTC Binance = pas assez de BTC
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `2. Donner une valeur au rééquilibrage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RISK-0041`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, ACCOUNTING, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0183 — 3. L’idéal : attendre les opportunités inverses

- Source: `SRC-003`
- Location: lines 3853–3890; heading `3. L’idéal : attendre les opportunités inverses`
- Domain tags: INVENTORY, PRODUCT, FUTURE
- Source statement: 3. L’idéal : attendre les opportunités inverses: C’est le meilleur rebalance possible. * gagne lui aussi de l’argent ;
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `3. L’idéal : attendre les opportunités inverses` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INV-0014`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0184 — 4. Si le marché reste dans la même direction trop longtemps

- Source: `SRC-003`
- Location: lines 3891–3928; heading `4. Si le marché reste dans la même direction trop longtemps`
- Domain tags: RISK, INFRA, SECURITY, ACCOUNTING, INVENTORY, CAPITAL, ROUTING, CROSS_EXCHANGE
- Source statement: 4. Si le marché reste dans la même direction trop longtemps: C’est là que ça se complique. Supposons pendant 6 heures :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `4. Si le marché reste dans la même direction trop longtemps` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RISK-0042`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, SECURITY, ACCOUNTING, INVENTORY, CAPITAL, ROUTING, CROSS_EXCHANGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-003-ITEM-0185 — Le moteur doit accumuler les besoins de rebalance

- Source: `SRC-003`
- Location: lines 3929–3961; heading `Le moteur doit accumuler les besoins de rebalance`
- Domain tags: INVENTORY, ACCOUNTING, FUTURE
- Source statement: Le moteur doit accumuler les besoins de rebalance: Parce que les prochains arbitrages peuvent naturellement réduire le déséquilibre.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Le moteur doit accumuler les besoins de rebalance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INV-0015`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, ACCOUNTING, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0186 — Donc le vrai calcul du rebalance

- Source: `SRC-003`
- Location: lines 3962–3971; heading `Donc le vrai calcul du rebalance`
- Domain tags: INVENTORY, ACCOUNTING
- Source statement: Donc le vrai calcul du rebalance: « Je suis déséquilibré → transfert. »
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Donc le vrai calcul du rebalance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0016`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0187 — Attendre

- Source: `SRC-003`
- Location: lines 3972–3980; heading `Attendre`
- Domain tags: RISK, CAPITAL, QUANT
- Source statement: Attendre: Coût : opportunités refusées
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Attendre` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0043`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0188 — Rebalancer

- Source: `SRC-003`
- Location: lines 3981–3991; heading `Rebalancer`
- Domain tags: INVENTORY, RISK, INFRA, SECURITY, OPERATIONS, ACCOUNTING, CROSS_EXCHANGE
- Source statement: Rebalancer: Le moteur choisit le moins mauvais.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Rebalancer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0017`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, RISK, INFRA, SECURITY, OPERATIONS, ACCOUNTING, CROSS_EXCHANGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0189 — Il nous faut donc un Venue Inventory Engine

- Source: `SRC-003`
- Location: lines 3992–4027; heading `Il nous faut donc un Venue Inventory Engine`
- Domain tags: INVENTORY, ACCOUNTING, GRAPH, ARCH
- Source statement: Il nous faut donc un Venue Inventory Engine: Notre graphe ne contient pas simplement : Et ça s’intègre parfaitement à notre architecture actuelle.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Il nous faut donc un Venue Inventory Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0018`; supporting items: SRC-006-ITEM-0367; domain indexes `INVENTORY, ACCOUNTING, GRAPH, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0190 — On peut même réserver une capacité dans chaque direction

- Source: `SRC-003`
- Location: lines 4028–4054; heading `On peut même réserver une capacité dans chaque direction`
- Domain tags: INFRA, CAPITAL, PRODUCT, ARCH
- Source statement: On peut même réserver une capacité dans chaque direction: Je ne veux pas que le bot utilise tout pour : Il doit conserver une partie permettant encore :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `On peut même réserver une capacité dans chaque direction` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0034`; supporting items: none found by conservative heading match; domain indexes `INFRA, CAPITAL, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0191 — Et notre Market Atlas doit mesurer le biais directionnel

- Source: `SRC-003`
- Location: lines 4055–4079; heading `Et notre Market Atlas doit mesurer le biais directionnel`
- Domain tags: MARKET_ATLAS, EXECUTION, RECORDER, INVENTORY, CAPITAL
- Source statement: Et notre Market Atlas doit mesurer le biais directionnel: Supposons qu’après 30 jours on découvre : Alors une allocation 50/50 n’est peut-être pas optimale.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Et notre Market Atlas doit mesurer le biais directionnel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ATLAS-0003`; supporting items: SRC-006-ITEM-0330; domain indexes `MARKET_ATLAS, EXECUTION, RECORDER, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0192 — Et si le déséquilibre devient dangereux très rapidement ?

- Source: `SRC-003`
- Location: lines 4080–4081; heading `Et si le déséquilibre devient dangereux très rapidement ?`
- Domain tags: ARCH
- Source statement: Et si le déséquilibre devient dangereux très rapidement ?: On a plusieurs possibilités.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Et si le déséquilibre devient dangereux très rapidement ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0071`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0193 — A. Stopper cette direction

- Source: `SRC-003`
- Location: lines 4082–4087; heading `A. Stopper cette direction`
- Domain tags: PRODUCT
- Source statement: A. Stopper cette direction: SELL BTC Binance disabled Simple et sûr.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `A. Stopper cette direction` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0013`; supporting items: none found by conservative heading match; domain indexes `PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0194 — B. Réduire les tailles

- Source: `SRC-003`
- Location: lines 4088–4101; heading `B. Réduire les tailles`
- Domain tags: RISK
- Source statement: B. Réduire les tailles: à mesure qu’on approche de la limite.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `B. Réduire les tailles` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0044`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0195 — C. Favoriser fortement la direction inverse

- Source: `SRC-003`
- Location: lines 4102–4103; heading `C. Favoriser fortement la direction inverse`
- Domain tags: ARCH
- Source statement: C. Favoriser fortement la direction inverse: Même avec un edge légèrement inférieur.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `C. Favoriser fortement la direction inverse` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0072`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0196 — D. Rebalance physique

- Source: `SRC-003`
- Location: lines 4104–4105; heading `D. Rebalance physique`
- Domain tags: INVENTORY
- Source statement: D. Rebalance physique: Crypto/stablecoin entre venues.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `D. Rebalance physique` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0019`; supporting items: none found by conservative heading match; domain indexes `INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0197 — E. Éventuellement utiliser des dérivés comme hedge temporaire

- Source: `SRC-003`
- Location: lines 4106–4109; heading `E. Éventuellement utiliser des dérivés comme hedge temporaire`
- Domain tags: RECOVERY, RISK
- Source statement: E. Éventuellement utiliser des dérivés comme hedge temporaire: Si un transfert nous laisse temporairement exposés directionnellement, un perp peut réduire le delta pendant la période de settlement. Mais ce serait un mécanisme de risk management, pas la source principale de l’arbitrage.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `E. Éventuellement utiliser des dérivés comme hedge temporaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RECOV-0015`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0198 — Et il ne faut surtout pas attendre d’être à zéro

- Source: `SRC-003`
- Location: lines 4110–4132; heading `Et il ne faut surtout pas attendre d’être à zéro`
- Domain tags: RISK, INVENTORY
- Source statement: Et il ne faut surtout pas attendre d’être à zéro: Je voudrais quelque chose comme : ├─ 90% only rebalancing trades
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Et il ne faut surtout pas attendre d’être à zéro` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0045`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0199 — Exemple complet

- Source: `SRC-003`
- Location: lines 4133–4144; heading `Exemple complet`
- Domain tags: CAPITAL
- Source statement: Exemple complet: Capital : HL:
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Exemple complet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0017`; supporting items: none found by conservative heading match; domain indexes `CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0200 — Opportunités 1–10

- Source: `SRC-003`
- Location: lines 4145–4164; heading `Opportunités 1–10`
- Domain tags: PRODUCT, ARCH
- Source statement: Opportunités 1–10: Toutes : BUY HL
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Opportunités 1–10` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0014`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0201 — Opportunité 11

- Source: `SRC-003`
- Location: lines 4165–4189; heading `Opportunité 11`
- Domain tags: ACCOUNTING, INVENTORY, ARCH
- Source statement: Opportunité 11: Même sens. PnL brut :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Opportunité 11` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0046`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, INVENTORY, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0202 — Opportunité 20

- Source: `SRC-003`
- Location: lines 4190–4209; heading `Opportunité 20`
- Domain tags: ACCOUNTING, INVENTORY
- Source statement: Opportunité 20: Binance BTC devient proche du minimum. Adjusted EV = -2 €
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Opportunité 20` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0047`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0203 — Puis opportunité inverse

- Source: `SRC-003`
- Location: lines 4210–4232; heading `Puis opportunité inverse`
- Domain tags: ACCOUNTING, INVENTORY, PRODUCT
- Source statement: Puis opportunité inverse: Adjusted EV = +8 €
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `Puis opportunité inverse` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0048`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-003-ITEM-0204 — C'est ce qui empêche réellement l'épuisement

- Source: `SRC-003`
- Location: lines 4233–4272; heading `C'est ce qui empêche réellement l'épuisement`
- Domain tags: EXECUTION, INFRA, VALIDATION, ACCOUNTING, INVENTORY, CAPITAL, PRODUCT, FUTURE
- Source statement: C'est ce qui empêche réellement l'épuisement: Le spatial arbitrage ne doit donc jamais être conçu comme : Et si on le fait correctement, le but n’est pas de ne jamais être déséquilibré. Un peu de déséquilibre est normal.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Recorder/storage and OWA/inventory refinement; closure dossiers prevail.
- Candidate canonical interpretation: Preserve `C'est ce qui empêche réellement l'épuisement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0097`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, VALIDATION, ACCOUNTING, INVENTORY, CAPITAL, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 199
- Requirements contributed: 199
- Supporting references contributed: 15 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 0
- Research items: 119
- Open items: 0
- External revalidation items: 27
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
