# SRC-007 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-007`
- Filename: `Oui, dans le modèle qu’on vient de définir, le plus propre est que….md`
- SHA-256: `df2e94843df1e4a28bec4699bf89c9d2f2b8faa91763b3d3e78bff05e8369490`
- Line count: 12371
- Authority profile: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Main domains: QUANT, EXECUTION, RISK, ACCOUNTING, SURVIVAL, PARTICIPANTS, ROUTING, MICROSTRUCTURE, ARCH, PRODUCT, INFRA, INVENTORY
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-007-ITEM-0001 — Source preamble

- Source: `SRC-007`
- Location: lines 1–16; heading `Source preamble`
- Domain tags: INFRA, DEPLOYMENT, CLIENT, CAPITAL
- Source statement: Source preamble: Oui, dans le modèle qu’on vient de définir, le plus propre est que chaque client ait sa propre machine, généralement son propre VPS Tokyo. Ce n’est pas nécessairement « un VPS acheté chez toi ». Le client peut utiliser :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Source preamble` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0035`; supporting items: SRC-003-ITEM-0001, SRC-008-ITEM-0001; domain indexes `INFRA, DEPLOYMENT, CLIENT, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0002 — Pourquoi c’est probablement le meilleur modèle

- Source: `SRC-007`
- Location: lines 17–28; heading `Pourquoi c’est probablement le meilleur modèle`
- Domain tags: QUANT, EXECUTION, RISK, RECORDER, INFRA, CLIENT, CAPITAL
- Source statement: Pourquoi c’est probablement le meilleur modèle: Ça nous donne une isolation presque parfaite : * ses clés restent chez lui ;
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Pourquoi c’est probablement le meilleur modèle` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0006`; supporting items: none found by conservative heading match; domain indexes `QUANT, EXECUTION, RISK, RECORDER, INFRA, CLIENT, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0003 — Le VPS n’est cependant pas techniquement obligatoire

- Source: `SRC-007`
- Location: lines 29–57; heading `Le VPS n’est cependant pas techniquement obligatoire`
- Domain tags: INFRA, BENCHMARK, DEPLOYMENT, MICROSTRUCTURE, CAPITAL, QUANT, RESEARCH
- Source statement: Le VPS n’est cependant pas techniquement obligatoire: Notre Docker pourrait fonctionner sur : Mais pour exploiter sérieusement la stratégie, on pourrait recommander :
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Le VPS n’est cependant pas techniquement obligatoire` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0036`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, DEPLOYMENT, MICROSTRUCTURE, CAPITAL, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0004 — Et chaque client ne doit pas forcément prendre le même VPS

- Source: `SRC-007`
- Location: lines 58–103; heading `Et chaque client ne doit pas forcément prendre le même VPS`
- Domain tags: INFRA, CLIENT, EXECUTION, BENCHMARK, ACCOUNTING, SURVIVAL, MICROSTRUCTURE, CAPITAL
- Source statement: Et chaque client ne doit pas forcément prendre le même VPS: C'est là que notre benchmark sera utile. Après calibration, on pourrait publier quelque chose du genre :
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Et chaque client ne doit pas forcément prendre le même VPS` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0037`; supporting items: none found by conservative heading match; domain indexes `INFRA, CLIENT, EXECUTION, BENCHMARK, ACCOUNTING, SURVIVAL, MICROSTRUCTURE, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0005 — Ça pourrait même devenir une fonctionnalité du Docker

- Source: `SRC-007`
- Location: lines 104–150; heading `Ça pourrait même devenir une fonctionnalité du Docker`
- Domain tags: DEPLOYMENT, EXECUTION, INFRA, BENCHMARK, CLIENT, ACCOUNTING
- Source statement: Ça pourrait même devenir une fonctionnalité du Docker: Je trouve cette approche particulièrement intéressante. Le client installe notre image.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Ça pourrait même devenir une fonctionnalité du Docker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-DEPLOY-0216`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, INFRA, BENCHMARK, CLIENT, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0006 — Commercialement

- Source: `SRC-007`
- Location: lines 151–325; heading `Commercialement`
- Domain tags: PRODUCT, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, CLOCK, INFRA
- Source statement: Commercialement: Ton modèle devient assez simple : paie son propre VPS (~30–50 €/mois au départ)
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Commercialement` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-PRODUCT-0015`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, CLOCK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0009 — 1. Objectif réel de cette partie

- Source: `SRC-007`
- Location: lines 328–390; heading `1. Objectif réel de cette partie`
- Domain tags: EXECUTION, RECOVERY, ACCOUNTING, PARTICIPANTS, TRIANGLE, QUANT
- Source statement: 1. Objectif réel de cette partie: Le Market Participants Model ne doit pas chercher à reconstruire psychologiquement chaque trader. Nous n’avons pas besoin de savoir :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `1. Objectif réel de cette partie` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0240`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, ACCOUNTING, PARTICIPANTS, TRIANGLE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0010 — 2. Principe fondamental

- Source: `SRC-007`
- Location: lines 391–420; heading `2. Principe fondamental`
- Domain tags: EXECUTION, RISK, VALIDATION, PRODUCT, FUTURE, RESEARCH
- Source statement: 2. Principe fondamental: Notre modèle doit être construit dans cet ordre : espérer qu'elle ressemble au marché
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `2. Principe fondamental` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0241`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, VALIDATION, PRODUCT, FUTURE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0011 — 3. Pourquoi cette brique est particulièrement importante pour l’arbitrage

- Source: `SRC-007`
- Location: lines 421–470; heading `3. Pourquoi cette brique est particulièrement importante pour l’arbitrage`
- Domain tags: EXECUTION, RECOVERY, ACCOUNTING, PARTICIPANTS, MICROSTRUCTURE, OWA, ARCH
- Source statement: 3. Pourquoi cette brique est particulièrement importante pour l’arbitrage: Un edge d’arbitrage est généralement temporaire. Le récent travail 2026 sur le One-Way Arbitrage identifie des centaines de millions de séquences sur Binance et observe notamment que ces séquences sont devenues plus rapides avec le temps tandis que leur profit unitaire a diminué. C’est exactement le comportement attendu lorsque davantage d’agents se disputent les mêmes anomalies.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `3. Pourquoi cette brique est particulièrement importante pour l’arbitrage` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0242`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, ACCOUNTING, PARTICIPANTS, MICROSTRUCTURE, OWA, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0012 — 4. Nouvelle brique centrale : Edge Survival Engine

- Source: `SRC-007`
- Location: lines 471–508; heading `4. Nouvelle brique centrale : Edge Survival Engine`
- Domain tags: SURVIVAL, RISK, SIMULATOR, PARTICIPANTS, ROUTING, ARCH
- Source statement: 4. Nouvelle brique centrale : Edge Survival Engine: Competition / Edge Survival Engine Il devient une brique majeure entre :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `4. Nouvelle brique centrale : Edge Survival Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0001`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, RISK, SIMULATOR, PARTICIPANTS, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0013 — 5. Définition mathématique de la vie d’une opportunité

- Source: `SRC-007`
- Location: lines 509–582; heading `5. Définition mathématique de la vie d’une opportunité`
- Domain tags: EXECUTION, RISK, ACCOUNTING, ROUTING
- Source statement: 5. Définition mathématique de la vie d’une opportunité: représente son edge net exécutable. Une opportunité naît lorsque :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `5. Définition mathématique de la vie d’une opportunité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0243`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0014 — 6. Variable de survie

- Source: `SRC-007`
- Location: lines 583–629; heading `6. Variable de survie`
- Domain tags: ACCOUNTING, SURVIVAL, ROUTING
- Source statement: 6. Variable de survie: temps restant avant disparition de l’opportunit T_r = \text{temps restant avant disparition de l'opportunité}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `6. Variable de survie` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0049`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, SURVIVAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0015 — 7. Limite actuelle du feed public Hyperliquid

- Source: `SRC-007`
- Location: lines 630–659; heading `7. Limite actuelle du feed public Hyperliquid`
- Domain tags: RISK, ACCOUNTING, EXECUTION, MICROSTRUCTURE, ROUTING
- Source statement: 7. Limite actuelle du feed public Hyperliquid: Le l2Book public Hyperliquid est actuellement documenté comme un snapshot poussé par bloc, lorsqu’au moins environ 0,5 seconde s’est écoulée depuis le push précédent. Le flux trades, lui, est également disponible séparément. nous ne connaissons pas précisément chaque :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `7. Limite actuelle du feed public Hyperliquid` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RISK-0299`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, EXECUTION, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0016 — 8. Le node changera énormément cette partie plus tard

- Source: `SRC-007`
- Location: lines 660–688; heading `8. Le node changera énormément cette partie plus tard`
- Domain tags: FUTURE, EXECUTION, NODE, PARTICIPANTS, ARCH
- Source statement: 8. Le node changera énormément cette partie plus tard: Hyperliquid indique aujourd’hui qu’un non-validator node peut produire notamment : et qu’il peut également calculer des snapshots L4 complets. Hyperliquid recommande explicitement de reconstruire localement l’état du marché pour les applications sensibles à la latence, car les sorties du node sont plus rapides et granulaires que l’API.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `8. Le node changera énormément cette partie plus tard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-FUTURE-0005`; supporting items: none found by conservative heading match; domain indexes `FUTURE, EXECUTION, NODE, PARTICIPANTS, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0017 — 9. La Hazard Function

- Source: `SRC-007`
- Location: lines 689–739; heading `9. La Hazard Function`
- Domain tags: SURVIVAL, QUANT, ARCH
- Source statement: 9. La Hazard Function: En plus de la survival function : la probabilité instantanée que l’opportunité disparaisse maintenant, sachant qu’elle était encore vivante juste avant.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `9. La Hazard Function` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0002`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0018 — 10. Pourquoi le hazard est parfait pour les arbitrageurs concurrents

- Source: `SRC-007`
- Location: lines 740–792; heading `10. Pourquoi le hazard est parfait pour les arbitrageurs concurrents`
- Domain tags: SURVIVAL, FORMULA, EXECUTION, PARTICIPANTS, ARCH
- Source statement: 10. Pourquoi le hazard est parfait pour les arbitrageurs concurrents: Supposons que plusieurs bots puissent corriger une anomalie. Nous n’avons pas besoin de savoir :
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `10. Pourquoi le hazard est parfait pour les arbitrageurs concurrents` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0003`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, FORMULA, EXECUTION, PARTICIPANTS, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0019 — 11. Lien direct avec la PARTIE 1 sur les VPS

- Source: `SRC-007`
- Location: lines 793–914; heading `11. Lien direct avec la PARTIE 1 sur les VPS`
- Domain tags: INFRA, EXECUTION, ACCOUNTING, PARTICIPANTS, SURVIVAL, PRODUCT
- Source statement: 11. Lien direct avec la PARTIE 1 sur les VPS: Nous pouvons maintenant relier mathématiquement les autres bots à notre Infrastructure ROI. La valeur économique de B vient donc de :
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `11. Lien direct avec la PARTIE 1 sur les VPS` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0038`; supporting items: SRC-002-ITEM-0154; domain indexes `INFRA, EXECUTION, ACCOUNTING, PARTICIPANTS, SURVIVAL, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0020 — 12. Ne pas confondre disparition de l’edge et concurrence

- Source: `SRC-007`
- Location: lines 915–935; heading `12. Ne pas confondre disparition de l’edge et concurrence`
- Domain tags: EXECUTION, RISK, DEPLOYMENT, ROUTING, RESEARCH
- Source statement: 12. Ne pas confondre disparition de l’edge et concurrence: Une opportunité peut mourir parce que : market maker retire sa liquidité
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `12. Ne pas confondre disparition de l’edge et concurrence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0244`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, DEPLOYMENT, ROUTING, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0021 — 13. Cause-Specific Hazard

- Source: `SRC-007`
- Location: lines 936–969; heading `13. Cause-Specific Hazard`
- Domain tags: SURVIVAL, EXECUTION, CROSS_MARKET, ROUTING, QUANT, FUTURE
- Source statement: 13. Cause-Specific Hazard: \lambda_{\text{total}} = \lambda_{\text{trade consume}} + \lambda_{\text{cancel}} + \lambda_{\text{repricing}} + \lambda_{\text{cross-market}} + \lambda_{\text{other}} Route death probability next horizon
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `13. Cause-Specific Hazard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-SURV-0004`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, EXECUTION, CROSS_MARKET, ROUTING, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0022 — 14. Edge Half-Life

- Source: `SRC-007`
- Location: lines 970–1013; heading `14. Edge Half-Life`
- Domain tags: SURVIVAL, QUANT
- Source statement: 14. Edge Half-Life: Une métrique très intuitive : t_{50} = \min \{t : S(t)\leq0.5\}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `14. Edge Half-Life` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0005`; supporting items: SRC-004-ITEM-0207; domain indexes `SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0023 — 15. Les features du modèle de survie

- Source: `SRC-007`
- Location: lines 1014–1056; heading `15. Les features du modèle de survie`
- Domain tags: EXECUTION, ACCOUNTING, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, INVENTORY, ROUTING
- Source statement: 15. Les features du modèle de survie: doit intégrer principalement des variables microstructurelles. edge derivative / decay velocity
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `15. Les features du modèle de survie` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0245`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0024 — 16. Order Flow Imbalance

- Source: `SRC-007`
- Location: lines 1057–1083; heading `16. Order Flow Imbalance`
- Domain tags: EXECUTION, MICROSTRUCTURE, INVENTORY, RISK
- Source statement: 16. Order Flow Imbalance: Un élément important vient de Cont, Kukanov et Stoikov. Ils montrent que, sur de courtes périodes, les mouvements de prix sont fortement associés à l’Order Flow Imbalance, qui combine les effets des :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `16. Order Flow Imbalance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0246`; supporting items: SRC-002-ITEM-0013, SRC-008-ITEM-0014; domain indexes `EXECUTION, MICROSTRUCTURE, INVENTORY, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0025 — 17. Multi-Level OFI

- Source: `SRC-007`
- Location: lines 1084–1157; heading `17. Multi-Level OFI`
- Domain tags: MICROSTRUCTURE, RISK, QUANT
- Source statement: 17. Multi-Level OFI: Nous ne devons pas nous limiter au meilleur bid/ask. Pour les tailles que notre bot exécutera, il faut considérer plusieurs niveaux.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `17. Multi-Level OFI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-MICRO-0006`; supporting items: SRC-004-ITEM-0187, SRC-004-ITEM-0192; domain indexes `MICROSTRUCTURE, RISK, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0026 — 18. Queue Imbalance

- Source: `SRC-007`
- Location: lines 1158–1199; heading `18. Queue Imbalance`
- Domain tags: MICROSTRUCTURE, INVENTORY, EXECUTION, SURVIVAL, QUANT
- Source statement: 18. Queue Imbalance: Pour le meilleur bid et ask : → beaucoup plus de quantité bid
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `18. Queue Imbalance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-MICRO-0007`; supporting items: SRC-004-ITEM-0186; domain indexes `MICROSTRUCTURE, INVENTORY, EXECUTION, SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0027 — 19. Microprice

- Source: `SRC-007`
- Location: lines 1200–1225; heading `19. Microprice`
- Domain tags: MICROSTRUCTURE, EXECUTION, MAKER_MODEL
- Source statement: 19. Microprice: On peut également calculer un microprice simplifié. le microprice donne davantage de poids au côté dont la queue opposée suggère une pression plus forte.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `19. Microprice` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0008`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0028 — 20. Market Participants : comportement plutôt qu’identité

- Source: `SRC-007`
- Location: lines 1226–1247; heading `20. Market Participants : comportement plutôt qu’identité`
- Domain tags: PARTICIPANTS, EXECUTION, INFRA, LIQUIDITY_RESPONSE
- Source statement: 20. Market Participants : comportement plutôt qu’identité: Je séparerais les comportements en grandes familles fonctionnelles. Behaviour latent | Ce qu’on cherche à prédire
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `20. Market Participants : comportement plutôt qu’identité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-PART-0001`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, EXECUTION, INFRA, LIQUIDITY_RESPONSE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0029 — 21. Hyperliquid nous offre néanmoins une donnée inhabituelle

- Source: `SRC-007`
- Location: lines 1248–1262; heading `21. Hyperliquid nous offre néanmoins une donnée inhabituelle`
- Domain tags: PARTICIPANTS, OWA, PRODUCT
- Source statement: 21. Hyperliquid nous offre néanmoins une donnée inhabituelle: Le flux public trades Hyperliquid contient actuellement : donc les deux adresses pseudonymes impliquées dans chaque exécution.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `21. Hyperliquid nous offre néanmoins une donnée inhabituelle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-PART-0002`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, OWA, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0030 — 22. Mais une adresse n’est PAS une identité

- Source: `SRC-007`
- Location: lines 1263–1292; heading `22. Mais une adresse n’est PAS une identité`
- Domain tags: EXECUTION, PARTICIPANTS
- Source statement: 22. Mais une adresse n’est PAS une identité: Une même entité peut utiliser : et un même wallet peut également exécuter plusieurs stratégies.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `22. Mais une adresse n’est PAS une identité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0247`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0031 — 23. Address Behaviour Signature

- Source: `SRC-007`
- Location: lines 1293–1340; heading `23. Address Behaviour Signature`
- Domain tags: CROSS_MARKET, GRAPH, PRODUCT
- Source statement: 23. Address Behaviour Signature: Pour une adresse observée passivement dans le flux trades, on peut apprendre :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `23. Address Behaviour Signature` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0001`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET, GRAPH, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0032 — 24. Détecter les arbitrageurs sans connaître leur stratégie

- Source: `SRC-007`
- Location: lines 1341–1386; heading `24. Détecter les arbitrageurs sans connaître leur stratégie`
- Domain tags: PRODUCT
- Source statement: 24. Détecter les arbitrageurs sans connaître leur stratégie: Nous observons ensuite une adresse qui intervient régulièrement : et dont les trades contribuent systématiquement à réduire l’anomalie.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `24. Détecter les arbitrageurs sans connaître leur stratégie` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-PRODUCT-0016`; supporting items: none found by conservative heading match; domain indexes `PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0033 — 25. Le meilleur signal n’est pas « qui », mais « quand »

- Source: `SRC-007`
- Location: lines 1387–1407; heading `25. Le meilleur signal n’est pas « qui », mais « quand »`
- Domain tags: ACCOUNTING, MICROSTRUCTURE
- Source statement: 25. Le meilleur signal n’est pas « qui », mais « quand »: Pour notre profit, l’information importante est : On crée donc pour chaque opportunité historique :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `25. Le meilleur signal n’est pas « qui », mais « quand »` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0050`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0034 — 26. Correction Velocity

- Source: `SRC-007`
- Location: lines 1408–1494; heading `26. Correction Velocity`
- Domain tags: CROSS_MARKET, PRODUCT
- Source statement: 26. Correction Velocity: Une anomalie peut disparaître brutalement ou progressivement. t = 0 edge = 10 bps
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `26. Correction Velocity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0002`; supporting items: SRC-004-ITEM-0242; domain indexes `CROSS_MARKET, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0035 — 27. Liquidity Response Engine

- Source: `SRC-007`
- Location: lines 1495–1527; heading `27. Liquidity Response Engine`
- Domain tags: LIQUIDITY_RESPONSE, PARTICIPANTS, MICROSTRUCTURE
- Source statement: 27. Liquidity Response Engine: Les autres participants ne font pas uniquement bouger les prix. P(\Delta Book | X, shock)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `27. Liquidity Response Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-LIQ-0001`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE, PARTICIPANTS, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0036 — 28. Les événements fondamentaux

- Source: `SRC-007`
- Location: lines 1528–1550; heading `28. Les événements fondamentaux`
- Domain tags: EXECUTION, MICROSTRUCTURE, PRODUCT
- Source statement: 28. Les événements fondamentaux: Les modèles classiques de carnet comme le Queue-Reactive Model représentent justement le carnet comme un système de queues dans lequel les intensités de ces événements dépendent de l’état courant du carnet. C’est extrêmement proche de notre besoin.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `28. Les événements fondamentaux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0248`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MICROSTRUCTURE, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0037 — 29. Queue-Reactive Model : rôle chez nous

- Source: `SRC-007`
- Location: lines 1551–1676; heading `29. Queue-Reactive Model : rôle chez nous`
- Domain tags: MICROSTRUCTURE, EXECUTION, INVENTORY, QUANT, PRODUCT
- Source statement: 29. Queue-Reactive Model : rôle chez nous: Je ne copierais pas directement le modèle académique comme stratégie de production. Je reprendrais son idée fondamentale :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `29. Queue-Reactive Model : rôle chez nous` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0009`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION, INVENTORY, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0038 — 30. Replenishment

- Source: `SRC-007`
- Location: lines 1677–1762; heading `30. Replenishment`
- Domain tags: LIQUIDITY_RESPONSE, SLICING
- Source statement: 30. Replenishment: Après qu’une partie de la liquidité a été consommée, le marché peut la reconstruire rapidement. C’est fondamental pour notre fragmentation/slicing.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `30. Replenishment` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0002`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE, SLICING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0039 — 31. Pourquoi ça change notre slicing

- Source: `SRC-007`
- Location: lines 1763–1877; heading `31. Pourquoi ça change notre slicing`
- Domain tags: SLICING, RISK, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CAPITAL, ROUTING, RESEARCH
- Source statement: 31. Pourquoi ça change notre slicing: route capacity immédiate = 500 € 80 % du depth est replenished en 200 ms
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `31. Pourquoi ça change notre slicing` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SLICE-0003`; supporting items: none found by conservative heading match; domain indexes `SLICING, RISK, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CAPITAL, ROUTING, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0040 — 32. Cancellation/Toxicity Response

- Source: `SRC-007`
- Location: lines 1878–1907; heading `32. Cancellation/Toxicity Response`
- Domain tags: EXECUTION, CROSS_MARKET, MICROSTRUCTURE, QUANT
- Source statement: 32. Cancellation/Toxicity Response: Un market maker ne laisse pas nécessairement sa liquidité en place quand le flux devient dangereux. Cette probabilité est fondamentale pour nos ordres taker :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `32. Cancellation/Toxicity Response` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0249`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CROSS_MARKET, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0041 — 33. Future Depth

- Source: `SRC-007`
- Location: lines 1908–1980; heading `33. Future Depth`
- Domain tags: LIQUIDITY_RESPONSE, FUTURE, EXECUTION, SIMULATOR, PRODUCT
- Source statement: 33. Future Depth: Donc notre Execution Simulator ne doit pas seulement utiliser : ExpectedFill = E[ Fill(q,Book_{arrival}) ]
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `33. Future Depth` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-LIQ-0003`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE, FUTURE, EXECUTION, SIMULATOR, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0042 — 34. Market maker adverse selection

- Source: `SRC-007`
- Location: lines 1981–2004; heading `34. Market maker adverse selection`
- Domain tags: EXECUTION, MAKER_MODEL, TRIANGLE, ARCH, FUTURE
- Source statement: 34. Market maker adverse selection: Pour MT/MTT, c’est encore plus important. Un maker order rempli peut être une mauvaise nouvelle.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `34. Market maker adverse selection` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0250`; supporting items: SRC-004-ITEM-0214, SRC-008-ITEM-0035; domain indexes `EXECUTION, MAKER_MODEL, TRIANGLE, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0043 — 35. Maker model complet

- Source: `SRC-007`
- Location: lines 2005–2111; heading `35. Maker model complet`
- Domain tags: EXECUTION, RECOVERY, RISK, SURVIVAL, MAKER_MODEL, QUANT, PRODUCT
- Source statement: 35. Maker model complet: Le Maker Engine ne doit donc jamais demander uniquement : EV_{maker} = ExecutionBenefit - AdverseSelection - FailedHedgeRisk
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `35. Maker model complet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0251`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, SURVIVAL, MAKER_MODEL, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0044 — 36. MT : formulation plus correcte

- Source: `SRC-007`
- Location: lines 2112–2205; heading `36. MT : formulation plus correcte`
- Domain tags: EXECUTION, RECOVERY, RISK, PARTICIPANTS, SURVIVAL, MAKER_MODEL
- Source statement: 36. MT : formulation plus correcte: EV_{MT} = \int f_{fill}(t|X) \cdot EV_{leg2}(t) dt - AdverseSelection - RecoveryRisk leg2 edge still viable at
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `36. MT : formulation plus correcte` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0252`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, PARTICIPANTS, SURVIVAL, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0045 — 37. Hawkes Processes : challenger utile

- Source: `SRC-007`
- Location: lines 2206–2246; heading `37. Hawkes Processes : challenger utile`
- Domain tags: QUANT, FUTURE, EXECUTION, RISK, MICROSTRUCTURE, ROUTING, HOT_WARM_COLD, PRODUCT
- Source statement: 37. Hawkes Processes : challenger utile: Les événements de marché ne sont pas indépendants. Un market order peut provoquer :
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `37. Hawkes Processes : challenger utile` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-QUANT-0007`; supporting items: none found by conservative heading match; domain indexes `QUANT, FUTURE, EXECUTION, RISK, MICROSTRUCTURE, ROUTING, HOT_WARM_COLD, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0046 — 38. Champion vs Challenger

- Source: `SRC-007`
- Location: lines 2247–2248; heading `38. Champion vs Challenger`
- Domain tags: FUTURE, ARCH
- Source statement: 38. Champion vs Challenger: Notre architecture finale doit permettre plusieurs modèles.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `38. Champion vs Challenger` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0006`; supporting items: SRC-001-ITEM-0109, SRC-005-ITEM-0455, SRC-008-ITEM-0085; domain indexes `FUTURE, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0047 — Champion initial

- Source: `SRC-007`
- Location: lines 2249–2256; heading `Champion initial`
- Domain tags: SURVIVAL
- Source statement: Champion initial: Empirical / survival model simple
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Champion initial` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0006`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0048 — Challenger

- Source: `SRC-007`
- Location: lines 2257–2261; heading `Challenger`
- Domain tags: FUTURE, MICROSTRUCTURE
- Source statement: Challenger: Queue-Reactive
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Challenger` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0007`; supporting items: none found by conservative heading match; domain indexes `FUTURE, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0049 — Challenger supplémentaire

- Source: `SRC-007`
- Location: lines 2262–2266; heading `Challenger supplémentaire`
- Domain tags: FUTURE, QUANT
- Source statement: Challenger supplémentaire: Hawkes
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Challenger supplémentaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0008`; supporting items: none found by conservative heading match; domain indexes `FUTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0050 — Challenger ML

- Source: `SRC-007`
- Location: lines 2267–2271; heading `Challenger ML`
- Domain tags: FUTURE, SURVIVAL, QUANT
- Source statement: Challenger ML: GBDT / survival ML
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Challenger ML` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0009`; supporting items: none found by conservative heading match; domain indexes `FUTURE, SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0051 — Research only

- Source: `SRC-007`
- Location: lines 2272–2285; heading `Research only`
- Domain tags: RESEARCH, ACCOUNTING, QUANT
- Source statement: Research only: ABIDES / full agent simulation Nous gardons le modèle qui produit le meilleur :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Research only` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0016`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0052 — 39. Cross-Market Response Engine

- Source: `SRC-007`
- Location: lines 2286–2306; heading `39. Cross-Market Response Engine`
- Domain tags: CROSS_MARKET, PARTICIPANTS, TRIANGLE, QUANT
- Source statement: 39. Cross-Market Response Engine: Cette partie est essentielle pour notre triangle. Un mouvement sur BTC/HYPE peut être suivi d’une réaction sur les deux autres marchés.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `39. Cross-Market Response Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0003`; supporting items: SRC-004-ITEM-0241, SRC-008-ITEM-0039; domain indexes `CROSS_MARKET, PARTICIPANTS, TRIANGLE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0053 — 40. CrossMarketResponseMatrix

- Source: `SRC-007`
- Location: lines 2307–2370; heading `40. CrossMarketResponseMatrix`
- Domain tags: CROSS_MARKET
- Source statement: 40. CrossMarketResponseMatrix: Pour un shock sur le marché P( \Delta Market_j(h) | Shock_i,X )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `40. CrossMarketResponseMatrix` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0004`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0054 — 41. Ne pas créer une énorme matrice dense

- Source: `SRC-007`
- Location: lines 2371–2409; heading `41. Ne pas créer une énorme matrice dense`
- Domain tags: CROSS_MARKET, TRIANGLE, ROUTING, GRAPH
- Source statement: 41. Ne pas créer une énorme matrice dense: Nous devons utiliser notre Graph Engine. On ne modélise principalement que :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `41. Ne pas créer une énorme matrice dense` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-XMARKET-0005`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET, TRIANGLE, ROUTING, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0055 — 42. Sparse Cross-Market Model

- Source: `SRC-007`
- Location: lines 2410–2469; heading `42. Sparse Cross-Market Model`
- Domain tags: CROSS_MARKET, INFRA, PORTFOLIO
- Source statement: 42. Sparse Cross-Market Model: Le modèle devient : ResponseNeighborhood(i) = \{j_1,j_2,...\}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `42. Sparse Cross-Market Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0006`; supporting items: SRC-006-ITEM-0340; domain indexes `CROSS_MARKET, INFRA, PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0056 — 43. Attention à la causalité

- Source: `SRC-007`
- Location: lines 2470–2488; heading `43. Attention à la causalité`
- Domain tags: EXECUTION, PORTFOLIO, QUANT
- Source statement: 43. Attention à la causalité: Si BTC/HYPE et HYPE/USDC bougent ensemble, cela ne signifie pas nécessairement : Ils peuvent tous les deux répondre à :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `43. Attention à la causalité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0253`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PORTFOLIO, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0057 — 44. Méthode cross-market recommandée

- Source: `SRC-007`
- Location: lines 2489–2547; heading `44. Méthode cross-market recommandée`
- Domain tags: CROSS_MARKET, MICROSTRUCTURE, QUANT
- Source statement: 44. Méthode cross-market recommandée: Je procéderais d’abord avec des event studies. Puis pour chaque marché voisin :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `44. Méthode cross-market recommandée` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0007`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0058 — 45. Lead-Lag Discovery

- Source: `SRC-007`
- Location: lines 2548–2560; heading `45. Lead-Lag Discovery`
- Domain tags: CROSS_MARKET, PORTFOLIO, QUANT, PRODUCT, RESEARCH
- Source statement: 45. Lead-Lag Discovery: La première étape de recherche peut utiliser : pour identifier les relations candidates.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `45. Lead-Lag Discovery` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0008`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET, PORTFOLIO, QUANT, PRODUCT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0059 — 46. Cross-market response et arbitrageurs

- Source: `SRC-007`
- Location: lines 2561–2587; heading `46. Cross-market response et arbitrageurs`
- Domain tags: CROSS_MARKET, EXECUTION, INFRA
- Source statement: 46. Cross-market response et arbitrageurs: Cette matrice nous permet également d’observer indirectement les autres arbitrageurs. HYPE/USDC réagit typiquement 120 ms après
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `46. Cross-market response et arbitrageurs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0009`; supporting items: SRC-004-ITEM-0241, SRC-008-ITEM-0039; domain indexes `CROSS_MARKET, EXECUTION, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0060 — 47. Route-level Competition Model

- Source: `SRC-007`
- Location: lines 2588–2624; heading `47. Route-level Competition Model`
- Domain tags: PARTICIPANTS, ROUTING, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, ARCH
- Source statement: 47. Route-level Competition Model: On ne veut pas seulement un modèle marché par marché. nous devons créer un :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `47. Route-level Competition Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0003`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, ROUTING, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0061 — 48. Dominant Decay Leg

- Source: `SRC-007`
- Location: lines 2625–2649; heading `48. Dominant Decay Leg`
- Domain tags: EXECUTION, RECOVERY, DETERMINISM, ROUTING
- Source statement: 48. Dominant Decay Leg: Une route peut régulièrement mourir à cause du même leg. 67 % des edge deaths
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `48. Dominant Decay Leg` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0254`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, DETERMINISM, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0062 — 49. Route Competition Score

- Source: `SRC-007`
- Location: lines 2650–2693; heading `49. Route Competition Score`
- Domain tags: PARTICIPANTS, ROUTING, ARCH, RISK, OPERATIONS, SURVIVAL
- Source statement: 49. Route Competition Score: Pour monitoring uniquement, on peut créer un score : Mais le Risk Engine ne doit pas utiliser aveuglément un score abstrait.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `49. Route Competition Score` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-PART-0004`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, ROUTING, ARCH, RISK, OPERATIONS, SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0063 — 50. Integration avec notre Latency Distribution

- Source: `SRC-007`
- Location: lines 2694–2746; heading `50. Integration avec notre Latency Distribution`
- Domain tags: INFRA, PRODUCT, RISK, BENCHMARK, PARTICIPANTS
- Source statement: 50. Integration avec notre Latency Distribution: Notre infrastructure nous fournit une distribution : Le Participant Model fournit :
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `50. Integration avec notre Latency Distribution` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0039`; supporting items: none found by conservative heading match; domain indexes `INFRA, PRODUCT, RISK, BENCHMARK, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0064 — 51. Expected Edge at Arrival

- Source: `SRC-007`
- Location: lines 2747–2810; heading `51. Expected Edge at Arrival`
- Domain tags: PRODUCT
- Source statement: 51. Expected Edge at Arrival: Donc le Response Engine prédit une distribution : P( Edge_{arrival} | X )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `51. Expected Edge at Arrival` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-PRODUCT-0017`; supporting items: SRC-004-ITEM-0209, SRC-005-ITEM-0051; domain indexes `PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0065 — 52. Route EV avec Competition Model

- Source: `SRC-007`
- Location: lines 2811–2963; heading `52. Route EV avec Competition Model`
- Domain tags: PARTICIPANTS, ROUTING, EXECUTION, RECOVERY, INFRA, ACCOUNTING, SURVIVAL, QUANT
- Source statement: 52. Route EV avec Competition Model: EV_{route} = P_{success} \cdot E[PnL|success] - P_{partial} \cdot E[RecoveryLoss] - P_{failure} \cdot E[FailureLoss] P_{success} = f( EdgeSurvival, FillProbability, Latency, LiquidityResponse )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `52. Route EV avec Competition Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0005`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, ROUTING, EXECUTION, RECOVERY, INFRA, ACCOUNTING, SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0066 — 53. On ne doit PAS simplement multiplier edge × survival

- Source: `SRC-007`
- Location: lines 2964–2999; heading `53. On ne doit PAS simplement multiplier edge × survival`
- Domain tags: SURVIVAL, FORMULA, EXECUTION, RECOVERY, ACCOUNTING, SIMULATOR, INVENTORY, QUANT
- Source statement: 53. On ne doit PAS simplement multiplier edge × survival: EV = Edge \times P_{survive} Parce que si l’edge disparaît pendant l’exécution, le résultat n’est pas forcément :
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `53. On ne doit PAS simplement multiplier edge × survival` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SURV-0007`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, FORMULA, EXECUTION, RECOVERY, ACCOUNTING, SIMULATOR, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0067 — 54. Intégration exacte avec le Counterfactual Simulator

- Source: `SRC-007`
- Location: lines 3000–3072; heading `54. Intégration exacte avec le Counterfactual Simulator`
- Domain tags: SIMULATOR, PARTICIPANTS, CROSS_MARKET, QUANT, ARCH
- Source statement: 54. Intégration exacte avec le Counterfactual Simulator: World_{cf} = HistoricalBaseline + \Delta our + \Delta response La partie 4 fournit :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `54. Intégration exacte avec le Counterfactual Simulator` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0001`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, PARTICIPANTS, CROSS_MARKET, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0068 — 55. Réaction à notre propre ordre

- Source: `SRC-007`
- Location: lines 3073–3104; heading `55. Réaction à notre propre ordre`
- Domain tags: EXECUTION, PARTICIPANTS, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE
- Source statement: 55. Réaction à notre propre ordre: Notre ordre peut lui-même changer le comportement des autres participants. nous consommons 40 % du best ask
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `55. Réaction à notre propre ordre` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0255`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PARTICIPANTS, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0069 — 56. Mechanical Impact vs Participant Response

- Source: `SRC-007`
- Location: lines 3105–3106; heading `56. Mechanical Impact vs Participant Response`
- Domain tags: PARTICIPANTS, QUANT
- Source statement: 56. Mechanical Impact vs Participant Response: Il faut maintenir cette séparation absolument stricte.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `56. Mechanical Impact vs Participant Response` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0006`; supporting items: SRC-004-ITEM-0202; domain indexes `PARTICIPANTS, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0070 — Mechanical

- Source: `SRC-007`
- Location: lines 3107–3116; heading `Mechanical`
- Domain tags: ARCH
- Source statement: Mechanical: sur un ask de 500
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Mechanical` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0073`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0071 — Participant response

- Source: `SRC-007`
- Location: lines 3117–3126; heading `Participant response`
- Domain tags: PARTICIPANTS, EXECUTION, QUANT
- Source statement: Participant response: un arbitrageur trade sur pair voisin Ne jamais mélanger les deux.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Participant response` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0007`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, EXECUTION, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0072 — 57. Response Model input principal : OFI shock

- Source: `SRC-007`
- Location: lines 3127–3194; heading `57. Response Model input principal : OFI shock`
- Domain tags: MICROSTRUCTURE, EXECUTION, QUANT
- Source statement: 57. Response Model input principal : OFI shock: Notre ordre produit un shock dans l’order flow. Cont et al. montrent que l’OFI est fortement relié aux mouvements très court terme et que l’impact est plus élevé lorsque la profondeur disponible est faible.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `57. Response Model input principal : OFI shock` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0010`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0073 — 58. Impact Ratio

- Source: `SRC-007`
- Location: lines 3195–3299; heading `58. Impact Ratio`
- Domain tags: QUANT, PRODUCT
- Source statement: 58. Impact Ratio: Ces variables détermineront si nous sommes :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `58. Impact Ratio` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0008`; supporting items: none found by conservative heading match; domain indexes `QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0074 — 59. OOD Protection

- Source: `SRC-007`
- Location: lines 3300–3324; heading `59. OOD Protection`
- Domain tags: RISK, SIZING, QUANT, PRODUCT
- Source statement: 59. OOD Protection: Si notre historique contient principalement : orders représentant 1–5 % du depth
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `59. OOD Protection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0300`; supporting items: none found by conservative heading match; domain indexes `RISK, SIZING, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0075 — 60. Participant Model Confidence

- Source: `SRC-007`
- Location: lines 3325–3358; heading `60. Participant Model Confidence`
- Domain tags: PARTICIPANTS, RISK, BENCHMARK, ACCOUNTING, SIMULATOR, ROUTING
- Source statement: 60. Participant Model Confidence: Je créerais : ParticipantModelConfidence
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `60. Participant Model Confidence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0008`; supporting items: SRC-006-ITEM-0338; domain indexes `PARTICIPANTS, RISK, BENCHMARK, ACCOUNTING, SIMULATOR, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0076 — 61. Public L2 mode vs future L4 mode

- Source: `SRC-007`
- Location: lines 3359–3396; heading `61. Public L2 mode vs future L4 mode`
- Domain tags: FUTURE, EXECUTION, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, ROUTING
- Source statement: 61. Public L2 mode vs future L4 mode: Nous devons explicitement séparer les capacités. Mais ne permet pas avec certitude :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `61. Public L2 mode vs future L4 mode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0010`; supporting items: none found by conservative heading match; domain indexes `FUTURE, EXECUTION, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0077 — 62. Adresse-level modeling : activation secondaire

- Source: `SRC-007`
- Location: lines 3397–3445; heading `62. Adresse-level modeling : activation secondaire`
- Domain tags: EXECUTION, RECORDER, QUANT, PRODUCT, ARCH
- Source statement: 62. Adresse-level modeling : activation secondaire: Grâce au champ public : je stockerais les adresses dès le Recorder initial.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `62. Adresse-level modeling : activation secondaire` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0256`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, QUANT, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0078 — 63. Participant clustering

- Source: `SRC-007`
- Location: lines 3446–3485; heading `63. Participant clustering`
- Domain tags: PARTICIPANTS, CROSS_MARKET, ARCH, FUTURE
- Source statement: 63. Participant clustering: Plus tard, des adresses peuvent être regroupées par similarité de comportement. Mais encore une fois :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `63. Participant clustering` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-PART-0009`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, CROSS_MARKET, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0079 — 64. Privacy / stockage

- Source: `SRC-007`
- Location: lines 3486–3495; heading `64. Privacy / stockage`
- Domain tags: DATA, DETERMINISM, CLIENT, PRODUCT
- Source statement: 64. Privacy / stockage: Les adresses étant publiques, elles peuvent techniquement être stockées. Je recommanderais néanmoins en production client :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `64. Privacy / stockage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0316`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM, CLIENT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0080 — 65. Pas de requêtes API individuelles massives

- Source: `SRC-007`
- Location: lines 3496–3514; heading `65. Pas de requêtes API individuelles massives`
- Domain tags: RISK, INVENTORY
- Source statement: 65. Pas de requêtes API individuelles massives: Même si nous voyons une adresse trader, nous n’allons pas immédiatement interroger Hyperliquid : Notre première couche address-model repose uniquement sur le flux passif.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `65. Pas de requêtes API individuelles massives` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-RISK-0301`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0081 — 66. Data collection requise

- Source: `SRC-007`
- Location: lines 3515–3539; heading `66. Data collection requise`
- Domain tags: EXECUTION, RECORDER, CLOCK, INFRA, ROUTING, PRODUCT
- Source statement: 66. Data collection requise: Notre Recorder doit désormais explicitement conserver :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `66. Data collection requise` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0257`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, CLOCK, INFRA, ROUTING, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0082 — 67. Opportunity Dataset

- Source: `SRC-007`
- Location: lines 3540–3573; heading `67. Opportunity Dataset`
- Domain tags: DATA, PARTICIPANTS, ROUTING
- Source statement: 67. Opportunity Dataset: Chaque opportunité doit devenir un objet historique. C’est notre dataset principal pour le Competition Engine.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `67. Opportunity Dataset` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0317`; supporting items: none found by conservative heading match; domain indexes `DATA, PARTICIPANTS, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0083 — 68. Important : stocker aussi les non-opportunités

- Source: `SRC-007`
- Location: lines 3574–3591; heading `68. Important : stocker aussi les non-opportunités`
- Domain tags: ARCH
- Source statement: 68. Important : stocker aussi les non-opportunités: Sinon nous créons un énorme biais. Il faut également enregistrer des :
- Nature: rejected approach
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `68. Important : stocker aussi les non-opportunités` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-ARCH-0074`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0084 — 69. Edge birth labeling

- Source: `SRC-007`
- Location: lines 3592–3619; heading `69. Edge birth labeling`
- Domain tags: CLOCK, ACCOUNTING, REPLAY
- Source statement: 69. Edge birth labeling: Une mauvaise définition de birth peut complètement contaminer le modèle. Il faudra une règle du type :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `69. Edge birth labeling` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-CLOCK-0014`; supporting items: none found by conservative heading match; domain indexes `CLOCK, ACCOUNTING, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0085 — 70. Censoring

- Source: `SRC-007`
- Location: lines 3620–3641; heading `70. Censoring`
- Domain tags: ACCOUNTING, SURVIVAL, ARCH
- Source statement: 70. Censoring: La survival analysis gère très bien un problème important. Supposons qu’une opportunité existe encore lorsque :
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `70. Censoring` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0051`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, SURVIVAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0086 — 71. Premier modèle : empirical survival

- Source: `SRC-007`
- Location: lines 3642–3666; heading `71. Premier modèle : empirical survival`
- Domain tags: SURVIVAL, ROUTING, QUANT
- Source statement: 71. Premier modèle : empirical survival: Puis Kaplan-Meier / empirical survival. Cela crée une baseline extrêmement utile et difficile à tromper.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `71. Premier modèle : empirical survival` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0008`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0087 — 72. Deuxième modèle : discrete hazard

- Source: `SRC-007`
- Location: lines 3667–3723; heading `72. Deuxième modèle : discrete hazard`
- Domain tags: SURVIVAL, QUANT, PRODUCT, ARCH
- Source statement: 72. Deuxième modèle : discrete hazard: P( death_{t,t+\Delta} | alive_t,X_t ) = \sigma( \beta^T X_t ) Très bonne première solution production.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `72. Deuxième modèle : discrete hazard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0009`; supporting items: SRC-004-ITEM-0205; domain indexes `SURVIVAL, QUANT, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0088 — 73. Troisième modèle : survival GBDT

- Source: `SRC-007`
- Location: lines 3724–3740; heading `73. Troisième modèle : survival GBDT`
- Domain tags: SURVIVAL, QUANT, ARCH, FUTURE
- Source statement: 73. Troisième modèle : survival GBDT: sans nécessiter un réseau neuronal. Rust charge un modèle compact ou une représentation exportée.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `73. Troisième modèle : survival GBDT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-SURV-0010`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, QUANT, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0089 — 74. Deep survival : seulement si nécessaire

- Source: `SRC-007`
- Location: lines 3741–3756; heading `74. Deep survival : seulement si nécessaire`
- Domain tags: SURVIVAL, EXECUTION, ACCOUNTING, REPLAY, MAKER_MODEL, QUANT, RESEARCH
- Source statement: 74. Deep survival : seulement si nécessaire: La recherche moderne montre que des modèles neural/transformer peuvent améliorer l’estimation de time-to-fill. une amélioration statistique ne signifie pas automatiquement une amélioration économique.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `74. Deep survival : seulement si nécessaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0011`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, EXECUTION, ACCOUNTING, REPLAY, MAKER_MODEL, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0090 — 75. Train/Test split

- Source: `SRC-007`
- Location: lines 3757–3784; heading `75. Train/Test split`
- Domain tags: VALIDATION, QUANT, FUTURE
- Source statement: 75. Train/Test split: et également des tests :
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `75. Train/Test split` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0368`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0091 — 76. Walk-forward validation

- Source: `SRC-007`
- Location: lines 3785–3811; heading `76. Walk-forward validation`
- Domain tags: VALIDATION
- Source statement: 76. Walk-forward validation: Cela mesure la dégradation dans le temps.
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `76. Walk-forward validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0369`; supporting items: SRC-001-ITEM-0059, SRC-006-ITEM-0482; domain indexes `VALIDATION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0092 — 77. Probability calibration

- Source: `SRC-007`
- Location: lines 3812–3835; heading `77. Probability calibration`
- Domain tags: QUANT
- Source statement: 77. Probability calibration: P(edge survives horizon) = 70 % Sur 1000 cas similaires, nous voulons environ :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `77. Probability calibration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0009`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0093 — 78. Métriques statistiques

- Source: `SRC-007`
- Location: lines 3836–3852; heading `78. Métriques statistiques`
- Domain tags: ACCOUNTING, PARTICIPANTS, SURVIVAL, ARCH
- Source statement: 78. Métriques statistiques: Pour le survival/competition model : La métrique finale reste :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `78. Métriques statistiques` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0052`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, PARTICIPANTS, SURVIVAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0094 — 79. Economic Lift

- Source: `SRC-007`
- Location: lines 3853–3854; heading `79. Economic Lift`
- Domain tags: ACCOUNTING
- Source statement: 79. Economic Lift: On compare :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `79. Economic Lift` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0053`; supporting items: SRC-004-ITEM-0260; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0095 — Baseline

- Source: `SRC-007`
- Location: lines 3855–3859; heading `Baseline`
- Domain tags: ARCH
- Source statement: Baseline: trade if raw net edge > threshold
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Baseline` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ARCH-0075`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0096 — New

- Source: `SRC-007`
- Location: lines 3860–3917; heading `New`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING, SURVIVAL, CAPITAL
- Source statement: New: EconomicLift = PnL_{model} - PnL_{baseline}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `New` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0258`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING, SURVIVAL, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0097 — 80. Calibration avec Micro-Live

- Source: `SRC-007`
- Location: lines 3918–3941; heading `80. Calibration avec Micro-Live`
- Domain tags: VALIDATION, EXECUTION, DATA, REPLAY, SURVIVAL
- Source statement: 80. Calibration avec Micro-Live: Une fois le modèle stable en replay : Ce dataset réel devient extrêmement précieux.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `80. Calibration avec Micro-Live` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0370`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481, SRC-006-ITEM-0418; domain indexes `VALIDATION, EXECUTION, DATA, REPLAY, SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0098 — 81. Address behaviour calibration en live

- Source: `SRC-007`
- Location: lines 3942–3957; heading `81. Address behaviour calibration en live`
- Domain tags: INFRA, PARTICIPANTS
- Source statement: 81. Address behaviour calibration en live: On peut également vérifier : did known address cluster actually trade?
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `81. Address behaviour calibration en live` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0040`; supporting items: none found by conservative heading match; domain indexes `INFRA, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0099 — 82. Model Drift

- Source: `SRC-007`
- Location: lines 3958–4001; heading `82. Model Drift`
- Domain tags: SURVIVAL, OWA
- Source statement: 82. Model Drift: Le travail OWA récent observe justement une accélération des séquences au fil du temps. ne peut pas être calibré une fois pour toujours.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `82. Model Drift` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-SURV-0012`; supporting items: SRC-005-ITEM-0108, SRC-006-ITEM-0557; domain indexes `SURVIVAL, OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0100 — 83. Fast / Recent / Medium / Long

- Source: `SRC-007`
- Location: lines 4002–4026; heading `83. Fast / Recent / Medium / Long`
- Domain tags: PARTICIPANTS, ARCH
- Source statement: 83. Fast / Recent / Medium / Long: Comme dans notre architecture générale : last hour t50 = 170ms
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `83. Fast / Recent / Medium / Long` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-PART-0010`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0101 — 84. Regime Classifier

- Source: `SRC-007`
- Location: lines 4027–4045; heading `84. Regime Classifier`
- Domain tags: OPERATIONS, PARTICIPANTS, QUANT
- Source statement: 84. Regime Classifier: Je créerais donc également : Mais ces noms sont des labels de monitoring.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `84. Regime Classifier` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OPS-0018`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, PARTICIPANTS, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0102 — 85. Online learning : pas directement dans la production

- Source: `SRC-007`
- Location: lines 4046–4067; heading `85. Online learning : pas directement dans la production`
- Domain tags: PRODUCT, ACCOUNTING, ARCH
- Source statement: 85. Online learning : pas directement dans la production: bot modifies model weights live Un nouveau modèle est validé.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `85. Online learning : pas directement dans la production` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0018`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, ACCOUNTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0103 — 86. Champion / Challenger production

- Source: `SRC-007`
- Location: lines 4068–4092; heading `86. Champion / Challenger production`
- Domain tags: PRODUCT, FUTURE, ACCOUNTING, SIMULATOR
- Source statement: 86. Champion / Challenger production: → no effect on orders
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `86. Champion / Challenger production` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-PRODUCT-0019`; supporting items: SRC-005-ITEM-0455, SRC-008-ITEM-0085; domain indexes `PRODUCT, FUTURE, ACCOUNTING, SIMULATOR`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0104 — 87. Versionnement des modèles

- Source: `SRC-007`
- Location: lines 4093–4114; heading `87. Versionnement des modèles`
- Domain tags: DATA, INFRA, VALIDATION, RESEARCH
- Source statement: 87. Versionnement des modèles: Il est impossible de faire de la vraie recherche scientifique sans ça.
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `87. Versionnement des modèles` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0318`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, VALIDATION, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0105 — 88. Hot Path : aucune grosse simulation

- Source: `SRC-007`
- Location: lines 4115–4143; heading `88. Hot Path : aucune grosse simulation`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, DEPLOYMENT, SIMULATOR, LIQUIDITY_RESPONSE, MAKER_MODEL
- Source statement: 88. Hot Path : aucune grosse simulation: Le live Rust ne doit pas faire : 10 000 Monte Carlo paths
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `88. Hot Path : aucune grosse simulation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ROUTE-0028`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH, EXECUTION, DEPLOYMENT, SIMULATOR, LIQUIDITY_RESPONSE, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0106 — 89. Monte Carlo reste dans Execution Simulator

- Source: `SRC-007`
- Location: lines 4144–4159; heading `89. Monte Carlo reste dans Execution Simulator`
- Domain tags: SIMULATOR, RISK, PARTICIPANTS, QUANT, PRODUCT
- Source statement: 89. Monte Carlo reste dans Execution Simulator: Le Simulator peut ensuite, lorsqu’il en a besoin : depuis les distributions produites par le Participant Model.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `89. Monte Carlo reste dans Execution Simulator` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0002`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, RISK, PARTICIPANTS, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0107 — 90. Architecture Rust

- Source: `SRC-007`
- Location: lines 4160–4181; heading `90. Architecture Rust`
- Domain tags: ARCH, DEPLOYMENT, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, INVENTORY
- Source statement: 90. Architecture Rust: Je créerais : src/
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `90. Architecture Rust` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0076`; supporting items: SRC-002-ITEM-0148; domain indexes `ARCH, DEPLOYMENT, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0108 — 91. Integration simulator

- Source: `SRC-007`
- Location: lines 4182–4195; heading `91. Integration simulator`
- Domain tags: SIMULATOR, PARTICIPANTS, PRODUCT, FUTURE
- Source statement: 91. Integration simulator: L’agent challenger n’est pas utilisé en production initiale.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `91. Integration simulator` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-SIM-0003`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, PARTICIPANTS, PRODUCT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0109 — 92. Python R&D

- Source: `SRC-007`
- Location: lines 4196–4216; heading `92. Python R&D`
- Domain tags: ARCH, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, QUANT, PRODUCT
- Source statement: 92. Python R&D: Même philosophie que le reste du projet.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `92. Python R&D` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0077`; supporting items: none found by conservative heading match; domain indexes `ARCH, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, MICROSTRUCTURE, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0110 — 93. Structures live

- Source: `SRC-007`
- Location: lines 4217–4237; heading `93. Structures live`
- Domain tags: BENCHMARK, PARTICIPANTS
- Source statement: 93. Structures live: Conceptuellement : CompetitionForecast {
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `93. Structures live` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-BENCH-0006`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0111 — 94. Liquidity forecast

- Source: `SRC-007`
- Location: lines 4238–4255; heading `94. Liquidity forecast`
- Domain tags: LIQUIDITY_RESPONSE
- Source statement: 94. Liquidity forecast: LiquidityForecast { expected_depth_arrival,
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `94. Liquidity forecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0004`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0112 — 95. Maker forecast

- Source: `SRC-007`
- Location: lines 4256–4276; heading `95. Maker forecast`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: 95. Maker forecast: Les horizons seront adaptés à la fidélité réelle de nos données.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `95. Maker forecast` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0259`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0113 — 96. Cross-market forecast

- Source: `SRC-007`
- Location: lines 4277–4291; heading `96. Cross-market forecast`
- Domain tags: CROSS_MARKET, PRODUCT
- Source statement: 96. Cross-market forecast: CrossMarketForecast { affected_pairs[],
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `96. Cross-market forecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0010`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0114 — 97. Participant address forecast — optionnel

- Source: `SRC-007`
- Location: lines 4292–4307; heading `97. Participant address forecast — optionnel`
- Domain tags: PARTICIPANTS, QUANT
- Source statement: 97. Participant address forecast — optionnel: Pas nécessairement activé au départ.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `97. Participant address forecast — optionnel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0011`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0115 — 98. HOT / WARM / COLD

- Source: `SRC-007`
- Location: lines 4308–4309; heading `98. HOT / WARM / COLD`
- Domain tags: HOT_WARM_COLD, CAPITAL, ARCH
- Source statement: 98. HOT / WARM / COLD: Ce module suit notre architecture capital-aware.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `98. HOT / WARM / COLD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0028`; supporting items: SRC-001-ITEM-0049, SRC-001-ITEM-0051, SRC-002-ITEM-0106, SRC-002-ITEM-0124; domain indexes `HOT_WARM_COLD, CAPITAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0116 — HOT

- Source: `SRC-007`
- Location: lines 4310–4318; heading `HOT`
- Domain tags: HOT_WARM_COLD, SURVIVAL, CROSS_MARKET
- Source statement: HOT: full features survival
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `HOT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0029`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD, SURVIVAL, CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0117 — WARM

- Source: `SRC-007`
- Location: lines 4319–4326; heading `WARM`
- Domain tags: HOT_WARM_COLD, SURVIVAL, LIQUIDITY_RESPONSE, MICROSTRUCTURE
- Source statement: WARM: basic survival trade activity
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `WARM` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0030`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD, SURVIVAL, LIQUIDITY_RESPONSE, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0118 — COLD

- Source: `SRC-007`
- Location: lines 4327–4334; heading `COLD`
- Domain tags: HOT_WARM_COLD, INFRA, PARTICIPANTS, SURVIVAL, GRAPH
- Source statement: COLD: Ainsi le Participant Model ne transforme pas le Global Graph entier en monstre CPU.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `COLD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0031`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD, INFRA, PARTICIPANTS, SURVIVAL, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0119 — 99. Global Watcher

- Source: `SRC-007`
- Location: lines 4335–4352; heading `99. Global Watcher`
- Domain tags: INFRA, MICROSTRUCTURE, HOT_WARM_COLD
- Source statement: 99. Global Watcher: Le Global Watcher pourra également observer :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `99. Global Watcher` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0041`; supporting items: SRC-002-ITEM-0098; domain indexes `INFRA, MICROSTRUCTURE, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0120 — 100. Participant Model et Sizing

- Source: `SRC-007`
- Location: lines 4353–4444; heading `100. Participant Model et Sizing`
- Domain tags: PARTICIPANTS, SIZING, RECOVERY, RISK, SURVIVAL, CAPITAL, QUANT, PRODUCT
- Source statement: 100. Participant Model et Sizing: La taille ne dépend plus seulement du L2 actuel. q^* = f( CurrentDepth, FutureDepthDistribution, EdgeSurvival, Impact, RecoveryRisk )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `100. Participant Model et Sizing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-PART-0012`; supporting items: SRC-006-ITEM-0338; domain indexes `PARTICIPANTS, SIZING, RECOVERY, RISK, SURVIVAL, CAPITAL, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0121 — 101. Participant Model et slicing

- Source: `SRC-007`
- Location: lines 4445–4519; heading `101. Participant Model et slicing`
- Domain tags: PARTICIPANTS, SLICING, EXECUTION, SURVIVAL, LIQUIDITY_RESPONSE, ARCH
- Source statement: 101. Participant Model et slicing: OptimalSlice = f( ReplenishmentCurve, EdgeSurvivalCurve, CompetitionHazard ) Une replenishment rapide ne justifie pas un deuxième child order si l’edge meurt encore plus vite.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `101. Participant Model et slicing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0013`; supporting items: SRC-006-ITEM-0338; domain indexes `PARTICIPANTS, SLICING, EXECUTION, SURVIVAL, LIQUIDITY_RESPONSE, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0122 — 102. Participant Model et Infrastructure

- Source: `SRC-007`
- Location: lines 4520–4580; heading `102. Participant Model et Infrastructure`
- Domain tags: INFRA, PARTICIPANTS, ACCOUNTING, QUANT
- Source statement: 102. Participant Model et Infrastructure: Nous avons désormais une connexion complète : InfrastructureLatency \rightarrow P_{survive} \rightarrow CaptureRatio \rightarrow PnL \rightarrow InfraROI
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `102. Participant Model et Infrastructure` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0042`; supporting items: SRC-006-ITEM-0338; domain indexes `INFRA, PARTICIPANTS, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0123 — 103. Participant Model et Market Atlas

- Source: `SRC-007`
- Location: lines 4581–4614; heading `103. Participant Model et Market Atlas`
- Domain tags: PARTICIPANTS, MARKET_ATLAS, EXECUTION, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, INVENTORY, ROUTING
- Source statement: 103. Participant Model et Market Atlas: Le Market Atlas pourra apprendre pour chaque : Ce sont d’excellentes features pour décider quels actifs doivent être :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `103. Participant Model et Market Atlas` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0014`; supporting items: SRC-006-ITEM-0330, SRC-006-ITEM-0338; domain indexes `PARTICIPANTS, MARKET_ATLAS, EXECUTION, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0124 — 104. Participant Model et Bridge Engine

- Source: `SRC-007`
- Location: lines 4615–4646; heading `104. Participant Model et Bridge Engine`
- Domain tags: PARTICIPANTS, BRIDGE, EXECUTION, ACCOUNTING, CAPITAL
- Source statement: 104. Participant Model et Bridge Engine: Même le Capital Relocation Engine peut utiliser cette information. median lifetime = extremely short
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `104. Participant Model et Bridge Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0015`; supporting items: SRC-006-ITEM-0338, SRC-006-ITEM-0373; domain indexes `PARTICIPANTS, BRIDGE, EXECUTION, ACCOUNTING, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0125 — 105. Participant Model et Recovery

- Source: `SRC-007`
- Location: lines 4647–4672; heading `105. Participant Model et Recovery`
- Domain tags: RECOVERY, PARTICIPANTS, EXECUTION, CROSS_MARKET, QUANT
- Source statement: 105. Participant Model et Recovery: Après un partial fill, nous devons savoir : où le flux se dirige probablement
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `105. Participant Model et Recovery` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0016`; supporting items: SRC-006-ITEM-0338; domain indexes `RECOVERY, PARTICIPANTS, EXECUTION, CROSS_MARKET, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0126 — 106. Ce qu’il ne faut SURTOUT PAS construire

- Source: `SRC-007`
- Location: lines 4673–4685; heading `106. Ce qu’il ne faut SURTOUT PAS construire`
- Domain tags: EXECUTION, RISK
- Source statement: 106. Ce qu’il ne faut SURTOUT PAS construire: Je déconseille absolument de partir sur : On obtiendrait un monde extrêmement sophistiqué mais potentiellement faux.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `106. Ce qu’il ne faut SURTOUT PAS construire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0260`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0127 — 107. Agent-based simulation : véritable rôle

- Source: `SRC-007`
- Location: lines 4686–4715; heading `107. Agent-based simulation : véritable rôle`
- Domain tags: PARTICIPANTS, EXECUTION, SIMULATOR, CROSS_EXCHANGE, FUTURE, RESEARCH
- Source statement: 107. Agent-based simulation : véritable rôle: peut servir à des stress tests : what if arbitrage response becomes 3× faster?
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `107. Agent-based simulation : véritable rôle` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0016`; supporting items: SRC-008-ITEM-0069; domain indexes `PARTICIPANTS, EXECUTION, SIMULATOR, CROSS_EXCHANGE, FUTURE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0128 — 108. Architecture finale : Fidelity Levels

- Source: `SRC-007`
- Location: lines 4716–4718; heading `108. Architecture finale : Fidelity Levels`
- Domain tags: SIMULATOR, ARCH
- Source statement: 108. Architecture finale : Fidelity Levels: Une seule architecture. Pas plusieurs bots.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `108. Architecture finale : Fidelity Levels` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0004`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0129 — P0 — Historical participants

- Source: `SRC-007`
- Location: lines 4719–4720; heading `P0 — Historical participants`
- Domain tags: PARTICIPANTS
- Source statement: P0 — Historical participants: Le tape historique contient déjà l’activité réelle.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `P0 — Historical participants` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0017`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0130 — P1 — Edge Survival

- Source: `SRC-007`
- Location: lines 4721–4725; heading `P1 — Edge Survival`
- Domain tags: SURVIVAL
- Source statement: P1 — Edge Survival: survival / hazard
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `P1 — Edge Survival` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0013`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0131 — P2 — Aggregate Response

- Source: `SRC-007`
- Location: lines 4726–4733; heading `P2 — Aggregate Response`
- Domain tags: EXECUTION, LIQUIDITY_RESPONSE, MICROSTRUCTURE
- Source statement: P2 — Aggregate Response: liquidity replenishment
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `P2 — Aggregate Response` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0261`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, LIQUIDITY_RESPONSE, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0132 — P3 — Cross Market

- Source: `SRC-007`
- Location: lines 4734–4739; heading `P3 — Cross Market`
- Domain tags: CROSS_MARKET
- Source statement: P3 — Cross Market: lead-lag response matrix
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `P3 — Cross Market` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0011`; supporting items: SRC-004-ITEM-0241, SRC-005-ITEM-0114, SRC-006-ITEM-0340, SRC-006-ITEM-0342; domain indexes `CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0133 — P4 — Participant Signatures

- Source: `SRC-007`
- Location: lines 4740–4744; heading `P4 — Participant Signatures`
- Domain tags: PARTICIPANTS
- Source statement: P4 — Participant Signatures: address / behaviour clusters
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `P4 — Participant Signatures` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0018`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0134 — P5 — Interactive Research

- Source: `SRC-007`
- Location: lines 4745–4754; heading `P5 — Interactive Research`
- Domain tags: SIMULATOR, RESEARCH, MICROSTRUCTURE, QUANT, ARCH
- Source statement: P5 — Interactive Research: Toutes les interfaces existent dans l’architecture dès le départ. On active progressivement la fidélité selon les données.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `P5 — Interactive Research` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0005`; supporting items: SRC-008-ITEM-0077; domain indexes `SIMULATOR, RESEARCH, MICROSTRUCTURE, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0135 — 109. Priorité de développement

- Source: `SRC-007`
- Location: lines 4755–4756; heading `109. Priorité de développement`
- Domain tags: ARCH
- Source statement: 109. Priorité de développement: L’ordre de développement que je recommande est très précis.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `109. Priorité de développement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0078`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0136 — Première priorité

- Source: `SRC-007`
- Location: lines 4757–4763; heading `Première priorité`
- Domain tags: EXECUTION, RECORDER, DATA, PARTICIPANTS
- Source statement: Première priorité: Recorder + OpportunityEpisodes. Sans dataset :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Première priorité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0262`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, DATA, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0137 — Ensuite

- Source: `SRC-007`
- Location: lines 4764–4766; heading `Ensuite`
- Domain tags: SURVIVAL, QUANT
- Source statement: Ensuite: C’est probablement le plus gros gain valeur/complexité.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Ensuite` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0014`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0138 — Puis

- Source: `SRC-007`
- Location: lines 4767–4768; heading `Puis`
- Domain tags: LIQUIDITY_RESPONSE, MICROSTRUCTURE
- Source statement: Puis: OFI + liquidity response.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Puis` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0005`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0139 — Puis

- Source: `SRC-007`
- Location: lines 4769–4770; heading `Puis`
- Domain tags: EXECUTION, MAKER_MODEL
- Source statement: Puis: Maker fill/adverse selection.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Puis` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0263`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0140 — Puis

- Source: `SRC-007`
- Location: lines 4771–4772; heading `Puis`
- Domain tags: CROSS_MARKET
- Source statement: Puis: CrossMarketResponse.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Puis` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0012`; supporting items: none found by conservative heading match; domain indexes `CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0141 — Puis seulement

- Source: `SRC-007`
- Location: lines 4773–4774; heading `Puis seulement`
- Domain tags: PARTICIPANTS
- Source statement: Puis seulement: Participant addresses/clusters.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Puis seulement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0019`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0142 — Enfin

- Source: `SRC-007`
- Location: lines 4775–4777; heading `Enfin`
- Domain tags: PARTICIPANTS, MICROSTRUCTURE, QUANT, FUTURE
- Source statement: Enfin: Queue-Reactive/Hawkes/agent-based challengers.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Enfin` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-PART-0020`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, MICROSTRUCTURE, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0143 — 110. Pourquoi Survival avant identification des bots

- Source: `SRC-007`
- Location: lines 4778–4800; heading `110. Pourquoi Survival avant identification des bots`
- Domain tags: SURVIVAL, EXECUTION, RISK, INFRA, SIZING, ROUTING
- Source statement: 110. Pourquoi Survival avant identification des bots: Parce que pour gagner une course, nous avons besoin de connaître : P(\text{course ends before } t)
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `110. Pourquoi Survival avant identification des bots` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-SURV-0015`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, EXECUTION, RISK, INFRA, SIZING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0144 — 111. Acceptation d’un nouveau modèle

- Source: `SRC-007`
- Location: lines 4801–4876; heading `111. Acceptation d’un nouveau modèle`
- Domain tags: ACCOUNTING, FUTURE
- Source statement: 111. Acceptation d’un nouveau modèle: Un Challenger ne passe Champion que s’il satisfait simultanément :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `111. Acceptation d’un nouveau modèle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ACCT-0054`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0145 — 112. Safety fallback

- Source: `SRC-007`
- Location: lines 4877–4899; heading `112. Safety fallback`
- Domain tags: RISK, SURVIVAL, SIZING, ROUTING
- Source statement: 112. Safety fallback: Si le modèle devient indisponible : le bot ne doit pas faire n’importe quoi.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `112. Safety fallback` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0302`; supporting items: none found by conservative heading match; domain indexes `RISK, SURVIVAL, SIZING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0146 — 113. Model disagreement

- Source: `SRC-007`
- Location: lines 4900–4931; heading `113. Model disagreement`
- Domain tags: RISK, FUTURE
- Source statement: 113. Model disagreement: Le désaccord entre modèles peut lui-même devenir un Risk Signal.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `113. Model disagreement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0303`; supporting items: SRC-004-ITEM-0262, SRC-005-ITEM-0056; domain indexes `RISK, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0147 — 114. Final execution formula

- Source: `SRC-007`
- Location: lines 4932–5138; heading `114. Final execution formula`
- Domain tags: RISK, INFRA, OPERATIONS, ACCOUNTING, PARTICIPANTS, INVENTORY, QUANT
- Source statement: 114. Final execution formula: Notre logique finale peut être conceptualisée ainsi : ExpectedEconomicPnL(r,q) = E[ PnL | MarketState, ParticipantResponse, Latency, Impact ]
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `114. Final execution formula` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0304`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, OPERATIONS, ACCOUNTING, PARTICIPANTS, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0148 — 115. Version simplifiée de notre décision

- Source: `SRC-007`
- Location: lines 5139–5188; heading `115. Version simplifiée de notre décision`
- Domain tags: EXECUTION, RECOVERY, RISK, INFRA, ACCOUNTING, SURVIVAL, CROSS_MARKET, ROUTING
- Source statement: 115. Version simplifiée de notre décision: Edge survival at our latency C’est une logique de niveau professionnel.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `115. Version simplifiée de notre décision` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0264`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, INFRA, ACCOUNTING, SURVIVAL, CROSS_MARKET, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0149 — 116. Ce que cette partie apporte réellement au projet

- Source: `SRC-007`
- Location: lines 5189–5206; heading `116. Ce que cette partie apporte réellement au projet`
- Domain tags: EXECUTION, RECOVERY, RISK, INFRA, SIMULATOR, CAPITAL, SIZING, MARKET_ATLAS
- Source statement: 116. Ce que cette partie apporte réellement au projet: Cette partie ne sert pas seulement au Simulator. Elle devient donc une brique transversale.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `116. Ce que cette partie apporte réellement au projet` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0265`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, INFRA, SIMULATOR, CAPITAL, SIZING, MARKET_ATLAS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0150 — 117. Les trois modèles réellement fondamentaux

- Source: `SRC-007`
- Location: lines 5207–5208; heading `117. Les trois modèles réellement fondamentaux`
- Domain tags: ARCH
- Source statement: 117. Les trois modèles réellement fondamentaux: Si je devais résumer tout ce travail en trois objets :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `117. Les trois modèles réellement fondamentaux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0079`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0151 — 1 — Edge Survival Model

- Source: `SRC-007`
- Location: lines 5209–5235; heading `1 — Edge Survival Model`
- Domain tags: SURVIVAL, ARCH
- Source statement: 1 — Edge Survival Model: P( Edge_{t+h} > threshold | X_t ) aurons-nous encore une opportunité quand nous arriverons ?
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `1 — Edge Survival Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-SURV-0016`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0152 — 2 — Liquidity Response Model

- Source: `SRC-007`
- Location: lines 5236–5269; heading `2 — Liquidity Response Model`
- Domain tags: LIQUIDITY_RESPONSE
- Source statement: 2 — Liquidity Response Model: P( Book_{t+h} | Book_t, Flow, OurShock ) quel carnet allons-nous réellement rencontrer ?
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `2 — Liquidity Response Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0006`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0153 — 3 — Cross-Market Response Model

- Source: `SRC-007`
- Location: lines 5270–5299; heading `3 — Cross-Market Response Model`
- Domain tags: CROSS_MARKET, ROUTING
- Source statement: 3 — Cross-Market Response Model: P( Market_j(t+h) | Shock_i, X ) comment les autres marchés de notre route vont-ils réagir ?
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `3 — Cross-Market Response Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-XMARKET-0013`; supporting items: SRC-004-ITEM-0241, SRC-006-ITEM-0340, SRC-008-ITEM-0039; domain indexes `CROSS_MARKET, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0154 — 118. Conclusion scientifique

- Source: `SRC-007`
- Location: lines 5300–5309; heading `118. Conclusion scientifique`
- Domain tags: EXECUTION, RISK, SURVIVAL, MICROSTRUCTURE, INVENTORY, OWA, QUANT, PRODUCT
- Source statement: 118. Conclusion scientifique: La littérature donne plusieurs enseignements compatibles entre eux. L’OFI et l’état du carnet contiennent une information importante sur les mouvements très court terme.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `118. Conclusion scientifique` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0266`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, SURVIVAL, MICROSTRUCTURE, INVENTORY, OWA, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0155 — 119. Direction définitive que je recommande

- Source: `SRC-007`
- Location: lines 5310–5342; heading `119. Direction définitive que je recommande`
- Domain tags: EXECUTION, RISK, SIMULATOR, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, INVENTORY
- Source statement: 119. Direction définitive que je recommande: Le bot ne doit PAS être : Il doit progressivement devenir :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `119. Direction définitive que je recommande` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0267`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, SIMULATOR, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0156 — 120. Principe final de la partie 4

- Source: `SRC-007`
- Location: lines 5343–5387; heading `120. Principe final de la partie 4`
- Domain tags: INFRA, ACCOUNTING, PARTICIPANTS, QUANT, PRODUCT
- Source statement: 120. Principe final de la partie 4: La question que notre bot doit poser n’est pas : « Qui sont mes concurrents ? »
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `120. Principe final de la partie 4` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0043`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, PARTICIPANTS, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0158 — 1. Rôle général de la couche Quant

- Source: `SRC-007`
- Location: lines 5389–5448; heading `1. Rôle général de la couche Quant`
- Domain tags: QUANT, RISK, ACCOUNTING, SIMULATOR, PARTICIPANTS, SURVIVAL, SIZING, ROUTING
- Source statement: 1. Rôle général de la couche Quant: Notre bot ne doit pas être construit comme : La couche quantitative répond essentiellement à six questions :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `1. Rôle général de la couche Quant` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-QUANT-0010`; supporting items: none found by conservative heading match; domain indexes `QUANT, RISK, ACCOUNTING, SIMULATOR, PARTICIPANTS, SURVIVAL, SIZING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0159 — 2. Architecture Quant recommandée

- Source: `SRC-007`
- Location: lines 5449–5502; heading `2. Architecture Quant recommandée`
- Domain tags: QUANT, ARCH, RISK, SURVIVAL, LIQUIDITY_RESPONSE, MICROSTRUCTURE, INVENTORY, CAPITAL
- Source statement: 2. Architecture Quant recommandée: quant/ fournit les primitives mathématiques et les modèles. Il ne décide pas lui-même de trader. La décision reste dans :
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `2. Architecture Quant recommandée` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-QUANT-0011`; supporting items: none found by conservative heading match; domain indexes `QUANT, ARCH, RISK, SURVIVAL, LIQUIDITY_RESPONSE, MICROSTRUCTURE, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0161 — Où ?

- Source: `SRC-007`
- Location: lines 5504–5514; heading `Où ?`
- Domain tags: ARCH
- Source statement: Où ?: execution/ conversion.rs
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0080`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0162 — Contexte

- Source: `SRC-007`
- Location: lines 5515–5531; heading `Contexte`
- Domain tags: RECOVERY, BRIDGE, OWA, TRIANGLE, CROSS_EXCHANGE
- Source statement: Contexte: À chaque fois que l’on veut savoir : Combien de B recevrais-je réellement
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Contexte` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RECOV-0017`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, BRIDGE, OWA, TRIANGLE, CROSS_EXCHANGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0163 — Formulation

- Source: `SRC-007`
- Location: lines 5532–5613; heading `Formulation`
- Domain tags: RISK, ACCOUNTING, ROUTING
- Source statement: Formulation: Cette fonction doit intégrer : BookWalk + Fees + Precision + Rounding + MinNotional + PriceLimits
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Formulation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0305`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0164 — 4. Book Walk

- Source: `SRC-007`
- Location: lines 5614–5668; heading `4. Book Walk`
- Domain tags: ACCOUNTING
- Source statement: 4. Book Walk: Supposons que nous achetions B avec A. Pour acheter 4 unités :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `4. Book Walk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0055`; supporting items: SRC-004-ITEM-0167, SRC-004-ITEM-0168, SRC-004-ITEM-0277; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0165 — Pourquoi ?

- Source: `SRC-007`
- Location: lines 5669–5676; heading `Pourquoi ?`
- Domain tags: QUANT
- Source statement: Pourquoi ?: serait complètement faux dès que notre quantité dépasse le premier niveau.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Pourquoi ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0012`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0167 — Où ?

- Source: `SRC-007`
- Location: lines 5678–5683; heading `Où ?`
- Domain tags: MICROSTRUCTURE, ROUTING, QUANT
- Source statement: Où ?: quant/microstructure/impact.rs ou directement dans NetConvert.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0011`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0168 — Formule

- Source: `SRC-007`
- Location: lines 5684–5731; heading `Formule`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: Formule: Pour notre exécution immédiate, le best executable price est souvent la référence la plus naturelle.
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Formule` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-FORMULA-0140`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0169 — Utilité

- Source: `SRC-007`
- Location: lines 5732–5742; heading `Utilité`
- Domain tags: RECOVERY, ACCOUNTING, SIMULATOR, CAPITAL, SIZING, ROUTING
- Source statement: Utilité: Le slippage intervient dans :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Utilité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0018`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, ACCOUNTING, SIMULATOR, CAPITAL, SIZING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0170 — 6. Fees

- Source: `SRC-007`
- Location: lines 5743–5821; heading `6. Fees`
- Domain tags: ACCOUNTING, EXECUTION
- Source statement: 6. Fees: Output_{net} = Output_{gross} - Fees ou selon le marché :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `6. Fees` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0056`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0171 — 7. OWA 2 jambes

- Source: `SRC-007`
- Location: lines 5822–5834; heading `7. OWA 2 jambes`
- Domain tags: OWA
- Source statement: 7. OWA 2 jambes: est comparé au direct :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `7. OWA 2 jambes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OWA-0005`; supporting items: none found by conservative heading match; domain indexes `OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0172 — Direct

- Source: `SRC-007`
- Location: lines 5835–5860; heading `Direct`
- Domain tags: ROUTING
- Source statement: Direct: D(q_A) = NetConvert(A,B,q_A)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Direct` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0029`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0173 — Indirect

- Source: `SRC-007`
- Location: lines 5861–5908; heading `Indirect`
- Domain tags: ROUTING
- Source statement: Indirect: q_X = NetConvert(A,X,q_A) I(q_A) = NetConvert(X,B,q_X)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Indirect` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0030`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0174 — Edge

- Source: `SRC-007`
- Location: lines 5909–5934; heading `Edge`
- Domain tags: OWA
- Source statement: Edge: Edge_{OWA}(q_A) = \frac{I(q_A)} {D(q_A)} -1
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Edge` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-OWA-0006`; supporting items: none found by conservative heading match; domain indexes `OWA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0175 — Gain absolu

- Source: `SRC-007`
- Location: lines 5935–5958; heading `Gain absolu`
- Domain tags: ARCH
- Source statement: Gain absolu: Gain_B(q_A) = I(q_A)-D(q_A)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Gain absolu` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0081`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0176 — 8. Où utiliser l’OWA Edge ?

- Source: `SRC-007`
- Location: lines 5959–5980; heading `8. Où utiliser l’OWA Edge ?`
- Domain tags: OWA, QUANT
- Source statement: 8. Où utiliser l’OWA Edge ?: mais les primitives restent dans : Il ne doit pas réimplémenter le carnet.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `8. Où utiliser l’OWA Edge ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OWA-0007`; supporting items: none found by conservative heading match; domain indexes `OWA, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0177 — 9. Important : l’edge est une fonction de la taille

- Source: `SRC-007`
- Location: lines 5981–6030; heading `9. Important : l’edge est une fonction de la taille`
- Domain tags: RISK, ROUTING
- Source statement: 9. Important : l’edge est une fonction de la taille: Il faut toujours penser :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `9. Important : l’edge est une fonction de la taille` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0306`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0178 — 10. Edge Curve

- Source: `SRC-007`
- Location: lines 6031–6083; heading `10. Edge Curve`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE, RESEARCH
- Source statement: 10. Edge Curve: On peut représenter : E(q)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `10. Edge Curve` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0307`; supporting items: SRC-004-ITEM-0184; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0179 — 11. Triangle 3 jambes

- Source: `SRC-007`
- Location: lines 6084–6213; heading `11. Triangle 3 jambes`
- Domain tags: TRIANGLE, RISK, ACCOUNTING, MICROSTRUCTURE, ROUTING
- Source statement: 11. Triangle 3 jambes: est dépendant de la taille.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `11. Triangle 3 jambes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-TRI-0002`; supporting items: none found by conservative heading match; domain indexes `TRIANGLE, RISK, ACCOUNTING, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0180 — 12. Conversion Alpha vs Execution Alpha

- Source: `SRC-007`
- Location: lines 6214–6286; heading `12. Conversion Alpha vs Execution Alpha`
- Domain tags: EXECUTION, ROUTING
- Source statement: 12. Conversion Alpha vs Execution Alpha: Mais si MT nous donne : TotalAlpha = ConversionAlpha + ExecutionAlpha
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `12. Conversion Alpha vs Execution Alpha` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0268`; supporting items: SRC-004-ITEM-0182, SRC-004-ITEM-0183; domain indexes `EXECUTION, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0182 — Où ?

- Source: `SRC-007`
- Location: lines 6288–6298; heading `Où ?`
- Domain tags: RISK, ACCOUNTING, QUANT
- Source statement: Où ?: quant/risk/ execution/ev.rs
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0308`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0183 — Formulation simple

- Source: `SRC-007`
- Location: lines 6299–6399; heading `Formulation simple`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: Formulation simple: EV = \sum_i P_i\times PnL_i EV = P_{full}G_{full} + P_{partial}PnL_{partial} + P_{fail}PnL_{fail}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Formulation simple` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0269`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0184 — 14. Version plus complète

- Source: `SRC-007`
- Location: lines 6400–6480; heading `14. Version plus complète`
- Domain tags: EXECUTION, RECOVERY, INFRA, ACCOUNTING, ROUTING, QUANT, PRODUCT
- Source statement: 14. Version plus complète: EV_{route} = P_{full} E[PnL|full] + P_{partial} E[PnL|partial] + P_{failed} E[PnL|failed] déjà dans les distributions de résultat.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `14. Version plus complète` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0270`; supporting items: SRC-003-ITEM-0149; domain indexes `EXECUTION, RECOVERY, INFRA, ACCOUNTING, ROUTING, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0185 — 15. Pourquoi l’EV est supérieure au simple edge

- Source: `SRC-007`
- Location: lines 6481–6514; heading `15. Pourquoi l’EV est supérieure au simple edge`
- Domain tags: EXECUTION, ACCOUNTING, ROUTING
- Source statement: 15. Pourquoi l’EV est supérieure au simple edge: Le bot doit donc classer les opportunités selon :
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `15. Pourquoi l’EV est supérieure au simple edge` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0271`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0187 — Où ?

- Source: `SRC-007`
- Location: lines 6516–6523; heading `Où ?`
- Domain tags: PARTICIPANTS, SURVIVAL, QUANT
- Source statement: Où ?: participants/edge_survival.rs quant/survival/
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0021`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0188 — Question

- Source: `SRC-007`
- Location: lines 6524–6556; heading `Question`
- Domain tags: SURVIVAL, ARCH
- Source statement: Question: P( \text{edge encore vivant après }t ) T = \text{remaining edge lifetime}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Question` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0017`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0189 — 17. Pourquoi c’est central

- Source: `SRC-007`
- Location: lines 6557–6577; heading `17. Pourquoi c’est central`
- Domain tags: SURVIVAL, ROUTING
- Source statement: 17. Pourquoi c’est central: qui disparaît presque toujours avant notre arrivée peut être moins bonne qu’une : Notre route doit donc transporter :
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `17. Pourquoi c’est central` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SURV-0018`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0190 — 18. Hazard Rate

- Source: `SRC-007`
- Location: lines 6578–6614; heading `18. Hazard Rate`
- Domain tags: SURVIVAL
- Source statement: 18. Hazard Rate: représente la vitesse instantanée de disparition.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `18. Hazard Rate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0019`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0191 — 19. Edge Half-Life

- Source: `SRC-007`
- Location: lines 6615–6643; heading `19. Edge Half-Life`
- Domain tags: SURVIVAL, OPERATIONS, ROUTING
- Source statement: 19. Edge Half-Life: Cela ne remplace pas la courbe entière mais donne une excellente métrique synthétique.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `19. Edge Half-Life` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0020`; supporting items: SRC-004-ITEM-0207; domain indexes `SURVIVAL, OPERATIONS, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0192 — 20. Lien Survival × infrastructure

- Source: `SRC-007`
- Location: lines 6644–6687; heading `20. Lien Survival × infrastructure`
- Domain tags: INFRA, SURVIVAL, RISK, QUANT, PRODUCT
- Source statement: 20. Lien Survival × infrastructure: Nous avons une distribution réelle de latence : La probabilité d’arriver avant disparition est :
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `20. Lien Survival × infrastructure` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0044`; supporting items: none found by conservative heading match; domain indexes `INFRA, SURVIVAL, RISK, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0193 — 21. Exemple

- Source: `SRC-007`
- Location: lines 6688–6717; heading `21. Exemple`
- Domain tags: INFRA, BENCHMARK, QUANT
- Source statement: 21. Exemple: Même si la moyenne est proche, B peut considérablement améliorer : sur des edges très courts.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `21. Exemple` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0045`; supporting items: none found by conservative heading match; domain indexes `INFRA, BENCHMARK, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0194 — 22. Expected Edge at Arrival

- Source: `SRC-007`
- Location: lines 6718–6757; heading `22. Expected Edge at Arrival`
- Domain tags: BENCHMARK, PRODUCT, ARCH
- Source statement: 22. Expected Edge at Arrival: Encore plus important que la survie binaire : On veut une distribution :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `22. Expected Edge at Arrival` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0007`; supporting items: SRC-004-ITEM-0209, SRC-005-ITEM-0051; domain indexes `BENCHMARK, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0196 — Où ?

- Source: `SRC-007`
- Location: lines 6759–6805; heading `Où ?`
- Domain tags: FORMULA, MICROSTRUCTURE, INVENTORY, QUANT
- Source statement: Où ?: quant/microstructure/imbalance.rs Formule simple :
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-FORMULA-0141`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0197 — 24. Où utiliser QI ?

- Source: `SRC-007`
- Location: lines 6806–6826; heading `24. Où utiliser QI ?`
- Domain tags: EXECUTION, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, MAKER_MODEL, FUTURE
- Source statement: 24. Où utiliser QI ?: Pas comme signal autonome de trading. si nous voulons acheter et :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `24. Où utiliser QI ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0272`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PARTICIPANTS, SURVIVAL, LIQUIDITY_RESPONSE, MAKER_MODEL, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0199 — Où ?

- Source: `SRC-007`
- Location: lines 6828–6868; heading `Où ?`
- Domain tags: EXECUTION, RISK, MICROSTRUCTURE, QUANT, PRODUCT
- Source statement: Où ?: OFI est beaucoup plus intéressant qu’un simple : buy volume - sell volume
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0273`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, MICROSTRUCTURE, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0200 — 26. Multi-Level OFI

- Source: `SRC-007`
- Location: lines 6869–6926; heading `26. Multi-Level OFI`
- Domain tags: MICROSTRUCTURE, ROUTING
- Source statement: 26. Multi-Level OFI: Si une route nécessite 4 niveaux : ne représente pas vraiment notre risque.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `26. Multi-Level OFI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-MICRO-0012`; supporting items: SRC-004-ITEM-0187, SRC-004-ITEM-0192; domain indexes `MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0201 — 27. Utilisation de l’OFI

- Source: `SRC-007`
- Location: lines 6927–6959; heading `27. Utilisation de l’OFI`
- Domain tags: MICROSTRUCTURE, PARTICIPANTS, CROSS_MARKET, QUANT, FUTURE
- Source statement: 27. Utilisation de l’OFI: Il nous aide à estimer : P( Book_{future} | Book_{now} )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `27. Utilisation de l’OFI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-MICRO-0013`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, PARTICIPANTS, CROSS_MARKET, QUANT, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0203 — Où ?

- Source: `SRC-007`
- Location: lines 6961–7021; heading `Où ?`
- Domain tags: MICROSTRUCTURE, QUANT
- Source statement: Où ?: MicroPrice = \frac{ Ask\times Q_{bid} + Bid\times Q_{ask} }{ Q_{bid}+Q_{ask} } le prix est légèrement déplacé vers le côté susceptible d’être traversé.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-MICRO-0014`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0204 — 29. Pourquoi Microprice ?

- Source: `SRC-007`
- Location: lines 7022–7031; heading `29. Pourquoi Microprice ?`
- Domain tags: MICROSTRUCTURE, EXECUTION
- Source statement: 29. Pourquoi Microprice ?: Principalement comme feature de : Pas comme prix « juste » absolu.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `29. Pourquoi Microprice ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-MICRO-0015`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0206 — Où ?

- Source: `SRC-007`
- Location: lines 7033–7072; heading `Où ?`
- Domain tags: QUANT
- Source statement: Où ?: r_t = \ln \left( \frac{P_t}{P_{t-1}} \right)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0013`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0207 — 31. Horizons multiples

- Source: `SRC-007`
- Location: lines 7073–7091; heading `31. Horizons multiples`
- Domain tags: ACCOUNTING
- Source statement: 31. Horizons multiples: Nous avons besoin de plusieurs horizons : mais les horizons seront calibrés selon la fidélité réelle du feed.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `31. Horizons multiples` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ACCT-0057`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0208 — 32. Pourquoi la volatilité ?

- Source: `SRC-007`
- Location: lines 7092–7105; heading `32. Pourquoi la volatilité ?`
- Domain tags: RECOVERY, RISK, SURVIVAL, INVENTORY, SIZING, BRIDGE, QUANT
- Source statement: 32. Pourquoi la volatilité ?: Elle ne sert pas principalement à prévoir une tendance.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `32. Pourquoi la volatilité ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0019`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, RISK, SURVIVAL, INVENTORY, SIZING, BRIDGE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0209 — 33. Jump Risk

- Source: `SRC-007`
- Location: lines 7106–7131; heading `33. Jump Risk`
- Domain tags: RISK, QUANT
- Source statement: 33. Jump Risk: La variance seule peut masquer les gros mouvements.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `33. Jump Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0309`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0210 — 34. Impact

- Source: `SRC-007`
- Location: lines 7132–7133; heading `34. Impact`
- Domain tags: QUANT
- Source statement: 34. Impact: Deux types différents.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `34. Impact` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0014`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0211 — Mechanical Impact

- Source: `SRC-007`
- Location: lines 7134–7142; heading `Mechanical Impact`
- Domain tags: QUANT
- Source statement: Mechanical Impact: Notre ordre consomme réellement :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Mechanical Impact` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0015`; supporting items: SRC-004-ITEM-0202, SRC-008-ITEM-0006; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0212 — Response Impact

- Source: `SRC-007`
- Location: lines 7143–7147; heading `Response Impact`
- Domain tags: QUANT
- Source statement: Response Impact: Le marché réagit ensuite. Probabiliste.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Response Impact` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0016`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0213 — 35. Depth Participation

- Source: `SRC-007`
- Location: lines 7148–7184; heading `35. Depth Participation`
- Domain tags: QUANT
- Source statement: 35. Depth Participation: Cette variable aide à déterminer :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `35. Depth Participation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0017`; supporting items: SRC-004-ITEM-0199; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0214 — 36. Volume Participation

- Source: `SRC-007`
- Location: lines 7185–7217; heading `36. Volume Participation`
- Domain tags: EXECUTION
- Source statement: 36. Volume Participation: Si notre ordre représente une fraction énorme du volume récent : doit devenir beaucoup plus prudent.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `36. Volume Participation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0274`; supporting items: SRC-004-ITEM-0200, SRC-005-ITEM-0046; domain indexes `EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0215 — 37. Out-of-Distribution

- Source: `SRC-007`
- Location: lines 7218–7236; heading `37. Out-of-Distribution`
- Domain tags: PRODUCT, EXECUTION
- Source statement: 37. Out-of-Distribution: Le modèle doit savoir quand il ne sait pas.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `37. Out-of-Distribution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-PRODUCT-0020`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, EXECUTION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0216 — 38. Liquidity Resilience

- Source: `SRC-007`
- Location: lines 7237–7301; heading `38. Liquidity Resilience`
- Domain tags: LIQUIDITY_RESPONSE
- Source statement: 38. Liquidity Resilience: R(t) = \frac{ D(t)-D_s }{ D_0-D_s }
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `38. Liquidity Resilience` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0007`; supporting items: SRC-004-ITEM-0203; domain indexes `LIQUIDITY_RESPONSE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0217 — 39. Pourquoi ?

- Source: `SRC-007`
- Location: lines 7302–7325; heading `39. Pourquoi ?`
- Domain tags: LIQUIDITY_RESPONSE
- Source statement: 39. Pourquoi ?: Cela détermine s’il est intéressant de fractionner. 80 % replenished in 200ms
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `39. Pourquoi ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-LIQ-0008`; supporting items: none found by conservative heading match; domain indexes `LIQUIDITY_RESPONSE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0218 — 40. Optimal Slicing

- Source: `SRC-007`
- Location: lines 7326–7416; heading `40. Optimal Slicing`
- Domain tags: SLICING, EXECUTION, SURVIVAL, LIQUIDITY_RESPONSE, QUANT
- Source statement: 40. Optimal Slicing: On veut optimiser simultanément : SliceInterval^* = \arg\max_{\Delta t} EV( Replenishment(\Delta t), Survival(\Delta t) )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `40. Optimal Slicing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SLICE-0004`; supporting items: none found by conservative heading match; domain indexes `SLICING, EXECUTION, SURVIVAL, LIQUIDITY_RESPONSE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0220 — Où ?

- Source: `SRC-007`
- Location: lines 7418–7449; heading `Où ?`
- Domain tags: EXECUTION, PARTICIPANTS
- Source statement: Où ?: P( T_{fill}\leq t | X )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0275`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PARTICIPANTS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0221 — 42. Fill Probability n’est pas suffisante

- Source: `SRC-007`
- Location: lines 7450–7493; heading `42. Fill Probability n’est pas suffisante`
- Domain tags: EXECUTION, QUANT
- Source statement: 42. Fill Probability n’est pas suffisante: Alors notre maker est toxique. E[ AdverseMove | fill ]
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `42. Fill Probability n’est pas suffisante` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0276`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0222 — 43. Adverse Selection

- Source: `SRC-007`
- Location: lines 7494–7544; heading `43. Adverse Selection`
- Domain tags: MAKER_MODEL, EXECUTION, PRODUCT
- Source statement: 43. Adverse Selection: AS(h) = P_{fill} - Mid_{t+h} AS_{bps} = \frac{ P_{fill}-Mid_{t+h} }{ P_{fill} } \times10^4
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `43. Adverse Selection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-MAKER-0001`; supporting items: SRC-004-ITEM-0214, SRC-004-ITEM-0215, SRC-006-ITEM-0346, SRC-008-ITEM-0035; domain indexes `MAKER_MODEL, EXECUTION, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0223 — 44. EV Maker

- Source: `SRC-007`
- Location: lines 7545–7673; heading `44. EV Maker`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING
- Source statement: 44. EV Maker: EV_{maker} = MakerBenefit - ExpectedAdverseSelection - FailedHedgeRisk - OpportunityCost EV_{MT} = \int f_{fill}(t) EV_{leg2}(t) dt - AS - RecoveryRisk
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `44. EV Maker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0277`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0225 — Où ?

- Source: `SRC-007`
- Location: lines 7675–7699; heading `Où ?`
- Domain tags: RISK, QUANT, PRODUCT
- Source statement: Où ?: est notre distribution de perte : est le quantile de perte au niveau
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0310`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0226 — 46. Pourquoi VaR n’est pas suffisante

- Source: `SRC-007`
- Location: lines 7700–7712; heading `46. Pourquoi VaR n’est pas suffisante`
- Domain tags: RISK, MICROSTRUCTURE
- Source statement: 46. Pourquoi VaR n’est pas suffisante: à quel point cette queue est mauvaise C’est pourquoi la CVaR est plus importante pour nous.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `46. Pourquoi VaR n’est pas suffisante` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0311`; supporting items: none found by conservative heading match; domain indexes `RISK, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0227 — 47. CVaR

- Source: `SRC-007`
- Location: lines 7713–7740; heading `47. CVaR`
- Domain tags: RISK
- Source statement: 47. CVaR: CVaR_\alpha = E[ Loss | Loss\geq VaR_\alpha ] lorsque nous tombons dans les pires cas, quelle est la perte moyenne ?
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `47. CVaR` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0312`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0228 — 48. Utilisation de CVaR

- Source: `SRC-007`
- Location: lines 7741–7773; heading `48. Utilisation de CVaR`
- Domain tags: RISK, SIZING
- Source statement: 48. Utilisation de CVaR: Le deuxième trade gagne davantage en moyenne mais peut être refusé.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `48. Utilisation de CVaR` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0313`; supporting items: none found by conservative heading match; domain indexes `RISK, SIZING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0229 — 49. Expected Shortfall par route

- Source: `SRC-007`
- Location: lines 7774–7793; heading `49. Expected Shortfall par route`
- Domain tags: ROUTING, RISK, ARCH
- Source statement: 49. Expected Shortfall par route: On peut également comparer : Mais ne pas transformer ça automatiquement en unique score.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `49. Expected Shortfall par route` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0031`; supporting items: none found by conservative heading match; domain indexes `ROUTING, RISK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0231 — Où ?

- Source: `SRC-007`
- Location: lines 7795–7831; heading `Où ?`
- Domain tags: EXECUTION, RECOVERY, INFRA, ACCOUNTING, SIMULATOR, LIQUIDITY_RESPONSE, CROSS_MARKET, ROUTING
- Source statement: Où ?: Pas forcément dans le hot path live.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0278`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, INFRA, ACCOUNTING, SIMULATOR, LIQUIDITY_RESPONSE, CROSS_MARKET, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0232 — 51. Sorties Monte Carlo

- Source: `SRC-007`
- Location: lines 7832–7887; heading `51. Sorties Monte Carlo`
- Domain tags: SIMULATOR, EXECUTION, RECOVERY, RISK, ACCOUNTING
- Source statement: 51. Sorties Monte Carlo: E[PnL] Median(PnL)
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `51. Sorties Monte Carlo` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-SIM-0006`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, EXECUTION, RECOVERY, RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0233 — 52. Monte Carlo : optimisation

- Source: `SRC-007`
- Location: lines 7888–7907; heading `52. Monte Carlo : optimisation`
- Domain tags: SIMULATOR, DEPLOYMENT, REPLAY, QUANT, RESEARCH
- Source statement: 52. Monte Carlo : optimisation: Ne surtout pas lancer : pour chaque market update live.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `52. Monte Carlo : optimisation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0007`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, DEPLOYMENT, REPLAY, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0235 — Où ?

- Source: `SRC-007`
- Location: lines 7909–7942; heading `Où ?`
- Domain tags: RISK, SIZING, QUANT
- Source statement: Où ?: quant/optimization/sizing.rs Le problème :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0314`; supporting items: none found by conservative heading match; domain indexes `RISK, SIZING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0236 — 54. Contraintes de sizing

- Source: `SRC-007`
- Location: lines 7943–8086; heading `54. Contraintes de sizing`
- Domain tags: SIZING, RISK, ACCOUNTING, INVENTORY, CAPITAL, ROUTING, QUANT
- Source statement: 54. Contraintes de sizing: q\leq AvailableBalance q\leq RouteCapacity
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `54. Contraintes de sizing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIZE-0003`; supporting items: SRC-003-ITEM-0156; domain indexes `SIZING, RISK, ACCOUNTING, INVENTORY, CAPITAL, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0237 — 55. Validated Capacity

- Source: `SRC-007`
- Location: lines 8087–8107; heading `55. Validated Capacity`
- Domain tags: CAPITAL, SIZING, RISK
- Source statement: 55. Validated Capacity: Donc notre vraie capacité : est la plus grande taille satisfaisant toutes les conditions.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `55. Validated Capacity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0018`; supporting items: SRC-004-ITEM-0236; domain indexes `CAPITAL, SIZING, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0238 — 56. Search de q*

- Source: `SRC-007`
- Location: lines 8108–8132; heading `56. Search de q*`
- Domain tags: ACCOUNTING
- Source statement: 56. Search de q*: Comme notre fonction de PnL peut être non linéaire et non lisse à cause du carnet : pas besoin de dérivée analytique
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `56. Search de q*` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0058`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0239 — 57. Opportunity Portfolio Optimization

- Source: `SRC-007`
- Location: lines 8133–8148; heading `57. Opportunity Portfolio Optimization`
- Domain tags: PORTFOLIO
- Source statement: 57. Opportunity Portfolio Optimization: Si plusieurs opportunités arrivent ensemble :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `57. Opportunity Portfolio Optimization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PORT-0001`; supporting items: none found by conservative heading match; domain indexes `PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0240 — 58. Contraintes portefeuille

- Source: `SRC-007`
- Location: lines 8149–8267; heading `58. Contraintes portefeuille`
- Domain tags: RISK, INVENTORY, CAPITAL, PORTFOLIO, ROUTING, FUTURE
- Source statement: 58. Contraintes portefeuille: \sum_{i\in routes(book_j)} Consumption_{ij} \leq AvailableDepth_j
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `58. Contraintes portefeuille` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0315`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, CAPITAL, PORTFOLIO, ROUTING, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0241 — 59. Pourquoi ?

- Source: `SRC-007`
- Location: lines 8268–8283; heading `59. Pourquoi ?`
- Domain tags: EXECUTION, RISK, PORTFOLIO, ROUTING
- Source statement: 59. Pourquoi ?: A et B utilisent exactement le même HYPE ask. Prendre les deux à pleine taille :
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `59. Pourquoi ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0279`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, PORTFOLIO, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0242 — 60. Balance Reservation

- Source: `SRC-007`
- Location: lines 8284–8378; heading `60. Balance Reservation`
- Domain tags: INVENTORY, ROUTING
- Source statement: 60. Balance Reservation: Quand une route est sélectionnée : AvailableBalance = ActualBalance - ReservedBalance
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `60. Balance Reservation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0020`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0243 — 61. Inventory Penalty

- Source: `SRC-007`
- Location: lines 8379–8447; heading `61. Inventory Penalty`
- Domain tags: INVENTORY, RISK, ROUTING, ARCH
- Source statement: 61. Inventory Penalty: Si nous détenons trop de B : une route qui produit encore plus de B doit devenir moins attractive.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `61. Inventory Penalty` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INV-0021`; supporting items: SRC-004-ITEM-0225; domain indexes `INVENTORY, RISK, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0244 — 62. Pourquoi quadratique ?

- Source: `SRC-007`
- Location: lines 8448–8461; heading `62. Pourquoi quadratique ?`
- Domain tags: ARCH
- Source statement: 62. Pourquoi quadratique ?: Près de la cible : Mais cette forme doit être calibrée.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `62. Pourquoi quadratique ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ARCH-0082`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0245 — 63. Portfolio Adjusted EV

- Source: `SRC-007`
- Location: lines 8462–8557; heading `63. Portfolio Adjusted EV`
- Domain tags: PORTFOLIO, INVENTORY, CAPITAL
- Source statement: 63. Portfolio Adjusted EV: PortfolioAdjustedEV = ExecutionEV - InventoryPenalty - StrandedCapitalPenalty + RebalanceValue ne doit pas transformer artificiellement un trade perdant en « arbitrage rentable ».
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `63. Portfolio Adjusted EV` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PORT-0002`; supporting items: none found by conservative heading match; domain indexes `PORTFOLIO, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0246 — 64. Stranded Capital Penalty

- Source: `SRC-007`
- Location: lines 8558–8633; heading `64. Stranded Capital Penalty`
- Domain tags: INVENTORY, CAPITAL, RISK, ACCOUNTING, ROUTING
- Source statement: 64. Stranded Capital Penalty: Supposons qu’une route nous laisse dans un token très difficile à ressortir. StrandedPenalty = ExpectedExitCost + ExpectedIdleCapitalCost + RiskCost
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `64. Stranded Capital Penalty` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0022`; supporting items: SRC-004-ITEM-0229; domain indexes `INVENTORY, CAPITAL, RISK, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0247 — 65. Bridge Optimization

- Source: `SRC-007`
- Location: lines 8634–8701; heading `65. Bridge Optimization`
- Domain tags: BRIDGE, RISK, ACCOUNTING, CAPITAL
- Source statement: 65. Bridge Optimization: Pour déplacer le capital : BridgeCost = Fees + Spread + Slippage + ExpectedMarketRisk
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `65. Bridge Optimization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BRIDGE-0011`; supporting items: none found by conservative heading match; domain indexes `BRIDGE, RISK, ACCOUNTING, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0248 — 66. Break-even Cycles

- Source: `SRC-007`
- Location: lines 8702–8781; heading `66. Break-even Cycles`
- Domain tags: BRIDGE, ROUTING, EXECUTION, ACCOUNTING
- Source statement: 66. Break-even Cycles: BreakEvenCycles = \frac{ BridgeCost + ExpectedExitCost }{ MeanNetPnLPerCycle } nécessaires juste pour rembourser le déplacement.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `66. Break-even Cycles` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BRIDGE-0012`; supporting items: SRC-004-ITEM-0231; domain indexes `BRIDGE, ROUTING, EXECUTION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0249 — 67. Capital Relocation EV

- Source: `SRC-007`
- Location: lines 8782–8876; heading `67. Capital Relocation EV`
- Domain tags: CAPITAL, BRIDGE, RISK, ACCOUNTING
- Source statement: 67. Capital Relocation EV: Value(move) = EV_{destination} - BridgeCost - ExitCost - RiskCost - EV_{stay} On déplace uniquement si :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `67. Capital Relocation EV` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0019`; supporting items: SRC-002-ITEM-0108, SRC-004-ITEM-0232; domain indexes `CAPITAL, BRIDGE, RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0250 — 68. Opportunity Cost

- Source: `SRC-007`
- Location: lines 8877–8917; heading `68. Opportunity Cost`
- Domain tags: ACCOUNTING, CAPITAL, ROUTING
- Source statement: 68. Opportunity Cost: Si le capital est immobilisé dans une route A : pondéré par la durée d’immobilisation.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `68. Opportunity Cost` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0059`; supporting items: SRC-001-ITEM-0034; domain indexes `ACCOUNTING, CAPITAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0252 — Où ?

- Source: `SRC-007`
- Location: lines 8919–8961; heading `Où ?`
- Domain tags: PARTICIPANTS, CROSS_MARKET
- Source statement: Où ?: P( \Delta Market_j(h) | Shock_i,X )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0022`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0253 — 70. Usage

- Source: `SRC-007`
- Location: lines 8962–8974; heading `70. Usage`
- Domain tags: PARTICIPANTS, TRIANGLE, QUANT
- Source statement: 70. Usage: notre Leg1 BTC/HYPE peut être suivi d’une réaction sur les deux autres marchés. Par réaction des autres participants.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `70. Usage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0023`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, TRIANGLE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0254 — 71. Cross-impact n’est pas forcément causal

- Source: `SRC-007`
- Location: lines 8975–8988; heading `71. Cross-impact n’est pas forcément causal`
- Domain tags: QUANT, VALIDATION, PORTFOLIO
- Source statement: 71. Cross-impact n’est pas forcément causal: sert à découvrir des candidats. Ne jamais mettre une relation en prod simplement parce que :
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `71. Cross-impact n’est pas forcément causal` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0018`; supporting items: none found by conservative heading match; domain indexes `QUANT, VALIDATION, PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0256 — Où ?

- Source: `SRC-007`
- Location: lines 8990–9022; heading `Où ?`
- Domain tags: QUANT, PRODUCT, ARCH, FUTURE
- Source statement: Où ?: mais challenger, pas core V1. \lambda(t) = \mu + \sum_{t_i<t} \alpha e^{-\beta(t-t_i)}
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-QUANT-0019`; supporting items: none found by conservative heading match; domain indexes `QUANT, PRODUCT, ARCH, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0257 — 73. Usage potentiel

- Source: `SRC-007`
- Location: lines 9023–9034; heading `73. Usage potentiel`
- Domain tags: EXECUTION, PARTICIPANTS, LIQUIDITY_RESPONSE, CROSS_MARKET
- Source statement: 73. Usage potentiel: market order bursts cancel cascades
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `73. Usage potentiel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0280`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PARTICIPANTS, LIQUIDITY_RESPONSE, CROSS_MARKET`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0258 — 74. Quand utiliser Hawkes ?

- Source: `SRC-007`
- Location: lines 9035–9058; heading `74. Quand utiliser Hawkes ?`
- Domain tags: QUANT, ACCOUNTING, REPLAY, SURVIVAL, FUTURE
- Source statement: 74. Quand utiliser Hawkes ?: ne prédit pas suffisamment bien les événements.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `74. Quand utiliser Hawkes ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-QUANT-0020`; supporting items: none found by conservative heading match; domain indexes `QUANT, ACCOUNTING, REPLAY, SURVIVAL, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0259 — 75. Queue-Reactive

- Source: `SRC-007`
- Location: lines 9059–9103; heading `75. Queue-Reactive`
- Domain tags: MICROSTRUCTURE, EXECUTION, LIQUIDITY_RESPONSE, FUTURE
- Source statement: 75. Queue-Reactive: On modélise les intensités :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `75. Queue-Reactive` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-MICRO-0016`; supporting items: SRC-008-ITEM-0017; domain indexes `MICROSTRUCTURE, EXECUTION, LIQUIDITY_RESPONSE, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0260 — 76. Pourquoi pas tout de suite ?

- Source: `SRC-007`
- Location: lines 9104–9112; heading `76. Pourquoi pas tout de suite ?`
- Domain tags: ACCOUNTING
- Source statement: 76. Pourquoi pas tout de suite ?: Parce qu’avec L2 public coarse : Donc modèle trop sophistiqué avec mauvaises données = illusion de précision.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `76. Pourquoi pas tout de suite ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0060`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0261 — 77. Drawdown

- Source: `SRC-007`
- Location: lines 9113–9162; heading `77. Drawdown`
- Domain tags: RISK, ACCOUNTING, PARTICIPANTS, INVENTORY
- Source statement: 77. Drawdown: Même si notre stratégie est très court terme, il faut suivre : DD_t = PeakEquity_t - Equity_t
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `77. Drawdown` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0316`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, PARTICIPANTS, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0262 — 78. Sharpe Ratio ?

- Source: `SRC-007`
- Location: lines 9163–9200; heading `78. Sharpe Ratio ?`
- Domain tags: EXECUTION, RECOVERY, RISK, ACCOUNTING, CAPITAL
- Source statement: 78. Sharpe Ratio ?: On peut le calculer : Sharpe = \frac{ E[R]-R_f }{ \sigma_R }
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `78. Sharpe Ratio ?` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0281`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, ACCOUNTING, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0263 — 79. Sortino

- Source: `SRC-007`
- Location: lines 9201–9242; heading `79. Sortino`
- Domain tags: ARCH, RESEARCH
- Source statement: 79. Sortino: Sortino = \frac{ E[R]-R_f }{ DownsideDeviation } Un peu plus intéressant car il pénalise principalement les mauvais mouvements.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `79. Sortino` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0083`; supporting items: none found by conservative heading match; domain indexes `ARCH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0264 — 80. Kelly Criterion ?

- Source: `SRC-007`
- Location: lines 9243–9268; heading `80. Kelly Criterion ?`
- Domain tags: FORMULA, RISK, INVENTORY, QUANT, PRODUCT
- Source statement: 80. Kelly Criterion ?: Je ne l’utiliserais pas directement pour dimensionner notre bot. ne sont pas Bernoulli simples
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `80. Kelly Criterion ?` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0142`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, INVENTORY, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0265 — 81. Usage éventuel de Kelly

- Source: `SRC-007`
- Location: lines 9269–9294; heading `81. Usage éventuel de Kelly`
- Domain tags: RISK, INVENTORY, SIZING, QUANT
- Source statement: 81. Usage éventuel de Kelly: ou version fractional Kelly très conservatrice. Mais notre sizing principal reste :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `81. Usage éventuel de Kelly` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0317`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, SIZING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0266 — 82. Bayesian Updating

- Source: `SRC-007`
- Location: lines 9295–9316; heading `82. Bayesian Updating`
- Domain tags: EXECUTION, FUTURE
- Source statement: 82. Bayesian Updating: Les dernières heures montrent : au lieu de jeter brutalement tout l’historique.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `82. Bayesian Updating` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0282`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0267 — 83. Où ?

- Source: `SRC-007`
- Location: lines 9317–9331; heading `83. Où ?`
- Domain tags: PARTICIPANTS, QUANT, PRODUCT
- Source statement: 83. Où ?: Pas nécessaire dans la toute première V1.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `83. Où ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PART-0024`; supporting items: none found by conservative heading match; domain indexes `PARTICIPANTS, QUANT, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0268 — 84. Confidence Intervals

- Source: `SRC-007`
- Location: lines 9332–9355; heading `84. Confidence Intervals`
- Domain tags: BENCHMARK, ACCOUNTING, SIMULATOR, QUANT
- Source statement: 84. Confidence Intervals: Toute prédiction doit idéalement avoir : C’est exactement pourquoi Monte Carlo et quantiles sont importants.
- Nature: rationale
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `84. Confidence Intervals` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BENCH-0008`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, ACCOUNTING, SIMULATOR, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0269 — 85. Lower Confidence Bound

- Source: `SRC-007`
- Location: lines 9356–9398; heading `85. Lower Confidence Bound`
- Domain tags: INFRA, DEPLOYMENT, CAPITAL, BRIDGE, ROUTING
- Source statement: 85. Lower Confidence Bound: Très utile pour prendre une décision conservatrice. LCB = Estimate - k\times Uncertainty
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `85. Lower Confidence Bound` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-INFRA-0046`; supporting items: none found by conservative heading match; domain indexes `INFRA, DEPLOYMENT, CAPITAL, BRIDGE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0270 — 86. Infrastructure ROI

- Source: `SRC-007`
- Location: lines 9399–9474; heading `86. Infrastructure ROI`
- Domain tags: INFRA, ACCOUNTING, QUANT
- Source statement: 86. Infrastructure ROI: Déjà étudié mais à intégrer à cette couche quantitative. NetPnL_s = TradingPnL_s - InfraCost_s
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `86. Infrastructure ROI` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0047`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0271 — 87. ROI incrémental

- Source: `SRC-007`
- Location: lines 9475–9541; heading `87. ROI incrémental`
- Domain tags: INFRA, ACCOUNTING, QUANT
- Source statement: 87. ROI incrémental: InfraROI = \frac{ \Delta GrossPnL }{ \Delta InfraCost } LCB(\Delta GrossPnL) > SafetyFactor \times \Delta Cost
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `87. ROI incrémental` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0048`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0272 — 88. Simulation Confidence

- Source: `SRC-007`
- Location: lines 9542–9635; heading `88. Simulation Confidence`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 88. Simulation Confidence: Créer une vraie métrique : Confidence = f( DataQuality, OOD, SampleSize, ModelAgreement, LatencyUncertainty, FeedFreshness )
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `88. Simulation Confidence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0049`; supporting items: SRC-004-ITEM-0264, SRC-008-ITEM-0049; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0273 — 89. Exemple

- Source: `SRC-007`
- Location: lines 9636–9654; heading `89. Exemple`
- Domain tags: ACCOUNTING, QUANT
- Source statement: 89. Exemple: Sample support HIGH Feed freshness HIGH
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `89. Exemple` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0061`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0274 — 90. Model Disagreement

- Source: `SRC-007`
- Location: lines 9655–9690; heading `90. Model Disagreement`
- Domain tags: SURVIVAL, QUANT
- Source statement: 90. Model Disagreement: Le désaccord peut devenir :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `90. Model Disagreement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0021`; supporting items: SRC-004-ITEM-0262, SRC-005-ITEM-0056; domain indexes `SURVIVAL, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0275 — 91. Risk Adjusted EV

- Source: `SRC-007`
- Location: lines 9691–9825; heading `91. Risk Adjusted EV`
- Domain tags: RISK, FORMULA, INFRA, ACCOUNTING, INVENTORY, ROUTING
- Source statement: 91. Risk Adjusted EV: On arrive à une formule centrale : RiskAdjustedEV = ExpectedPnL - TailRiskPenalty - InventoryPenalty - ModelUncertaintyPenalty - InfrastructurePenalty
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `91. Risk Adjusted EV` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0318`; supporting items: SRC-004-ITEM-0223; domain indexes `RISK, FORMULA, INFRA, ACCOUNTING, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0276 — 92. Attention au double comptage

- Source: `SRC-007`
- Location: lines 9826–9856; heading `92. Attention au double comptage`
- Domain tags: EXECUTION, ACCOUNTING, QUANT, PRODUCT, ARCH
- Source statement: 92. Attention au double comptage: intègre déjà la distribution de slippage : ne pas retirer ensuite :
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `92. Attention au double comptage` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0283`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, QUANT, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0277 — 93. Cela implique un Accounting Schema strict

- Source: `SRC-007`
- Location: lines 9857–9881; heading `93. Cela implique un Accounting Schema strict`
- Domain tags: DATA, ACCOUNTING, EXECUTION, RECOVERY, RISK, PARTICIPANTS, INVENTORY, ROUTING
- Source statement: 93. Cela implique un Accounting Schema strict: Ainsi nous savons exactement pourquoi la route passe ou non.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `93. Cela implique un Accounting Schema strict` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0319`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, EXECUTION, RECOVERY, RISK, PARTICIPANTS, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0278 — 94. Black-Scholes

- Source: `SRC-007`
- Location: lines 9882–9905; heading `94. Black-Scholes`
- Domain tags: MICROSTRUCTURE, ARCH
- Source statement: 94. Black-Scholes: Dans notre architecture actuelle :
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `94. Black-Scholes` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0017`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0279 — 95. Si options futures

- Source: `SRC-007`
- Location: lines 9906–9917; heading `95. Si options futures`
- Domain tags: FUTURE, EXECUTION, QUANT, ARCH
- Source statement: 95. Si options futures: Mais uniquement lorsqu’une stratégie options existe réellement.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `95. Si options futures` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0011`; supporting items: none found by conservative heading match; domain indexes `FUTURE, EXECUTION, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0280 — 96. Perps futurs

- Source: `SRC-007`
- Location: lines 9918–9970; heading `96. Perps futurs`
- Domain tags: INVENTORY, QUANT, CROSS_EXCHANGE
- Source statement: 96. Perps futurs: Plus probable que les options pour nous. Si nous utilisons des perps pour couvrir inventory/cross-exchange :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `96. Perps futurs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-INV-0023`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, QUANT, CROSS_EXCHANGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0281 — 97. Funding

- Source: `SRC-007`
- Location: lines 9971–10094; heading `97. Funding`
- Domain tags: RECOVERY, ACCOUNTING, CROSS_EXCHANGE, FUTURE
- Source statement: 97. Funding: ExpectedFundingCost = PositionNotional \times ExpectedFundingRate \times HoldingPeriods HedgedPnL = SpotPnL + PerpPnL - Funding - Fees - Slippage
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `97. Funding` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RECOV-0020`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, ACCOUNTING, CROSS_EXCHANGE, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0282 — 98. Hedge Ratio

- Source: `SRC-007`
- Location: lines 10095–10131; heading `98. Hedge Ratio`
- Domain tags: RECOVERY, RISK, FUTURE
- Source statement: 98. Hedge Ratio: Si nous voulons couvrir : on peut commencer par :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `98. Hedge Ratio` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RECOV-0021`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, RISK, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0283 — 99. Ce qu’on doit calculer en HOT PATH

- Source: `SRC-007`
- Location: lines 10132–10165; heading `99. Ce qu’on doit calculer en HOT PATH`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH, RISK, BENCHMARK, ACCOUNTING, SURVIVAL, MICROSTRUCTURE
- Source statement: 99. Ce qu’on doit calculer en HOT PATH: Très important pour la performance.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `99. Ce qu’on doit calculer en HOT PATH` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-ROUTE-0032`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH, RISK, BENCHMARK, ACCOUNTING, SURVIVAL, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0284 — 100. Ce qu’on ne calcule PAS dans le hot path

- Source: `SRC-007`
- Location: lines 10166–10182; heading `100. Ce qu’on ne calcule PAS dans le hot path`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH, VALIDATION, SIMULATOR, REPLAY, QUANT, RESEARCH
- Source statement: 100. Ce qu’on ne calcule PAS dans le hot path: R&D / offline / replay / background research pipeline
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `100. Ce qu’on ne calcule PAS dans le hot path` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0033`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH, VALIDATION, SIMULATOR, REPLAY, QUANT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0285 — 101. Pré-calculs

- Source: `SRC-007`
- Location: lines 10183–10204; heading `101. Pré-calculs`
- Domain tags: RISK, ACCOUNTING, SURVIVAL, ROUTING, QUANT
- Source statement: 101. Pré-calculs: Pour réduire la latence : Même chose pour certains modèles :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `101. Pré-calculs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0319`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, SURVIVAL, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0286 — 102. Incremental computation

- Source: `SRC-007`
- Location: lines 10205–10225; heading `102. Incremental computation`
- Domain tags: MICROSTRUCTURE, INVENTORY, QUANT
- Source statement: 102. Incremental computation: ne pas recalculer 10 minutes d’historique. calcul direct sur state actuel.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `102. Incremental computation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0018`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0287 — 103. SIMD / optimisation prématurée

- Source: `SRC-007`
- Location: lines 10226–10237; heading `103. SIMD / optimisation prématurée`
- Domain tags: RISK, MICROSTRUCTURE
- Source statement: 103. SIMD / optimisation prématurée: Ne pas coder immédiatement : Puis optimise les vrais hotspots.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `103. SIMD / optimisation prématurée` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0320`; supporting items: none found by conservative heading match; domain indexes `RISK, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0288 — 104. Recherche Python

- Source: `SRC-007`
- Location: lines 10238–10252; heading `104. Recherche Python`
- Domain tags: ARCH, RESEARCH, RISK, INFRA, VALIDATION, SIMULATOR, SURVIVAL, SIZING
- Source statement: 104. Recherche Python: Tout ce qui sert à calibrer : est d’abord étudié en Python.
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `104. Recherche Python` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ARCH-0084`; supporting items: none found by conservative heading match; domain indexes `ARCH, RESEARCH, RISK, INFRA, VALIDATION, SIMULATOR, SURVIVAL, SIZING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0289 — 105. Production Rust

- Source: `SRC-007`
- Location: lines 10253–10296; heading `105. Production Rust`
- Domain tags: PRODUCT, ARCH, INFRA
- Source statement: 105. Production Rust: Une fois le modèle validé :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `105. Production Rust` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PRODUCT-0021`; supporting items: none found by conservative heading match; domain indexes `PRODUCT, ARCH, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0290 — 106. Golden Tests

- Source: `SRC-007`
- Location: lines 10297–10316; heading `106. Golden Tests`
- Domain tags: VALIDATION, RISK, SURVIVAL, MICROSTRUCTURE, SIZING, ROUTING, ARCH
- Source statement: 106. Golden Tests: Python et Rust doivent produire la même chose dans la tolérance numérique définie.
- Nature: protocol/validation
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `106. Golden Tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0371`; supporting items: SRC-004-ITEM-0276, SRC-004-ITEM-0278, SRC-006-ITEM-0316; domain indexes `VALIDATION, RISK, SURVIVAL, MICROSTRUCTURE, SIZING, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0291 — 107. Numerical Stability

- Source: `SRC-007`
- Location: lines 10317–10334; heading `107. Numerical Stability`
- Domain tags: QUANT
- Source statement: 107. Numerical Stability: Ne jamais comparer directement : une représentation en unités discrètes peut être préférable.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `107. Numerical Stability` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-QUANT-0021`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0292 — 108. Precision / Rounding

- Source: `SRC-007`
- Location: lines 10335–10355; heading `108. Precision / Rounding`
- Domain tags: RECOVERY, ACCOUNTING
- Source statement: 108. Precision / Rounding: Cela doit faire partie du modèle économique. Donc chaque simulation passe par les mêmes règles que l’exécution réelle.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `108. Precision / Rounding` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0022`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0293 — 109. Route Confidence

- Source: `SRC-007`
- Location: lines 10356–10384; heading `109. Route Confidence`
- Domain tags: ROUTING, EXECUTION, RISK, BENCHMARK, ACCOUNTING, INVENTORY, QUANT
- Source statement: 109. Route Confidence: Une route devrait finalement transporter : C’est probablement l’objet le plus utile pour le Risk Engine.
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `109. Route Confidence` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0034`; supporting items: none found by conservative heading match; domain indexes `ROUTING, EXECUTION, RISK, BENCHMARK, ACCOUNTING, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0294 — 110. Décision finale

- Source: `SRC-007`
- Location: lines 10385–10513; heading `110. Décision finale`
- Domain tags: EXECUTION, RISK, INFRA, OPERATIONS, ACCOUNTING, INVENTORY
- Source statement: 110. Décision finale: Le Risk Engine reçoit :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `110. Décision finale` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0284`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, OPERATIONS, ACCOUNTING, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0295 — 111. Ce que notre bot devient réellement

- Source: `SRC-007`
- Location: lines 10514–10641; heading `111. Ce que notre bot devient réellement`
- Domain tags: RISK, INFRA, ACCOUNTING, PARTICIPANTS, INVENTORY, ROUTING
- Source statement: 111. Ce que notre bot devient réellement: Ce n’est donc plus simplement : mais un système qui résout approximativement :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `111. Ce que notre bot devient réellement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0321`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, ACCOUNTING, PARTICIPANTS, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0296 — 112. Les 10 outils Quant réellement CORE

- Source: `SRC-007`
- Location: lines 10642–10643; heading `112. Les 10 outils Quant réellement CORE`
- Domain tags: QUANT, ARCH
- Source statement: 112. Les 10 outils Quant réellement CORE: Si je devais ne garder que les dix indispensables :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `112. Les 10 outils Quant réellement CORE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0022`; supporting items: none found by conservative heading match; domain indexes `QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0297 — 1. NetConvert / L2 Book Walk

- Source: `SRC-007`
- Location: lines 10644–10645; heading `1. NetConvert / L2 Book Walk`
- Domain tags: ROUTING
- Source statement: 1. NetConvert / L2 Book Walk: Pour savoir ce que vaut réellement une conversion.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `1. NetConvert / L2 Book Walk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0035`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0298 — 2. Expected Value

- Source: `SRC-007`
- Location: lines 10646–10647; heading `2. Expected Value`
- Domain tags: QUANT
- Source statement: 2. Expected Value: Pour transformer probabilités d’exécution en argent.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `2. Expected Value` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0023`; supporting items: SRC-004-ITEM-0216; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0299 — 3. Edge Survival / Hazard

- Source: `SRC-007`
- Location: lines 10648–10649; heading `3. Edge Survival / Hazard`
- Domain tags: SURVIVAL
- Source statement: 3. Edge Survival / Hazard: Pour mesurer si l’opportunité survivra jusqu’à nous.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `3. Edge Survival / Hazard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SURV-0022`; supporting items: none found by conservative heading match; domain indexes `SURVIVAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0300 — 4. OFI / Queue Imbalance / Microprice

- Source: `SRC-007`
- Location: lines 10650–10651; heading `4. OFI / Queue Imbalance / Microprice`
- Domain tags: MICROSTRUCTURE, INVENTORY
- Source statement: 4. OFI / Queue Imbalance / Microprice: Pour représenter la pression microstructurelle.
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `4. OFI / Queue Imbalance / Microprice` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0019`; supporting items: SRC-004-ITEM-0186; domain indexes `MICROSTRUCTURE, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0301 — 5. Volatility / Jump Risk

- Source: `SRC-007`
- Location: lines 10652–10653; heading `5. Volatility / Jump Risk`
- Domain tags: RISK, QUANT
- Source statement: 5. Volatility / Jump Risk: Pour mesurer les mouvements adverses possibles.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `5. Volatility / Jump Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0322`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0302 — 6. Fill & Adverse Selection

- Source: `SRC-007`
- Location: lines 10654–10655; heading `6. Fill & Adverse Selection`
- Domain tags: EXECUTION, MAKER_MODEL
- Source statement: 6. Fill & Adverse Selection: Pour maker/taker.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `6. Fill & Adverse Selection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0285`; supporting items: SRC-004-ITEM-0214, SRC-008-ITEM-0035; domain indexes `EXECUTION, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0303 — 7. Monte Carlo / Outcome Distribution

- Source: `SRC-007`
- Location: lines 10656–10657; heading `7. Monte Carlo / Outcome Distribution`
- Domain tags: SIMULATOR, PRODUCT, ACCOUNTING
- Source statement: 7. Monte Carlo / Outcome Distribution: Pour connaître la distribution réelle du PnL.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `7. Monte Carlo / Outcome Distribution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIM-0008`; supporting items: none found by conservative heading match; domain indexes `SIMULATOR, PRODUCT, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0304 — 8. CVaR / Tail Risk

- Source: `SRC-007`
- Location: lines 10658–10659; heading `8. CVaR / Tail Risk`
- Domain tags: RISK
- Source statement: 8. CVaR / Tail Risk: Pour éviter qu’une belle moyenne cache des catastrophes.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `8. CVaR / Tail Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0323`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0305 — 9. Constrained Position Sizing

- Source: `SRC-007`
- Location: lines 10660–10661; heading `9. Constrained Position Sizing`
- Domain tags: SIZING
- Source statement: 9. Constrained Position Sizing: Pour déterminer combien engager.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `9. Constrained Position Sizing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-SIZE-0004`; supporting items: SRC-006-ITEM-0358; domain indexes `SIZING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0306 — 10. Portfolio Optimization

- Source: `SRC-007`
- Location: lines 10662–10664; heading `10. Portfolio Optimization`
- Domain tags: PORTFOLIO
- Source statement: 10. Portfolio Optimization: Pour choisir le meilleur ensemble d’opportunités simultanées.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `10. Portfolio Optimization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PORT-0003`; supporting items: SRC-005-ITEM-0161; domain indexes `PORTFOLIO`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0307 — 113. Les modèles QUANT de deuxième niveau

- Source: `SRC-007`
- Location: lines 10665–10677; heading `113. Les modèles QUANT de deuxième niveau`
- Domain tags: QUANT, PARTICIPANTS, MICROSTRUCTURE, PRODUCT
- Source statement: 113. Les modèles QUANT de deuxième niveau: Après accumulation de données : Ils challengent les modèles simples.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `113. Les modèles QUANT de deuxième niveau` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-QUANT-0024`; supporting items: none found by conservative heading match; domain indexes `QUANT, PARTICIPANTS, MICROSTRUCTURE, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0308 — 114. Les modèles qu’on n’a PAS besoin de construire maintenant

- Source: `SRC-007`
- Location: lines 10678–10692; heading `114. Les modèles qu’on n’a PAS besoin de construire maintenant`
- Domain tags: PORTFOLIO, QUANT
- Source statement: 114. Les modèles qu’on n’a PAS besoin de construire maintenant: Ils sont intéressants en finance quantitative générale. Mais pas directement utiles à notre problème actuel.
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `114. Les modèles qu’on n’a PAS besoin de construire maintenant` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-PORT-0004`; supporting items: none found by conservative heading match; domain indexes `PORTFOLIO, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0309 — 115. Principe d’optimisation général

- Source: `SRC-007`
- Location: lines 10693–10717; heading `115. Principe d’optimisation général`
- Domain tags: FORMULA, VALIDATION, ACCOUNTING, REPLAY, PRODUCT
- Source statement: 115. Principe d’optimisation général: Pour chaque nouvelle formule/modèle, on doit se demander : 1. Quelle décision influence-t-elle ?
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `115. Principe d’optimisation général` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-FORMULA-0143`; supporting items: none found by conservative heading match; domain indexes `FORMULA, VALIDATION, ACCOUNTING, REPLAY, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0310 — 116. Quant Model ROI

- Source: `SRC-007`
- Location: lines 10718–10806; heading `116. Quant Model ROI`
- Domain tags: QUANT, INFRA, ACCOUNTING
- Source statement: 116. Quant Model ROI: Même philosophie que nos VPS. mais améliore ExpectedPnL de :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `116. Quant Model ROI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0025`; supporting items: SRC-004-ITEM-0261, SRC-006-ITEM-0464; domain indexes `QUANT, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0311 — 117. La véritable philosophie Quant du projet

- Source: `SRC-007`
- Location: lines 10807–10879; heading `117. La véritable philosophie Quant du projet`
- Domain tags: QUANT, FORMULA, RISK, INFRA, ACCOUNTING, PARTICIPANTS, INVENTORY, CAPITAL
- Source statement: 117. La véritable philosophie Quant du projet: Notre bot ne cherche pas : la formule parfaite du marché.
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `117. La véritable philosophie Quant du projet` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0026`; supporting items: none found by conservative heading match; domain indexes `QUANT, FORMULA, RISK, INFRA, ACCOUNTING, PARTICIPANTS, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0312 — 118. Résumé architectural final

- Source: `SRC-007`
- Location: lines 10880–10934; heading `118. Résumé architectural final`
- Domain tags: RISK, ACCOUNTING, SIMULATOR, PARTICIPANTS, SURVIVAL, CROSS_MARKET, MICROSTRUCTURE, INVENTORY
- Source statement: 118. Résumé architectural final: MARKET DATA BOOK ENGINE
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `118. Résumé architectural final` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0324`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, SIMULATOR, PARTICIPANTS, SURVIVAL, CROSS_MARKET, MICROSTRUCTURE, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0313 — 119. La formule conceptuelle ultime

- Source: `SRC-007`
- Location: lines 10935–11159; heading `119. La formule conceptuelle ultime`
- Domain tags: FORMULA, RISK, INFRA, ACCOUNTING, PARTICIPANTS, INVENTORY, CAPITAL, ROUTING
- Source statement: 119. La formule conceptuelle ultime: Notre problème complet peut être écrit : (r^*,q^*,e^*) = \arg\max_{r,q,e} E[ PnL(r,q,e) | MarketState, Competition, Latency ]
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `119. La formule conceptuelle ultime` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-FORMULA-0144`; supporting items: SRC-004-ITEM-0282; domain indexes `FORMULA, RISK, INFRA, ACCOUNTING, PARTICIPANTS, INVENTORY, CAPITAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0314 — 120. Conclusion

- Source: `SRC-007`
- Location: lines 11160–11210; heading `120. Conclusion`
- Domain tags: FORMULA, EXECUTION, RECOVERY, RISK, ACCOUNTING, SURVIVAL, MICROSTRUCTURE, QUANT
- Source statement: 120. Conclusion: Oui, notre bot doit devenir fortement quantitatif. Mais notre branche de quant est très clairement :
- Nature: edge-case/failure behaviour
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `120. Conclusion` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0145`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, RECOVERY, RISK, ACCOUNTING, SURVIVAL, MICROSTRUCTURE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0315 — 1. Formules déjà quasiment définitives

- Source: `SRC-007`
- Location: lines 11211–11724; heading `1. Formules déjà quasiment définitives`
- Domain tags: FORMULA, RISK, INFRA, ACCOUNTING, SURVIVAL, MICROSTRUCTURE, INVENTORY, BRIDGE
- Source statement: 1. Formules déjà quasiment définitives: Celles-ci peuvent entrer telles quelles dans la spécification mathématique du bot, à quelques conventions près. Hazard → survival | S
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `1. Formules déjà quasiment définitives` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-FORMULA-0146`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, INFRA, ACCOUNTING, SURVIVAL, MICROSTRUCTURE, INVENTORY, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0316 — 2. Formules dont la structure est définie, mais dont les paramètres doivent être appris

- Source: `SRC-007`
- Location: lines 11725–11912; heading `2. Formules dont la structure est définie, mais dont les paramètres doivent être appris`
- Domain tags: FORMULA, INFRA, RISK, VALIDATION, ACCOUNTING, REPLAY, INVENTORY, ARCH
- Source statement: 2. Formules dont la structure est définie, mais dont les paramètres doivent être appris: InventoryPenalty = k \left( \frac{I-I^*}{Band} \right)^2 La forme quadratique est plausible, mais on ne sait pas encore si notre meilleur modèle réel sera exactement celui-là.
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `2. Formules dont la structure est définie, mais dont les paramètres doivent être appris` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0147`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, RISK, VALIDATION, ACCOUNTING, REPLAY, INVENTORY, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0317 — 3. Formules volontairement conceptuelles

- Source: `SRC-007`
- Location: lines 11913–12061; heading `3. Formules volontairement conceptuelles`
- Domain tags: FORMULA, SURVIVAL, MICROSTRUCTURE, QUANT, ARCH
- Source statement: 3. Formules volontairement conceptuelles: ShockIntensity = f( OurSize, Depth, OFI, Spread, Volatility ) Confidence = f( DataQuality, OOD, SampleSize, ModelAgreement,\ldots )
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `3. Formules volontairement conceptuelles` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-FORMULA-0148`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SURVIVAL, MICROSTRUCTURE, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0318 — Un exemple très concret : OFI

- Source: `SRC-007`
- Location: lines 12062–12119; heading `Un exemple très concret : OFI`
- Domain tags: MICROSTRUCTURE, RISK, ARCH
- Source statement: Un exemple très concret : OFI: Dans ma réponse précédente, j'ai dit qu'on utiliserait l'OFI, mais je ne t'ai pas encore donné sa définition algorithmique complète finale. Pour le meilleur niveau, on peut définir pour le bid une contribution
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Un exemple très concret : OFI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-MICRO-0020`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, RISK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-007-ITEM-0319 — Même chose pour la volatilité

- Source: `SRC-007`
- Location: lines 12120–12204; heading `Même chose pour la volatilité`
- Domain tags: FORMULA, RISK
- Source statement: Même chose pour la volatilité: Ce sont de vraies formules. Mais il reste à décider si notre Risk Engine utilisera :
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Même chose pour la volatilité` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-FORMULA-0149`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0320 — Ce qui manque donc réellement maintenant

- Source: `SRC-007`
- Location: lines 12205–12310; heading `Ce qui manque donc réellement maintenant`
- Domain tags: FORMULA, EXECUTION, INFRA, DEPLOYMENT, MICROSTRUCTURE, INVENTORY, ROUTING, HOT_WARM_COLD
- Source statement: Ce qui manque donc réellement maintenant: Pour avoir une spécification quantitative complètement codable, il faudrait faire un document beaucoup plus strict : où pour chaque calcul on aurait exactement :
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Ce qui manque donc réellement maintenant` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0150`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, INFRA, DEPLOYMENT, MICROSTRUCTURE, INVENTORY, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-001; external revalidation: NO.

### SRC-007-ITEM-0321 — Et il nous faut faire ça pour environ 25–35 calculs centraux

- Source: `SRC-007`
- Location: lines 12311–12314; heading `Et il nous faut faire ça pour environ 25–35 calculs centraux`
- Domain tags: QUANT
- Source statement: Et il nous faut faire ça pour environ 25–35 calculs centraux: Les 110 sections expliquaient l'écosystème complet. Mais le vrai noyau mathématique codé devrait probablement tenir dans environ :
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Et il nous faut faire ça pour environ 25–35 calculs centraux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0027`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0322 — Pricing / arbitrage

- Source: `SRC-007`
- Location: lines 12315–12324; heading `Pricing / arbitrage`
- Domain tags: ACCOUNTING, OWA, TRIANGLE, ROUTING
- Source statement: Pricing / arbitrage: 1. NetConvert 2. BookWalk
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Pricing / arbitrage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0062`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, OWA, TRIANGLE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0323 — Microstructure

- Source: `SRC-007`
- Location: lines 12325–12336; heading `Microstructure`
- Domain tags: MICROSTRUCTURE, LIQUIDITY_RESPONSE, INVENTORY, QUANT
- Source statement: Microstructure: 1. Spread 2. Depth
- Nature: data/architecture contract
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Microstructure` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-MICRO-0021`; supporting items: none found by conservative heading match; domain indexes `MICROSTRUCTURE, LIQUIDITY_RESPONSE, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0324 — Probability / execution

- Source: `SRC-007`
- Location: lines 12337–12345; heading `Probability / execution`
- Domain tags: QUANT, EXECUTION, SURVIVAL, MAKER_MODEL
- Source statement: Probability / execution: 5. Expected edge at arrival
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Probability / execution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-QUANT-0028`; supporting items: SRC-004-ITEM-0210; domain indexes `QUANT, EXECUTION, SURVIVAL, MAKER_MODEL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0325 — Risk

- Source: `SRC-007`
- Location: lines 12346–12350; heading `Risk`
- Domain tags: RISK, ACCOUNTING
- Source statement: Risk: 4. confidence / OOD gate
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0325`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0326 — Optimization

- Source: `SRC-007`
- Location: lines 12351–12356; heading `Optimization`
- Domain tags: INVENTORY, CAPITAL, SIZING, PORTFOLIO, BRIDGE
- Source statement: Optimization: 1. Position sizing objective 2. Validated Capacity
- Nature: decision/policy/concept
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Optimization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0024`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, CAPITAL, SIZING, PORTFOLIO, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-007-ITEM-0327 — Infrastructure

- Source: `SRC-007`
- Location: lines 12357–12371; heading `Infrastructure`
- Domain tags: INFRA, FORMULA, EXECUTION, RISK, ACCOUNTING, PRODUCT, ARCH
- Source statement: Infrastructure: Donc la réponse précise est : Non, je ne t'ai pas encore fourni un “livre de formules final” où chacune des ~40 équations du bot est complètement spécifiée et prête à coder.
- Nature: formula/definition
- Temporal interpretation: advanced refinement
- Authority: Advanced refinement for client model, participants, survival and quant; Formula Book prevails.
- Candidate canonical interpretation: Preserve `Infrastructure` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0050`; supporting items: none found by conservative heading match; domain indexes `INFRA, FORMULA, EXECUTION, RISK, ACCOUNTING, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 310
- Requirements contributed: 310
- Supporting references contributed: 109 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 0
- Research items: 203
- Open items: 1
- External revalidation items: 17
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
