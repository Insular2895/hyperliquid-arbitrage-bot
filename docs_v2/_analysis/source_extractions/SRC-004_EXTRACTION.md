# SRC-004 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-004`
- Filename: `DOSSIER 16 — EXECUTION STATE MACHINE.md`
- SHA-256: `df5b1720a26889fce2a74fbc380bad4bda2e2aacdb4f02054c7270e5eb04b5b9`
- Line count: 9953
- Authority profile: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Main domains: EXECUTION, FORMULA, ACCOUNTING, RECOVERY, RISK, ROUTING, INVENTORY, QUANT, RECONCILIATION, INFRA, ARCH, MICROSTRUCTURE
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-004-ITEM-0004 — 1. Objectif

- Source: `SRC-004`
- Location: lines 4–32; heading `1. Objectif`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: 1. Objectif: L’Execution State Machine est la couche qui transforme : Son objectif principal n’est pas de maximiser le nombre d’ordres envoyés.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `1. Objectif` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0098`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0005 — 2. Principe fondamental : la stratégie ne contrôle jamais directement l’exchange

- Source: `SRC-004`
- Location: lines 33–55; heading `2. Principe fondamental : la stratégie ne contrôle jamais directement l’exchange`
- Domain tags: EXECUTION, FORMULA, RECOVERY, RECONCILIATION
- Source statement: 2. Principe fondamental : la stratégie ne contrôle jamais directement l’exchange: La séparation doit être : La stratégie formule une intention économique.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `2. Principe fondamental : la stratégie ne contrôle jamais directement l’exchange` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0099`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, FORMULA, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0006 — 3. Les cinq automates distincts

- Source: `SRC-004`
- Location: lines 56–69; heading `3. Les cinq automates distincts`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, ROUTING
- Source statement: 3. Les cinq automates distincts: Je recommande de ne surtout pas construire un seul énorme enum contenant 80 états. On sépare cinq state machines coordonnées :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `3. Les cinq automates distincts` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0100`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0007 — 4. EngineState — état global du bot

- Source: `SRC-004`
- Location: lines 70–90; heading `4. EngineState — état global du bot`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION
- Source statement: 4. EngineState — état global du bot: BOOTING SYNCING
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `4. EngineState — état global du bot` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0101`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0008 — 5. BOOTING

- Source: `SRC-004`
- Location: lines 91–116; heading `5. BOOTING`
- Domain tags: EXECUTION, RECORDER, SECURITY
- Source statement: 5. BOOTING: Le processus vient de démarrer.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `5. BOOTING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0102`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECORDER, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0009 — 6. SYNCING

- Source: `SRC-004`
- Location: lines 117–151; heading `6. SYNCING`
- Domain tags: EXECUTION, RECONCILIATION, CLOCK, DEPLOYMENT, OPERATIONS, ACCOUNTING
- Source statement: 6. SYNCING: Le bot reconnecte toutes les sources nécessaires. Hyperliquid fournit notamment les subscriptions WebSocket orderUpdates, userFills, openOrders et spotState. Les snapshots initiaux de certaines subscriptions utilisateur permettent aussi de récupérer les événements manqués après reconnexion.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `6. SYNCING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0103`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, CLOCK, DEPLOYMENT, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0010 — 7. RECONCILING

- Source: `SRC-004`
- Location: lines 152–188; heading `7. RECONCILING`
- Domain tags: EXECUTION, RECONCILIATION, INVENTORY
- Source statement: 7. RECONCILING: Le bot récupère la vérité actuelle de l’exchange : order statuses for unresolved orders
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `7. RECONCILING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0104`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0011 — 8. READY

- Source: `SRC-004`
- Location: lines 189–207; heading `8. READY`
- Domain tags: EXECUTION, RECONCILIATION, RISK, CLOCK, SECURITY, OPERATIONS
- Source statement: 8. READY: READY signifie exactement : market state valid
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `8. READY` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0105`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, RISK, CLOCK, SECURITY, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0012 — 9. DEGRADED

- Source: `SRC-004`
- Location: lines 208–224; heading `9. DEGRADED`
- Domain tags: EXECUTION, RISK, RECORDER, ARCH
- Source statement: 9. DEGRADED: Un composant secondaire est dégradé mais le système est encore capable de gérer ses positions. Les conditions exactes seront définies dans la Risk Constitution.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `9. DEGRADED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0106`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, RECORDER, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0013 — 10. RECOVERY_ONLY

- Source: `SRC-004`
- Location: lines 225–256; heading `10. RECOVERY_ONLY`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, RISK, INFRA, ACCOUNTING, INVENTORY
- Source statement: 10. RECOVERY_ONLY: Le bot n’a plus le droit de prendre une nouvelle opportunité. Mais il doit pouvoir :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `10. RECOVERY_ONLY` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0107`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, RISK, INFRA, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0014 — 11. HALTED

- Source: `SRC-004`
- Location: lines 257–277; heading `11. HALTED`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION
- Source statement: 11. HALTED: Seules certaines actions de sécurité restent permises : Le passage HALTED → READY nécessite toujours une nouvelle reconciliation.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `11. HALTED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0108`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0015 — 12. RouteExecutionState

- Source: `SRC-004`
- Location: lines 278–308; heading `12. RouteExecutionState`
- Domain tags: EXECUTION, ROUTING, RECOVERY, RECONCILIATION
- Source statement: 12. RouteExecutionState: Chaque opportunité réellement sélectionnée reçoit :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `12. RouteExecutionState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0109`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0016 — 13. DETECTED

- Source: `SRC-004`
- Location: lines 309–324; heading `13. DETECTED`
- Domain tags: EXECUTION, CLOCK, ACCOUNTING, CAPITAL, ROUTING, ARCH
- Source statement: 13. DETECTED: Une opportunité vient d’être détectée. Aucun capital n’est encore réservé.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `13. DETECTED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0110`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CLOCK, ACCOUNTING, CAPITAL, ROUTING, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0017 — 14. VALIDATING

- Source: `SRC-004`
- Location: lines 325–354; heading `14. VALIDATING`
- Domain tags: EXECUTION, RISK, INFRA, VALIDATION, OPERATIONS, ACCOUNTING, PARTICIPANTS, SURVIVAL
- Source statement: 14. VALIDATING: Le système refait les derniers gates immédiatement avant réservation. Cette validation doit être effectuée sur le state actuel, pas sur celui qui a déclenché le scanner quelques instants auparavant.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `14. VALIDATING` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0111`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, VALIDATION, OPERATIONS, ACCOUNTING, PARTICIPANTS, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0018 — 15. RESERVING

- Source: `SRC-004`
- Location: lines 355–457; heading `15. RESERVING`
- Domain tags: EXECUTION, RISK, INVENTORY, CAPITAL, ROUTING
- Source statement: 15. RESERVING: Avant tout ordre, le système réserve les ressources nécessaires. AvailableBalance = ActualBalance - ReservedBalance
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `15. RESERVING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0112`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INVENTORY, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0019 — 16. Pourquoi réserver avant d’envoyer

- Source: `SRC-004`
- Location: lines 458–478; heading `16. Pourquoi réserver avant d’envoyer`
- Domain tags: EXECUTION, INFRA, ROUTING
- Source statement: 16. Pourquoi réserver avant d’envoyer: Route A sees 1000 USDC Route B sees 1000 USDC
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `16. Pourquoi réserver avant d’envoyer` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0113`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0020 — 17. PLANNED

- Source: `SRC-004`
- Location: lines 479–508; heading `17. PLANNED`
- Domain tags: EXECUTION, RECOVERY, CLOCK, ROUTING
- Source statement: 17. PLANNED: Après réservation, l’objet final : Toute modification importante crée un nouveau :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `17. PLANNED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0114`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, CLOCK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0021 — 18. EXECUTING

- Source: `SRC-004`
- Location: lines 509–517; heading `18. EXECUTING`
- Domain tags: EXECUTION
- Source statement: 18. EXECUTING: Le plan est transmis au : qui lance les jambes dans l’ordre prévu.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `18. EXECUTING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0115`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0022 — 19. OrderIntent

- Source: `SRC-004`
- Location: lines 518–550; heading `19. OrderIntent`
- Domain tags: EXECUTION, RISK
- Source statement: 19. OrderIntent: Chaque jambe devient d’abord : Le cloid doit être généré avant l’envoi et rester stable pour cette intention logique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `19. OrderIntent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0116`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0023 — 20. Pourquoi le CLOID est fondamental

- Source: `SRC-004`
- Location: lines 551–583; heading `20. Pourquoi le CLOID est fondamental`
- Domain tags: EXECUTION
- Source statement: 20. Pourquoi le CLOID est fondamental: Nous ne savons pas si : A. Hyperliquid n'a jamais reçu l'ordre
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `20. Pourquoi le CLOID est fondamental` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0117`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0024 — 21. Règle fondamentale : NO BLIND RETRY

- Source: `SRC-004`
- Location: lines 584–604; heading `21. Règle fondamentale : NO BLIND RETRY`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 21. Règle fondamentale : NO BLIND RETRY: query order status / fills / open orders
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `21. Règle fondamentale : NO BLIND RETRY` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-EXEC-0118`; supporting items: SRC-005-ITEM-0024; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0025 — 22. OrderState

- Source: `SRC-004`
- Location: lines 605–635; heading `22. OrderState`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION
- Source statement: 22. OrderState: Un ordre suit conceptuellement : Tous les états finaux convergent vers :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `22. OrderState` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-EXEC-0119`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0026 — 23. CREATED

- Source: `SRC-004`
- Location: lines 636–640; heading `23. CREATED`
- Domain tags: EXECUTION, ARCH
- Source statement: 23. CREATED: Il peut encore être supprimé sans conséquence économique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `23. CREATED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0120`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0027 — 24. NONCE_ASSIGNED

- Source: `SRC-004`
- Location: lines 641–651; heading `24. NONCE_ASSIGNED`
- Domain tags: EXECUTION, SECURITY, ARCH
- Source statement: 24. NONCE_ASSIGNED: Un nonce unique a été attribué. Hyperliquid suit les nonces par signer, donc plusieurs subaccounts utilisant le même API wallet partagent le même espace de nonce. La documentation recommande un API wallet séparé par processus de trading et, en pratique, par subaccount utilisé en parallèle.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `24. NONCE_ASSIGNED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0121`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, SECURITY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0028 — 25. NonceManager

- Source: `SRC-004`
- Location: lines 652–673; heading `25. NonceManager`
- Domain tags: EXECUTION, SECURITY
- Source statement: 25. NonceManager: Le processus maintient un compteur atomique : Jamais deux threads ne génèrent leur nonce indépendamment.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `25. NonceManager` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0122`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0029 — 26. SIGNED

- Source: `SRC-004`
- Location: lines 674–684; heading `26. SIGNED`
- Domain tags: EXECUTION
- Source statement: 26. SIGNED: Après signature, le contenu économique ne change plus. Sinon il faut créer une nouvelle intention/signature.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `26. SIGNED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0123`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0030 — 27. SENT

- Source: `SRC-004`
- Location: lines 685–699; heading `27. SENT`
- Domain tags: EXECUTION, CLOCK
- Source statement: 27. SENT: Le message a quitté notre processus. À partir de cet instant :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `27. SENT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0124`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0031 — 28. PENDING_RESOLUTION

- Source: `SRC-004`
- Location: lines 700–712; heading `28. PENDING_RESOLUTION`
- Domain tags: EXECUTION, RECONCILIATION, DEPLOYMENT
- Source statement: 28. PENDING_RESOLUTION: Nous attendons une preuve exchange. Elle peut arriver par plusieurs canaux :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `28. PENDING_RESOLUTION` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0125`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0032 — 29. Event reducer plutôt que logique impérative fragile

- Source: `SRC-004`
- Location: lines 713–753; heading `29. Event reducer plutôt que logique impérative fragile`
- Domain tags: EXECUTION, DEPLOYMENT
- Source statement: 29. Event reducer plutôt que logique impérative fragile: Toutes les informations exchange sont converties en : Cela permet de recevoir :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `29. Event reducer plutôt que logique impérative fragile` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0126`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0033 — 30. Fills = événements économiques immuables

- Source: `SRC-004`
- Location: lines 754–771; heading `30. Fills = événements économiques immuables`
- Domain tags: EXECUTION, RECONCILIATION
- Source statement: 30. Fills = événements économiques immuables: Un fill confirmé n’est jamais « annulé » localement. Chaque fill possède un identifiant permettant la déduplication.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `30. Fills = événements économiques immuables` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0127`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0034 — 31. RESTING

- Source: `SRC-004`
- Location: lines 772–786; heading `31. RESTING`
- Domain tags: EXECUTION, ARCH
- Source statement: 31. RESTING: L’exchange indique que l’ordre repose dans le carnet. Pour notre architecture actuelle :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `31. RESTING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0128`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0035 — 32. PARTIALLY_FILLED

- Source: `SRC-004`
- Location: lines 787–849; heading `32. PARTIALLY_FILLED`
- Domain tags: EXECUTION, ACCOUNTING, QUANT
- Source statement: 32. PARTIALLY_FILLED: 0 < q_{filled} < q_{requested} q_{remaining} = q_{requested} - q_{filled}
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `32. PARTIALLY_FILLED` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0129`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0036 — 33. FILLED

- Source: `SRC-004`
- Location: lines 850–882; heading `33. FILLED`
- Domain tags: EXECUTION, ROUTING
- Source statement: 33. FILLED: Un ordre est rempli lorsque : dans les tolérances de lot/rounding prévues.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `33. FILLED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0130`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0037 — 34. REJECTED

- Source: `SRC-004`
- Location: lines 883–914; heading `34. REJECTED`
- Domain tags: EXECUTION, RECOVERY, INVENTORY
- Source statement: 34. REJECTED: Hyperliquid expose de nombreux statuts explicites : par exemple invalid tick, minimum notional, mauvais ALO price, IOC incapable de matcher, balance spot insuffisante, etc. Le moteur convertit chaque statut exchange en :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `34. REJECTED` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-EXEC-0131`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0038 — 35. UNKNOWN

- Source: `SRC-004`
- Location: lines 915–934; heading `35. UNKNOWN`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, INVENTORY, ARCH
- Source statement: 35. UNKNOWN: C’est un état de première classe. nous avons peut-être modifié notre exposition économique mais nous ne pouvons pas encore le prouver.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `35. UNKNOWN` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0132`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, INVENTORY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0039 — 36. CANCEL_REQUESTED

- Source: `SRC-004`
- Location: lines 935–964; heading `36. CANCEL_REQUESTED`
- Domain tags: EXECUTION
- Source statement: 36. CANCEL_REQUESTED: ou idéalement dans certains workflows : cancel request sent ≠ order canceled.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `36. CANCEL_REQUESTED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0133`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0040 — 37. Cancel race

- Source: `SRC-004`
- Location: lines 965–981; heading `37. Cancel race`
- Domain tags: EXECUTION, PARTICIPANTS, FUTURE
- Source statement: 37. Cancel race: T1 another participant hits order T3 cancel response says order already filled
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `37. Cancel race` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0134`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, PARTICIPANTS, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0041 — 38. CANCELED

- Source: `SRC-004`
- Location: lines 982–991; heading `38. CANCELED`
- Domain tags: EXECUTION, SIZING, QUANT
- Source statement: 38. CANCELED: L’exchange confirme que l’ordre n’est plus actif. Mais on vérifie toujours les fills accumulés avant la cancellation.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `38. CANCELED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0135`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0042 — 39. Terminal states

- Source: `SRC-004`
- Location: lines 992–1013; heading `39. Terminal states`
- Domain tags: EXECUTION, RECONCILIATION, INVENTORY
- Source statement: 39. Terminal states: Un ordre ne devient :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `39. Terminal states` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0136`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0043 — 40. Source of truth

- Source: `SRC-004`
- Location: lines 1014–1033; heading `40. Source of truth`
- Domain tags: EXECUTION, RECONCILIATION, DEPLOYMENT, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 40. Source of truth: Pour le hot path : Pour résoudre une ambiguïté :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `40. Source of truth` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0137`; supporting items: SRC-005-ITEM-0434, SRC-005-ITEM-0502; domain indexes `EXECUTION, RECONCILIATION, DEPLOYMENT, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0044 — 41. TT — 2-leg execution

- Source: `SRC-004`
- Location: lines 1034–1047; heading `41. TT — 2-leg execution`
- Domain tags: EXECUTION
- Source statement: 41. TT — 2-leg execution: Plan : A → X
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `41. TT — 2-leg execution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0138`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0045 — 42. Leg 1 TT

- Source: `SRC-004`
- Location: lines 1048–1063; heading `42. Leg 1 TT`
- Domain tags: EXECUTION, RISK
- Source statement: 42. Leg 1 TT: qui interdit au bot de traverser le carnet au-delà du slippage accepté. Hyperliquid documente l’IOC comme un ordre dont toute partie non exécutée est automatiquement annulée plutôt que laissée dans le carnet.
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `42. Leg 1 TT` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0139`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0046 — 43. Leg 1 : zéro fill

- Source: `SRC-004`
- Location: lines 1064–1088; heading `43. Leg 1 : zéro fill`
- Domain tags: EXECUTION, RISK, INVENTORY, ROUTING
- Source statement: 43. Leg 1 : zéro fill: Si : q_{fill1}=0
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `43. Leg 1 : zéro fill` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0140`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0047 — 44. Leg 1 : full fill

- Source: `SRC-004`
- Location: lines 1089–1124; heading `44. Leg 1 : full fill`
- Domain tags: EXECUTION, ACCOUNTING, QUANT
- Source statement: 44. Leg 1 : full fill: on calcule immédiatement la quantité réellement disponible de X. La jambe 2 est basée sur :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `44. Leg 1 : full fill` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0141`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0048 — 45. Revalidation avant Leg 2

- Source: `SRC-004`
- Location: lines 1125–1138; heading `45. Revalidation avant Leg 2`
- Domain tags: EXECUTION, VALIDATION, RECOVERY, DEPLOYMENT, INVENTORY, TRIANGLE
- Source statement: 45. Revalidation avant Leg 2: Même dans un triangle supposé ultra-rapide : recalculate Leg2 / recovery alternatives
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `45. Revalidation avant Leg 2` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0142`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, VALIDATION, RECOVERY, DEPLOYMENT, INVENTORY, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0049 — 46. Continuation Decision

- Source: `SRC-004`
- Location: lines 1139–1173; heading `46. Continuation Decision`
- Domain tags: EXECUTION, RECOVERY, ROUTING, FUTURE
- Source statement: 46. Continuation Decision: La question n’est plus : la route originale est-elle toujours rentable ?
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `46. Continuation Decision` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0143`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, ROUTING, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0050 — 47. Si continuation reste optimale

- Source: `SRC-004`
- Location: lines 1174–1185; heading `47. Si continuation reste optimale`
- Domain tags: EXECUTION, INVENTORY, QUANT
- Source statement: 47. Si continuation reste optimale: avec quantité basée sur :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `47. Si continuation reste optimale` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0144`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INVENTORY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0051 — 48. Si continuation n’est plus optimale

- Source: `SRC-004`
- Location: lines 1186–1202; heading `48. Si continuation n’est plus optimale`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 48. Si continuation n’est plus optimale: Le Recovery Engine peut choisir : selon la configuration économique réelle.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `48. Si continuation n’est plus optimale` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0145`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0052 — 49. Leg 1 partial fill

- Source: `SRC-004`
- Location: lines 1203–1242; heading `49. Leg 1 partial fill`
- Domain tags: EXECUTION, RISK, INFRA, ROUTING
- Source statement: 49. Leg 1 partial fill: unfilled portion is canceled automatically La route n’essaye surtout pas de conserver la taille initialement prévue.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `49. Leg 1 partial fill` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0146`; supporting items: SRC-001-ITEM-0068, SRC-005-ITEM-0026; domain indexes `EXECUTION, RISK, INFRA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0053 — 50. Partial continuation

- Source: `SRC-004`
- Location: lines 1243–1264; heading `50. Partial continuation`
- Domain tags: EXECUTION, ACCOUNTING, ROUTING, QUANT
- Source statement: 50. Partial continuation: pour la quantité partiellement remplie.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `50. Partial continuation` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0147`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0054 — 51. Dust problem

- Source: `SRC-004`
- Location: lines 1265–1286; heading `51. Dust problem`
- Domain tags: EXECUTION, RECOVERY, INVENTORY, ROUTING, QUANT
- Source statement: 51. Dust problem: Un partial fill peut produire une quantité trop faible pour : La gestion de dust doit être explicitement prévue.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `51. Dust problem` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0148`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, INVENTORY, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0055 — 52. Leg 2 partial fill

- Source: `SRC-004`
- Location: lines 1287–1301; heading `52. Leg 2 partial fill`
- Domain tags: EXECUTION, RECOVERY, ROUTING
- Source statement: 52. Leg 2 partial fill: Si la deuxième jambe n’exécute qu’une partie : remaining X → Recovery Engine
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `52. Leg 2 partial fill` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0149`; supporting items: SRC-001-ITEM-0068, SRC-005-ITEM-0026; domain indexes `EXECUTION, RECOVERY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0056 — 53. Quand une route TT est COMPLETED

- Source: `SRC-004`
- Location: lines 1302–1320; heading `53. Quand une route TT est COMPLETED`
- Domain tags: EXECUTION, ROUTING, RECOVERY, RECONCILIATION, DEPLOYMENT, ACCOUNTING, INVENTORY
- Source statement: 53. Quand une route TT est COMPLETED: Pas simplement lorsque les deux ordres ont reçu un ack. remaining intermediate exposure <= permitted dust
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `53. Quand une route TT est COMPLETED` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0150`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING, RECOVERY, RECONCILIATION, DEPLOYMENT, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0057 — 54. MT — Maker/Taker

- Source: `SRC-004`
- Location: lines 1321–1334; heading `54. MT — Maker/Taker`
- Domain tags: EXECUTION
- Source statement: 54. MT — Maker/Taker: La première jambe utilise : Hyperliquid définit ALO comme « add liquidity only » : s’il matcherait immédiatement, l’ordre est annulé/rejeté plutôt que de devenir taker.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `54. MT — Maker/Taker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0151`; supporting items: SRC-002-ITEM-0079, SRC-005-ITEM-0131, SRC-008-ITEM-0103, SRC-008-ITEM-0104; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0058 — 55. Maker leg lifecycle

- Source: `SRC-004`
- Location: lines 1335–1353; heading `55. Maker leg lifecycle`
- Domain tags: EXECUTION, ROUTING
- Source statement: 55. Maker leg lifecycle: SUBMITTED RESTING
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `55. Maker leg lifecycle` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0152`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0059 — 56. Tant que maker repose

- Source: `SRC-004`
- Location: lines 1354–1370; heading `56. Tant que maker repose`
- Domain tags: EXECUTION, RISK, SURVIVAL, MICROSTRUCTURE, MAKER_MODEL, INVENTORY, ROUTING
- Source statement: 56. Tant que maker repose: Le moteur continue à calculer : Si les conditions disparaissent :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `56. Tant que maker repose` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0153`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, SURVIVAL, MICROSTRUCTURE, MAKER_MODEL, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0060 — 57. Maker stale condition

- Source: `SRC-004`
- Location: lines 1371–1386; heading `57. Maker stale condition`
- Domain tags: EXECUTION, FORMULA, SURVIVAL, MAKER_MODEL, PRODUCT
- Source statement: 57. Maker stale condition: La durée maximale ne doit pas être un chiffre arbitraire du type : Elle doit dépendre notamment de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `57. Maker stale condition` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0154`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, FORMULA, SURVIVAL, MAKER_MODEL, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0061 — 58. Maker partial fill

- Source: `SRC-004`
- Location: lines 1387–1397; heading `58. Maker partial fill`
- Domain tags: EXECUTION, QUANT
- Source statement: 58. Maker partial fill: maker requested = 500 HYPE Le bot possède réellement les 120 HYPE.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `58. Maker partial fill` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0155`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0062 — 59. Politique recommandée pour MT

- Source: `SRC-004`
- Location: lines 1398–1417; heading `59. Politique recommandée pour MT`
- Domain tags: EXECUTION, RECOVERY, SIZING, ROUTING, QUANT
- Source statement: 59. Politique recommandée pour MT: chaque quantité maker économiquement exécutable doit être hedgée/convertie rapidement par la jambe taker correspondante. La partie maker restante peut rester active uniquement si :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `59. Politique recommandée pour MT` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0156`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, SIZING, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0063 — 60. Small partial below minimum

- Source: `SRC-004`
- Location: lines 1418–1437; heading `60. Small partial below minimum`
- Domain tags: EXECUTION, RECOVERY, INVENTORY
- Source statement: 60. Small partial below minimum: Si le fill maker est trop petit pour le minimum de la jambe 2 : peut temporairement agréger plusieurs fills du même contexte économique compatible.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `60. Small partial below minimum` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0157`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0064 — 61. Maker cancellation after partial

- Source: `SRC-004`
- Location: lines 1438–1454; heading `61. Maker cancellation after partial`
- Domain tags: EXECUTION, OPERATIONS, MAKER_MODEL
- Source statement: 61. Maker cancellation after partial: 1. sends cancel for remaining maker 2. assumes remaining may still fill
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `61. Maker cancellation after partial` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0158`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, OPERATIONS, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0065 — 62. TTT — triangle taker

- Source: `SRC-004`
- Location: lines 1455–1480; heading `62. TTT — triangle taker`
- Domain tags: EXECUTION, TRIANGLE
- Source statement: 62. TTT — triangle taker: Les trois jambes utilisent : La logique est récursive :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `62. TTT — triangle taker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0159`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0066 — 63. Important : triangle non atomique

- Source: `SRC-004`
- Location: lines 1481–1492; heading `63. Important : triangle non atomique`
- Domain tags: EXECUTION, TRIANGLE
- Source statement: 63. Important : triangle non atomique: Même si les trois ordres peuvent éventuellement être envoyés rapidement ou batchés au niveau API : notre modèle ne doit jamais considérer le triangle comme atomique.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `63. Important : triangle non atomique` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0160`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0067 — 64. Après chaque jambe TTT

- Source: `SRC-004`
- Location: lines 1493–1519; heading `64. Après chaque jambe TTT`
- Domain tags: EXECUTION, TRIANGLE, RECOVERY, CAPITAL, ROUTING
- Source statement: 64. Après chaque jambe TTT: La route originale n’a aucun privilège une fois le capital réellement exposé.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `64. Après chaque jambe TTT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0161`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, TRIANGLE, RECOVERY, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0068 — 65. MTT

- Source: `SRC-004`
- Location: lines 1520–1535; heading `65. MTT`
- Domain tags: EXECUTION, TRIANGLE
- Source statement: 65. MTT: Même logique MT pour la première jambe. Une fois un fill maker obtenu :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `65. MTT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0162`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0069 — 66. TM et MM

- Source: `SRC-004`
- Location: lines 1536–1555; heading `66. TM et MM`
- Domain tags: EXECUTION, RISK, ARCH, FUTURE
- Source statement: 66. TM et MM: car la jambe maker après une première exposition laisse l’intermediate asset exposé à une attente incertaine.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `66. TM et MM` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0163`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, ARCH, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0070 — 67. Recovery State Machine

- Source: `SRC-004`
- Location: lines 1556–1578; heading `67. Recovery State Machine`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 67. Recovery State Machine: États : RECOVERY_REQUIRED
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `67. Recovery State Machine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0164`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0071 — 68. RECOVERY_REQUIRED

- Source: `SRC-004`
- Location: lines 1579–1594; heading `68. RECOVERY_REQUIRED`
- Domain tags: EXECUTION, RECOVERY, RISK, INVENTORY, CAPITAL
- Source statement: 68. RECOVERY_REQUIRED: Déclenché par exemple par : second leg no longer viable
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `68. RECOVERY_REQUIRED` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0165`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, INVENTORY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0072 — 69. Recovery objective

- Source: `SRC-004`
- Location: lines 1595–1679; heading `69. Recovery objective`
- Domain tags: EXECUTION, RECOVERY, PORTFOLIO, ROUTING
- Source statement: 69. Recovery objective: Le Recovery Engine ne cherche pas forcément à terminer la route originale.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `69. Recovery objective` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0166`; supporting items: SRC-006-ITEM-0398; domain indexes `EXECUTION, RECOVERY, PORTFOLIO, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0073 — 70. Candidate exits

- Source: `SRC-004`
- Location: lines 1680–1692; heading `70. Candidate exits`
- Domain tags: EXECUTION, INVENTORY, GRAPH, ARCH
- Source statement: 70. Candidate exits: Pour un intermediate X : X → other core inventory
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `70. Candidate exits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0167`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INVENTORY, GRAPH, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0074 — 71. Recovery orders

- Source: `SRC-004`
- Location: lines 1693–1712; heading `71. Recovery orders`
- Domain tags: EXECUTION, RECOVERY, RISK, MICROSTRUCTURE
- Source statement: 71. Recovery orders: Les Recovery Orders utilisent : Ils peuvent accepter un EV négatif :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `71. Recovery orders` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0168`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0075 — 72. Ne pas confondre perte et permission illimitée

- Source: `SRC-004`
- Location: lines 1713–1726; heading `72. Ne pas confondre perte et permission illimitée`
- Domain tags: EXECUTION, RISK, RECOVERY, ACCOUNTING
- Source statement: 72. Ne pas confondre perte et permission illimitée: accept another 100€ of slippage Les sunk costs restent sunk.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `72. Ne pas confondre perte et permission illimitée` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0169`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, RECOVERY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0076 — 73. Recovery split

- Source: `SRC-004`
- Location: lines 1727–1747; heading `73. Recovery split`
- Domain tags: EXECUTION, RECOVERY, RISK, QUANT
- Source statement: 73. Recovery split: Le meilleur exit peut être : Le Recovery Engine doit donc supporter des sorties multiples.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `73. Recovery split` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0170`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RISK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0077 — 74. Recovery failure

- Source: `SRC-004`
- Location: lines 1748–1765; heading `74. Recovery failure`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, INFRA
- Source statement: 74. Recovery failure: Si un recovery order échoue : never blindly retry same parameters
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `74. Recovery failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0171`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0078 — 75. RECONCILIATION State Machine

- Source: `SRC-004`
- Location: lines 1766–1785; heading `75. RECONCILIATION State Machine`
- Domain tags: EXECUTION, RECONCILIATION
- Source statement: 75. RECONCILIATION State Machine: États : RECONCILE_REQUESTED
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `75. RECONCILIATION State Machine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0172`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0079 — 76. Sources utilisées

- Source: `SRC-004`
- Location: lines 1786–1798; heading `76. Sources utilisées`
- Domain tags: EXECUTION, RECONCILIATION
- Source statement: 76. Sources utilisées: Hyperliquid expose ces informations via Info API et WebSocket.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `76. Sources utilisées` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0173`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0080 — 77. Reconciliation algorithm

- Source: `SRC-004`
- Location: lines 1799–1822; heading `77. Reconciliation algorithm`
- Domain tags: EXECUTION, RECONCILIATION, RECOVERY, INVENTORY
- Source statement: 77. Reconciliation algorithm: Pour chaque ordre local non terminal : Ensuite récupérer les fills correspondants.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `77. Reconciliation algorithm` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-EXEC-0174`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0081 — 78. Balance reconciliation

- Source: `SRC-004`
- Location: lines 1823–1904; heading `78. Balance reconciliation`
- Domain tags: EXECUTION, RECONCILIATION, INVENTORY, RECOVERY
- Source statement: 78. Balance reconciliation: Diff_a = ExchangeBalance_a - ExpectedLocalBalance_a et le moteur ne retourne pas READY sans résolution.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `78. Balance reconciliation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0175`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, INVENTORY, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0082 — 79. Startup after crash

- Source: `SRC-004`
- Location: lines 1905–1927; heading `79. Startup after crash`
- Domain tags: EXECUTION, OPERATIONS, RECONCILIATION
- Source statement: 79. Startup after crash: before local persistence of ack local state may be incomplete
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `79. Startup after crash` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0176`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, OPERATIONS, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0083 — 80. Persistent Execution Journal

- Source: `SRC-004`
- Location: lines 1928–1956; heading `80. Persistent Execution Journal`
- Domain tags: EXECUTION, DATA, RECOVERY, MICROSTRUCTURE, ROUTING, HOT_WARM_COLD, QUANT, ARCH
- Source statement: 80. Persistent Execution Journal: Les événements critiques doivent être persistés : Le journal ne doit néanmoins pas introduire des disk writes bloquants dans le hot path.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `80. Persistent Execution Journal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0177`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DATA, RECOVERY, MICROSTRUCTURE, ROUTING, HOT_WARM_COLD, QUANT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0084 — 81. Crash consistency

- Source: `SRC-004`
- Location: lines 1957–1977; heading `81. Crash consistency`
- Domain tags: EXECUTION, OPERATIONS, INFRA, INVENTORY, ARCH, FUTURE
- Source statement: 81. Crash consistency: On devra déterminer plus tard le compromis exact entre : Mais la vérité exchange reste toujours reconstructible grâce à :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `81. Crash consistency` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0178`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, OPERATIONS, INFRA, INVENTORY, ARCH, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0085 — 82. Disconnect market feed

- Source: `SRC-004`
- Location: lines 1978–1997; heading `82. Disconnect market feed`
- Domain tags: EXECUTION, ACCOUNTING, RECOVERY, RISK
- Source statement: 82. Disconnect market feed: Si market WebSocket tombe : si la fraîcheur dépasse le threshold.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `82. Disconnect market feed` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0179`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0086 — 83. Disconnect account/order feed

- Source: `SRC-004`
- Location: lines 1998–2016; heading `83. Disconnect account/order feed`
- Domain tags: EXECUTION, ACCOUNTING, RECONCILIATION, RISK, DEPLOYMENT, ARCH
- Source statement: 83. Disconnect account/order feed: ne sont plus fiables :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `83. Disconnect account/order feed` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0180`; supporting items: SRC-006-ITEM-0518; domain indexes `EXECUTION, ACCOUNTING, RECONCILIATION, RISK, DEPLOYMENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0087 — 84. Reconnect

- Source: `SRC-004`
- Location: lines 2017–2038; heading `84. Reconnect`
- Domain tags: EXECUTION, RECONCILIATION, RISK, CLIENT
- Source statement: 84. Reconnect: Hyperliquid précise que les connexions WebSocket peuvent être interrompues périodiquement et que les clients automatisés doivent gérer proprement la reconnexion ; les snapshots ou requêtes Info peuvent servir à récupérer ce qui a été manqué.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `84. Reconnect` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0181`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION, RISK, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0088 — 85. Dead Man's Switch

- Source: `SRC-004`
- Location: lines 2039–2049; heading `85. Dead Man's Switch`
- Domain tags: EXECUTION, RISK, CLOCK, INFRA
- Source statement: 85. Dead Man's Switch: Il permet de programmer un cancel-all futur. La documentation actuelle impose que le timestamp soit au moins cinq secondes dans le futur et limite à dix les déclenchements effectifs par jour.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `85. Dead Man's Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0182`; supporting items: SRC-008-ITEM-0212; domain indexes `EXECUTION, RISK, CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0089 — 86. Fonctionnement recommandé

- Source: `SRC-004`
- Location: lines 2050–2066; heading `86. Fonctionnement recommandé`
- Domain tags: EXECUTION
- Source statement: 86. Fonctionnement recommandé: Pendant qu’un maker order existe : Si le bot meurt complètement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `86. Fonctionnement recommandé` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-EXEC-0183`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0090 — 87. Pourquoi pas pour IOC

- Source: `SRC-004`
- Location: lines 2067–2075; heading `87. Pourquoi pas pour IOC`
- Domain tags: EXECUTION
- Source statement: 87. Pourquoi pas pour IOC: IOC ne reste pas dans le carnet. Donc le dead-man switch est particulièrement intéressant pour :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `87. Pourquoi pas pour IOC` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0184`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0091 — 88. Timers

- Source: `SRC-004`
- Location: lines 2076–2088; heading `88. Timers`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, BENCHMARK
- Source statement: 88. Timers: Aucun timeout critique ne doit être choisi arbitrairement. Ils doivent venir de nos benchmarks.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `88. Timers` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0185`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0092 — 89. ACK timeout

- Source: `SRC-004`
- Location: lines 2089–2142; heading `89. ACK timeout`
- Domain tags: EXECUTION, INFRA, BENCHMARK, ACCOUNTING, PRODUCT
- Source statement: 89. ACK timeout: T_{ack} = f( ObservedAckLatencyDistribution ) Par exemple basé sur :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `89. ACK timeout` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0186`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, BENCHMARK, ACCOUNTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0093 — 90. Maker maximum age

- Source: `SRC-004`
- Location: lines 2143–2207; heading `90. Maker maximum age`
- Domain tags: EXECUTION, FORMULA, SURVIVAL, PRODUCT
- Source statement: 90. Maker maximum age: T_{maker,max} = f( FillDistribution, EdgeSurvival, AdverseSelection ) Le Formula Book fixera la relation exacte.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `90. Maker maximum age` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0187`; supporting items: SRC-005-ITEM-0081, SRC-005-ITEM-0082; domain indexes `EXECUTION, FORMULA, SURVIVAL, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0094 — 91. Route timeout

- Source: `SRC-004`
- Location: lines 2208–2218; heading `91. Route timeout`
- Domain tags: EXECUTION, ROUTING, RISK, INVENTORY, TRIANGLE
- Source statement: 91. Route timeout: Le timeout d’une route n’est pas un timeout réseau. Une route TTT peut devenir économiquement invalide bien avant qu’un HTTP timeout classique n’expire.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `91. Route timeout` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0188`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING, RISK, INVENTORY, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0095 — 92. Protected price

- Source: `SRC-004`
- Location: lines 2219–2279; heading `92. Protected price`
- Domain tags: EXECUTION, RISK, PRODUCT
- Source statement: 92. Protected price: Aucun taker ne doit utiliser : Le moteur utilise un prix limite protecteur :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `92. Protected price` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0189`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0096 — 93. Exchange ACK ≠ economic success

- Source: `SRC-004`
- Location: lines 2280–2300; heading `93. Exchange ACK ≠ economic success`
- Domain tags: EXECUTION, ACCOUNTING, MICROSTRUCTURE, ROUTING
- Source statement: 93. Exchange ACK ≠ economic success: Hyperliquid peut répondre par exemple : Un status: ok HTTP ne veut donc pas dire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `93. Exchange ACK ≠ economic success` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0190`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0097 — 94. Actual fill accounting

- Source: `SRC-004`
- Location: lines 2301–2333; heading `94. Actual fill accounting`
- Domain tags: EXECUTION, ACCOUNTING, CLOCK
- Source statement: 94. Actual fill accounting: VWAP = \frac{\sum p_iq_i}{\sum q_i} est fait sur les fills réels.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `94. Actual fill accounting` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0191`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0098 — 95. Leg accounting

- Source: `SRC-004`
- Location: lines 2334–2350; heading `95. Leg accounting`
- Domain tags: EXECUTION, ACCOUNTING, INFRA
- Source statement: 95. Leg accounting: Chaque leg produit : actual_input
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `95. Leg accounting` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0192`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0099 — 96. Route accounting

- Source: `SRC-004`
- Location: lines 2351–2374; heading `96. Route accounting`
- Domain tags: EXECUTION, ACCOUNTING, ROUTING, INFRA, SIMULATOR, PARTICIPANTS
- Source statement: 96. Route accounting: Route terminée : ExpectedPnL
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `96. Route accounting` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0193`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, ROUTING, INFRA, SIMULATOR, PARTICIPANTS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0100 — 97. Execution ownership

- Source: `SRC-004`
- Location: lines 2375–2393; heading `97. Execution ownership`
- Domain tags: EXECUTION, ARCH
- Source statement: 97. Execution ownership: Une seule tâche logique doit posséder un : pour éviter deux threads écrivant simultanément les transitions.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `97. Execution ownership` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0194`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0101 — 98. Idempotency

- Source: `SRC-004`
- Location: lines 2394–2456; heading `98. Idempotency`
- Domain tags: EXECUTION, DATA, ROUTING
- Source statement: 98. Idempotency: Un événement reçu deux fois : must produce same final state
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `98. Idempotency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0195`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0102 — 99. Monotonicity

- Source: `SRC-004`
- Location: lines 2457–2475; heading `99. Monotonicity`
- Domain tags: EXECUTION, CLOCK
- Source statement: 99. Monotonicity: ne doit jamais redevenir : Un événement tardif incompatible est :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `99. Monotonicity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0196`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0103 — 100. Important : état économique séparé de l’état transport

- Source: `SRC-004`
- Location: lines 2476–2498; heading `100. Important : état économique séparé de l’état transport`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: 100. Important : état économique séparé de l’état transport: On peut avoir : HTTP request = timeout
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `100. Important : état économique séparé de l’état transport` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0197`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0104 — 101. Reservations lifecycle

- Source: `SRC-004`
- Location: lines 2499–2519; heading `101. Reservations lifecycle`
- Domain tags: EXECUTION, ROUTING, RECOVERY, RECONCILIATION
- Source statement: 101. Reservations lifecycle: Reservation créée avant le trade.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `101. Reservations lifecycle` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0198`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ROUTING, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0105 — 102. Never spend unknown capital

- Source: `SRC-004`
- Location: lines 2520–2532; heading `102. Never spend unknown capital`
- Domain tags: EXECUTION, RECOVERY, CAPITAL, ROUTING
- Source statement: 102. Never spend unknown capital: les fonds potentiellement consommés restent : Une nouvelle route ne peut pas les utiliser.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `102. Never spend unknown capital` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0199`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0106 — 103. Risk reduction always has priority

- Source: `SRC-004`
- Location: lines 2533–2544; heading `103. Risk reduction always has priority`
- Domain tags: EXECUTION, RISK, RECOVERY, RECONCILIATION, BENCHMARK
- Source statement: 103. Risk reduction always has priority: 4. continuation of existing execution Un nouveau +5 bps n’a aucune priorité sur une exposition existante non résolue.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `103. Risk reduction always has priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0200`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, RECOVERY, RECONCILIATION, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0107 — 104. Global PnL cannot alter execution safety

- Source: `SRC-004`
- Location: lines 2545–2554; heading `104. Global PnL cannot alter execution safety`
- Domain tags: EXECUTION, ACCOUNTING, RECOVERY, RISK, MICROSTRUCTURE
- Source statement: 104. Global PnL cannot alter execution safety: therefore allow more recovery slippage Le state machine ne connaît pas ce genre d’exception.
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `104. Global PnL cannot alter execution safety` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0201`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, RECOVERY, RISK, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0108 — 105. Rust modules

- Source: `SRC-004`
- Location: lines 2555–2577; heading `105. Rust modules`
- Domain tags: EXECUTION, ARCH, RECOVERY, RECONCILIATION, DATA, SECURITY, ACCOUNTING, ROUTING
- Source statement: 105. Rust modules: Je proposerais : src/
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `105. Rust modules` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0202`; supporting items: SRC-008-ITEM-0174; domain indexes `EXECUTION, ARCH, RECOVERY, RECONCILIATION, DATA, SECURITY, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0109 — 106. Structures principales

- Source: `SRC-004`
- Location: lines 2578–2599; heading `106. Structures principales`
- Domain tags: EXECUTION, INFRA, ROUTING
- Source statement: 106. Structures principales: doivent être des types distincts. Cela réduit énormément les erreurs de programmation.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `106. Structures principales` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0203`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0110 — 107. ExecutionState

- Source: `SRC-004`
- Location: lines 2600–2627; heading `107. ExecutionState`
- Domain tags: EXECUTION, RECOVERY, DEPLOYMENT, ACCOUNTING, INVENTORY, ROUTING
- Source statement: 107. ExecutionState: Conceptuellement : ExecutionState {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `107. ExecutionState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0204`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, DEPLOYMENT, ACCOUNTING, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0111 — 108. LegExecutionState

- Source: `SRC-004`
- Location: lines 2628–2651; heading `108. LegExecutionState`
- Domain tags: EXECUTION, ACCOUNTING
- Source statement: 108. LegExecutionState: LegExecutionState { leg_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `108. LegExecutionState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0205`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0112 — 109. OrderRecord

- Source: `SRC-004`
- Location: lines 2652–2680; heading `109. OrderRecord`
- Domain tags: EXECUTION, RISK
- Source statement: 109. OrderRecord: OrderRecord { intent_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `109. OrderRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0206`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0113 — 110. RejectReason taxonomy

- Source: `SRC-004`
- Location: lines 2681–2715; heading `110. RejectReason taxonomy`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION, RISK, INFRA, INVENTORY, CAPITAL
- Source statement: 110. RejectReason taxonomy: Les rejects doivent être structurés.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `110. RejectReason taxonomy` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0207`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION, RISK, INFRA, INVENTORY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0114 — 111. Pourquoi stocker tous les rejects

- Source: `SRC-004`
- Location: lines 2716–2730; heading `111. Pourquoi stocker tous les rejects`
- Domain tags: EXECUTION
- Source statement: 111. Pourquoi stocker tous les rejects: Sinon le backtest souffre de : what we intentionally did not trade
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `111. Pourquoi stocker tous les rejects` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0208`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0115 — 112. Test obligatoire n°1 — Full IOC success

- Source: `SRC-004`
- Location: lines 2731–2746; heading `112. Test obligatoire n°1 — Full IOC success`
- Domain tags: EXECUTION, ACCOUNTING, INVENTORY
- Source statement: 112. Test obligatoire n°1 — Full IOC success: Scenario : Leg1 full
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `112. Test obligatoire n°1 — Full IOC success` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0209`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0116 — 113. Test n°2 — Leg1 zero fill

- Source: `SRC-004`
- Location: lines 2747–2760; heading `113. Test n°2 — Leg1 zero fill`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 113. Test n°2 — Leg1 zero fill: IOC fills 0 Attendu :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `113. Test n°2 — Leg1 zero fill` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0210`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0117 — 114. Test n°3 — Leg1 partial

- Source: `SRC-004`
- Location: lines 2761–2773; heading `114. Test n°3 — Leg1 partial`
- Domain tags: EXECUTION
- Source statement: 114. Test n°3 — Leg1 partial: requested 100 filled 40
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `114. Test n°3 — Leg1 partial` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0211`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0118 — 115. Test n°4 — Leg2 edge dies

- Source: `SRC-004`
- Location: lines 2774–2790; heading `115. Test n°4 — Leg2 edge dies`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 115. Test n°4 — Leg2 edge dies: Leg1 filled Leg2 now negative
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `115. Test n°4 — Leg2 edge dies` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0212`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0119 — 116. Test n°5 — network timeout after submit

- Source: `SRC-004`
- Location: lines 2791–2806; heading `116. Test n°5 — network timeout after submit`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 116. Test n°5 — network timeout after submit: Simulation : order actually filled
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `116. Test n°5 — network timeout after submit` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0213`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0120 — 117. Test n°6 — duplicate WebSocket fill

- Source: `SRC-004`
- Location: lines 2807–2814; heading `117. Test n°6 — duplicate WebSocket fill`
- Domain tags: EXECUTION, DEPLOYMENT, INVENTORY
- Source statement: 117. Test n°6 — duplicate WebSocket fill: Même fill reçu deux fois.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `117. Test n°6 — duplicate WebSocket fill` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0214`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DEPLOYMENT, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0121 — 118. Test n°7 — fill during cancellation

- Source: `SRC-004`
- Location: lines 2815–2830; heading `118. Test n°7 — fill during cancellation`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 118. Test n°7 — fill during cancellation: maker resting cancel sent
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `118. Test n°7 — fill during cancellation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0215`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0122 — 119. Test n°8 — process crash

- Source: `SRC-004`
- Location: lines 2831–2851; heading `119. Test n°8 — process crash`
- Domain tags: EXECUTION, OPERATIONS, RECONCILIATION
- Source statement: 119. Test n°8 — process crash: Aucun nouvel ordre avant reconciliation.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `119. Test n°8 — process crash` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0216`; supporting items: SRC-006-ITEM-0577; domain indexes `EXECUTION, OPERATIONS, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0123 — 120. Test n°9 — balance mismatch

- Source: `SRC-004`
- Location: lines 2852–2869; heading `120. Test n°9 — balance mismatch`
- Domain tags: EXECUTION, INVENTORY
- Source statement: 120. Test n°9 — balance mismatch: Local : 1000 USDC
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `120. Test n°9 — balance mismatch` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0217`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0124 — 121. Test n°10 — stale feed while maker resting

- Source: `SRC-004`
- Location: lines 2870–2878; heading `121. Test n°10 — stale feed while maker resting`
- Domain tags: EXECUTION, ACCOUNTING, RECOVERY, RISK
- Source statement: 121. Test n°10 — stale feed while maker resting: Attendu : stop new risk
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `121. Test n°10 — stale feed while maker resting` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0218`; supporting items: SRC-005-ITEM-0207; domain indexes `EXECUTION, ACCOUNTING, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0125 — 122. Property tests

- Source: `SRC-004`
- Location: lines 2879–2899; heading `122. Property tests`
- Domain tags: EXECUTION, VALIDATION, RECOVERY, INVENTORY
- Source statement: 122. Property tests: En plus des scénarios : filled <= requested + tolerance
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `122. Property tests` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0219`; supporting items: SRC-005-ITEM-0536; domain indexes `EXECUTION, VALIDATION, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0126 — 123. Replay determinism requirement

- Source: `SRC-004`
- Location: lines 2900–2918; heading `123. Replay determinism requirement`
- Domain tags: EXECUTION, DETERMINISM, REPLAY, CLOCK, ACCOUNTING
- Source statement: 123. Replay determinism requirement: Pour une séquence identique : le state reducer doit produire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `123. Replay determinism requirement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0220`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, DETERMINISM, REPLAY, CLOCK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0127 — 124. Logging

- Source: `SRC-004`
- Location: lines 2919–2937; heading `124. Logging`
- Domain tags: EXECUTION, RECOVERY, CLOCK, PORTFOLIO
- Source statement: 124. Logging: Cela permettra de reconstituer : Pourquoi ce trade est-il parti ?
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `124. Logging` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0221`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, CLOCK, PORTFOLIO`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0128 — 125. Metrics

- Source: `SRC-004`
- Location: lines 2938–2966; heading `125. Metrics`
- Domain tags: EXECUTION, RECOVERY, RECONCILIATION
- Source statement: 125. Metrics: À mesurer : executions_started
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `125. Metrics` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0222`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0129 — 126. State transition latency

- Source: `SRC-004`
- Location: lines 2967–2986; heading `126. State transition latency`
- Domain tags: EXECUTION, INFRA, RECOVERY, BENCHMARK, SIMULATOR, SURVIVAL
- Source statement: 126. State transition latency: Ces métriques alimenteront directement :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `126. State transition latency` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0223`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, INFRA, RECOVERY, BENCHMARK, SIMULATOR, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0130 — 127. Interaction avec le Participant Model

- Source: `SRC-004`
- Location: lines 2987–3002; heading `127. Interaction avec le Participant Model`
- Domain tags: EXECUTION, PARTICIPANTS, SURVIVAL, CROSS_MARKET, ROUTING, FUTURE
- Source statement: 127. Interaction avec le Participant Model: Quand Leg1 est réellement filled : Ainsi l’Execution State Machine utilise les modèles prédictifs mais reste responsable de la sécurité.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `127. Interaction avec le Participant Model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-EXEC-0224`; supporting items: SRC-006-ITEM-0338; domain indexes `EXECUTION, PARTICIPANTS, SURVIVAL, CROSS_MARKET, ROUTING, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0131 — 128. Interaction avec le Simulator

- Source: `SRC-004`
- Location: lines 3003–3020; heading `128. Interaction avec le Simulator`
- Domain tags: EXECUTION, SIMULATOR
- Source statement: 128. Interaction avec le Simulator: La State Machine produit : Chaque exécution crée ensuite :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `128. Interaction avec le Simulator` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0225`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0132 — 129. Interaction avec le Risk Engine

- Source: `SRC-004`
- Location: lines 3021–3039; heading `129. Interaction avec le Risk Engine`
- Domain tags: EXECUTION, RISK, RECOVERY
- Source statement: 129. Interaction avec le Risk Engine: Avant chaque transition qui augmente le risque : En revanche certaines transitions qui réduisent le risque :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `129. Interaction avec le Risk Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0226`; supporting items: SRC-006-ITEM-0382; domain indexes `EXECUTION, RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0133 — 130. Interaction avec Inventory Engine

- Source: `SRC-004`
- Location: lines 3040–3052; heading `130. Interaction avec Inventory Engine`
- Domain tags: EXECUTION, INVENTORY, ROUTING
- Source statement: 130. Interaction avec Inventory Engine: Chaque fill modifie immédiatement : On ne met pas à jour l’inventaire uniquement lorsque la route entière est terminée.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `130. Interaction avec Inventory Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0227`; supporting items: SRC-006-ITEM-0367; domain indexes `EXECUTION, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0134 — 131. Interaction avec HOT/WARM/COLD

- Source: `SRC-004`
- Location: lines 3053–3068; heading `131. Interaction avec HOT/WARM/COLD`
- Domain tags: EXECUTION, HOT_WARM_COLD, DEPLOYMENT, CAPITAL
- Source statement: 131. Interaction avec HOT/WARM/COLD: Un fill peut modifier le capital reachable. Donc après changement significatif d’inventaire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `131. Interaction avec HOT/WARM/COLD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0228`; supporting items: SRC-001-ITEM-0049, SRC-006-ITEM-0332, SRC-007-ITEM-0115; domain indexes `EXECUTION, HOT_WARM_COLD, DEPLOYMENT, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0135 — 132. Batching Hyperliquid

- Source: `SRC-004`
- Location: lines 3069–3082; heading `132. Batching Hyperliquid`
- Domain tags: EXECUTION, RISK, INFRA, BENCHMARK, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 132. Batching Hyperliquid: La documentation Hyperliquid recommande, pour les stratégies automatisées, de centraliser ordres/cancels dans une tâche de batching et cite une cadence de 0,1 seconde, tout en séparant idéalement les batches ALO des IOC/GTC car les batches ALO-only bénéficient d’un traitement spécifique.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `132. Batching Hyperliquid` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0229`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RISK, INFRA, BENCHMARK, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0136 — 133. WebSocket POST vs HTTP POST

- Source: `SRC-004`
- Location: lines 3083–3105; heading `133. WebSocket POST vs HTTP POST`
- Domain tags: EXECUTION, BENCHMARK, ARCH
- Source statement: 133. WebSocket POST vs HTTP POST: Hyperliquid permet également l’envoi de requêtes via WebSocket en alternative à HTTP. Le benchmark décidera lequel donne :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `133. WebSocket POST vs HTTP POST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0230`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, BENCHMARK, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0137 — 134. Execution State Machine — règle absolue

- Source: `SRC-004`
- Location: lines 3106–3109; heading `134. Execution State Machine — règle absolue`
- Domain tags: EXECUTION
- Source statement: 134. Execution State Machine — règle absolue: La règle fondamentale est : On ne déduit jamais l’état économique du compte à partir de ce que nous pensions envoyer. On le déduit des fills et de l’état exchange réellement observés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `134. Execution State Machine — règle absolue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0231`; supporting items: SRC-006-ITEM-0391, SRC-005-ITEM-0473; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0138 — 135. Deuxième règle absolue

- Source: `SRC-004`
- Location: lines 3110–3112; heading `135. Deuxième règle absolue`
- Domain tags: EXECUTION, RECONCILIATION
- Source statement: 135. Deuxième règle absolue: Toute ambiguïté bloque la prise de nouveau risque sur les ressources concernées jusqu’à reconciliation.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `135. Deuxième règle absolue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0232`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0139 — 136. Troisième règle absolue

- Source: `SRC-004`
- Location: lines 3113–3115; heading `136. Troisième règle absolue`
- Domain tags: EXECUTION, QUANT
- Source statement: 136. Troisième règle absolue: Une jambe suivante utilise toujours la quantité réellement obtenue par la jambe précédente, jamais la quantité théorique prévue avant exécution.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `136. Troisième règle absolue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0233`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0140 — 137. Quatrième règle absolue

- Source: `SRC-004`
- Location: lines 3116–3118; heading `137. Quatrième règle absolue`
- Domain tags: EXECUTION, RECOVERY, ROUTING
- Source statement: 137. Quatrième règle absolue: Une route originale n’a aucun droit particulier après un partial fill : le système choisit alors la meilleure continuation ou recovery à partir de l’état réel.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `137. Quatrième règle absolue` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0234`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0141 — 138. Cinquième règle absolue

- Source: `SRC-004`
- Location: lines 3119–3121; heading `138. Cinquième règle absolue`
- Domain tags: EXECUTION
- Source statement: 138. Cinquième règle absolue: Cancel, timeout et erreur réseau ne signifient jamais automatiquement “ordre non exécuté”.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `138. Cinquième règle absolue` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0235`; supporting items: none found by conservative heading match; domain indexes `EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0142 — 139. Sixième règle absolue

- Source: `SRC-004`
- Location: lines 3122–3134; heading `139. Sixième règle absolue`
- Domain tags: EXECUTION, RECOVERY
- Source statement: 139. Sixième règle absolue: Le bot doit toujours pouvoir réduire le risque même lorsqu’il refuse de prendre de nouveaux trades. est un état distinct de :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `139. Sixième règle absolue` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0236`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0143 — 140. Definition of Done de l’Execution State Machine

- Source: `SRC-004`
- Location: lines 3135–3172; heading `140. Definition of Done de l’Execution State Machine`
- Domain tags: EXECUTION, VALIDATION, RECOVERY, RECONCILIATION, DETERMINISM, BENCHMARK, OPERATIONS, ACCOUNTING
- Source statement: 140. Definition of Done de l’Execution State Machine: Le module ne sera pas considéré comme terminé parce qu’il : Il sera considéré validé lorsque :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `140. Definition of Done de l’Execution State Machine` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0237`; supporting items: SRC-006-ITEM-0278, SRC-006-ITEM-0391, SRC-005-ITEM-0473; domain indexes `EXECUTION, VALIDATION, RECOVERY, RECONCILIATION, DETERMINISM, BENCHMARK, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0144 — 141. Architecture finale de cette brique

- Source: `SRC-004`
- Location: lines 3173–3217; heading `141. Architecture finale de cette brique`
- Domain tags: EXECUTION, ARCH, RECOVERY, RECONCILIATION, DEPLOYMENT, ROUTING
- Source statement: 141. Architecture finale de cette brique: STRATEGY ExecutionPlan
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `141. Architecture finale de cette brique` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0238`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, ARCH, RECOVERY, RECONCILIATION, DEPLOYMENT, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0145 — 142. Conclusion

- Source: `SRC-004`
- Location: lines 3218–3309; heading `142. Conclusion`
- Domain tags: EXECUTION, RECOVERY, OPERATIONS, INVENTORY, SIZING, QUANT
- Source statement: 142. Conclusion: Cette state machine doit rendre impossible, par construction, les comportements les plus dangereux : use of stale theoretical quantity
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `142. Conclusion` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-EXEC-0239`; supporting items: none found by conservative heading match; domain indexes `EXECUTION, RECOVERY, OPERATIONS, INVENTORY, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0148 — 1. Statuts des formules

- Source: `SRC-004`
- Location: lines 3312–3398; heading `1. Statuts des formules`
- Domain tags: FORMULA, INFRA, SURVIVAL, INVENTORY, QUANT, FUTURE
- Source statement: 1. Statuts des formules: Chaque formule reçoit l’un de ces trois statuts. La définition mathématique est déterminée.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `1. Statuts des formules` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0003`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, SURVIVAL, INVENTORY, QUANT, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0149 — 2. Conventions générales

- Source: `SRC-004`
- Location: lines 3399–3400; heading `2. Conventions générales`
- Domain tags: FORMULA
- Source statement: 2. Conventions générales: Toutes les formules doivent respecter les mêmes conventions.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `2. Conventions générales` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0004`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0150 — Prix

- Source: `SRC-004`
- Location: lines 3401–3440; heading `Prix`
- Domain tags: FORMULA
- Source statement: Prix: Pour un marché : M=(B,Q)
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Prix` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0005`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0151 — 3. Quantité

- Source: `SRC-004`
- Location: lines 3441–3456; heading `3. Quantité`
- Domain tags: FORMULA, QUANT
- Source statement: 3. Quantité: désigne une quantité de base. désigne une quantité de quote.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `3. Quantité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0006`; supporting items: none found by conservative heading match; domain indexes `FORMULA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0152 — 4. Convention PnL

- Source: `SRC-004`
- Location: lines 3457–3494; heading `4. Convention PnL`
- Domain tags: FORMULA, ACCOUNTING, RISK
- Source statement: 4. Convention PnL: Pour les variables Loss : Cela évite les erreurs de signe dans VaR/CVaR.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `4. Convention PnL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0007`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0153 — 5. Basis points

- Source: `SRC-004`
- Location: lines 3495–3518; heading `5. Basis points`
- Domain tags: FORMULA
- Source statement: 5. Basis points: 1bp=10^{-4} Conversion :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `5. Basis points` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0008`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0154 — 6. FORMULA QF-001 — Mid Price

- Source: `SRC-004`
- Location: lines 3519–3536; heading `6. FORMULA QF-001 — Mid Price`
- Domain tags: FORMULA
- Source statement: 6. FORMULA QF-001 — Mid Price: Mid_t = \frac{ Bid_t+Ask_t }{2}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `6. FORMULA QF-001 — Mid Price` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0009`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-001; external revalidation: NO.

### SRC-004-ITEM-0155 — Où

- Source: `SRC-004`
- Location: lines 3537–3541; heading `Où`
- Domain tags: FORMULA, MICROSTRUCTURE, QUANT
- Source statement: Où: quant/microstructure/mid.rs
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Où` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0010`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0156 — Utilisation

- Source: `SRC-004`
- Location: lines 3542–3550; heading `Utilisation`
- Domain tags: FORMULA, CROSS_MARKET, MICROSTRUCTURE, MAKER_MODEL, QUANT
- Source statement: Utilisation: reference price volatility
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Utilisation` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0011`; supporting items: none found by conservative heading match; domain indexes `FORMULA, CROSS_MARKET, MICROSTRUCTURE, MAKER_MODEL, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0157 — Cas invalide

- Source: `SRC-004`
- Location: lines 3551–3562; heading `Cas invalide`
- Domain tags: FORMULA
- Source statement: Cas invalide: sans raison explicable par la structure du marché :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Cas invalide` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0012`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0158 — 7. QF-002 — Absolute Spread

- Source: `SRC-004`
- Location: lines 3563–3588; heading `7. QF-002 — Absolute Spread`
- Domain tags: FORMULA
- Source statement: 7. QF-002 — Absolute Spread: Spread_t = Ask_t-Bid_t
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `7. QF-002 — Absolute Spread` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0013`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-002; external revalidation: NO.

### SRC-004-ITEM-0159 — 8. QF-003 — Relative Spread

- Source: `SRC-004`
- Location: lines 3589–3640; heading `8. QF-003 — Relative Spread`
- Domain tags: FORMULA
- Source statement: 8. QF-003 — Relative Spread: SpreadBps_t = 10^4SpreadRel_t
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `8. QF-003 — Relative Spread` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0014`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-003; external revalidation: NO.

### SRC-004-ITEM-0160 — Pourquoi

- Source: `SRC-004`
- Location: lines 3641–3650; heading `Pourquoi`
- Domain tags: FORMULA
- Source statement: Pourquoi: Permet de comparer : tokens à faible prix
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Pourquoi` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0015`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0161 — 9. QF-004 — Cumulative Base Depth

- Source: `SRC-004`
- Location: lines 3651–3682; heading `9. QF-004 — Cumulative Base Depth`
- Domain tags: FORMULA
- Source statement: 9. QF-004 — Cumulative Base Depth: DepthBase_s(K) = \sum_{i=1}^{K}q_i
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `9. QF-004 — Cumulative Base Depth` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0016`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-004; external revalidation: NO.

### SRC-004-ITEM-0162 — 10. QF-005 — Cumulative Quote Depth

- Source: `SRC-004`
- Location: lines 3683–3709; heading `10. QF-005 — Cumulative Quote Depth`
- Domain tags: FORMULA
- Source statement: 10. QF-005 — Cumulative Quote Depth: DepthQuote_s(K) = \sum_{i=1}^{K}p_iq_i
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `10. QF-005 — Cumulative Quote Depth` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0017`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-005; external revalidation: NO.

### SRC-004-ITEM-0163 — Utilisation

- Source: `SRC-004`
- Location: lines 3710–3718; heading `Utilisation`
- Domain tags: FORMULA, SIZING, QUANT
- Source statement: Utilisation: sizing impact
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Utilisation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0018`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0164 — 11. QF-006 — Depth Within Price Band

- Source: `SRC-004`
- Location: lines 3719–3792; heading `11. QF-006 — Depth Within Price Band`
- Domain tags: FORMULA
- Source statement: 11. QF-006 — Depth Within Price Band: D_{bid}(\delta) = \sum_{i: p_i\geq Bid_1(1-\delta)} p_iq_i
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `11. QF-006 — Depth Within Price Band` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0019`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-006; external revalidation: NO.

### SRC-004-ITEM-0165 — 12. QF-007 — Hyperliquid Size Quantization

- Source: `SRC-004`
- Location: lines 3793–3826; heading `12. QF-007 — Hyperliquid Size Quantization`
- Domain tags: FORMULA, QUANT, EXECUTION, RISK
- Source statement: 12. QF-007 — Hyperliquid Size Quantization: q_{valid} = \left\lfloor q10^d \right\rfloor10^{-d}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `12. QF-007 — Hyperliquid Size Quantization` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0020`; supporting items: none found by conservative heading match; domain indexes `FORMULA, QUANT, EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-007; external revalidation: NO.

### SRC-004-ITEM-0166 — 13. QF-008 — Hyperliquid Price Validity

- Source: `SRC-004`
- Location: lines 3827–3847; heading `13. QF-008 — Hyperliquid Price Validity`
- Domain tags: FORMULA, QUANT
- Source statement: 13. QF-008 — Hyperliquid Price Validity: maximum decimal places = 8 - szDecimals
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `13. QF-008 — Hyperliquid Price Validity` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0021`; supporting items: none found by conservative heading match; domain indexes `FORMULA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-008; external revalidation: NO.

### SRC-004-ITEM-0167 — 14. QF-009 — Book Walk Base → Quote

- Source: `SRC-004`
- Location: lines 3848–3913; heading `14. QF-009 — Book Walk Base → Quote`
- Domain tags: FORMULA, EXECUTION
- Source statement: 14. QF-009 — Book Walk Base → Quote: \sum_i x_i=q_B^{filled}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `14. QF-009 — Book Walk Base → Quote` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0022`; supporting items: SRC-007-ITEM-0164; domain indexes `FORMULA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-009; external revalidation: NO.

### SRC-004-ITEM-0168 — 15. QF-010 — Book Walk Quote → Base

- Source: `SRC-004`
- Location: lines 3914–3971; heading `15. QF-010 — Book Walk Quote → Base`
- Domain tags: FORMULA
- Source statement: 15. QF-010 — Book Walk Quote → Base: GrossBase = \sum_i x_i
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `15. QF-010 — Book Walk Quote → Base` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0023`; supporting items: SRC-007-ITEM-0164; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-010; external revalidation: NO.

### SRC-004-ITEM-0169 — 16. QF-011 — VWAP

- Source: `SRC-004`
- Location: lines 3972–4012; heading `16. QF-011 — VWAP`
- Domain tags: FORMULA, EXECUTION, QUANT
- Source statement: 16. QF-011 — VWAP: VWAP = undefined
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `16. QF-011 — VWAP` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0024`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-011; external revalidation: NO.

### SRC-004-ITEM-0170 — 17. QF-012 — Mechanical Slippage BUY

- Source: `SRC-004`
- Location: lines 4013–4076; heading `17. QF-012 — Mechanical Slippage BUY`
- Domain tags: FORMULA
- Source statement: 17. QF-012 — Mechanical Slippage BUY: SlippageBps = 10^4Slippage
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `17. QF-012 — Mechanical Slippage BUY` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0025`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-012; external revalidation: NO.

### SRC-004-ITEM-0171 — 18. QF-013 — Mechanical Slippage SELL

- Source: `SRC-004`
- Location: lines 4077–4120; heading `18. QF-013 — Mechanical Slippage SELL`
- Domain tags: FORMULA, PRODUCT, RISK
- Source statement: 18. QF-013 — Mechanical Slippage SELL: Slippage_{sell} = \frac{ Bid_1-VWAP }{ Bid_1 }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `18. QF-013 — Mechanical Slippage SELL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0026`; supporting items: none found by conservative heading match; domain indexes `FORMULA, PRODUCT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-013; external revalidation: NO.

### SRC-004-ITEM-0172 — 19. QF-014 — Fee Rate

- Source: `SRC-004`
- Location: lines 4121–4148; heading `19. QF-014 — Fee Rate`
- Domain tags: FORMULA, ACCOUNTING, EXECUTION
- Source statement: 19. QF-014 — Fee Rate: maker spot rate = userSpotAddRate
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `19. QF-014 — Fee Rate` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0027`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-014; external revalidation: NO.

### SRC-004-ITEM-0173 — 20. QF-015 — Fee Amount

- Source: `SRC-004`
- Location: lines 4149–4181; heading `20. QF-015 — Fee Amount`
- Domain tags: FORMULA, ACCOUNTING, RECONCILIATION
- Source statement: 20. QF-015 — Fee Amount: FeeValue = Notional \times f
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `20. QF-015 — Fee Amount` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0028`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-015; external revalidation: NO.

### SRC-004-ITEM-0174 — 21. QF-016 — NetConvert

- Source: `SRC-004`
- Location: lines 4182–4325; heading `21. QF-016 — NetConvert`
- Domain tags: FORMULA, ROUTING, ACCOUNTING, QUANT, PRODUCT, ARCH
- Source statement: 21. QF-016 — NetConvert: EconomicOutput = GrossOutput - FeeValueConverted
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `21. QF-016 — NetConvert` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0029`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ROUTING, ACCOUNTING, QUANT, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-016; external revalidation: NO.

### SRC-004-ITEM-0175 — 22. QF-017 — Direct Route Output

- Source: `SRC-004`
- Location: lines 4326–4358; heading `22. QF-017 — Direct Route Output`
- Domain tags: FORMULA, ROUTING
- Source statement: 22. QF-017 — Direct Route Output: D(q_A) = NetConvert(A,B,q_A)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `22. QF-017 — Direct Route Output` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0030`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-017; external revalidation: NO.

### SRC-004-ITEM-0176 — 23. QF-018 — 2-Leg Indirect Output

- Source: `SRC-004`
- Location: lines 4359–4415; heading `23. QF-018 — 2-Leg Indirect Output`
- Domain tags: FORMULA, ROUTING
- Source statement: 23. QF-018 — 2-Leg Indirect Output: I(q_A) = NetConvert(X,B,q_X)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `23. QF-018 — 2-Leg Indirect Output` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0031`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-018; external revalidation: NO.

### SRC-004-ITEM-0177 — 24. QF-019 — OWA Relative Edge

- Source: `SRC-004`
- Location: lines 4416–4466; heading `24. QF-019 — OWA Relative Edge`
- Domain tags: FORMULA, OWA
- Source statement: 24. QF-019 — OWA Relative Edge: Edge_{OWA,bps} = 10^4Edge_{OWA}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `24. QF-019 — OWA Relative Edge` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0032`; supporting items: none found by conservative heading match; domain indexes `FORMULA, OWA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-019; external revalidation: NO.

### SRC-004-ITEM-0178 — 25. QF-020 — OWA Absolute Gain

- Source: `SRC-004`
- Location: lines 4467–4493; heading `25. QF-020 — OWA Absolute Gain`
- Domain tags: FORMULA, OWA
- Source statement: 25. QF-020 — OWA Absolute Gain: Gain_B(q_A) = I(q_A)-D(q_A)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `25. QF-020 — OWA Absolute Gain` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0033`; supporting items: none found by conservative heading match; domain indexes `FORMULA, OWA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-020; external revalidation: NO.

### SRC-004-ITEM-0179 — 26. QF-021 — Triangular Output

- Source: `SRC-004`
- Location: lines 4494–4572; heading `26. QF-021 — Triangular Output`
- Domain tags: FORMULA, TRIANGLE, ROUTING
- Source statement: 26. QF-021 — Triangular Output: q'_A = NetConvert(B,A,q_B)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `26. QF-021 — Triangular Output` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0034`; supporting items: none found by conservative heading match; domain indexes `FORMULA, TRIANGLE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-021; external revalidation: NO.

### SRC-004-ITEM-0180 — 27. QF-022 — Triangle Return

- Source: `SRC-004`
- Location: lines 4573–4597; heading `27. QF-022 — Triangle Return`
- Domain tags: FORMULA, TRIANGLE
- Source statement: 27. QF-022 — Triangle Return: R_{triangle}(q_A) = \frac{ q'_A }{ q_A } -1
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `27. QF-022 — Triangle Return` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0035`; supporting items: none found by conservative heading match; domain indexes `FORMULA, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-022; external revalidation: NO.

### SRC-004-ITEM-0181 — 28. QF-023 — Triangle PnL

- Source: `SRC-004`
- Location: lines 4598–4616; heading `28. QF-023 — Triangle PnL`
- Domain tags: FORMULA, ACCOUNTING, TRIANGLE
- Source statement: 28. QF-023 — Triangle PnL: PnL_A(q_A) = q'_A-q_A
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `28. QF-023 — Triangle PnL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0036`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-023; external revalidation: NO.

### SRC-004-ITEM-0182 — 29. QF-024 — Conversion Alpha

- Source: `SRC-004`
- Location: lines 4617–4671; heading `29. QF-024 — Conversion Alpha`
- Domain tags: FORMULA
- Source statement: 29. QF-024 — Conversion Alpha: ConversionAlpha = \frac{ Output_{Indirect,TT} }{ Output_{Direct,T} } -1
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `29. QF-024 — Conversion Alpha` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0037`; supporting items: SRC-007-ITEM-0180; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-024; external revalidation: NO.

### SRC-004-ITEM-0183 — 30. QF-025 — Execution Alpha

- Source: `SRC-004`
- Location: lines 4672–4739; heading `30. QF-025 — Execution Alpha`
- Domain tags: FORMULA, EXECUTION, ROUTING
- Source statement: 30. QF-025 — Execution Alpha: ExecutionAlpha_{MT} = \frac{ Output_{Indirect,MT} }{ Output_{Indirect,TT} } -1
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `30. QF-025 — Execution Alpha` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0038`; supporting items: SRC-007-ITEM-0180; domain indexes `FORMULA, EXECUTION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-025; external revalidation: NO.

### SRC-004-ITEM-0184 — 31. QF-026 — Edge Curve

- Source: `SRC-004`
- Location: lines 4740–4765; heading `31. QF-026 — Edge Curve`
- Domain tags: FORMULA, RISK, ACCOUNTING
- Source statement: 31. QF-026 — Edge Curve: est calculé en répétant la simulation pour différentes tailles Il ne s’agit pas d’une interpolation théorique imposée.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `31. QF-026 — Edge Curve` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0039`; supporting items: SRC-007-ITEM-0178; domain indexes `FORMULA, RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-026; external revalidation: NO.

### SRC-004-ITEM-0185 — 32. QF-027 — Maximum Profitable Size

- Source: `SRC-004`
- Location: lines 4766–4803; heading `32. QF-027 — Maximum Profitable Size`
- Domain tags: FORMULA, ACCOUNTING, MICROSTRUCTURE
- Source statement: 32. QF-027 — Maximum Profitable Size: Q_{profitable} = \sup \{ q: E(q)\geq E_{min} \}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `32. QF-027 — Maximum Profitable Size` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0040`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-027; external revalidation: NO.

### SRC-004-ITEM-0186 — 33. QF-028 — Queue Imbalance

- Source: `SRC-004`
- Location: lines 4804–4859; heading `33. QF-028 — Queue Imbalance`
- Domain tags: FORMULA, MICROSTRUCTURE, INVENTORY, EXECUTION
- Source statement: 33. QF-028 — Queue Imbalance: Q_{bid}+Q_{ask}=0
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `33. QF-028 — Queue Imbalance` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0041`; supporting items: SRC-007-ITEM-0026, SRC-007-ITEM-0300; domain indexes `FORMULA, MICROSTRUCTURE, INVENTORY, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-028; external revalidation: NO.

### SRC-004-ITEM-0187 — 34. QF-029 — Multi-Level Imbalance

- Source: `SRC-004`
- Location: lines 4860–4925; heading `34. QF-029 — Multi-Level Imbalance`
- Domain tags: FORMULA, MICROSTRUCTURE, INVENTORY
- Source statement: 34. QF-029 — Multi-Level Imbalance: QI_K = \frac{ \sum_{k=1}^Kw_kQ^b_k - \sum_{k=1}^Kw_kQ^a_k }{ \sum_{k=1}^Kw_kQ^b_k + \sum_{k=1}^Kw_kQ^a_k }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `34. QF-029 — Multi-Level Imbalance` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0042`; supporting items: SRC-007-ITEM-0025, SRC-007-ITEM-0200; domain indexes `FORMULA, MICROSTRUCTURE, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-029; external revalidation: NO.

### SRC-004-ITEM-0188 — 35. QF-030 — Event-Level Bid OFI Contribution

- Source: `SRC-004`
- Location: lines 4926–4971; heading `35. QF-030 — Event-Level Bid OFI Contribution`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: 35. QF-030 — Event-Level Bid OFI Contribution: e^b_n = \mathbf1_{P^b_n\geq P^b_{n-1}}Q^b_n - \mathbf1_{P^b_n\leq P^b_{n-1}}Q^b_{n-1}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `35. QF-030 — Event-Level Bid OFI Contribution` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0043`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-030; external revalidation: NO.

### SRC-004-ITEM-0189 — 36. QF-031 — Ask OFI Contribution

- Source: `SRC-004`
- Location: lines 4972–5008; heading `36. QF-031 — Ask OFI Contribution`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: 36. QF-031 — Ask OFI Contribution: e^a_n = \mathbf1_{P^a_n\leq P^a_{n-1}}Q^a_n - \mathbf1_{P^a_n\geq P^a_{n-1}}Q^a_{n-1}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `36. QF-031 — Ask OFI Contribution` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0044`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-031; external revalidation: NO.

### SRC-004-ITEM-0190 — 37. QF-032 — OFI

- Source: `SRC-004`
- Location: lines 5009–5041; heading `37. QF-032 — OFI`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: 37. QF-032 — OFI: OFI_W = \sum_{n\in W}OFI_n
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `37. QF-032 — OFI` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0045`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-032; external revalidation: NO.

### SRC-004-ITEM-0191 — Important

- Source: `SRC-004`
- Location: lines 5042–5050; heading `Important`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: Important: Avec le public L2 snapshot Hyperliquid, cette grandeur est : et non un véritable event-by-event OFI si plusieurs événements ont eu lieu entre snapshots.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Important` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0046`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0192 — 38. QF-033 — Multi-Level OFI

- Source: `SRC-004`
- Location: lines 5051–5094; heading `38. QF-033 — Multi-Level OFI`
- Domain tags: FORMULA, MICROSTRUCTURE, FUTURE
- Source statement: 38. QF-033 — Multi-Level OFI: MLOFI = \sum_{k=1}^{K} w_kOFI^{(k)}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `38. QF-033 — Multi-Level OFI` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0047`; supporting items: SRC-007-ITEM-0025, SRC-007-ITEM-0200; domain indexes `FORMULA, MICROSTRUCTURE, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-033; external revalidation: NO.

### SRC-004-ITEM-0193 — 39. QF-034 — Microprice

- Source: `SRC-004`
- Location: lines 5095–5154; heading `39. QF-034 — Microprice`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: 39. QF-034 — Microprice: MicroPrice = \frac{ AskQ_{bid} + BidQ_{ask} }{ Q_{bid}+Q_{ask} }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `39. QF-034 — Microprice` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0048`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-034; external revalidation: NO.

### SRC-004-ITEM-0194 — 40. QF-035 — Microprice Dislocation

- Source: `SRC-004`
- Location: lines 5155–5232; heading `40. QF-035 — Microprice Dislocation`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: 40. QF-035 — Microprice Dislocation: MicroDislocation_{bps} = 10^4MicroDislocation
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `40. QF-035 — Microprice Dislocation` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0049`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-035; external revalidation: NO.

### SRC-004-ITEM-0195 — 41. QF-036 — Log Return

- Source: `SRC-004`
- Location: lines 5233–5262; heading `41. QF-036 — Log Return`
- Domain tags: FORMULA, MICROSTRUCTURE
- Source statement: 41. QF-036 — Log Return: r_t = \ln \left( \frac{P_t}{P_{t-1}} \right)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `41. QF-036 — Log Return` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0050`; supporting items: none found by conservative heading match; domain indexes `FORMULA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-036; external revalidation: NO.

### SRC-004-ITEM-0196 — 42. QF-037 — Realized Variance

- Source: `SRC-004`
- Location: lines 5263–5281; heading `42. QF-037 — Realized Variance`
- Domain tags: FORMULA
- Source statement: 42. QF-037 — Realized Variance: RV_W = \sum_{t\in W}r_t^2
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `42. QF-037 — Realized Variance` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0051`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-037; external revalidation: NO.

### SRC-004-ITEM-0197 — 43. QF-038 — Realized Volatility

- Source: `SRC-004`
- Location: lines 5282–5298; heading `43. QF-038 — Realized Volatility`
- Domain tags: FORMULA, QUANT, RISK, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 43. QF-038 — Realized Volatility: \sigma_W = \sqrt{RV_W}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `43. QF-038 — Realized Volatility` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0052`; supporting items: none found by conservative heading match; domain indexes `FORMULA, QUANT, RISK, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-038; external revalidation: NO.

### SRC-004-ITEM-0198 — 44. QF-039 — Robust Jump Score

- Source: `SRC-004`
- Location: lines 5299–5363; heading `44. QF-039 — Robust Jump Score`
- Domain tags: FORMULA, ARCH
- Source statement: 44. QF-039 — Robust Jump Score: JumpScore_t = \frac{ |r_t| }{ \sigma_{fast,t}+\epsilon }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `44. QF-039 — Robust Jump Score` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0053`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-039; external revalidation: NO.

### SRC-004-ITEM-0199 — 45. QF-040 — Depth Participation

- Source: `SRC-004`
- Location: lines 5364–5409; heading `45. QF-040 — Depth Participation`
- Domain tags: FORMULA, ROUTING
- Source statement: 45. QF-040 — Depth Participation: DP(q,\delta) = \frac{ Notional(q) }{ DepthQuote(\delta) }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `45. QF-040 — Depth Participation` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0054`; supporting items: SRC-007-ITEM-0213; domain indexes `FORMULA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-040; external revalidation: NO.

### SRC-004-ITEM-0200 — 46. QF-041 — Volume Participation

- Source: `SRC-004`
- Location: lines 5410–5446; heading `46. QF-041 — Volume Participation`
- Domain tags: FORMULA, EXECUTION
- Source statement: 46. QF-041 — Volume Participation: VP(q,W) = \frac{ Notional(q) }{ ExecutedVolume_W }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `46. QF-041 — Volume Participation` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0055`; supporting items: SRC-005-ITEM-0046, SRC-007-ITEM-0214; domain indexes `FORMULA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-041; external revalidation: NO.

### SRC-004-ITEM-0201 — Pourquoi

- Source: `SRC-004`
- Location: lines 5447–5459; heading `Pourquoi`
- Domain tags: FORMULA, QUANT
- Source statement: Pourquoi: ne doivent pas utiliser la même confidence d’impact.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `Pourquoi` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0056`; supporting items: none found by conservative heading match; domain indexes `FORMULA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0202 — 47. QF-042 — Mechanical Impact

- Source: `SRC-004`
- Location: lines 5460–5515; heading `47. QF-042 — Mechanical Impact`
- Domain tags: FORMULA, QUANT, PRODUCT
- Source statement: 47. QF-042 — Mechanical Impact: Impact_{sell} = \frac{ Mid_0-VWAP }{ Mid_0 }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `47. QF-042 — Mechanical Impact` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0057`; supporting items: SRC-007-ITEM-0069, SRC-007-ITEM-0211, SRC-008-ITEM-0006; domain indexes `FORMULA, QUANT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-042; external revalidation: NO.

### SRC-004-ITEM-0203 — 48. QF-043 — Liquidity Resilience

- Source: `SRC-004`
- Location: lines 5516–5583; heading `48. QF-043 — Liquidity Resilience`
- Domain tags: FORMULA, LIQUIDITY_RESPONSE, EXECUTION, INFRA
- Source statement: 48. QF-043 — Liquidity Resilience: Resilience(t) = \frac{ D_t-D_s }{ D_0-D_s }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `48. QF-043 — Liquidity Resilience` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0058`; supporting items: SRC-007-ITEM-0216; domain indexes `FORMULA, LIQUIDITY_RESPONSE, EXECUTION, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-043; external revalidation: NO.

### SRC-004-ITEM-0204 — 49. QF-044 — Survival Function

- Source: `SRC-004`
- Location: lines 5584–5610; heading `49. QF-044 — Survival Function`
- Domain tags: FORMULA, SURVIVAL
- Source statement: 49. QF-044 — Survival Function: T = \text{temps restant jusqu'à mort de l'edge}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `49. QF-044 — Survival Function` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0059`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-044; external revalidation: NO.

### SRC-004-ITEM-0205 — 50. QF-045 — Discrete Hazard

- Source: `SRC-004`
- Location: lines 5611–5674; heading `50. QF-045 — Discrete Hazard`
- Domain tags: FORMULA, SURVIVAL
- Source statement: 50. QF-045 — Discrete Hazard: \sigma(z) = \frac1{1+e^{-z}}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `50. QF-045 — Discrete Hazard` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LEARNED`
- Cross-source references: `REQ-FORMULA-0060`; supporting items: SRC-007-ITEM-0087; domain indexes `FORMULA, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-045; external revalidation: NO.

### SRC-004-ITEM-0206 — 51. QF-046 — Survival from Discrete Hazard

- Source: `SRC-004`
- Location: lines 5675–5693; heading `51. QF-046 — Survival from Discrete Hazard`
- Domain tags: FORMULA, SURVIVAL, QUANT, PRODUCT
- Source statement: 51. QF-046 — Survival from Discrete Hazard: S_k = \prod_{j=1}^{k} (1-h_j)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `51. QF-046 — Survival from Discrete Hazard` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0061`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SURVIVAL, QUANT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-046; external revalidation: NO.

### SRC-004-ITEM-0207 — 52. QF-047 — Edge Half-Life

- Source: `SRC-004`
- Location: lines 5694–5726; heading `52. QF-047 — Edge Half-Life`
- Domain tags: FORMULA, SURVIVAL
- Source statement: 52. QF-047 — Edge Half-Life: t_{50} = \inf \{ t:S(t)\leq0.5 \}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `52. QF-047 — Edge Half-Life` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0062`; supporting items: SRC-007-ITEM-0022, SRC-007-ITEM-0191; domain indexes `FORMULA, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-047; external revalidation: NO.

### SRC-004-ITEM-0208 — 53. QF-048 — Capture Probability

- Source: `SRC-004`
- Location: lines 5727–5784; heading `53. QF-048 — Capture Probability`
- Domain tags: FORMULA, SURVIVAL, QUANT, INFRA
- Source statement: 53. QF-048 — Capture Probability: P_{capture} = \sum_{m=1}^{M} P(L\in B_m) S(\ell_m)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `53. QF-048 — Capture Probability` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0063`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SURVIVAL, QUANT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-048; external revalidation: NO.

### SRC-004-ITEM-0209 — 54. QF-049 — Expected Edge at Arrival

- Source: `SRC-004`
- Location: lines 5785–5817; heading `54. QF-049 — Expected Edge at Arrival`
- Domain tags: FORMULA, PRODUCT
- Source statement: 54. QF-049 — Expected Edge at Arrival: E_{arrival} = E[ Edge_{t+L} | X_t ]
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `54. QF-049 — Expected Edge at Arrival` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LEARNED`
- Cross-source references: `REQ-FORMULA-0064`; supporting items: SRC-005-ITEM-0051, SRC-007-ITEM-0064, SRC-007-ITEM-0194; domain indexes `FORMULA, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-049; external revalidation: NO.

### SRC-004-ITEM-0210 — 55. QF-050 — Probability Above Execution Threshold

- Source: `SRC-004`
- Location: lines 5818–5861; heading `55. QF-050 — Probability Above Execution Threshold`
- Domain tags: FORMULA, QUANT
- Source statement: 55. QF-050 — Probability Above Execution Threshold: P_{exec} = P( Edge_{t+L} > E_{minimum} | X_t )
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `55. QF-050 — Probability Above Execution Threshold` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LEARNED`
- Cross-source references: `REQ-FORMULA-0065`; supporting items: SRC-007-ITEM-0324; domain indexes `FORMULA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-050; external revalidation: NO.

### SRC-004-ITEM-0211 — 56. QF-051 — Maker Fill Survival

- Source: `SRC-004`
- Location: lines 5862–5889; heading `56. QF-051 — Maker Fill Survival`
- Domain tags: FORMULA, EXECUTION, SURVIVAL, MAKER_MODEL
- Source statement: 56. QF-051 — Maker Fill Survival: S_f(t|X) = P(T_f>t|X)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `56. QF-051 — Maker Fill Survival` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LEARNED`
- Cross-source references: `REQ-FORMULA-0066`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, SURVIVAL, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-051; external revalidation: NO.

### SRC-004-ITEM-0212 — 57. QF-052 — Maker Fill CDF

- Source: `SRC-004`
- Location: lines 5890–5925; heading `57. QF-052 — Maker Fill CDF`
- Domain tags: FORMULA, EXECUTION, MAKER_MODEL, SURVIVAL
- Source statement: 57. QF-052 — Maker Fill CDF: P(T_f\leq t)=F_f(t)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `57. QF-052 — Maker Fill CDF` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0067`; supporting items: SRC-005-ITEM-0085, SRC-006-ITEM-0344; domain indexes `FORMULA, EXECUTION, MAKER_MODEL, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-052; external revalidation: NO.

### SRC-004-ITEM-0213 — 58. QF-053 — Expected Fill Time

- Source: `SRC-004`
- Location: lines 5926–5971; heading `58. QF-053 — Expected Fill Time`
- Domain tags: FORMULA, EXECUTION
- Source statement: 58. QF-053 — Expected Fill Time: E[T_f] = \int_0^\infty S_f(t)\,dt
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `58. QF-053 — Expected Fill Time` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0068`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-053; external revalidation: NO.

### SRC-004-ITEM-0214 — 59. QF-054 — Adverse Selection BUY

- Source: `SRC-004`
- Location: lines 5972–6021; heading `59. QF-054 — Adverse Selection BUY`
- Domain tags: FORMULA, MAKER_MODEL, EXECUTION
- Source statement: 59. QF-054 — Adverse Selection BUY: Positif = mouvement contre nous.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `59. QF-054 — Adverse Selection BUY` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0069`; supporting items: SRC-006-ITEM-0346, SRC-007-ITEM-0042, SRC-007-ITEM-0222, SRC-007-ITEM-0302; domain indexes `FORMULA, MAKER_MODEL, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-054; external revalidation: NO.

### SRC-004-ITEM-0215 — 60. QF-055 — Adverse Selection SELL

- Source: `SRC-004`
- Location: lines 6022–6054; heading `60. QF-055 — Adverse Selection SELL`
- Domain tags: FORMULA, MAKER_MODEL, PRODUCT
- Source statement: 60. QF-055 — Adverse Selection SELL: = mauvais pour nous.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `60. QF-055 — Adverse Selection SELL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0070`; supporting items: SRC-007-ITEM-0222, SRC-008-ITEM-0035; domain indexes `FORMULA, MAKER_MODEL, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-055; external revalidation: NO.

### SRC-004-ITEM-0216 — 61. QF-056 — Expected Value

- Source: `SRC-004`
- Location: lines 6055–6081; heading `61. QF-056 — Expected Value`
- Domain tags: FORMULA, QUANT, ACCOUNTING
- Source statement: 61. QF-056 — Expected Value: \sum_i p_i=1
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `61. QF-056 — Expected Value` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0071`; supporting items: SRC-007-ITEM-0298; domain indexes `FORMULA, QUANT, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-056; external revalidation: NO.

### SRC-004-ITEM-0217 — 62. QF-057 — Execution EV

- Source: `SRC-004`
- Location: lines 6082–6149; heading `62. QF-057 — Execution EV`
- Domain tags: FORMULA, EXECUTION, RECOVERY, ACCOUNTING
- Source statement: 62. QF-057 — Execution EV: X = failure/other terminal scenario
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `62. QF-057 — Execution EV` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0072`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, RECOVERY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-057; external revalidation: NO.

### SRC-004-ITEM-0218 — 63. QF-058 — MT EV

- Source: `SRC-004`
- Location: lines 6150–6245; heading `63. QF-058 — MT EV`
- Domain tags: FORMULA, EXECUTION, RECOVERY
- Source statement: 63. QF-058 — MT EV: EV_{MT} = \sum_k P(T_f\in B_k) EV_{leg2}(t_k) - C_{adverse} - C_{recovery}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `63. QF-058 — MT EV` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0073`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-058; external revalidation: NO.

### SRC-004-ITEM-0219 — 64. QF-059 — Probability of Positive PnL

- Source: `SRC-004`
- Location: lines 6246–6282; heading `64. QF-059 — Probability of Positive PnL`
- Domain tags: FORMULA, ACCOUNTING, QUANT, SIMULATOR
- Source statement: 64. QF-059 — Probability of Positive PnL: \hat P_+ = \frac{ 1 }{ N } \sum_{i=1}^{N} \mathbf1(PnL_i>0)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `64. QF-059 — Probability of Positive PnL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0074`; supporting items: SRC-005-ITEM-0058; domain indexes `FORMULA, ACCOUNTING, QUANT, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-059; external revalidation: NO.

### SRC-004-ITEM-0220 — 65. QF-060 — Loss Variable

- Source: `SRC-004`
- Location: lines 6283–6313; heading `65. QF-060 — Loss Variable`
- Domain tags: FORMULA, RISK, ACCOUNTING, MICROSTRUCTURE, ROUTING, PRODUCT
- Source statement: 65. QF-060 — Loss Variable: Loss = -PnL
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `65. QF-060 — Loss Variable` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0075`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, ACCOUNTING, MICROSTRUCTURE, ROUTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-060; external revalidation: NO.

### SRC-004-ITEM-0221 — 66. QF-061 — VaR

- Source: `SRC-004`
- Location: lines 6314–6342; heading `66. QF-061 — VaR`
- Domain tags: FORMULA, RISK, QUANT, PRODUCT
- Source statement: 66. QF-061 — VaR: = quantile 99 % de la distribution de perte.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `66. QF-061 — VaR` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0076`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, QUANT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-061; external revalidation: NO.

### SRC-004-ITEM-0222 — 67. QF-062 — CVaR / Expected Shortfall

- Source: `SRC-004`
- Location: lines 6343–6391; heading `67. QF-062 — CVaR / Expected Shortfall`
- Domain tags: FORMULA, RISK, PRODUCT
- Source statement: 67. QF-062 — CVaR / Expected Shortfall: ES_\alpha = \frac1{1-\alpha} \int_\alpha^1 VaR_u\,du
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `67. QF-062 — CVaR / Expected Shortfall` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0077`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-062; external revalidation: NO.

### SRC-004-ITEM-0223 — 68. QF-063 — Risk-Adjusted EV

- Source: `SRC-004`
- Location: lines 6392–6491; heading `68. QF-063 — Risk-Adjusted EV`
- Domain tags: FORMULA, RISK, EXECUTION, RECOVERY, ACCOUNTING, INVENTORY
- Source statement: 68. QF-063 — Risk-Adjusted EV: RAEV = EV_{execution} - InventoryPenalty - StrandedPenalty - ModelUncertaintyPenalty
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `68. QF-063 — Risk-Adjusted EV` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0078`; supporting items: SRC-007-ITEM-0275; domain indexes `FORMULA, RISK, EXECUTION, RECOVERY, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-063; external revalidation: NO.

### SRC-004-ITEM-0224 — 69. QF-064 — Normalized Inventory Deviation

- Source: `SRC-004`
- Location: lines 6492–6517; heading `69. QF-064 — Normalized Inventory Deviation`
- Domain tags: FORMULA, INVENTORY
- Source statement: 69. QF-064 — Normalized Inventory Deviation: B_a = scaling band
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `69. QF-064 — Normalized Inventory Deviation` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0079`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-064; external revalidation: NO.

### SRC-004-ITEM-0225 — 70. QF-065 — Soft Inventory Penalty

- Source: `SRC-004`
- Location: lines 6518–6542; heading `70. QF-065 — Soft Inventory Penalty`
- Domain tags: FORMULA, INVENTORY, RISK, REPLAY
- Source statement: 70. QF-065 — Soft Inventory Penalty: Penalty_a = \kappa_a z_a^2
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `70. QF-065 — Soft Inventory Penalty` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0080`; supporting items: SRC-007-ITEM-0243; domain indexes `FORMULA, INVENTORY, RISK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-065; external revalidation: NO.

### SRC-004-ITEM-0226 — 71. QF-066 — Hard Inventory Gate

- Source: `SRC-004`
- Location: lines 6543–6589; heading `71. QF-066 — Hard Inventory Gate`
- Domain tags: FORMULA, INVENTORY, EXECUTION, RISK, FUTURE
- Source statement: 71. QF-066 — Hard Inventory Gate: Pas de pénalité permettant de contourner le hard gate.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `71. QF-066 — Hard Inventory Gate` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0081`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INVENTORY, EXECUTION, RISK, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-066; external revalidation: NO.

### SRC-004-ITEM-0227 — 72. QF-067 — Net Flow

- Source: `SRC-004`
- Location: lines 6590–6622; heading `72. QF-067 — Net Flow`
- Domain tags: FORMULA, RISK
- Source statement: 72. QF-067 — Net Flow: NetFlow_a(W) = \sum_{trades\in W} \Delta I_a
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `72. QF-067 — Net Flow` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0082`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-067; external revalidation: NO.

### SRC-004-ITEM-0228 — 73. QF-068 — Expected Exit Cost

- Source: `SRC-004`
- Location: lines 6623–6692; heading `73. QF-068 — Expected Exit Cost`
- Domain tags: FORMULA, ACCOUNTING, BRIDGE
- Source statement: 73. QF-068 — Expected Exit Cost: ExitCost(X) = CurrentValue(X) - BestExecutableExitValue(X)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `73. QF-068 — Expected Exit Cost` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0083`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, BRIDGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-068; external revalidation: NO.

### SRC-004-ITEM-0229 — 74. QF-069 — Stranded Capital Penalty

- Source: `SRC-004`
- Location: lines 6693–6763; heading `74. QF-069 — Stranded Capital Penalty`
- Domain tags: FORMULA, INVENTORY, CAPITAL, RISK, ACCOUNTING
- Source statement: 74. QF-069 — Stranded Capital Penalty: StrandedPenalty = ExpectedExitCost + ExpectedIdleCost + ExpectedRiskCost
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `74. QF-069 — Stranded Capital Penalty` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0084`; supporting items: SRC-007-ITEM-0246; domain indexes `FORMULA, INVENTORY, CAPITAL, RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-069; external revalidation: NO.

### SRC-004-ITEM-0230 — 75. QF-070 — Bridge Cost

- Source: `SRC-004`
- Location: lines 6764–6820; heading `75. QF-070 — Bridge Cost`
- Domain tags: FORMULA, ACCOUNTING, BRIDGE, RISK, ROUTING
- Source statement: 75. QF-070 — Bridge Cost: BridgeCost(P) = V_{start} - V_{end}^{net} + RiskCost(P)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `75. QF-070 — Bridge Cost` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0085`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, BRIDGE, RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-070; external revalidation: NO.

### SRC-004-ITEM-0231 — 76. QF-071 — Bridge Break-Even Cycles

- Source: `SRC-004`
- Location: lines 6821–6886; heading `76. QF-071 — Bridge Break-Even Cycles`
- Domain tags: FORMULA, BRIDGE, ROUTING, ACCOUNTING
- Source statement: 76. QF-071 — Bridge Break-Even Cycles: N_BE = ∞
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `76. QF-071 — Bridge Break-Even Cycles` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0086`; supporting items: SRC-007-ITEM-0248; domain indexes `FORMULA, BRIDGE, ROUTING, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-071; external revalidation: NO.

### SRC-004-ITEM-0232 — 77. QF-072 — Capital Relocation Value

- Source: `SRC-004`
- Location: lines 6887–7003; heading `77. QF-072 — Capital Relocation Value`
- Domain tags: FORMULA, CAPITAL, BRIDGE, RISK, ACCOUNTING
- Source statement: 77. QF-072 — Capital Relocation Value: Value(move) = EV_{destination} - EV_{stay} - BridgeCost - ExpectedExitCost - RelocationRiskCost
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `77. QF-072 — Capital Relocation Value` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0087`; supporting items: SRC-007-ITEM-0249; domain indexes `FORMULA, CAPITAL, BRIDGE, RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-072; external revalidation: NO.

### SRC-004-ITEM-0233 — 78. QF-073 — Available Balance

- Source: `SRC-004`
- Location: lines 7004–7078; heading `78. QF-073 — Available Balance`
- Domain tags: FORMULA, INVENTORY
- Source statement: 78. QF-073 — Available Balance: AvailableBalance_a = ActualBalance_a - ReservedBalance_a
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `78. QF-073 — Available Balance` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0088`; supporting items: SRC-005-ITEM-0017; domain indexes `FORMULA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-073; external revalidation: NO.

### SRC-004-ITEM-0234 — 79. QF-074 — Available Book Capacity

- Source: `SRC-004`
- Location: lines 7079–7140; heading `79. QF-074 — Available Book Capacity`
- Domain tags: FORMULA, CAPITAL
- Source statement: 79. QF-074 — Available Book Capacity: AvailableCapacity_j = ObservedCapacity_j - ReservedCapacity_j
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `79. QF-074 — Available Book Capacity` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0089`; supporting items: none found by conservative heading match; domain indexes `FORMULA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-074; external revalidation: NO.

### SRC-004-ITEM-0235 — 80. QF-075 — Position Sizing Objective

- Source: `SRC-004`
- Location: lines 7141–7273; heading `80. QF-075 — Position Sizing Objective`
- Domain tags: FORMULA, SIZING, RISK, INVENTORY, CAPITAL, QUANT
- Source statement: 80. QF-075 — Position Sizing Objective: q^* = \arg\max_q RAEV(q)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `80. QF-075 — Position Sizing Objective` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0090`; supporting items: SRC-006-ITEM-0358; domain indexes `FORMULA, SIZING, RISK, INVENTORY, CAPITAL, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-075; external revalidation: NO.

### SRC-004-ITEM-0236 — 81. QF-076 — Validated Capacity

- Source: `SRC-004`
- Location: lines 7274–7313; heading `81. QF-076 — Validated Capacity`
- Domain tags: FORMULA, CAPITAL, SIZING
- Source statement: 81. QF-076 — Validated Capacity: Q_{validated} = \sup \{ q: Gates(q)=TRUE \}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `81. QF-076 — Validated Capacity` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0091`; supporting items: SRC-007-ITEM-0237; domain indexes `FORMULA, CAPITAL, SIZING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-076; external revalidation: NO.

### SRC-004-ITEM-0237 — 82. QF-077 — Sizing Search

- Source: `SRC-004`
- Location: lines 7314–7342; heading `82. QF-077 — Sizing Search`
- Domain tags: FORMULA, SIZING, RISK
- Source statement: 82. QF-077 — Sizing Search: raffinement local entre tailles voisines. peut être discontinu à cause des niveaux du carnet et du rounding.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `82. QF-077 — Sizing Search` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0092`; supporting items: none found by conservative heading match; domain indexes `FORMULA, SIZING, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-077; external revalidation: NO.

### SRC-004-ITEM-0238 — 83. QF-078 — Multi-Opportunity Allocation

- Source: `SRC-004`
- Location: lines 7343–7380; heading `83. QF-078 — Multi-Opportunity Allocation`
- Domain tags: FORMULA, CAPITAL, RISK, INVENTORY
- Source statement: 83. QF-078 — Multi-Opportunity Allocation: \max_{\mathbf q} \sum_{i=1}^{N} RAEV_i(q_i)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `83. QF-078 — Multi-Opportunity Allocation` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0093`; supporting items: none found by conservative heading match; domain indexes `FORMULA, CAPITAL, RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-078; external revalidation: NO.

### SRC-004-ITEM-0239 — 84. QF-079 — Recovery Objective

- Source: `SRC-004`
- Location: lines 7381–7468; heading `84. QF-079 — Recovery Objective`
- Domain tags: FORMULA, RECOVERY, PORTFOLIO
- Source statement: 84. QF-079 — Recovery Objective: a^* = \arg\min_a ExpectedRecoveryLoss(a)
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `84. QF-079 — Recovery Objective` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0094`; supporting items: SRC-006-ITEM-0398; domain indexes `FORMULA, RECOVERY, PORTFOLIO`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-079; external revalidation: NO.

### SRC-004-ITEM-0240 — 85. QF-080 — Recovery Loss

- Source: `SRC-004`
- Location: lines 7469–7546; heading `85. QF-080 — Recovery Loss`
- Domain tags: FORMULA, RECOVERY, ACCOUNTING, PORTFOLIO
- Source statement: 85. QF-080 — Recovery Loss: RecoveryLoss = PortfolioValue_{beforeRecovery} - PortfolioValue_{afterRecovery}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `85. QF-080 — Recovery Loss` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0095`; supporting items: SRC-006-ITEM-0400; domain indexes `FORMULA, RECOVERY, ACCOUNTING, PORTFOLIO`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-080; external revalidation: NO.

### SRC-004-ITEM-0241 — 86. QF-081 — Cross-Market Response

- Source: `SRC-004`
- Location: lines 7547–7587; heading `86. QF-081 — Cross-Market Response`
- Domain tags: FORMULA, CROSS_MARKET, INFRA, PRODUCT
- Source statement: 86. QF-081 — Cross-Market Response: R_{i\rightarrow j}(h) = P( \Delta Market_j(h) | Shock_i,X )
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `86. QF-081 — Cross-Market Response` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LEARNED`
- Cross-source references: `REQ-FORMULA-0096`; supporting items: SRC-007-ITEM-0052, SRC-007-ITEM-0059, SRC-007-ITEM-0132, SRC-007-ITEM-0153; domain indexes `FORMULA, CROSS_MARKET, INFRA, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-081; external revalidation: NO.

### SRC-004-ITEM-0242 — 87. QF-082 — Correction Velocity

- Source: `SRC-004`
- Location: lines 7588–7638; heading `87. QF-082 — Correction Velocity`
- Domain tags: FORMULA, CROSS_MARKET
- Source statement: 87. QF-082 — Correction Velocity: Correction=1
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `87. QF-082 — Correction Velocity` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0097`; supporting items: SRC-007-ITEM-0034; domain indexes `FORMULA, CROSS_MARKET`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-082; external revalidation: NO.

### SRC-004-ITEM-0243 — 88. QF-083 — Competition Hazard

- Source: `SRC-004`
- Location: lines 7639–7659; heading `88. QF-083 — Competition Hazard`
- Domain tags: FORMULA, PARTICIPANTS, SURVIVAL, PRODUCT
- Source statement: 88. QF-083 — Competition Hazard: est le hazard de disparition attribuable à la dynamique concurrentielle/market response. En pratique, la V1 commencera souvent avec :
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `88. QF-083 — Competition Hazard` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LEARNED`
- Cross-source references: `REQ-FORMULA-0098`; supporting items: none found by conservative heading match; domain indexes `FORMULA, PARTICIPANTS, SURVIVAL, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-083; external revalidation: NO.

### SRC-004-ITEM-0244 — 89. QF-084 — Infrastructure Latency

- Source: `SRC-004`
- Location: lines 7660–7765; heading `89. QF-084 — Infrastructure Latency`
- Domain tags: FORMULA, INFRA, RISK, ACCOUNTING, ROUTING
- Source statement: 89. QF-084 — Infrastructure Latency: L_{compute} = L_{decode} + L_{book} + L_{route} + L_{simulation} + L_{risk} + L_{decision}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `89. QF-084 — Infrastructure Latency` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0099`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, RISK, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-084; external revalidation: NO.

### SRC-004-ITEM-0245 — 90. QF-085 — Opportunity Capture vs Infrastructure

- Source: `SRC-004`
- Location: lines 7766–7801; heading `90. QF-085 — Opportunity Capture vs Infrastructure`
- Domain tags: FORMULA, INFRA, PARTICIPANTS, SURVIVAL
- Source statement: 90. QF-085 — Opportunity Capture vs Infrastructure: P_{capture,s} = E_{L_s} [ S(L_s) ]
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `90. QF-085 — Opportunity Capture vs Infrastructure` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0100`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, PARTICIPANTS, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-085; external revalidation: NO.

### SRC-004-ITEM-0246 — 91. QF-086 — Infrastructure Gross PnL Difference

- Source: `SRC-004`
- Location: lines 7802–7855; heading `91. QF-086 — Infrastructure Gross PnL Difference`
- Domain tags: FORMULA, INFRA, ACCOUNTING, CAPITAL
- Source statement: 91. QF-086 — Infrastructure Gross PnL Difference: \Delta GrossPnL = GrossPnL_{candidate} - GrossPnL_{current}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `91. QF-086 — Infrastructure Gross PnL Difference` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0101`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, ACCOUNTING, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-086; external revalidation: NO.

### SRC-004-ITEM-0247 — 92. QF-087 — Incremental Infrastructure Cost

- Source: `SRC-004`
- Location: lines 7856–7890; heading `92. QF-087 — Incremental Infrastructure Cost`
- Domain tags: FORMULA, INFRA, ACCOUNTING
- Source statement: 92. QF-087 — Incremental Infrastructure Cost: \Delta Cost = Cost_{candidate} - Cost_{current}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `92. QF-087 — Incremental Infrastructure Cost` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0102`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-087; external revalidation: NO.

### SRC-004-ITEM-0248 — 93. QF-088 — Net Upgrade Value

- Source: `SRC-004`
- Location: lines 7891–7925; heading `93. QF-088 — Net Upgrade Value`
- Domain tags: FORMULA, ACCOUNTING
- Source statement: 93. QF-088 — Net Upgrade Value: NetUpgradeValue = \Delta GrossPnL - \Delta Cost
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `93. QF-088 — Net Upgrade Value` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0103`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-088; external revalidation: NO.

### SRC-004-ITEM-0249 — 94. QF-089 — Infrastructure ROI

- Source: `SRC-004`
- Location: lines 7926–7971; heading `94. QF-089 — Infrastructure ROI`
- Domain tags: FORMULA, INFRA, ACCOUNTING
- Source statement: 94. QF-089 — Infrastructure ROI: InfraROI = \frac{ \Delta GrossPnL }{ \Delta Cost }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `94. QF-089 — Infrastructure ROI` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0104`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-089; external revalidation: NO.

### SRC-004-ITEM-0250 — 95. QF-090 — Infrastructure Net PnL

- Source: `SRC-004`
- Location: lines 7972–8035; heading `95. QF-090 — Infrastructure Net PnL`
- Domain tags: FORMULA, INFRA, ACCOUNTING
- Source statement: 95. QF-090 — Infrastructure Net PnL: NetPnL_s = GrossTradingPnL_s - TradingCosts_s - InfrastructureCost_s
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `95. QF-090 — Infrastructure Net PnL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0105`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-090; external revalidation: NO.

### SRC-004-ITEM-0251 — 96. QF-091 — Infrastructure Upgrade Gate

- Source: `SRC-004`
- Location: lines 8036–8076; heading `96. QF-091 — Infrastructure Upgrade Gate`
- Domain tags: FORMULA, INFRA, ACCOUNTING
- Source statement: 96. QF-091 — Infrastructure Upgrade Gate: SF = safety factor
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `96. QF-091 — Infrastructure Upgrade Gate` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0106`; supporting items: SRC-008-ITEM-0161; domain indexes `FORMULA, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-091; external revalidation: NO.

### SRC-004-ITEM-0252 — 97. QF-092 — Infrastructure Efficiency

- Source: `SRC-004`
- Location: lines 8077–8123; heading `97. QF-092 — Infrastructure Efficiency`
- Domain tags: FORMULA, INFRA, ACCOUNTING
- Source statement: 97. QF-092 — Infrastructure Efficiency: InfraEfficiency = \frac{ NetPnL }{ InfraCost }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `97. QF-092 — Infrastructure Efficiency` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0107`; supporting items: SRC-008-ITEM-0168; domain indexes `FORMULA, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-092; external revalidation: NO.

### SRC-004-ITEM-0253 — 98. QF-093 — Capture Ratio

- Source: `SRC-004`
- Location: lines 8124–8227; heading `98. QF-093 — Capture Ratio`
- Domain tags: FORMULA, ACCOUNTING
- Source statement: 98. QF-093 — Capture Ratio: CaptureRatio = \frac{ \sum_i RealizedPnL_i }{ \sum_i ExpectedExecutablePnL_i }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `98. QF-093 — Capture Ratio` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0108`; supporting items: SRC-008-ITEM-0151; domain indexes `FORMULA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-093; external revalidation: NO.

### SRC-004-ITEM-0254 — 99. QF-094 — Opportunity Survival Rate Empirique

- Source: `SRC-004`
- Location: lines 8228–8274; heading `99. QF-094 — Opportunity Survival Rate Empirique`
- Domain tags: FORMULA, SURVIVAL
- Source statement: 99. QF-094 — Opportunity Survival Rate Empirique: ObservedSurvival(h) = \frac{ N_{alive}(h) }{ N_{eligible} }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `99. QF-094 — Opportunity Survival Rate Empirique` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0109`; supporting items: SRC-008-ITEM-0152; domain indexes `FORMULA, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-094; external revalidation: NO.

### SRC-004-ITEM-0255 — 100. QF-095 — Brier Score

- Source: `SRC-004`
- Location: lines 8275–8308; heading `100. QF-095 — Brier Score`
- Domain tags: FORMULA, ARCH
- Source statement: 100. QF-095 — Brier Score: Plus faible = meilleur.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `100. QF-095 — Brier Score` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0110`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-095; external revalidation: NO.

### SRC-004-ITEM-0256 — 101. QF-096 — Log Loss

- Source: `SRC-004`
- Location: lines 8309–8360; heading `101. QF-096 — Log Loss`
- Domain tags: FORMULA
- Source statement: 101. QF-096 — Log Loss: LL = -\frac1N \sum_i [ y_i\ln p_i + (1-y_i)\ln(1-p_i) ]
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `101. QF-096 — Log Loss` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0111`; supporting items: none found by conservative heading match; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-096; external revalidation: NO.

### SRC-004-ITEM-0257 — 102. QF-097 — Prediction Error PnL

- Source: `SRC-004`
- Location: lines 8361–8430; heading `102. QF-097 — Prediction Error PnL`
- Domain tags: FORMULA, ACCOUNTING
- Source statement: 102. QF-097 — Prediction Error PnL: PnLBias = E[PnLError]
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `102. QF-097 — Prediction Error PnL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0112`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-097; external revalidation: NO.

### SRC-004-ITEM-0258 — 103. QF-098 — Slippage Prediction Error

- Source: `SRC-004`
- Location: lines 8431–8486; heading `103. QF-098 — Slippage Prediction Error`
- Domain tags: FORMULA, ACCOUNTING
- Source statement: 103. QF-098 — Slippage Prediction Error: SlippageError = ActualSlippage - PredictedSlippage
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `103. QF-098 — Slippage Prediction Error` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0113`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-098; external revalidation: NO.

### SRC-004-ITEM-0259 — 104. QF-099 — Fill Calibration Error

- Source: `SRC-004`
- Location: lines 8487–8559; heading `104. QF-099 — Fill Calibration Error`
- Domain tags: FORMULA, EXECUTION, QUANT
- Source statement: 104. QF-099 — Fill Calibration Error: CalibrationError_B = ObservedFillRate_B - MeanPredictedFill_B
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `104. QF-099 — Fill Calibration Error` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0114`; supporting items: SRC-006-ITEM-0345; domain indexes `FORMULA, EXECUTION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-099; external revalidation: NO.

### SRC-004-ITEM-0260 — 105. QF-100 — Model Economic Lift

- Source: `SRC-004`
- Location: lines 8560–8611; heading `105. QF-100 — Model Economic Lift`
- Domain tags: FORMULA, ACCOUNTING, RISK, DATA, CAPITAL
- Source statement: 105. QF-100 — Model Economic Lift: EconomicLift = NetPnL_{model} - NetPnL_{baseline}
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `105. QF-100 — Model Economic Lift` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0115`; supporting items: SRC-007-ITEM-0094; domain indexes `FORMULA, ACCOUNTING, RISK, DATA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-100; external revalidation: NO.

### SRC-004-ITEM-0261 — 106. QF-101 — Quant Model Value After Latency Cost

- Source: `SRC-004`
- Location: lines 8612–8701; heading `106. QF-101 — Quant Model Value After Latency Cost`
- Domain tags: FORMULA, INFRA, ACCOUNTING, QUANT, OPERATIONS
- Source statement: 106. QF-101 — Quant Model Value After Latency Cost: ModelValue = PnL_{with} - PnL_{without} - PnLLostDueToAddedLatency - OperationalCost
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `106. QF-101 — Quant Model Value After Latency Cost` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0116`; supporting items: SRC-006-ITEM-0464, SRC-007-ITEM-0310; domain indexes `FORMULA, INFRA, ACCOUNTING, QUANT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-101; external revalidation: NO.

### SRC-004-ITEM-0262 — 107. QF-102 — Model Disagreement

- Source: `SRC-004`
- Location: lines 8702–8750; heading `107. QF-102 — Model Disagreement`
- Domain tags: FORMULA, QUANT
- Source statement: 107. QF-102 — Model Disagreement: Disagreement = \sqrt{ \frac1M \sum_m (p_m-\bar p)^2 }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `107. QF-102 — Model Disagreement` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0117`; supporting items: SRC-005-ITEM-0056, SRC-007-ITEM-0146, SRC-007-ITEM-0274; domain indexes `FORMULA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-102; external revalidation: NO.

### SRC-004-ITEM-0263 — 108. QF-103 — OOD Distance

- Source: `SRC-004`
- Location: lines 8751–8781; heading `108. QF-103 — OOD Distance`
- Domain tags: FORMULA, PRODUCT, ARCH
- Source statement: 108. QF-103 — OOD Distance: larger = further outside validated support
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `108. QF-103 — OOD Distance` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0118`; supporting items: none found by conservative heading match; domain indexes `FORMULA, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-103; external revalidation: NO.

### SRC-004-ITEM-0264 — 109. QF-104 — Simulation Confidence

- Source: `SRC-004`
- Location: lines 8782–8832; heading `109. QF-104 — Simulation Confidence`
- Domain tags: FORMULA, INFRA, SIMULATOR, PRODUCT, ARCH
- Source statement: 109. QF-104 — Simulation Confidence: PAS DE FAUX SCORE PONDÉRÉ FIGÉ Je déconseille une formule arbitraire du style :
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `109. QF-104 — Simulation Confidence` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0119`; supporting items: SRC-007-ITEM-0272, SRC-008-ITEM-0049; domain indexes `FORMULA, INFRA, SIMULATOR, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-104; external revalidation: NO.

### SRC-004-ITEM-0265 — 110. QF-105 — Expected Idle Capital Cost

- Source: `SRC-004`
- Location: lines 8833–8890; heading `110. QF-105 — Expected Idle Capital Cost`
- Domain tags: FORMULA, ACCOUNTING, CAPITAL, EXECUTION
- Source statement: 110. QF-105 — Expected Idle Capital Cost: IdleCost = C \times OpportunityRate \times T
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `110. QF-105 — Expected Idle Capital Cost` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-FORMULA-0120`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, CAPITAL, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: QF-105; external revalidation: NO.

### SRC-004-ITEM-0266 — 111. QF-106 — Economic PnL global

- Source: `SRC-004`
- Location: lines 8891–8984; heading `111. QF-106 — Economic PnL global`
- Domain tags: FORMULA, ACCOUNTING, INFRA, INVENTORY, BRIDGE, ROUTING
- Source statement: 111. QF-106 — Economic PnL global: EconomicPnL = ExecutionPnL + InventoryMTM + RebalancePnL + BridgePnL - InfrastructureCost
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `111. QF-106 — Economic PnL global` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0121`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, INFRA, INVENTORY, BRIDGE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-106; external revalidation: NO.

### SRC-004-ITEM-0267 — 112. QF-107 — Inventory Mark-to-Market

- Source: `SRC-004`
- Location: lines 8985–9048; heading `112. QF-107 — Inventory Mark-to-Market`
- Domain tags: FORMULA, INVENTORY, ACCOUNTING, MICROSTRUCTURE
- Source statement: 112. QF-107 — Inventory Mark-to-Market: \Delta MTM_a = MTM_{a,t} - MTM_{a,t-1} - ExternalFlow_a
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `112. QF-107 — Inventory Mark-to-Market` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0122`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INVENTORY, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-107; external revalidation: NO.

### SRC-004-ITEM-0268 — 113. QF-108 — Total Strategy PnL

- Source: `SRC-004`
- Location: lines 9049–9147; heading `113. QF-108 — Total Strategy PnL`
- Domain tags: FORMULA, ACCOUNTING, RECOVERY, INFRA, INVENTORY, ROUTING
- Source statement: 113. QF-108 — Total Strategy PnL: EconomicPnL = StrategyPnL - InfraCost
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `113. QF-108 — Total Strategy PnL` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0123`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, RECOVERY, INFRA, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-108; external revalidation: NO.

### SRC-004-ITEM-0269 — 114. QF-109 — Drawdown

- Source: `SRC-004`
- Location: lines 9148–9204; heading `114. QF-109 — Drawdown`
- Domain tags: FORMULA, RISK
- Source statement: 114. QF-109 — Drawdown: DD^{rel}_t = \frac{ Peak_t-E_t }{ Peak_t }
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `114. QF-109 — Drawdown` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0124`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-109; external revalidation: NO.

### SRC-004-ITEM-0270 — 115. QF-110 — Maximum Drawdown

- Source: `SRC-004`
- Location: lines 9205–9224; heading `115. QF-110 — Maximum Drawdown`
- Domain tags: FORMULA, RISK, CAPITAL
- Source statement: 115. QF-110 — Maximum Drawdown: MDD = \max_t DD_t
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `115. QF-110 — Maximum Drawdown` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0125`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: QF-110; external revalidation: NO.

### SRC-004-ITEM-0271 — 116. Les formules volontairement NON intégrées

- Source: `SRC-004`
- Location: lines 9225–9238; heading `116. Les formules volontairement NON intégrées`
- Domain tags: FORMULA, QUANT, PRODUCT, ARCH
- Source statement: 116. Les formules volontairement NON intégrées: Nous n’intégrons pas dans le Core V1 : car elles ne répondent pas à notre stratégie spot actuelle.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `116. Les formules volontairement NON intégrées` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0126`; supporting items: none found by conservative heading match; domain indexes `FORMULA, QUANT, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0272 — 117. Ce qui est mathématiquement figé

- Source: `SRC-004`
- Location: lines 9239–9284; heading `117. Ce qui est mathématiquement figé`
- Domain tags: FORMULA, RISK, INFRA, ACCOUNTING, SURVIVAL, LIQUIDITY_RESPONSE, MICROSTRUCTURE, INVENTORY
- Source statement: 117. Ce qui est mathématiquement figé: Les éléments suivants sont essentiellement codables immédiatement : prices / spread / mid
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `117. Ce qui est mathématiquement figé` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0127`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, INFRA, ACCOUNTING, SURVIVAL, LIQUIDITY_RESPONSE, MICROSTRUCTURE, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0273 — 118. Ce qui DOIT attendre les données

- Source: `SRC-004`
- Location: lines 9285–9322; heading `118. Ce qui DOIT attendre les données`
- Domain tags: FORMULA, EXECUTION, RISK, INFRA, ACCOUNTING, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET
- Source statement: 118. Ce qui DOIT attendre les données: Nous ne fixons pas artificiellement aujourd’hui : Ils font partie de la calibration expérimentale.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `118. Ce qui DOIT attendre les données` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0128`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, RISK, INFRA, ACCOUNTING, SURVIVAL, LIQUIDITY_RESPONSE, CROSS_MARKET`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0274 — 119. Principe important : paramètres ≠ architecture

- Source: `SRC-004`
- Location: lines 9323–9353; heading `119. Principe important : paramètres ≠ architecture`
- Domain tags: FORMULA, INFRA, ARCH, ACCOUNTING
- Source statement: 119. Principe important : paramètres ≠ architecture: n’est pas une décision architecturale. La décision architecturale est :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `119. Principe important : paramètres ≠ architecture` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0129`; supporting items: none found by conservative heading match; domain indexes `FORMULA, INFRA, ARCH, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0275 — 120. Formula Registry

- Source: `SRC-004`
- Location: lines 9354–9370; heading `120. Formula Registry`
- Domain tags: FORMULA, DEPLOYMENT, RISK, DATA, INFRA, ACCOUNTING, SURVIVAL, INVENTORY
- Source statement: 120. Formula Registry: Je recommande que toutes les constantes et modèles soient référencés dans un registre versionné. Chaque trade conserve ces versions.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `120. Formula Registry` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0130`; supporting items: none found by conservative heading match; domain indexes `FORMULA, DEPLOYMENT, RISK, DATA, INFRA, ACCOUNTING, SURVIVAL, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0276 — 121. Golden Formula Tests

- Source: `SRC-004`
- Location: lines 9371–9406; heading `121. Golden Formula Tests`
- Domain tags: FORMULA
- Source statement: 121. Golden Formula Tests: Chaque formule LOCKED doit disposer d’exemples déterministes.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `121. Golden Formula Tests` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0131`; supporting items: SRC-007-ITEM-0290; domain indexes `FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0277 — 122. Golden Book-Walk Test

- Source: `SRC-004`
- Location: lines 9407–9453; heading `122. Golden Book-Walk Test`
- Domain tags: FORMULA, ACCOUNTING
- Source statement: 122. Golden Book-Walk Test: Achat de 4 base : Cost = 2(100)+2(101) = 402
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `122. Golden Book-Walk Test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0132`; supporting items: SRC-006-ITEM-0306, SRC-006-ITEM-0468, SRC-007-ITEM-0164; domain indexes `FORMULA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0278 — 123. Precision Golden Tests

- Source: `SRC-004`
- Location: lines 9454–9465; heading `123. Precision Golden Tests`
- Domain tags: FORMULA, VALIDATION
- Source statement: 123. Precision Golden Tests: Tester les frontières Hyperliquid : directement contre les règles szDecimals.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `123. Precision Golden Tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0133`; supporting items: SRC-007-ITEM-0290; domain indexes `FORMULA, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0279 — 124. Python/Rust Parity

- Source: `SRC-004`
- Location: lines 9466–9512; heading `124. Python/Rust Parity`
- Domain tags: FORMULA, ARCH, QUANT
- Source statement: 124. Python/Rust Parity: La tolérance doit être définie selon : Pas une tolérance globale arbitraire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `124. Python/Rust Parity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0134`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ARCH, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0280 — 125. Calculs monétaires critiques

- Source: `SRC-004`
- Location: lines 9513–9537; heading `125. Calculs monétaires critiques`
- Domain tags: FORMULA, ACCOUNTING, INVENTORY
- Source statement: 125. Calculs monétaires critiques: plutôt qu’une accumulation libre en f64. Les modèles statistiques peuvent utiliser :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `125. Calculs monétaires critiques` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0135`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0281 — 126. Ordre exact des calculs d’une route

- Source: `SRC-004`
- Location: lines 9538–9587; heading `126. Ordre exact des calculs d’une route`
- Domain tags: FORMULA, ROUTING, RISK, ACCOUNTING, PARTICIPANTS, INVENTORY, SIZING, QUANT
- Source statement: 126. Ordre exact des calculs d’une route: Le pipeline mathématique standard doit être : 7. next leg L2 walk
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `126. Ordre exact des calculs d’une route` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0136`; supporting items: none found by conservative heading match; domain indexes `FORMULA, ROUTING, RISK, ACCOUNTING, PARTICIPANTS, INVENTORY, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0282 — 127. Formule conceptuelle finale du bot

- Source: `SRC-004`
- Location: lines 9588–9777; heading `127. Formule conceptuelle finale du bot`
- Domain tags: FORMULA, RISK, INFRA, ACCOUNTING, PARTICIPANTS, LIQUIDITY_RESPONSE, INVENTORY, ROUTING
- Source statement: 127. Formule conceptuelle finale du bot: (r^*,q^*,e^*) = \arg\max_{r,q,e} E[ PnL(r,q,e) | M, L, C, I ]
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `127. Formule conceptuelle finale du bot` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0137`; supporting items: SRC-007-ITEM-0313; domain indexes `FORMULA, RISK, INFRA, ACCOUNTING, PARTICIPANTS, LIQUIDITY_RESPONSE, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0283 — 128. Principe final du Formula Book

- Source: `SRC-004`
- Location: lines 9778–9808; heading `128. Principe final du Formula Book`
- Domain tags: FORMULA, RISK, ACCOUNTING, QUANT, PRODUCT
- Source statement: 128. Principe final du Formula Book: Aucune formule ne doit exister parce qu’elle est : Si une nouvelle formule n’améliore ni :
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `128. Principe final du Formula Book` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0138`; supporting items: none found by conservative heading match; domain indexes `FORMULA, RISK, ACCOUNTING, QUANT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-004-ITEM-0284 — 129. Résumé des objets mathématiques centraux

- Source: `SRC-004`
- Location: lines 9809–9953; heading `129. Résumé des objets mathématiques centraux`
- Domain tags: FORMULA, EXECUTION, ACCOUNTING, ROUTING, QUANT
- Source statement: 129. Résumé des objets mathématiques centraux: Le noyau du bot devient essentiellement : C’est ce noyau qui doit rester stable même si les modèles qui estiment certaines probabilités évoluent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Execution State Machine and Formula Book QF-001..QF-110.
- Candidate canonical interpretation: Preserve `129. Résumé des objets mathématiques centraux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-FORMULA-0139`; supporting items: none found by conservative heading match; domain indexes `FORMULA, EXECUTION, ACCOUNTING, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 279
- Requirements contributed: 279
- Supporting references contributed: 100 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 0
- Research items: 0
- Open items: 3
- External revalidation items: 0
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
