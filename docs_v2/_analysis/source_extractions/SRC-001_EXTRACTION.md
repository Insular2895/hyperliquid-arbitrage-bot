# SRC-001 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-001`
- Filename: `23. Lock-free  ring buffers  zero-copy.md`
- SHA-256: `061043598486f7e4fa357e681dfb67e909989945be0b8c82e1070cb7ff559921`
- Line count: 5255
- Authority profile: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Main domains: ACCOUNTING, RISK, EXECUTION, ROUTING, ARCH, BRIDGE, HOT_WARM_COLD, INFRA, CAPITAL, VALIDATION, INVENTORY, REPLAY
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-001-ITEM-0001 — 23. Lock-free / ring buffers / zero-copy

- Source: `SRC-001`
- Location: lines 1–19; heading `23. Lock-free / ring buffers / zero-copy`
- Domain tags: BENCHMARK, MICROSTRUCTURE, ARCH
- Source statement: 23. Lock-free / ring buffers / zero-copy: Ces idées avaient déjà été évoquées pour diminuer la latence. Elles restent intéressantes, mais je ne les imposerais pas partout dès la première ligne de code.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `23. Lock-free / ring buffers / zero-copy` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0001`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, MICROSTRUCTURE, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0002 — 24. Aucun appel bloquant pendant une opportunité

- Source: `SRC-001`
- Location: lines 20–50; heading `24. Aucun appel bloquant pendant une opportunité`
- Domain tags: QUANT, RISK, ACCOUNTING, INVENTORY
- Source statement: 24. Aucun appel bloquant pendant une opportunité: C'était déjà une règle ancienne essentielle. le bot ne doit pas devoir demander :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `24. Aucun appel bloquant pendant une opportunité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-QUANT-0001`; supporting items: none found by conservative heading match; domain indexes `QUANT, RISK, ACCOUNTING, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0003 — 25. Vérifier le solde AVANT l'ordre

- Source: `SRC-001`
- Location: lines 51–67; heading `25. Vérifier le solde AVANT l'ordre`
- Domain tags: SECURITY, INVENTORY, ARCH
- Source statement: 25. Vérifier le solde AVANT l'ordre: On a eu des problèmes historiques de : Donc chaque ExecutionPlan doit savoir :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `25. Vérifier le solde AVANT l'ordre` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0001`; supporting items: none found by conservative heading match; domain indexes `SECURITY, INVENTORY, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0004 — 26. Tick size / lot size / min notional

- Source: `SRC-001`
- Location: lines 68–87; heading `26. Tick size / lot size / min notional`
- Domain tags: QUANT
- Source statement: 26. Tick size / lot size / min notional: On avait explicitement prévu : Sur Hyperliquid, les règles ne sont pas identiques, mais le problème général reste exactement le même.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `26. Tick size / lot size / min notional` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-QUANT-0002`; supporting items: none found by conservative heading match; domain indexes `QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0005 — 27. Clock sync / timestamps

- Source: `SRC-001`
- Location: lines 88–104; heading `27. Clock sync / timestamps`
- Domain tags: CLOCK, ARCH
- Source statement: 27. Clock sync / timestamps: On avait eu notamment le fameux problème Binance : * horloge correctement synchronisée ;
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `27. Clock sync / timestamps` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0001`; supporting items: none found by conservative heading match; domain indexes `CLOCK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0006 — 28. Rate limits / retries

- Source: `SRC-001`
- Location: lines 105–126; heading `28. Rate limits / retries`
- Domain tags: RISK
- Source statement: 28. Rate limits / retries: * API qui refuse ; Mais jamais de retry aveugle d'ordre.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `28. Rate limits / retries` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0001`; supporting items: SRC-008-ITEM-0211; domain indexes `RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0007 — 29. IOC/FOK plutôt que market aveugle

- Source: `SRC-001`
- Location: lines 127–143; heading `29. IOC/FOK plutôt que market aveugle`
- Domain tags: EXECUTION, RISK
- Source statement: 29. IOC/FOK plutôt que market aveugle: On avait initialement voulu beaucoup utiliser : pour éviter les partial fills.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `29. IOC/FOK plutôt que market aveugle` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0001`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0008 — 30. Partial fills = scénario normal, pas exception

- Source: `SRC-001`
- Location: lines 144–179; heading `30. Partial fills = scénario normal, pas exception`
- Domain tags: EXECUTION, RECOVERY, RISK, DEPLOYMENT
- Source statement: 30. Partial fills = scénario normal, pas exception: si les trois jambes ne remplissent pas complètement, catastrophe. On avait déjà prévu :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `30. Partial fills = scénario normal, pas exception` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0002`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, DEPLOYMENT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0009 — 31. Ne jamais dépendre d'une exécution atomique des 3 jambes

- Source: `SRC-001`
- Location: lines 180–195; heading `31. Ne jamais dépendre d'une exécution atomique des 3 jambes`
- Domain tags: RECOVERY
- Source statement: 31. Ne jamais dépendre d'une exécution atomique des 3 jambes: Même si on envoie un batch : on doit toujours concevoir le système comme si :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `31. Ne jamais dépendre d'une exécution atomique des 3 jambes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0001`; supporting items: none found by conservative heading match; domain indexes `RECOVERY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0010 — 32. Kill switch de latence

- Source: `SRC-001`
- Location: lines 196–217; heading `32. Kill switch de latence`
- Domain tags: RISK, INFRA
- Source statement: 32. Kill switch de latence: On avait anciennement parlé de quelque chose autour de : Je ne conserverais absolument pas ce chiffre.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `32. Kill switch de latence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `SUPERSEDED`
- Cross-source references: `REQ-RISK-0002`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0011 — 33. Max slippage

- Source: `SRC-001`
- Location: lines 218–232; heading `33. Max slippage`
- Domain tags: EXECUTION, RISK, ARCH
- Source statement: 33. Max slippage: aucune exécution au-delà d'un slippage maximum. Aujourd'hui encore plus propre :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `33. Max slippage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0003`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0012 — 34. Limites par trade et par asset

- Source: `SRC-001`
- Location: lines 233–256; heading `34. Limites par trade et par asset`
- Domain tags: RISK, INVENTORY, ROUTING
- Source statement: 34. Limites par trade et par asset: Il nous faut toujours cela.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `34. Limites par trade et par asset` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0003`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0013 — 35. Circuit breakers

- Source: `SRC-001`
- Location: lines 257–278; heading `35. Circuit breakers`
- Domain tags: RISK, ACCOUNTING, ROUTING, QUANT
- Source statement: 35. Circuit breakers: On avait même proposé des règles du genre : * 3 pertes / 5 min ;
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `35. Circuit breakers` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0004`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0014 — 36. Whitelist de liquidité

- Source: `SRC-001`
- Location: lines 279–307; heading `36. Whitelist de liquidité`
- Domain tags: GRAPH, QUANT, ARCH
- Source statement: 36. Whitelist de liquidité: top 1–10 assets liquides et exclure les paires pourries. Très bonne protection, mais trop rigide aujourd'hui.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `36. Whitelist de liquidité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-GRAPH-0001`; supporting items: none found by conservative heading match; domain indexes `GRAPH, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0015 — 37. Filtre volume/liquidité

- Source: `SRC-001`
- Location: lines 308–316; heading `37. Filtre volume/liquidité`
- Domain tags: INFRA, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 37. Filtre volume/liquidité: On avait même évoqué à l'époque : Je ne conserverais pas 10 M$.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `37. Filtre volume/liquidité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0001`; supporting items: none found by conservative heading match; domain indexes `INFRA, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0016 — 38. Paper/live avec le même code

- Source: `SRC-001`
- Location: lines 317–356; heading `38. Paper/live avec le même code`
- Domain tags: RESEARCH, ACCOUNTING, REPLAY, ARCH
- Source statement: 38. Paper/live avec le même code: Ça, je considère que c'était une excellente décision historique. mais même code de stratégie.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `38. Paper/live avec le même code` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RESEARCH-0001`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, ACCOUNTING, REPLAY, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0017 — 39. Shadow mode

- Source: `SRC-001`
- Location: lines 357–368; heading `39. Shadow mode`
- Domain tags: VALIDATION, EXECUTION, QUANT
- Source statement: 39. Shadow mode: Ça avait déjà été prévu. * regarde le vrai marché ;
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `39. Shadow mode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0001`; supporting items: SRC-006-ITEM-0414; domain indexes `VALIDATION, EXECUTION, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0018 — 40. Micro-live

- Source: `SRC-001`
- Location: lines 369–390; heading `40. Micro-live`
- Domain tags: VALIDATION, REPLAY, CAPITAL, FUTURE, RESEARCH
- Source statement: 40. Micro-live: On avait parlé de 50–100 € pour les premiers vrais tests dans les anciens projets. Le capital exact sera décidé plus tard.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `40. Micro-live` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-VALID-0002`; supporting items: SRC-005-ITEM-0481, SRC-005-ITEM-0606, SRC-006-ITEM-0258, SRC-006-ITEM-0287; domain indexes `VALIDATION, REPLAY, CAPITAL, FUTURE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0019 — 41. Recorder

- Source: `SRC-001`
- Location: lines 391–416; heading `41. Recorder`
- Domain tags: EXECUTION, RECORDER, CLOCK, REPLAY, ARCH, RESEARCH
- Source statement: 41. Recorder: Avant même les papiers, on avait déjà prévu : Aujourd'hui il devient encore plus central.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `41. Recorder` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0004`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, CLOCK, REPLAY, ARCH, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0020 — 42. Replay avec latence artificielle

- Source: `SRC-001`
- Location: lines 417–438; heading `42. Replay avec latence artificielle`
- Domain tags: REPLAY, RISK, INFRA, ACCOUNTING, RESEARCH
- Source statement: 42. Replay avec latence artificielle: C'était déjà une de nos bonnes idées d'août avant d'approfondir les papiers. Prendre une même opportunité et tester :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `42. Replay avec latence artificielle` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0001`; supporting items: none found by conservative heading match; domain indexes `REPLAY, RISK, INFRA, ACCOUNTING, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0021 — 43. Replay multi-size

- Source: `SRC-001`
- Location: lines 439–459; heading `43. Replay multi-size`
- Domain tags: REPLAY, QUANT
- Source statement: 43. Replay multi-size: Même événement : 100 €
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `43. Replay multi-size` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REPLAY-0002`; supporting items: none found by conservative heading match; domain indexes `REPLAY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0022 — 44. Comparer simulation et vrai fill

- Source: `SRC-001`
- Location: lines 460–479; heading `44. Comparer simulation et vrai fill`
- Domain tags: EXECUTION, VALIDATION
- Source statement: 44. Comparer simulation et vrai fill: Sans ça, un backtest peut rester faussement optimiste.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `44. Comparer simulation et vrai fill` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0005`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, VALIDATION`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0023 — 45. Reason Codes

- Source: `SRC-001`
- Location: lines 480–502; heading `45. Reason Codes`
- Domain tags: EXECUTION, RISK, INFRA, INVENTORY, ROUTING, ARCH
- Source statement: 45. Reason Codes: L'idée existait déjà dans nos architectures précédentes. Chaque rejet doit dire pourquoi :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `45. Reason Codes` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0006`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, INVENTORY, ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0024 — 46. Observabilité complète

- Source: `SRC-001`
- Location: lines 503–534; heading `46. Observabilité complète`
- Domain tags: EXECUTION, INFRA, ACCOUNTING
- Source statement: 46. Observabilité complète: Les technologies pourront changer, mais l'idée reste indispensable.
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `46. Observabilité complète` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-EXEC-0007`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0025 — 47. Heartbeat / health monitoring

- Source: `SRC-001`
- Location: lines 535–554; heading `47. Heartbeat / health monitoring`
- Domain tags: OPERATIONS, EXECUTION, RISK, RECORDER, CLOCK, ACCOUNTING
- Source statement: 47. Heartbeat / health monitoring: Le bot ne doit pas simplement : Si un composant essentiel devient mauvais :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `47. Heartbeat / health monitoring` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0001`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, EXECUTION, RISK, RECORDER, CLOCK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0026 — 48. Persistance de l'état

- Source: `SRC-001`
- Location: lines 555–576; heading `48. Persistance de l'état`
- Domain tags: RECOVERY, OPERATIONS, ACCOUNTING, INVENTORY, ROUTING, QUANT
- Source statement: 48. Persistance de l'état: Le principe reste très bon, même si je ne ferais probablement pas tout dans un simple JSON. Après crash/restart, le bot doit connaître :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `48. Persistance de l'état` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0002`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, OPERATIONS, ACCOUNTING, INVENTORY, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0027 — 49. Redémarrage sûr

- Source: `SRC-001`
- Location: lines 577–611; heading `49. Redémarrage sûr`
- Domain tags: RECONCILIATION, RISK, INVENTORY, GRAPH
- Source statement: 49. Redémarrage sûr: Un redémarrage ne doit jamais signifier :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `49. Redémarrage sûr` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-RECON-0001`; supporting items: none found by conservative heading match; domain indexes `RECONCILIATION, RISK, INVENTORY, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0028 — 50. Clés API limitées

- Source: `SRC-001`
- Location: lines 612–623; heading `50. Clés API limitées`
- Domain tags: RISK, SECURITY, CROSS_EXCHANGE, RESEARCH
- Source statement: 50. Clés API limitées: Ancienne règle très saine : le bot peut trader, jamais retirer les fonds.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `50. Clés API limitées` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0005`; supporting items: none found by conservative heading match; domain indexes `RISK, SECURITY, CROSS_EXCHANGE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0029 — 51. Config centralisée

- Source: `SRC-001`
- Location: lines 624–641; heading `51. Config centralisée`
- Domain tags: RISK, INFRA, ACCOUNTING, ROUTING
- Source statement: 51. Config centralisée: On avait parlé de YAML/config. Mais les paramètres importants doivent être versionnés :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `51. Config centralisée` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-RISK-0006`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0030 — 52. Benchmarks avant optimisation extrême

- Source: `SRC-001`
- Location: lines 642–676; heading `52. Benchmarks avant optimisation extrême`
- Domain tags: BENCHMARK, RISK, INFRA, DEPLOYMENT, ROUTING
- Source statement: 52. Benchmarks avant optimisation extrême: La vraie bonne leçon derrière ça :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `52. Benchmarks avant optimisation extrême` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0002`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, RISK, INFRA, DEPLOYMENT, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0031 — 53. Ne pas confondre CPU rapide et système rapide

- Source: `SRC-001`
- Location: lines 677–696; heading `53. Ne pas confondre CPU rapide et système rapide`
- Domain tags: INFRA, ACCOUNTING
- Source statement: 53. Ne pas confondre CPU rapide et système rapide: Cette intuition existait déjà quand on comparait VPS, GPU et CPU. Aujourd'hui on la formalise :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `53. Ne pas confondre CPU rapide et système rapide` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INFRA-0002`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0032 — 54. Seuil de profit minimal

- Source: `SRC-001`
- Location: lines 697–724; heading `54. Seuil de profit minimal`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, RISK, INFRA, TRIANGLE, ROUTING
- Source statement: 54. Seuil de profit minimal: On avait des anciens chiffres comme : Je ne veux surtout pas les reprendre tels quels.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `54. Seuil de profit minimal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ACCT-0001`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, RISK, INFRA, TRIANGLE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0033 — 55. Hystérésis / éviter le flip-flop

- Source: `SRC-001`
- Location: lines 725–763; heading `55. Hystérésis / éviter le flip-flop`
- Domain tags: CAPITAL, BRIDGE, ROUTING, HOT_WARM_COLD, FUTURE
- Source statement: 55. Hystérésis / éviter le flip-flop: Dans les anciens bots multi-paires/funding, on avait parlé de : * éviter les changements incessants ;
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `55. Hystérésis / éviter le flip-flop` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-CAP-0001`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, BRIDGE, ROUTING, HOT_WARM_COLD, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0034 — 56. Opportunity cost

- Source: `SRC-001`
- Location: lines 764–786; heading `56. Opportunity cost`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, CAPITAL
- Source statement: 56. Opportunity cost: L'ancien top-K / allocation avait déjà implicitement ce problème : mettre de l'argent sur A signifie ne pas l'avoir sur B.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `56. Opportunity cost` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ACCT-0002`; supporting items: SRC-007-ITEM-0250; domain indexes `ACCOUNTING, MICROSTRUCTURE, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0035 — 57. Auto-compounding : à garder avec prudence

- Source: `SRC-001`
- Location: lines 787–818; heading `57. Auto-compounding : à garder avec prudence`
- Domain tags: RISK, VALIDATION, ACCOUNTING, MICROSTRUCTURE, CAPITAL
- Source statement: 57. Auto-compounding : à garder avec prudence: On avait déjà évoqué le réinvestissement automatique des profits dans d'autres bots. Je ne veux pas :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `57. Auto-compounding : à garder avec prudence` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0007`; supporting items: SRC-005-ITEM-0164; domain indexes `RISK, VALIDATION, ACCOUNTING, MICROSTRUCTURE, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0036 — 58. Ce qu'on ne reprend PAS

- Source: `SRC-001`
- Location: lines 819–963; heading `58. Ce qu'on ne reprend PAS`
- Domain tags: EXECUTION, RECOVERY, RISK, RECORDER, INFRA, DEPLOYMENT, VALIDATION, ACCOUNTING
- Source statement: 58. Ce qu'on ne reprend PAS: Il y a plusieurs anciennes idées que je sortirais clairement de la V1. Incompatible avec notre direction latency/Hyperliquid.
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `58. Ce qu'on ne reprend PAS` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0008`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, RECORDER, INFRA, DEPLOYMENT, VALIDATION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0037 — 1. D’abord : séparer architecture et validation

- Source: `SRC-001`
- Location: lines 964–996; heading `1. D’abord : séparer architecture et validation`
- Domain tags: VALIDATION, ARCH, REPLAY
- Source statement: 1. D’abord : séparer architecture et validation: On avait parfois tendance à mélanger : * écrire le bot ;
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `1. D’abord : séparer architecture et validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0003`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0038 — 2. Première brique développée : Recorder + Market Graph

- Source: `SRC-001`
- Location: lines 997–1046; heading `2. Première brique développée : Recorder + Market Graph`
- Domain tags: EXECUTION, RECORDER, GRAPH, CLOCK, ACCOUNTING, TRIANGLE, ROUTING
- Source statement: 2. Première brique développée : Recorder + Market Graph: Avant le vrai moteur d’exécution. C’était déjà une de nos idées fortes : commencer à enregistrer le marché pendant qu’on développe le reste.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `2. Première brique développée : Recorder + Market Graph` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0009`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, GRAPH, CLOCK, ACCOUNTING, TRIANGLE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0039 — 3. Phase 1 = Cartographier avant de chercher à gagner

- Source: `SRC-001`
- Location: lines 1047–1094; heading `3. Phase 1 = Cartographier avant de chercher à gagner`
- Domain tags: GRAPH, ACCOUNTING, CAPITAL, BRIDGE, TRIANGLE, ROUTING, MARKET_ATLAS, ARCH
- Source statement: 3. Phase 1 = Cartographier avant de chercher à gagner: Ça devient encore plus important avec notre direction actuelle. On ne commence pas en disant :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `3. Phase 1 = Cartographier avant de chercher à gagner` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-GRAPH-0002`; supporting items: none found by conservative heading match; domain indexes `GRAPH, ACCOUNTING, CAPITAL, BRIDGE, TRIANGLE, ROUTING, MARKET_ATLAS, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0040 — 4. Ne jamais tester seulement “le meilleur cas”

- Source: `SRC-001`
- Location: lines 1095–1098; heading `4. Ne jamais tester seulement “le meilleur cas”`
- Domain tags: RISK
- Source statement: 4. Ne jamais tester seulement “le meilleur cas”: Ça aussi faisait partie de notre réflexion ancienne sur les tailles et latences. Une opportunité doit être rejouée dans une matrice de scénarios.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `4. Ne jamais tester seulement “le meilleur cas”` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0008`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0041 — Taille

- Source: `SRC-001`
- Location: lines 1099–1110; heading `Taille`
- Domain tags: RISK
- Source statement: Taille: 100 € 250 €
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Taille` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0009`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0042 — Latence

- Source: `SRC-001`
- Location: lines 1111–1126; heading `Latence`
- Domain tags: ARCH
- Source statement: Latence: 0.5 ms si la donnée permet réellement de le simuler
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Latence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0001`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0044 — Inventaire

- Source: `SRC-001`
- Location: lines 1138–1169; heading `Inventaire`
- Domain tags: BRIDGE, ROUTING
- Source statement: Inventaire: asset de départ déjà disponible Une route n’est donc pas :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Inventaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BRIDGE-0001`; supporting items: none found by conservative heading match; domain indexes `BRIDGE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0045 — 5. Toujours comparer le théorique au réellement exécutable

- Source: `SRC-001`
- Location: lines 1170–1207; heading `5. Toujours comparer le théorique au réellement exécutable`
- Domain tags: EXECUTION, RISK, INFRA, ACCOUNTING, TRIANGLE
- Source statement: 5. Toujours comparer le théorique au réellement exécutable: C’était l’une des grandes leçons du bot Binance. Je garderais plusieurs niveaux de PnL :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `5. Toujours comparer le théorique au réellement exécutable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0010`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, ACCOUNTING, TRIANGLE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0046 — 6. Une hypothèse = une métrique = un critère de rejet

- Source: `SRC-001`
- Location: lines 1208–1210; heading `6. Une hypothèse = une métrique = un critère de rejet`
- Domain tags: RESEARCH, QUANT
- Source statement: 6. Une hypothèse = une métrique = un critère de rejet: C’est probablement la meilleure amélioration méthodologique qu’on puisse apporter maintenant.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `6. Une hypothèse = une métrique = un critère de rejet` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0002`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0047 — Hypothèse

- Source: `SRC-001`
- Location: lines 1211–1223; heading `Hypothèse`
- Domain tags: RESEARCH, INFRA, ACCOUNTING, ROUTING, HOT_WARM_COLD
- Source statement: Hypothèse: HOT/WARM/COLD réduit fortement le calcul sans perdre beaucoup de PnL.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Hypothèse` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0003`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, INFRA, ACCOUNTING, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0048 — Full graph

- Source: `SRC-001`
- Location: lines 1224–1231; heading `Full graph`
- Domain tags: GRAPH, INFRA, ACCOUNTING
- Source statement: Full graph: CPU = 100 PnL = 100 %
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Full graph` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-GRAPH-0003`; supporting items: none found by conservative heading match; domain indexes `GRAPH, INFRA, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0049 — HOT/WARM/COLD

- Source: `SRC-001`
- Location: lines 1232–1251; heading `HOT/WARM/COLD`
- Domain tags: HOT_WARM_COLD, INFRA, ACCOUNTING, BRIDGE
- Source statement: HOT/WARM/COLD: → notre activation est mauvaise. Même chose avec le Bridge Engine.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `HOT/WARM/COLD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0001`; supporting items: SRC-002-ITEM-0106, SRC-002-ITEM-0124, SRC-002-ITEM-0132, SRC-002-ITEM-0154; domain indexes `HOT_WARM_COLD, INFRA, ACCOUNTING, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0050 — Hypothèse

- Source: `SRC-001`
- Location: lines 1252–1275; heading `Hypothèse`
- Domain tags: RESEARCH, ACCOUNTING, BRIDGE
- Source statement: Hypothèse: déplacer BTC vers ETH vaut parfois le coût.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Hypothèse` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0004`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, ACCOUNTING, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0051 — 7. HOT/WARM/COLD doit être backtesté comme une stratégie

- Source: `SRC-001`
- Location: lines 1276–1279; heading `7. HOT/WARM/COLD doit être backtesté comme une stratégie`
- Domain tags: HOT_WARM_COLD
- Source statement: 7. HOT/WARM/COLD doit être backtesté comme une stratégie: Ce n’est pas seulement une optimisation informatique. On doit rejouer le même historique avec plusieurs politiques.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `7. HOT/WARM/COLD doit être backtesté comme une stratégie` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-HWC-0002`; supporting items: SRC-006-ITEM-0332, SRC-007-ITEM-0115; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0052 — Policy A

- Source: `SRC-001`
- Location: lines 1280–1281; heading `Policy A`
- Domain tags: HOT_WARM_COLD
- Source statement: Policy A: Tout HOT.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Policy A` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0003`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0053 — Policy B

- Source: `SRC-001`
- Location: lines 1282–1283; heading `Policy B`
- Domain tags: ARCH
- Source statement: Policy B: Seulement les marchés directement reliés à notre inventaire.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Policy B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0002`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0054 — Policy C

- Source: `SRC-001`
- Location: lines 1284–1292; heading `Policy C`
- Domain tags: HOT_WARM_COLD
- Source statement: Policy C: WARM = next-hop + anomalies
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Policy C` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0004`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0055 — Policy D

- Source: `SRC-001`
- Location: lines 1293–1304; heading `Policy D`
- Domain tags: INFRA, ACCOUNTING, BRIDGE, HOT_WARM_COLD
- Source statement: Policy D: Version plus agressive de WARM. Policy | CPU | PnL capturé | Missed Opps | Relocations
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Policy D` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0003`; supporting items: none found by conservative heading match; domain indexes `INFRA, ACCOUNTING, BRIDGE, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0056 — 8. Même chose pour le capital

- Source: `SRC-001`
- Location: lines 1305–1361; heading `8. Même chose pour le capital`
- Domain tags: CAPITAL, RISK, ACCOUNTING, REPLAY, INVENTORY, BRIDGE, TRIANGLE, GRAPH
- Source statement: 8. Même chose pour le capital: On ne teste pas seulement les trades. On teste le chemin du capital.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `8. Même chose pour le capital` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0002`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, RISK, ACCOUNTING, REPLAY, INVENTORY, BRIDGE, TRIANGLE, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0057 — 9. Le Bridge Engine doit avoir son propre protocole expérimental

- Source: `SRC-001`
- Location: lines 1362–1399; heading `9. Le Bridge Engine doit avoir son propre protocole expérimental`
- Domain tags: BRIDGE, ACCOUNTING, REPLAY, SURVIVAL, ROUTING
- Source statement: 9. Le Bridge Engine doit avoir son propre protocole expérimental: Avant de déplacer BTC → ETH : Et on enregistre ensuite ce qui s’est réellement produit.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `9. Le Bridge Engine doit avoir son propre protocole expérimental` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-BRIDGE-0002`; supporting items: SRC-006-ITEM-0373; domain indexes `BRIDGE, ACCOUNTING, REPLAY, SURVIVAL, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0058 — 10. Pas d’optimisation sur le même dataset que l’évaluation

- Source: `SRC-001`
- Location: lines 1400–1434; heading `10. Pas d’optimisation sur le même dataset que l’évaluation`
- Domain tags: DATA, INFRA, VALIDATION, FUTURE
- Source statement: 10. Pas d’optimisation sur le même dataset que l’évaluation: C’est un point méthodologique que je rendrais maintenant explicite. Si on regarde 30 jours Hyperliquid et qu’on choisit :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `10. Pas d’optimisation sur le même dataset que l’évaluation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-DATA-0001`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, VALIDATION, FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0059 — Walk-forward

- Source: `SRC-001`
- Location: lines 1435–1454; heading `Walk-forward`
- Domain tags: EXECUTION, MICROSTRUCTURE, CAPITAL, BRIDGE, HOT_WARM_COLD, QUANT
- Source statement: Walk-forward: calibrer N jours tester période suivante
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Walk-forward` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0011`; supporting items: SRC-006-ITEM-0482, SRC-007-ITEM-0091; domain indexes `EXECUTION, MICROSTRUCTURE, CAPITAL, BRIDGE, HOT_WARM_COLD, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0060 — 11. Ne pas optimiser uniquement le PnL

- Source: `SRC-001`
- Location: lines 1455–1476; heading `11. Ne pas optimiser uniquement le PnL`
- Domain tags: ACCOUNTING, EXECUTION, RISK, INFRA, INVENTORY, CAPITAL, BRIDGE
- Source statement: 11. Ne pas optimiser uniquement le PnL: Sinon on risque de créer une bombe. Chaque version doit être jugée sur plusieurs dimensions :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `11. Ne pas optimiser uniquement le PnL` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ACCT-0003`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, EXECUTION, RISK, INFRA, INVENTORY, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0061 — Version A

- Source: `SRC-001`
- Location: lines 1477–1484; heading `Version A`
- Domain tags: RISK, ACCOUNTING
- Source statement: Version A: PnL +15 % Drawdown -3 %
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Version A` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0010`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0062 — Version B

- Source: `SRC-001`
- Location: lines 1485–1494; heading `Version B`
- Domain tags: RISK, ACCOUNTING
- Source statement: Version B: Je ne prends pas automatiquement B.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Version B` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0011`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0063 — 12. Et surtout séparer les niveaux de PnL

- Source: `SRC-001`
- Location: lines 1495–1520; heading `12. Et surtout séparer les niveaux de PnL`
- Domain tags: ACCOUNTING, INVENTORY, BRIDGE, ROUTING
- Source statement: 12. Et surtout séparer les niveaux de PnL: On en a beaucoup parlé récemment. Méthodologiquement, on doit donc stocker :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `12. Et surtout séparer les niveaux de PnL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ACCT-0004`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, INVENTORY, BRIDGE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0064 — 13. Tests déterministes avant simulation marché

- Source: `SRC-001`
- Location: lines 1521–1524; heading `13. Tests déterministes avant simulation marché`
- Domain tags: ARCH
- Source statement: 13. Tests déterministes avant simulation marché: On avait déjà voulu une vraie parité backtest/live. Avant même les tests économiques :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `13. Tests déterministes avant simulation marché` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0003`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0065 — Unit tests

- Source: `SRC-001`
- Location: lines 1525–1537; heading `Unit tests`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: Unit tests: Exemple : 1000 USDC
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Unit tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0012`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0066 — Route test

- Source: `SRC-001`
- Location: lines 1538–1545; heading `Route test`
- Domain tags: ROUTING
- Source statement: Route test: BTC → HYPE → USDC résultat connu.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Route test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0001`; supporting items: none found by conservative heading match; domain indexes `ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0067 — Rounding tests

- Source: `SRC-001`
- Location: lines 1546–1550; heading `Rounding tests`
- Domain tags: ACCOUNTING, SIZING, QUANT
- Source statement: Rounding tests: * tick ; * quantity ;
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Rounding tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0005`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, SIZING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0068 — Partial fill tests

- Source: `SRC-001`
- Location: lines 1551–1559; heading `Partial fill tests`
- Domain tags: EXECUTION, RECOVERY
- Source statement: Partial fill tests: → Recovery Engine doit produire la bonne action.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Partial fill tests` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0013`; supporting items: SRC-004-ITEM-0052, SRC-004-ITEM-0055; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0069 — Crash recovery tests

- Source: `SRC-001`
- Location: lines 1560–1563; heading `Crash recovery tests`
- Domain tags: RECOVERY, OPERATIONS
- Source statement: Crash recovery tests: Tout cela doit être déterministe.
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Crash recovery tests` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RECOV-0003`; supporting items: none found by conservative heading match; domain indexes `RECOVERY, OPERATIONS`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0070 — 14. Puis tests adversariaux

- Source: `SRC-001`
- Location: lines 1564–1599; heading `14. Puis tests adversariaux`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, CLOCK, DEPLOYMENT, RESEARCH
- Source statement: 14. Puis tests adversariaux: On avait déjà parlé de stress tests, même avant les papiers. Le bon comportement n’est pas :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `14. Puis tests adversariaux` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0014`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, CLOCK, DEPLOYMENT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0071 — 15. Ensuite : Replay

- Source: `SRC-001`
- Location: lines 1600–1640; heading `15. Ensuite : Replay`
- Domain tags: REPLAY, RISK, ACCOUNTING, BRIDGE, GRAPH, HOT_WARM_COLD, PRODUCT, ARCH
- Source statement: 15. Ensuite : Replay: Seulement une fois les primitives validées. à la place de :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `15. Ensuite : Replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-REPLAY-0003`; supporting items: none found by conservative heading match; domain indexes `REPLAY, RISK, ACCOUNTING, BRIDGE, GRAPH, HOT_WARM_COLD, PRODUCT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0072 — 16. Paper n’est pas suffisant

- Source: `SRC-001`
- Location: lines 1641–1666; heading `16. Paper n’est pas suffisant`
- Domain tags: RESEARCH, EXECUTION, VALIDATION, REPLAY, MICROSTRUCTURE
- Source statement: 16. Paper n’est pas suffisant: Ça aussi était dans notre ancienne méthode. Le paper trading ne permet pas de mesurer réellement :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `16. Paper n’est pas suffisant` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-RESEARCH-0005`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, EXECUTION, VALIDATION, REPLAY, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0073 — 17. Différence Paper / Shadow

- Source: `SRC-001`
- Location: lines 1667–1668; heading `17. Différence Paper / Shadow`
- Domain tags: VALIDATION, RESEARCH
- Source statement: 17. Différence Paper / Shadow: Je la préciserais.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `17. Différence Paper / Shadow` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0004`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0074 — PAPER

- Source: `SRC-001`
- Location: lines 1669–1670; heading `PAPER`
- Domain tags: RESEARCH, ACCOUNTING
- Source statement: PAPER: Feed réel ou historique, broker simulé.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `PAPER` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RESEARCH-0006`; supporting items: none found by conservative heading match; domain indexes `RESEARCH, ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0075 — SHADOW

- Source: `SRC-001`
- Location: lines 1671–1692; heading `SHADOW`
- Domain tags: VALIDATION, EXECUTION, ACCOUNTING, INVENTORY
- Source statement: SHADOW: Le bot tourne exactement dans les conditions live : Si on avait envoyé maintenant, qu’aurait-on fait ?
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `SHADOW` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-VALID-0005`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, ACCOUNTING, INVENTORY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0076 — 18. Micro-live obligatoire

- Source: `SRC-001`
- Location: lines 1693–1734; heading `18. Micro-live obligatoire`
- Domain tags: VALIDATION, EXECUTION, INFRA, SIMULATOR, CAPITAL
- Source statement: 18. Micro-live obligatoire: Ça avait été prévu très tôt. On commence avec un capital suffisamment petit pour que les erreurs soient supportables.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `18. Micro-live obligatoire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0006`; supporting items: SRC-005-ITEM-0481, SRC-006-ITEM-0418; domain indexes `VALIDATION, EXECUTION, INFRA, SIMULATOR, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0077 — 19. Scaling par paliers

- Source: `SRC-001`
- Location: lines 1735–1769; heading `19. Scaling par paliers`
- Domain tags: EXECUTION, RISK, VALIDATION, ACCOUNTING, CAPITAL
- Source statement: 19. Scaling par paliers: Je préfère maintenant une méthode beaucoup plus rigoureuse : Mais chaque palier exige que :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `19. Scaling par paliers` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0015`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, VALIDATION, ACCOUNTING, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0078 — 20. Les critères GO / NO-GO doivent être définis avant les résultats

- Source: `SRC-001`
- Location: lines 1770–1800; heading `20. Les critères GO / NO-GO doivent être définis avant les résultats`
- Domain tags: VALIDATION, ACCOUNTING, RESEARCH
- Source statement: 20. Les critères GO / NO-GO doivent être définis avant les résultats: Très important pour éviter de nous raconter une histoire après coup. Avant une période de test, on écrit :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `20. Les critères GO / NO-GO doivent être définis avant les résultats` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-VALID-0007`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0079 — 21. On garde également les résultats négatifs

- Source: `SRC-001`
- Location: lines 1801–1824; heading `21. On garde également les résultats négatifs`
- Domain tags: EXECUTION, RECORDER, DATA
- Source statement: 21. On garde également les résultats négatifs: Le Recorder doit enregistrer : mais aussi tous les :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `21. On garde également les résultats négatifs` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0016`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, DATA`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0080 — 22. Versionner absolument tout

- Source: `SRC-001`
- Location: lines 1825–1844; heading `22. Versionner absolument tout`
- Domain tags: DATA, CLOCK, DETERMINISM, ACCOUNTING, REPLAY, MICROSTRUCTURE
- Source statement: 22. Versionner absolument tout: Chaque replay devrait produire quelque chose comme : Parce qu’on va rapidement avoir :
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `22. Versionner absolument tout` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0002`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, DETERMINISM, ACCOUNTING, REPLAY, MICROSTRUCTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0081 — 23. Le benchmark informatique fait partie de la méthodologie

- Source: `SRC-001`
- Location: lines 1845–1874; heading `23. Le benchmark informatique fait partie de la méthodologie`
- Domain tags: BENCHMARK, RISK, DEPLOYMENT, ACCOUNTING, MICROSTRUCTURE, ROUTING
- Source statement: 23. Le benchmark informatique fait partie de la méthodologie: Chaque version est benchmarkée : Notre objectif autour de 0,5 ms interne devient ainsi une métrique scientifique, pas une phrase marketing.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `23. Le benchmark informatique fait partie de la méthodologie` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BENCH-0003`; supporting items: none found by conservative heading match; domain indexes `BENCHMARK, RISK, DEPLOYMENT, ACCOUNTING, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0082 — 24. Méthodologie spécifique à notre Global Graph

- Source: `SRC-001`
- Location: lines 1875–1890; heading `24. Méthodologie spécifique à notre Global Graph`
- Domain tags: GRAPH, ACCOUNTING, ROUTING, RESEARCH
- Source statement: 24. Méthodologie spécifique à notre Global Graph: Notre graphe complet devient notre univers de recherche.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `24. Méthodologie spécifique à notre Global Graph` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-GRAPH-0004`; supporting items: none found by conservative heading match; domain indexes `GRAPH, ACCOUNTING, ROUTING, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0083 — CORE route

- Source: `SRC-001`
- Location: lines 1891–1892; heading `CORE route`
- Domain tags: ROUTING, ARCH
- Source statement: CORE route: Beaucoup d'opportunités / bonne profondeur.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `CORE route` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0002`; supporting items: none found by conservative heading match; domain indexes `ROUTING, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0084 — SECONDARY

- Source: `SRC-001`
- Location: lines 1893–1894; heading `SECONDARY`
- Domain tags: ARCH
- Source statement: SECONDARY: Occasionnelle mais intéressante.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `SECONDARY` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0004`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0085 — TRANSIT

- Source: `SRC-001`
- Location: lines 1895–1896; heading `TRANSIT`
- Domain tags: BRIDGE
- Source statement: TRANSIT: Principalement utile pour bridge.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `TRANSIT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BRIDGE-0003`; supporting items: none found by conservative heading match; domain indexes `BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0086 — REJECTED

- Source: `SRC-001`
- Location: lines 1897–1900; heading `REJECTED`
- Domain tags: HOT_WARM_COLD
- Source statement: REJECTED: Économiquement inutile ou trop risquée. Cela évite que HOT/WARM/COLD repose sur des règles arbitraires.
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `REJECTED` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-HWC-0005`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0087 — 25. Et on doit recalculer périodiquement cette cartographie

- Source: `SRC-001`
- Location: lines 1901–1928; heading `25. Et on doit recalculer périodiquement cette cartographie`
- Domain tags: GRAPH, VALIDATION, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 25. Et on doit recalculer périodiquement cette cartographie: Ce qu’on apprend le mois 1 peut devenir faux le mois 3. Donc la méthodologie inclut :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `25. Et on doit recalculer périodiquement cette cartographie` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-GRAPH-0005`; supporting items: none found by conservative heading match; domain indexes `GRAPH, VALIDATION, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0088 — 26. Notre méthode finale devient presque scientifique

- Source: `SRC-001`
- Location: lines 1929–2008; heading `26. Notre méthode finale devient presque scientifique`
- Domain tags: EXECUTION, RECORDER, INFRA, VALIDATION, ACCOUNTING, REPLAY, CAPITAL, BRIDGE
- Source statement: 26. Notre méthode finale devient presque scientifique: Je la résumerais en cette boucle : Global Graph / Market Atlas
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `26. Notre méthode finale devient presque scientifique` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0017`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, INFRA, VALIDATION, ACCOUNTING, REPLAY, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0089 — Et j'ajouterais une règle maîtresse pour notre direction actuelle

- Source: `SRC-001`
- Location: lines 2009–2010; heading `Et j'ajouterais une règle maîtresse pour notre direction actuelle`
- Domain tags: ARCH
- Source statement: Et j'ajouterais une règle maîtresse pour notre direction actuelle: Chaque nouvelle idée doit répondre à trois questions :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Et j'ajouterais une règle maîtresse pour notre direction actuelle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-ARCH-0005`; supporting items: SRC-002-ITEM-0120; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0090 — A — Est-ce que ça augmente l’Expected Economic PnL ?

- Source: `SRC-001`
- Location: lines 2011–2012; heading `A — Est-ce que ça augmente l’Expected Economic PnL ?`
- Domain tags: ACCOUNTING
- Source statement: A — Est-ce que ça augmente l’Expected Economic PnL ?: Pas le PnL théorique.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `A — Est-ce que ça augmente l’Expected Economic PnL ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0006`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0091 — B — Est-ce que ça améliore ou détériore le risque ?

- Source: `SRC-001`
- Location: lines 2013–2014; heading `B — Est-ce que ça améliore ou détériore le risque ?`
- Domain tags: INVENTORY, ROUTING
- Source statement: B — Est-ce que ça améliore ou détériore le risque ?: Leg / route / inventory / global.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `B — Est-ce que ça améliore ou détériore le risque ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INV-0001`; supporting items: none found by conservative heading match; domain indexes `INVENTORY, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0092 — C — Combien de calcul/latence ça coûte ?

- Source: `SRC-001`
- Location: lines 2015–2027; heading `C — Combien de calcul/latence ça coûte ?`
- Domain tags: INFRA, MICROSTRUCTURE, CAPITAL, BRIDGE, TRIANGLE, ROUTING, GRAPH, HOT_WARM_COLD
- Source statement: C — Combien de calcul/latence ça coûte ?: Parce qu’un modèle qui améliore de : 3 ms au hot path
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `C — Combien de calcul/latence ça coûte ?` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0004`; supporting items: none found by conservative heading match; domain indexes `INFRA, MICROSTRUCTURE, CAPITAL, BRIDGE, TRIANGLE, ROUTING, GRAPH, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0093 — 1. Le graphe structurel est mis à jour dès que Hyperliquid change

- Source: `SRC-001`
- Location: lines 2028–2056; heading `1. Le graphe structurel est mis à jour dès que Hyperliquid change`
- Domain tags: GRAPH, BRIDGE, ROUTING
- Source statement: 1. Le graphe structurel est mis à jour dès que Hyperliquid change: On conserve en permanence : Si Hyperliquid ajoute/supprime une paire ou modifie ses métadonnées :
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `1. Le graphe structurel est mis à jour dès que Hyperliquid change` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-GRAPH-0006`; supporting items: none found by conservative heading match; domain indexes `GRAPH, BRIDGE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0094 — 2. En temps réel, le bot maintient des statistiques courtes

- Source: `SRC-001`
- Location: lines 2057–2093; heading `2. En temps réel, le bot maintient des statistiques courtes`
- Domain tags: EXECUTION, RECORDER, ACCOUNTING, MICROSTRUCTURE, ROUTING
- Source statement: 2. En temps réel, le bot maintient des statistiques courtes: Le Recorder alimente constamment des métriques par marché, asset, route et cluster. Par exemple pour HYPE/USDC :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `2. En temps réel, le bot maintient des statistiques courtes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0018`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, ACCOUNTING, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0095 — 3. On garde plusieurs fenêtres en parallèle

- Source: `SRC-001`
- Location: lines 2094–2116; heading `3. On garde plusieurs fenêtres en parallèle`
- Domain tags: FUTURE
- Source statement: 3. On garde plusieurs fenêtres en parallèle: « les 30 derniers jours ». Parce que ça réagit trop lentement.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `3. On garde plusieurs fenêtres en parallèle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0001`; supporting items: none found by conservative heading match; domain indexes `FUTURE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0096 — FAST

- Source: `SRC-001`
- Location: lines 2117–2129; heading `FAST`
- Domain tags: HOT_WARM_COLD
- Source statement: FAST: Quelque chose vient-il de changer brutalement ? → peut provoquer COLD → WARM.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `FAST` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0006`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0097 — RECENT

- Source: `SRC-001`
- Location: lines 2130–2140; heading `RECENT`
- Domain tags: ACCOUNTING, MICROSTRUCTURE, BRIDGE
- Source statement: RECENT: Est-ce que le changement semble durer ? ETH profitable depuis 2 h
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `RECENT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0007`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, MICROSTRUCTURE, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0098 — MEDIUM

- Source: `SRC-001`
- Location: lines 2141–2151; heading `MEDIUM`
- Domain tags: CAPITAL, ARCH
- Source statement: MEDIUM: Est-ce devenu un vrai régime de marché ? HYPE cluster performant depuis 4 jours
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `MEDIUM` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0003`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0099 — LONG

- Source: `SRC-001`
- Location: lines 2152–2159; heading `LONG`
- Domain tags: ARCH
- Source statement: LONG: Cet asset reste-t-il structurellement intéressant ? * CORE / TRANSIT / EXCLUDED ;
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `LONG` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0006`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0100 — 4. Exemple concret : ETH devient soudain intéressant

- Source: `SRC-001`
- Location: lines 2160–2204; heading `4. Exemple concret : ETH devient soudain intéressant`
- Domain tags: ACCOUNTING, INVENTORY, BRIDGE, HOT_WARM_COLD
- Source statement: 4. Exemple concret : ETH devient soudain intéressant: Inventory = 1000 € BTC Le Global Watcher constate :
- Nature: rejected approach
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `4. Exemple concret : ETH devient soudain intéressant` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-ACCT-0008`; supporting items: SRC-002-ITEM-0064; domain indexes `ACCOUNTING, INVENTORY, BRIDGE, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0101 — 5. WARM sert précisément à confirmer

- Source: `SRC-001`
- Location: lines 2205–2268; heading `5. WARM sert précisément à confirmer`
- Domain tags: HOT_WARM_COLD, ACCOUNTING, CAPITAL, BRIDGE, TRIANGLE, ROUTING, QUANT, ARCH
- Source statement: 5. WARM sert précisément à confirmer: Une fois ETH WARM : on active davantage de calcul :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `5. WARM sert précisément à confirmer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0007`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD, ACCOUNTING, CAPITAL, BRIDGE, TRIANGLE, ROUTING, QUANT, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0102 — 6. Pourquoi je disais « ne pas modifier automatiquement les réglages dans le hot path »

- Source: `SRC-001`
- Location: lines 2269–2270; heading `6. Pourquoi je disais « ne pas modifier automatiquement les réglages dans le hot path »`
- Domain tags: ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 6. Pourquoi je disais « ne pas modifier automatiquement les réglages dans le hot path »: Il faut distinguer deux choses.
- Nature: rationale
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `6. Pourquoi je disais « ne pas modifier automatiquement les réglages dans le hot path »` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0003`; supporting items: none found by conservative heading match; domain indexes `ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0103 — Ça peut être automatique en live :

- Source: `SRC-001`
- Location: lines 2271–2291; heading `Ça peut être automatique en live :`
- Domain tags: CAPITAL, BRIDGE, ROUTING, HOT_WARM_COLD
- Source statement: Ça peut être automatique en live :: Parce que ce sont des décisions prévues par notre stratégie. Le moteur est justement fait pour prendre ces décisions automatiquement.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Ça peut être automatique en live :` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CAP-0004`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, BRIDGE, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0104 — Ce que je ne veux PAS :

- Source: `SRC-001`
- Location: lines 2292–2324; heading `Ce que je ne veux PAS :`
- Domain tags: INFRA, VALIDATION, INVENTORY, QUANT
- Source statement: Ce que je ne veux PAS :: Que le bot observe 20 mauvaises minutes et fasse lui-même : je le change à 0.03 %
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Ce que je ne veux PAS :` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0005`; supporting items: none found by conservative heading match; domain indexes `INFRA, VALIDATION, INVENTORY, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0106 — A. Dynamic State

- Source: `SRC-001`
- Location: lines 2326–2342; heading `A. Dynamic State`
- Domain tags: ACCOUNTING, INVENTORY, BRIDGE, ROUTING, HOT_WARM_COLD, QUANT
- Source statement: A. Dynamic State: Change automatiquement en permanence :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `A. Dynamic State` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0009`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING, INVENTORY, BRIDGE, ROUTING, HOT_WARM_COLD, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0107 — B. Strategy Parameters

- Source: `SRC-001`
- Location: lines 2343–2360; heading `B. Strategy Parameters`
- Domain tags: INFRA, RISK, VALIDATION, MICROSTRUCTURE, INVENTORY, BRIDGE, HOT_WARM_COLD, QUANT
- Source statement: B. Strategy Parameters: Ne changent qu’après validation : Ce sont les règles qui interprètent le marché.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `B. Strategy Parameters` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0006`; supporting items: none found by conservative heading match; domain indexes `INFRA, RISK, VALIDATION, MICROSTRUCTURE, INVENTORY, BRIDGE, HOT_WARM_COLD, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0108 — 8. Comment actualiser ces paramètres alors ?

- Source: `SRC-001`
- Location: lines 2361–2430; heading `8. Comment actualiser ces paramètres alors ?`
- Domain tags: EXECUTION, INFRA, RISK, RECORDER, DATA, VALIDATION, ACCOUNTING, REPLAY
- Source statement: 8. Comment actualiser ces paramètres alors ?: Automatiquement côté recherche, mais pas automatiquement côté production. Nos données des deux dernières semaines montrent qu’un seuil de :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `8. Comment actualiser ces paramètres alors ?` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0019`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, RISK, RECORDER, DATA, VALIDATION, ACCOUNTING, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0109 — 9. On peut même faire du Champion / Challenger

- Source: `SRC-001`
- Location: lines 2431–2474; heading `9. On peut même faire du Champion / Challenger`
- Domain tags: FUTURE, EXECUTION, RISK, BENCHMARK, ACCOUNTING, PRODUCT
- Source statement: 9. On peut même faire du Champion / Challenger: Je pense que ce serait très bien pour notre projet. En parallèle, sans envoyer d’ordres :
- Nature: edge-case/failure behaviour
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `9. On peut même faire du Champion / Challenger` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-FUTURE-0002`; supporting items: SRC-005-ITEM-0455, SRC-007-ITEM-0046, SRC-008-ITEM-0085; domain indexes `FUTURE, EXECUTION, RISK, BENCHMARK, ACCOUNTING, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0110 — 10. Et la cartographie elle-même devient un score roulant

- Source: `SRC-001`
- Location: lines 2475–2502; heading `10. Et la cartographie elle-même devient un score roulant`
- Domain tags: GRAPH, ARCH, RISK, ACCOUNTING, BRIDGE, QUANT
- Source statement: 10. Et la cartographie elle-même devient un score roulant: Par exemple pour ETH : Mais chaque composante existe sur plusieurs horizons :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `10. Et la cartographie elle-même devient un score roulant` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-GRAPH-0007`; supporting items: none found by conservative heading match; domain indexes `GRAPH, ARCH, RISK, ACCOUNTING, BRIDGE, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0111 — Boom temporaire

- Source: `SRC-001`
- Location: lines 2503–2512; heading `Boom temporaire`
- Domain tags: HOT_WARM_COLD
- Source statement: Boom temporaire: → WARM / opportunité tactique.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Boom temporaire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0008`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0112 — Amélioration structurelle

- Source: `SRC-001`
- Location: lines 2513–2525; heading `Amélioration structurelle`
- Domain tags: ARCH
- Source statement: Amélioration structurelle: → potentiellement augmenter progressivement son importance stratégique.
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Amélioration structurelle` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0007`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0113 — 11. Et l’hystérésis empêche le bot de devenir fou

- Source: `SRC-001`
- Location: lines 2526–2577; heading `11. Et l’hystérésis empêche le bot de devenir fou`
- Domain tags: CAPITAL, BRIDGE, HOT_WARM_COLD, ARCH
- Source statement: 11. Et l’hystérésis empêche le bot de devenir fou: Très important pour notre Capital Relocation Engine. On ne veut pas :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `11. Et l’hystérésis empêche le bot de devenir fou` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-CAP-0005`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, BRIDGE, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0114 — 12. Au final, notre système fonctionne sur trois vitesses

- Source: `SRC-001`
- Location: lines 2578–2634; heading `12. Au final, notre système fonctionne sur trois vitesses`
- Domain tags: EXECUTION, RISK, VALIDATION, REPLAY, CAPITAL, BRIDGE, TRIANGLE, ROUTING
- Source statement: 12. Au final, notre système fonctionne sur trois vitesses: Replay → Validation → Shadow → Production. La “mise à jour” doit fonctionner comme un pipeline événementiel. On ne recalcule pas toute la carte de zéro en permanence.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `12. Au final, notre système fonctionne sur trois vitesses` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0020`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, VALIDATION, REPLAY, CAPITAL, BRIDGE, TRIANGLE, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0115 — Exemple simple

- Source: `SRC-001`
- Location: lines 2635–2669; heading `Exemple simple`
- Domain tags: EXECUTION, CAPITAL, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: Exemple simple: et notre capital est actuellement en BTC. Hyperliquid envoie une mise à jour de HYPE/ETH.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Exemple simple` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-EXEC-0021`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CAPITAL, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0116 — 1. La carte structurelle change rarement

- Source: `SRC-001`
- Location: lines 2670–2715; heading `1. La carte structurelle change rarement`
- Domain tags: DEPLOYMENT, ROUTING, GRAPH
- Source statement: 1. La carte structurelle change rarement: On a d'abord une carte de base : construite avec les marchés disponibles.
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `1. La carte structurelle change rarement` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DEPLOY-0001`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ROUTING, GRAPH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0117 — 2. Ce qui change tout le temps, c'est le MarketState

- Source: `SRC-001`
- Location: lines 2716–2754; heading `2. Ce qui change tout le temps, c'est le MarketState`
- Domain tags: INFRA, DEPLOYMENT, QUANT
- Source statement: 2. Ce qui change tout le temps, c'est le MarketState: Pour chaque marché on garde un état en RAM : Quand un nouveau carnet arrive :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `2. Ce qui change tout le temps, c'est le MarketState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-INFRA-0007`; supporting items: none found by conservative heading match; domain indexes `INFRA, DEPLOYMENT, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0118 — 3. Les fenêtres sont mises à jour progressivement

- Source: `SRC-001`
- Location: lines 2755–2810; heading `3. Les fenêtres sont mises à jour progressivement`
- Domain tags: ACCOUNTING
- Source statement: 3. Les fenêtres sont mises à jour progressivement: On ne reprend pas 30 jours de données et on recalcule tout. On utilise des rolling windows.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `3. Les fenêtres sont mises à jour progressivement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ACCT-0010`; supporting items: none found by conservative heading match; domain indexes `ACCOUNTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0119 — 4. Les routes sont également mises à jour par dépendance

- Source: `SRC-001`
- Location: lines 2811–2843; heading `4. Les routes sont également mises à jour par dépendance`
- Domain tags: ROUTING, DEPLOYMENT, ACCOUNTING, GRAPH, HOT_WARM_COLD
- Source statement: 4. Les routes sont également mises à jour par dépendance: C'est là que pair_to_routes devient important. Donc une update HYPE/ETH déclenche uniquement ces routes.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `4. Les routes sont également mises à jour par dépendance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ROUTE-0004`; supporting items: none found by conservative heading match; domain indexes `ROUTING, DEPLOYMENT, ACCOUNTING, GRAPH, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0120 — 5. Ensuite on met à jour le score de l'asset/cluster

- Source: `SRC-001`
- Location: lines 2844–2887; heading `5. Ensuite on met à jour le score de l'asset/cluster`
- Domain tags: ARCH, EXECUTION, ACCOUNTING, TRIANGLE, HOT_WARM_COLD
- Source statement: 5. Ensuite on met à jour le score de l'asset/cluster: Supposons que ETH était : Les dernières minutes changent :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `5. Ensuite on met à jour le score de l'asset/cluster` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-ARCH-0008`; supporting items: none found by conservative heading match; domain indexes `ARCH, EXECUTION, ACCOUNTING, TRIANGLE, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0121 — 6. WARM déclenche ensuite une analyse plus poussée

- Source: `SRC-001`
- Location: lines 2888–2971; heading `6. WARM déclenche ensuite une analyse plus poussée`
- Domain tags: HOT_WARM_COLD, EXECUTION, INFRA, ACCOUNTING, CAPITAL, BRIDGE, ROUTING, QUANT
- Source statement: 6. WARM déclenche ensuite une analyse plus poussée: Le système augmente automatiquement les ressources consacrées à ETH : notre capital est en BTC, est-ce que ça vaut le coup d'aller en ETH ?
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `6. WARM déclenche ensuite une analyse plus poussée` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0009`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD, EXECUTION, INFRA, ACCOUNTING, CAPITAL, BRIDGE, ROUTING, QUANT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0122 — 7. Après le déplacement, la carte se met encore à jour

- Source: `SRC-001`
- Location: lines 2972–3015; heading `7. Après le déplacement, la carte se met encore à jour`
- Domain tags: ARCH, INVENTORY, CAPITAL, ROUTING, HOT_WARM_COLD
- Source statement: 7. Après le déplacement, la carte se met encore à jour: Cet événement déclenche immédiatement : quelles routes sont maintenant directement utilisables ?
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `7. Après le déplacement, la carte se met encore à jour` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0009`; supporting items: none found by conservative heading match; domain indexes `ARCH, INVENTORY, CAPITAL, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0123 — 8. Et quand ETH devient mauvais ?

- Source: `SRC-001`
- Location: lines 3016–3061; heading `8. Et quand ETH devient mauvais ?`
- Domain tags: HOT_WARM_COLD, ARCH
- Source statement: 8. Et quand ETH devient mauvais ?: Même mécanisme dans l'autre sens. On ne veut pas :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `8. Et quand ETH devient mauvais ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0010`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0124 — 9. Ce qui NE se met pas à jour automatiquement

- Source: `SRC-001`
- Location: lines 3062–3126; heading `9. Ce qui NE se met pas à jour automatiquement`
- Domain tags: INFRA, VALIDATION, REPLAY, INVENTORY, HOT_WARM_COLD, PRODUCT
- Source statement: 9. Ce qui NE se met pas à jour automatiquement: Imaginons que notre stratégie utilise : Ces paramètres ne changent pas parce que le marché bouge.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `9. Ce qui NE se met pas à jour automatiquement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0008`; supporting items: none found by conservative heading match; domain indexes `INFRA, VALIDATION, REPLAY, INVENTORY, HOT_WARM_COLD, PRODUCT`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0126 — Mise à jour marché — permanente

- Source: `SRC-001`
- Location: lines 3128–3146; heading `Mise à jour marché — permanente`
- Domain tags: INVENTORY, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: Mise à jour marché — permanente: Toutes les ms/s : carnet
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Mise à jour marché — permanente` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-INV-0002`; supporting items: SRC-006-ITEM-0274; domain indexes `INVENTORY, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

### SRC-001-ITEM-0127 — Mise à jour stratégique — contrôlée

- Source: `SRC-001`
- Location: lines 3147–3172; heading `Mise à jour stratégique — contrôlée`
- Domain tags: RISK, VALIDATION, REPLAY, PRODUCT, RESEARCH
- Source statement: Mise à jour stratégique — contrôlée: Toutes les heures/jours/semaines selon besoin :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Mise à jour stratégique — contrôlée` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0012`; supporting items: SRC-006-ITEM-0274; domain indexes `RISK, VALIDATION, REPLAY, PRODUCT, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0128 — Exemple complet en 30 secondes de marché

- Source: `SRC-001`
- Location: lines 3173–3264; heading `Exemple complet en 30 secondes de marché`
- Domain tags: EXECUTION, RISK, RECORDER, VALIDATION, REPLAY, INVENTORY, CAPITAL, BRIDGE
- Source statement: Exemple complet en 30 secondes de marché: Plusieurs routes ETH deviennent positives → ETH score dépasse COLD threshold.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Exemple complet en 30 secondes de marché` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-EXEC-0022`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, RECORDER, VALIDATION, REPLAY, INVENTORY, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0129 — 1. Jour 1 : on construit la couche “observation”

- Source: `SRC-001`
- Location: lines 3265–3303; heading `1. Jour 1 : on construit la couche “observation”`
- Domain tags: EXECUTION, RECORDER, ACCOUNTING, BRIDGE, ROUTING, GRAPH, ARCH
- Source statement: 1. Jour 1 : on construit la couche “observation”: Premier morceau de Rust : Le Global Graph récupère par exemple :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `1. Jour 1 : on construit la couche “observation”` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0023`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, ACCOUNTING, BRIDGE, ROUTING, GRAPH, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0130 — 2. Pendant ce temps, le Recorder tourne 24/7

- Source: `SRC-001`
- Location: lines 3304–3337; heading `2. Pendant ce temps, le Recorder tourne 24/7`
- Domain tags: EXECUTION, RECORDER, CLOCK, BENCHMARK, ACCOUNTING, ROUTING
- Source statement: 2. Pendant ce temps, le Recorder tourne 24/7: Donc après quelques jours on commence à avoir : Et on peut commencer à dire :
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `2. Pendant ce temps, le Recorder tourne 24/7` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0024`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, CLOCK, BENCHMARK, ACCOUNTING, ROUTING`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0131 — Carte structurelle

- Source: `SRC-001`
- Location: lines 3338–3345; heading `Carte structurelle`
- Domain tags: ARCH
- Source statement: Carte structurelle: BTC → HYPE → ETH et :
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Carte structurelle` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0010`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0132 — Carte économique

- Source: `SRC-001`
- Location: lines 3346–3358; heading `Carte économique`
- Domain tags: ARCH
- Source statement: Carte économique: BTC → HYPE → ETH opportunities/day = X
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Carte économique` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0011`; supporting items: SRC-002-ITEM-0048; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0133 — 3. On ne reste pas à attendre que le dataset soit terminé

- Source: `SRC-001`
- Location: lines 3359–3407; heading `3. On ne reste pas à attendre que le dataset soit terminé`
- Domain tags: DATA, EXECUTION, RISK, RECORDER, ACCOUNTING, REPLAY, INVENTORY, CAPITAL
- Source statement: 3. On ne reste pas à attendre que le dataset soit terminé: Je ne ferais pas : On fait en parallèle :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `3. On ne reste pas à attendre que le dataset soit terminé` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0003`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RISK, RECORDER, ACCOUNTING, REPLAY, INVENTORY, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0134 — 4. Première utilisation des données : construire le Market Atlas

- Source: `SRC-001`
- Location: lines 3408–3452; heading `4. Première utilisation des données : construire le Market Atlas`
- Domain tags: MARKET_ATLAS, RISK, ACCOUNTING, BRIDGE, ROUTING, GRAPH, HOT_WARM_COLD, ARCH
- Source statement: 4. Première utilisation des données : construire le Market Atlas: À ce moment-là on combine : Asset | Routes 2L | Cycles 3L | Opps/h | Depth | Idle risk | Bridge cost
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `4. Première utilisation des données : construire le Market Atlas` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ATLAS-0001`; supporting items: SRC-006-ITEM-0330; domain indexes `MARKET_ATLAS, RISK, ACCOUNTING, BRIDGE, ROUTING, GRAPH, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0135 — 5. Ensuite le Replay Engine prend exactement ces données

- Source: `SRC-001`
- Location: lines 3453–3492; heading `5. Ensuite le Replay Engine prend exactement ces données`
- Domain tags: REPLAY, RISK, CLOCK, ACCOUNTING, SIMULATOR, INVENTORY, CAPITAL, BRIDGE
- Source statement: 5. Ensuite le Replay Engine prend exactement ces données: C'est ici qu'on commence réellement à tester notre bot. Supposons qu'on possède 7 jours enregistrés.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `5. Ensuite le Replay Engine prend exactement ces données` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-REPLAY-0004`; supporting items: SRC-006-ITEM-0409; domain indexes `REPLAY, RISK, CLOCK, ACCOUNTING, SIMULATOR, INVENTORY, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0136 — 6. Et on regarde comment son capital se déplace réellement

- Source: `SRC-001`
- Location: lines 3493–3550; heading `6. Et on regarde comment son capital se déplace réellement`
- Domain tags: CAPITAL, EXECUTION, ACCOUNTING, REPLAY, BRIDGE, ROUTING, HOT_WARM_COLD
- Source statement: 6. Et on regarde comment son capital se déplace réellement: Puis le replay décide : parce que le cluster BTC devient intéressant.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `6. Et on regarde comment son capital se déplace réellement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0006`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, EXECUTION, ACCOUNTING, REPLAY, BRIDGE, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0137 — 7. Ensuite on rejoue la même semaine avec différentes politiques

- Source: `SRC-001`
- Location: lines 3551–3555; heading `7. Ensuite on rejoue la même semaine avec différentes politiques`
- Domain tags: DATA, CAPITAL
- Source statement: 7. Ensuite on rejoue la même semaine avec différentes politiques: C'est là que notre dataset devient extrêmement précieux.
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `7. Ensuite on rejoue la même semaine avec différentes politiques` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0004`; supporting items: none found by conservative heading match; domain indexes `DATA, CAPITAL`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0138 — Test A

- Source: `SRC-001`
- Location: lines 3556–3563; heading `Test A`
- Domain tags: HOT_WARM_COLD
- Source statement: Test A: No HOT/WARM/COLD tout scanner
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Test A` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0011`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0139 — Test B

- Source: `SRC-001`
- Location: lines 3564–3570; heading `Test B`
- Domain tags: HOT_WARM_COLD
- Source statement: Test B: HOT/WARM/COLD
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Test B` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-HWC-0012`; supporting items: none found by conservative heading match; domain indexes `HOT_WARM_COLD`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0140 — Test C

- Source: `SRC-001`
- Location: lines 3571–3577; heading `Test C`
- Domain tags: BRIDGE
- Source statement: Test C: pas de relocation
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Test C` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-BRIDGE-0004`; supporting items: none found by conservative heading match; domain indexes `BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0141 — Test D

- Source: `SRC-001`
- Location: lines 3578–3584; heading `Test D`
- Domain tags: CAPITAL, BRIDGE
- Source statement: Test D: Capital Relocation
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Test D` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-CAP-0007`; supporting items: none found by conservative heading match; domain indexes `CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0142 — Test E

- Source: `SRC-001`
- Location: lines 3585–3591; heading `Test E`
- Domain tags: ARCH
- Source statement: Test E: TT seulement
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Test E` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-ARCH-0012`; supporting items: none found by conservative heading match; domain indexes `ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0143 — Test F

- Source: `SRC-001`
- Location: lines 3592–3615; heading `Test F`
- Domain tags: RISK, INFRA, ACCOUNTING, INVENTORY, CAPITAL, BRIDGE
- Source statement: Test F: C'est comme ça qu'on prouve que chaque brique apporte réellement quelque chose.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Test F` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0013`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, ACCOUNTING, INVENTORY, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0144 — 8. Ensuite seulement on calibre les paramètres

- Source: `SRC-001`
- Location: lines 3616–3658; heading `8. Ensuite seulement on calibre les paramètres`
- Domain tags: INFRA, DATA, VALIDATION, BRIDGE, HOT_WARM_COLD, ARCH
- Source statement: 8. Ensuite seulement on calibre les paramètres: Par exemple les données montrent peut-être : n'est intéressant que si :
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `8. Ensuite seulement on calibre les paramètres` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-INFRA-0009`; supporting items: none found by conservative heading match; domain indexes `INFRA, DATA, VALIDATION, BRIDGE, HOT_WARM_COLD, ARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0145 — 9. Puis le Shadow

- Source: `SRC-001`
- Location: lines 3659–3682; heading `9. Puis le Shadow`
- Domain tags: VALIDATION, EXECUTION, INFRA, REPLAY, ARCH, FUTURE, RESEARCH
- Source statement: 9. Puis le Shadow: le vrai programme Rust tourne sur le vrai Hyperliquid. Donc on voit en live :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `9. Puis le Shadow` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-VALID-0008`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, INFRA, REPLAY, ARCH, FUTURE, RESEARCH`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0146 — 10. Puis Micro-live

- Source: `SRC-001`
- Location: lines 3683–3710; heading `10. Puis Micro-live`
- Domain tags: VALIDATION, EXECUTION, INFRA, ACCOUNTING, CAPITAL, BRIDGE
- Source statement: 10. Puis Micro-live: Seulement là on met réellement un petit capital. Si simulation et réalité correspondent suffisamment :
- Nature: decision/policy/concept
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `10. Puis Micro-live` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0009`; supporting items: SRC-005-ITEM-0481, SRC-006-ITEM-0418; domain indexes `VALIDATION, EXECUTION, INFRA, ACCOUNTING, CAPITAL, BRIDGE`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0147 — Donc la chronologie exacte que je recommande

- Source: `SRC-001`
- Location: lines 3711–3830; heading `Donc la chronologie exacte que je recommande`
- Domain tags: EXECUTION, RISK, RECORDER, DATA, VALIDATION, ACCOUNTING, SIMULATOR, REPLAY
- Source statement: Donc la chronologie exacte que je recommande: Pendant que Recorder tourne :
- Nature: data/architecture contract
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Donc la chronologie exacte que je recommande` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-EXEC-0025`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, RECORDER, DATA, VALIDATION, ACCOUNTING, SIMULATOR, REPLAY`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-001-ITEM-0148 — Donc la correction importante à ta phrase :

- Source: `SRC-001`
- Location: lines 3831–5255; heading `Donc la correction importante à ta phrase :`
- Domain tags: FORMULA, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, DATA, CLOCK
- Source statement: Donc la correction importante à ta phrase :: on enregistre → on construit le graphe à partir de l'enregistrement → on build le bot. on construit le graphe structurel immédiatement à partir de l’univers Hyperliquid, on commence immédiatement à enregistrer le comportement de ce graphe, puis on construit le bot pendant que les données s’accumulent. Ensuite ces données servent à transformer notre graphe structurel en carte économique et à tester le même bot Rust en replay avant le live.
- Nature: protocol/validation
- Temporal interpretation: refinement
- Authority: Exploratory consolidation and production rationale; closure dossiers prevail in their domains.
- Candidate canonical interpretation: Preserve `Donc la correction importante à ta phrase :` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `EXTERNAL_REVALIDATION`
- Cross-source references: `REQ-FORMULA-0001`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, DATA, CLOCK`.
- Potential conflicts: Closure authority check required against later sources.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: YES.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 145
- Requirements contributed: 145
- Supporting references contributed: 33 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 1
- Research items: 83
- Open items: 1
- External revalidation items: 10
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
