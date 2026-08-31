# SRC-008 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-008`
- Filename: `Oui. Et en creusant le sujet, je corrigerais une chose fondamentale….md`
- SHA-256: `8b7924d664bd718e324bc3d7f50f0a461244b2638a69d7601caf132d8a849f50`
- Line count: 6937
- Authority profile: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Main domains: INFRA, EXECUTION, ACCOUNTING, RISK, QUANT, MICROSTRUCTURE, BENCHMARK, ARCH, ROUTING, PRODUCT, DEPLOYMENT, VALIDATION
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-008-ITEM-0001 — Source preamble

- Source: `SRC-008`
- Location: lines 1–16; heading `Source preamble`
- Domain tags: QUANT, PRODUCT
- Source statement: Source preamble: Oui. Et en creusant le sujet, je corrigerais une chose fondamentale dans notre formulation initiale : On ne pourra jamais reconstruire exactement le monde alternatif dans lequel notre ordre avait existé.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Source preamble` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-QUANT-0029`; supporting items: SRC-003-ITEM-0001, SRC-007-ITEM-0001; domain indexes `QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0002 — 1. Il faut séparer trois problèmes

- Source: `SRC-008`
- Location: lines 17–34; heading `1. Il faut séparer trois problèmes`
- Domain tags: EXECUTION, REPLAY, PARTICIPANTS, QUANT
- Source statement: 1. Il faut séparer trois problèmes: Il y a en réalité trois couches très différentes. Que fait mécaniquement notre ordre au carnet ?
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `1. Il faut séparer trois problèmes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0286`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, REPLAY, PARTICIPANTS, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0003 — 2. Première couche : reproduire Hyperliquid lui-même

- Source: `SRC-008`
- Location: lines 35–50; heading `2. Première couche : reproduire Hyperliquid lui-même`
- Domain tags: EXECUTION, CLOCK, ARCH
- Source statement: 2. Première couche : reproduire Hyperliquid lui-même: Avant de simuler les autres traders, notre simulateur doit reproduire correctement l'exchange. Hyperliquid indique officiellement que ses ordres sont matchés en price-time priority. Il supporte notamment IOC, ALO/Post Only et GTC. (hyperliquid.gitbook.io)
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `2. Première couche : reproduire Hyperliquid lui-même` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0287`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CLOCK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0004 — 3. Timeline exacte d'une décision

- Source: `SRC-008`
- Location: lines 51–144; heading `3. Timeline exacte d'une décision`
- Domain tags: EXECUTION, RISK, DETERMINISM, INFRA, DEPLOYMENT, ROUTING, PRODUCT
- Source statement: 3. Timeline exacte d'une décision: Supposons qu'une opportunité apparaisse à t0. Le mauvais backtest fait :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `3. Timeline exacte d'une décision` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0288`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, DETERMINISM, INFRA, DEPLOYMENT, ROUTING, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0005 — 4. C'est déjà une énorme amélioration

- Source: `SRC-008`
- Location: lines 145–170; heading `4. C'est déjà une énorme amélioration`
- Domain tags: INFRA, REPLAY, ROUTING, QUANT
- Source statement: 4. C'est déjà une énorme amélioration: Notre stratégie qui semblait excellente en backtest naïf devient perdante avec sa vraie latence. Donc avant même le sophisticated market impact :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `4. C'est déjà une énorme amélioration` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0051`; supporting items: none found by conservative heading match; domain indexes `INFRA, REPLAY, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0006 — 5. Taker : Mechanical Impact

- Source: `SRC-008`
- Location: lines 171–214; heading `5. Taker : Mechanical Impact`
- Domain tags: EXECUTION, QUANT, RECOVERY, RISK, VALIDATION, ACCOUNTING
- Source statement: 5. Taker : Mechanical Impact: Là, notre idée précédente reste correcte. Notre IOC marketable limit veut acheter 1 000 €.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `5. Taker : Mechanical Impact` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0289`; supporting items: SRC-004-ITEM-0202, SRC-007-ITEM-0211; domain indexes `EXECUTION, QUANT, RECOVERY, RISK, VALIDATION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0007 — 6. Correction importante pour les triangles

- Source: `SRC-008`
- Location: lines 215–260; heading `6. Correction importante pour les triangles`
- Domain tags: TRIANGLE, EXECUTION, VALIDATION, SIMULATOR, CROSS_MARKET, QUANT
- Source statement: 6. Correction importante pour les triangles: Notre précédent schéma pouvait laisser croire que : ne sont pas mécaniquement modifiés par Leg1.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `6. Correction importante pour les triangles` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-TRI-0003`; supporting items: none found by conservative heading match; domain indexes `TRIANGLE, EXECUTION, VALIDATION, SIMULATOR, CROSS_MARKET, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0008 — 7. Notre Shadow State devient donc multi-market

- Source: `SRC-008`
- Location: lines 261–281; heading `7. Notre Shadow State devient donc multi-market`
- Domain tags: VALIDATION, SIMULATOR, CROSS_MARKET
- Source statement: 7. Notre Shadow State devient donc multi-market: Chaque carnet possède sa propre branche.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `7. Notre Shadow State devient donc multi-market` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0372`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0009 — 8. Le plus gros problème du Shadow Book

- Source: `SRC-008`
- Location: lines 282–316; heading `8. Le plus gros problème du Shadow Book`
- Domain tags: VALIDATION, EXECUTION, FUTURE
- Source statement: 8. Le plus gros problème du Shadow Book: C'est ici que les backtests deviennent subtils. Nous ajoutons notre ordre fictif :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `8. Le plus gros problème du Shadow Book` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-VALID-0373`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0010 — 9. C'est le vrai problème scientifique du market replay

- Source: `SRC-008`
- Location: lines 317–329; heading `9. C'est le vrai problème scientifique du market replay`
- Domain tags: REPLAY, EXECUTION, INFRA, SIMULATOR, QUANT, RESEARCH
- Source statement: 9. C'est le vrai problème scientifique du market replay: Dès qu'on intervient dans l'histoire : les événements historiques futurs ne sont plus nécessairement compatibles avec le nouveau carnet.
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `9. C'est le vrai problème scientifique du market replay` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REPLAY-0018`; supporting items: none found by conservative heading match; domain indexes `REPLAY, EXECUTION, INFRA, SIMULATOR, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0011 — 10. Donc il faut deux branches bien distinctes

- Source: `SRC-008`
- Location: lines 330–357; heading `10. Donc il faut deux branches bien distinctes`
- Domain tags: EXECUTION, ACCOUNTING, SIMULATOR, REPLAY, CROSS_MARKET, MICROSTRUCTURE, QUANT
- Source statement: 10. Donc il faut deux branches bien distinctes: Je veux que notre simulateur produise au minimum : Le futur historique reste considéré comme donné.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `10. Donc il faut deux branches bien distinctes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0290`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, SIMULATOR, REPLAY, CROSS_MARKET, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0012 — 11. Pourquoi garder le mode historique simple ?

- Source: `SRC-008`
- Location: lines 358–373; heading `11. Pourquoi garder le mode historique simple ?`
- Domain tags: REPLAY, QUANT, FUTURE
- Source statement: 11. Pourquoi garder le mode historique simple ?: Parce que pour un tout petit ordre : market_depth = 500 000 €
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `11. Pourquoi garder le mode historique simple ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-REPLAY-0019`; supporting items: none found by conservative heading match; domain indexes `REPLAY, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0013 — 12. Taker impact : le bon indicateur n'est pas seulement la taille

- Source: `SRC-008`
- Location: lines 374–526; heading `12. Taker impact : le bon indicateur n'est pas seulement la taille`
- Domain tags: EXECUTION, RISK, QUANT, FORMULA, LIQUIDITY_RESPONSE, MICROSTRUCTURE, INVENTORY
- Source statement: 12. Taker impact : le bon indicateur n'est pas seulement la taille: reste utile, mais elle est insuffisante. 1000 € sur BTC très liquide
- Nature: formula/definition
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `12. Taker impact : le bon indicateur n'est pas seulement la taille` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0291`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, QUANT, FORMULA, LIQUIDITY_RESPONSE, MICROSTRUCTURE, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0014 — 13. Order Flow Imbalance

- Source: `SRC-008`
- Location: lines 527–574; heading `13. Order Flow Imbalance`
- Domain tags: EXECUTION, MICROSTRUCTURE, INVENTORY, RISK, QUANT, RESEARCH
- Source statement: 13. Order Flow Imbalance: Le papier de Cont, Kukanov et Stoikov est particulièrement utile ici. Ils montrent qu'à très court horizon, le changement de prix est fortement lié à l'Order Flow Imbalance, qui combine notamment :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `13. Order Flow Imbalance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0292`; supporting items: SRC-002-ITEM-0013, SRC-007-ITEM-0024; domain indexes `EXECUTION, MICROSTRUCTURE, INVENTORY, RISK, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0015 — 14. Notre ordre crée donc un OFI shock

- Source: `SRC-008`
- Location: lines 575–606; heading `14. Notre ordre crée donc un OFI shock`
- Domain tags: MICROSTRUCTURE, EXECUTION, INVENTORY, QUANT
- Source statement: 14. Notre ordre crée donc un OFI shock: Par exemple notre market buy de 500 € : Le MarketResponseModel peut ensuite apprendre :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `14. Notre ordre crée donc un OFI shock` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0022`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0016 — 15. Et pas uniquement au prix

- Source: `SRC-008`
- Location: lines 607–631; heading `15. Et pas uniquement au prix`
- Domain tags: EXECUTION, RISK, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE
- Source statement: 15. Et pas uniquement au prix: Nous voulons prédire un vecteur : Donc on simule réellement la structure du carnet.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `15. Et pas uniquement au prix` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0293`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0017 — 16. Queue-Reactive Model : très pertinent

- Source: `SRC-008`
- Location: lines 632–727; heading `16. Queue-Reactive Model : très pertinent`
- Domain tags: MICROSTRUCTURE, EXECUTION, RISK, QUANT
- Source statement: 16. Queue-Reactive Model : très pertinent: Huang, Lehalle et Rosenbaum proposent justement un modèle dans lequel les intensités d'arrivée : dépendent de l'état courant des files du carnet.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `16. Queue-Reactive Model : très pertinent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-MICRO-0023`; supporting items: SRC-007-ITEM-0259; domain indexes `MICROSTRUCTURE, EXECUTION, RISK, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0018 — 17. Hawkes : deuxième outil utile

- Source: `SRC-008`
- Location: lines 728–744; heading `17. Hawkes : deuxième outil utile`
- Domain tags: QUANT, EXECUTION, RISK, MICROSTRUCTURE, INVENTORY, PRODUCT, FUTURE
- Source statement: 17. Hawkes : deuxième outil utile: Une autre famille intéressante est le processus de Hawkes. Des travaux de microstructure modélisent :
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `17. Hawkes : deuxième outil utile` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-QUANT-0030`; supporting items: none found by conservative heading match; domain indexes `QUANT, EXECUTION, RISK, MICROSTRUCTURE, INVENTORY, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0019 — 18. Je ne choisirais pourtant PAS directement un énorme modèle Hawkes

- Source: `SRC-008`
- Location: lines 745–773; heading `18. Je ne choisirais pourtant PAS directement un énorme modèle Hawkes`
- Domain tags: QUANT, MICROSTRUCTURE, INVENTORY, PRODUCT
- Source statement: 18. Je ne choisirais pourtant PAS directement un énorme modèle Hawkes: Pour notre première calibration, je commencerais beaucoup plus empiriquement. On prend des événements historiques qui ressemblent à notre intervention.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `18. Je ne choisirais pourtant PAS directement un énorme modèle Hawkes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0031`; supporting items: none found by conservative heading match; domain indexes `QUANT, MICROSTRUCTURE, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0020 — 19. Donc notre premier Response Model devrait être un Conditional Empirical Model

- Source: `SRC-008`
- Location: lines 774–810; heading `19. Donc notre premier Response Model devrait être un Conditional Empirical Model`
- Domain tags: EXECUTION, MICROSTRUCTURE, INVENTORY, QUANT, PRODUCT
- Source statement: 19. Donc notre premier Response Model devrait être un Conditional Empirical Model: C'est beaucoup plus transparent qu'un modèle ML complexe.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `19. Donc notre premier Response Model devrait être un Conditional Empirical Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0294`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, INVENTORY, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0021 — 20. Exemple

- Source: `SRC-008`
- Location: lines 811–841; heading `20. Exemple`
- Domain tags: EXECUTION, RECOVERY, MICROSTRUCTURE, INVENTORY, QUANT, PRODUCT
- Source statement: 20. Exemple: Nous avons trouvé historiquement 3 800 événements proches de : P(+3 ticks or more) 9%
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `20. Exemple` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0295`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, MICROSTRUCTURE, INVENTORY, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0022 — 21. Ensuite seulement modèle paramétrique

- Source: `SRC-008`
- Location: lines 842–857; heading `21. Ensuite seulement modèle paramétrique`
- Domain tags: INFRA, MICROSTRUCTURE, QUANT, FUTURE
- Source statement: 21. Ensuite seulement modèle paramétrique: Quand on aura assez de données : Le meilleur modèle gagne selon sa capacité à prédire du out-of-sample réel.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `21. Ensuite seulement modèle paramétrique` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INFRA-0052`; supporting items: none found by conservative heading match; domain indexes `INFRA, MICROSTRUCTURE, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0023 — 22. Le maker est un problème différent

- Source: `SRC-008`
- Location: lines 858–876; heading `22. Le maker est un problème différent`
- Domain tags: EXECUTION, MICROSTRUCTURE
- Source statement: 22. Le maker est un problème différent: il ne suffit pas de connaître : BID @100 = 10 000
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `22. Le maker est un problème différent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0296`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0024 — 23. Mais il y a une subtilité importante avec le L2

- Source: `SRC-008`
- Location: lines 877–905; heading `23. Mais il y a une subtilité importante avec le L2`
- Domain tags: EXECUTION
- Source statement: 23. Mais il y a une subtilité importante avec le L2: Si on dispose uniquement : 100.00 = 10 000 total
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `23. Mais il y a une subtilité importante avec le L2` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0297`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0026 — L2

- Source: `SRC-008`
- Location: lines 907–912; heading `L2`
- Domain tags: ARCH
- Source statement: L2: price aggregated size
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `L2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0085`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0027 — L4

- Source: `SRC-008`
- Location: lines 913–934; heading `L4`
- Domain tags: EXECUTION, RISK, INFRA, NODE, ACCOUNTING, PRODUCT, ARCH
- Source statement: L4: Le node Hyperliquid sait notamment produire des snapshots l4Snapshots contenant l'information détaillée du carnet. (GitHub) Il existe également un order_book_server capable de reconstruire un L4 snapshot + diffs par bloc, mais sa version actuellement publiée indique explicitement ne pas supporter les spot order books. Il ne faut donc pas construire notre V1 spot en supposant que cette solution est disponible. (GitHub)
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `L4` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0298`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, NODE, ACCOUNTING, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0028 — 25. Avec seulement du L2, je veux trois simulations de queue

- Source: `SRC-008`
- Location: lines 935–936; heading `25. Avec seulement du L2, je veux trois simulations de queue`
- Domain tags: MICROSTRUCTURE
- Source statement: 25. Avec seulement du L2, je veux trois simulations de queue: C'est très utile.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `25. Avec seulement du L2, je veux trois simulations de queue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0024`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0029 — Pessimistic Queue

- Source: `SRC-008`
- Location: lines 937–944; heading `Pessimistic Queue`
- Domain tags: MICROSTRUCTURE, EXECUTION
- Source statement: Pessimistic Queue: Les cancellations ne réduisent jamais queue_ahead. Seuls les vrais trades la réduisent.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Pessimistic Queue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0025`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0030 — Optimistic Queue

- Source: `SRC-008`
- Location: lines 945–951; heading `Optimistic Queue`
- Domain tags: MICROSTRUCTURE, EXECUTION
- Source statement: Optimistic Queue: Toutes les cancellations au niveau devant notre ordre sont considérées comme favorables.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Optimistic Queue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0026`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0031 — Probabilistic Queue

- Source: `SRC-008`
- Location: lines 952–981; heading `Probabilistic Queue`
- Domain tags: MICROSTRUCTURE, QUANT, EXECUTION
- Source statement: Probabilistic Queue: et simule la diminution de la queue.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Probabilistic Queue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0027`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, QUANT, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0032 — 26. Ça nous donne immédiatement une fourchette

- Source: `SRC-008`
- Location: lines 982–1003; heading `26. Ça nous donne immédiatement une fourchette`
- Domain tags: EXECUTION, QUANT
- Source statement: 26. Ça nous donne immédiatement une fourchette: Si notre stratégie est rentable uniquement avec : on sait que sa robustesse est mauvaise.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `26. Ça nous donne immédiatement une fourchette` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0299`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0033 — 27. Notre Queue Model doit prédire plus qu'un simple fill

- Source: `SRC-008`
- Location: lines 1004–1019; heading `27. Notre Queue Model doit prédire plus qu'un simple fill`
- Domain tags: EXECUTION, MICROSTRUCTURE, MAKER_MODEL, PRODUCT
- Source statement: 27. Notre Queue Model doit prédire plus qu'un simple fill: Il existe justement une littérature dédiée à l'estimation de la distribution du *time-to-fill* conditionnellement aux conditions du carnet. (DOI)
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `27. Notre Queue Model doit prédire plus qu'un simple fill` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0300`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, MAKER_MODEL, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0034 — 28. C'est crucial pour notre stratégie MT

- Source: `SRC-008`
- Location: lines 1020–1070; heading `28. C'est crucial pour notre stratégie MT`
- Domain tags: EXECUTION, RISK, ACCOUNTING, MAKER_MODEL
- Source statement: 28. C'est crucial pour notre stratégie MT: La valeur réelle n'est pas : EV_{MT} = \int P(fill=t) \times EV_{Leg2}(t) \;dt
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `28. C'est crucial pour notre stratégie MT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0301`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, ACCOUNTING, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0035 — 29. Adverse selection

- Source: `SRC-008`
- Location: lines 1071–1093; heading `29. Adverse selection`
- Domain tags: MAKER_MODEL, EXECUTION, MICROSTRUCTURE, QUANT
- Source statement: 29. Adverse selection: Peut-être parce qu'un vendeur non informé voulait simplement vendre. Mais peut-être parce que :
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `29. Adverse selection` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-MAKER-0002`; supporting items: SRC-004-ITEM-0214, SRC-004-ITEM-0215, SRC-006-ITEM-0346, SRC-007-ITEM-0042; domain indexes `MAKER_MODEL, EXECUTION, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0036 — 30. Maintenant : comment inclure les autres bots ?

- Source: `SRC-008`
- Location: lines 1094–1106; heading `30. Maintenant : comment inclure les autres bots ?`
- Domain tags: EXECUTION, INFRA, PARTICIPANTS, RESEARCH
- Source statement: 30. Maintenant : comment inclure les autres bots ?: Je ne commencerais PAS avec : On ne sait pas qui ils sont ni leurs stratégies.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `30. Maintenant : comment inclure les autres bots ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0302`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, PARTICIPANTS, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0037 — 31. Les autres traders deviennent des processus de flux

- Source: `SRC-008`
- Location: lines 1107–1133; heading `31. Les autres traders deviennent des processus de flux`
- Domain tags: EXECUTION, RISK, QUANT, PRODUCT
- Source statement: 31. Les autres traders deviennent des processus de flux: Leur fréquence dépend de : On n'a pas besoin de savoir :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `31. Les autres traders deviennent des processus de flux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0303`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0038 — 32. Ça peut produire des comportements qui ressemblent naturellement à des bots

- Source: `SRC-008`
- Location: lines 1134–1163; heading `32. Ça peut produire des comportements qui ressemblent naturellement à des bots`
- Domain tags: EXECUTION, RISK, QUANT
- Source statement: 32. Ça peut produire des comportements qui ressemblent naturellement à des bots: forte probabilité de new limit ask Mais nous n'avons pas besoin d'inventer son identité.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `32. Ça peut produire des comportements qui ressemblent naturellement à des bots` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0304`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0039 — 33. Cross-market response : indispensable pour nous

- Source: `SRC-008`
- Location: lines 1164–1185; heading `33. Cross-market response : indispensable pour nous`
- Domain tags: CROSS_MARKET, GRAPH
- Source statement: 33. Cross-market response : indispensable pour nous: Donc notre response model ne peut pas être uniquement : Il faut aussi apprendre :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `33. Cross-market response : indispensable pour nous` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0014`; supporting items: SRC-004-ITEM-0241, SRC-007-ITEM-0132, SRC-007-ITEM-0052, SRC-007-ITEM-0059; domain indexes `CROSS_MARKET, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0040 — 34. Notre pair_to_routes peut devenir aussi un pair_to_response_neighborhood

- Source: `SRC-008`
- Location: lines 1186–1203; heading `34. Notre pair_to_routes peut devenir aussi un pair_to_response_neighborhood`
- Domain tags: ROUTING, GRAPH
- Source statement: 34. Notre pair_to_routes peut devenir aussi un pair_to_response_neighborhood: On ne réévalue pas tous les markets Hyperliquid. On connaît immédiatement les marchés économiquement liés :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `34. Notre pair_to_routes peut devenir aussi un pair_to_response_neighborhood` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0036`; supporting items: none found by conservative heading match; domain indexes `ROUTING, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0041 — 35. Comment apprendre ces réactions cross-market ?

- Source: `SRC-008`
- Location: lines 1204–1250; heading `35. Comment apprendre ces réactions cross-market ?`
- Domain tags: CROSS_MARKET
- Source statement: 35. Comment apprendre ces réactions cross-market ?: P( \Delta Book_j(t+h) \mid Shock_i, State ) pour marchés i et j.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `35. Comment apprendre ces réactions cross-market ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0015`; supporting items: SRC-007-ITEM-0132; domain indexes `CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0042 — 36. Cela nous donne un CrossMarketResponseMatrix

- Source: `SRC-008`
- Location: lines 1251–1269; heading `36. Cela nous donne un CrossMarketResponseMatrix`
- Domain tags: CROSS_MARKET, QUANT
- Source statement: 36. Cela nous donne un CrossMarketResponseMatrix: La matrice change naturellement selon :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `36. Cela nous donne un CrossMarketResponseMatrix` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0016`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0043 — 37. Et elle répond directement au problème des autres arbitrage bots

- Source: `SRC-008`
- Location: lines 1270–1292; heading `37. Et elle répond directement au problème des autres arbitrage bots`
- Domain tags: QUANT
- Source statement: 37. Et elle répond directement au problème des autres arbitrage bots: Si nous créons nous-mêmes une anomalie : d'autres bots peuvent comparer :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `37. Et elle répond directement au problème des autres arbitrage bots` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0032`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0044 — 38. Comment représenter le futur ?

- Source: `SRC-008`
- Location: lines 1293–1321; heading `38. Comment représenter le futur ?`
- Domain tags: EXECUTION, INFRA, ACCOUNTING, CROSS_MARKET, MICROSTRUCTURE, ROUTING, PRODUCT
- Source statement: 38. Comment représenter le futur ?: Pas une trajectoire. Des scénarios.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `38. Comment représenter le futur ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0305`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ACCOUNTING, CROSS_MARKET, MICROSTRUCTURE, ROUTING, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0045 — 39. Résultat attendu

- Source: `SRC-008`
- Location: lines 1322–1348; heading `39. Résultat attendu`
- Domain tags: EXECUTION, RECOVERY, RISK, BENCHMARK, ACCOUNTING, ROUTING
- Source statement: 39. Résultat attendu: Expected PnL = +1.73 € P(PnL > 0) 87.4 %
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `39. Résultat attendu` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0306`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, BENCHMARK, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0046 — 40. Il nous faut notamment la CVaR

- Source: `SRC-008`
- Location: lines 1349–1350; heading `40. Il nous faut notamment la CVaR`
- Domain tags: RISK, ROUTING
- Source statement: 40. Il nous faut notamment la CVaR: Deux routes :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `40. Il nous faut notamment la CVaR` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0326`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0047 — A

- Source: `SRC-008`
- Location: lines 1351–1357; heading `A`
- Domain tags: ARCH
- Source statement: A: mais perte si fail = -80 €
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `A` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0086`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0048 — B

- Source: `SRC-008`
- Location: lines 1358–1376; heading `B`
- Domain tags: RECOVERY, RISK, ACCOUNTING
- Source statement: B: perte moyenne fail = -3 € Le simple expected PnL peut mal hiérarchiser leur risque.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0023`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0049 — 41. Simulation Confidence : on peut maintenant le définir correctement

- Source: `SRC-008`
- Location: lines 1377–1392; heading `41. Simulation Confidence : on peut maintenant le définir correctement`
- Domain tags: INFRA, BENCHMARK, ACCOUNTING, SIMULATOR, CROSS_MARKET, MICROSTRUCTURE, QUANT, ARCH
- Source statement: 41. Simulation Confidence : on peut maintenant le définir correctement: Je ne veux pas un score esthétique arbitraire. Il doit dépendre de plusieurs dimensions :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `41. Simulation Confidence : on peut maintenant le définir correctement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0053`; supporting items: SRC-004-ITEM-0264, SRC-007-ITEM-0272; domain indexes `INFRA, BENCHMARK, ACCOUNTING, SIMULATOR, CROSS_MARKET, MICROSTRUCTURE, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0050 — 42. Très important : Out-of-Distribution

- Source: `SRC-008`
- Location: lines 1393–1425; heading `42. Très important : Out-of-Distribution`
- Domain tags: PRODUCT, ACCOUNTING, QUANT
- Source statement: 42. Très important : Out-of-Distribution: Supposons que notre modèle ait appris essentiellement sur : et qu'on lui demande :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `42. Très important : Out-of-Distribution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-PRODUCT-0022`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0051 — 43. Donc la confiance peut devenir un Risk Gate

- Source: `SRC-008`
- Location: lines 1426–1444; heading `43. Donc la confiance peut devenir un Risk Gate`
- Domain tags: RISK, ACCOUNTING
- Source statement: 43. Donc la confiance peut devenir un Risk Gate: → reject / reduce size C'est exactement ce qui empêchera notre bot de scaler au-delà de ce qu'il sait réellement simuler.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `43. Donc la confiance peut devenir un Risk Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0327`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0052 — 44. Capacity = capacité VALIDÉE, pas profondeur brute

- Source: `SRC-008`
- Location: lines 1445–1484; heading `44. Capacity = capacité VALIDÉE, pas profondeur brute`
- Domain tags: CAPITAL, RISK, ACCOUNTING, ROUTING, QUANT
- Source statement: 44. Capacity = capacité VALIDÉE, pas profondeur brute: C'est une correction conceptuelle très importante. La capacité d'une route n'est pas simplement :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `44. Capacity = capacité VALIDÉE, pas profondeur brute` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-CAP-0020`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, RISK, ACCOUNTING, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0053 — 45. Ça répond directement au scaling

- Source: `SRC-008`
- Location: lines 1485–1507; heading `45. Ça répond directement au scaling`
- Domain tags: EXECUTION, ACCOUNTING, CAPITAL, SIZING, PRODUCT
- Source statement: 45. Ça répond directement au scaling: 100 € → HIGH confidence 10k theoretical PnL = +25 €
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `45. Ça répond directement au scaling` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0307`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, CAPITAL, SIZING, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0054 — 46. Fragmentation : notre simulateur pourra enfin répondre scientifiquement

- Source: `SRC-008`
- Location: lines 1508–1509; heading `46. Fragmentation : notre simulateur pourra enfin répondre scientifiquement`
- Domain tags: SLICING
- Source statement: 46. Fragmentation : notre simulateur pourra enfin répondre scientifiquement: On compare :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `46. Fragmentation : notre simulateur pourra enfin répondre scientifiquement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SLICE-0005`; supporting items: none found by conservative heading match; domain indexes `SLICING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0055 — scénario A

- Source: `SRC-008`
- Location: lines 1510–1514; heading `scénario A`
- Domain tags: ARCH
- Source statement: scénario A: 1 × 2000 €
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `scénario A` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0087`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0056 — scénario B

- Source: `SRC-008`
- Location: lines 1515–1520; heading `scénario B`
- Domain tags: ARCH
- Source statement: scénario B: 40 × 50 € simultaneous
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `scénario B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0088`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0057 — scénario C

- Source: `SRC-008`
- Location: lines 1521–1526; heading `scénario C`
- Domain tags: ARCH
- Source statement: scénario C: 20 ×100 € spaced 2ms
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `scénario C` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0089`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0058 — scénario D

- Source: `SRC-008`
- Location: lines 1527–1536; heading `scénario D`
- Domain tags: ARCH
- Source statement: scénario D: adaptive: 100
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `scénario D` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0090`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0059 — 47. Même instant, même carnet

- Source: `SRC-008`
- Location: lines 1537–1550; heading `47. Même instant, même carnet`
- Domain tags: QUANT
- Source statement: 47. Même instant, même carnet: Comme on l'avait conclu : ont quasiment le même mechanical impact si tout frappe les mêmes niveaux immédiatement.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `47. Même instant, même carnet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0033`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0060 — 48. Fragmentation temporelle

- Source: `SRC-008`
- Location: lines 1551–1609; heading `48. Fragmentation temporelle`
- Domain tags: SLICING, RISK, ACCOUNTING, PARTICIPANTS, LIQUIDITY_RESPONSE, INVENTORY
- Source statement: 48. Fragmentation temporelle: Là il y a un compromis. Donc le problème devient :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `48. Fragmentation temporelle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-SLICE-0006`; supporting items: none found by conservative heading match; domain indexes `SLICING, RISK, ACCOUNTING, PARTICIPANTS, LIQUIDITY_RESPONSE, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0061 — 49. Le marché Bitcoin lui-même montre que le market impact ne se réduit pas à une simple règle linéaire

- Source: `SRC-008`
- Location: lines 1610–1621; heading `49. Le marché Bitcoin lui-même montre que le market impact ne se réduit pas à une simple règle linéaire`
- Domain tags: QUANT, RISK, VALIDATION, MICROSTRUCTURE, RESEARCH
- Source statement: 49. Le marché Bitcoin lui-même montre que le market impact ne se réduit pas à une simple règle linéaire: Des travaux sur plus d'un million de metaorders Bitcoin trouvent une relation de type *square-root* entre taille et market impact à plus grande échelle. Cela renforce l'idée qu'on ne doit pas extrapoler linéairement : Pour notre HFT court horizon, je donnerais néanmoins priorité aux données LOB/OFI Hyperliquid plutôt qu'à appliquer directement une square-root law générique.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `49. Le marché Bitcoin lui-même montre que le market impact ne se réduit pas à une simple règle linéaire` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-QUANT-0034`; supporting items: none found by conservative heading match; domain indexes `QUANT, RISK, VALIDATION, MICROSTRUCTURE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0062 — 50. Comment gérer le futur historique après notre intervention ?

- Source: `SRC-008`
- Location: lines 1622–1672; heading `50. Comment gérer le futur historique après notre intervention ?`
- Domain tags: SIMULATOR
- Source statement: 50. Comment gérer le futur historique après notre intervention ?: Je propose une solution hybride très précise. World_{cf} = World_{hist} + \Delta_{our} + \Delta_{response}
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `50. Comment gérer le futur historique après notre intervention ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-SIM-0009`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0063 — 51. Au moment de l'ordre

- Source: `SRC-008`
- Location: lines 1673–1686; heading `51. Au moment de l'ordre`
- Domain tags: EXECUTION, MICROSTRUCTURE, MAKER_MODEL
- Source statement: 51. Au moment de l'ordre: Δour contient :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `51. Au moment de l'ordre` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0308`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0064 — 52. Le marché possède une résilience

- Source: `SRC-008`
- Location: lines 1687–1694; heading `52. Le marché possède une résilience`
- Domain tags: EXECUTION, LIQUIDITY_RESPONSE, QUANT
- Source statement: 52. Le marché possède une résilience: Après un choc, la liquidité peut : La littérature parle justement de order-book resiliency, c'est-à-dire la vitesse/probabilité avec laquelle le carnet retrouve une structure normale après un choc. Cette résilience peut être modélisée via l'intensité des ordres/cancellations et n'est pas garantie après chaque gros trade. (ScienceDirect)
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `52. Le marché possède une résilience` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0309`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, LIQUIDITY_RESPONSE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0065 — 53. On aura donc une fonction de decay/résilience

- Source: `SRC-008`
- Location: lines 1695–1730; heading `53. On aura donc une fonction de decay/résilience`
- Domain tags: EXECUTION, RECOVERY, RECORDER, QUANT
- Source statement: 53. On aura donc une fonction de decay/résilience: τ = temps depuis notre intervention Les vrais chiffres viennent du Recorder.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `53. On aura donc une fonction de decay/résilience` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0310`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECORDER, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0066 — 54. Branch-and-rejoin

- Source: `SRC-008`
- Location: lines 1731–1750; heading `54. Branch-and-rejoin`
- Domain tags: RECOVERY, SIMULATOR, REPLAY, QUANT
- Source statement: 54. Branch-and-rejoin: C'est une idée que je recommande fortement. On ne tente pas de simuler un univers parallèle pendant 24 heures après un ordre de 50 €.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `54. Branch-and-rejoin` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0024`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, SIMULATOR, REPLAY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0067 — 55. Horizon variable

- Source: `SRC-008`
- Location: lines 1751–1768; heading `55. Horizon variable`
- Domain tags: LIQUIDITY_RESPONSE, QUANT
- Source statement: 55. Horizon variable: Il ne doit pas être : Un ordre minuscule sur BTC peut rejoin presque immédiatement.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `55. Horizon variable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIQ-0009`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0068 — 56. Cas où on ne rejoin PAS facilement

- Source: `SRC-008`
- Location: lines 1769–1784; heading `56. Cas où on ne rejoin PAS facilement`
- Domain tags: SIMULATOR
- Source statement: 56. Cas où on ne rejoin PAS facilement: Si notre ordre représente : et déplace le prix de plusieurs ticks :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `56. Cas où on ne rejoin PAS facilement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-SIM-0010`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0069 — 57. Agent-based simulation : est-ce qu'on la garde ?

- Source: `SRC-008`
- Location: lines 1785–1798; heading `57. Agent-based simulation : est-ce qu'on la garde ?`
- Domain tags: PARTICIPANTS, EXECUTION, INVENTORY, PRODUCT, FUTURE
- Source statement: 57. Agent-based simulation : est-ce qu'on la garde ?: Oui, mais comme laboratoire challenger, pas comme vérité de production. ABIDES démontre qu'il est possible de créer des populations importantes d'agents qui interagissent avec un exchange simulé et d'étudier l'effet d'un agent d'exécution sur le marché. (GitHub)
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `57. Agent-based simulation : est-ce qu'on la garde ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-PART-0025`; supporting items: SRC-007-ITEM-0127; domain indexes `PARTICIPANTS, EXECUTION, INVENTORY, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0070 — 58. Ce que je NE veux surtout pas

- Source: `SRC-008`
- Location: lines 1799–1821; heading `58. Ce que je NE veux surtout pas`
- Domain tags: EXECUTION, INFRA, PARTICIPANTS
- Source statement: 58. Ce que je NE veux surtout pas: "On pense qu'un market maker réagit comme ça" La littérature sur les modèles agent-based montre justement que les paramètres comportementaux peuvent être difficiles à identifier correctement même lorsque le marché simulé reproduit certaines statistiques observées. (ScienceDirect)
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `58. Ce que je NE veux surtout pas` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0311`; supporting items: SRC-003-ITEM-0111; domain indexes `EXECUTION, INFRA, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0071 — 59. Architecture finale que je construirais

- Source: `SRC-008`
- Location: lines 1822–1885; heading `59. Architecture finale que je construirais`
- Domain tags: ARCH, EXECUTION, RECONCILIATION, CLOCK, INFRA, VALIDATION, ACCOUNTING, SIMULATOR
- Source statement: 59. Architecture finale que je construirais: Tout ça en Rust côté moteur.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `59. Architecture finale que je construirais` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0091`; supporting items: none found by conservative heading match; domain indexes `ARCH, EXECUTION, RECONCILIATION, CLOCK, INFRA, VALIDATION, ACCOUNTING, SIMULATOR`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0072 — 60. Architecture de fidélité — je modifierais notre V1/V2/V3/V4

- Source: `SRC-008`
- Location: lines 1886–1888; heading `60. Architecture de fidélité — je modifierais notre V1/V2/V3/V4`
- Domain tags: PRODUCT, ARCH, FUTURE
- Source statement: 60. Architecture de fidélité — je modifierais notre V1/V2/V3/V4: Comme on veut une architecture finale dès le départ, je ne parlerais plus de versions successives du bot. Je parlerais de niveaux de fidélité du même simulateur.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `60. Architecture de fidélité — je modifierais notre V1/V2/V3/V4` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-PRODUCT-0023`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0073 — F0 — Historical

- Source: `SRC-008`
- Location: lines 1889–1897; heading `F0 — Historical`
- Domain tags: ACCOUNTING
- Source statement: F0 — Historical: historical book L2 execution
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `F0 — Historical` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0063`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0074 — F1 — Latency + Mechanical

- Source: `SRC-008`
- Location: lines 1898–1910; heading `F1 — Latency + Mechanical`
- Domain tags: INFRA, EXECUTION, VALIDATION
- Source statement: F1 — Latency + Mechanical: real arrival time shadow book
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `F1 — Latency + Mechanical` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0054`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, VALIDATION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0075 — F2 — Queue

- Source: `SRC-008`
- Location: lines 1911–1923; heading `F2 — Queue`
- Domain tags: MICROSTRUCTURE, EXECUTION, QUANT, PRODUCT
- Source statement: F2 — Queue: price-time priority maker queue
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `F2 — Queue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0028`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0076 — F3 — Responsive

- Source: `SRC-008`
- Location: lines 1924–1936; heading `F3 — Responsive`
- Domain tags: LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE
- Source statement: F3 — Responsive: resilience empirical response
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `F3 — Responsive` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0010`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0077 — F4 — Interactive Research

- Source: `SRC-008`
- Location: lines 1937–1950; heading `F4 — Interactive Research`
- Domain tags: SIMULATOR, RESEARCH, EXECUTION, PARTICIPANTS, MICROSTRUCTURE, QUANT, ARCH
- Source statement: F4 — Interactive Research: Différents niveaux activés selon disponibilité des données.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `F4 — Interactive Research` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0011`; supporting items: SRC-007-ITEM-0134; domain indexes `SIMULATOR, RESEARCH, EXECUTION, PARTICIPANTS, MICROSTRUCTURE, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0078 — 61. Et le simulateur choisit lui-même son niveau de confiance

- Source: `SRC-008`
- Location: lines 1951–1985; heading `61. Et le simulateur choisit lui-même son niveau de confiance`
- Domain tags: EXECUTION, MICROSTRUCTURE, TRIANGLE, ROUTING, QUANT
- Source statement: 61. Et le simulateur choisit lui-même son niveau de confiance: Pas besoin de 10 000 agents artificiels.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `61. Et le simulateur choisit lui-même son niveau de confiance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0312`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, TRIANGLE, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0079 — 62. Données qu'on DOIT absolument enregistrer

- Source: `SRC-008`
- Location: lines 1986–2009; heading `62. Données qu'on DOIT absolument enregistrer`
- Domain tags: EXECUTION, RECORDER, CLOCK, DETERMINISM, INFRA, VALIDATION, ACCOUNTING, MICROSTRUCTURE
- Source statement: 62. Données qu'on DOIT absolument enregistrer: Pour rendre tout cela possible : raw market payload | reconstruire
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `62. Données qu'on DOIT absolument enregistrer` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0313`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, CLOCK, DETERMINISM, INFRA, VALIDATION, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0080 — 63. Micro-live devient absolument indispensable

- Source: `SRC-008`
- Location: lines 2010–2022; heading `63. Micro-live devient absolument indispensable`
- Domain tags: VALIDATION, RISK, REPLAY
- Source statement: 63. Micro-live devient absolument indispensable: Le Replay peut apprendre sur le marché historique. Mais il nous manque :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `63. Micro-live devient absolument indispensable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0374`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481, SRC-006-ITEM-0418; domain indexes `VALIDATION, RISK, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0081 — 64. Chaque micro-live produit un datapoint

- Source: `SRC-008`
- Location: lines 2023–2054; heading `64. Chaque micro-live produit un datapoint`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, INFRA, ACCOUNTING, MICROSTRUCTURE, INVENTORY, ROUTING
- Source statement: 64. Chaque micro-live produit un datapoint: Avant ordre : spread
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `64. Chaque micro-live produit un datapoint` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0375`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481, SRC-006-ITEM-0418; domain indexes `VALIDATION, EXECUTION, RECOVERY, INFRA, ACCOUNTING, MICROSTRUCTURE, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0082 — 65. Pour le maker particulièrement

- Source: `SRC-008`
- Location: lines 2055–2071; heading `65. Pour le maker particulièrement`
- Domain tags: EXECUTION, MICROSTRUCTURE, QUANT
- Source statement: 65. Pour le maker particulièrement: Après 1 000 ordres qui avaient une prédiction autour de 70 % : notre Queue Model est mauvais.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `65. Pour le maker particulièrement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0314`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0083 — 66. Validation du slippage

- Source: `SRC-008`
- Location: lines 2072–2128; heading `66. Validation du slippage`
- Domain tags: VALIDATION, QUANT
- Source statement: 66. Validation du slippage: Error = ActualSlippage - PredictedSlippage On ne veut pas uniquement :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `66. Validation du slippage` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0376`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0084 — 67. Validation de la distribution

- Source: `SRC-008`
- Location: lines 2129–2143; heading `67. Validation de la distribution`
- Domain tags: VALIDATION, PRODUCT, EXECUTION
- Source statement: 67. Validation de la distribution: Si notre modèle dit régulièrement : alors environ 95 % des vrais résultats comparables devraient tomber dedans.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `67. Validation de la distribution` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0377`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0085 — 68. Champion / Challenger

- Source: `SRC-008`
- Location: lines 2144–2167; heading `68. Champion / Challenger`
- Domain tags: FUTURE, EXECUTION, VALIDATION, ACCOUNTING, MICROSTRUCTURE, PRODUCT
- Source statement: 68. Champion / Challenger: Comme le reste du bot : doit battre v3 sur :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `68. Champion / Challenger` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0012`; supporting items: SRC-001-ITEM-0109, SRC-005-ITEM-0455, SRC-007-ITEM-0046, SRC-007-ITEM-0103; domain indexes `FUTURE, EXECUTION, VALIDATION, ACCOUNTING, MICROSTRUCTURE, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0086 — 69. Les autres bots seront donc intégrés à trois niveaux

- Source: `SRC-008`
- Location: lines 2168–2169; heading `69. Les autres bots seront donc intégrés à trois niveaux`
- Domain tags: ARCH
- Source statement: 69. Les autres bots seront donc intégrés à trois niveaux: C'est la bonne réponse à ta question initiale.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `69. Les autres bots seront donc intégrés à trois niveaux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0092`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0087 — Niveau A — implicitement

- Source: `SRC-008`
- Location: lines 2170–2173; heading `Niveau A — implicitement`
- Domain tags: ARCH
- Source statement: Niveau A — implicitement: L'historique contient déjà leur activité réelle.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Niveau A — implicitement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0093`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0088 — Niveau B — statistiquement

- Source: `SRC-008`
- Location: lines 2174–2182; heading `Niveau B — statistiquement`
- Domain tags: ARCH
- Source statement: Niveau B — statistiquement: On apprend : leur réaction agrégée
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Niveau B — statistiquement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0094`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0089 — Niveau C — explicitement

- Source: `SRC-008`
- Location: lines 2183–2186; heading `Niveau C — explicitement`
- Domain tags: PARTICIPANTS
- Source statement: Niveau C — explicitement: Agent-based model avec agents synthétiques.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Niveau C — explicitement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0026`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0090 — 70. Ce que je considère comme NON nécessaire au départ

- Source: `SRC-008`
- Location: lines 2187–2200; heading `70. Ce que je considère comme NON nécessaire au départ`
- Domain tags: EXECUTION, ACCOUNTING, SIMULATOR, FUTURE
- Source statement: 70. Ce que je considère comme NON nécessaire au départ: Je ne construirais pas immédiatement : Ça peut devenir intéressant plus tard.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `70. Ce que je considère comme NON nécessaire au départ` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0315`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, SIMULATOR, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0091 — 71. En revanche certaines choses sont NON négociables dès le départ

- Source: `SRC-008`
- Location: lines 2201–2219; heading `71. En revanche certaines choses sont NON négociables dès le départ`
- Domain tags: EXECUTION, VALIDATION, SIMULATOR, REPLAY, CROSS_MARKET, MICROSTRUCTURE, QUANT, ARCH
- Source statement: 71. En revanche certaines choses sont NON négociables dès le départ: Je veux dans l'architecture finale : 2. replay au vrai temps d'arrivée.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `71. En revanche certaines choses sont NON négociables dès le départ` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0316`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, VALIDATION, SIMULATOR, REPLAY, CROSS_MARKET, MICROSTRUCTURE, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0092 — 72. Décision d'exécution finale

- Source: `SRC-008`
- Location: lines 2220–2262; heading `72. Décision d'exécution finale`
- Domain tags: EXECUTION, RECOVERY, RISK, INFRA, ACCOUNTING, MICROSTRUCTURE, CAPITAL, ROUTING
- Source statement: 72. Décision d'exécution finale: À terme notre route ne dit plus : Puis le Risk Engine décide.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `72. Décision d'exécution finale` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0317`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, INFRA, ACCOUNTING, MICROSTRUCTURE, CAPITAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0093 — 73. Exemple réaliste

- Source: `SRC-008`
- Location: lines 2263–2313; heading `73. Exemple réaliste`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING
- Source statement: 73. Exemple réaliste: Mais notre simulateur trouve : mean recovery loss -1.80 €
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `73. Exemple réaliste` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0318`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0094 — 74. Même route à 5 000 €

- Source: `SRC-008`
- Location: lines 2314–2351; heading `74. Même route à 5 000 €`
- Domain tags: ROUTING, EXECUTION, RISK, ACCOUNTING, CROSS_MARKET, SIZING, QUANT
- Source statement: 74. Même route à 5 000 €: validated size = 1 150 € C’est là que notre dynamic sizing devient extrêmement puissant.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `74. Même route à 5 000 €` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0037`; supporting items: none found by conservative heading match; domain indexes `ROUTING, EXECUTION, RISK, ACCOUNTING, CROSS_MARKET, SIZING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0095 — 75. Donc notre sizing pourra utiliser directement le simulateur

- Source: `SRC-008`
- Location: lines 2352–2431; heading `75. Donc notre sizing pourra utiliser directement le simulateur`
- Domain tags: SIZING, RISK, ACCOUNTING
- Source statement: 75. Donc notre sizing pourra utiliser directement le simulateur: et toutes nos limites portefeuille. Le résultat peut être :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `75. Donc notre sizing pourra utiliser directement le simulateur` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIZE-0005`; supporting items: none found by conservative heading match; domain indexes `SIZING, RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0097 — On garde

- Source: `SRC-008`
- Location: lines 2433–2445; heading `On garde`
- Domain tags: EXECUTION, VALIDATION, SIMULATOR, PARTICIPANTS, MICROSTRUCTURE, QUANT
- Source statement: On garde: Shadow Book Mechanical Impact
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `On garde` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0319`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, VALIDATION, SIMULATOR, PARTICIPANTS, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0098 — On corrige

- Source: `SRC-008`
- Location: lines 2446–2463; heading `On corrige`
- Domain tags: EXECUTION, SIMULATOR, REPLAY, CROSS_MARKET, MICROSTRUCTURE, CAPITAL, QUANT, FUTURE
- Source statement: On corrige: “Leg1 modifie mécaniquement les autres books.” Elle ne modifie directement que le book utilisé ; les autres passent par CrossMarketResponse.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `On corrige` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0320`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, SIMULATOR, REPLAY, CROSS_MARKET, MICROSTRUCTURE, CAPITAL, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0099 — 77. La réponse fondamentale à notre interrogation n°3

- Source: `SRC-008`
- Location: lines 2464–2564; heading `77. La réponse fondamentale à notre interrogation n°3`
- Domain tags: FORMULA, SIMULATOR, QUANT, FUTURE
- Source statement: 77. La réponse fondamentale à notre interrogation n°3: Notre Counterfactual Simulator doit être conçu autour de cette équation conceptuelle : Future_{CF} = HistoricalBaseline + OurMechanicalIntervention + StochasticMarketResponse
- Nature: formula/definition
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `77. La réponse fondamentale à notre interrogation n°3` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FORMULA-0151`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SIMULATOR, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0100 — 78. Direction que je figerais pour le projet

- Source: `SRC-008`
- Location: lines 2565–2620; heading `78. Direction que je figerais pour le projet`
- Domain tags: EXECUTION, RISK, INFRA, VALIDATION, ACCOUNTING, SIMULATOR, REPLAY, CROSS_MARKET
- Source statement: 78. Direction que je figerais pour le projet: Je considère maintenant cette architecture comme notre cible :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `78. Direction que je figerais pour le projet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0321`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, VALIDATION, ACCOUNTING, SIMULATOR, REPLAY, CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0101 — Le principe final

- Source: `SRC-008`
- Location: lines 2621–2640; heading `Le principe final`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING, CAPITAL, SIZING, QUANT, PRODUCT
- Source statement: Le principe final: On ne cherchera jamais à prétendre avoir un “backtest parfait”. On cherchera quelque chose de beaucoup plus utile :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Le principe final` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0322`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING, CAPITAL, SIZING, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0102 — 1. TT — Taker → Taker

- Source: `SRC-008`
- Location: lines 2641–2663; heading `1. TT — Taker → Taker`
- Domain tags: EXECUTION, OWA
- Source statement: 1. TT — Taker → Taker: A ──T──> X ──T──> B C’est le vrai OWA immédiat.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `1. TT — Taker → Taker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0323`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0103 — 2. MT — Maker → Taker

- Source: `SRC-008`
- Location: lines 2664–2706; heading `2. MT — Maker → Taker`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING, SIMULATOR, MICROSTRUCTURE, MAKER_MODEL, QUANT
- Source statement: 2. MT — Maker → Taker: A ──M──> X ──T──> B C’est probablement la deuxième stratégie majeure.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `2. MT — Maker → Taker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0324`; supporting items: SRC-002-ITEM-0079, SRC-004-ITEM-0057, SRC-005-ITEM-0131; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING, SIMULATOR, MICROSTRUCTURE, MAKER_MODEL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0104 — 3. TM — Taker → Maker

- Source: `SRC-008`
- Location: lines 2707–2748; heading `3. TM — Taker → Maker`
- Domain tags: EXECUTION, RISK, ACCOUNTING, INVENTORY, PRODUCT
- Source statement: 3. TM — Taker → Maker: A ──T──> X ──M──> B On vient donc de transformer un arbitrage très court en :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `3. TM — Taker → Maker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0325`; supporting items: SRC-002-ITEM-0079, SRC-004-ITEM-0057, SRC-005-ITEM-0131; domain indexes `EXECUTION, RISK, ACCOUNTING, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0105 — 4. MM — Maker → Maker

- Source: `SRC-008`
- Location: lines 2749–2775; heading `4. MM — Maker → Maker`
- Domain tags: EXECUTION, MICROSTRUCTURE, MAKER_MODEL, ROUTING, ARCH
- Source statement: 4. MM — Maker → Maker: A ──M──> X ──M──> B La première jambe peut être relativement sûre puisqu’on reste en A avant son fill.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `4. MM — Maker → Maker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0326`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, MAKER_MODEL, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0106 — La subtilité importante pour notre OWA

- Source: `SRC-008`
- Location: lines 2776–2826; heading `La subtilité importante pour notre OWA`
- Domain tags: OWA, EXECUTION, ROUTING
- Source statement: La subtilité importante pour notre OWA: Quand on compare la route indirecte à la route directe, il faut comparer des stratégies d’exécution cohérentes. Par exemple pour TT :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `La subtilité importante pour notre OWA` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OWA-0008`; supporting items: none found by conservative heading match; domain indexes `OWA, EXECUTION, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0107 — Ce que je corrigerais donc dans l’interrogation n°2

- Source: `SRC-008`
- Location: lines 2827–2861; heading `Ce que je corrigerais donc dans l’interrogation n°2`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING, REPLAY, INVENTORY, ROUTING, ARCH
- Source statement: Ce que je corrigerais donc dans l’interrogation n°2: ├── TM → SUPPORTED / DISABLED └── MM → SUPPORTED / DISABLED
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Ce que je corrigerais donc dans l’interrogation n°2` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0327`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING, REPLAY, INVENTORY, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0109 — 1. Objectif de l’infrastructure

- Source: `SRC-008`
- Location: lines 2863–2928; heading `1. Objectif de l’infrastructure`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 1. Objectif de l’infrastructure: L’objectif n’est pas d’avoir « le serveur le plus puissant ». Recevoir l’information Hyperliquid suffisamment tôt, prendre la décision suffisamment vite, envoyer l’ordre avec une latence et un jitter suffisamment faibles, tout en maximisant le PnL net après coût d’infrastructure.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `1. Objectif de l’infrastructure` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0055`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0110 — 2. Décomposition de la latence

- Source: `SRC-008`
- Location: lines 2929–3185; heading `2. Décomposition de la latence`
- Domain tags: EXECUTION, RISK, ACCOUNTING, ROUTING, ARCH
- Source statement: 2. Décomposition de la latence: La latence complète d’une opportunité peut être représentée par : L_{total} = L_{feed} + L_{network,in} + L_{decode} + L_{book} + L_{routes} + L_{simulation} + L_{risk} + L_{decision} + L_{sign} + L_{network,out} + L_{exchange}
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `2. Décomposition de la latence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0328`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, ACCOUNTING, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0111 — 3. Localisation : Tokyo

- Source: `SRC-008`
- Location: lines 3186–3205; heading `3. Localisation : Tokyo`
- Domain tags: INFRA, NODE, ARCH
- Source statement: 3. Localisation : Tokyo: Pour Hyperliquid, Tokyo est notre région de référence. La documentation officielle du node indique actuellement :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `3. Localisation : Tokyo` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0056`; supporting items: none found by conservative heading match; domain indexes `INFRA, NODE, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0112 — 4. Le node n’est PAS notre infrastructure de départ

- Source: `SRC-008`
- Location: lines 3206–3238; heading `4. Le node n’est PAS notre infrastructure de départ`
- Domain tags: INFRA, EXECUTION, RISK, NODE, ACCOUNTING, ARCH, FUTURE
- Source statement: 4. Le node n’est PAS notre infrastructure de départ: Notre architecture doit être compatible avec : mais le bot démarre avec :
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `4. Le node n’est PAS notre infrastructure de départ` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INFRA-0057`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, RISK, NODE, ACCOUNTING, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0113 — 5. Infrastructure minimum de départ

- Source: `SRC-008`
- Location: lines 3239–3276; heading `5. Infrastructure minimum de départ`
- Domain tags: INFRA, RISK, CLIENT, ACCOUNTING, ROUTING
- Source statement: 5. Infrastructure minimum de départ: Notre bot personnel n’a pas besoin aujourd’hui de : Ubuntu 24.04 x86-64 de préférence
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `5. Infrastructure minimum de départ` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0058`; supporting items: none found by conservative heading match; domain indexes `INFRA, RISK, CLIENT, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0114 — 6. Pourquoi CPU dédié > beaucoup de vCPU partagés

- Source: `SRC-008`
- Location: lines 3277–3308; heading `6. Pourquoi CPU dédié > beaucoup de vCPU partagés`
- Domain tags: INFRA, RISK, BENCHMARK, DEPLOYMENT, ROUTING, GRAPH, HOT_WARM_COLD, ARCH
- Source statement: 6. Pourquoi CPU dédié > beaucoup de vCPU partagés: Notre hot path est court : * de la performance single-thread ;
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `6. Pourquoi CPU dédié > beaucoup de vCPU partagés` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0059`; supporting items: none found by conservative heading match; domain indexes `INFRA, RISK, BENCHMARK, DEPLOYMENT, ROUTING, GRAPH, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0115 — 7. 10 Gb/s n’est pas notre KPI principal

- Source: `SRC-008`
- Location: lines 3309–3339; heading `7. 10 Gb/s n’est pas notre KPI principal`
- Domain tags: INFRA, BENCHMARK, ROUTING
- Source statement: 7. 10 Gb/s n’est pas notre KPI principal: Notre flux de trading consomme très peu de bande passante comparé à 1 Gb/s. Nos KPI réseau sont donc :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `7. 10 Gb/s n’est pas notre KPI principal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0060`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0117 — TradingFXVPS — VPS standard

- Source: `SRC-008`
- Location: lines 3341–3370; heading `TradingFXVPS — VPS standard`
- Domain tags: INFRA, EXECUTION, DEPLOYMENT, ARCH
- Source statement: TradingFXVPS — VPS standard: Leur gamme standard comprend actuellement notamment : 2 cores AMD Ryzen 9 @ 4.3 GHz
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `TradingFXVPS — VPS standard` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0061`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, DEPLOYMENT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0118 — 9. TradingFXVPS — HFT VPS

- Source: `SRC-008`
- Location: lines 3371–3463; heading `9. TradingFXVPS — HFT VPS`
- Domain tags: INFRA, EXECUTION, BENCHMARK, ACCOUNTING, ARCH
- Source statement: 9. TradingFXVPS — HFT VPS: Leur Standard HFT est actuellement : 4 cores @ 4.30 GHz+
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `9. TradingFXVPS — HFT VPS` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0062`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, BENCHMARK, ACCOUNTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0119 — 10. TradingFXVPS — Semi-Dedicated

- Source: `SRC-008`
- Location: lines 3464–3482; heading `10. TradingFXVPS — Semi-Dedicated`
- Domain tags: INFRA, EXECUTION, RISK, ARCH
- Source statement: 10. TradingFXVPS — Semi-Dedicated: Ils proposent aussi Tokyo : 10 cores Ryzen 4.30 GHz
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `10. TradingFXVPS — Semi-Dedicated` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0063`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, RISK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0120 — 11. TradingFXVPS — HFT Dedicated

- Source: `SRC-008`
- Location: lines 3483–3502; heading `11. TradingFXVPS — HFT Dedicated`
- Domain tags: INFRA, NODE, ACCOUNTING
- Source statement: 11. TradingFXVPS — HFT Dedicated: Tokyo est également disponible : 2 × 2 TB NVMe RAID1
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `11. TradingFXVPS — HFT Dedicated` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0064`; supporting items: none found by conservative heading match; domain indexes `INFRA, NODE, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0121 — 12. Akamai / Linode Dedicated CPU

- Source: `SRC-008`
- Location: lines 3503–3528; heading `12. Akamai / Linode Dedicated CPU`
- Domain tags: INFRA, BENCHMARK
- Source statement: 12. Akamai / Linode Dedicated CPU: Akamai propose en Asie-Pacifique, dont Tokyo, des plans Dedicated CPU. C’est un excellent benchmark parce qu’on dispose :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `12. Akamai / Linode Dedicated CPU` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0065`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0122 — 13. Kamatera Type B

- Source: `SRC-008`
- Location: lines 3529–3542; heading `13. Kamatera Type B`
- Domain tags: INFRA
- Source statement: 13. Kamatera Type B: Le Type B attribue un thread CPU dédié avec ressources réservées afin de réduire les fluctuations de charge. C’est également un excellent candidat pour notre gamme économique.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `13. Kamatera Type B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0066`; supporting items: none found by conservative heading match; domain indexes `INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0123 — 14. AWS Lightsail Compute Optimized

- Source: `SRC-008`
- Location: lines 3543–3557; heading `14. AWS Lightsail Compute Optimized`
- Domain tags: INFRA, BENCHMARK
- Source statement: 14. AWS Lightsail Compute Optimized: AWS Tokyo mérite d’être testé, notamment parce que la Foundation Hyperliquid indique que son non-validating node tourne actuellement sur AWS apne1-az1. Cela ne signifie pas que l’API publique y est colocalisée, mais justifie au minimum un benchmark.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `14. AWS Lightsail Compute Optimized` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0067`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0124 — 15. Sakura VPS Tokyo

- Source: `SRC-008`
- Location: lines 3558–3583; heading `15. Sakura VPS Tokyo`
- Domain tags: INFRA, BENCHMARK, FUTURE
- Source statement: 15. Sakura VPS Tokyo: Sakura est particulièrement intéressant comme challenger économique local japonais. 3 630 ¥ / mois équivalent
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `15. Sakura VPS Tokyo` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0068`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0125 — 16. Cherry Servers Performance VDS

- Source: `SRC-008`
- Location: lines 3584–3610; heading `16. Cherry Servers Performance VDS`
- Domain tags: INFRA, BENCHMARK, RISK, ARCH, FUTURE
- Source statement: 16. Cherry Servers Performance VDS: Pour avoir une référence « performance Linux » sans aller directement au bare metal à 500 €, Cherry propose à Tokyo : 4 vCores @ 4.5 GHz
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `16. Cherry Servers Performance VDS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0069`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, RISK, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0126 — 17. Shortlist de benchmark initial

- Source: `SRC-008`
- Location: lines 3611–3632; heading `17. Shortlist de benchmark initial`
- Domain tags: BENCHMARK, INFRA, NODE, ACCOUNTING
- Source statement: 17. Shortlist de benchmark initial: La première campagne doit tester : Trading économique | TradingFX Advanced
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `17. Shortlist de benchmark initial` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BENCH-0009`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, INFRA, NODE, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0127 — 18. Pourquoi benchmarker TradingFX Advanced ET HFT

- Source: `SRC-008`
- Location: lines 3633–3659; heading `18. Pourquoi benchmarker TradingFX Advanced ET HFT`
- Domain tags: INFRA, BENCHMARK, ARCH
- Source statement: 18. Pourquoi benchmarker TradingFX Advanced ET HFT: Parce que c’est une question économique extrêmement intéressante. +1 % de performance technique
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `18. Pourquoi benchmarker TradingFX Advanced ET HFT` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0070`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0128 — 19. Principe du benchmark

- Source: `SRC-008`
- Location: lines 3660–3682; heading `19. Principe du benchmark`
- Domain tags: BENCHMARK, INFRA, ARCH
- Source statement: 19. Principe du benchmark: On ne compare jamais les fournisseurs via : On construit un programme Rust :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `19. Principe du benchmark` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BENCH-0010`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, INFRA, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0130 — Phase A — Screening

- Source: `SRC-008`
- Location: lines 3684–3691; heading `Phase A — Screening`
- Domain tags: ARCH
- Source statement: Phase A — Screening: Durée : 72 heures
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Phase A — Screening` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0095`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0131 — Phase B — Finalistes

- Source: `SRC-008`
- Location: lines 3692–3710; heading `Phase B — Finalistes`
- Domain tags: RISK, INFRA, BENCHMARK, ROUTING
- Source statement: Phase B — Finalistes: Les deux meilleurs restent actifs : On ne sélectionne pas un VPS après dix minutes de ping.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Phase B — Finalistes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0328`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, BENCHMARK, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0132 — 21. Synchronisation des horloges

- Source: `SRC-008`
- Location: lines 3711–3769; heading `21. Synchronisation des horloges`
- Domain tags: CLOCK, INFRA
- Source statement: 21. Synchronisation des horloges: Pour comparer la réception d’un même événement sur plusieurs serveurs : Pour les durées internes du programme :
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `21. Synchronisation des horloges` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CLOCK-0015`; supporting items: none found by conservative heading match; domain indexes `CLOCK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0133 — 22. Benchmark n°1 — First Market Data Arrival

- Source: `SRC-008`
- Location: lines 3770–3846; heading `22. Benchmark n°1 — First Market Data Arrival`
- Domain tags: BENCHMARK, RISK, DATA, CLOCK, INFRA, CROSS_MARKET, QUANT
- Source statement: 22. Benchmark n°1 — First Market Data Arrival: C’est probablement notre test principal. Tous les VPS souscrivent au même événement.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `22. Benchmark n°1 — First Market Data Arrival` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-BENCH-0011`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, RISK, DATA, CLOCK, INFRA, CROSS_MARKET, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0134 — 23. Benchmark n°2 — Feed Age

- Source: `SRC-008`
- Location: lines 3847–3889; heading `23. Benchmark n°2 — Feed Age`
- Domain tags: BENCHMARK, ACCOUNTING, CLOCK, INFRA
- Source statement: 23. Benchmark n°2 — Feed Age: Si l’événement contient un timestamp exchange exploitable : FeedAge = RecvTime - ExchangeTime
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `23. Benchmark n°2 — Feed Age` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0012`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, ACCOUNTING, CLOCK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0135 — 24. Benchmark n°3 — API / WebSocket RTT

- Source: `SRC-008`
- Location: lines 3890–3915; heading `24. Benchmark n°3 — API / WebSocket RTT`
- Domain tags: BENCHMARK, INFRA
- Source statement: 24. Benchmark n°3 — API / WebSocket RTT: On ne recrée pas TCP/TLS pour chaque requête puisque notre bot réel ne fonctionnerait pas ainsi.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `24. Benchmark n°3 — API / WebSocket RTT` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0013`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0136 — 25. Benchmark n°4 — Full Reconnect

- Source: `SRC-008`
- Location: lines 3916–3947; heading `25. Benchmark n°4 — Full Reconnect`
- Domain tags: BENCHMARK, OPERATIONS, ACCOUNTING
- Source statement: 25. Benchmark n°4 — Full Reconnect: → first valid market event Le bot doit savoir combien de temps il lui faut pour retrouver un état de marché utilisable après une panne.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `25. Benchmark n°4 — Full Reconnect` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BENCH-0014`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, OPERATIONS, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0137 — 26. Benchmark n°5 — Network Stability

- Source: `SRC-008`
- Location: lines 3948–3967; heading `26. Benchmark n°5 — Network Stability`
- Domain tags: BENCHMARK, ROUTING
- Source statement: 26. Benchmark n°5 — Network Stability: Toutes les quelques minutes : détecter les fournisseurs excellents à 3 h du matin mais mauvais pendant les périodes de charge.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `26. Benchmark n°5 — Network Stability` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0015`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0138 — 27. Benchmark n°6 — Hot-Path CPU

- Source: `SRC-008`
- Location: lines 3968–4005; heading `27. Benchmark n°6 — Hot-Path CPU`
- Domain tags: INFRA, BENCHMARK, ROUTING, HOT_WARM_COLD, RISK, DEPLOYMENT, ACCOUNTING, GRAPH
- Source statement: 27. Benchmark n°6 — Hot-Path CPU: On ne se fie pas principalement à Geekbench. On utilise notre propre workload.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `27. Benchmark n°6 — Hot-Path CPU` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0071`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, ROUTING, HOT_WARM_COLD, RISK, DEPLOYMENT, ACCOUNTING, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0139 — 28. Benchmark n°7 — Scheduler Jitter

- Source: `SRC-008`
- Location: lines 4006–4075; heading `28. Benchmark n°7 — Scheduler Jitter`
- Domain tags: INFRA, BENCHMARK, QUANT, RESEARCH
- Source statement: 28. Benchmark n°7 — Scheduler Jitter: Un thread de benchmark demande à être réveillé à des intervalles réguliers. SchedulerDelay = ActualWake - ExpectedWake
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `28. Benchmark n°7 — Scheduler Jitter` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0072`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0140 — 29. Benchmark n°8 — CPU contention

- Source: `SRC-008`
- Location: lines 4076–4093; heading `29. Benchmark n°8 — CPU contention`
- Domain tags: INFRA, BENCHMARK, EXECUTION, MICROSTRUCTURE
- Source statement: 29. Benchmark n°8 — CPU contention: Un VPS partagé peut être excellent pendant 90 % du temps mais catastrophique lorsque ses voisins utilisent l’hyperviseur.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `29. Benchmark n°8 — CPU contention` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0073`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, EXECUTION, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0141 — 30. Benchmark n°9 — Recorder Stress

- Source: `SRC-008`
- Location: lines 4094–4181; heading `30. Benchmark n°9 — Recorder Stress`
- Domain tags: EXECUTION, RECORDER, BENCHMARK, INFRA, ROUTING, ARCH
- Source statement: 30. Benchmark n°9 — Recorder Stress: RecorderPenalty = Latency_{with\ recorder} - Latency_{without} Si le Recorder fait passer :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `30. Benchmark n°9 — Recorder Stress` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0329`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, BENCHMARK, INFRA, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0142 — 31. Benchmark n°10 — Storage

- Source: `SRC-008`
- Location: lines 4182–4195; heading `31. Benchmark n°10 — Storage`
- Domain tags: BENCHMARK, EXECUTION, RECORDER, INFRA, MICROSTRUCTURE, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 31. Benchmark n°10 — Storage: Le but n’est pas de gagner un concours NVMe. le stockage ne doit jamais perturber notre hot path.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `31. Benchmark n°10 — Storage` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BENCH-0016`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, EXECUTION, RECORDER, INFRA, MICROSTRUCTURE, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0143 — 32. Benchmark n°11 — RAM

- Source: `SRC-008`
- Location: lines 4196–4227; heading `32. Benchmark n°11 — RAM`
- Domain tags: INFRA, BENCHMARK, EXECUTION, RECORDER, INVENTORY, ROUTING, GRAPH, HOT_WARM_COLD
- Source statement: 32. Benchmark n°11 — RAM: Ça décidera réellement si :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `32. Benchmark n°11 — RAM` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0074`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, EXECUTION, RECORDER, INVENTORY, ROUTING, GRAPH, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0144 — 33. Benchmark n°12 — Docker Overhead

- Source: `SRC-008`
- Location: lines 4228–4230; heading `33. Benchmark n°12 — Docker Overhead`
- Domain tags: BENCHMARK, DEPLOYMENT
- Source statement: 33. Benchmark n°12 — Docker Overhead: Notre produit final sera une image Docker.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `33. Benchmark n°12 — Docker Overhead` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0017`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, DEPLOYMENT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0145 — Native

- Source: `SRC-008`
- Location: lines 4231–4235; heading `Native`
- Domain tags: ARCH
- Source statement: Native: ./trading-engine
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Native` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0096`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0146 — Docker

- Source: `SRC-008`
- Location: lines 4236–4250; heading `Docker`
- Domain tags: DEPLOYMENT, RECORDER, INFRA, BENCHMARK, ROUTING
- Source statement: Docker: L’image Docker ne doit pas introduire une dégradation matérielle significative.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Docker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0217`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECORDER, INFRA, BENCHMARK, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0147 — 34. Score technique de screening

- Source: `SRC-008`
- Location: lines 4251–4377; heading `34. Score technique de screening`
- Domain tags: ARCH, EXECUTION, INFRA, BENCHMARK, DEPLOYMENT, OPERATIONS, ACCOUNTING, ROUTING
- Source statement: 34. Score technique de screening: On peut créer un score de 100 points : TechnicalScore = 0.25S_{feed} + 0.20S_{network} + 0.10S_{jitter} + 0.15S_{compute} + 0.10S_{scheduler} + 0.08S_{operations} + 0.07S_{cost} + 0.03S_{storage} + 0.02S_{reliability}
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `34. Score technique de screening` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0097`; supporting items: none found by conservative heading match; domain indexes `ARCH, EXECUTION, INFRA, BENCHMARK, DEPLOYMENT, OPERATIONS, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0148 — 35. Testnet Hyperliquid

- Source: `SRC-008`
- Location: lines 4378–4412; heading `35. Testnet Hyperliquid`
- Domain tags: EXECUTION, INFRA, BENCHMARK
- Source statement: 35. Testnet Hyperliquid: Après le benchmark purement infrastructure : les performances testnet ne doivent pas être considérées comme identiques au mainnet.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `35. Testnet Hyperliquid` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0330`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0149 — 36. Micro-live mainnet

- Source: `SRC-008`
- Location: lines 4413–4442; heading `36. Micro-live mainnet`
- Domain tags: VALIDATION, EXECUTION, RISK, ACCOUNTING, SIZING
- Source statement: 36. Micro-live mainnet: Cette taille n’est pas notre sizing stratégique définitif. Elle est un outil de calibration.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `36. Micro-live mainnet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0378`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481, SRC-006-ITEM-0418; domain indexes `VALIDATION, EXECUTION, RISK, ACCOUNTING, SIZING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0150 — 37. Test A/B entre deux infrastructures

- Source: `SRC-008`
- Location: lines 4443–4456; heading `37. Test A/B entre deux infrastructures`
- Domain tags: INFRA
- Source statement: 37. Test A/B entre deux infrastructures: On ne fait pas envoyer simultanément deux ordres identiques depuis deux serveurs. Opportunity 1 → Provider A
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `37. Test A/B entre deux infrastructures` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0075`; supporting items: none found by conservative heading match; domain indexes `INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0151 — 38. KPI économique n°1 — Capture Ratio

- Source: `SRC-008`
- Location: lines 4457–4574; heading `38. KPI économique n°1 — Capture Ratio`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 38. KPI économique n°1 — Capture Ratio: WeightedCaptureRatio = \frac{\sum RealizedPnL} {\sum ExpectedPnL} sur un ensemble comparable d’ordres.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `38. KPI économique n°1 — Capture Ratio` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0076`; supporting items: SRC-004-ITEM-0253; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0152 — 39. KPI n°2 — Opportunity Survival

- Source: `SRC-008`
- Location: lines 4575–4649; heading `39. KPI n°2 — Opportunity Survival`
- Domain tags: SURVIVAL, EXECUTION, INFRA, ACCOUNTING, MICROSTRUCTURE
- Source statement: 39. KPI n°2 — Opportunity Survival: profitable at estimated order arrival? Ça mesure directement la capacité de notre infrastructure à arriver avant disparition de l’edge.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `39. KPI n°2 — Opportunity Survival` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0023`; supporting items: SRC-004-ITEM-0254; domain indexes `SURVIVAL, EXECUTION, INFRA, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0153 — 40. KPI n°3 — Missed Opportunity Due To Infra

- Source: `SRC-008`
- Location: lines 4650–4681; heading `40. KPI n°3 — Missed Opportunity Due To Infra`
- Domain tags: INFRA, EXECUTION, RISK, ACCOUNTING, INVENTORY, QUANT
- Source statement: 40. KPI n°3 — Missed Opportunity Due To Infra: Chaque opportunité ratée reçoit une cause. c’est-à-dire le PnL théorique réaliste que notre infrastructure actuelle nous fait perdre.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `40. KPI n°3 — Missed Opportunity Due To Infra` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0077`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, RISK, ACCOUNTING, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0154 — 41. Pourquoi InfraLostPnL est fondamental

- Source: `SRC-008`
- Location: lines 4682–4705; heading `41. Pourquoi InfraLostPnL est fondamental`
- Domain tags: EXECUTION, INFRA, ACCOUNTING
- Source statement: 41. Pourquoi InfraLostPnL est fondamental: PnL actuel = 1 000 €/mois et les opportunités perdues sont estimées à :
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `41. Pourquoi InfraLostPnL est fondamental` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0331`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0155 — 42. Shadow Infrastructure

- Source: `SRC-008`
- Location: lines 4706–4739; heading `42. Shadow Infrastructure`
- Domain tags: INFRA, VALIDATION, EXECUTION, RISK, ACCOUNTING, SURVIVAL, SIZING, ROUTING
- Source statement: 42. Shadow Infrastructure: Pour tester une machine plus chère sans lui confier immédiatement le trading :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `42. Shadow Infrastructure` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INFRA-0078`; supporting items: none found by conservative heading match; domain indexes `INFRA, VALIDATION, EXECUTION, RISK, ACCOUNTING, SURVIVAL, SIZING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0156 — 43. Counterfactual Infra PnL

- Source: `SRC-008`
- Location: lines 4740–4810; heading `43. Counterfactual Infra PnL`
- Domain tags: INFRA, ACCOUNTING, SIMULATOR, VALIDATION, REPLAY, FUTURE
- Source statement: 43. Counterfactual Infra PnL: \Delta GrossPnL = GrossPnL_{candidate} - GrossPnL_{current} Le PnL challenger vient de notre Replay/Counterfactual Simulator.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `43. Counterfactual Infra PnL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INFRA-0079`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, SIMULATOR, VALIDATION, REPLAY, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0157 — 44. Coût incrémental

- Source: `SRC-008`
- Location: lines 4811–4859; heading `44. Coût incrémental`
- Domain tags: ACCOUNTING
- Source statement: 44. Coût incrémental: \Delta Cost = Cost_{candidate} - Cost_{current}
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `44. Coût incrémental` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0064`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0158 — 45. Valeur nette de l’upgrade

- Source: `SRC-008`
- Location: lines 4860–4908; heading `45. Valeur nette de l’upgrade`
- Domain tags: ACCOUNTING
- Source statement: 45. Valeur nette de l’upgrade: NetUpgradeValue = \Delta GrossPnL - \Delta Cost 160 - 60 = +100€/mois
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `45. Valeur nette de l’upgrade` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-ACCT-0065`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0159 — 46. Mais une valeur attendue positive ne suffit pas

- Source: `SRC-008`
- Location: lines 4909–4924; heading `46. Mais une valeur attendue positive ne suffit pas`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 46. Mais une valeur attendue positive ne suffit pas: Expected ΔPnL = 65 € Un mauvais mois et l’infrastructure premium devient moins rentable.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `46. Mais une valeur attendue positive ne suffit pas` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0080`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0160 — 47. Conservative Lower Bound

- Source: `SRC-008`
- Location: lines 4925–4951; heading `47. Conservative Lower Bound`
- Domain tags: ACCOUNTING, REPLAY, PRODUCT
- Source statement: 47. Conservative Lower Bound: On estime une borne basse : par bootstrap, replay, distribution observée ou autre méthode statistique appropriée.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `47. Conservative Lower Bound` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0066`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, REPLAY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0161 — 48. Infrastructure ROI Gate

- Source: `SRC-008`
- Location: lines 4952–5008; heading `48. Infrastructure ROI Gate`
- Domain tags: INFRA, CLIENT, ACCOUNTING
- Source statement: 48. Infrastructure ROI Gate: LCB(\Delta GrossPnL) > SafetyFactor \times \Delta Cost Au début, avec forte incertitude :
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `48. Infrastructure ROI Gate` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INFRA-0081`; supporting items: SRC-004-ITEM-0251; domain indexes `INFRA, CLIENT, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0162 — 49. Incremental Infra ROI

- Source: `SRC-008`
- Location: lines 5009–5051; heading `49. Incremental Infra ROI`
- Domain tags: INFRA, ACCOUNTING, MICROSTRUCTURE
- Source statement: 49. Incremental Infra ROI: InfraROI = \frac{\Delta GrossPnL} {\Delta Cost}
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `49. Incremental Infra ROI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0082`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0163 — 50. PnL net absolu reste le KPI final

- Source: `SRC-008`
- Location: lines 5052–5168; heading `50. PnL net absolu reste le KPI final`
- Domain tags: ACCOUNTING, FORMULA, RISK, INFRA, OPERATIONS
- Source statement: 50. PnL net absolu reste le KPI final: La formule la plus importante reste : NetPnL(server) = TradingPnL_{net\ fees/slippage} - InfrastructureCost - OperationalInfraCost
- Nature: formula/definition
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `50. PnL net absolu reste le KPI final` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0067`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, FORMULA, RISK, INFRA, OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0165 — VPS 40 €

- Source: `SRC-008`
- Location: lines 5170–5177; heading `VPS 40 €`
- Domain tags: INFRA, ACCOUNTING
- Source statement: VPS 40 €: Gross trading PnL = 1 000 €
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `VPS 40 €` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0083`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0166 — Dedicated 500 €

- Source: `SRC-008`
- Location: lines 5178–5198; heading `Dedicated 500 €`
- Domain tags: INFRA, ACCOUNTING
- Source statement: Dedicated 500 €: Gross trading PnL = 1 300 € Le serveur à 500 € est :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Dedicated 500 €` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0084`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0167 — 52. Ce que doit créer un serveur 500 €

- Source: `SRC-008`
- Location: lines 5199–5229; heading `52. Ce que doit créer un serveur 500 €`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 52. Ce que doit créer un serveur 500 €: Current VPS = 65 € Je ne veux pas simplement :
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `52. Ce que doit créer un serveur 500 €` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0085`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0168 — 53. Infrastructure Efficiency

- Source: `SRC-008`
- Location: lines 5230–5272; heading `53. Infrastructure Efficiency`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 53. Infrastructure Efficiency: Ce ratio détecte le surdimensionnement. Une machine peut avoir une efficacité plus faible mais générer plus d’argent net total.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `53. Infrastructure Efficiency` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0086`; supporting items: SRC-004-ITEM-0252; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0169 — 54. Upgrade ET downgrade

- Source: `SRC-008`
- Location: lines 5273–5298; heading `54. Upgrade ET downgrade`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 54. Upgrade ET downgrade: L’Infrastructure ROI Engine doit fonctionner dans les deux directions. Current HFT = 65 €/mois
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `54. Upgrade ET downgrade` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0087`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0170 — 55. Le capital n’est pas directement le trigger d’upgrade

- Source: `SRC-008`
- Location: lines 5299–5356; heading `55. Le capital n’est pas directement le trigger d’upgrade`
- Domain tags: CAPITAL, EXECUTION, INFRA, ACCOUNTING
- Source statement: 55. Le capital n’est pas directement le trigger d’upgrade: Capital = 100 000 € Si la stratégie ne peut exécuter que 500 € par opportunité à cause de la profondeur :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `55. Le capital n’est pas directement le trigger d’upgrade` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CAP-0021`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, EXECUTION, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0171 — 56. Capital Bands : seulement comme résultat empirique

- Source: `SRC-008`
- Location: lines 5357–5385; heading `56. Capital Bands : seulement comme résultat empirique`
- Domain tags: CAPITAL, EXECUTION, INFRA, ACCOUNTING, MARKET_ATLAS
- Source statement: 56. Capital Bands : seulement comme résultat empirique: Après suffisamment de live, on pourra découvrir par exemple : → premium / bare metal
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `56. Capital Bands : seulement comme résultat empirique` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0022`; supporting items: SRC-005-ITEM-0166; domain indexes `CAPITAL, EXECUTION, INFRA, ACCOUNTING, MARKET_ATLAS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0172 — 57. Quand envisager un node Hyperliquid

- Source: `SRC-008`
- Location: lines 5386–5471; heading `57. Quand envisager un node Hyperliquid`
- Domain tags: NODE, INFRA, OPERATIONS, ACCOUNTING
- Source statement: 57. Quand envisager un node Hyperliquid: « les données sont plus rapides ». PnL perdu à cause de la qualité/cadence du PublicFeed
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `57. Quand envisager un node Hyperliquid` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-NODE-0003`; supporting items: SRC-002-ITEM-0139; domain indexes `NODE, INFRA, OPERATIONS, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0173 — 58. Architecture logicielle : aucun code provider-specific

- Source: `SRC-008`
- Location: lines 5472–5492; heading `58. Architecture logicielle : aucun code provider-specific`
- Domain tags: INFRA, ARCH, EXECUTION, RECORDER, CLOCK, DEPLOYMENT, ACCOUNTING
- Source statement: 58. Architecture logicielle : aucun code provider-specific: Le moteur ne doit jamais connaître : Il connaît uniquement des interfaces.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `58. Architecture logicielle : aucun code provider-specific` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0088`; supporting items: none found by conservative heading match; domain indexes `INFRA, ARCH, EXECUTION, RECORDER, CLOCK, DEPLOYMENT, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0174 — 59. Modules Rust infrastructure

- Source: `SRC-008`
- Location: lines 5493–5517; heading `59. Modules Rust infrastructure`
- Domain tags: INFRA, ARCH, CLOCK, BENCHMARK, OPERATIONS, ACCOUNTING
- Source statement: 59. Modules Rust infrastructure: Organisation possible : src/
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `59. Modules Rust infrastructure` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0089`; supporting items: SRC-004-ITEM-0108; domain indexes `INFRA, ARCH, CLOCK, BENCHMARK, OPERATIONS, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0175 — 60. Instrumentation du hot path

- Source: `SRC-008`
- Location: lines 5518–5557; heading `60. Instrumentation du hot path`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, RISK, CLOCK
- Source statement: 60. Instrumentation du hot path: On doit timestamp chaque étape : Mais l’enregistrement des metrics reste asynchrone.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `60. Instrumentation du hot path` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ROUTE-0038`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, RISK, CLOCK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0176 — 61. Structure LatencyTrace

- Source: `SRC-008`
- Location: lines 5558–5587; heading `61. Structure LatencyTrace`
- Domain tags: INFRA, EXECUTION, RISK, DATA, ROUTING
- Source statement: 61. Structure LatencyTrace: Conceptuellement : LatencyTrace {
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `61. Structure LatencyTrace` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0090`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, RISK, DATA, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0177 — 62. InfraSnapshot

- Source: `SRC-008`
- Location: lines 5588–5614; heading `62. InfraSnapshot`
- Domain tags: INFRA, RECORDER, CLOCK, BENCHMARK, MICROSTRUCTURE
- Source statement: 62. InfraSnapshot: Toutes les quelques secondes : Ça permet de répondre :
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `62. InfraSnapshot` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0091`; supporting items: none found by conservative heading match; domain indexes `INFRA, RECORDER, CLOCK, BENCHMARK, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0178 — 63. Attribution des pertes infra

- Source: `SRC-008`
- Location: lines 5615–5690; heading `63. Attribution des pertes infra`
- Domain tags: INFRA, EXECUTION, ACCOUNTING
- Source statement: 63. Attribution des pertes infra: Pour chaque opportunité ratée : InfraLostPnL = Loss_{feed} + Loss_{compute} + Loss_{sign} + Loss_{network}
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `63. Attribution des pertes infra` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0092`; supporting items: none found by conservative heading match; domain indexes `INFRA, EXECUTION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0179 — 64. Il faut éviter le double comptage

- Source: `SRC-008`
- Location: lines 5691–5726; heading `64. Il faut éviter le double comptage`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: 64. Il faut éviter le double comptage: Si une opportunité disparaît pendant : on ne doit pas ensuite lui ajouter :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `64. Il faut éviter le double comptage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0332`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0180 — 65. Benchmark data versioning

- Source: `SRC-008`
- Location: lines 5727–5768; heading `65. Benchmark data versioning`
- Domain tags: BENCHMARK, CLOCK, DETERMINISM, INFRA, DEPLOYMENT, PRODUCT, FUTURE
- Source statement: 65. Benchmark data versioning: Chaque benchmark doit être reproductible. On ne compare jamais :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `65. Benchmark data versioning` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-BENCH-0018`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, CLOCK, DETERMINISM, INFRA, DEPLOYMENT, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0181 — 66. Benchmark sans tuning d’abord

- Source: `SRC-008`
- Location: lines 5769–5798; heading `66. Benchmark sans tuning d’abord`
- Domain tags: BENCHMARK, INFRA, DEPLOYMENT
- Source statement: 66. Benchmark sans tuning d’abord: Puis les deux finalistes reçoivent :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `66. Benchmark sans tuning d’abord` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-BENCH-0019`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, INFRA, DEPLOYMENT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0182 — 67. Pas de DPDK/kernel bypass au départ

- Source: `SRC-008`
- Location: lines 5799–5823; heading `67. Pas de DPDK/kernel bypass au départ`
- Domain tags: MICROSTRUCTURE
- Source statement: 67. Pas de DPDK/kernel bypass au départ: Gagner quelques microsecondes via : peut n’avoir pratiquement aucune valeur économique.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `67. Pas de DPDK/kernel bypass au départ` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0029`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0183 — 68. Même règle pour SolarFlare

- Source: `SRC-008`
- Location: lines 5824–5833; heading `68. Même règle pour SolarFlare`
- Domain tags: EXECUTION, INFRA, BENCHMARK
- Source statement: 68. Même règle pour SolarFlare: TradingFX HFT annonce SolarFlare 10GbE. Cela devient intéressant uniquement si :
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `68. Même règle pour SolarFlare` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0333`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0184 — 69. Déploiement de notre bot personnel

- Source: `SRC-008`
- Location: lines 5834–5859; heading `69. Déploiement de notre bot personnel`
- Domain tags: EXECUTION, RECORDER, INFRA, DEPLOYMENT, OPERATIONS, ACCOUNTING
- Source statement: 69. Déploiement de notre bot personnel: Départ : ONE VPS TOKYO
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `69. Déploiement de notre bot personnel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0334`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, DEPLOYMENT, OPERATIONS, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0185 — 70. Déploiement pour les clients

- Source: `SRC-008`
- Location: lines 5860–5891; heading `70. Déploiement pour les clients`
- Domain tags: CLIENT, EXECUTION, INFRA, DEPLOYMENT, INVENTORY, PRODUCT
- Source statement: 70. Déploiement pour les clients: Notre modèle commercial prévu n’est pas un SaaS. Chaque client dispose de :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `70. Déploiement pour les clients` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CLIENT-0025`; supporting items: none found by conservative heading match; domain indexes `CLIENT, EXECUTION, INFRA, DEPLOYMENT, INVENTORY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0186 — 71. Docker comme contrat de déploiement

- Source: `SRC-008`
- Location: lines 5892–5908; heading `71. Docker comme contrat de déploiement`
- Domain tags: DEPLOYMENT, RISK, LICENSE, PRODUCT, FUTURE
- Source statement: 71. Docker comme contrat de déploiement: Notre référence devrait être : Les détails de licence/distribution seront définis plus tard.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `71. Docker comme contrat de déploiement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-DEPLOY-0218`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, LICENSE, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0187 — 72. Configuration client

- Source: `SRC-008`
- Location: lines 5909–5932; heading `72. Configuration client`
- Domain tags: CLIENT, RISK, DEPLOYMENT, SECURITY, ACCOUNTING
- Source statement: 72. Configuration client: Montée dans le container : mais pas une clé privée en clair dans une image Docker.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `72. Configuration client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CLIENT-0026`; supporting items: none found by conservative heading match; domain indexes `CLIENT, RISK, DEPLOYMENT, SECURITY, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0188 — 73. API wallet par processus

- Source: `SRC-008`
- Location: lines 5933–5947; heading `73. API wallet par processus`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 73. API wallet par processus: un API wallet par processus de trading. L’image Docker ne contient évidemment aucune clé client.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `73. API wallet par processus` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-DEPLOY-0219`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0189 — 74. Secrets

- Source: `SRC-008`
- Location: lines 5948–5965; heading `74. Secrets`
- Domain tags: SECURITY, EXECUTION, DEPLOYMENT
- Source statement: 74. Secrets: Les clés ne doivent jamais être : Elles sont fournies au runtime via :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `74. Secrets` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SEC-0021`; supporting items: none found by conservative heading match; domain indexes `SECURITY, EXECUTION, DEPLOYMENT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0190 — 75. Pas de service externe dans le hot path

- Source: `SRC-008`
- Location: lines 5966–5989; heading `75. Pas de service externe dans le hot path`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, RECOVERY, RISK, DEPLOYMENT, LICENSE
- Source statement: 75. Pas de service externe dans le hot path: Si nous avons plus tard : ils ne doivent jamais intervenir dans :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `75. Pas de service externe dans le hot path` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ROUTE-0039`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, RECOVERY, RISK, DEPLOYMENT, LICENSE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0191 — 76. Les clients ne doivent PAS avoir besoin d’un node

- Source: `SRC-008`
- Location: lines 5990–6011; heading `76. Les clients ne doivent PAS avoir besoin d’un node`
- Domain tags: CLIENT, DEPLOYMENT, ACCOUNTING, CAPITAL, ARCH
- Source statement: 76. Les clients ne doivent PAS avoir besoin d’un node: Notre Docker de référence doit fonctionner avec : Le node devient une option :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `76. Les clients ne doivent PAS avoir besoin d’un node` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0027`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, ACCOUNTING, CAPITAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0192 — 77. Profils matériels clients

- Source: `SRC-008`
- Location: lines 6012–6013; heading `77. Profils matériels clients`
- Domain tags: CLIENT, MICROSTRUCTURE, BENCHMARK
- Source statement: 77. Profils matériels clients: Après nos benchmarks, on pourra publier trois niveaux.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `77. Profils matériels clients` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CLIENT-0028`; supporting items: none found by conservative heading match; domain indexes `CLIENT, MICROSTRUCTURE, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0193 — Minimum validé

- Source: `SRC-008`
- Location: lines 6014–6021; heading `Minimum validé`
- Domain tags: INFRA
- Source statement: Minimum validé: Exemple futur : 2 vCPU
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Minimum validé` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INFRA-0093`; supporting items: none found by conservative heading match; domain indexes `INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0194 — Recommended

- Source: `SRC-008`
- Location: lines 6022–6028; heading `Recommended`
- Domain tags: INFRA
- Source statement: Recommended: 2 dedicated/reserved vCPU 4–8 GB
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Recommended` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0094`; supporting items: none found by conservative heading match; domain indexes `INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0195 — Performance

- Source: `SRC-008`
- Location: lines 6029–6037; heading `Performance`
- Domain tags: BENCHMARK, INFRA
- Source statement: Performance: Mais les valeurs finales viendront de nos mesures.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0020`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0196 — 78. Le produit doit faire son propre diagnostic infra

- Source: `SRC-008`
- Location: lines 6038–6061; heading `78. Le produit doit faire son propre diagnostic infra`
- Domain tags: INFRA, RISK, CLOCK, DEPLOYMENT, MICROSTRUCTURE
- Source statement: 78. Le produit doit faire son propre diagnostic infra: Au démarrage, le Docker mesure : Le bot ne devine pas que tous les VPS sont équivalents.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `78. Le produit doit faire son propre diagnostic infra` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0095`; supporting items: none found by conservative heading match; domain indexes `INFRA, RISK, CLOCK, DEPLOYMENT, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0197 — 79. Monitoring production

- Source: `SRC-008`
- Location: lines 6062–6094; heading `79. Monitoring production`
- Domain tags: OPERATIONS, PRODUCT, EXECUTION, RECORDER, CLOCK, INFRA, BENCHMARK, ACCOUNTING
- Source statement: 79. Monitoring production: KPI machine : feed age
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `79. Monitoring production` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OPS-0019`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, PRODUCT, EXECUTION, RECORDER, CLOCK, INFRA, BENCHMARK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0198 — 80. Alertes importantes

- Source: `SRC-008`
- Location: lines 6095–6113; heading `80. Alertes importantes`
- Domain tags: OPERATIONS, RISK, RECORDER, CLOCK, INFRA, BENCHMARK, ACCOUNTING
- Source statement: 80. Alertes importantes: Ces signaux peuvent éventuellement mettre : si la qualité de l’infrastructure devient incompatible avec nos Risk Gates.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `80. Alertes importantes` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-OPS-0020`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, RISK, RECORDER, CLOCK, INFRA, BENCHMARK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0199 — 81. La performance infra doit entrer dans le Risk Engine

- Source: `SRC-008`
- Location: lines 6114–6139; heading `81. La performance infra doit entrer dans le Risk Engine`
- Domain tags: RISK, INFRA, BENCHMARK, OPERATIONS, ACCOUNTING, ROUTING
- Source statement: 81. La performance infra doit entrer dans le Risk Engine: la même route peut devenir : Donc l’infra n’est pas seulement du monitoring externe.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `81. La performance infra doit entrer dans le Risk Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0329`; supporting items: SRC-006-ITEM-0382, SRC-006-ITEM-0390; domain indexes `RISK, INFRA, BENCHMARK, OPERATIONS, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0200 — 82. Rolling Infra Model

- Source: `SRC-008`
- Location: lines 6140–6166; heading `82. Rolling Infra Model`
- Domain tags: INFRA, RISK, BENCHMARK
- Source statement: 82. Rolling Infra Model: On conserve plusieurs horizons : network P99 30d = excellent
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `82. Rolling Infra Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0096`; supporting items: none found by conservative heading match; domain indexes `INFRA, RISK, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0201 — 83. Décision d’upgrade : pipeline complet

- Source: `SRC-008`
- Location: lines 6167–6200; heading `83. Décision d’upgrade : pipeline complet`
- Domain tags: EXECUTION, RISK, INFRA, BENCHMARK, VALIDATION, ACCOUNTING
- Source statement: 83. Décision d’upgrade : pipeline complet: Current infrastructure Measure InfraLostPnL
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `83. Décision d’upgrade : pipeline complet` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0335`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, BENCHMARK, VALIDATION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0202 — 84. Conditions finales d’upgrade

- Source: `SRC-008`
- Location: lines 6201–6224; heading `84. Conditions finales d’upgrade`
- Domain tags: RISK, VALIDATION, ACCOUNTING
- Source statement: 84. Conditions finales d’upgrade: On upgrade seulement si : 3. gain économique attribuable à cette amélioration
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `84. Conditions finales d’upgrade` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0330`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0203 — 85. Condition de downgrade

- Source: `SRC-008`
- Location: lines 6225–6241; heading `85. Condition de downgrade`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 85. Condition de downgrade: On ne garde jamais une infrastructure premium simplement parce qu’on l’a déjà achetée. Les coûts passés sont sunk costs.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `85. Condition de downgrade` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0097`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0204 — 86. Rapport automatique mensuel

- Source: `SRC-008`
- Location: lines 6242–6288; heading `86. Rapport automatique mensuel`
- Domain tags: EXECUTION, INFRA, VALIDATION, ACCOUNTING
- Source statement: 86. Rapport automatique mensuel: Ce rapport doit être générable automatiquement.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `86. Rapport automatique mensuel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0336`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, VALIDATION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0205 — 87. Exemple inverse

- Source: `SRC-008`
- Location: lines 6289–6321; heading `87. Exemple inverse`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 87. Exemple inverse: Current: Premium VDS
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `87. Exemple inverse` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0098`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0206 — 88. Relation avec notre Replay Engine

- Source: `SRC-008`
- Location: lines 6322–6361; heading `88. Relation avec notre Replay Engine`
- Domain tags: REPLAY, EXECUTION, INFRA, ACCOUNTING, SIMULATOR, SURVIVAL, QUANT, PRODUCT
- Source statement: 88. Relation avec notre Replay Engine: La partie infrastructure doit utiliser le Counterfactual Simulator étudié en partie 3. Donc le serveur challenger ne gagne pas simplement parce qu’il est :
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `88. Relation avec notre Replay Engine` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-REPLAY-0020`; supporting items: SRC-006-ITEM-0409; domain indexes `REPLAY, EXECUTION, INFRA, ACCOUNTING, SIMULATOR, SURVIVAL, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0207 — 89. Relation avec le sizing

- Source: `SRC-008`
- Location: lines 6362–6393; heading `89. Relation avec le sizing`
- Domain tags: SIZING, INFRA, CAPITAL, ROUTING
- Source statement: 89. Relation avec le sizing: Un meilleur serveur peut également augmenter notre : Si cela permet réellement d’engager plus de capital sans augmenter excessivement le risque :
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `89. Relation avec le sizing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIZE-0006`; supporting items: none found by conservative heading match; domain indexes `SIZING, INFRA, CAPITAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0208 — 90. Relation avec maker/taker

- Source: `SRC-008`
- Location: lines 6394–6395; heading `90. Relation avec maker/taker`
- Domain tags: EXECUTION, INFRA
- Source statement: 90. Relation avec maker/taker: L’infrastructure peut avoir des effets différents.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `90. Relation avec maker/taker` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0337`; supporting items: SRC-004-ITEM-0057; domain indexes `EXECUTION, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0209 — TT / TTT

- Source: `SRC-008`
- Location: lines 6396–6403; heading `TT / TTT`
- Domain tags: TRIANGLE, EXECUTION, INFRA, ACCOUNTING
- Source statement: TT / TTT: Très sensibles à : feed delay
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `TT / TTT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-TRI-0004`; supporting items: none found by conservative heading match; domain indexes `TRIANGLE, EXECUTION, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0210 — MT / MTT

- Source: `SRC-008`
- Location: lines 6404–6421; heading `MT / MTT`
- Domain tags: TRIANGLE, EXECUTION, INFRA, BENCHMARK, ACCOUNTING, MICROSTRUCTURE, MAKER_MODEL
- Source statement: MT / MTT: Notre benchmark économique doit donc segmenter : pour comprendre où une meilleure infrastructure apporte réellement de la valeur.
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `MT / MTT` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-TRI-0005`; supporting items: none found by conservative heading match; domain indexes `TRIANGLE, EXECUTION, INFRA, BENCHMARK, ACCOUNTING, MICROSTRUCTURE, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0211 — 91. Rate limits

- Source: `SRC-008`
- Location: lines 6422–6438; heading `91. Rate limits`
- Domain tags: RISK, DEPLOYMENT, CLIENT
- Source statement: 91. Rate limits: Hyperliquid applique actuellement notamment : maximum 30 new WS connections/min
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `91. Rate limits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RISK-0331`; supporting items: SRC-001-ITEM-0006; domain indexes `RISK, DEPLOYMENT, CLIENT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0212 — 92. Dead Man’s Switch

- Source: `SRC-008`
- Location: lines 6439–6453; heading `92. Dead Man’s Switch`
- Domain tags: EXECUTION, INFRA
- Source statement: 92. Dead Man’s Switch: Hyperliquid possède également scheduleCancel, permettant de programmer un cancel-all futur. Ce mécanisme pourra être utilisé pour nos ordres maker.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `92. Dead Man’s Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0338`; supporting items: SRC-004-ITEM-0088; domain indexes `EXECUTION, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0213 — 93. Restart sécurisé

- Source: `SRC-008`
- Location: lines 6454–6499; heading `93. Restart sécurisé`
- Domain tags: OPERATIONS, EXECUTION, RECOVERY, RECONCILIATION, RISK, CLOCK, DEPLOYMENT, ACCOUNTING
- Source statement: 93. Restart sécurisé: Un container qui redémarre ne passe jamais immédiatement en READY.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `93. Restart sécurisé` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-OPS-0021`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, EXECUTION, RECOVERY, RECONCILIATION, RISK, CLOCK, DEPLOYMENT, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0214 — 94. Infrastructure de backup

- Source: `SRC-008`
- Location: lines 6500–6545; heading `94. Infrastructure de backup`
- Domain tags: INFRA, OPERATIONS, ACCOUNTING
- Source statement: 94. Infrastructure de backup: On n’achète pas nécessairement un deuxième VPS dès le début. Le backup devient justifié lorsque :
- Nature: rationale
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `94. Infrastructure de backup` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0099`; supporting items: none found by conservative heading match; domain indexes `INFRA, OPERATIONS, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0215 — 95. Expected Downtime Loss

- Source: `SRC-008`
- Location: lines 6546–6628; heading `95. Expected Downtime Loss`
- Domain tags: OPERATIONS, ACCOUNTING, QUANT
- Source statement: 95. Expected Downtime Loss: ExpectedDowntimeLoss = DowntimeHours \times ExpectedPnLPerHour ajusté par la probabilité de panne.
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `95. Expected Downtime Loss` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-OPS-0022`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0216 — 96. Le backup peut également commencer cheap

- Source: `SRC-008`
- Location: lines 6629–6645; heading `96. Le backup peut également commencer cheap`
- Domain tags: OPERATIONS, INFRA, DEPLOYMENT, HOT_WARM_COLD
- Source statement: 96. Le backup peut également commencer cheap: Avant un vrai hot standby : permettant de recréer rapidement une machine.
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `96. Le backup peut également commencer cheap` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OPS-0023`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, INFRA, DEPLOYMENT, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0217 — 97. Budget benchmark

- Source: `SRC-008`
- Location: lines 6646–6660; heading `97. Budget benchmark`
- Domain tags: BENCHMARK, INFRA
- Source statement: 97. Budget benchmark: pour tester plusieurs fournisseurs est parfaitement rationnel. des centaines d’euros par mois
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `97. Budget benchmark` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0021`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0219 — Wave 1

- Source: `SRC-008`
- Location: lines 6662–6671; heading `Wave 1`
- Domain tags: INFRA
- Source statement: Wave 1: TradingFX Advanced TradingFX Standard HFT
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Wave 1` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0100`; supporting items: none found by conservative heading match; domain indexes `INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0220 — Wave 2 seulement si nécessaire

- Source: `SRC-008`
- Location: lines 6672–6680; heading `Wave 2 seulement si nécessaire`
- Domain tags: INFRA, BENCHMARK
- Source statement: Wave 2 seulement si nécessaire: Cherry Performance VDS Vultr
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Wave 2 seulement si nécessaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0101`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0221 — Beaucoup plus tard

- Source: `SRC-008`
- Location: lines 6681–6689; heading `Beaucoup plus tard`
- Domain tags: FUTURE
- Source statement: Beaucoup plus tard: Semi-dedicated Bare metal
- Nature: decision/policy/concept
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `Beaucoup plus tard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0013`; supporting items: none found by conservative heading match; domain indexes `FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0222 — 99. Ce qu’on ne fait PAS

- Source: `SRC-008`
- Location: lines 6690–6725; heading `99. Ce qu’on ne fait PAS`
- Domain tags: DEPLOYMENT, CLIENT, CAPITAL, ROUTING, HOT_WARM_COLD, PRODUCT, ARCH
- Source statement: 99. Ce qu’on ne fait PAS: On n’achète pas une machine parce que : On n’upgrade pas parce que :
- Nature: rejected approach
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `99. Ce qu’on ne fait PAS` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-DEPLOY-0220`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT, CAPITAL, ROUTING, HOT_WARM_COLD, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0223 — 100. Ce que l’on GARDE définitivement

- Source: `SRC-008`
- Location: lines 6726–6779; heading `100. Ce que l’on GARDE définitivement`
- Domain tags: EXECUTION, RECORDER, INFRA, BENCHMARK, DEPLOYMENT, CLIENT, ACCOUNTING, SIMULATOR
- Source statement: 100. Ce que l’on GARDE définitivement: Upgrade + downgrade ROI gate one isolated Docker per client
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `100. Ce que l’on GARDE définitivement` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0339`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, BENCHMARK, DEPLOYMENT, CLIENT, ACCOUNTING, SIMULATOR`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-008-ITEM-0224 — 101. Principe final de toute la partie 1

- Source: `SRC-008`
- Location: lines 6780–6879; heading `101. Principe final de toute la partie 1`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 101. Principe final de toute la partie 1: L’infrastructure n’est pas un prestige technique. EconomicValue_{infra} = PnL_{enabled} - Cost_{infra}
- Nature: data/architecture contract
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `101. Principe final de toute la partie 1` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0102`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-008-ITEM-0225 — 102. Direction finale pour notre démarrage

- Source: `SRC-008`
- Location: lines 6880–6937; heading `102. Direction finale pour notre démarrage`
- Domain tags: EXECUTION, RECORDER, INFRA, BENCHMARK, DEPLOYMENT, CLIENT, VALIDATION, ACCOUNTING
- Source statement: 102. Direction finale pour notre démarrage: Aujourd’hui, la direction rationnelle est : → upgrade only if profitable
- Nature: protocol/validation
- Temporal interpretation: advanced correction/refinement
- Authority: Advanced correction for simulator and deep infrastructure; closure dossiers prevail for final contracts.
- Candidate canonical interpretation: Preserve `102. Direction finale pour notre démarrage` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0340`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, BENCHMARK, DEPLOYMENT, CLIENT, VALIDATION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 218
- Requirements contributed: 218
- Supporting references contributed: 53 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 0
- Research items: 118
- Open items: 1
- External revalidation items: 48
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
