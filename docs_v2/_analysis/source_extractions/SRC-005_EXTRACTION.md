# SRC-005 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-005`
- Filename: `DOSSIER 36 — RISK CONSTITUTION V1.md`
- SHA-256: `798a0f60a14397926505b470aeee5ded11507c04c6bb489a4b1f5fe950ecd66f`
- Line count: 9877
- Authority profile: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Main domains: DATA, RISK, EXECUTION, ROUTING, ACCOUNTING, INVENTORY, RECOVERY, REPLAY, INFRA, ARCH, QUANT, CLOCK
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-005-ITEM-0003 — 1. Objectif

- Source: `SRC-005`
- Location: lines 3–90; heading `1. Objectif`
- Domain tags: RISK, ACCOUNTING
- Source statement: 1. Objectif: La Risk Constitution définit les règles fondamentales qui gouvernent toutes les décisions du bot. Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `1. Objectif` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0046`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0004 — 2. Principe constitutionnel principal

- Source: `SRC-005`
- Location: lines 91–145; heading `2. Principe constitutionnel principal`
- Domain tags: RISK, ACCOUNTING
- Source statement: 2. Principe constitutionnel principal: uniquement dans l’ensemble des actions autorisées : \max_a EV(a) \quad \text{sous} \quad a\in\mathcal A_{safe}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `2. Principe constitutionnel principal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0047`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0006 — HARD INVARIANT

- Source: `SRC-005`
- Location: lines 147–160; heading `HARD INVARIANT`
- Domain tags: RISK
- Source statement: HARD INVARIANT: Impossible à contourner. Exemple :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `HARD INVARIANT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0048`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0007 — CALIBRATED POLICY

- Source: `SRC-005`
- Location: lines 161–178; heading `CALIBRATED POLICY`
- Domain tags: RISK, VALIDATION, REPLAY, QUANT
- Source statement: CALIBRATED POLICY: Limite quantitative ajustable après replay/micro-live.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `CALIBRATED POLICY` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-RISK-0049`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, REPLAY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0008 — 4. Ordre de priorité du système

- Source: `SRC-005`
- Location: lines 179–198; heading `4. Ordre de priorité du système`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION, INVENTORY, ROUTING
- Source statement: 4. Ordre de priorité du système: 2. CANCEL UNSAFE RESTING ORDERS 5. COMPLETE SAFE EXISTING ROUTE
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `4. Ordre de priorité du système` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0050`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0009 — 5. Risk Layers

- Source: `SRC-005`
- Location: lines 199–221; heading `5. Risk Layers`
- Domain tags: RISK, EXECUTION, INVENTORY, CAPITAL, ROUTING
- Source statement: 5. Risk Layers: Une couche supérieure peut : Elle ne peut pas l’autoriser à violer ses propres limites.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `5. Risk Layers` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0051`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, INVENTORY, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0010 — 6. Principe : Global PnL ne relaxe jamais Leg Risk

- Source: `SRC-005`
- Location: lines 222–242; heading `6. Principe : Global PnL ne relaxe jamais Leg Risk`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE
- Source statement: 6. Principe : Global PnL ne relaxe jamais Leg Risk: → on peut accepter plus de slippage → on peut ignorer un book stale
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `6. Principe : Global PnL ne relaxe jamais Leg Risk` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0052`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0011 — 7. INV-001 — No Trade Without Valid Market State

- Source: `SRC-005`
- Location: lines 243–259; heading `7. INV-001 — No Trade Without Valid Market State`
- Domain tags: RISK, ACCOUNTING
- Source statement: 7. INV-001 — No Trade Without Valid Market State: Une nouvelle exécution nécessite :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `7. INV-001 — No Trade Without Valid Market State` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0053`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0012 — 8. INV-002 — No Trade On Stale Book

- Source: `SRC-005`
- Location: lines 260–328; heading `8. INV-002 — No Trade On Stale Book`
- Domain tags: RISK, DEPLOYMENT
- Source statement: 8. INV-002 — No Trade On Stale Book: Age_{book} = Now - LastValidUpdate La règle ne l’est pas.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `8. INV-002 — No Trade On Stale Book` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0054`; supporting items: none found by conservative heading match; domain indexes `RISK, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0013 — 9. INV-003 — Route Freshness = Worst Leg Freshness

- Source: `SRC-005`
- Location: lines 329–356; heading `9. INV-003 — Route Freshness = Worst Leg Freshness`
- Domain tags: RISK, ROUTING
- Source statement: 9. INV-003 — Route Freshness = Worst Leg Freshness: Age_r = \max_{j\in legs(r)} Age_j La route n’est jamais considérée plus fraîche que sa jambe la plus vieille.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `9. INV-003 — Route Freshness = Worst Leg Freshness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0055`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0014 — 10. INV-004 — No Unknown Metadata

- Source: `SRC-005`
- Location: lines 357–368; heading `10. INV-004 — No Unknown Metadata`
- Domain tags: RISK, RECOVERY, ACCOUNTING, ROUTING
- Source statement: 10. INV-004 — No Unknown Metadata: Aucune route si nous ne connaissons pas exactement : Pas de valeur par défaut silencieuse.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `10. INV-004 — No Unknown Metadata` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0056`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0015 — 11. INV-005 — Fees Must Be Known

- Source: `SRC-005`
- Location: lines 369–380; heading `11. INV-005 — Fees Must Be Known`
- Domain tags: RISK, ACCOUNTING, RECOVERY
- Source statement: 11. INV-005 — Fees Must Be Known: Si le Fee Engine ne peut pas déterminer les frais applicables :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `11. INV-005 — Fees Must Be Known` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0057`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0016 — 12. INV-006 — Exchange Precision Is Mandatory

- Source: `SRC-005`
- Location: lines 381–396; heading `12. INV-006 — Exchange Precision Is Mandatory`
- Domain tags: RISK, SIZING, QUANT
- Source statement: 12. INV-006 — Exchange Precision Is Mandatory: Toute taille et tout prix doivent passer : Aucune stratégie ne peut envoyer directement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `12. INV-006 — Exchange Precision Is Mandatory` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0058`; supporting items: none found by conservative heading match; domain indexes `RISK, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0017 — 13. INV-007 — No Negative Available Balance

- Source: `SRC-005`
- Location: lines 397–472; heading `13. INV-007 — No Negative Available Balance`
- Domain tags: RISK, INVENTORY
- Source statement: 13. INV-007 — No Negative Available Balance: AvailableBalance = ActualBalance - ReservedBalance
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `13. INV-007 — No Negative Available Balance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0059`; supporting items: SRC-004-ITEM-0233; domain indexes `RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0018 — 14. INV-008 — Unknown Capital Is Reserved Capital

- Source: `SRC-005`
- Location: lines 473–485; heading `14. INV-008 — Unknown Capital Is Reserved Capital`
- Domain tags: RISK, RECOVERY, CAPITAL, RECONCILIATION
- Source statement: 14. INV-008 — Unknown Capital Is Reserved Capital: Si un ordre est : tout capital potentiellement consommé reste :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `14. INV-008 — Unknown Capital Is Reserved Capital` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0060`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, CAPITAL, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0019 — 15. INV-009 — No Double Spending

- Source: `SRC-005`
- Location: lines 486–498; heading `15. INV-009 — No Double Spending`
- Domain tags: RISK, ROUTING
- Source statement: 15. INV-009 — No Double Spending: Deux routes ne peuvent jamais utiliser simultanément : au-delà de leur capacité réelle.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `15. INV-009 — No Double Spending` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0061`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0020 — 16. INV-010 — Reservations Before Orders

- Source: `SRC-005`
- Location: lines 499–516; heading `16. INV-010 — Reservations Before Orders`
- Domain tags: RISK, EXECUTION
- Source statement: 16. INV-010 — Reservations Before Orders: Ordre : VALIDATE
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `16. INV-010 — Reservations Before Orders` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0062`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0021 — 17. INV-011 — Shared Depth Cannot Be Double Counted

- Source: `SRC-005`
- Location: lines 517–565; heading `17. INV-011 — Shared Depth Cannot Be Double Counted`
- Domain tags: RISK, ROUTING
- Source statement: 17. INV-011 — Shared Depth Cannot Be Double Counted: Sinon les nouvelles routes utilisant ce carnet sont rejetées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `17. INV-011 — Shared Depth Cannot Be Double Counted` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0063`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0022 — 18. INV-012 — Actual Fill Beats Expected Fill

- Source: `SRC-005`
- Location: lines 566–592; heading `18. INV-012 — Actual Fill Beats Expected Fill`
- Domain tags: RISK, EXECUTION
- Source statement: 18. INV-012 — Actual Fill Beats Expected Fill: La simulation ne peut jamais écraser l’état réel.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `18. INV-012 — Actual Fill Beats Expected Fill` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0064`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0023 — 19. INV-013 — Next Leg Uses Actual Previous Fill

- Source: `SRC-005`
- Location: lines 593–656; heading `19. INV-013 — Next Leg Uses Actual Previous Fill`
- Domain tags: RISK, EXECUTION, ACCOUNTING
- Source statement: 19. INV-013 — Next Leg Uses Actual Previous Fill: Pour Leg n+1
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `19. INV-013 — Next Leg Uses Actual Previous Fill` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0065`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0024 — 20. INV-014 — No Blind Retry

- Source: `SRC-005`
- Location: lines 657–673; heading `20. INV-014 — No Blind Retry`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION
- Source statement: 20. INV-014 — No Blind Retry: avant toute nouvelle intention économique équivalente.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `20. INV-014 — No Blind Retry` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0066`; supporting items: SRC-004-ITEM-0024, SRC-006-ITEM-0392; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0025 — 21. INV-015 — Cancel Sent ≠ Canceled

- Source: `SRC-005`
- Location: lines 674–683; heading `21. INV-015 — Cancel Sent ≠ Canceled`
- Domain tags: RISK, EXECUTION, INVENTORY
- Source statement: 21. INV-015 — Cancel Sent ≠ Canceled: Une cancellation ne libère jamais immédiatement : Elle attend l’état exchange terminal.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `21. INV-015 — Cancel Sent ≠ Canceled` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0067`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0026 — 22. INV-016 — Partial Fill Creates Real Exposure

- Source: `SRC-005`
- Location: lines 684–707; heading `22. INV-016 — Partial Fill Creates Real Exposure`
- Domain tags: RISK, EXECUTION, INVENTORY, ROUTING, ARCH
- Source statement: 22. INV-016 — Partial Fill Creates Real Exposure: l’Inventory Engine est mis à jour.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `22. INV-016 — Partial Fill Creates Real Exposure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0068`; supporting items: SRC-004-ITEM-0052, SRC-004-ITEM-0055; domain indexes `RISK, EXECUTION, INVENTORY, ROUTING, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0027 — 23. INV-017 — Existing Exposure Has Priority

- Source: `SRC-005`
- Location: lines 708–717; heading `23. INV-017 — Existing Exposure Has Priority`
- Domain tags: RISK, EXECUTION, RECOVERY, CAPITAL
- Source statement: 23. INV-017 — Existing Exposure Has Priority: Une nouvelle opportunité ne peut pas utiliser du capital ou du risque nécessaire à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `23. INV-017 — Existing Exposure Has Priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0069`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0028 — 24. INV-018 — Recovery May Be Negative EV

- Source: `SRC-005`
- Location: lines 718–756; heading `24. INV-018 — Recovery May Be Negative EV`
- Domain tags: RISK, RECOVERY, PORTFOLIO
- Source statement: 24. INV-018 — Recovery May Be Negative EV: Une recovery peut accepter : parce que l’exposition existe déjà.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `24. INV-018 — Recovery May Be Negative EV` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0070`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, PORTFOLIO`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0029 — 25. INV-019 — Recovery Is Not Unlimited

- Source: `SRC-005`
- Location: lines 757–768; heading `25. INV-019 — Recovery Is Not Unlimited`
- Domain tags: RISK, RECOVERY
- Source statement: 25. INV-019 — Recovery Is Not Unlimited: Une perte existante ne crée jamais une autorisation illimitée.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `25. INV-019 — Recovery Is Not Unlimited` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0071`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0030 — 26. INV-020 — Sunk Costs Are Sunk

- Source: `SRC-005`
- Location: lines 769–799; heading `26. INV-020 — Sunk Costs Are Sunk`
- Domain tags: RISK, ACCOUNTING, FUTURE
- Source statement: 26. INV-020 — Sunk Costs Are Sunk: Si une première jambe a perdu : la décision suivante optimise :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `26. INV-020 — Sunk Costs Are Sunk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0072`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0031 — 27. INV-021 — No Averaging Down By Default

- Source: `SRC-005`
- Location: lines 800–808; heading `27. INV-021 — No Averaging Down By Default`
- Domain tags: RISK, QUANT
- Source statement: 27. INV-021 — No Averaging Down By Default: Le bot ne peut pas augmenter une exposition déficitaire uniquement parce que son prix a baissé. Toute nouvelle quantité doit constituer :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `27. INV-021 — No Averaging Down By Default` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0073`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0032 — 28. INV-022 — No Martingale

- Source: `SRC-005`
- Location: lines 809–836; heading `28. INV-022 — No Martingale`
- Domain tags: RISK
- Source statement: 28. INV-022 — No Martingale: q_{next} = q_{previous} \times f(loss) si l’augmentation est motivée uniquement par la perte précédente.
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `28. INV-022 — No Martingale` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0074`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0033 — 29. INV-023 — No New Risk In RECOVERY_ONLY

- Source: `SRC-005`
- Location: lines 837–857; heading `29. INV-023 — No New Risk In RECOVERY_ONLY`
- Domain tags: RISK, RECOVERY, EXECUTION, RECONCILIATION, INVENTORY
- Source statement: 29. INV-023 — No New Risk In RECOVERY_ONLY: État : RECOVERY_ONLY
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `29. INV-023 — No New Risk In RECOVERY_ONLY` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0075`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, EXECUTION, RECONCILIATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0034 — 30. INV-024 — No New Risk In HALTED

- Source: `SRC-005`
- Location: lines 858–869; heading `30. INV-024 — No New Risk In HALTED`
- Domain tags: RISK, RECONCILIATION
- Source statement: 30. INV-024 — No New Risk In HALTED: Le retour passe obligatoirement par :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `30. INV-024 — No New Risk In HALTED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0076`; supporting items: none found by conservative heading match; domain indexes `RISK, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0035 — 31. INV-025 — No Trading While Account State Is Unreconciled

- Source: `SRC-005`
- Location: lines 870–883; heading `31. INV-025 — No Trading While Account State Is Unreconciled`
- Domain tags: RISK, RECONCILIATION, INVENTORY
- Source statement: 31. INV-025 — No Trading While Account State Is Unreconciled: Si : local balance
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `31. INV-025 — No Trading While Account State Is Unreconciled` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0077`; supporting items: none found by conservative heading match; domain indexes `RISK, RECONCILIATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0036 — 32. INV-026 — Clock Must Be Healthy

- Source: `SRC-005`
- Location: lines 884–922; heading `32. INV-026 — Clock Must Be Healthy`
- Domain tags: RISK, CLOCK, OPERATIONS, RECOVERY, INFRA, BENCHMARK, ACCOUNTING, SURVIVAL
- Source statement: 32. INV-026 — Clock Must Be Healthy: Si l’incertitude de l’horloge dépasse : les modèles dépendant de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `32. INV-026 — Clock Must Be Healthy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0078`; supporting items: none found by conservative heading match; domain indexes `RISK, CLOCK, OPERATIONS, RECOVERY, INFRA, BENCHMARK, ACCOUNTING, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0037 — 33. INV-027 — Required Feeds Must Be Healthy

- Source: `SRC-005`
- Location: lines 923–937; heading `33. INV-027 — Required Feeds Must Be Healthy`
- Domain tags: RISK, OPERATIONS, ACCOUNTING, EXECUTION, RECOVERY, RECONCILIATION, DEPLOYMENT
- Source statement: 33. INV-027 — Required Feeds Must Be Healthy: Les feeds critiques incluent : Une panne d’un feed critique :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `33. INV-027 — Required Feeds Must Be Healthy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0079`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS, ACCOUNTING, EXECUTION, RECOVERY, RECONCILIATION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0038 — 34. INV-028 — Trading Requires InfraHealth == ACCEPTABLE

- Source: `SRC-005`
- Location: lines 938–951; heading `34. INV-028 — Trading Requires InfraHealth == ACCEPTABLE`
- Domain tags: RISK, INFRA, OPERATIONS
- Source statement: 34. INV-028 — Trading Requires InfraHealth == ACCEPTABLE: Infrastructure state : HEALTHY
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `34. INV-028 — Trading Requires InfraHealth == ACCEPTABLE` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0080`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0039 — 35. Infra Health Inputs

- Source: `SRC-005`
- Location: lines 952–966; heading `35. Infra Health Inputs`
- Domain tags: RISK, INFRA, OPERATIONS, EXECUTION, RECORDER, CLOCK, BENCHMARK, ACCOUNTING
- Source statement: 35. Infra Health Inputs: Au minimum : feed age
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `35. Infra Health Inputs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0081`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, OPERATIONS, EXECUTION, RECORDER, CLOCK, BENCHMARK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0040 — 36. INV-029 — Slow Compute Can Become a Risk Event

- Source: `SRC-005`
- Location: lines 967–1013; heading `36. INV-029 — Slow Compute Can Become a Risk Event`
- Domain tags: RISK, RECOVERY, INFRA, BENCHMARK, ROUTING
- Source statement: 36. INV-029 — Slow Compute Can Become a Risk Event: de façon persistante ou extrême : Performance et sécurité ne sont donc pas totalement séparées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `36. INV-029 — Slow Compute Can Become a Risk Event` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0082`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, INFRA, BENCHMARK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0041 — 37. INV-030 — Recorder Must Never Block Execution

- Source: `SRC-005`
- Location: lines 1014–1032; heading `37. INV-030 — Recorder Must Never Block Execution`
- Domain tags: RISK, EXECUTION, RECORDER, SIMULATOR, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 37. INV-030 — Recorder Must Never Block Execution: avant de bloquer le hot path. Les événements d’exécution critiques gardent une priorité supérieure.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `37. INV-030 — Recorder Must Never Block Execution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0083`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECORDER, SIMULATOR, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0042 — 38. Market Risk Gates

- Source: `SRC-005`
- Location: lines 1033–1044; heading `38. Market Risk Gates`
- Domain tags: RISK, ROUTING, QUANT
- Source statement: 38. Market Risk Gates: Chaque nouvelle route passe au minimum :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `38. Market Risk Gates` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0084`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0043 — 39. Spread Gate

- Source: `SRC-005`
- Location: lines 1045–1088; heading `39. Spread Gate`
- Domain tags: RISK
- Source statement: 39. Spread Gate: Un spread trop large peut signaler :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `39. Spread Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0085`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0044 — 40. Liquidity Gate

- Source: `SRC-005`
- Location: lines 1089–1120; heading `40. Liquidity Gate`
- Domain tags: RISK, CAPITAL
- Source statement: 40. Liquidity Gate: Pour taille Q_{validated}(r) \geq q
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `40. Liquidity Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0086`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0045 — 41. Impact Gate

- Source: `SRC-005`
- Location: lines 1121–1182; heading `41. Impact Gate`
- Domain tags: RISK, QUANT
- Source statement: 41. Impact Gate: DepthParticipation(q) \leq DP_{max} et/ou :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `41. Impact Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0087`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0046 — 42. Volume Participation Gate

- Source: `SRC-005`
- Location: lines 1183–1202; heading `42. Volume Participation Gate`
- Domain tags: RISK
- Source statement: 42. Volume Participation Gate: si le modèle sait traiter cette zone.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `42. Volume Participation Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0088`; supporting items: SRC-004-ITEM-0200, SRC-007-ITEM-0214; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0047 — 43. Jump Gate

- Source: `SRC-005`
- Location: lines 1203–1255; heading `43. Jump Gate`
- Domain tags: RISK, EXECUTION, ARCH
- Source statement: 43. Jump Gate: Si : JumpScore>J_{hard}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `43. Jump Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0089`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0048 — 44. Volatility Gate

- Source: `SRC-005`
- Location: lines 1256–1272; heading `44. Volatility Gate`
- Domain tags: RISK, QUANT, RECOVERY, ROUTING
- Source statement: 44. Volatility Gate: La volatilité n’est pas seulement une pénalité. Au-dessus d’un seuil extrême :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `44. Volatility Gate` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-RISK-0090`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT, RECOVERY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0049 — 45. Competition / Survival Gates

- Source: `SRC-005`
- Location: lines 1273–1328; heading `45. Competition / Survival Gates`
- Domain tags: RISK, PARTICIPANTS, SURVIVAL, ROUTING
- Source statement: 45. Competition / Survival Gates: P_{exec} = P( Edge_{arrival}>E_{minimum} )
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `45. Competition / Survival Gates` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0091`; supporting items: none found by conservative heading match; domain indexes `RISK, PARTICIPANTS, SURVIVAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0050 — 46. Survival Gate

- Source: `SRC-005`
- Location: lines 1329–1354; heading `46. Survival Gate`
- Domain tags: RISK, SURVIVAL, INFRA
- Source statement: 46. Survival Gate: Condition possible : P_{capture} \geq P_{capture,min}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `46. Survival Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0092`; supporting items: none found by conservative heading match; domain indexes `RISK, SURVIVAL, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0051 — 47. Expected Arrival Edge Gate

- Source: `SRC-005`
- Location: lines 1355–1395; heading `47. Expected Arrival Edge Gate`
- Domain tags: RISK, ACCOUNTING, QUANT
- Source statement: 47. Expected Arrival Edge Gate: Mais cette condition seule n’est pas suffisante.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `47. Expected Arrival Edge Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0093`; supporting items: SRC-004-ITEM-0209, SRC-007-ITEM-0064, SRC-007-ITEM-0194; domain indexes `RISK, ACCOUNTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0052 — 48. Model Confidence Gate

- Source: `SRC-005`
- Location: lines 1396–1416; heading `48. Model Confidence Gate`
- Domain tags: RISK
- Source statement: 48. Model Confidence Gate: reject or severe size reduction
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `48. Model Confidence Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0094`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0053 — 49. OOD Gate

- Source: `SRC-005`
- Location: lines 1417–1432; heading `49. OOD Gate`
- Domain tags: RISK, QUANT
- Source statement: 49. OOD Gate: est hors domaine validé : Le bot ne peut pas utiliser aveuglément la prédiction.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `49. OOD Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0095`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0054 — 50. Hard OOD

- Source: `SRC-005`
- Location: lines 1433–1439; heading `50. Hard OOD`
- Domain tags: RISK
- Source statement: 50. Hard OOD: Si l’extrapolation dépasse la zone autorisée :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `50. Hard OOD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0096`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0055 — 51. Soft OOD

- Source: `SRC-005`
- Location: lines 1440–1453; heading `51. Soft OOD`
- Domain tags: RISK, VALIDATION
- Source statement: 51. Soft OOD: Zone limite : reduce size
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `51. Soft OOD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0097`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0056 — 52. Model Disagreement Gate

- Source: `SRC-005`
- Location: lines 1454–1484; heading `52. Model Disagreement Gate`
- Domain tags: RISK, EXECUTION
- Source statement: 52. Model Disagreement Gate: Si les modèles principaux donnent des résultats fortement contradictoires :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `52. Model Disagreement Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0098`; supporting items: SRC-004-ITEM-0262, SRC-007-ITEM-0146, SRC-007-ITEM-0274; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0057 — 53. Simulation Gate

- Source: `SRC-005`
- Location: lines 1485–1497; heading `53. Simulation Gate`
- Domain tags: RISK, CAPITAL, ROUTING
- Source statement: 53. Simulation Gate: Une route doit disposer de : avant réel capital, sauf mode explicite :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `53. Simulation Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0099`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0058 — 54. Positive PnL Probability Gate

- Source: `SRC-005`
- Location: lines 1498–1514; heading `54. Positive PnL Probability Gate`
- Domain tags: RISK, ACCOUNTING, QUANT, INFRA
- Source statement: 54. Positive PnL Probability Gate: Paramètre calibré par stratégie/execution mode.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `54. Positive PnL Probability Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0100`; supporting items: SRC-004-ITEM-0219; domain indexes `RISK, ACCOUNTING, QUANT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0059 — 55. Expected PnL Gate

- Source: `SRC-005`
- Location: lines 1515–1541; heading `55. Expected PnL Gate`
- Domain tags: RISK, ACCOUNTING
- Source statement: 55. Expected PnL Gate: Les deux peuvent être nécessaires.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `55. Expected PnL Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0101`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0060 — 56. Tail Risk Gate

- Source: `SRC-005`
- Location: lines 1542–1561; heading `56. Tail Risk Gate`
- Domain tags: RISK
- Source statement: 56. Tail Risk Gate: Aucune EV positive ne peut contourner ce hard limit.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `56. Tail Risk Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0102`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0061 — 57. Max Single-Route Loss

- Source: `SRC-005`
- Location: lines 1562–1624; heading `57. Max Single-Route Loss`
- Domain tags: RISK, ROUTING
- Source statement: 57. Max Single-Route Loss: Chaque route possède : WorstValidatedLoss(q)
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `57. Max Single-Route Loss` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0103`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0062 — 58. Recovery Tail Risk

- Source: `SRC-005`
- Location: lines 1625–1667; heading `58. Recovery Tail Risk`
- Domain tags: RISK, RECOVERY
- Source statement: 58. Recovery Tail Risk: Même la recovery doit vérifier :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `58. Recovery Tail Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0104`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0063 — 59. Position Sizing Risk Gate

- Source: `SRC-005`
- Location: lines 1668–1723; heading `59. Position Sizing Risk Gate`
- Domain tags: RISK, SIZING, INVENTORY, QUANT
- Source statement: 59. Position Sizing Risk Gate: q^* \leq \min( Q_{validated}, Q_{balance}, Q_{inventory}, Q_{impact}, Q_{risk} ) Puis optimisation EV à l’intérieur de cette région.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `59. Position Sizing Risk Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0105`; supporting items: SRC-006-ITEM-0358; domain indexes `RISK, SIZING, INVENTORY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0064 — 60. No Fixed Universal Trade Size

- Source: `SRC-005`
- Location: lines 1724–1736; heading `60. No Fixed Universal Trade Size`
- Domain tags: RISK, VALIDATION
- Source statement: 60. No Fixed Universal Trade Size: La taille normale est dynamique.
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `60. No Fixed Universal Trade Size` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0106`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0065 — 61. Probe Mode

- Source: `SRC-005`
- Location: lines 1737–1756; heading `61. Probe Mode`
- Domain tags: RISK, ACCOUNTING
- Source statement: 61. Probe Mode: Mode spécial : MICRO_LIVE_PROBE
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `61. Probe Mode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0107`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0066 — 62. Inventory Constitution

- Source: `SRC-005`
- Location: lines 1757–1807; heading `62. Inventory Constitution`
- Domain tags: RISK, INVENTORY
- Source statement: 62. Inventory Constitution: Chaque actif tradable possède : HardMin \leq SoftMin \leq Target \leq SoftMax \leq HardMax
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `62. Inventory Constitution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0108`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0067 — 63. Soft Inventory Region

- Source: `SRC-005`
- Location: lines 1808–1823; heading `63. Soft Inventory Region`
- Domain tags: RISK, INVENTORY
- Source statement: 63. Soft Inventory Region: aucun hard reject uniquement dû au niveau d’inventaire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `63. Soft Inventory Region` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0109`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0068 — 64. Outside Soft Band

- Source: `SRC-005`
- Location: lines 1824–1861; heading `64. Outside Soft Band`
- Domain tags: RISK, ROUTING
- Source statement: 64. Outside Soft Band: Si : I_a<SoftMin
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `64. Outside Soft Band` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0110`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0069 — 65. Hard Inventory Region

- Source: `SRC-005`
- Location: lines 1862–1910; heading `65. Hard Inventory Region`
- Domain tags: RISK, INVENTORY, EXECUTION, FUTURE
- Source statement: 65. Hard Inventory Region: sauf action explicitement classée : qui améliore la violation existante.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `65. Hard Inventory Region` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0111`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, EXECUTION, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0070 — 66. Risk-Reducing Exception

- Source: `SRC-005`
- Location: lines 1911–1928; heading `66. Risk-Reducing Exception`
- Domain tags: RISK, INVENTORY
- Source statement: 66. Risk-Reducing Exception: Une action peut franchir certaines limites normales uniquement si elle réduit strictement une exposition déjà hors limite.
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `66. Risk-Reducing Exception` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0112`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0071 — 67. Net Flow Gate

- Source: `SRC-005`
- Location: lines 1929–1953; heading `67. Net Flow Gate`
- Domain tags: RISK, PRODUCT
- Source statement: 67. Net Flow Gate: est surveillé sur plusieurs horizons. Si accumulation directionnelle anormale :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `67. Net Flow Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0113`; supporting items: none found by conservative heading match; domain indexes `RISK, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0072 — 68. Inventory Concentration

- Source: `SRC-005`
- Location: lines 1954–2027; heading `68. Inventory Concentration`
- Domain tags: RISK, INVENTORY, PORTFOLIO, ARCH
- Source statement: 68. Inventory Concentration: Concentration_a = \frac{ Value_a }{ PortfolioValue } hors core assets explicitement autorisés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `68. Inventory Concentration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0114`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, PORTFOLIO, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0073 — 69. Transit Asset Risk

- Source: `SRC-005`
- Location: lines 2028–2077; heading `69. Transit Asset Risk`
- Domain tags: RISK, RECOVERY, INVENTORY
- Source statement: 69. Transit Asset Risk: Une exposition TRANSIT dépassant :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `69. Transit Asset Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0115`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0074 — 70. Stranded Asset Gate

- Source: `SRC-005`
- Location: lines 2078–2090; heading `70. Stranded Asset Gate`
- Domain tags: RISK, INVENTORY, ACCOUNTING, ROUTING
- Source statement: 70. Stranded Asset Gate: Une route finissant dans un actif dont : dépasse les limites peut être rejetée même avec conversion alpha positif.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `70. Stranded Asset Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0116`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0075 — 71. Terminal Viability Gate

- Source: `SRC-005`
- Location: lines 2091–2111; heading `71. Terminal Viability Gate`
- Domain tags: RISK, BRIDGE, MARKET_ATLAS, INVENTORY, OWA, QUANT, FUTURE
- Source statement: 71. Terminal Viability Gate: Pour OWA : A → X → B
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `71. Terminal Viability Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0117`; supporting items: SRC-003-ITEM-0139, SRC-006-ITEM-0372; domain indexes `RISK, BRIDGE, MARKET_ATLAS, INVENTORY, OWA, QUANT, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0076 — 72. Bridge Risk

- Source: `SRC-005`
- Location: lines 2112–2141; heading `72. Bridge Risk`
- Domain tags: RISK, BRIDGE, CAPITAL
- Source statement: 72. Bridge Risk: Un mouvement de capital doit respecter :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `72. Bridge Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0118`; supporting items: none found by conservative heading match; domain indexes `RISK, BRIDGE, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0077 — 73. Bridge Cannot Hide Arbitrage Loss

- Source: `SRC-005`
- Location: lines 2142–2155; heading `73. Bridge Cannot Hide Arbitrage Loss`
- Domain tags: RISK, BRIDGE, ACCOUNTING, MICROSTRUCTURE, INVENTORY, ROUTING
- Source statement: 73. Bridge Cannot Hide Arbitrage Loss: Une route perdante ne peut pas être reclassée artificiellement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `73. Bridge Cannot Hide Arbitrage Loss` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0119`; supporting items: none found by conservative heading match; domain indexes `RISK, BRIDGE, ACCOUNTING, MICROSTRUCTURE, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0078 — 74. Relocation Hysteresis

- Source: `SRC-005`
- Location: lines 2156–2171; heading `74. Relocation Hysteresis`
- Domain tags: RISK, BRIDGE
- Source statement: 74. Relocation Hysteresis: Pour éviter : BTC → ETH
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `74. Relocation Hysteresis` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0120`; supporting items: none found by conservative heading match; domain indexes `RISK, BRIDGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0079 — 75. Maker Risk Constitution

- Source: `SRC-005`
- Location: lines 2172–2182; heading `75. Maker Risk Constitution`
- Domain tags: RISK, EXECUTION, MICROSTRUCTURE, MAKER_MODEL
- Source statement: 75. Maker Risk Constitution: Un ordre maker introduit : Il possède donc des gates supplémentaires.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `75. Maker Risk Constitution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0121`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, MICROSTRUCTURE, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0080 — 76. Maker Must Be ALO

- Source: `SRC-005`
- Location: lines 2183–2199; heading `76. Maker Must Be ALO`
- Domain tags: RISK, EXECUTION
- Source statement: 76. Maker Must Be ALO: Pour un plan classé : l’ordre doit utiliser un mécanisme garantissant :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `76. Maker Must Be ALO` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0122`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0081 — 77. Maker Maximum Exposure

- Source: `SRC-005`
- Location: lines 2200–2243; heading `77. Maker Maximum Exposure`
- Domain tags: RISK, EXECUTION, RECOVERY, MAKER_MODEL, ARCH
- Source statement: 77. Maker Maximum Exposure: Somme des maker fills non encore hedgés :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `77. Maker Maximum Exposure` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0123`; supporting items: SRC-004-ITEM-0093; domain indexes `RISK, EXECUTION, RECOVERY, MAKER_MODEL, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0082 — 78. Maker Maximum Age

- Source: `SRC-005`
- Location: lines 2244–2289; heading `78. Maker Maximum Age`
- Domain tags: RISK, EXECUTION
- Source statement: 78. Maker Maximum Age: Tout maker possède : Age_{maker}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `78. Maker Maximum Age` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0124`; supporting items: SRC-004-ITEM-0093; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0083 — 79. Maker Edge Death

- Source: `SRC-005`
- Location: lines 2290–2326; heading `79. Maker Edge Death`
- Domain tags: RISK, EXECUTION
- Source statement: 79. Maker Edge Death: le maker doit être annulé. Pas attendre uniquement un timeout.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `79. Maker Edge Death` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0125`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0084 — 80. Maker Toxicity Gate

- Source: `SRC-005`
- Location: lines 2327–2341; heading `80. Maker Toxicity Gate`
- Domain tags: RISK, EXECUTION, CROSS_MARKET, MICROSTRUCTURE, MAKER_MODEL, QUANT
- Source statement: 80. Maker Toxicity Gate: indiquent une adverse selection trop importante : cancel / do not place
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `80. Maker Toxicity Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0126`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, CROSS_MARKET, MICROSTRUCTURE, MAKER_MODEL, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0085 — 81. Maker Fill Must Trigger Immediate Reassessment

- Source: `SRC-005`
- Location: lines 2342–2357; heading `81. Maker Fill Must Trigger Immediate Reassessment`
- Domain tags: RISK, EXECUTION, MAKER_MODEL, RECOVERY, DEPLOYMENT, INVENTORY
- Source statement: 81. Maker Fill Must Trigger Immediate Reassessment: leg continuation / hedge evaluation
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `81. Maker Fill Must Trigger Immediate Reassessment` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0127`; supporting items: SRC-004-ITEM-0212; domain indexes `RISK, EXECUTION, MAKER_MODEL, RECOVERY, DEPLOYMENT, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0086 — 82. Taker Risk Constitution

- Source: `SRC-005`
- Location: lines 2358–2378; heading `82. Taker Risk Constitution`
- Domain tags: RISK, EXECUTION
- Source statement: 82. Taker Risk Constitution: Toute exécution taker utilise : protected IOC / marketable limit
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `82. Taker Risk Constitution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0128`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0087 — 83. Maximum Taker Slippage

- Source: `SRC-005`
- Location: lines 2379–2414; heading `83. Maximum Taker Slippage`
- Domain tags: RISK, EXECUTION
- Source statement: 83. Maximum Taker Slippage: protégé autant que possible par :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `83. Maximum Taker Slippage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0129`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0088 — 84. Multi-Leg Risk

- Source: `SRC-005`
- Location: lines 2415–2427; heading `84. Multi-Leg Risk`
- Domain tags: RISK, VALIDATION, ROUTING, FUTURE
- Source statement: 84. Multi-Leg Risk: La validation initiale n’autorise pas automatiquement toutes les jambes futures.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `84. Multi-Leg Risk` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0130`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, ROUTING, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0089 — 85. Continuation Gate

- Source: `SRC-005`
- Location: lines 2428–2457; heading `85. Continuation Gate`
- Domain tags: RISK, RECOVERY
- Source statement: 85. Continuation Gate: Le meilleur choix sous contraintes gagne.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `85. Continuation Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0131`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0090 — 86. No Route Loyalty

- Source: `SRC-005`
- Location: lines 2458–2484; heading `86. No Route Loyalty`
- Domain tags: RISK, ROUTING, EXECUTION, RECOVERY
- Source statement: 86. No Route Loyalty: Une route originale n’a aucun privilège après un fill.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `86. No Route Loyalty` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0132`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING, EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0091 — 87. Dust Risk

- Source: `SRC-005`
- Location: lines 2485–2512; heading `87. Dust Risk`
- Domain tags: RISK, RECOVERY, INVENTORY
- Source statement: 87. Dust Risk: Chaque actif possède : DustTolerance_a
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `87. Dust Risk` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0133`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0092 — 88. Global Capital Risk

- Source: `SRC-005`
- Location: lines 2513–2569; heading `88. Global Capital Risk`
- Domain tags: RISK, CAPITAL
- Source statement: 88. Global Capital Risk: comme capital engagé dans :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `88. Global Capital Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-RISK-0134`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0093 — 89. Concurrent Execution Limit

- Source: `SRC-005`
- Location: lines 2570–2593; heading `89. Concurrent Execution Limit`
- Domain tags: RISK, INFRA, CAPITAL
- Source statement: 89. Concurrent Execution Limit: Mais la vraie limite vient surtout des : Le nombre est un garde-fou supplémentaire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `89. Concurrent Execution Limit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0135`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0094 — 90. Route Correlation / Dependency

- Source: `SRC-005`
- Location: lines 2594–2604; heading `90. Route Correlation / Dependency`
- Domain tags: RISK, PORTFOLIO, ROUTING
- Source statement: 90. Route Correlation / Dependency: ne sont pas considérées indépendantes. Le Portfolio Engine doit agréger leur risque.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `90. Route Correlation / Dependency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0136`; supporting items: none found by conservative heading match; domain indexes `RISK, PORTFOLIO, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0095 — 91. Portfolio Tail Risk

- Source: `SRC-005`
- Location: lines 2605–2644; heading `91. Portfolio Tail Risk`
- Domain tags: RISK, PORTFOLIO, ROUTING
- Source statement: 91. Portfolio Tail Risk: À terme : ES_{\alpha,portfolio} \leq PortfolioESLimit
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `91. Portfolio Tail Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0137`; supporting items: none found by conservative heading match; domain indexes `RISK, PORTFOLIO, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0096 — 92. Drawdown Constitution

- Source: `SRC-005`
- Location: lines 2645–2652; heading `92. Drawdown Constitution`
- Domain tags: RISK, CAPITAL
- Source statement: 92. Drawdown Constitution: Le drawdown peut réduire : mais jamais relaxer un risque.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `92. Drawdown Constitution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0138`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0097 — 93. Drawdown Bands

- Source: `SRC-005`
- Location: lines 2653–2663; heading `93. Drawdown Bands`
- Domain tags: RISK
- Source statement: 93. Drawdown Bands: Les seuils précis sont calibrés.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `93. Drawdown Bands` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0139`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0098 — 94. CAUTION

- Source: `SRC-005`
- Location: lines 2664–2672; heading `94. CAUTION`
- Domain tags: RISK, CAPITAL, ROUTING
- Source statement: 94. CAUTION: Actions possibles : reduce max capital utilization
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `94. CAUTION` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0140`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0099 — 95. RISK_OFF

- Source: `SRC-005`
- Location: lines 2673–2685; heading `95. RISK_OFF`
- Domain tags: RISK, RECOVERY
- Source statement: 95. RISK_OFF: new risk heavily restricted Les actions de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `95. RISK_OFF` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0141`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0100 — 96. HALT Drawdown

- Source: `SRC-005`
- Location: lines 2686–2699; heading `96. HALT Drawdown`
- Domain tags: RISK, RECONCILIATION, OPERATIONS
- Source statement: 96. HALT Drawdown: Au-dessus d’un hard drawdown :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `96. HALT Drawdown` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0142`; supporting items: none found by conservative heading match; domain indexes `RISK, RECONCILIATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0101 — 97. Drawdown Cannot Trigger Martingale

- Source: `SRC-005`
- Location: lines 2700–2707; heading `97. Drawdown Cannot Trigger Martingale`
- Domain tags: RISK
- Source statement: 97. Drawdown Cannot Trigger Martingale: est interdit comme mécanisme automatique de récupération.
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `97. Drawdown Cannot Trigger Martingale` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0143`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0102 — 98. Daily/Session Loss Limits

- Source: `SRC-005`
- Location: lines 2708–2745; heading `98. Daily/Session Loss Limits`
- Domain tags: RISK
- Source statement: 98. Daily/Session Loss Limits: On peut définir : Loss_{window} \leq LossLimit_{window}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `98. Daily/Session Loss Limits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0144`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0103 — 99. Why Multiple Windows

- Source: `SRC-005`
- Location: lines 2746–2760; heading `99. Why Multiple Windows`
- Domain tags: RISK, ARCH
- Source statement: 99. Why Multiple Windows: avant que le drawdown global soit encore important.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `99. Why Multiple Windows` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0145`; supporting items: none found by conservative heading match; domain indexes `RISK, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0104 — 100. Loss Velocity

- Source: `SRC-005`
- Location: lines 2761–2800; heading `100. Loss Velocity`
- Domain tags: RISK, ACCOUNTING
- Source statement: 100. Loss Velocity: LossVelocity_W = \frac{ PnL_{start}-PnL_{end} }{ W } Un rythme de perte anormal peut déclencher :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `100. Loss Velocity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0146`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0105 — 101. Consecutive Failure Monitor

- Source: `SRC-005`
- Location: lines 2801–2811; heading `101. Consecutive Failure Monitor`
- Domain tags: RISK, OPERATIONS, EXECUTION, RECOVERY
- Source statement: 101. Consecutive Failure Monitor: Une augmentation brutale peut signaler un problème d’exécution plutôt qu’une simple mauvaise stratégie.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `101. Consecutive Failure Monitor` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0147`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS, EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0106 — 102. Execution Quality Kill Switch

- Source: `SRC-005`
- Location: lines 2812–2825; heading `102. Execution Quality Kill Switch`
- Domain tags: RISK, ROUTING, GRAPH
- Source statement: 102. Execution Quality Kill Switch: Si : actual slippage
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `102. Execution Quality Kill Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0148`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0107 — 103. Simulator Calibration Kill Switch

- Source: `SRC-005`
- Location: lines 2826–2848; heading `103. Simulator Calibration Kill Switch`
- Domain tags: RISK, SIMULATOR, EXECUTION, ACCOUNTING
- Source statement: 103. Simulator Calibration Kill Switch: reduce size / disable model-dependent strategies
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `103. Simulator Calibration Kill Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0149`; supporting items: none found by conservative heading match; domain indexes `RISK, SIMULATOR, EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0108 — 104. Participant Model Drift Kill Switch

- Source: `SRC-005`
- Location: lines 2849–2861; heading `104. Participant Model Drift Kill Switch`
- Domain tags: RISK, PARTICIPANTS, EXECUTION, SURVIVAL, ROUTING
- Source statement: 104. Participant Model Drift Kill Switch: les routes sensibles à la concurrence utilisent :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `104. Participant Model Drift Kill Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0150`; supporting items: SRC-006-ITEM-0338, SRC-007-ITEM-0099; domain indexes `RISK, PARTICIPANTS, EXECUTION, SURVIVAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0109 — 105. Fallback Risk Principle

- Source: `SRC-005`
- Location: lines 2862–2874; heading `105. Fallback Risk Principle`
- Domain tags: RISK
- Source statement: 105. Fallback Risk Principle: Si un modèle sophistiqué tombe : fallback must be MORE conservative
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `105. Fallback Risk Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0151`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0110 — 106. Fee Change Kill Switch

- Source: `SRC-005`
- Location: lines 2875–2883; heading `106. Fee Change Kill Switch`
- Domain tags: RISK, ACCOUNTING, ROUTING
- Source statement: 106. Fee Change Kill Switch: Si les frais changent : Pas continuer avec anciens thresholds.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `106. Fee Change Kill Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0152`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0111 — 107. Metadata Change Kill Switch

- Source: `SRC-005`
- Location: lines 2884–2899; heading `107. Metadata Change Kill Switch`
- Domain tags: RISK, ROUTING, GRAPH
- Source statement: 107. Metadata Change Kill Switch: Si : precision
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `107. Metadata Change Kill Switch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0153`; supporting items: SRC-006-ITEM-0311; domain indexes `RISK, ROUTING, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0112 — 108. Feed Sequence Integrity

- Source: `SRC-005`
- Location: lines 2900–2913; heading `108. Feed Sequence Integrity`
- Domain tags: RISK, ACCOUNTING, EXECUTION
- Source statement: 108. Feed Sequence Integrity: Si un feed nécessite une séquence et que nous détectons : le book concerné devient :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `108. Feed Sequence Integrity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0154`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0113 — 109. No Silent Data Repair

- Source: `SRC-005`
- Location: lines 2914–2927; heading `109. No Silent Data Repair`
- Domain tags: RISK
- Source statement: 109. No Silent Data Repair: Interdit : guess missing book event
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `109. No Silent Data Repair` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0155`; supporting items: SRC-006-ITEM-0307; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0114 — 110. Cross-Market Consistency

- Source: `SRC-005`
- Location: lines 2928–2936; heading `110. Cross-Market Consistency`
- Domain tags: RISK, CROSS_MARKET
- Source statement: 110. Cross-Market Consistency: Une anomalie énorme détectée avec : Les plus beaux faux arbitrages viennent souvent d’une donnée mauvaise.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `110. Cross-Market Consistency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0156`; supporting items: SRC-007-ITEM-0132; domain indexes `RISK, CROSS_MARKET`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0115 — 111. Opportunity Outlier Gate

- Source: `SRC-005`
- Location: lines 2937–2976; heading `111. Opportunity Outlier Gate`
- Domain tags: RISK, ACCOUNTING
- Source statement: 111. Opportunity Outlier Gate: Si : Edge \gg HistoricalSupport
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `111. Opportunity Outlier Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0157`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0116 — 112. “Too Good To Be True” Rule

- Source: `SRC-005`
- Location: lines 2977–2984; heading `112. “Too Good To Be True” Rule`
- Domain tags: RISK, VALIDATION, PRODUCT
- Source statement: 112. “Too Good To Be True” Rule: Plus un edge sort de sa distribution habituelle : plus les validations doivent être strictes
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `112. “Too Good To Be True” Rule` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0158`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0117 — 113. Infrastructure Risk

- Source: `SRC-005`
- Location: lines 2985–2997; heading `113. Infrastructure Risk`
- Domain tags: RISK, INFRA
- Source statement: 113. Infrastructure Risk: mais le Risk Engine décide : si le serveur actuel est suffisamment sain pour trader maintenant.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `113. Infrastructure Risk` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0159`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0119 — Level 0

- Source: `SRC-005`
- Location: lines 2999–3003; heading `Level 0`
- Domain tags: RISK, OPERATIONS
- Source statement: Level 0: HEALTHY
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `Level 0` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0160`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0120 — Level 1

- Source: `SRC-005`
- Location: lines 3004–3014; heading `Level 1`
- Domain tags: RISK
- Source statement: Level 1: DEGRADED Possible :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `Level 1` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0161`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0121 — Level 2

- Source: `SRC-005`
- Location: lines 3015–3020; heading `Level 2`
- Domain tags: RISK
- Source statement: Level 2: UNSAFE new risk off
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `Level 2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0162`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0122 — Level 3

- Source: `SRC-005`
- Location: lines 3021–3027; heading `Level 3`
- Domain tags: RISK, EXECUTION, RECOVERY
- Source statement: Level 3: cancel + recovery + halt
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `Level 3` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0163`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0123 — 115. API Rate Limit Risk

- Source: `SRC-005`
- Location: lines 3028–3043; heading `115. API Rate Limit Risk`
- Domain tags: RISK
- Source statement: 115. API Rate Limit Risk: Le bot doit suivre :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `115. API Rate Limit Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0164`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0124 — 116. Rate-Limit Reservation

- Source: `SRC-005`
- Location: lines 3044–3058; heading `116. Rate-Limit Reservation`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION, CAPITAL
- Source statement: 116. Rate-Limit Reservation: peut être réservée pour :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `116. Rate-Limit Reservation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0165`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0125 — 117. Cancels Have Priority Over New Orders

- Source: `SRC-005`
- Location: lines 3059–3070; heading `117. Cancels Have Priority Over New Orders`
- Domain tags: RISK, EXECUTION, RECOVERY, CAPITAL
- Source statement: 117. Cancels Have Priority Over New Orders: Si API capacity devient rare :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `117. Cancels Have Priority Over New Orders` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0166`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0126 — 118. Risk Budget Architecture

- Source: `SRC-005`
- Location: lines 3071–3084; heading `118. Risk Budget Architecture`
- Domain tags: RISK, ARCH, INFRA, INVENTORY, CAPITAL
- Source statement: 118. Risk Budget Architecture: Le capital n’est pas le seul budget.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `118. Risk Budget Architecture` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0167`; supporting items: none found by conservative heading match; domain indexes `RISK, ARCH, INFRA, INVENTORY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0127 — 119. Risk Budget Consumption

- Source: `SRC-005`
- Location: lines 3085–3088; heading `119. Risk Budget Consumption`
- Domain tags: RISK
- Source statement: 119. Risk Budget Consumption: Chaque ExecutionPlan réserve les budgets nécessaires avant envoi. Ils sont libérés uniquement quand l’exposition correspondante disparaît.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `119. Risk Budget Consumption` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0168`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0128 — 120. Per-Market Limits

- Source: `SRC-005`
- Location: lines 3089–3100; heading `120. Per-Market Limits`
- Domain tags: RISK, ROUTING, MARKET_ATLAS, QUANT
- Source statement: 120. Per-Market Limits: Chaque marché possède : MaxOrderNotional
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `120. Per-Market Limits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0169`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING, MARKET_ATLAS, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0129 — 121. Per-Asset Limits

- Source: `SRC-005`
- Location: lines 3101–3110; heading `121. Per-Asset Limits`
- Domain tags: RISK, INVENTORY
- Source statement: 121. Per-Asset Limits: Chaque asset possède : inventory bands
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `121. Per-Asset Limits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0170`; supporting items: none found by conservative heading match; domain indexes `RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0130 — 122. Per-Strategy Limits

- Source: `SRC-005`
- Location: lines 3111–3123; heading `122. Per-Strategy Limits`
- Domain tags: RISK, RECOVERY, MICROSTRUCTURE, BRIDGE, OWA, TRIANGLE
- Source statement: 122. Per-Strategy Limits: Car leurs profils de risque sont différents.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `122. Per-Strategy Limits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0171`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, MICROSTRUCTURE, BRIDGE, OWA, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0131 — 123. Maker/Taker Limits Are Separate

- Source: `SRC-005`
- Location: lines 3124–3136; heading `123. Maker/Taker Limits Are Separate`
- Domain tags: RISK, EXECUTION
- Source statement: 123. Maker/Taker Limits Are Separate: Un marché peut autoriser : ou l’inverse selon les données.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `123. Maker/Taker Limits Are Separate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0172`; supporting items: SRC-004-ITEM-0057, SRC-008-ITEM-0103, SRC-008-ITEM-0104; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0132 — 124. Per-Client Risk Profile

- Source: `SRC-005`
- Location: lines 3137–3145; heading `124. Per-Client Risk Profile`
- Domain tags: RISK, CLIENT, MICROSTRUCTURE, DEPLOYMENT
- Source statement: 124. Per-Client Risk Profile: Dans l’image Docker client : peut contenir des limites configurables.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `124. Per-Client Risk Profile` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0173`; supporting items: none found by conservative heading match; domain indexes `RISK, CLIENT, MICROSTRUCTURE, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0133 — 125. Constitutional Floor

- Source: `SRC-005`
- Location: lines 3146–3166; heading `125. Constitutional Floor`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION, CLIENT
- Source statement: 125. Constitutional Floor: Le client peut demander : Il peut réduire le risque.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `125. Constitutional Floor` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0174`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0134 — 126. Safe Direction of Configuration

- Source: `SRC-005`
- Location: lines 3167–3179; heading `126. Safe Direction of Configuration`
- Domain tags: RISK, CLIENT
- Source statement: 126. Safe Direction of Configuration: Pour les desserrer au-delà des bornes validées :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `126. Safe Direction of Configuration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0175`; supporting items: none found by conservative heading match; domain indexes `RISK, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0135 — 127. Config Validation

- Source: `SRC-005`
- Location: lines 3180–3199; heading `127. Config Validation`
- Domain tags: RISK, VALIDATION
- Source statement: 127. Config Validation: Au démarrage : RiskConfig
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `127. Config Validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0176`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0136 — 128. Runtime Config Changes

- Source: `SRC-005`
- Location: lines 3200–3209; heading `128. Runtime Config Changes`
- Domain tags: RISK, PRODUCT
- Source statement: 128. Runtime Config Changes: Une modification de limite en production doit être : et ne s’applique jamais rétroactivement pour rendre une exposition existante “acceptable”.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `128. Runtime Config Changes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0177`; supporting items: none found by conservative heading match; domain indexes `RISK, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0137 — 129. No Risk Change During Critical Transition

- Source: `SRC-005`
- Location: lines 3210–3224; heading `129. No Risk Change During Critical Transition`
- Domain tags: RISK, ROUTING
- Source statement: 129. No Risk Change During Critical Transition: Éviter qu’une config change : Les emergency hard limits globaux peuvent néanmoins stopper une continuation.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `129. No Risk Change During Critical Transition` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0178`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0138 — 130. Kill Switch Taxonomy

- Source: `SRC-005`
- Location: lines 3225–3237; heading `130. Kill Switch Taxonomy`
- Domain tags: RISK, INFRA
- Source statement: 130. Kill Switch Taxonomy: Nous aurons au minimum :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `130. Kill Switch Taxonomy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0179`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0139 — 131. GLOBAL_KILL

- Source: `SRC-005`
- Location: lines 3238–3247; heading `131. GLOBAL_KILL`
- Domain tags: RISK, EXECUTION, RECONCILIATION
- Source statement: 131. GLOBAL_KILL: Effet : new risk off everywhere
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `131. GLOBAL_KILL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0180`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0140 — 132. MARKET_KILL

- Source: `SRC-005`
- Location: lines 3248–3260; heading `132. MARKET_KILL`
- Domain tags: RISK, ROUTING, GRAPH
- Source statement: 132. MARKET_KILL: Toutes les routes dépendantes sont automatiquement désactivées via :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `132. MARKET_KILL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0181`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0141 — 133. ASSET_KILL

- Source: `SRC-005`
- Location: lines 3261–3272; heading `133. ASSET_KILL`
- Domain tags: RISK, ROUTING
- Source statement: 133. ASSET_KILL: Si actif suspect : all routes touching asset
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `133. ASSET_KILL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0182`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0142 — 134. STRATEGY_KILL

- Source: `SRC-005`
- Location: lines 3273–3281; heading `134. STRATEGY_KILL`
- Domain tags: RISK, EXECUTION
- Source statement: 134. STRATEGY_KILL: Très utile si maker model se dégrade.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `134. STRATEGY_KILL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0183`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0143 — 135. MODEL_KILL

- Source: `SRC-005`
- Location: lines 3282–3290; heading `135. MODEL_KILL`
- Domain tags: RISK, CROSS_MARKET
- Source statement: 135. MODEL_KILL: est défectueux, ne pas forcément arrêter tout le bot. Désactiver uniquement les stratégies qui en dépendent obligatoirement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `135. MODEL_KILL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0184`; supporting items: none found by conservative heading match; domain indexes `RISK, CROSS_MARKET`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0144 — 136. Dependency-Aware Risk

- Source: `SRC-005`
- Location: lines 3291–3300; heading `136. Dependency-Aware Risk`
- Domain tags: RISK
- Source statement: 136. Dependency-Aware Risk: Le Risk Engine sait donc précisément ce qu’une panne doit désactiver.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `136. Dependency-Aware Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0185`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0145 — 137. Fail-Closed Principle

- Source: `SRC-005`
- Location: lines 3301–3317; heading `137. Fail-Closed Principle`
- Domain tags: RISK
- Source statement: 137. Fail-Closed Principle: Lorsque le système ne peut pas déterminer si une action :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `137. Fail-Closed Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0186`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0146 — 138. Fail-Open Exception

- Source: `SRC-005`
- Location: lines 3318–3329; heading `138. Fail-Open Exception`
- Domain tags: RISK, RECOVERY, ARCH
- Source statement: 138. Fail-Open Exception: actions reducing a known exposure
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `138. Fail-Open Exception` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-RISK-0187`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0147 — 139. Risk Decision Object

- Source: `SRC-005`
- Location: lines 3330–3352; heading `139. Risk Decision Object`
- Domain tags: RISK
- Source statement: 139. Risk Decision Object: Chaque évaluation retourne : RiskDecision {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `139. Risk Decision Object` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0188`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0148 — 140. Risk Action

- Source: `SRC-005`
- Location: lines 3353–3365; heading `140. Risk Action`
- Domain tags: RISK, RECOVERY
- Source statement: 140. Risk Action: Valeurs possibles : ALLOW
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `140. Risk Action` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0189`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0149 — 141. Reject Reasons Must Be Machine-Readable

- Source: `SRC-005`
- Location: lines 3366–3383; heading `141. Reject Reasons Must Be Machine-Readable`
- Domain tags: RISK, RECOVERY, RECONCILIATION, INFRA, INVENTORY
- Source statement: 141. Reject Reasons Must Be Machine-Readable: Exemples : RISK_BOOK_STALE
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `141. Reject Reasons Must Be Machine-Readable` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-RISK-0190`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, RECONCILIATION, INFRA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0150 — 142. Risk Decision Audit

- Source: `SRC-005`
- Location: lines 3384–3398; heading `142. Risk Decision Audit`
- Domain tags: RISK, DETERMINISM, INVENTORY, FUTURE
- Source statement: 142. Risk Decision Audit: On doit pouvoir répondre : Pourquoi ce trade a été rejeté ?
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `142. Risk Decision Audit` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0191`; supporting items: none found by conservative heading match; domain indexes `RISK, DETERMINISM, INVENTORY, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0151 — 143. Risk Is Re-Evaluated At Multiple Times

- Source: `SRC-005`
- Location: lines 3399–3400; heading `143. Risk Is Re-Evaluated At Multiple Times`
- Domain tags: RISK
- Source statement: 143. Risk Is Re-Evaluated At Multiple Times: Pas seulement au scanner.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `143. Risk Is Re-Evaluated At Multiple Times` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0192`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0152 — T0

- Source: `SRC-005`
- Location: lines 3401–3405; heading `T0`
- Domain tags: RISK
- Source statement: T0: Opportunity detected
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `T0` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0193`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0153 — T1

- Source: `SRC-005`
- Location: lines 3406–3410; heading `T1`
- Domain tags: RISK
- Source statement: T1: before reservation
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `T1` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0194`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0154 — T2

- Source: `SRC-005`
- Location: lines 3411–3415; heading `T2`
- Domain tags: RISK, EXECUTION
- Source statement: T2: immediately before order send
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `T2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0195`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0155 — T3

- Source: `SRC-005`
- Location: lines 3416–3420; heading `T3`
- Domain tags: RISK, EXECUTION
- Source statement: T3: after each fill
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `T3` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0196`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0156 — T4

- Source: `SRC-005`
- Location: lines 3421–3425; heading `T4`
- Domain tags: RISK
- Source statement: T4: before every next leg
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `T4` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0197`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0157 — T5

- Source: `SRC-005`
- Location: lines 3426–3431; heading `T5`
- Domain tags: RISK, EXECUTION
- Source statement: T5: during resting maker
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `T5` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0198`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0158 — 144. Time-of-Check / Time-of-Use Protection

- Source: `SRC-005`
- Location: lines 3432–3455; heading `144. Time-of-Check / Time-of-Use Protection`
- Domain tags: RISK, ACCOUNTING, SIMULATOR, SURVIVAL
- Source statement: 144. Time-of-Check / Time-of-Use Protection: Le TTL est calibré selon :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `144. Time-of-Check / Time-of-Use Protection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0199`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, SIMULATOR, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0159 — 145. Risk Snapshot

- Source: `SRC-005`
- Location: lines 3456–3474; heading `145. Risk Snapshot`
- Domain tags: RISK, INFRA, OPERATIONS, INVENTORY
- Source statement: 145. Risk Snapshot: Chaque décision se base sur un immutable : Cela empêche de mélanger plusieurs états temporels incohérents.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `145. Risk Snapshot` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0200`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, OPERATIONS, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0160 — 146. Route-Level Expected Loss Budget

- Source: `SRC-005`
- Location: lines 3475–3504; heading `146. Route-Level Expected Loss Budget`
- Domain tags: RISK, ROUTING
- Source statement: 146. Route-Level Expected Loss Budget: peut être agrégée au portefeuille. Cela sert surtout lors de multiples opportunités simultanées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `146. Route-Level Expected Loss Budget` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0201`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0161 — 147. Portfolio Optimization Is Subordinate To Hard Gates

- Source: `SRC-005`
- Location: lines 3505–3517; heading `147. Portfolio Optimization Is Subordinate To Hard Gates`
- Domain tags: RISK, PORTFOLIO, ROUTING
- Source statement: 147. Portfolio Optimization Is Subordinate To Hard Gates: Le Portfolio Optimizer ne reçoit que : Il ne peut pas choisir :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `147. Portfolio Optimization Is Subordinate To Hard Gates` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-RISK-0202`; supporting items: SRC-007-ITEM-0306; domain indexes `RISK, PORTFOLIO, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0162 — 148. Risk Cannot Be Overridden By Optimizer

- Source: `SRC-005`
- Location: lines 3518–3530; heading `148. Risk Cannot Be Overridden By Optimizer`
- Domain tags: RISK, ARCH
- Source statement: 148. Risk Cannot Be Overridden By Optimizer: Architecture : Candidate
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `148. Risk Cannot Be Overridden By Optimizer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0203`; supporting items: none found by conservative heading match; domain indexes `RISK, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0163 — 149. Capital Scaling

- Source: `SRC-005`
- Location: lines 3531–3545; heading `149. Capital Scaling`
- Domain tags: RISK, CAPITAL, SIZING, QUANT
- Source statement: 149. Capital Scaling: Augmenter le capital ne modifie jamais automatiquement : Le sizing monte seulement si :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `149. Capital Scaling` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0204`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0164 — 150. Auto-Compounding

- Source: `SRC-005`
- Location: lines 3546–3586; heading `150. Auto-Compounding`
- Domain tags: RISK, EXECUTION, ACCOUNTING, MICROSTRUCTURE, CAPITAL
- Source statement: 150. Auto-Compounding: Si profits augmentent le capital :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `150. Auto-Compounding` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0205`; supporting items: SRC-001-ITEM-0035; domain indexes `RISK, EXECUTION, ACCOUNTING, MICROSTRUCTURE, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0165 — 151. Scaling Gate

- Source: `SRC-005`
- Location: lines 3587–3596; heading `151. Scaling Gate`
- Domain tags: RISK, VALIDATION
- Source statement: 151. Scaling Gate: Augmenter une taille validée nécessite :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `151. Scaling Gate` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0206`; supporting items: SRC-006-ITEM-0427; domain indexes `RISK, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0166 — 152. Capital Bands

- Source: `SRC-005`
- Location: lines 3597–3605; heading `152. Capital Bands`
- Domain tags: RISK, CAPITAL, SIZING
- Source statement: 152. Capital Bands: Les bandes de capital peuvent exister pour configuration opérationnelle.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `152. Capital Bands` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0207`; supporting items: SRC-008-ITEM-0171; domain indexes `RISK, CAPITAL, SIZING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0167 — 153. Infrastructure Scaling

- Source: `SRC-005`
- Location: lines 3606–3643; heading `153. Infrastructure Scaling`
- Domain tags: RISK, INFRA, ACCOUNTING
- Source statement: 153. Infrastructure Scaling: LCB(\Delta PnL) > SafetyFactor \times \Delta Cost Le Risk Engine ne considère pas un serveur plus cher comme intrinsèquement plus sûr.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `153. Infrastructure Scaling` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0208`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0168 — 154. Production Deployment Risk

- Source: `SRC-005`
- Location: lines 3644–3656; heading `154. Production Deployment Risk`
- Domain tags: RISK, DEPLOYMENT, PRODUCT, CLIENT
- Source statement: 154. Production Deployment Risk: Chaque container client doit démarrer : auto trade immediately on process start
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `154. Production Deployment Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0209`; supporting items: none found by conservative heading match; domain indexes `RISK, DEPLOYMENT, PRODUCT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0169 — 155. Startup Risk Sequence

- Source: `SRC-005`
- Location: lines 3657–3682; heading `155. Startup Risk Sequence`
- Domain tags: RISK, EXECUTION, RECONCILIATION, CLOCK, OPERATIONS, ACCOUNTING
- Source statement: 155. Startup Risk Sequence: CONFIG VALIDATE CLOCK
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `155. Startup Risk Sequence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-RISK-0210`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECONCILIATION, CLOCK, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0170 — 156. Shutdown Risk Sequence

- Source: `SRC-005`
- Location: lines 3683–3696; heading `156. Shutdown Risk Sequence`
- Domain tags: RISK
- Source statement: 156. Shutdown Risk Sequence: STOP NEW RISK HANDLE RESTING ORDERS
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `156. Shutdown Risk Sequence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0211`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0171 — 157. Crash Restart

- Source: `SRC-005`
- Location: lines 3697–3709; heading `157. Crash Restart`
- Domain tags: RISK, OPERATIONS, RECONCILIATION
- Source statement: 157. Crash Restart: assume local state may be incomplete doit reconstruire l’état avant reprise.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `157. Crash Restart` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0212`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0172 — 158. Secrets Failure

- Source: `SRC-005`
- Location: lines 3710–3722; heading `158. Secrets Failure`
- Domain tags: RISK, SECURITY, EXECUTION, RECOVERY, RECONCILIATION, OPERATIONS
- Source statement: 158. Secrets Failure: Si signer est nécessaire pour cancel/recovery :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `158. Secrets Failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0213`; supporting items: none found by conservative heading match; domain indexes `RISK, SECURITY, EXECUTION, RECOVERY, RECONCILIATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0173 — 159. API Wallet Safety

- Source: `SRC-005`
- Location: lines 3723–3735; heading `159. API Wallet Safety`
- Domain tags: RISK, SECURITY, CROSS_EXCHANGE
- Source statement: 159. API Wallet Safety: Le bot ne doit pas nécessiter :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `159. API Wallet Safety` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0214`; supporting items: none found by conservative heading match; domain indexes `RISK, SECURITY, CROSS_EXCHANGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0174 — 160. Client Secret Isolation

- Source: `SRC-005`
- Location: lines 3736–3745; heading `160. Client Secret Isolation`
- Domain tags: RISK, SECURITY, CLIENT, DEPLOYMENT
- Source statement: 160. Client Secret Isolation: Une image Docker ne contient jamais : Les secrets arrivent au runtime.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `160. Client Secret Isolation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0215`; supporting items: none found by conservative heading match; domain indexes `RISK, SECURITY, CLIENT, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0175 — 161. Telemetry Secret Rule

- Source: `SRC-005`
- Location: lines 3746–3754; heading `161. Telemetry Secret Rule`
- Domain tags: RISK, SECURITY
- Source statement: 161. Telemetry Secret Rule: Aucun log/metric externe ne contient :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `161. Telemetry Secret Rule` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0216`; supporting items: none found by conservative heading match; domain indexes `RISK, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0176 — 162. Panic Policy

- Source: `SRC-005`
- Location: lines 3755–3768; heading `162. Panic Policy`
- Domain tags: RISK, OPERATIONS, ARCH
- Source statement: 162. Panic Policy: Un panic dans un module non critique : must not silently corrupt state
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `162. Panic Policy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0217`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0177 — 163. Memory/State Corruption

- Source: `SRC-005`
- Location: lines 3769–3783; heading `163. Memory/State Corruption`
- Domain tags: RISK, EXECUTION, INVENTORY, QUANT
- Source statement: 163. Memory/State Corruption: Si invariant interne impossible : Le bot ne tente pas de “corriger” silencieusement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `163. Memory/State Corruption` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0218`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, INVENTORY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0178 — 164. Numerical Risk

- Source: `SRC-005`
- Location: lines 3784–3801; heading `164. Numerical Risk`
- Domain tags: RISK
- Source statement: 164. Numerical Risk: hard reject / panic-safe halt Aucune valeur numérique invalide ne peut atteindre l’Execution Engine.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `164. Numerical Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0219`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0179 — 165. Zero Division

- Source: `SRC-005`
- Location: lines 3802–3817; heading `165. Zero Division`
- Domain tags: RISK, FORMULA
- Source statement: 165. Zero Division: doivent définir explicitement leurs cas de dénominateur nul.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `165. Zero Division` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0220`; supporting items: none found by conservative heading match; domain indexes `RISK, FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0180 — 166. Accounting Invariants

- Source: `SRC-005`
- Location: lines 3818–3846; heading `166. Accounting Invariants`
- Domain tags: RISK, ACCOUNTING, EXECUTION, RECONCILIATION
- Source statement: 166. Accounting Invariants: Pour chaque Execution : \sum AssetDeltas
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `166. Accounting Invariants` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0221`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0181 — 167. PnL Separation

- Source: `SRC-005`
- Location: lines 3847–3859; heading `167. PnL Separation`
- Domain tags: RISK, ACCOUNTING, RECOVERY, INFRA, MICROSTRUCTURE, INVENTORY, BRIDGE, ROUTING
- Source statement: 167. PnL Separation: Un profit d’inventaire ne peut masquer un mauvais Execution Engine.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `167. PnL Separation` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0222`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, RECOVERY, INFRA, MICROSTRUCTURE, INVENTORY, BRIDGE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0182 — 168. Risk Metrics By Source

- Source: `SRC-005`
- Location: lines 3860–3874; heading `168. Risk Metrics By Source`
- Domain tags: RISK, EXECUTION, RECOVERY, INFRA, ACCOUNTING, INVENTORY
- Source statement: 168. Risk Metrics By Source: On suit séparément les pertes provenant de : Cela permet d’arrêter précisément le composant défectueux.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `168. Risk Metrics By Source` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0223`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, INFRA, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0183 — 169. Global Kill Trigger Examples

- Source: `SRC-005`
- Location: lines 3875–3887; heading `169. Global Kill Trigger Examples`
- Domain tags: RISK, RECOVERY, SECURITY, ACCOUNTING
- Source statement: 169. Global Kill Trigger Examples: exchange behavior inconsistent with model
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `169. Global Kill Trigger Examples` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0224`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, SECURITY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0184 — 170. Market Kill Trigger Examples

- Source: `SRC-005`
- Location: lines 3888–3897; heading `170. Market Kill Trigger Examples`
- Domain tags: RISK, QUANT
- Source statement: 170. Market Kill Trigger Examples: book corruption extreme volatility
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `170. Market Kill Trigger Examples` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0225`; supporting items: none found by conservative heading match; domain indexes `RISK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0185 — 171. Strategy Kill Examples

- Source: `SRC-005`
- Location: lines 3898–3906; heading `171. Strategy Kill Examples`
- Domain tags: RISK, EXECUTION, RECOVERY, ACCOUNTING, MICROSTRUCTURE, MAKER_MODEL, OWA, TRIANGLE
- Source statement: 171. Strategy Kill Examples: triangle recovery rate too high
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `171. Strategy Kill Examples` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0226`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, ACCOUNTING, MICROSTRUCTURE, MAKER_MODEL, OWA, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0186 — 172. Automatic Restart Is Not Automatic Re-Trading

- Source: `SRC-005`
- Location: lines 3907–3923; heading `172. Automatic Restart Is Not Automatic Re-Trading`
- Domain tags: RISK, OPERATIONS, RECONCILIATION, DEPLOYMENT
- Source statement: 172. Automatic Restart Is Not Automatic Re-Trading: Un service manager peut redémarrer : mais le moteur recommence par :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `172. Automatic Restart Is Not Automatic Re-Trading` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0227`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS, RECONCILIATION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0187 — 173. Manual Override

- Source: `SRC-005`
- Location: lines 3924–3933; heading `173. Manual Override`
- Domain tags: RISK, ARCH
- Source statement: 173. Manual Override: Une interface opérateur peut :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `173. Manual Override` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0228`; supporting items: none found by conservative heading match; domain indexes `RISK, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0188 — 174. Dangerous Manual Override

- Source: `SRC-005`
- Location: lines 3934–3944; heading `174. Dangerous Manual Override`
- Domain tags: RISK, RECOVERY, RECONCILIATION
- Source statement: 174. Dangerous Manual Override: Elle ne doit pas pouvoir :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `174. Dangerous Manual Override` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0229`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0190 — CONSTITUTIONAL

- Source: `SRC-005`
- Location: lines 3946–3957; heading `CONSTITUTIONAL`
- Domain tags: RISK, EXECUTION, RECONCILIATION, OPERATIONS, INVENTORY
- Source statement: CONSTITUTIONAL: Exemples : no blind retry
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `CONSTITUTIONAL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0230`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECONCILIATION, OPERATIONS, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0191 — TUNABLE

- Source: `SRC-005`
- Location: lines 3958–3969; heading `TUNABLE`
- Domain tags: RISK, EXECUTION, INVENTORY, QUANT
- Source statement: TUNABLE: Exemples : MaxImpact
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `TUNABLE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0231`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, INVENTORY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0192 — 176. Parameter Governance

- Source: `SRC-005`
- Location: lines 3970–3982; heading `176. Parameter Governance`
- Domain tags: RISK, INFRA, CLOCK, VALIDATION, PRODUCT
- Source statement: 176. Parameter Governance: Chaque tunable parameter contient :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `176. Parameter Governance` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0232`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, CLOCK, VALIDATION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0193 — 177. No Magic Numbers

- Source: `SRC-005`
- Location: lines 3983–3996; heading `177. No Magic Numbers`
- Domain tags: RISK, INFRA
- Source statement: 177. No Magic Numbers: if latency > 500 { source = infrastructure calibration run XXX
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `177. No Magic Numbers` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0233`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0194 — 178. Parameter Provenance

- Source: `SRC-005`
- Location: lines 3997–4007; heading `178. Parameter Provenance`
- Domain tags: RISK, INFRA
- Source statement: 178. Parameter Provenance: Cela permet de savoir pourquoi un seuil existe.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `178. Parameter Provenance` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-RISK-0234`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0195 — 179. Safety Defaults

- Source: `SRC-005`
- Location: lines 4008–4020; heading `179. Safety Defaults`
- Domain tags: RISK, INFRA
- Source statement: 179. Safety Defaults: On n’utilise pas un paramètre agressif parce que :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `179. Safety Defaults` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0235`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0196 — 180. Model Promotion Risk

- Source: `SRC-005`
- Location: lines 4021–4034; heading `180. Model Promotion Risk`
- Domain tags: RISK, VALIDATION, ACCOUNTING, FUTURE
- Source statement: 180. Model Promotion Risk: Un modèle Challenger ne devient Champion que s’il améliore :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `180. Model Promotion Risk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0236`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION, ACCOUNTING, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0197 — 181. Champion Failure

- Source: `SRC-005`
- Location: lines 4035–4047; heading `181. Champion Failure`
- Domain tags: RISK
- Source statement: 181. Champion Failure: Si Champion échoue : fallback conservative model
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `181. Champion Failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0237`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0198 — 182. Research Features Cannot Leak Into Production Unvalidated

- Source: `SRC-005`
- Location: lines 4048–4062; heading `182. Research Features Cannot Leak Into Production Unvalidated`
- Domain tags: RISK, PRODUCT, RESEARCH, PARTICIPANTS, QUANT
- Source statement: 182. Research Features Cannot Leak Into Production Unvalidated: ne peut modifier les trades réels tant qu’elle n’est pas :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `182. Research Features Cannot Leak Into Production Unvalidated` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-RISK-0238`; supporting items: none found by conservative heading match; domain indexes `RISK, PRODUCT, RESEARCH, PARTICIPANTS, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0199 — 183. Backtest Cannot Override Live Evidence

- Source: `SRC-005`
- Location: lines 4063–4075; heading `183. Backtest Cannot Override Live Evidence`
- Domain tags: RISK, EXECUTION, VALIDATION, REPLAY
- Source statement: 183. Backtest Cannot Override Live Evidence: Si replay dit : excellent
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `183. Backtest Cannot Override Live Evidence` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0239`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0200 — 184. Live Evidence Needs Statistical Support

- Source: `SRC-005`
- Location: lines 4076–4089; heading `184. Live Evidence Needs Statistical Support`
- Domain tags: RISK, EXECUTION, OPERATIONS
- Source statement: 184. Live Evidence Needs Statistical Support: ne suffisent pas nécessairement à modifier un modèle.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `184. Live Evidence Needs Statistical Support` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0240`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0201 — 185. Incident Mode

- Source: `SRC-005`
- Location: lines 4090–4102; heading `185. Incident Mode`
- Domain tags: RISK, OPERATIONS, VALIDATION
- Source statement: 185. Incident Mode: Après anomalie critique : affected market/strategy
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `185. Incident Mode` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0241`; supporting items: none found by conservative heading match; domain indexes `RISK, OPERATIONS, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0202 — 186. Risk Constitution Testing

- Source: `SRC-005`
- Location: lines 4103–4112; heading `186. Risk Constitution Testing`
- Domain tags: RISK, VALIDATION
- Source statement: 186. Risk Constitution Testing: Chaque invariant doit avoir :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `186. Risk Constitution Testing` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0242`; supporting items: none found by conservative heading match; domain indexes `RISK, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0203 — 187. Property Test — No Overspend

- Source: `SRC-005`
- Location: lines 4113–4147; heading `187. Property Test — No Overspend`
- Domain tags: RISK, VALIDATION, INVENTORY
- Source statement: 187. Property Test — No Overspend: Pour toute séquence aléatoire :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `187. Property Test — No Overspend` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0243`; supporting items: SRC-006-ITEM-0469; domain indexes `RISK, VALIDATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0204 — 188. Property Test — No Overfill

- Source: `SRC-005`
- Location: lines 4148–4177; heading `188. Property Test — No Overfill`
- Domain tags: RISK, EXECUTION, VALIDATION
- Source statement: 188. Property Test — No Overfill: FilledSize \leq RequestedSize+\epsilon Sinon invariant fatal.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `188. Property Test — No Overfill` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0244`; supporting items: SRC-006-ITEM-0469; domain indexes `RISK, EXECUTION, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0205 — 189. Property Test — Hard Inventory

- Source: `SRC-005`
- Location: lines 4178–4211; heading `189. Property Test — Hard Inventory`
- Domain tags: RISK, VALIDATION, INVENTORY, FUTURE
- Source statement: 189. Property Test — Hard Inventory: Aucune action classée : NEW_RISK
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `189. Property Test — Hard Inventory` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0245`; supporting items: SRC-006-ITEM-0385, SRC-006-ITEM-0469; domain indexes `RISK, VALIDATION, INVENTORY, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0206 — 190. Property Test — No New Risk During Unknown

- Source: `SRC-005`
- Location: lines 4212–4225; heading `190. Property Test — No New Risk During Unknown`
- Domain tags: RISK, RECOVERY, VALIDATION, ROUTING
- Source statement: 190. Property Test — No New Risk During Unknown: aucune nouvelle route ne peut utiliser la portion réservée de
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `190. Property Test — No New Risk During Unknown` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0246`; supporting items: SRC-006-ITEM-0469; domain indexes `RISK, RECOVERY, VALIDATION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0207 — 191. Property Test — Stale Feed

- Source: `SRC-005`
- Location: lines 4226–4257; heading `191. Property Test — Stale Feed`
- Domain tags: RISK, VALIDATION, ACCOUNTING
- Source statement: 191. Property Test — Stale Feed: dépendant du book retourne :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `191. Property Test — Stale Feed` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0247`; supporting items: SRC-006-ITEM-0469, SRC-004-ITEM-0124; domain indexes `RISK, VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0208 — 192. Property Test — Risk Reduction Exception

- Source: `SRC-005`
- Location: lines 4258–4267; heading `192. Property Test — Risk Reduction Exception`
- Domain tags: RISK, VALIDATION, RECOVERY, PRODUCT
- Source statement: 192. Property Test — Risk Reduction Exception: Si inventaire dépasse HardMax : → may pass recovery gates
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `192. Property Test — Risk Reduction Exception` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0248`; supporting items: SRC-006-ITEM-0469; domain indexes `RISK, VALIDATION, RECOVERY, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0209 — 193. Fault Injection — Lost HTTP Response

- Source: `SRC-005`
- Location: lines 4268–4277; heading `193. Fault Injection — Lost HTTP Response`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION
- Source statement: 193. Fault Injection — Lost HTTP Response: Order sent, filled exchange-side, response lost.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `193. Fault Injection — Lost HTTP Response` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0249`; supporting items: SRC-006-ITEM-0472; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0210 — 194. Fault Injection — Market Feed Loss

- Source: `SRC-005`
- Location: lines 4278–4287; heading `194. Fault Injection — Market Feed Loss`
- Domain tags: RISK, ACCOUNTING, EXECUTION, RECOVERY
- Source statement: 194. Fault Injection — Market Feed Loss: Pendant maker resting. Attendu :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `194. Fault Injection — Market Feed Loss` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0250`; supporting items: SRC-006-ITEM-0472; domain indexes `RISK, ACCOUNTING, EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0211 — 195. Fault Injection — Account Feed Loss

- Source: `SRC-005`
- Location: lines 4288–4295; heading `195. Fault Injection — Account Feed Loss`
- Domain tags: RISK, ACCOUNTING, RECONCILIATION
- Source statement: 195. Fault Injection — Account Feed Loss: Attendu : new risk off
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `195. Fault Injection — Account Feed Loss` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0251`; supporting items: SRC-006-ITEM-0472, SRC-006-ITEM-0518; domain indexes `RISK, ACCOUNTING, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0212 — 196. Fault Injection — Clock Failure

- Source: `SRC-005`
- Location: lines 4296–4307; heading `196. Fault Injection — Clock Failure`
- Domain tags: RISK, CLOCK, RECOVERY, INFRA
- Source statement: 196. Fault Injection — Clock Failure: Attendu : disable latency-sensitive decisions
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `196. Fault Injection — Clock Failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0252`; supporting items: SRC-006-ITEM-0472; domain indexes `RISK, CLOCK, RECOVERY, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0213 — 197. Fault Injection — Model NaN

- Source: `SRC-005`
- Location: lines 4308–4316; heading `197. Fault Injection — Model NaN`
- Domain tags: RISK, OPERATIONS, ROUTING
- Source statement: 197. Fault Injection — Model NaN: Attendu : route reject
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `197. Fault Injection — Model NaN` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0253`; supporting items: SRC-006-ITEM-0472; domain indexes `RISK, OPERATIONS, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0214 — 198. Fault Injection — Disk Full

- Source: `SRC-005`
- Location: lines 4317–4330; heading `198. Fault Injection — Disk Full`
- Domain tags: RISK, EXECUTION, RECORDER, OPERATIONS, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 198. Fault Injection — Disk Full: Si persistence critique impossible :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `198. Fault Injection — Disk Full` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0254`; supporting items: SRC-006-ITEM-0472; domain indexes `RISK, EXECUTION, RECORDER, OPERATIONS, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0215 — 199. Fault Injection — CPU Saturation

- Source: `SRC-005`
- Location: lines 4331–4338; heading `199. Fault Injection — CPU Saturation`
- Domain tags: RISK, INFRA
- Source statement: 199. Fault Injection — CPU Saturation: Si latence dépasse limites :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `199. Fault Injection — CPU Saturation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0255`; supporting items: SRC-006-ITEM-0472; domain indexes `RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0216 — 200. Definition of Constitutional Compliance

- Source: `SRC-005`
- Location: lines 4339–4355; heading `200. Definition of Constitutional Compliance`
- Domain tags: RISK, EXECUTION, INVENTORY, ARCH
- Source statement: 200. Definition of Constitutional Compliance: Un module est constitutionnellement compatible seulement s’il : cannot directly submit unapproved order
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `200. Definition of Constitutional Compliance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0256`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, INVENTORY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0217 — 201. Architecture du Risk Engine

- Source: `SRC-005`
- Location: lines 4356–4395; heading `201. Architecture du Risk Engine`
- Domain tags: RISK, ARCH, INFRA, INVENTORY, ROUTING
- Source statement: 201. Architecture du Risk Engine: MarketState ├──────────────┐
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `201. Architecture du Risk Engine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0257`; supporting items: SRC-006-ITEM-0382; domain indexes `RISK, ARCH, INFRA, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0218 — 202. Risk Gate Ordering

- Source: `SRC-005`
- Location: lines 4396–4428; heading `202. Risk Gate Ordering`
- Domain tags: RISK, DETERMINISM, VALIDATION, OPERATIONS, INVENTORY, PORTFOLIO, ROUTING, QUANT
- Source statement: 202. Risk Gate Ordering: 7. MODEL SUPPORT / OOD 10. SOFT INVENTORY / PORTFOLIO
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `202. Risk Gate Ordering` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0258`; supporting items: none found by conservative heading match; domain indexes `RISK, DETERMINISM, VALIDATION, OPERATIONS, INVENTORY, PORTFOLIO, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0219 — 203. Fast Reject Path

- Source: `SRC-005`
- Location: lines 4429–4442; heading `203. Fast Reject Path`
- Domain tags: RISK, ROUTING, SIMULATOR, PORTFOLIO
- Source statement: 203. Fast Reject Path: Le système ne lance pas :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `203. Fast Reject Path` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0259`; supporting items: none found by conservative heading match; domain indexes `RISK, ROUTING, SIMULATOR, PORTFOLIO`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0220 — 204. Risk Engine Hot Path

- Source: `SRC-005`
- Location: lines 4443–4458; heading `204. Risk Engine Hot Path`
- Domain tags: RISK, ROUTING, HOT_WARM_COLD, ARCH, DETERMINISM, INFRA, CAPITAL
- Source statement: 204. Risk Engine Hot Path: Aucune requête réseau dans : Les données nécessaires doivent déjà être en RAM.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `204. Risk Engine Hot Path` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0260`; supporting items: SRC-006-ITEM-0382; domain indexes `RISK, ROUTING, HOT_WARM_COLD, ARCH, DETERMINISM, INFRA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0221 — 205. Risk Snapshot Immutability

- Source: `SRC-005`
- Location: lines 4459–4472; heading `205. Risk Snapshot Immutability`
- Domain tags: RISK, CLOCK
- Source statement: 205. Risk Snapshot Immutability: Le prochain market event crée : Pas de lecture incohérente de deux timestamps différents.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `205. Risk Snapshot Immutability` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0261`; supporting items: none found by conservative heading match; domain indexes `RISK, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0222 — 206. Risk Config Versioning

- Source: `SRC-005`
- Location: lines 4473–4484; heading `206. Risk Config Versioning`
- Domain tags: RISK, ACCOUNTING
- Source statement: 206. Risk Config Versioning: Cela permet de comparer : PnL avant/après changement de politique
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `206. Risk Config Versioning` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0262`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0223 — 207. Risk Replay

- Source: `SRC-005`
- Location: lines 4485–4498; heading `207. Risk Replay`
- Domain tags: RISK, REPLAY, QUANT
- Source statement: 207. Risk Replay: Le Replay doit pouvoir exécuter : what if MaxImpact was lower?
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `207. Risk Replay` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0263`; supporting items: none found by conservative heading match; domain indexes `RISK, REPLAY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0224 — 208. Reject Dataset

- Source: `SRC-005`
- Location: lines 4499–4509; heading `208. Reject Dataset`
- Domain tags: RISK, DATA, SIMULATOR, FUTURE
- Source statement: 208. Reject Dataset: Chaque reject devient une observation : Très important pour calibrer les thresholds.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `208. Reject Dataset` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-RISK-0264`; supporting items: none found by conservative heading match; domain indexes `RISK, DATA, SIMULATOR, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0225 — 209. Why Store Rejects

- Source: `SRC-005`
- Location: lines 4510–4523; heading `209. Why Store Rejects`
- Domain tags: RISK, ACCOUNTING
- Source statement: 209. Why Store Rejects: on connaît uniquement les trades choisis
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `209. Why Store Rejects` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0265`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0226 — 210. Risk Threshold Optimization

- Source: `SRC-005`
- Location: lines 4524–4594; heading `210. Risk Threshold Optimization`
- Domain tags: RISK, RECOVERY, ACCOUNTING, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 210. Risk Threshold Optimization: ne doit pas être choisi seulement pour maximiser : Objective(\theta) = NetPnL - \lambda_1 Drawdown - \lambda_2 ES - \lambda_3 RecoveryFrequency
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `210. Risk Threshold Optimization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0266`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, ACCOUNTING, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0227 — 211. Risk Budget Must Match Capital

- Source: `SRC-005`
- Location: lines 4595–4609; heading `211. Risk Budget Must Match Capital`
- Domain tags: RISK, CAPITAL, ROUTING
- Source statement: 211. Risk Budget Must Match Capital: Certains limits absolus évoluent avec le capital. si la liquidité n’a pas augmenté.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `211. Risk Budget Must Match Capital` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0267`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0228 — 212. Risk Budget Must Match Capacity

- Source: `SRC-005`
- Location: lines 4610–4627; heading `212. Risk Budget Must Match Capacity`
- Domain tags: RISK, CAPITAL
- Source statement: 212. Risk Budget Must Match Capacity: La vraie relation est :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `212. Risk Budget Must Match Capacity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0268`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0229 — 213. Minimum Economic Significance

- Source: `SRC-005`
- Location: lines 4628–4651; heading `213. Minimum Economic Significance`
- Domain tags: RISK, ACCOUNTING, OPERATIONS, CAPITAL, ROUTING
- Source statement: 213. Minimum Economic Significance: Même une route sûre peut être rejetée si : est trop faible par rapport à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `213. Minimum Economic Significance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0269`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, OPERATIONS, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0230 — 214. Risk vs Economic Gate

- Source: `SRC-005`
- Location: lines 4652–4674; heading `214. Risk vs Economic Gate`
- Domain tags: RISK, ACCOUNTING, ROUTING
- Source statement: 214. Risk vs Economic Gate: route safe but only +0.001€
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `214. Risk vs Economic Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0270`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0231 — 215. Risk Accounting

- Source: `SRC-005`
- Location: lines 4675–4685; heading `215. Risk Accounting`
- Domain tags: RISK, ACCOUNTING
- Source statement: 215. Risk Accounting: On doit pouvoir produire :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `215. Risk Accounting` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-RISK-0271`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0232 — 216. Constitution Principle — Risk Is Observable

- Source: `SRC-005`
- Location: lines 4686–4695; heading `216. Constitution Principle — Risk Is Observable`
- Domain tags: RISK
- Source statement: 216. Constitution Principle — Risk Is Observable: Aucune règle importante ne doit agir silencieusement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `216. Constitution Principle — Risk Is Observable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0272`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0233 — 217. Constitution Principle — Risk Is Deterministic Given Inputs

- Source: `SRC-005`
- Location: lines 4696–4709; heading `217. Constitution Principle — Risk Is Deterministic Given Inputs`
- Domain tags: RISK, DETERMINISM
- Source statement: 217. Constitution Principle — Risk Is Deterministic Given Inputs: Pour : same RiskSnapshot
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `217. Constitution Principle — Risk Is Deterministic Given Inputs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0273`; supporting items: none found by conservative heading match; domain indexes `RISK, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0234 — 218. Constitution Principle — Risk Is Reproducible

- Source: `SRC-005`
- Location: lines 4710–4721; heading `218. Constitution Principle — Risk Is Reproducible`
- Domain tags: RISK, DETERMINISM, REPLAY
- Source statement: 218. Constitution Principle — Risk Is Reproducible: Le Replay doit pouvoir reconstruire exactement :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `218. Constitution Principle — Risk Is Reproducible` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-RISK-0274`; supporting items: none found by conservative heading match; domain indexes `RISK, DETERMINISM, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0235 — 219. Constitution Principle — Risk Does Not Predict Profit

- Source: `SRC-005`
- Location: lines 4722–4734; heading `219. Constitution Principle — Risk Does Not Predict Profit`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE
- Source statement: 219. Constitution Principle — Risk Does Not Predict Profit: Le Risk Engine n’est pas :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `219. Constitution Principle — Risk Does Not Predict Profit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0275`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0236 — 220. Constitution Principle — Uncertainty Is Risk

- Source: `SRC-005`
- Location: lines 4735–4746; heading `220. Constitution Principle — Uncertainty Is Risk`
- Domain tags: RISK, EXECUTION, INFRA, INVENTORY
- Source statement: 220. Constitution Principle — Uncertainty Is Risk: Si nous ne savons pas correctement : l’incertitude elle-même est une raison de réduire ou refuser le risque.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `220. Constitution Principle — Uncertainty Is Risk` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0276`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, INFRA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0237 — 221. Constitution Principle — Complexity Must Fail Safe

- Source: `SRC-005`
- Location: lines 4747–4761; heading `221. Constitution Principle — Complexity Must Fail Safe`
- Domain tags: RISK, PARTICIPANTS, CROSS_MARKET, QUANT
- Source statement: 221. Constitution Principle — Complexity Must Fail Safe: plus leur panne doit : et jamais rendre le bot plus agressif.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `221. Constitution Principle — Complexity Must Fail Safe` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0277`; supporting items: none found by conservative heading match; domain indexes `RISK, PARTICIPANTS, CROSS_MARKET, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0238 — 222. Constitution Principle — Existing Exposure Beats New Alpha

- Source: `SRC-005`
- Location: lines 4762–4814; heading `222. Constitution Principle — Existing Exposure Beats New Alpha`
- Domain tags: RISK, ACCOUNTING
- Source statement: 222. Constitution Principle — Existing Exposure Beats New Alpha: Formellement : Priority(RiskReduction) > Priority(NewExpectedPnL)
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `222. Constitution Principle — Existing Exposure Beats New Alpha` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0278`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0239 — 223. Constitution Principle — Exchange Truth Beats Model Truth

- Source: `SRC-005`
- Location: lines 4815–4876; heading `223. Constitution Principle — Exchange Truth Beats Model Truth`
- Domain tags: RISK, RECONCILIATION, EXECUTION, INVENTORY
- Source statement: 223. Constitution Principle — Exchange Truth Beats Model Truth: ObservedFill > PredictedFill ObservedBalance > ExpectedBalance
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `223. Constitution Principle — Exchange Truth Beats Model Truth` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0279`; supporting items: none found by conservative heading match; domain indexes `RISK, RECONCILIATION, EXECUTION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0240 — 224. Constitution Principle — Hard Rules Beat EV

- Source: `SRC-005`
- Location: lines 4877–4894; heading `224. Constitution Principle — Hard Rules Beat EV`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION, INVENTORY
- Source statement: 224. Constitution Principle — Hard Rules Beat EV: Même : 100
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `224. Constitution Principle — Hard Rules Beat EV` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0280`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0241 — 225. Constitution Principle — No Hidden Leverage

- Source: `SRC-005`
- Location: lines 4895–4904; heading `225. Constitution Principle — No Hidden Leverage`
- Domain tags: RISK, CAPITAL, ROUTING
- Source statement: 225. Constitution Principle — No Hidden Leverage: Le spot bot ne doit jamais créer volontairement un risque équivalent à du leverage caché via : Le capital réellement engagé doit être traçable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `225. Constitution Principle — No Hidden Leverage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0281`; supporting items: none found by conservative heading match; domain indexes `RISK, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0242 — 226. Constitution Principle — No Unlimited Recovery Loop

- Source: `SRC-005`
- Location: lines 4905–4923; heading `226. Constitution Principle — No Unlimited Recovery Loop`
- Domain tags: RISK, RECOVERY
- Source statement: 226. Constitution Principle — No Unlimited Recovery Loop: Pas une boucle infinie de : trade → fail → recovery → fail → recovery
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `226. Constitution Principle — No Unlimited Recovery Loop` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0282`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0243 — 227. Constitution Principle — Model Confidence Cannot Be Purchased With Size

- Source: `SRC-005`
- Location: lines 4924–4941; heading `227. Constitution Principle — Model Confidence Cannot Be Purchased With Size`
- Domain tags: RISK
- Source statement: 227. Constitution Principle — Model Confidence Cannot Be Purchased With Size: si le modèle est complètement : Réduire la taille n’est valable que dans les zones :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `227. Constitution Principle — Model Confidence Cannot Be Purchased With Size` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0283`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0244 — 228. Constitution Principle — Low Liquidity Cannot Be Fixed With Faster VPS

- Source: `SRC-005`
- Location: lines 4942–4958; heading `228. Constitution Principle — Low Liquidity Cannot Be Fixed With Faster VPS`
- Domain tags: RISK, INFRA, CAPITAL
- Source statement: 228. Constitution Principle — Low Liquidity Cannot Be Fixed With Faster VPS: does not increase actual book capacity Le Risk Engine ne confond jamais :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `228. Constitution Principle — Low Liquidity Cannot Be Fixed With Faster VPS` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0284`; supporting items: none found by conservative heading match; domain indexes `RISK, INFRA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0245 — 229. Constitution Principle — Profitability Must Survive Real Costs

- Source: `SRC-005`
- Location: lines 4959–4970; heading `229. Constitution Principle — Profitability Must Survive Real Costs`
- Domain tags: RISK, ACCOUNTING, MICROSTRUCTURE, ROUTING, QUANT
- Source statement: 229. Constitution Principle — Profitability Must Survive Real Costs: Une route n’est jamais considérée profitable avant :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `229. Constitution Principle — Profitability Must Survive Real Costs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0285`; supporting items: none found by conservative heading match; domain indexes `RISK, ACCOUNTING, MICROSTRUCTURE, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0246 — 230. Constitution Principle — Every Risk Increase Is Explicit

- Source: `SRC-005`
- Location: lines 4971–4980; heading `230. Constitution Principle — Every Risk Increase Is Explicit`
- Domain tags: RISK
- Source statement: 230. Constitution Principle — Every Risk Increase Is Explicit: Chaque action est classifiée : Les règles peuvent dépendre de cette classification.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `230. Constitution Principle — Every Risk Increase Is Explicit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0286`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0247 — 231. Risk-Increasing Action

- Source: `SRC-005`
- Location: lines 4981–4990; heading `231. Risk-Increasing Action`
- Domain tags: RISK, EXECUTION, ROUTING
- Source statement: 231. Risk-Increasing Action: buy more asset above target
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `231. Risk-Increasing Action` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0287`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0248 — 232. Risk-Neutral Action

- Source: `SRC-005`
- Location: lines 4991–5000; heading `232. Risk-Neutral Action`
- Domain tags: RISK, EXECUTION, RECONCILIATION
- Source statement: 232. Risk-Neutral Action: Exemple : query
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `232. Risk-Neutral Action` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0288`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0249 — 233. Risk-Reducing Action

- Source: `SRC-005`
- Location: lines 5001–5009; heading `233. Risk-Reducing Action`
- Domain tags: RISK, EXECUTION, PRODUCT
- Source statement: 233. Risk-Reducing Action: peut être autorisée sous conditions plus larges.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `233. Risk-Reducing Action` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0289`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0250 — 234. Final RiskDecision Contract

- Source: `SRC-005`
- Location: lines 5010–5029; heading `234. Final RiskDecision Contract`
- Domain tags: RISK
- Source statement: 234. Final RiskDecision Contract: Avant tout ordre réel : Donc même un bug dans Strategy ne peut idéalement pas envoyer un ordre directement.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `234. Final RiskDecision Contract` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0290`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0251 — 235. Defense in Depth

- Source: `SRC-005`
- Location: lines 5030–5050; heading `235. Defense in Depth`
- Domain tags: RISK
- Source statement: 235. Defense in Depth: L’Execution Layer revérifie au minimum :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `235. Defense in Depth` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0291`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0252 — 236. Risk Constitution in Docker Client

- Source: `SRC-005`
- Location: lines 5051–5059; heading `236. Risk Constitution in Docker Client`
- Domain tags: RISK, DEPLOYMENT, CLIENT
- Source statement: 236. Risk Constitution in Docker Client: La constitution est compilée avec le bot. mais pas un moyen de supprimer les invariants.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `236. Risk Constitution in Docker Client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0292`; supporting items: none found by conservative heading match; domain indexes `RISK, DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0253 — 237. Unsupported Risk Configuration

- Source: `SRC-005`
- Location: lines 5060–5068; heading `237. Unsupported Risk Configuration`
- Domain tags: RISK, CLIENT, QUANT
- Source statement: 237. Unsupported Risk Configuration: Si client demande : MaxImpact = 100%
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `237. Unsupported Risk Configuration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0293`; supporting items: none found by conservative heading match; domain indexes `RISK, CLIENT, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0254 — 238. Risk Profile Levels

- Source: `SRC-005`
- Location: lines 5069–5080; heading `238. Risk Profile Levels`
- Domain tags: RISK, MICROSTRUCTURE, INFRA, BENCHMARK
- Source statement: 238. Risk Profile Levels: Nous pourrons éventuellement fournir : Mais ce sont seulement des presets de paramètres tunables.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `238. Risk Profile Levels` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0294`; supporting items: none found by conservative heading match; domain indexes `RISK, MICROSTRUCTURE, INFRA, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0255 — 239. Final Architecture

- Source: `SRC-005`
- Location: lines 5081–5131; heading `239. Final Architecture`
- Domain tags: RISK, ARCH, RECONCILIATION, OPERATIONS, ACCOUNTING, INVENTORY, CAPITAL, SIZING
- Source statement: 239. Final Architecture: REJECT? ─── YES ──> STOP
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `239. Final Architecture` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0295`; supporting items: none found by conservative heading match; domain indexes `RISK, ARCH, RECONCILIATION, OPERATIONS, ACCOUNTING, INVENTORY, CAPITAL, SIZING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0256 — 240. Résumé des invariants majeurs

- Source: `SRC-005`
- Location: lines 5132–5185; heading `240. Résumé des invariants majeurs`
- Domain tags: RISK, EXECUTION, RECOVERY, RECONCILIATION, ACCOUNTING, MICROSTRUCTURE, INVENTORY, CAPITAL
- Source statement: 240. Résumé des invariants majeurs: Les règles à retenir absolument : PARTIAL FILL = REAL EXPOSURE
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `240. Résumé des invariants majeurs` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0296`; supporting items: none found by conservative heading match; domain indexes `RISK, EXECUTION, RECOVERY, RECONCILIATION, ACCOUNTING, MICROSTRUCTURE, INVENTORY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0257 — 241. Definition of Constitutional Success

- Source: `SRC-005`
- Location: lines 5186–5241; heading `241. Definition of Constitutional Success`
- Domain tags: RISK
- Source statement: 241. Definition of Constitutional Success: La constitution est réussie si un bug ou une panne transforme le bot préférentiellement en : C’est la propriété fondamentale recherchée.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `241. Definition of Constitutional Success` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0297`; supporting items: none found by conservative heading match; domain indexes `RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0258 — 242. Principe final

- Source: `SRC-005`
- Location: lines 5242–5373; heading `242. Principe final`
- Domain tags: RISK, RECOVERY, ACCOUNTING, MICROSTRUCTURE
- Source statement: 242. Principe final: Le bot peut être : pendant quelques minutes à cause d’une protection conservatrice.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `242. Principe final` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-RISK-0298`; supporting items: none found by conservative heading match; domain indexes `RISK, RECOVERY, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0261 — 1. Objectif

- Source: `SRC-005`
- Location: lines 5376–5410; heading `1. Objectif`
- Domain tags: DATA, EXECUTION, CLOCK, VALIDATION, REPLAY, ARCH, RESEARCH
- Source statement: 1. Objectif: Le but est de garantir : qu’un même état de marché, un même état de compte, une même configuration, les mêmes modèles et le même seed produisent exactement la même décision, que le moteur tourne en Replay, Paper, Shadow, Micro-live ou Live.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `1. Objectif` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0010`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, CLOCK, VALIDATION, REPLAY, ARCH, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0262 — 2. Principe fondamental

- Source: `SRC-005`
- Location: lines 5411–5438; heading `2. Principe fondamental`
- Domain tags: DATA
- Source statement: 2. Principe fondamental: Aucune couche ne doit mélanger les responsabilités.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `2. Principe fondamental` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0011`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0264 — L0 — Raw

- Source: `SRC-005`
- Location: lines 5440–5450; heading `L0 — Raw`
- Domain tags: DATA
- Source statement: L0 — Raw: Ce que la source nous envoie réellement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `L0 — Raw` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0012`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0265 — L1 — Normalized Events

- Source: `SRC-005`
- Location: lines 5451–5462; heading `L1 — Normalized Events`
- Domain tags: DATA, EXECUTION, DEPLOYMENT, INVENTORY
- Source statement: L1 — Normalized Events: Événements convertis dans notre schema interne.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `L1 — Normalized Events` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0013`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, DEPLOYMENT, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0266 — L2 — State

- Source: `SRC-005`
- Location: lines 5463–5472; heading `L2 — State`
- Domain tags: DATA, INFRA, INVENTORY
- Source statement: L2 — State: État reconstruit : BookState
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `L2 — State` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0014`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0267 — L3 — Derived Features

- Source: `SRC-005`
- Location: lines 5473–5482; heading `L3 — Derived Features`
- Domain tags: DATA, SURVIVAL, MICROSTRUCTURE, CAPITAL, ROUTING, QUANT
- Source statement: L3 — Derived Features: volatility survival forecast
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `L3 — Derived Features` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0015`; supporting items: SRC-003-ITEM-0043; domain indexes `DATA, SURVIVAL, MICROSTRUCTURE, CAPITAL, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0268 — L4 — Decisions / Results

- Source: `SRC-005`
- Location: lines 5483–5492; heading `L4 — Decisions / Results`
- Domain tags: DATA, RISK
- Source statement: L4 — Decisions / Results: Opportunity ExecutionPlan
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `L4 — Decisions / Results` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0016`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0269 — 4. Règle RAW

- Source: `SRC-005`
- Location: lines 5493–5503; heading `4. Règle RAW`
- Domain tags: DATA, CLOCK
- Source statement: 4. Règle RAW: On ne réécrit jamais l’histoire source.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `4. Règle RAW` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0017`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0270 — 5. RawEvent

- Source: `SRC-005`
- Location: lines 5504–5530; heading `5. RawEvent`
- Domain tags: DATA, RECORDER, CLOCK
- Source statement: 5. RawEvent: Structure conceptuelle : RawEvent {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `5. RawEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0018`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0271 — 6. event_id

- Source: `SRC-005`
- Location: lines 5531–5548; heading `6. event_id`
- Domain tags: DATA, REPLAY
- Source statement: 6. event_id: Idéalement dérivé d’une combinaison : ou généré localement de manière unique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `6. event_id` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0019`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0272 — 7. recorder_seq

- Source: `SRC-005`
- Location: lines 5549–5565; heading `7. recorder_seq`
- Domain tags: RECORDER, EXECUTION
- Source statement: 7. recorder_seq: Elle constitue l’ordre local définitif d’observation.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `7. recorder_seq` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REC-0008`; supporting items: none found by conservative heading match; domain indexes `RECORDER, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0273 — 8. exchange_ts

- Source: `SRC-005`
- Location: lines 5566–5579; heading `8. exchange_ts`
- Domain tags: DATA, CLOCK
- Source statement: 8. exchange_ts: Timestamp produit par la source/exchange lorsque disponible. si l’exchange ne fournit pas de timestamp.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `8. exchange_ts` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0020`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0274 — 9. recv_wallclock_ts

- Source: `SRC-005`
- Location: lines 5580–5589; heading `9. recv_wallclock_ts`
- Domain tags: CLOCK
- Source statement: 9. recv_wallclock_ts: Sous réserve de qualité de synchronisation.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `9. recv_wallclock_ts` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0004`; supporting items: none found by conservative heading match; domain indexes `CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0275 — 10. recv_monotonic_ns

- Source: `SRC-005`
- Location: lines 5590–5599; heading `10. recv_monotonic_ns`
- Domain tags: CLOCK, INFRA
- Source statement: 10. recv_monotonic_ns: C’est la référence des mesures internes.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `10. recv_monotonic_ns` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0005`; supporting items: none found by conservative heading match; domain indexes `CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0276 — 11. Source

- Source: `SRC-005`
- Location: lines 5600–5613; heading `11. Source`
- Domain tags: DATA, REPLAY
- Source statement: 11. Source: Enum : Source {
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `11. Source` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0021`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0277 — 12. Source quality

- Source: `SRC-005`
- Location: lines 5614–5625; heading `12. Source quality`
- Domain tags: DATA, CLOCK, SIMULATOR
- Source statement: 12. Source quality: Chaque event normalisé peut transporter :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `12. Source quality` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0022`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0278 — 13. Normalized MarketEvent

- Source: `SRC-005`
- Location: lines 5626–5639; heading `13. Normalized MarketEvent`
- Domain tags: DATA, DEPLOYMENT
- Source statement: 13. Normalized MarketEvent: Enum central : MarketEvent {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `13. Normalized MarketEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0023`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0279 — 14. BookSnapshot

- Source: `SRC-005`
- Location: lines 5640–5660; heading `14. BookSnapshot`
- Domain tags: DATA, SIMULATOR
- Source statement: 14. BookSnapshot: BookSnapshot { market_id,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `14. BookSnapshot` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0024`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0280 — 15. PriceLevel

- Source: `SRC-005`
- Location: lines 5661–5676; heading `15. PriceLevel`
- Domain tags: DATA, SIZING, QUANT
- Source statement: 15. PriceLevel: aux f64 pour la représentation exchange.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `15. PriceLevel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0025`; supporting items: none found by conservative heading match; domain indexes `DATA, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0281 — 16. Pourquoi ticks/lots

- Source: `SRC-005`
- Location: lines 5677–5692; heading `16. Pourquoi ticks/lots`
- Domain tags: DATA, INVENTORY
- Source statement: 16. Pourquoi ticks/lots: 0.1 + 0.2 != 0.3 Les conversions vers f64 sont réservées aux modèles statistiques.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `16. Pourquoi ticks/lots` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0026`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0282 — 17. BookDiff

- Source: `SRC-005`
- Location: lines 5693–5706; heading `17. BookDiff`
- Domain tags: DATA, SIMULATOR
- Source statement: 17. BookDiff: Prévu dès maintenant même si la source spot initiale peut ne pas fournir une granularité L4 suffisante.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `17. BookDiff` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0027`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0283 — 18. TradeEvent

- Source: `SRC-005`
- Location: lines 5707–5729; heading `18. TradeEvent`
- Domain tags: DATA, SIZING, QUANT, PRODUCT
- Source statement: 18. TradeEvent: TradeEvent { trade_id?,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `18. TradeEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0028`; supporting items: none found by conservative heading match; domain indexes `DATA, SIZING, QUANT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0284 — 19. Side

- Source: `SRC-005`
- Location: lines 5730–5744; heading `19. Side`
- Domain tags: DATA, PRODUCT
- Source statement: 19. Side: Enum : Side {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `19. Side` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0029`; supporting items: none found by conservative heading match; domain indexes `DATA, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0285 — 20. MarketId

- Source: `SRC-005`
- Location: lines 5745–5752; heading `20. MarketId`
- Domain tags: DATA
- Source statement: 20. MarketId: Pas une chaîne utilisée partout.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `20. MarketId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0030`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0286 — 21. AssetId

- Source: `SRC-005`
- Location: lines 5753–5759; heading `21. AssetId`
- Domain tags: DATA
- Source statement: 21. AssetId: Même logique : struct AssetId(...)
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `21. AssetId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0031`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0287 — 22. MarketDefinition

- Source: `SRC-005`
- Location: lines 5760–5779; heading `22. MarketDefinition`
- Domain tags: DATA
- Source statement: 22. MarketDefinition: MarketDefinition { market_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `22. MarketDefinition` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0032`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0288 — 23. MetadataVersion

- Source: `SRC-005`
- Location: lines 5780–5787; heading `23. MetadataVersion`
- Domain tags: DATA, EXECUTION, ROUTING
- Source statement: 23. MetadataVersion: Toutes les routes dépendantes savent exactement quelle version elles utilisent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `23. MetadataVersion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0033`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0289 — 24. BookState

- Source: `SRC-005`
- Location: lines 5788–5810; heading `24. BookState`
- Domain tags: DATA, DEPLOYMENT
- Source statement: 24. BookState: Objet local construit à partir des MarketEvents.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `24. BookState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0034`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0290 — 25. BookVersion

- Source: `SRC-005`
- Location: lines 5811–5848; heading `25. BookVersion`
- Domain tags: DATA, RISK
- Source statement: 25. BookVersion: Permet à un RiskSnapshot de référencer précisément :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `25. BookVersion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0035`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0291 — 26. Book invariants

- Source: `SRC-005`
- Location: lines 5849–5862; heading `26. Book invariants`
- Domain tags: DATA, QUANT
- Source statement: 26. Book invariants: hors éventuel état transitoire rejeté.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `26. Book invariants` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0036`; supporting items: none found by conservative heading match; domain indexes `DATA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0292 — 27. Invalid Book

- Source: `SRC-005`
- Location: lines 5863–5870; heading `27. Invalid Book`
- Domain tags: DATA
- Source statement: 27. Invalid Book: Un book invalide devient : On ne tente pas de le corriger silencieusement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `27. Invalid Book` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0037`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0293 — 28. BookSnapshotId

- Source: `SRC-005`
- Location: lines 5871–5878; heading `28. BookSnapshotId`
- Domain tags: DATA
- Source statement: 28. BookSnapshotId: Pour chaque décision importante : permet d’identifier les versions de books utilisées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `28. BookSnapshotId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0038`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0294 — 29. AccountEvent

- Source: `SRC-005`
- Location: lines 5879–5891; heading `29. AccountEvent`
- Domain tags: DATA, EXECUTION, DEPLOYMENT, ACCOUNTING, INVENTORY
- Source statement: 29. AccountEvent: Enum : AccountEvent {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `29. AccountEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0039`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, DEPLOYMENT, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0295 — 30. OrderUpdate

- Source: `SRC-005`
- Location: lines 5892–5912; heading `30. OrderUpdate`
- Domain tags: DATA, DEPLOYMENT, EXECUTION
- Source statement: 30. OrderUpdate: OrderUpdate { cloid?,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `30. OrderUpdate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0040`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0296 — 31. FillEvent

- Source: `SRC-005`
- Location: lines 5913–5937; heading `31. FillEvent`
- Domain tags: DATA, EXECUTION, ACCOUNTING
- Source statement: 31. FillEvent: FillEvent { fill_id,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `31. FillEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0041`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0297 — 32. FillId

- Source: `SRC-005`
- Location: lines 5938–5952; heading `32. FillId`
- Domain tags: DATA, EXECUTION, RECONCILIATION
- Source statement: 32. FillId: Même fill reçu par :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `32. FillId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0042`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0298 — 33. Balance

- Source: `SRC-005`
- Location: lines 5953–5990; heading `33. Balance`
- Domain tags: DATA, INVENTORY
- Source statement: 33. Balance: AssetBalance { asset_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `33. Balance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0043`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0299 — 34. AccountState

- Source: `SRC-005`
- Location: lines 5991–6006; heading `34. AccountState`
- Domain tags: DATA, EXECUTION, RECONCILIATION, ACCOUNTING, INVENTORY
- Source statement: 34. AccountState: AccountState { balances,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `34. AccountState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0044`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECONCILIATION, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0300 — 35. AccountVersion

- Source: `SRC-005`
- Location: lines 6007–6013; heading `35. AccountVersion`
- Domain tags: DATA
- Source statement: 35. AccountVersion: Chaque changement économique réel :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `35. AccountVersion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0045`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0301 — 36. InventoryState

- Source: `SRC-005`
- Location: lines 6014–6031; heading `36. InventoryState`
- Domain tags: DATA, INVENTORY
- Source statement: 36. InventoryState: Séparé du simple wallet. InventoryState {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `36. InventoryState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0046`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0302 — 37. AssetClassification

- Source: `SRC-005`
- Location: lines 6032–6042; heading `37. AssetClassification`
- Domain tags: DATA, INVENTORY, ARCH
- Source statement: 37. AssetClassification: Enum : AssetClass {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `37. AssetClassification` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0047`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0303 — 38. InventoryPosition

- Source: `SRC-005`
- Location: lines 6043–6060; heading `38. InventoryPosition`
- Domain tags: DATA, INVENTORY, SIZING, QUANT
- Source statement: 38. InventoryPosition: InventoryPosition { asset_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `38. InventoryPosition` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0048`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY, SIZING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0304 — 39. ReservationState

- Source: `SRC-005`
- Location: lines 6061–6072; heading `39. ReservationState`
- Domain tags: DATA, RISK, INVENTORY
- Source statement: 39. ReservationState: ReservationState { balance_reservations,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `39. ReservationState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0049`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0305 — 40. BalanceReservation

- Source: `SRC-005`
- Location: lines 6073–6087; heading `40. BalanceReservation`
- Domain tags: DATA, INVENTORY
- Source statement: 40. BalanceReservation: BalanceReservation { reservation_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `40. BalanceReservation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0050`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0306 — 41. BookCapacityReservation

- Source: `SRC-005`
- Location: lines 6088–6104; heading `41. BookCapacityReservation`
- Domain tags: DATA, CAPITAL
- Source statement: 41. BookCapacityReservation: BookCapacityReservation { reservation_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `41. BookCapacityReservation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0051`; supporting items: none found by conservative heading match; domain indexes `DATA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0307 — 42. Pourquoi book_version

- Source: `SRC-005`
- Location: lines 6105–6117; heading `42. Pourquoi book_version`
- Domain tags: DATA, VALIDATION, PRODUCT
- Source statement: 42. Pourquoi book_version: Une réservation calculée sur : ne doit pas être considérée automatiquement valide après :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `42. Pourquoi book_version` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0052`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0308 — 43. RouteDefinition

- Source: `SRC-005`
- Location: lines 6118–6137; heading `43. RouteDefinition`
- Domain tags: DATA, ROUTING
- Source statement: 43. RouteDefinition: Objet statique pré-calculé. RouteDefinition {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `43. RouteDefinition` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0053`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0309 — 44. RouteType

- Source: `SRC-005`
- Location: lines 6138–6149; heading `44. RouteType`
- Domain tags: DATA, ROUTING, RECOVERY, BRIDGE, TRIANGLE
- Source statement: 44. RouteType: RouteType { Direct,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `44. RouteType` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0054`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING, RECOVERY, BRIDGE, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0310 — 45. RouteLeg

- Source: `SRC-005`
- Location: lines 6150–6162; heading `45. RouteLeg`
- Domain tags: DATA, ROUTING
- Source statement: 45. RouteLeg: RouteLeg { market_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `45. RouteLeg` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0055`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0311 — 46. ConversionDirection

- Source: `SRC-005`
- Location: lines 6163–6177; heading `46. ConversionDirection`
- Domain tags: DATA, PRODUCT
- Source statement: 46. ConversionDirection: Ne pas stocker seulement : Ça réduit les erreurs de sens.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `46. ConversionDirection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0056`; supporting items: none found by conservative heading match; domain indexes `DATA, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0312 — 47. RouteDependencies

- Source: `SRC-005`
- Location: lines 6178–6188; heading `47. RouteDependencies`
- Domain tags: DATA, ROUTING
- Source statement: 47. RouteDependencies: RouteDependencies { markets[],
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `47. RouteDependencies` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0057`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0313 — 48. pair_to_routes

- Source: `SRC-005`
- Location: lines 6189–6197; heading `48. pair_to_routes`
- Domain tags: DATA, ROUTING, GRAPH, DETERMINISM, DEPLOYMENT
- Source statement: 48. pair_to_routes: Chaque market update ne recalcule que les routes affectées.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `48. pair_to_routes` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0058`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING, GRAPH, DETERMINISM, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0314 — 49. Opportunity

- Source: `SRC-005`
- Location: lines 6198–6223; heading `49. Opportunity`
- Domain tags: DATA, ACCOUNTING, ROUTING
- Source statement: 49. Opportunity: Objet éphémère produit par Strategy.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `49. Opportunity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0059`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0315 — 50. Opportunity ≠ ExecutionPlan

- Source: `SRC-005`
- Location: lines 6224–6236; heading `50. Opportunity ≠ ExecutionPlan`
- Domain tags: DATA
- Source statement: 50. Opportunity ≠ ExecutionPlan: Une opportunity est : une possibilité économique
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `50. Opportunity ≠ ExecutionPlan` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0060`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0316 — 51. OpportunityId

- Source: `SRC-005`
- Location: lines 6237–6247; heading `51. OpportunityId`
- Domain tags: DATA
- Source statement: 51. OpportunityId: Unique par apparition/episode. Permet :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `51. OpportunityId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0061`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0317 — 52. OpportunityEpisode

- Source: `SRC-005`
- Location: lines 6248–6275; heading `52. OpportunityEpisode`
- Domain tags: DATA, ROUTING, RESEARCH
- Source statement: 52. OpportunityEpisode: Pour recherche : OpportunityEpisode {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `52. OpportunityEpisode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0062`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0318 — 53. FeatureSnapshot

- Source: `SRC-005`
- Location: lines 6276–6295; heading `53. FeatureSnapshot`
- Domain tags: DATA, CLOCK, MICROSTRUCTURE, INVENTORY, ROUTING, QUANT
- Source statement: 53. FeatureSnapshot: Objet immutable contenant les features quantitatives utilisées.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `53. FeatureSnapshot` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0063`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, MICROSTRUCTURE, INVENTORY, ROUTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0319 — 54. Pourquoi immutable

- Source: `SRC-005`
- Location: lines 6296–6304; heading `54. Pourquoi immutable`
- Domain tags: DATA
- Source statement: 54. Pourquoi immutable: On veut pouvoir répondre : quelles features exactes le modèle a-t-il vues ?
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `54. Pourquoi immutable` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0064`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0320 — 55. ModelForecast

- Source: `SRC-005`
- Location: lines 6305–6324; heading `55. ModelForecast`
- Domain tags: DATA, ARCH
- Source statement: 55. ModelForecast: Interface générique : ModelForecast {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `55. ModelForecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0065`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0321 — 56. EdgeSurvivalForecast

- Source: `SRC-005`
- Location: lines 6325–6341; heading `56. EdgeSurvivalForecast`
- Domain tags: DATA, SURVIVAL, QUANT
- Source statement: 56. EdgeSurvivalForecast: EdgeSurvivalForecast { p_survive_horizons[],
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `56. EdgeSurvivalForecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0066`; supporting items: none found by conservative heading match; domain indexes `DATA, SURVIVAL, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0322 — 57. LiquidityForecast

- Source: `SRC-005`
- Location: lines 6342–6359; heading `57. LiquidityForecast`
- Domain tags: DATA, LIQUIDITY_RESPONSE, QUANT
- Source statement: 57. LiquidityForecast: LiquidityForecast { expected_depth_arrival,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `57. LiquidityForecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0067`; supporting items: none found by conservative heading match; domain indexes `DATA, LIQUIDITY_RESPONSE, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0323 — 58. MakerForecast

- Source: `SRC-005`
- Location: lines 6360–6375; heading `58. MakerForecast`
- Domain tags: DATA, EXECUTION, QUANT
- Source statement: 58. MakerForecast: MakerForecast { fill_probability_by_horizon,
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `58. MakerForecast` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0068`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0324 — 59. CrossMarketForecast

- Source: `SRC-005`
- Location: lines 6376–6387; heading `59. CrossMarketForecast`
- Domain tags: DATA, CROSS_MARKET
- Source statement: 59. CrossMarketForecast: CrossMarketForecast { source_market,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `59. CrossMarketForecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0069`; supporting items: none found by conservative heading match; domain indexes `DATA, CROSS_MARKET`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0325 — 60. ResponseForecast

- Source: `SRC-005`
- Location: lines 6388–6403; heading `60. ResponseForecast`
- Domain tags: DATA, QUANT
- Source statement: 60. ResponseForecast: ResponseForecast { target_market,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `60. ResponseForecast` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0070`; supporting items: none found by conservative heading match; domain indexes `DATA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0326 — 61. ExecutionForecast

- Source: `SRC-005`
- Location: lines 6404–6432; heading `61. ExecutionForecast`
- Domain tags: DATA, EXECUTION, RECOVERY, ACCOUNTING, SIMULATOR, QUANT
- Source statement: 61. ExecutionForecast: Objet consolidé du Simulator. ExecutionForecast {
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `61. ExecutionForecast` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0071`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECOVERY, ACCOUNTING, SIMULATOR, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0327 — 62. RiskSnapshot

- Source: `SRC-005`
- Location: lines 6433–6455; heading `62. RiskSnapshot`
- Domain tags: DATA, RISK, INFRA, INVENTORY
- Source statement: 62. RiskSnapshot: Immutable. RiskSnapshot {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `62. RiskSnapshot` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0072`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, INFRA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0328 — 63. RiskDecision

- Source: `SRC-005`
- Location: lines 6456–6478; heading `63. RiskDecision`
- Domain tags: DATA, RISK
- Source statement: 63. RiskDecision: RiskDecision { decision_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `63. RiskDecision` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0073`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0329 — 64. ExecutionPlan

- Source: `SRC-005`
- Location: lines 6479–6508; heading `64. ExecutionPlan`
- Domain tags: DATA, RISK, ROUTING
- Source statement: 64. ExecutionPlan: Après RiskDecision favorable. ExecutionPlan {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `64. ExecutionPlan` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0074`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0330 — 65. ExecutionPlan immutability

- Source: `SRC-005`
- Location: lines 6509–6522; heading `65. ExecutionPlan immutability`
- Domain tags: DATA, FUTURE
- Source statement: 65. ExecutionPlan immutability: les champs économiques sont immutables.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `65. ExecutionPlan immutability` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0075`; supporting items: none found by conservative heading match; domain indexes `DATA, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0331 — 66. ExecutionMode

- Source: `SRC-005`
- Location: lines 6523–6536; heading `66. ExecutionMode`
- Domain tags: DATA, TRIANGLE
- Source statement: 66. ExecutionMode: Les modes désactivés restent représentables.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `66. ExecutionMode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0076`; supporting items: none found by conservative heading match; domain indexes `DATA, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0332 — 67. ExecutionLegPlan

- Source: `SRC-005`
- Location: lines 6537–6560; heading `67. ExecutionLegPlan`
- Domain tags: DATA
- Source statement: 67. ExecutionLegPlan: ExecutionLegPlan { leg_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `67. ExecutionLegPlan` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0077`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0333 — 68. Role

- Source: `SRC-005`
- Location: lines 6561–6571; heading `68. Role`
- Domain tags: DATA, RECOVERY, INVENTORY
- Source statement: 68. Role: LegRole { Primary,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `68. Role` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0078`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0334 — 69. OrderPolicy

- Source: `SRC-005`
- Location: lines 6572–6582; heading `69. OrderPolicy`
- Domain tags: DATA
- Source statement: 69. OrderPolicy: OrderPolicy { liquidity_role,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `69. OrderPolicy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0079`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0335 — 70. OrderIntent

- Source: `SRC-005`
- Location: lines 6583–6609; heading `70. OrderIntent`
- Domain tags: DATA, EXECUTION, RISK
- Source statement: 70. OrderIntent: Déjà vu en Dossier 1, mais schema figé ici.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `70. OrderIntent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0080`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0336 — 71. OrderIntent lifecycle

- Source: `SRC-005`
- Location: lines 6610–6618; heading `71. OrderIntent lifecycle`
- Domain tags: DATA, ROUTING, EXECUTION
- Source statement: 71. OrderIntent lifecycle: nonce peut être ajouté au moment approprié.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `71. OrderIntent lifecycle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0081`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0337 — 72. SignedOrderIntent

- Source: `SRC-005`
- Location: lines 6619–6631; heading `72. SignedOrderIntent`
- Domain tags: DATA, EXECUTION
- Source statement: 72. SignedOrderIntent: SignedOrderIntent { intent,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `72. SignedOrderIntent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0082`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0338 — 73. TransportRequest

- Source: `SRC-005`
- Location: lines 6632–6646; heading `73. TransportRequest`
- Domain tags: DATA
- Source statement: 73. TransportRequest: Séparé : TransportRequest {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `73. TransportRequest` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0083`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0339 — 74. Pourquoi séparer transport

- Source: `SRC-005`
- Location: lines 6647–6655; heading `74. Pourquoi séparer transport`
- Domain tags: DATA, SIMULATOR, REPLAY
- Source statement: 74. Pourquoi séparer transport: Le moteur ne doit pas savoir si l’ordre part via :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `74. Pourquoi séparer transport` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0084`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0340 — 75. ExecutionTransport trait

- Source: `SRC-005`
- Location: lines 6656–6675; heading `75. ExecutionTransport trait`
- Domain tags: DATA, EXECUTION, VALIDATION, REPLAY, RESEARCH
- Source statement: 75. ExecutionTransport trait: Conceptuellement : trait ExecutionTransport {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `75. ExecutionTransport trait` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0085`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, VALIDATION, REPLAY, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0341 — 76. NullShadowTransport

- Source: `SRC-005`
- Location: lines 6676–6689; heading `76. NullShadowTransport`
- Domain tags: DATA, VALIDATION
- Source statement: 76. NullShadowTransport: En Shadow : submit(intent)
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `76. NullShadowTransport` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0086`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0342 — 77. ReplayTransport

- Source: `SRC-005`
- Location: lines 6690–6708; heading `77. ReplayTransport`
- Domain tags: REPLAY, EXECUTION, DATA
- Source statement: 77. ReplayTransport: et le passe au : dans le même schema que Live.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `77. ReplayTransport` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0007`; supporting items: none found by conservative heading match; domain indexes `REPLAY, EXECUTION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0343 — 78. Principe majeur

- Source: `SRC-005`
- Location: lines 6709–6726; heading `78. Principe majeur`
- Domain tags: DATA, EXECUTION, REPLAY, ARCH
- Source statement: 78. Principe majeur: Le Core Engine ne doit pas savoir si :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `78. Principe majeur` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0087`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0344 — 79. EngineInputEvent

- Source: `SRC-005`
- Location: lines 6727–6739; heading `79. EngineInputEvent`
- Domain tags: DATA, INFRA
- Source statement: 79. EngineInputEvent: Union centrale : EngineInputEvent {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `79. EngineInputEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0088`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0345 — 80. InfraEvent

- Source: `SRC-005`
- Location: lines 6740–6751; heading `80. InfraEvent`
- Domain tags: DATA, INFRA, RECORDER, CLOCK, DEPLOYMENT, OPERATIONS, ACCOUNTING
- Source statement: 80. InfraEvent: InfraEvent { ClockUpdate,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `80. InfraEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0089`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, RECORDER, CLOCK, DEPLOYMENT, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0346 — 81. TimerEvent

- Source: `SRC-005`
- Location: lines 6752–6764; heading `81. TimerEvent`
- Domain tags: DATA, EXECUTION, RECOVERY, RECONCILIATION, RISK, REPLAY
- Source statement: 81. TimerEvent: Timers explicitement enregistrables en Replay.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `81. TimerEvent` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0090`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECOVERY, RECONCILIATION, RISK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0347 — 82. Pourquoi timers comme événements

- Source: `SRC-005`
- Location: lines 6765–6781; heading `82. Pourquoi timers comme événements`
- Domain tags: DATA, DETERMINISM, BENCHMARK, REPLAY
- Source statement: 82. Pourquoi timers comme événements: Sinon Replay peut diverger : En transformant les timers stratégiques en événements déterministes :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `82. Pourquoi timers comme événements` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0091`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM, BENCHMARK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0348 — 83. ControlEvent

- Source: `SRC-005`
- Location: lines 6782–6794; heading `83. ControlEvent`
- Domain tags: DATA, RISK, DEPLOYMENT
- Source statement: 83. ControlEvent: ControlEvent { Start,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `83. ControlEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0092`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0349 — 84. DecisionEvent

- Source: `SRC-005`
- Location: lines 6795–6810; heading `84. DecisionEvent`
- Domain tags: DATA, RECOVERY, RISK
- Source statement: 84. DecisionEvent: Toute décision interne importante produit :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `84. DecisionEvent` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0093`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0350 — 85. RejectEvent

- Source: `SRC-005`
- Location: lines 6811–6826; heading `85. RejectEvent`
- Domain tags: DATA, CLOCK, ROUTING
- Source statement: 85. RejectEvent: RejectEvent { opportunity_id?,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `85. RejectEvent` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0094`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0351 — 86. RejectReason

- Source: `SRC-005`
- Location: lines 6827–6842; heading `86. RejectReason`
- Domain tags: DATA, RECONCILIATION, RISK, INFRA, ACCOUNTING, INVENTORY
- Source statement: 86. RejectReason: Enum fermé/versionné. Familles :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `86. RejectReason` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0095`; supporting items: none found by conservative heading match; domain indexes `DATA, RECONCILIATION, RISK, INFRA, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0352 — 87. Pourquoi enum versionné

- Source: `SRC-005`
- Location: lines 6843–6857; heading `87. Pourquoi enum versionné`
- Domain tags: DATA, RISK
- Source statement: 87. Pourquoi enum versionné: On doit pouvoir agréger : Pas des chaînes légèrement différentes :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `87. Pourquoi enum versionné` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0096`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0353 — 88. InfraState

- Source: `SRC-005`
- Location: lines 6858–6881; heading `88. InfraState`
- Domain tags: DATA, INFRA, RECORDER, CLOCK, BENCHMARK, OPERATIONS, ACCOUNTING, PRODUCT
- Source statement: 88. InfraState: InfraState { clock_health,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `88. InfraState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0097`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, RECORDER, CLOCK, BENCHMARK, OPERATIONS, ACCOUNTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0354 — 89. InfraStateVersion

- Source: `SRC-005`
- Location: lines 6882–6889; heading `89. InfraStateVersion`
- Domain tags: DATA, INFRA, RISK
- Source statement: 89. InfraStateVersion: Chaque changement significatif : version += 1
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `89. InfraStateVersion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0098`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0355 — 90. ConfigVersion

- Source: `SRC-005`
- Location: lines 6890–6902; heading `90. ConfigVersion`
- Domain tags: DATA, EXECUTION, DETERMINISM
- Source statement: 90. ConfigVersion: Tous les fichiers de config aboutissent à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `90. ConfigVersion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0099`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0356 — 91. ResolvedConfig

- Source: `SRC-005`
- Location: lines 6903–6918; heading `91. ResolvedConfig`
- Domain tags: DATA, VALIDATION
- Source statement: 91. ResolvedConfig: Pas la config brute utilisateur. C’est cette config exacte qui est enregistrée avec les runs.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `91. ResolvedConfig` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0100`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0357 — 92. Pas de configuration implicite

- Source: `SRC-005`
- Location: lines 6919–6932; heading `92. Pas de configuration implicite`
- Domain tags: DATA
- Source statement: 92. Pas de configuration implicite: Toutes les valeurs déterminant une décision doivent provenir de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `92. Pas de configuration implicite` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0101`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0358 — 93. RunManifest

- Source: `SRC-005`
- Location: lines 6933–6959; heading `93. RunManifest`
- Domain tags: DATA, CLOCK, DETERMINISM
- Source statement: 93. RunManifest: Chaque session : RunManifest {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `93. RunManifest` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0102`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0359 — 94. RunMode

- Source: `SRC-005`
- Location: lines 6960–6971; heading `94. RunMode`
- Domain tags: DATA, VALIDATION, REPLAY, RESEARCH
- Source statement: 94. RunMode: RunMode { Replay,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `94. RunMode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0103`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION, REPLAY, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0360 — 95. RunMode cannot alter strategy logic

- Source: `SRC-005`
- Location: lines 6972–6995; heading `95. RunMode cannot alter strategy logic`
- Domain tags: DATA, EXECUTION, REPLAY
- Source statement: 95. RunMode cannot alter strategy logic: if mode == Replay { if mode == Live {
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `95. RunMode cannot alter strategy logic` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0104`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0361 — 96. Replay exactness principle

- Source: `SRC-005`
- Location: lines 6996–7034; heading `96. Replay exactness principle`
- Domain tags: REPLAY, CLOCK
- Source statement: 96. Replay exactness principle: Pour un run déterministe : Output = F( Events, Config, Models, Seed )
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `96. Replay exactness principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0008`; supporting items: none found by conservative heading match; domain indexes `REPLAY, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0362 — 97. Determinism identity

- Source: `SRC-005`
- Location: lines 7035–7075; heading `97. Determinism identity`
- Domain tags: DETERMINISM, EXECUTION, CLOCK
- Source statement: 97. Determinism identity: Si : Events_A = Events_B
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `97. Determinism identity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0001`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, EXECUTION, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0363 — 98. DecisionTrace

- Source: `SRC-005`
- Location: lines 7076–7086; heading `98. DecisionTrace`
- Domain tags: DATA, RISK
- Source statement: 98. DecisionTrace: DecisionTrace { ordered_decisions[],
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `98. DecisionTrace` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0105`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0364 — 99. Deterministic ordering

- Source: `SRC-005`
- Location: lines 7087–7097; heading `99. Deterministic ordering`
- Domain tags: DETERMINISM, EXECUTION, RECORDER, REPLAY
- Source statement: 99. Deterministic ordering: Tous les événements concurrents passent par une règle d’ordre explicite. 2. source priority if equal
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `99. Deterministic ordering` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0002`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, EXECUTION, RECORDER, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0365 — 100. Pourquoi ordre explicite

- Source: `SRC-005`
- Location: lines 7098–7112; heading `100. Pourquoi ordre explicite`
- Domain tags: DATA, REPLAY
- Source statement: 100. Pourquoi ordre explicite: doivent toujours être appliqués dans le même ordre en Replay.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `100. Pourquoi ordre explicite` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0106`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0366 — 101. EventTime vs ReceiveTime

- Source: `SRC-005`
- Location: lines 7113–7132; heading `101. EventTime vs ReceiveTime`
- Domain tags: DATA, REPLAY, RESEARCH
- Source statement: 101. EventTime vs ReceiveTime: what the bot actually knew when Pour simuler le bot réel :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `101. EventTime vs ReceiveTime` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0107`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0367 — 102. No Look-Ahead

- Source: `SRC-005`
- Location: lines 7133–7169; heading `102. No Look-Ahead`
- Domain tags: DATA, REPLAY
- Source statement: 102. No Look-Ahead: Le moteur Replay n’a jamais accès à un événement dont :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `102. No Look-Ahead` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0108`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0369 — EXACT RECEIVE-TIME

- Source: `SRC-005`
- Location: lines 7171–7179; heading `EXACT RECEIVE-TIME`
- Domain tags: DATA
- Source statement: EXACT RECEIVE-TIME: Utilisé pour reproduire le bot.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `EXACT RECEIVE-TIME` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0109`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0370 — ACCELERATED

- Source: `SRC-005`
- Location: lines 7180–7184; heading `ACCELERATED`
- Domain tags: REPLAY
- Source statement: ACCELERATED: La logique temporelle conserve les intervalles relatifs.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `ACCELERATED` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0009`; supporting items: none found by conservative heading match; domain indexes `REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0371 — COUNTERFACTUAL LATENCY

- Source: `SRC-005`
- Location: lines 7185–7188; heading `COUNTERFACTUAL LATENCY`
- Domain tags: DATA, INFRA, SIMULATOR, ROUTING
- Source statement: COUNTERFACTUAL LATENCY: Les événements marché restent historiques. Les timings de notre propre execution path sont modifiés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `COUNTERFACTUAL LATENCY` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0110`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, SIMULATOR, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0372 — INTERACTIVE

- Source: `SRC-005`
- Location: lines 7189–7191; heading `INTERACTIVE`
- Domain tags: DATA, SIMULATOR
- Source statement: INTERACTIVE: Le Simulator modifie également certaines réponses du marché.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `INTERACTIVE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0111`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0373 — 104. Replay clock

- Source: `SRC-005`
- Location: lines 7192–7204; heading `104. Replay clock`
- Domain tags: CLOCK, REPLAY, ARCH
- Source statement: 104. Replay clock: On ne doit jamais utiliser directement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `104. Replay clock` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0006`; supporting items: none found by conservative heading match; domain indexes `CLOCK, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0374 — 105. Clock implementations

- Source: `SRC-005`
- Location: lines 7205–7212; heading `105. Clock implementations`
- Domain tags: CLOCK, REPLAY
- Source statement: 105. Clock implementations: LiveClock ReplayClock
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `105. Clock implementations` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0007`; supporting items: none found by conservative heading match; domain indexes `CLOCK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0375 — 106. Why Clock abstraction

- Source: `SRC-005`
- Location: lines 7213–7222; heading `106. Why Clock abstraction`
- Domain tags: CLOCK, EXECUTION, RISK, REPLAY
- Source statement: 106. Why Clock abstraction: diffèrent entre Replay et Live.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `106. Why Clock abstraction` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0008`; supporting items: none found by conservative heading match; domain indexes `CLOCK, EXECUTION, RISK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0376 — 107. RNG abstraction

- Source: `SRC-005`
- Location: lines 7223–7229; heading `107. RNG abstraction`
- Domain tags: CLOCK, INFRA
- Source statement: 107. RNG abstraction: Même logique pour l’aléatoire. RngProvider
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `107. RNG abstraction` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0009`; supporting items: none found by conservative heading match; domain indexes `CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0377 — 108. Replay RNG

- Source: `SRC-005`
- Location: lines 7230–7236; heading `108. Replay RNG`
- Domain tags: CLOCK, REPLAY, DATA
- Source statement: 108. Replay RNG: Seed fixé dans : RunManifest
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `108. Replay RNG` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0010`; supporting items: none found by conservative heading match; domain indexes `CLOCK, REPLAY, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0378 — 109. Live RNG

- Source: `SRC-005`
- Location: lines 7237–7240; heading `109. Live RNG`
- Domain tags: CLOCK
- Source statement: 109. Live RNG: Peut utiliser une source appropriée. Mais toute décision stochastique importante doit être enregistrée pour audit.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `109. Live RNG` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0011`; supporting items: none found by conservative heading match; domain indexes `CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0379 — 110. De préférence : peu de stochasticité live

- Source: `SRC-005`
- Location: lines 7241–7251; heading `110. De préférence : peu de stochasticité live`
- Domain tags: DATA, DETERMINISM, SIMULATOR, QUANT, PRODUCT
- Source statement: 110. De préférence : peu de stochasticité live: Le live doit idéalement consommer : plutôt que prendre aléatoirement une décision.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `110. De préférence : peu de stochasticité live` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0112`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM, SIMULATOR, QUANT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0380 — 111. Model interface

- Source: `SRC-005`
- Location: lines 7252–7261; heading `111. Model interface`
- Domain tags: DATA, ARCH, ROUTING, HOT_WARM_COLD
- Source statement: 111. Model interface: fn predict(&self, input: &I) -> O; Pas de réseau externe dans le hot path.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `111. Model interface` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0113`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0381 — 112. Model inputs immutable

- Source: `SRC-005`
- Location: lines 7262–7269; heading `112. Model inputs immutable`
- Domain tags: DATA
- Source statement: 112. Model inputs immutable: pas des références à un state mutable qui peut changer pendant l’inférence.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `112. Model inputs immutable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0114`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0382 — 113. ModelVersion

- Source: `SRC-005`
- Location: lines 7270–7281; heading `113. ModelVersion`
- Domain tags: DATA, DETERMINISM
- Source statement: 113. ModelVersion: ModelVersion { model_id,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `113. ModelVersion` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0115`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0383 — 114. FeatureSchemaVersion

- Source: `SRC-005`
- Location: lines 7282–7294; heading `114. FeatureSchemaVersion`
- Domain tags: DATA, MICROSTRUCTURE, PRODUCT, FUTURE
- Source statement: 114. FeatureSchemaVersion: Un modèle entraîné sur : ne peut pas consommer silencieusement :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `114. FeatureSchemaVersion` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0116`; supporting items: none found by conservative heading match; domain indexes `DATA, MICROSTRUCTURE, PRODUCT, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0384 — 115. FormulaSchemaVersion

- Source: `SRC-005`
- Location: lines 7295–7308; heading `115. FormulaSchemaVersion`
- Domain tags: DATA, FORMULA, ACCOUNTING, ROUTING, PRODUCT
- Source statement: 115. FormulaSchemaVersion: Même chose pour les formules. Si logique fee/rounding change :
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `115. FormulaSchemaVersion` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0117`; supporting items: none found by conservative heading match; domain indexes `DATA, FORMULA, ACCOUNTING, ROUTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0385 — 116. DatasetId

- Source: `SRC-005`
- Location: lines 7309–7323; heading `116. DatasetId`
- Domain tags: DATA, RESEARCH
- Source statement: 116. DatasetId: Chaque dataset de recherche est identifié.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `116. DatasetId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0118`; supporting items: none found by conservative heading match; domain indexes `DATA, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0386 — 117. GoldenDataset

- Source: `SRC-005`
- Location: lines 7324–7333; heading `117. GoldenDataset`
- Domain tags: DATA, DETERMINISM, REPLAY, QUANT, ARCH
- Source statement: 117. GoldenDataset: Subset petit, permanent, fortement vérifié.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `117. GoldenDataset` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0119`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM, REPLAY, QUANT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0387 — 118. Data partitions

- Source: `SRC-005`
- Location: lines 7334–7353; heading `118. Data partitions`
- Domain tags: DATA
- Source statement: 118. Data partitions: Normalisé : market
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `118. Data partitions` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0120`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0388 — 119. Raw manifest

- Source: `SRC-005`
- Location: lines 7354–7372; heading `119. Raw manifest`
- Domain tags: DATA, RECORDER
- Source statement: 119. Raw manifest: Chaque chunk : RawChunkManifest {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `119. Raw manifest` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0121`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0389 — 120. Checksum

- Source: `SRC-005`
- Location: lines 7373–7380; heading `120. Checksum`
- Domain tags: DATA, RECORDER, GRAPH
- Source statement: 120. Checksum: Chaque chunk fermé possède :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `120. Checksum` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0122`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0390 — 121. Immutable RAW

- Source: `SRC-005`
- Location: lines 7381–7393; heading `121. Immutable RAW`
- Domain tags: DATA, FUTURE
- Source statement: 121. Immutable RAW: Une correction de normalization ne réécrit pas RAW.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `121. Immutable RAW` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0123`; supporting items: none found by conservative heading match; domain indexes `DATA, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0391 — 122. Normalization schema

- Source: `SRC-005`
- Location: lines 7394–7404; heading `122. Normalization schema`
- Domain tags: DATA
- Source statement: 122. Normalization schema: NormalizedEvent { normalized_schema_version,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `122. Normalization schema` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0124`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0392 — 123. Recorder thread

- Source: `SRC-005`
- Location: lines 7405–7419; heading `123. Recorder thread`
- Domain tags: RECORDER, EXECUTION, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 123. Recorder thread: Le Recorder reçoit des copies/références des événements via : Le Core ne fait pas :
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `123. Recorder thread` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REC-0009`; supporting items: none found by conservative heading match; domain indexes `RECORDER, EXECUTION, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0393 — 124. Recorder priority

- Source: `SRC-005`
- Location: lines 7420–7436; heading `124. Recorder priority`
- Domain tags: RECORDER, EXECUTION
- Source statement: 124. Recorder priority: fills / account / execution
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `124. Recorder priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REC-0010`; supporting items: SRC-006-ITEM-0406; domain indexes `RECORDER, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0394 — 125. Backpressure policy

- Source: `SRC-005`
- Location: lines 7437–7450; heading `125. Backpressure policy`
- Domain tags: DATA, EXECUTION, RECORDER, OPERATIONS, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 125. Backpressure policy: never silently block hot path On applique une politique explicite :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `125. Backpressure policy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0125`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECORDER, OPERATIONS, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0395 — 126. Event completeness metrics

- Source: `SRC-005`
- Location: lines 7451–7460; heading `126. Event completeness metrics`
- Domain tags: DATA, EXECUTION, RECORDER
- Source statement: 126. Event completeness metrics: Recorder mesure : events_received
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `126. Event completeness metrics` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0126`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0396 — 127. Dataset quality contract

- Source: `SRC-005`
- Location: lines 7461–7470; heading `127. Dataset quality contract`
- Domain tags: DATA, CLOCK, RESEARCH
- Source statement: 127. Dataset quality contract: Un run Research doit connaître :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `127. Dataset quality contract` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0127`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0397 — 128. Invalid dataset regions

- Source: `SRC-005`
- Location: lines 7471–7490; heading `128. Invalid dataset regions`
- Domain tags: DATA, CLOCK, ACCOUNTING, SIMULATOR, REPLAY
- Source statement: 128. Invalid dataset regions: Une plage avec : feed gap
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `128. Invalid dataset regions` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0128`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK, ACCOUNTING, SIMULATOR, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0398 — 129. Account data priority

- Source: `SRC-005`
- Location: lines 7491–7500; heading `129. Account data priority`
- Domain tags: DATA, EXECUTION, INVENTORY
- Source statement: 129. Account data priority: Même si on doit jeter du market RAW : ne doivent pas être jetés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `129. Account data priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0129`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0399 — 130. ExecutionJournal

- Source: `SRC-005`
- Location: lines 7501–7515; heading `130. ExecutionJournal`
- Domain tags: DATA, CLOCK
- Source statement: 130. ExecutionJournal: Append-only. ExecutionJournalEvent {
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `130. ExecutionJournal` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0130`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0400 — 131. Journal events

- Source: `SRC-005`
- Location: lines 7516–7528; heading `131. Journal events`
- Domain tags: DATA, EXECUTION, RECOVERY
- Source statement: 131. Journal events: ExecutionCreated ReservationCreated
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `131. Journal events` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0131`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0401 — 132. Journal replay

- Source: `SRC-005`
- Location: lines 7529–7537; heading `132. Journal replay`
- Domain tags: DATA, REPLAY, RECONCILIATION
- Source statement: 132. Journal replay: Le state d’exécution doit pouvoir être reconstruit depuis :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `132. Journal replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0132`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0402 — 133. EventReducer

- Source: `SRC-005`
- Location: lines 7538–7546; heading `133. EventReducer`
- Domain tags: DATA
- Source statement: 133. EventReducer: Élément clé. State_{n+1}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `133. EventReducer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0133`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0403 — 134. Reducer purity

- Source: `SRC-005`
- Location: lines 7547–7567; heading `134. Reducer purity`
- Domain tags: DATA
- Source statement: 134. Reducer purity: Autant que possible : no network
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `134. Reducer purity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0134`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0404 — 135. Effects

- Source: `SRC-005`
- Location: lines 7568–7580; heading `135. Effects`
- Domain tags: DATA, EXECUTION, RECONCILIATION
- Source statement: 135. Effects: Le reducer peut produire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `135. Effects` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0135`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0405 — 136. Effect executor

- Source: `SRC-005`
- Location: lines 7581–7589; heading `136. Effect executor`
- Domain tags: DATA, REPLAY
- Source statement: 136. Effect executor: Séparé du reducer. Cela rend :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `136. Effect executor` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0136`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0406 — 137. Example

- Source: `SRC-005`
- Location: lines 7590–7602; heading `137. Example`
- Domain tags: DATA, EXECUTION, INVENTORY, ROUTING
- Source statement: 137. Example: FillEvent Reducer
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `137. Example` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0137`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0407 — 138. Command/Event separation

- Source: `SRC-005`
- Location: lines 7603–7615; heading `138. Command/Event separation`
- Domain tags: DATA, EXECUTION
- Source statement: 138. Command/Event separation: Ne pas confondre intention et réalité.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `138. Command/Event separation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0138`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0408 — 139. Why

- Source: `SRC-005`
- Location: lines 7616–7633; heading `139. Why`
- Domain tags: DATA, EXECUTION, ARCH
- Source statement: 139. Why: L’architecture doit refléter le monde réel.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `139. Why` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0139`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0409 — 140. State hashes

- Source: `SRC-005`
- Location: lines 7634–7642; heading `140. State hashes`
- Domain tags: DETERMINISM, REPLAY
- Source statement: 140. State hashes: Permet de comparer Replay A/B.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `140. State hashes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0003`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0410 — 141. Determinism test

- Source: `SRC-005`
- Location: lines 7643–7657; heading `141. Determinism test`
- Domain tags: DETERMINISM, DATA, CLOCK
- Source statement: 141. Determinism test: Run deux fois : same dataset
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `141. Determinism test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0004`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0411 — 142. Divergence detector

- Source: `SRC-005`
- Location: lines 7658–7666; heading `142. Divergence detector`
- Domain tags: DATA, DETERMINISM
- Source statement: 142. Divergence detector: Si hashes divergent : first divergent event_seq
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `142. Divergence detector` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0140`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0412 — 143. Python/Rust contracts

- Source: `SRC-005`
- Location: lines 7667–7675; heading `143. Python/Rust contracts`
- Domain tags: DATA, ARCH
- Source statement: 143. Python/Rust contracts: Python ne doit pas réinventer les schemas. sont générées/exportées ou documentées formellement.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `143. Python/Rust contracts` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0141`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0413 — 144. Parquet schemas

- Source: `SRC-005`
- Location: lines 7676–7685; heading `144. Parquet schemas`
- Domain tags: DATA, RECORDER
- Source statement: 144. Parquet schemas: Chaque table possède : schema version
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `144. Parquet schemas` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0142`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0414 — 145. Units mandatory

- Source: `SRC-005`
- Location: lines 7686–7697; heading `145. Units mandatory`
- Domain tags: DATA, INFRA
- Source statement: 145. Units mandatory: Exemple mauvais : latency = 123
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `145. Units mandatory` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0143`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0415 — 146. Naming convention

- Source: `SRC-005`
- Location: lines 7698–7712; heading `146. Naming convention`
- Domain tags: DATA
- Source statement: 146. Naming convention: Suffixes : _ticks
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `146. Naming convention` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0144`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0416 — 147. Never ambiguous money

- Source: `SRC-005`
- Location: lines 7713–7725; heading `147. Never ambiguous money`
- Domain tags: DATA, RECOVERY, ACCOUNTING
- Source statement: 147. Never ambiguous money: Pas : pnl = 4.2
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `147. Never ambiguous money` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0145`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0417 — 148. Numeraire

- Source: `SRC-005`
- Location: lines 7726–7733; heading `148. Numeraire`
- Domain tags: DATA, PORTFOLIO, QUANT
- Source statement: 148. Numeraire: Le portfolio choisit un : probablement USDC dans notre contexte initial.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `148. Numeraire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0146`; supporting items: none found by conservative heading match; domain indexes `DATA, PORTFOLIO, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0418 — 149. EconomicValue

- Source: `SRC-005`
- Location: lines 7734–7743; heading `149. EconomicValue`
- Domain tags: DATA, ACCOUNTING
- Source statement: 149. EconomicValue: Type conceptuel : EconomicValue {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `149. EconomicValue` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0147`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0419 — 150. Conversion timestamp

- Source: `SRC-005`
- Location: lines 7744–7751; heading `150. Conversion timestamp`
- Domain tags: CLOCK, ACCOUNTING
- Source statement: 150. Conversion timestamp: Lorsqu’on convertit un asset PnL en numéraire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `150. Conversion timestamp` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0012`; supporting items: none found by conservative heading match; domain indexes `CLOCK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0420 — 151. PnL schema

- Source: `SRC-005`
- Location: lines 7752–7766; heading `151. PnL schema`
- Domain tags: DATA, ACCOUNTING, RECOVERY, INFRA, INVENTORY, BRIDGE, ROUTING
- Source statement: 151. PnL schema: PnLBreakdown { route_pnl,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `151. PnL schema` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0148`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, RECOVERY, INFRA, INVENTORY, BRIDGE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0421 — 152. No double accounting

- Source: `SRC-005`
- Location: lines 7767–7785; heading `152. No double accounting`
- Domain tags: DATA, ACCOUNTING, ROUTING
- Source statement: 152. No double accounting: Chaque composante doit avoir un ownership clair. ne doit pas être à la fois :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `152. No double accounting` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0149`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0422 — 153. Recommended convention

- Source: `SRC-005`
- Location: lines 7786–7804; heading `153. Recommended convention`
- Domain tags: DATA, ACCOUNTING, ROUTING
- Source statement: 153. Recommended convention: RoutePnL = after exchange fees and execution costs reste disponible à des fins analytiques.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `153. Recommended convention` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0150`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0423 — 154. ExternalFlows

- Source: `SRC-005`
- Location: lines 7805–7812; heading `154. ExternalFlows`
- Domain tags: DATA, ACCOUNTING
- Source statement: 154. ExternalFlows: Dépôts/retraits : ExternalFlow
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `154. ExternalFlows` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0151`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0424 — 155. CapitalState

- Source: `SRC-005`
- Location: lines 7813–7824; heading `155. CapitalState`
- Domain tags: DATA, CAPITAL, RISK
- Source statement: 155. CapitalState: CapitalState { gross_equity,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `155. CapitalState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0152`; supporting items: none found by conservative heading match; domain indexes `DATA, CAPITAL, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0425 — 156. HOT/WARM/COLD schema

- Source: `SRC-005`
- Location: lines 7825–7841; heading `156. HOT/WARM/COLD schema`
- Domain tags: DATA, HOT_WARM_COLD, DEPLOYMENT, CAPITAL, GRAPH
- Source statement: 156. HOT/WARM/COLD schema: GraphNodeState { asset_id,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `156. HOT/WARM/COLD schema` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0153`; supporting items: SRC-001-ITEM-0049, SRC-006-ITEM-0332, SRC-007-ITEM-0115; domain indexes `DATA, HOT_WARM_COLD, DEPLOYMENT, CAPITAL, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0426 — 157. Tier

- Source: `SRC-005`
- Location: lines 7842–7851; heading `157. Tier`
- Domain tags: DATA, GRAPH, HOT_WARM_COLD
- Source statement: 157. Tier: GraphTier { Hot,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `157. Tier` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0154`; supporting items: none found by conservative heading match; domain indexes `DATA, GRAPH, HOT_WARM_COLD`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0427 — 158. Tier transitions

- Source: `SRC-005`
- Location: lines 7852–7865; heading `158. Tier transitions`
- Domain tags: DATA, EXECUTION, CAPITAL, GRAPH
- Source statement: 158. Tier transitions: Produisent événements : GraphTierChanged
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `158. Tier transitions` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0155`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, CAPITAL, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0428 — 159. MarketAtlasRecord

- Source: `SRC-005`
- Location: lines 7866–7882; heading `159. MarketAtlasRecord`
- Domain tags: DATA, SURVIVAL, INVENTORY
- Source statement: 159. MarketAtlasRecord: MarketAtlasRecord { asset_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `159. MarketAtlasRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0156`; supporting items: none found by conservative heading match; domain indexes `DATA, SURVIVAL, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0429 — 160. Research vs live schemas

- Source: `SRC-005`
- Location: lines 7883–7887; heading `160. Research vs live schemas`
- Domain tags: DATA, RESEARCH
- Source statement: 160. Research vs live schemas: Le dataset R&D peut avoir plus de colonnes dérivées. Mais les colonnes live fondamentales ne sont pas renommées différemment.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `160. Research vs live schemas` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0157`; supporting items: none found by conservative heading match; domain indexes `DATA, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0430 — 161. Schema evolution

- Source: `SRC-005`
- Location: lines 7888–7900; heading `161. Schema evolution`
- Domain tags: DATA
- Source statement: 161. Schema evolution: Règle : backward compatible additive change
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `161. Schema evolution` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0158`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0431 — 162. Unknown fields

- Source: `SRC-005`
- Location: lines 7901–7908; heading `162. Unknown fields`
- Domain tags: DATA, RECOVERY
- Source statement: 162. Unknown fields: Les lecteurs plus anciens doivent idéalement pouvoir ignorer :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `162. Unknown fields` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0159`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0432 — 163. Removed fields

- Source: `SRC-005`
- Location: lines 7909–7917; heading `163. Removed fields`
- Domain tags: DATA
- Source statement: 163. Removed fields: Jamais supprimés silencieusement d’un schema permanent.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `163. Removed fields` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0160`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0433 — 164. Schema registry

- Source: `SRC-005`
- Location: lines 7918–7933; heading `164. Schema registry`
- Domain tags: DATA, DEPLOYMENT, RISK
- Source statement: 164. Schema registry: Fichier : schemas/
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `164. Schema registry` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0161`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0434 — 165. Internal Rust types are source of truth

- Source: `SRC-005`
- Location: lines 7934–7936; heading `165. Internal Rust types are source of truth`
- Domain tags: DATA, ARCH
- Source statement: 165. Internal Rust types are source of truth: Mais le contrat externe/dataset doit être documenté indépendamment du code pour audit.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `165. Internal Rust types are source of truth` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0162`; supporting items: SRC-004-ITEM-0043; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0435 — 166. Serialization

- Source: `SRC-005`
- Location: lines 7937–7952; heading `166. Serialization`
- Domain tags: DATA, RECORDER, HOT_WARM_COLD
- Source statement: 166. Serialization: pour RAW/hot pipelines si nécessaire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `166. Serialization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0163`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER, HOT_WARM_COLD`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0436 — 167. No giant JSON RAW

- Source: `SRC-005`
- Location: lines 7953–7960; heading `167. No giant JSON RAW`
- Domain tags: DATA
- Source statement: 167. No giant JSON RAW: Déjà fixé : binary + compression
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `167. No giant JSON RAW` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0164`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0437 — 168. Replay fidelity field

- Source: `SRC-005`
- Location: lines 7961–7973; heading `168. Replay fidelity field`
- Domain tags: REPLAY, SIMULATOR, INFRA, MICROSTRUCTURE
- Source statement: 168. Replay fidelity field: Chaque run Replay possède :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `168. Replay fidelity field` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0010`; supporting items: none found by conservative heading match; domain indexes `REPLAY, SIMULATOR, INFRA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0438 — 169. Why fidelity explicit

- Source: `SRC-005`
- Location: lines 7974–7986; heading `169. Why fidelity explicit`
- Domain tags: DATA, SIMULATOR, ACCOUNTING, RESEARCH
- Source statement: 169. Why fidelity explicit: On ne compare jamais : sans savoir que les hypothèses diffèrent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `169. Why fidelity explicit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0165`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR, ACCOUNTING, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0439 — 170. SimulationMode

- Source: `SRC-005`
- Location: lines 7987–7995; heading `170. SimulationMode`
- Domain tags: DATA, SIMULATOR, REPLAY
- Source statement: 170. SimulationMode: SimulationMode { ExogenousReplay,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `170. SimulationMode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0166`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0440 — 171. ExogenousReplay

- Source: `SRC-005`
- Location: lines 7996–8013; heading `171. ExogenousReplay`
- Domain tags: REPLAY, SIMULATOR, EXECUTION, INVENTORY, FUTURE
- Source statement: 171. ExogenousReplay: Le futur historique reste :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `171. ExogenousReplay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-REPLAY-0011`; supporting items: none found by conservative heading match; domain indexes `REPLAY, SIMULATOR, EXECUTION, INVENTORY, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0441 — 172. InteractiveCounterfactual

- Source: `SRC-005`
- Location: lines 8014–8024; heading `172. InteractiveCounterfactual`
- Domain tags: DATA, SIMULATOR, PARTICIPANTS, QUANT
- Source statement: 172. InteractiveCounterfactual: On applique : historical baseline
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `172. InteractiveCounterfactual` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0167`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR, PARTICIPANTS, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0442 — 173. BranchId

- Source: `SRC-005`
- Location: lines 8025–8031; heading `173. BranchId`
- Domain tags: DATA
- Source statement: 173. BranchId: Chaque scénario interactif : BranchId
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `173. BranchId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0168`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0443 — 174. MonteCarloPathId

- Source: `SRC-005`
- Location: lines 8032–8045; heading `174. MonteCarloPathId`
- Domain tags: DATA, CLOCK
- Source statement: 174. MonteCarloPathId: Chaque chemin : MonteCarloPathId
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `174. MonteCarloPathId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0169`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0444 — 175. Rejoin event

- Source: `SRC-005`
- Location: lines 8046–8053; heading `175. Rejoin event`
- Domain tags: DATA, SIMULATOR
- Source statement: 175. Rejoin event: Quand la perturbation est jugée dissipée :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `175. Rejoin event` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0170`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0445 — 176. Confidence schema

- Source: `SRC-005`
- Location: lines 8054–8074; heading `176. Confidence schema`
- Domain tags: DATA, INFRA, SIMULATOR
- Source statement: 176. Confidence schema: Pas juste : 0.78
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `176. Confidence schema` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0171`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0446 — 177. Why decomposed confidence

- Source: `SRC-005`
- Location: lines 8075–8087; heading `177. Why decomposed confidence`
- Domain tags: DATA, DEPLOYMENT, ACCOUNTING
- Source statement: 177. Why decomposed confidence: Ce n’est pas la même action.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `177. Why decomposed confidence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0172`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0447 — 178. LatencyTrace

- Source: `SRC-005`
- Location: lines 8088–8115; heading `178. LatencyTrace`
- Domain tags: DATA, INFRA, EXECUTION, RISK, ROUTING
- Source statement: 178. LatencyTrace: LatencyTrace { event_id?,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `178. LatencyTrace` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0173`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, EXECUTION, RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0448 — 179. InfraInstanceId

- Source: `SRC-005`
- Location: lines 8116–8125; heading `179. InfraInstanceId`
- Domain tags: DATA, INFRA, RISK
- Source statement: 179. InfraInstanceId: sans mettre ces détails partout.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `179. InfraInstanceId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0174`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0449 — 180. BenchmarkRun

- Source: `SRC-005`
- Location: lines 8126–8143; heading `180. BenchmarkRun`
- Domain tags: DATA, BENCHMARK
- Source statement: 180. BenchmarkRun: BenchmarkRun { benchmark_id,
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `180. BenchmarkRun` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0175`; supporting items: none found by conservative heading match; domain indexes `DATA, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0450 — 181. FirstArrivalRecord

- Source: `SRC-005`
- Location: lines 8144–8157; heading `181. FirstArrivalRecord`
- Domain tags: DATA
- Source statement: 181. FirstArrivalRecord: FirstArrivalRecord { canonical_event_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `181. FirstArrivalRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0176`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0451 — 182. InfraLostPnLRecord

- Source: `SRC-005`
- Location: lines 8158–8176; heading `182. InfraLostPnLRecord`
- Domain tags: DATA, EXECUTION, INFRA, ACCOUNTING
- Source statement: 182. InfraLostPnLRecord: InfraLostPnLRecord { opportunity_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `182. InfraLostPnLRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0177`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0452 — 183. Attribution must not double count

- Source: `SRC-005`
- Location: lines 8177–8184; heading `183. Attribution must not double count`
- Domain tags: DATA, INFRA
- Source statement: 183. Attribution must not double count: Le schema doit conserver chaque étape.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `183. Attribution must not double count` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0178`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0453 — 184. ModelPredictionRecord

- Source: `SRC-005`
- Location: lines 8185–8199; heading `184. ModelPredictionRecord`
- Domain tags: DATA
- Source statement: 184. ModelPredictionRecord: ModelPredictionRecord { model_version,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `184. ModelPredictionRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0179`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0454 — 185. CalibrationDataset

- Source: `SRC-005`
- Location: lines 8200–8208; heading `185. CalibrationDataset`
- Domain tags: DATA
- Source statement: 185. CalibrationDataset: Construit automatiquement depuis : predictions
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `185. CalibrationDataset` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0180`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0455 — 186. Champion / Challenger

- Source: `SRC-005`
- Location: lines 8209–8218; heading `186. Champion / Challenger`
- Domain tags: DATA, FUTURE
- Source statement: 186. Champion / Challenger: Chaque prediction porte : role {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `186. Champion / Challenger` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0181`; supporting items: SRC-001-ITEM-0109, SRC-007-ITEM-0046, SRC-007-ITEM-0103, SRC-008-ITEM-0085; domain indexes `DATA, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0456 — 187. Challenger never alters decision

- Source: `SRC-005`
- Location: lines 8219–8232; heading `187. Challenger never alters decision`
- Domain tags: DATA, FUTURE, RISK
- Source statement: 187. Challenger never alters decision: Il n’entre pas dans : tant qu’il n’est pas promu.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `187. Challenger never alters decision` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0182`; supporting items: none found by conservative heading match; domain indexes `DATA, FUTURE, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0457 — 188. PromotionEvent

- Source: `SRC-005`
- Location: lines 8233–8245; heading `188. PromotionEvent`
- Domain tags: DATA, VALIDATION
- Source statement: 188. PromotionEvent: ModelPromoted { old_champion,
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `188. PromotionEvent` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0183`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0458 — 189. DeploymentVersion

- Source: `SRC-005`
- Location: lines 8246–8255; heading `189. DeploymentVersion`
- Domain tags: DATA, DEPLOYMENT
- Source statement: 189. DeploymentVersion: Chaque Docker image possède :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `189. DeploymentVersion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0184`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0459 — 190. Why digest

- Source: `SRC-005`
- Location: lines 8256–8264; heading `190. Why digest`
- Domain tags: DATA, DEPLOYMENT, PRODUCT
- Source statement: 190. Why digest: ne doivent jamais être ambiguës.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `190. Why digest` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0185`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0460 — 191. ClientInstallationId

- Source: `SRC-005`
- Location: lines 8265–8272; heading `191. ClientInstallationId`
- Domain tags: DATA, DEPLOYMENT, CLIENT
- Source statement: 191. ClientInstallationId: sans nécessairement transmettre de données personnelles.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `191. ClientInstallationId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0186`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0461 — 192. Local-only by default

- Source: `SRC-005`
- Location: lines 8273–8280; heading `192. Local-only by default`
- Domain tags: DATA, CLIENT
- Source statement: 192. Local-only by default: Les schemas n’impliquent pas : Le client peut garder ses données localement.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `192. Local-only by default` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0187`; supporting items: none found by conservative heading match; domain indexes `DATA, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0462 — 193. Logs vs events

- Source: `SRC-005`
- Location: lines 8281–8293; heading `193. Logs vs events`
- Domain tags: DATA, REPLAY
- Source statement: 193. Logs vs events: Le système ne dépend pas des logs texte pour reconstruire son état.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `193. Logs vs events` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0188`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0463 — 194. StructuredEvent envelope

- Source: `SRC-005`
- Location: lines 8294–8311; heading `194. StructuredEvent envelope`
- Domain tags: DATA, CLOCK
- Source statement: 194. StructuredEvent envelope: EventEnvelope<T> { event_id,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `194. StructuredEvent envelope` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0189`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0464 — 195. Correlation IDs

- Source: `SRC-005`
- Location: lines 8312–8324; heading `195. Correlation IDs`
- Domain tags: DATA, PORTFOLIO, EXECUTION
- Source statement: 195. Correlation IDs: Pour relier : OpportunityId
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `195. Correlation IDs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0190`; supporting items: none found by conservative heading match; domain indexes `DATA, PORTFOLIO, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0465 — 196. Complete trace

- Source: `SRC-005`
- Location: lines 8325–8347; heading `196. Complete trace`
- Domain tags: DATA, EXECUTION, RISK, ACCOUNTING
- Source statement: 196. Complete trace: On doit pouvoir suivre :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `196. Complete trace` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0191`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0466 — 197. This trace is mandatory

- Source: `SRC-005`
- Location: lines 8348–8357; heading `197. This trace is mandatory`
- Domain tags: DATA, CLIENT, OPERATIONS, SIMULATOR
- Source statement: 197. This trace is mandatory: Sans ça : simulator calibration
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `197. This trace is mandatory` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0192`; supporting items: none found by conservative heading match; domain indexes `DATA, CLIENT, OPERATIONS, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0467 — 198. Deterministic numeric rules

- Source: `SRC-005`
- Location: lines 8358–8367; heading `198. Deterministic numeric rules`
- Domain tags: DETERMINISM, EXECUTION, REPLAY
- Source statement: 198. Deterministic numeric rules: Les conversions exchange utilisent : Le Replay et Live utilisent exactement le même code.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `198. Deterministic numeric rules` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0005`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, EXECUTION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0468 — 199. No duplicated formula implementations

- Source: `SRC-005`
- Location: lines 8368–8380; heading `199. No duplicated formula implementations`
- Domain tags: DATA, ROUTING
- Source statement: 199. No duplicated formula implementations: Interdit : live_net_convert()
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `199. No duplicated formula implementations` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0193`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0469 — 200. Same FeeEngine

- Source: `SRC-005`
- Location: lines 8381–8393; heading `200. Same FeeEngine`
- Domain tags: DATA, ACCOUNTING, REPLAY
- Source statement: 200. Same FeeEngine: Mais même code de calcul.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `200. Same FeeEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0194`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0470 — 201. Same PrecisionEngine

- Source: `SRC-005`
- Location: lines 8394–8396; heading `201. Same PrecisionEngine`
- Domain tags: DATA, QUANT
- Source statement: 201. Same PrecisionEngine: Même quantization.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `201. Same PrecisionEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0195`; supporting items: none found by conservative heading match; domain indexes `DATA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0471 — 202. Same RouteEngine

- Source: `SRC-005`
- Location: lines 8397–8399; heading `202. Same RouteEngine`
- Domain tags: DATA, ROUTING
- Source statement: 202. Same RouteEngine: Même precomputed routes.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `202. Same RouteEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0196`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0472 — 203. Same RiskEngine

- Source: `SRC-005`
- Location: lines 8400–8402; heading `203. Same RiskEngine`
- Domain tags: DATA, RISK
- Source statement: 203. Same RiskEngine: Même gates.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `203. Same RiskEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0197`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0473 — 204. Same Execution State Machine

- Source: `SRC-005`
- Location: lines 8403–8413; heading `204. Same Execution State Machine`
- Domain tags: DATA, EXECUTION, RECOVERY, REPLAY
- Source statement: 204. Same Execution State Machine: Replay génère les mêmes états :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `204. Same Execution State Machine` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0198`; supporting items: SRC-006-ITEM-0391, SRC-004-ITEM-0137, SRC-004-ITEM-0143; domain indexes `DATA, EXECUTION, RECOVERY, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0474 — 205. Same RecoveryEngine

- Source: `SRC-005`
- Location: lines 8414–8422; heading `205. Same RecoveryEngine`
- Domain tags: DATA, RECOVERY
- Source statement: 205. Same RecoveryEngine: Très important. Un backtest qui :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `205. Same RecoveryEngine` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0199`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0475 — 206. Same InventoryEngine

- Source: `SRC-005`
- Location: lines 8423–8430; heading `206. Same InventoryEngine`
- Domain tags: DATA, INVENTORY, REPLAY
- Source statement: 206. Same InventoryEngine: Replay doit connaître : actual simulated inventory
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `206. Same InventoryEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0200`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0476 — 207. Same ReservationEngine

- Source: `SRC-005`
- Location: lines 8431–8434; heading `207. Same ReservationEngine`
- Domain tags: DATA, REPLAY
- Source statement: 207. Same ReservationEngine: Même problème de double-spending en Replay.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `207. Same ReservationEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0201`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0477 — 208. Replay account state

- Source: `SRC-005`
- Location: lines 8435–8442; heading `208. Replay account state`
- Domain tags: REPLAY, RECONCILIATION
- Source statement: 208. Replay account state: Le Replay possède un : mais conforme au même AccountState.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `208. Replay account state` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0012`; supporting items: none found by conservative heading match; domain indexes `REPLAY, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0478 — 209. Shadow account state

- Source: `SRC-005`
- Location: lines 8443–8461; heading `209. Shadow account state`
- Domain tags: DATA, RECONCILIATION, VALIDATION, EXECUTION, SIMULATOR
- Source statement: 209. Shadow account state: ne modifie pas l’état réel.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `209. Shadow account state` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0202`; supporting items: none found by conservative heading match; domain indexes `DATA, RECONCILIATION, VALIDATION, EXECUTION, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0479 — 210. Important distinction Shadow

- Source: `SRC-005`
- Location: lines 8462–8474; heading `210. Important distinction Shadow`
- Domain tags: DATA, VALIDATION, SIMULATOR
- Source statement: 210. Important distinction Shadow: Deux états : ActualAccountState
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `210. Important distinction Shadow` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0203`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0480 — 211. Paper mode

- Source: `SRC-005`
- Location: lines 8475–8483; heading `211. Paper mode`
- Domain tags: DATA, RESEARCH, EXECUTION
- Source statement: 211. Paper mode: Paper peut utiliser : real market
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `211. Paper mode` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0204`; supporting items: none found by conservative heading match; domain indexes `DATA, RESEARCH, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0481 — 212. Micro-live

- Source: `SRC-005`
- Location: lines 8484–8493; heading `212. Micro-live`
- Domain tags: DATA, VALIDATION, EXECUTION, RISK
- Source statement: 212. Micro-live: Aucune logique spéciale d’exécution hormis les limites de risque/configuration.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `212. Micro-live` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0205`; supporting items: SRC-001-ITEM-0018, SRC-001-ITEM-0076, SRC-001-ITEM-0146, SRC-006-ITEM-0258; domain indexes `DATA, VALIDATION, EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0482 — 213. Live

- Source: `SRC-005`
- Location: lines 8494–8503; heading `213. Live`
- Domain tags: DATA, RISK, VALIDATION, MICROSTRUCTURE, CAPITAL
- Source statement: 213. Live: Même moteur. Seuls :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `213. Live` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0206`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, VALIDATION, MICROSTRUCTURE, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0483 — 214. Environment flag cannot change math

- Source: `SRC-005`
- Location: lines 8504–8513; heading `214. Environment flag cannot change math`
- Domain tags: DATA, RISK, MICROSTRUCTURE, ROUTING
- Source statement: 214. Environment flag cannot change math: LIVE ne doit jamais modifier :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `214. Environment flag cannot change math` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0207`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, MICROSTRUCTURE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0484 — 215. Data contract tests

- Source: `SRC-005`
- Location: lines 8514–8522; heading `215. Data contract tests`
- Domain tags: DATA
- Source statement: 215. Data contract tests: Pour chaque struct sérialisé :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `215. Data contract tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0208`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0485 — 216. Golden replay test

- Source: `SRC-005`
- Location: lines 8523–8538; heading `216. Golden replay test`
- Domain tags: REPLAY, DATA, ACCOUNTING
- Source statement: 216. Golden replay test: Petit dataset fixe : MarketEvents
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `216. Golden replay test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0013`; supporting items: SRC-006-ITEM-0468, SRC-006-ITEM-0471; domain indexes `REPLAY, DATA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0486 — 217. Replay determinism test

- Source: `SRC-005`
- Location: lines 8539–8547; heading `217. Replay determinism test`
- Domain tags: DETERMINISM, REPLAY
- Source statement: 217. Replay determinism test: 100 executions : Run A hash
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `217. Replay determinism test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0006`; supporting items: SRC-006-ITEM-0471; domain indexes `DETERMINISM, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0487 — 218. Multi-thread determinism

- Source: `SRC-005`
- Location: lines 8548–8566; heading `218. Multi-thread determinism`
- Domain tags: DETERMINISM, ROUTING, PRODUCT
- Source statement: 218. Multi-thread determinism: Si production utilise concurrence : On peut autoriser du parallélisme pour :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `218. Multi-thread determinism` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0007`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, ROUTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0488 — 219. Single-writer principle

- Source: `SRC-005`
- Location: lines 8567–8576; heading `219. Single-writer principle`
- Domain tags: DATA
- Source statement: 219. Single-writer principle: ont un propriétaire logique unique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `219. Single-writer principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0209`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0489 — 220. Why

- Source: `SRC-005`
- Location: lines 8577–8585; heading `220. Why`
- Domain tags: DATA, EXECUTION
- Source statement: 220. Why: Évite : race conditions
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `220. Why` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0210`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0490 — 221. Parallel readers

- Source: `SRC-005`
- Location: lines 8586–8592; heading `221. Parallel readers`
- Domain tags: DATA, EXECUTION, ARCH
- Source statement: 221. Parallel readers: Les autres modules lisent :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `221. Parallel readers` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0211`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0491 — 222. Snapshot publication

- Source: `SRC-005`
- Location: lines 8593–8603; heading `222. Snapshot publication`
- Domain tags: DATA
- Source statement: 222. Snapshot publication: Pattern : Mutable owner
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `222. Snapshot publication` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0212`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0492 — 223. Atomic snapshot version

- Source: `SRC-005`
- Location: lines 8604–8611; heading `223. Atomic snapshot version`
- Domain tags: DATA
- Source statement: 223. Atomic snapshot version: pour détecter une lecture périmée.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `223. Atomic snapshot version` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0213`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0493 — 224. TOCTOU protection

- Source: `SRC-005`
- Location: lines 8612–8624; heading `224. TOCTOU protection`
- Domain tags: DATA, RISK
- Source statement: 224. TOCTOU protection: est comparée au state actuel.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `224. TOCTOU protection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0214`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0494 — 225. Critical changes

- Source: `SRC-005`
- Location: lines 8625–8634; heading `225. Critical changes`
- Domain tags: DATA, RISK, INFRA, INVENTORY
- Source statement: 225. Critical changes: Exemples : book version changed materially
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `225. Critical changes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0215`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK, INFRA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0495 — 226. Not every market tick forces restart

- Source: `SRC-005`
- Location: lines 8635–8642; heading `226. Not every market tick forces restart`
- Domain tags: DATA, OPERATIONS
- Source statement: 226. Not every market tick forces restart: Le pre-send check décide si le changement : ou reste dans la tolérance prévue.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `226. Not every market tick forces restart` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0216`; supporting items: none found by conservative heading match; domain indexes `DATA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0496 — 227. Plan validity envelope

- Source: `SRC-005`
- Location: lines 8643–8651; heading `227. Plan validity envelope`
- Domain tags: DATA
- Source statement: 227. Plan validity envelope: ExecutionPlan peut contenir : max_book_version_age
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `227. Plan validity envelope` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0217`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0497 — 228. If envelope violated

- Source: `SRC-005`
- Location: lines 8652–8657; heading `228. If envelope violated`
- Domain tags: DATA
- Source statement: 228. If envelope violated: replan or abort
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `228. If envelope violated` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0218`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0498 — 229. Storage separation

- Source: `SRC-005`
- Location: lines 8658–8669; heading `229. Storage separation`
- Domain tags: DATA, INFRA
- Source statement: 229. Storage separation: Sur VPS : /data/raw
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `229. Storage separation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0219`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0499 — 230. Persistent state

- Source: `SRC-005`
- Location: lines 8670–8672; heading `230. Persistent state`
- Domain tags: DATA, DEPLOYMENT
- Source statement: 230. Persistent state: Doit survivre au remplacement du container.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `230. Persistent state` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0220`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0500 — 231. Ephemeral state

- Source: `SRC-005`
- Location: lines 8673–8681; heading `231. Ephemeral state`
- Domain tags: DATA, INFRA, DEPLOYMENT, ROUTING
- Source statement: 231. Ephemeral state: peuvent rester dans le container/RAM.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `231. Ephemeral state` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0221`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, DEPLOYMENT, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0501 — 232. State checkpoint

- Source: `SRC-005`
- Location: lines 8682–8692; heading `232. State checkpoint`
- Domain tags: DATA, INVENTORY
- Source statement: 232. State checkpoint: Périodiquement : AccountState snapshot
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `232. State checkpoint` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0222`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0502 — 233. Checkpoint is not source of truth

- Source: `SRC-005`
- Location: lines 8693–8703; heading `233. Checkpoint is not source of truth`
- Domain tags: DATA, RECONCILIATION, OPERATIONS
- Source statement: 233. Checkpoint is not source of truth: Au restart : checkpoint
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `233. Checkpoint is not source of truth` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0223`; supporting items: SRC-004-ITEM-0043; domain indexes `DATA, RECONCILIATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0503 — 234. Checkpoint version

- Source: `SRC-005`
- Location: lines 8704–8709; heading `234. Checkpoint version`
- Domain tags: DATA
- Source statement: 234. Checkpoint version: checkpoint_schema_version
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `234. Checkpoint version` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0224`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0504 — 235. Migration

- Source: `SRC-005`
- Location: lines 8710–8717; heading `235. Migration`
- Domain tags: DATA, DEPLOYMENT
- Source statement: 235. Migration: Une nouvelle image doit savoir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `235. Migration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0225`; supporting items: none found by conservative heading match; domain indexes `DATA, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0505 — 236. No silent state discard

- Source: `SRC-005`
- Location: lines 8718–8725; heading `236. No silent state discard`
- Domain tags: DATA, RECONCILIATION
- Source statement: 236. No silent state discard: Si checkpoint incompatible : do not boot READY
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `236. No silent state discard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0226`; supporting items: none found by conservative heading match; domain indexes `DATA, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0506 — 237. Event retention classes

- Source: `SRC-005`
- Location: lines 8726–8734; heading `237. Event retention classes`
- Domain tags: RECORDER
- Source statement: 237. Event retention classes: PERMANENT MEDIUM
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `237. Event retention classes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REC-0011`; supporting items: none found by conservative heading match; domain indexes `RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0507 — 238. Permanent

- Source: `SRC-005`
- Location: lines 8735–8746; heading `238. Permanent`
- Domain tags: DATA, EXECUTION, RISK, OPERATIONS
- Source statement: 238. Permanent: fills orders
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `238. Permanent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0227`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RISK, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0508 — 239. Short

- Source: `SRC-005`
- Location: lines 8747–8753; heading `239. Short`
- Domain tags: DATA
- Source statement: 239. Short: general raw market selon stockage.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `239. Short` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0228`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0509 — 240. Trade windows

- Source: `SRC-005`
- Location: lines 8754–8763; heading `240. Trade windows`
- Domain tags: DATA
- Source statement: 240. Trade windows: Pour chaque vrai trade : de market RAW conservés plus longtemps.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `240. Trade windows` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0229`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0510 — 241. Why

- Source: `SRC-005`
- Location: lines 8764–8773; heading `241. Why`
- Domain tags: DATA, RECOVERY, PARTICIPANTS
- Source statement: 241. Why: Essentiel pour : predicted vs actual
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `241. Why` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0230`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY, PARTICIPANTS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0511 — 242. Incident windows

- Source: `SRC-005`
- Location: lines 8774–8776; heading `242. Incident windows`
- Domain tags: DATA, OPERATIONS
- Source statement: 242. Incident windows: Même chose autour des incidents.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `242. Incident windows` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0231`; supporting items: none found by conservative heading match; domain indexes `DATA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0512 — 243. Schema validation on ingestion

- Source: `SRC-005`
- Location: lines 8777–8786; heading `243. Schema validation on ingestion`
- Domain tags: DATA, VALIDATION, RECOVERY
- Source statement: 243. Schema validation on ingestion: Un payload impossible : negative size
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `243. Schema validation on ingestion` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0232`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0513 — 244. Unknown event type

- Source: `SRC-005`
- Location: lines 8787–8795; heading `244. Unknown event type`
- Domain tags: DATA, RECOVERY, OPERATIONS
- Source statement: 244. Unknown event type: Si exchange ajoute un nouveau type :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `244. Unknown event type` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0233`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0514 — 245. Forward compatibility

- Source: `SRC-005`
- Location: lines 8796–8798; heading `245. Forward compatibility`
- Domain tags: DATA, FUTURE
- Source statement: 245. Forward compatibility: RAW permet de renormaliser plus tard un événement que notre ancienne version ne comprenait pas.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `245. Forward compatibility` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0234`; supporting items: none found by conservative heading match; domain indexes `DATA, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0515 — 246. Latency measurement contract

- Source: `SRC-005`
- Location: lines 8799–8806; heading `246. Latency measurement contract`
- Domain tags: DATA, INFRA, EXECUTION, CLOCK
- Source statement: 246. Latency measurement contract: Tous les timestamps internes utilisent :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `246. Latency measurement contract` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0235`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, EXECUTION, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0516 — 247. Cross-machine latency

- Source: `SRC-005`
- Location: lines 8807–8815; heading `247. Cross-machine latency`
- Domain tags: DATA, INFRA, CLOCK
- Source statement: 247. Cross-machine latency: Utilise : wall clock
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `247. Cross-machine latency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0236`; supporting items: none found by conservative heading match; domain indexes `DATA, INFRA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0517 — 248. ClockQualityRecord

- Source: `SRC-005`
- Location: lines 8816–8826; heading `248. ClockQualityRecord`
- Domain tags: CLOCK
- Source statement: 248. ClockQualityRecord: ClockQualityRecord { offset,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `248. ClockQualityRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLOCK-0013`; supporting items: none found by conservative heading match; domain indexes `CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0518 — 249. Timing validity

- Source: `SRC-005`
- Location: lines 8827–8842; heading `249. Timing validity`
- Domain tags: DATA
- Source statement: 249. Timing validity: Une mesure cross-machine est : ou autre règle statistique définie.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `249. Timing validity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0237`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0519 — 250. Benchmark data contract

- Source: `SRC-005`
- Location: lines 8843–8852; heading `250. Benchmark data contract`
- Domain tags: DATA, BENCHMARK, DETERMINISM, INFRA
- Source statement: 250. Benchmark data contract: Tous les candidats VPS doivent exécuter :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `250. Benchmark data contract` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0238`; supporting items: none found by conservative heading match; domain indexes `DATA, BENCHMARK, DETERMINISM, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0520 — 251. Formula input traceability

- Source: `SRC-005`
- Location: lines 8853–8867; heading `251. Formula input traceability`
- Domain tags: DATA, ACCOUNTING, ROUTING
- Source statement: 251. Formula input traceability: Chaque résultat important doit pouvoir référencer ses inputs.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `251. Formula input traceability` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0239`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0521 — 252. Why

- Source: `SRC-005`
- Location: lines 8868–8875; heading `252. Why`
- Domain tags: DATA, ACCOUNTING
- Source statement: 252. Why: on peut identifier tous les trades concernés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `252. Why` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0240`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0522 — 253. Data lineage

- Source: `SRC-005`
- Location: lines 8876–8898; heading `253. Data lineage`
- Domain tags: DATA, EXECUTION, RISK, ACCOUNTING
- Source statement: 253. Data lineage: Chaîne : RawEvent
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `253. Data lineage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0241`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0523 — 254. Every link traceable

- Source: `SRC-005`
- Location: lines 8899–8908; heading `254. Every link traceable`
- Domain tags: DATA, DETERMINISM
- Source statement: 254. Every link traceable: Pas forcément stocker une énorme copie de chaque objet.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `254. Every link traceable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0242`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0524 — 255. Dataset contamination prevention

- Source: `SRC-005`
- Location: lines 8909–8916; heading `255. Dataset contamination prevention`
- Domain tags: DATA, VALIDATION
- Source statement: 255. Dataset contamination prevention: Quand on entraîne un modèle :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `255. Dataset contamination prevention` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0243`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0525 — 256. Model artifact stores training range

- Source: `SRC-005`
- Location: lines 8917–8924; heading `256. Model artifact stores training range`
- Domain tags: DATA, REPLAY, FUTURE
- Source statement: 256. Model artifact stores training range: dans un replay historique antérieur.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `256. Model artifact stores training range` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-DATA-0244`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0526 — 257. Point-in-time correctness

- Source: `SRC-005`
- Location: lines 8925–8939; heading `257. Point-in-time correctness`
- Domain tags: DATA, ACCOUNTING, REPLAY
- Source statement: 257. Point-in-time correctness: ne peut utiliser que : qui auraient été disponibles à T dans le scénario testé.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `257. Point-in-time correctness` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0245`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0528 — Historical truth replay

- Source: `SRC-005`
- Location: lines 8941–8942; heading `Historical truth replay`
- Domain tags: REPLAY
- Source statement: Historical truth replay: Utilise les versions réellement existantes à T.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `Historical truth replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0014`; supporting items: SRC-006-ITEM-0313; domain indexes `REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0529 — Research counterfactual

- Source: `SRC-005`
- Location: lines 8943–8950; heading `Research counterfactual`
- Domain tags: DATA, SIMULATOR, RESEARCH
- Source statement: Research counterfactual: Peut utiliser un modèle moderne sur ancien dataset. Mais le RunManifest marque clairement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `Research counterfactual` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DATA-0246`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0530 — 259. No mixing without label

- Source: `SRC-005`
- Location: lines 8951–8953; heading `259. No mixing without label`
- Domain tags: DATA
- Source statement: 259. No mixing without label: Sinon backtest trompeur.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `259. No mixing without label` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0247`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0531 — 260. Config provenance

- Source: `SRC-005`
- Location: lines 8954–8971; heading `260. Config provenance`
- Domain tags: DATA
- Source statement: 260. Config provenance: ConfigValue { value,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `260. Config provenance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-DATA-0248`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0532 — 261. Client overrides

- Source: `SRC-005`
- Location: lines 8972–8974; heading `261. Client overrides`
- Domain tags: DATA, CLIENT, RISK
- Source statement: 261. Client overrides: Doivent respecter Risk Constitution.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `261. Client overrides` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0249`; supporting items: none found by conservative heading match; domain indexes `DATA, CLIENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0533 — 262. Invalid override

- Source: `SRC-005`
- Location: lines 8975–8977; heading `262. Invalid override`
- Domain tags: DATA
- Source statement: 262. Invalid override: Boot failure ou config rejected.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `262. Invalid override` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-DATA-0250`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0534 — 263. Test fixtures

- Source: `SRC-005`
- Location: lines 8978–8987; heading `263. Test fixtures`
- Domain tags: DATA, EXECUTION
- Source statement: 263. Test fixtures: faciles à construire pour tests.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `263. Test fixtures` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0251`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0535 — 264. Builders

- Source: `SRC-005`
- Location: lines 8988–8997; heading `264. Builders`
- Domain tags: DATA, ARCH
- Source statement: 264. Builders: pour réduire boilerplate et améliorer couverture.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `264. Builders` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0252`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0536 — 265. Property-based tests

- Source: `SRC-005`
- Location: lines 8998–9008; heading `265. Property-based tests`
- Domain tags: DATA, EXECUTION
- Source statement: 265. Property-based tests: Générer aléatoirement : event sequences
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `265. Property-based tests` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0253`; supporting items: SRC-004-ITEM-0125; domain indexes `DATA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0537 — 266. Fuzzing

- Source: `SRC-005`
- Location: lines 9009–9018; heading `266. Fuzzing`
- Domain tags: DATA
- Source statement: 266. Fuzzing: Cibles : market payload parser
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `266. Fuzzing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0254`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0538 — 267. Serialization fuzzing

- Source: `SRC-005`
- Location: lines 9019–9025; heading `267. Serialization fuzzing`
- Domain tags: DATA
- Source statement: 267. Serialization fuzzing: Input corrompu ne doit pas produire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `267. Serialization fuzzing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0255`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0539 — 268. API adapters cannot mutate core state directly

- Source: `SRC-005`
- Location: lines 9026–9032; heading `268. API adapters cannot mutate core state directly`
- Domain tags: DATA, ARCH
- Source statement: 268. API adapters cannot mutate core state directly: Ils émettent seulement : NormalizedEvents
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `268. API adapters cannot mutate core state directly` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0256`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0540 — 269. Core state mutations happen through reducers

- Source: `SRC-005`
- Location: lines 9033–9035; heading `269. Core state mutations happen through reducers`
- Domain tags: DATA, ARCH
- Source statement: 269. Core state mutations happen through reducers: Principe très important.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `269. Core state mutations happen through reducers` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0257`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0541 — 270. Strategy cannot mutate AccountState

- Source: `SRC-005`
- Location: lines 9036–9043; heading `270. Strategy cannot mutate AccountState`
- Domain tags: DATA
- Source statement: 270. Strategy cannot mutate AccountState: Elle lit. Elle produit :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `270. Strategy cannot mutate AccountState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0258`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0542 — 271. Risk cannot mutate AccountState

- Source: `SRC-005`
- Location: lines 9044–9050; heading `271. Risk cannot mutate AccountState`
- Domain tags: DATA, RISK
- Source statement: 271. Risk cannot mutate AccountState: Il produit : RiskDecision
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `271. Risk cannot mutate AccountState` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0259`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0543 — 272. ExecutionCoordinator can request effects

- Source: `SRC-005`
- Location: lines 9051–9057; heading `272. ExecutionCoordinator can request effects`
- Domain tags: DATA
- Source statement: 272. ExecutionCoordinator can request effects: Mais actual state change vient de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `272. ExecutionCoordinator can request effects` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0260`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0544 — 273. Why event-driven

- Source: `SRC-005`
- Location: lines 9058–9067; heading `273. Why event-driven`
- Domain tags: DATA, REPLAY
- Source statement: 273. Why event-driven: Cela rend : replay
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `273. Why event-driven` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0261`; supporting items: none found by conservative heading match; domain indexes `DATA, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0545 — 274. State transition schema

- Source: `SRC-005`
- Location: lines 9068–9085; heading `274. State transition schema`
- Domain tags: DATA, CLOCK
- Source statement: 274. State transition schema: StateTransition { entity_type,
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `274. State transition schema` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0262`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0546 — 275. Reason mandatory

- Source: `SRC-005`
- Location: lines 9086–9093; heading `275. Reason mandatory`
- Domain tags: DATA, RECOVERY
- Source statement: 275. Reason mandatory: Pas de transition : RECOVERY_REQUIRED
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `275. Reason mandatory` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0263`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0547 — 276. IncidentId

- Source: `SRC-005`
- Location: lines 9094–9100; heading `276. IncidentId`
- Domain tags: DATA, OPERATIONS
- Source statement: 276. IncidentId: Une anomalie peut regrouper plusieurs événements :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `276. IncidentId` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0264`; supporting items: none found by conservative heading match; domain indexes `DATA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0548 — 277. IncidentRecord

- Source: `SRC-005`
- Location: lines 9101–9119; heading `277. IncidentRecord`
- Domain tags: DATA, OPERATIONS
- Source statement: 277. IncidentRecord: IncidentRecord { incident_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `277. IncidentRecord` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0265`; supporting items: none found by conservative heading match; domain indexes `DATA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0549 — 278. Severity

- Source: `SRC-005`
- Location: lines 9120–9128; heading `278. Severity`
- Domain tags: DATA
- Source statement: 278. Severity: Warning Critical
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `278. Severity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0266`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0550 — 279. Incident does not equal log error

- Source: `SRC-005`
- Location: lines 9129–9131; heading `279. Incident does not equal log error`
- Domain tags: DATA, OPERATIONS
- Source statement: 279. Incident does not equal log error: C’est un objet métier exploitable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `279. Incident does not equal log error` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0267`; supporting items: none found by conservative heading match; domain indexes `DATA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0551 — 280. Deterministic risk snapshot creation

- Source: `SRC-005`
- Location: lines 9132–9134; heading `280. Deterministic risk snapshot creation`
- Domain tags: DETERMINISM, RISK
- Source statement: 280. Deterministic risk snapshot creation: La liste des books/assets/features dans un snapshot est triée de façon canonique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `280. Deterministic risk snapshot creation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0008`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0552 — 281. Canonical ordering

- Source: `SRC-005`
- Location: lines 9135–9142; heading `281. Canonical ordering`
- Domain tags: DETERMINISM
- Source statement: 281. Canonical ordering: Important pour : hashes
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `281. Canonical ordering` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0009`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0553 — 282. Hash canonicalization

- Source: `SRC-005`
- Location: lines 9143–9149; heading `282. Hash canonicalization`
- Domain tags: DETERMINISM, EXECUTION
- Source statement: 282. Hash canonicalization: Pas de hash dépendant :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `282. Hash canonicalization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0010`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0554 — 283. Float canonicalization

- Source: `SRC-005`
- Location: lines 9150–9157; heading `283. Float canonicalization`
- Domain tags: DATA, DETERMINISM
- Source statement: 283. Float canonicalization: Pour hashes : use fixed representation
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `283. Float canonicalization` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0268`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0555 — 284. Model deterministic inference

- Source: `SRC-005`
- Location: lines 9158–9160; heading `284. Model deterministic inference`
- Domain tags: DETERMINISM, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 284. Model deterministic inference: Les modèles utilisés en hot path doivent fonctionner en mode déterministe lorsque possible.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `284. Model deterministic inference` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0011`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0556 — 285. Hardware nondeterminism

- Source: `SRC-005`
- Location: lines 9161–9168; heading `285. Hardware nondeterminism`
- Domain tags: DETERMINISM
- Source statement: 285. Hardware nondeterminism: Si modèle/BLAS peut produire de minuscules différences : ne doivent pas être hypersensibles à 1e-15.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `285. Hardware nondeterminism` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0012`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0557 — 286. Numerical epsilon contract

- Source: `SRC-005`
- Location: lines 9169–9176; heading `286. Numerical epsilon contract`
- Domain tags: DATA, FORMULA
- Source statement: 286. Numerical epsilon contract: Chaque formule définit : comparison tolerance
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `286. Numerical epsilon contract` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0269`; supporting items: none found by conservative heading match; domain indexes `DATA, FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0558 — 287. Exchange boundary exactness

- Source: `SRC-005`
- Location: lines 9177–9185; heading `287. Exchange boundary exactness`
- Domain tags: DATA
- Source statement: 287. Exchange boundary exactness: Mais pour : ticks
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `287. Exchange boundary exactness` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0270`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0559 — 288. PnL tolerance

- Source: `SRC-005`
- Location: lines 9186–9193; heading `288. PnL tolerance`
- Domain tags: DATA, ACCOUNTING, EXECUTION, VALIDATION, QUANT
- Source statement: 288. PnL tolerance: Golden tests utilisent : economic tolerance
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `288. PnL tolerance` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0271`; supporting items: none found by conservative heading match; domain indexes `DATA, ACCOUNTING, EXECUTION, VALIDATION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0560 — 289. Replay performance

- Source: `SRC-005`
- Location: lines 9194–9201; heading `289. Replay performance`
- Domain tags: REPLAY, BENCHMARK
- Source statement: 289. Replay performance: Déterminisme ne doit pas empêcher : On peut paralléliser certaines features à condition que commit final reste ordonné.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `289. Replay performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0015`; supporting items: none found by conservative heading match; domain indexes `REPLAY, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0561 — 290. Event batching Replay

- Source: `SRC-005`
- Location: lines 9202–9209; heading `290. Event batching Replay`
- Domain tags: REPLAY, CLOCK, DETERMINISM
- Source statement: 290. Event batching Replay: Si plusieurs events partagent même timestamp :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `290. Event batching Replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0016`; supporting items: none found by conservative heading match; domain indexes `REPLAY, CLOCK, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0562 — 291. Live event concurrency

- Source: `SRC-005`
- Location: lines 9210–9217; heading `291. Live event concurrency`
- Domain tags: DATA, EXECUTION, ARCH
- Source statement: 291. Live event concurrency: Les adapters peuvent recevoir simultanément.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `291. Live event concurrency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0272`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0563 — 292. Event bus

- Source: `SRC-005`
- Location: lines 9218–9227; heading `292. Event bus`
- Domain tags: DATA, DETERMINISM
- Source statement: 292. Event bus: Responsable de : ordering
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `292. Event bus` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0273`; supporting items: none found by conservative heading match; domain indexes `DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0564 — 293. Priority

- Source: `SRC-005`
- Location: lines 9228–9236; heading `293. Priority`
- Domain tags: DATA
- Source statement: 293. Priority: Account/execution events peuvent avoir priorité supérieure aux : priorité ne doit pas réordonner artificiellement des événements économiques dépendants.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `293. Priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0274`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0565 — 294. Separate buses possible

- Source: `SRC-005`
- Location: lines 9237–9247; heading `294. Separate buses possible`
- Domain tags: DATA, ARCH
- Source statement: 294. Separate buses possible: Mais les dépendances d’ordre doivent être documentées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `294. Separate buses possible` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0275`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0566 — 295. Recommendation

- Source: `SRC-005`
- Location: lines 9248–9256; heading `295. Recommendation`
- Domain tags: DATA, PRODUCT, ARCH
- Source statement: 295. Recommendation: single core decision event loop avec workers de calcul autour.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `295. Recommendation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0276`; supporting items: none found by conservative heading match; domain indexes `DATA, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0567 — 296. Parallel workers

- Source: `SRC-005`
- Location: lines 9257–9266; heading `296. Parallel workers`
- Domain tags: DATA, ROUTING
- Source statement: 296. Parallel workers: Peuvent traiter : route simulation
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `296. Parallel workers` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0277`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0568 — 297. Stale worker result

- Source: `SRC-005`
- Location: lines 9267–9278; heading `297. Stale worker result`
- Domain tags: DATA
- Source statement: 297. Stale worker result: Chaque résultat worker transporte : Si state actuel a trop changé :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `297. Stale worker result` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0278`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0569 — 298. No stale prediction commit

- Source: `SRC-005`
- Location: lines 9279–9290; heading `298. No stale prediction commit`
- Domain tags: DATA, PRODUCT
- Source statement: 298. No stale prediction commit: Un modèle calculé sur : ne peut pas automatiquement décider sur :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `298. No stale prediction commit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0279`; supporting items: none found by conservative heading match; domain indexes `DATA, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0570 — 299. Prediction TTL

- Source: `SRC-005`
- Location: lines 9291–9298; heading `299. Prediction TTL`
- Domain tags: DATA
- Source statement: 299. Prediction TTL: Chaque forecast possède : valid_until
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `299. Prediction TTL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0280`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0571 — 300. Dataset version in every experiment

- Source: `SRC-005`
- Location: lines 9299–9306; heading `300. Dataset version in every experiment`
- Domain tags: DATA
- Source statement: 300. Dataset version in every experiment: Toute sortie R&D : run_id
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `300. Dataset version in every experiment` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0281`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0572 — 301. ExperimentResult

- Source: `SRC-005`
- Location: lines 9307–9322; heading `301. ExperimentResult`
- Domain tags: DATA
- Source statement: 301. ExperimentResult: ExperimentResult { run_id,
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `301. ExperimentResult` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0282`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0573 — 302. No notebook-only result

- Source: `SRC-005`
- Location: lines 9323–9330; heading `302. No notebook-only result`
- Domain tags: DATA
- Source statement: 302. No notebook-only result: Une conclusion importante doit avoir : Pas seulement une cellule notebook.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `302. No notebook-only result` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0283`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0574 — 303. Research reproducibility

- Source: `SRC-005`
- Location: lines 9331–9341; heading `303. Research reproducibility`
- Domain tags: DETERMINISM, RESEARCH, DATA, CLOCK
- Source statement: 303. Research reproducibility: Un autre run doit pouvoir reconstruire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `303. Research reproducibility` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-DET-0013`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, RESEARCH, DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0575 — 304. Python environment

- Source: `SRC-005`
- Location: lines 9342–9349; heading `304. Python environment`
- Domain tags: DATA, ARCH
- Source statement: 304. Python environment: À versionner également : dependencies
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `304. Python environment` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0284`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0576 — 305. Production build reproducibility

- Source: `SRC-005`
- Location: lines 9350–9358; heading `305. Production build reproducibility`
- Domain tags: DETERMINISM, PRODUCT, DEPLOYMENT
- Source statement: 305. Production build reproducibility: Docker build lié à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `305. Production build reproducibility` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0014`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, PRODUCT, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0577 — 306. Schema compatibility gate on startup

- Source: `SRC-005`
- Location: lines 9359–9368; heading `306. Schema compatibility gate on startup`
- Domain tags: DATA
- Source statement: 306. Schema compatibility gate on startup: Le bot vérifie : model feature schema
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `306. Schema compatibility gate on startup` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0285`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0578 — 307. Incompatible model

- Source: `SRC-005`
- Location: lines 9369–9375; heading `307. Incompatible model`
- Domain tags: DATA
- Source statement: 307. Incompatible model: MODEL_SCHEMA_INCOMPATIBLE → stratégie dépendante désactivée.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `307. Incompatible model` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0286`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0579 — 308. Incompatible state

- Source: `SRC-005`
- Location: lines 9376–9378; heading `308. Incompatible state`
- Domain tags: DATA, RECONCILIATION
- Source statement: 308. Incompatible state: → reconciliation/rebuild.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `308. Incompatible state` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0287`; supporting items: none found by conservative heading match; domain indexes `DATA, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0580 — 309. Incompatible config

- Source: `SRC-005`
- Location: lines 9379–9381; heading `309. Incompatible config`
- Domain tags: DATA
- Source statement: 309. Incompatible config: → boot failure.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `309. Incompatible config` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0288`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0581 — 310. No silent migration live

- Source: `SRC-005`
- Location: lines 9382–9390; heading `310. No silent migration live`
- Domain tags: DATA
- Source statement: 310. No silent migration live: Les migrations de state importantes sont :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `310. No silent migration live` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0289`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0582 — 311. Data contracts form part of API

- Source: `SRC-005`
- Location: lines 9391–9393; heading `311. Data contracts form part of API`
- Domain tags: DATA, ARCH
- Source statement: 311. Data contracts form part of API: Même si tous les modules sont dans le même repository.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `311. Data contracts form part of API` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0290`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0583 — 312. Module boundaries

- Source: `SRC-005`
- Location: lines 9394–9402; heading `312. Module boundaries`
- Domain tags: DATA, ARCH
- Source statement: 312. Module boundaries: Exemple : BookEngine
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `312. Module boundaries` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0291`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0584 — 313. RouteEngine

- Source: `SRC-005`
- Location: lines 9403–9413; heading `313. RouteEngine`
- Domain tags: DATA, ROUTING, ACCOUNTING
- Source statement: 313. RouteEngine: input: BookSnapshotRefs
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `313. RouteEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0292`; supporting items: none found by conservative heading match; domain indexes `DATA, ROUTING, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0585 — 314. ParticipantEngine

- Source: `SRC-005`
- Location: lines 9414–9423; heading `314. ParticipantEngine`
- Domain tags: DATA, PARTICIPANTS
- Source statement: 314. ParticipantEngine: input: FeatureSnapshot
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `314. ParticipantEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0293`; supporting items: none found by conservative heading match; domain indexes `DATA, PARTICIPANTS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0586 — 315. Simulator

- Source: `SRC-005`
- Location: lines 9424–9435; heading `315. Simulator`
- Domain tags: DATA, SIMULATOR
- Source statement: 315. Simulator: input: ExecutionPlanCandidate
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `315. Simulator` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0294`; supporting items: none found by conservative heading match; domain indexes `DATA, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0587 — 316. RiskEngine

- Source: `SRC-005`
- Location: lines 9436–9446; heading `316. RiskEngine`
- Domain tags: DATA, RISK
- Source statement: 316. RiskEngine: input: RiskSnapshot
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `316. RiskEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0295`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0588 — 317. ExecutionCoordinator

- Source: `SRC-005`
- Location: lines 9447–9456; heading `317. ExecutionCoordinator`
- Domain tags: DATA
- Source statement: 317. ExecutionCoordinator: input: ExecutionPlan
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `317. ExecutionCoordinator` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0296`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0589 — 318. InventoryEngine

- Source: `SRC-005`
- Location: lines 9457–9467; heading `318. InventoryEngine`
- Domain tags: DATA, INVENTORY, EXECUTION
- Source statement: 318. InventoryEngine: input: FillEvents
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `318. InventoryEngine` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0297`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0590 — 319. No cyclic hidden dependencies

- Source: `SRC-005`
- Location: lines 9468–9484; heading `319. No cyclic hidden dependencies`
- Domain tags: DATA, RISK
- Source statement: 319. No cyclic hidden dependencies: ne doit pas appeler :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `319. No cyclic hidden dependencies` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0298`; supporting items: none found by conservative heading match; domain indexes `DATA, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0591 — 320. Dependency direction

- Source: `SRC-005`
- Location: lines 9485–9504; heading `320. Dependency direction`
- Domain tags: DATA, RECONCILIATION, RISK, SIMULATOR, QUANT, ARCH
- Source statement: 320. Dependency direction: Idéalement : types
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `320. Dependency direction` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0299`; supporting items: none found by conservative heading match; domain indexes `DATA, RECONCILIATION, RISK, SIMULATOR, QUANT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0592 — 321. Domain types package

- Source: `SRC-005`
- Location: lines 9505–9512; heading `321. Domain types package`
- Domain tags: DATA
- Source statement: 321. Domain types package: Créer : src/domain/
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `321. Domain types package` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0300`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0593 — 322. Suggested structure

- Source: `SRC-005`
- Location: lines 9513–9539; heading `322. Suggested structure`
- Domain tags: DATA, EXECUTION, RISK, RECORDER, INFRA, SIMULATOR, PARTICIPANTS, INVENTORY
- Source statement: 322. Suggested structure: src/ ├── domain/
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `322. Suggested structure` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0301`; supporting items: none found by conservative heading match; domain indexes `DATA, EXECUTION, RISK, RECORDER, INFRA, SIMULATOR, PARTICIPANTS, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0594 — 323. Domain layer has no external APIs

- Source: `SRC-005`
- Location: lines 9540–9549; heading `323. Domain layer has no external APIs`
- Domain tags: DATA, RECORDER
- Source statement: 323. Domain layer has no external APIs: Les types fondamentaux ne dépendent pas :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `323. Domain layer has no external APIs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0302`; supporting items: none found by conservative heading match; domain indexes `DATA, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0595 — 324. Adapter layer

- Source: `SRC-005`
- Location: lines 9550–9558; heading `324. Adapter layer`
- Domain tags: DATA, ARCH
- Source statement: 324. Adapter layer: Convertit : Hyperliquid external schemas
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `324. Adapter layer` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0303`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0596 — 325. Exchange schema changes isolated

- Source: `SRC-005`
- Location: lines 9559–9567; heading `325. Exchange schema changes isolated`
- Domain tags: DATA, ARCH
- Source statement: 325. Exchange schema changes isolated: Si Hyperliquid modifie un payload :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `325. Exchange schema changes isolated` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0304`; supporting items: none found by conservative heading match; domain indexes `DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0597 — 326. Data contract acceptance tests

- Source: `SRC-005`
- Location: lines 9568–9570; heading `326. Data contract acceptance tests`
- Domain tags: DATA
- Source statement: 326. Data contract acceptance tests: Avec fixtures de vrais payloads exchange.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `326. Data contract acceptance tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0305`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0598 — 327. Parser regression corpus

- Source: `SRC-005`
- Location: lines 9571–9579; heading `327. Parser regression corpus`
- Domain tags: DATA, QUANT, INFRA
- Source statement: 327. Parser regression corpus: Conserver plusieurs exemples : normal
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `327. Parser regression corpus` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0306`; supporting items: none found by conservative heading match; domain indexes `DATA, QUANT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0599 — 328. Unknown fields tolerant

- Source: `SRC-005`
- Location: lines 9580–9582; heading `328. Unknown fields tolerant`
- Domain tags: DATA, RECOVERY
- Source statement: 328. Unknown fields tolerant: Lorsque sûr.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `328. Unknown fields tolerant` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0307`; supporting items: none found by conservative heading match; domain indexes `DATA, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0600 — 329. Missing required field strict

- Source: `SRC-005`
- Location: lines 9583–9585; heading `329. Missing required field strict`
- Domain tags: DATA
- Source statement: 329. Missing required field strict: Pas inventer.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `329. Missing required field strict` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0308`; supporting items: none found by conservative heading match; domain indexes `DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0601 — 330. Final Determinism Contract

- Source: `SRC-005`
- Location: lines 9586–9669; heading `330. Final Determinism Contract`
- Domain tags: DETERMINISM, CLOCK
- Source statement: 330. Final Determinism Contract: Le système doit satisfaire : DecisionTrace = F( OrderedEvents, ResolvedConfig, ModelArtifacts, FormulaVersion, Seed )
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `330. Final Determinism Contract` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DET-0015`; supporting items: none found by conservative heading match; domain indexes `DETERMINISM, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0602 — 331. Final Data Contract Principle

- Source: `SRC-005`
- Location: lines 9670–9680; heading `331. Final Data Contract Principle`
- Domain tags: DATA, CLOCK
- Source statement: 331. Final Data Contract Principle: Chaque nombre utilisé pour décider doit avoir :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `331. Final Data Contract Principle` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0309`; supporting items: none found by conservative heading match; domain indexes `DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0603 — 332. Final State Principle

- Source: `SRC-005`
- Location: lines 9681–9692; heading `332. Final State Principle`
- Domain tags: DATA, INVENTORY, ARCH
- Source statement: 332. Final State Principle: Aucun module ne doit maintenir une « vérité parallèle » non traçable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `332. Final State Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0310`; supporting items: none found by conservative heading match; domain indexes `DATA, INVENTORY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0604 — 333. Final Replay Principle

- Source: `SRC-005`
- Location: lines 9693–9702; heading `333. Final Replay Principle`
- Domain tags: REPLAY
- Source statement: 333. Final Replay Principle: Replay ne doit pas être une imitation simplifiée du bot. Replay est le bot, connecté à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `333. Final Replay Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-REPLAY-0017`; supporting items: none found by conservative heading match; domain indexes `REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0605 — 334. Final Shadow Principle

- Source: `SRC-005`
- Location: lines 9703–9710; heading `334. Final Shadow Principle`
- Domain tags: DATA, VALIDATION
- Source statement: 334. Final Shadow Principle: Shadow est le bot, connecté au marché réel mais à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `334. Final Shadow Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0311`; supporting items: none found by conservative heading match; domain indexes `DATA, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0606 — 335. Final Micro-Live Principle

- Source: `SRC-005`
- Location: lines 9711–9718; heading `335. Final Micro-Live Principle`
- Domain tags: DATA, VALIDATION, RISK
- Source statement: 335. Final Micro-Live Principle: Micro-live est le bot Live, avec :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `335. Final Micro-Live Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-DATA-0312`; supporting items: SRC-001-ITEM-0018, SRC-006-ITEM-0418; domain indexes `DATA, VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0607 — 336. Final Production Principle

- Source: `SRC-005`
- Location: lines 9719–9744; heading `336. Final Production Principle`
- Domain tags: DATA, PRODUCT, EXECUTION, RISK, VALIDATION, REPLAY, CAPITAL, RESEARCH
- Source statement: 336. Final Production Principle: Le passage : Replay
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `336. Final Production Principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0313`; supporting items: SRC-006-ITEM-0263; domain indexes `DATA, PRODUCT, EXECUTION, RISK, VALIDATION, REPLAY, CAPITAL, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0608 — 337. Definition of Done — Data Contracts

- Source: `SRC-005`
- Location: lines 9745–9779; heading `337. Definition of Done — Data Contracts`
- Domain tags: DATA, VALIDATION, EXECUTION, DETERMINISM, OPERATIONS, REPLAY, ARCH
- Source statement: 337. Definition of Done — Data Contracts: Ce dossier est implémenté lorsque : all central domain types exist
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `337. Definition of Done — Data Contracts` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0314`; supporting items: SRC-006-ITEM-0278; domain indexes `DATA, VALIDATION, EXECUTION, DETERMINISM, OPERATIONS, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-005-ITEM-0609 — 338. Principe final

- Source: `SRC-005`
- Location: lines 9780–9877; heading `338. Principe final`
- Domain tags: DATA, FORMULA, REPLAY, ARCH
- Source statement: 338. Principe final: Notre système doit pouvoir répondre à n’importe quel moment : Qu’est-ce que le bot savait ?
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Risk Constitution, Schemas, Data Contracts and determinism.
- Candidate canonical interpretation: Preserve `338. Principe final` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DATA-0315`; supporting items: none found by conservative heading match; domain indexes `DATA, FORMULA, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 599
- Requirements contributed: 599
- Supporting references contributed: 77 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 0
- Research items: 6
- Open items: 3
- External revalidation items: 0
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
