# Legacy Gap Analysis

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

Comparaison effectuée après les huit extractions et le ledger initial. Le score lexical mesure la présence, pas la justesse; aucune affirmation legacy n’est promue automatiquement.

| Requirement | Concept | Legacy location | Coverage | Correct? | Incomplete? | Over-compressed? | Contradicted? | Absent? |
|---|---|---|---|---|---|---|---|---|
| REQ-BENCH-0001 | 23. Lock-free / ring buffers / zero-copy | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0001 | 24. Aucun appel bloquant pendant une opportunité | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0001 | 25. Vérifier le solde AVANT l'ordre | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0002 | 26. Tick size / lot size / min notional | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0001 | 27. Clock sync / timestamps | `docs/specs/ClockAndRng.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0001 | 28. Rate limits / retries | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0001 | 29. IOC/FOK plutôt que market aveugle | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0002 | 30. Partial fills = scénario normal, pas exception | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0001 | 31. Ne jamais dépendre d'une exécution atomique des 3 jambes | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0002 | 32. Kill switch de latence | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0003 | 33. Max slippage | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0003 | 34. Limites par trade et par asset | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0004 | 35. Circuit breakers | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-GRAPH-0001 | 36. Whitelist de liquidité | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0001 | 37. Filtre volume/liquidité | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0001 | 38. Paper/live avec le même code | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0001 | 39. Shadow mode | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0002 | 40. Micro-live | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0004 | 41. Recorder | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REPLAY-0001 | 42. Replay avec latence artificielle | `docs/_analysis/extracted/risk.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REPLAY-0002 | 43. Replay multi-size | `docs/_analysis/TRACEABILITY_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0005 | 44. Comparer simulation et vrai fill | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0006 | 45. Reason Codes | `docs/specs/MODULE_INDEX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0007 | 46. Observabilité complète | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-OPS-0001 | 47. Heartbeat / health monitoring | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0002 | 48. Persistance de l'état | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECON-0001 | 49. Redémarrage sûr | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0005 | 50. Clés API limitées | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0006 | 51. Config centralisée | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0002 | 52. Benchmarks avant optimisation extrême | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0002 | 53. Ne pas confondre CPU rapide et système rapide | `docs/specs/GlobalGraph.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0001 | 54. Seuil de profit minimal | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0001 | 55. Hystérésis / éviter le flip-flop | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0002 | 56. Opportunity cost | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0007 | 57. Auto-compounding : à garder avec prudence | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0008 | 58. Ce qu'on ne reprend PAS | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0003 | 1. D’abord : séparer architecture et validation | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0009 | 2. Première brique développée : Recorder + Market Graph | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0002 | 3. Phase 1 = Cartographier avant de chercher à gagner | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0008 | 4. Ne jamais tester seulement “le meilleur cas” | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0009 | Taille | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0001 | Latence | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0001 | Inventaire | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0010 | 5. Toujours comparer le théorique au réellement exécutable | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0002 | 6. Une hypothèse = une métrique = un critère de rejet | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0003 | Hypothèse | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0003 | Full graph | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-HWC-0001 | HOT/WARM/COLD | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RESEARCH-0004 | Hypothèse | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0002 | 7. HOT/WARM/COLD doit être backtesté comme une stratégie | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0003 | Policy A | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0002 | Policy B | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0004 | Policy C | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0003 | Policy D | `docs/specs/MarketAtlas.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0002 | 8. Même chose pour le capital | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0002 | 9. Le Bridge Engine doit avoir son propre protocole expérimental | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0001 | 10. Pas d’optimisation sur le même dataset que l’évaluation | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0011 | Walk-forward | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0003 | 11. Ne pas optimiser uniquement le PnL | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0010 | Version A | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0011 | Version B | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0004 | 12. Et surtout séparer les niveaux de PnL | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0003 | 13. Tests déterministes avant simulation marché | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0012 | Unit tests | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0001 | Route test | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0005 | Rounding tests | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0013 | Partial fill tests | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RECOV-0003 | Crash recovery tests | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0014 | 14. Puis tests adversariaux | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0003 | 15. Ensuite : Replay | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0005 | 16. Paper n’est pas suffisant | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0004 | 17. Différence Paper / Shadow | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0006 | PAPER | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0005 | SHADOW | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0006 | 18. Micro-live obligatoire | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0015 | 19. Scaling par paliers | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0007 | 20. Les critères GO / NO-GO doivent être définis avant les résultats | `docs/_analysis/extracted/testing.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0016 | 21. On garde également les résultats négatifs | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0002 | 22. Versionner absolument tout | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0003 | 23. Le benchmark informatique fait partie de la méthodologie | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-GRAPH-0004 | 24. Méthodologie spécifique à notre Global Graph | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0002 | CORE route | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0004 | SECONDARY | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BRIDGE-0003 | TRANSIT | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0005 | REJECTED | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-GRAPH-0005 | 25. Et on doit recalculer périodiquement cette cartographie | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0017 | 26. Notre méthode finale devient presque scientifique | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0005 | Et j'ajouterais une règle maîtresse pour notre direction actuelle | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0006 | A — Est-ce que ça augmente l’Expected Economic PnL ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0001 | B — Est-ce que ça améliore ou détériore le risque ? | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0004 | C — Combien de calcul/latence ça coûte ? | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0006 | 1. Le graphe structurel est mis à jour dès que Hyperliquid change | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0018 | 2. En temps réel, le bot maintient des statistiques courtes | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FUTURE-0001 | 3. On garde plusieurs fenêtres en parallèle | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0006 | FAST | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0007 | RECENT | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0003 | MEDIUM | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0006 | LONG | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0008 | 4. Exemple concret : ETH devient soudain intéressant | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-HWC-0007 | 5. WARM sert précisément à confirmer | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0003 | 6. Pourquoi je disais « ne pas modifier automatiquement les réglages dans le hot path » | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0004 | Ça peut être automatique en live : | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0005 | Ce que je ne veux PAS : | `docs/specs/CapabilityRegistry.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0009 | A. Dynamic State | `docs/specs/MarketAtlas.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0006 | B. Strategy Parameters | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0019 | 8. Comment actualiser ces paramètres alors ? | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FUTURE-0002 | 9. On peut même faire du Champion / Challenger | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0007 | 10. Et la cartographie elle-même devient un score roulant | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0008 | Boom temporaire | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0007 | Amélioration structurelle | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0005 | 11. Et l’hystérésis empêche le bot de devenir fou | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0020 | 12. Au final, notre système fonctionne sur trois vitesses | `docs/_analysis/extracted/deployment.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0021 | Exemple simple | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0001 | 1. La carte structurelle change rarement | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0007 | 2. Ce qui change tout le temps, c'est le MarketState | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0010 | 3. Les fenêtres sont mises à jour progressivement | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0004 | 4. Les routes sont également mises à jour par dépendance | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0008 | 5. Ensuite on met à jour le score de l'asset/cluster | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-HWC-0009 | 6. WARM déclenche ensuite une analyse plus poussée | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0009 | 7. Après le déplacement, la carte se met encore à jour | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-HWC-0010 | 8. Et quand ETH devient mauvais ? | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0008 | 9. Ce qui NE se met pas à jour automatiquement | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0002 | Mise à jour marché — permanente | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0012 | Mise à jour stratégique — contrôlée | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0022 | Exemple complet en 30 secondes de marché | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0023 | 1. Jour 1 : on construit la couche “observation” | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0024 | 2. Pendant ce temps, le Recorder tourne 24/7 | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0010 | Carte structurelle | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0011 | Carte économique | `docs/specs/MarketAtlas.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0003 | 3. On ne reste pas à attendre que le dataset soit terminé | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ATLAS-0001 | 4. Première utilisation des données : construire le Market Atlas | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0004 | 5. Ensuite le Replay Engine prend exactement ces données | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0006 | 6. Et on regarde comment son capital se déplace réellement | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0004 | 7. Ensuite on rejoue la même semaine avec différentes politiques | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-HWC-0011 | Test A | `docs/_analysis/OPEN_ITEMS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-HWC-0012 | Test B | `docs/_analysis/OPEN_ITEMS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-BRIDGE-0004 | Test C | `docs/_analysis/TRACEABILITY_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CAP-0007 | Test D | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0012 | Test E | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0013 | Test F | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0009 | 8. Ensuite seulement on calibre les paramètres | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0008 | 9. Puis le Shadow | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0009 | 10. Puis Micro-live | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0025 | Donc la chronologie exacte que je recommande | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0001 | Donc la correction importante à ta phrase : | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0010 | Bot hyperliquid : | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0014 | Donc notre scanner devrait chercher les deux | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0013 | 1. spotMeta → découvrir automatiquement toutes les paires Hyperliquid | `docs/_analysis/extracted/deployment.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-GRAPH-0008 | 2. Construire un graphe des tokens | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0005 | Pour le 2 jambes | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0006 | Pour le 3 jambes | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0007 | Le gros avantage : on ne recherche pas tout à chaque tick | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0002 | Concrètement, je préparerais 3 tables | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0014 | Exemple 3 jambes | `docs/_analysis/FINAL_AUDIT.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0015 | Pour le 2 jambes, même principe | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0016 | Ce que j'intégrerais concrètement | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0001 | 1. Book imbalance | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0026 | 2. Order Flow Imbalance | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0011 | 3. Profondeur | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0027 | Ce que ça donnerait dans notre moteur | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0010 | Ça devient particulièrement utile pour le 3 jambes | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PRODUCT-0001 | Important : je ne le mettrais pas dès V1 comme condition obligatoire | `docs/12_RECORDER_AND_REPLAY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0028 | Ce que ça change | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0002 | Mais le Queue Model doit être pré-calculé en continu | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0029 | Et on intègre directement 2 jambes + 3 jambes | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0030 | Même chose pour le sandbox | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0017 | Donc je voudrais directement ces modules | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FUTURE-0003 | Et surtout : pas de features “pour plus tard” | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0031 | Pourquoi ça peut être économiquement très intéressant | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0032 | Mais je ne ferais pas Maker sur n'importe quelle jambe | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0003 | Et là notre Queue Model devient central | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0018 | Et j'irais encore un peu plus loin dans l'architecture finale | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0033 | Mais je ne convertirais pas à chaque opportunité | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-ARCH-0019 | Mais tu viens immédiatement de pointer le problème suivant | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0011 | Inventory PnL | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0020 | Donc j'ajoute un moteur supplémentaire à notre architecture | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0021 | OUI | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0003 | NON | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0022 | Mais il faut distinguer deux types de coûts | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0034 | Coût directement nécessaire au trade | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0004 | Coût de constitution d'inventaire | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0035 | Et pour les shitcoins : je serais beaucoup plus sévère | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0015 | Et oui : volatilité intégrée directement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0036 | BTC | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0037 | SHITCOIN | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0023 | Pour les 3 jambes c'est encore plus important | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0004 | Et pour les actifs extrêmement volatils | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0005 | Encore mieux : hedger l'inventaire | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0024 | Notre architecture devient donc beaucoup plus propre | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0008 | Le vrai danger, comme tu le dis, c’est d’être bloqué | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0012 | Je construirais une vraie carte économique des actifs | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0038 | On peut même mesurer le risque d’être bloqué mathématiquement | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0009 | Donc le capital ne sera pas réparti arbitrairement | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-CAP-0010 | Et je mettrais une règle absolue : chaque inventaire doit avoir une sortie | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0039 | C'est donc ça que notre recorder doit cartographier avant le live | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0009 | 1. Graphe dynamique selon notre inventaire | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0040 | Je ferais plutôt trois états | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0007 | Pourquoi je garderais quand même les routes COLD | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0008 | Donc oui : « activation de routes » | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0009 | Ça peut même énormément réduire notre hot path | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0012 | Maintenant ton deuxième point : PnL route vs PnL global | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0013 | Exemple | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0006 | Donc règle : | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0041 | Alors à quoi sert le PnL global ? | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0014 | PnL global très positif | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0015 | PnL global très négatif | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0042 | Et ton exemple des 20 € devient intéressant | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0016 | Option A | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0016 | Option B | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0017 | Mais attention au piège inverse | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0017 | Je structurerais donc le Risk Engine en niveaux | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0018 | Leg Risk | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0019 | Route Risk | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0020 | Inventory Risk | `docs/specs/BridgeEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0018 | Global PnL | `docs/_analysis/CONTRADICTIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0007 | Exemple concret | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0010 | 1. Route Activation Engine ✅ | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0019 | 2. PnL hiérarchique ✅ | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0043 | Exemple concret | `docs/_analysis/extracted/execution.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0044 | 2. Ça confirme exactement notre idée d’inventaire BTC/ETH/HYPE/USDC. | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0045 | 3. Ça valide fortement notre logique Maker → Taker. | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0013 | 4. Ça donne une justification scientifique à notre obsession de la latence. | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0011 | 5. Ça valide aussi notre système de routes dynamiques | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0020 | 6. Et ça répond à ta question précédente sur le PnL | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0008 | 7. Le papier nous suggère même comment sélectionner nos actifs | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0025 | Tier A — inventaire autorisé | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0026 | Tier B — inventaire plafonné | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0005 | Tier C — transit uniquement | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0009 | Ce que je retiens directement du papier dans notre SPEC | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0006 | Pourquoi c’est particulièrement adapté à A → X → B | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0046 | Ce qui fait que c’est meilleur que “scanner tout à fond” | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-HWC-0013 | COLD | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0014 | WARM | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-HWC-0015 | HOT | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0014 | Mais je mettrais une exception importante | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0010 | 1. Global Market Graph | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0007 | 2. Inventory Graph | `docs/specs/CapitalReachabilityEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0012 | 3. Route Activation Engine | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0011 | 4. Global Watcher | `docs/_analysis/extracted/architecture.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0015 | Et ça améliore aussi notre stratégie économique | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0011 | Et pour A → X → B, petit point essentiel | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0012 | Donc oui : je la figerais. | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0047 | Exemple | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FUTURE-0004 | Il faut compter aussi la sortie future | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0003 | Mais surtout : il doit savoir combien de circuits sont probablement disponibles | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0013 | Et tu as raison sur le temps de conversion | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-HWC-0016 | Ça transforme HOT/WARM/COLD en quelque chose de plus intelligent | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0021 | Et comment choisir le pont ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-CAP-0014 | Le calcul principal du Capital Relocation Engine | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0027 | Rester BTC | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-TRI-0001 | Déplacer vers ETH | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0021 | Et le nombre de circuits devient une métrique native | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0013 | 1. spotMeta = la carte complète du terrain | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0022 | 2. Le Fee Engine devient beaucoup plus important que juste “0,07 %” | `docs/_analysis/extracted/testing.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0023 | Arbitrage 3 jambes | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0014 | Route 2 jambes | `docs/decisions/ADR-010-recovery-first-class.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0024 | Pont | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0028 | Sortie finale | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0048 | Et ça permet exactement ton calcul de “combien de circuits pour amortir le pont” | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0015 | 3. l2Book = savoir combien la route rapporte vraiment | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0029 | Exemple avec notre direction actuelle | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0030 | Pont A | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BRIDGE-0005 | Pont B | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0022 | Et l2Book nous donne aussi la taille maximale rentable | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0017 | Et ça améliore énormément HOT/WARM/COLD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0018 | COLD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0019 | WARM | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0020 | HOT | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0025 | Surtout, ça permet un truc que je trouve très important | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0049 | Au final, les trois briques s'emboîtent comme ça | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0016 | 1. Le plus important : 0,5 ms de calcul ne sert à rien avec 500 ms d’information | `docs/_analysis/extracted/risk.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0026 | 2. On doit intégrer un Feed Abstraction Layer | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0021 | 3. Ça améliore directement notre HOT / WARM / COLD | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0022 | COLD | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0023 | WARM | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0024 | HOT | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0023 | 4. Le Public WS reste très utile | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-ACCT-0027 | 5. Ça nous donne une nouvelle métrique fondamentale | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0004 | 6. Et ça nous indique probablement où devra vivre le bot final | `docs/decisions/SUPERSEDED_DECISIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-NODE-0001 | Node Hyperliquid | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0031 | 7. Mais il y a encore un problème pour le spot | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0002 | 8. Ce que je changerais dans notre structure finale | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-GRAPH-0012 | Et ça change notre phase de cartographie | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0032 | Question A — économique | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0017 | Question B — technologique | `docs/_analysis/OPEN_ITEMS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0024 | Donc la conclusion pour notre direction | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0018 | 1. On copie ses bonnes idées d’infrastructure | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0050 | 2. Son mécanisme de sécurité est très intéressant pour nous | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0033 | 3. On peut l'utiliser comme laboratoire pour notre architecture Rust | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0019 | Là où je ne l'utiliserais PAS aujourd'hui | `docs/decisions/ADR-017-no-black-scholes-core.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0051 | À court terme je ferais donc ça | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0020 | Et on peut déjà faire une expérience très utile avec lui | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-NODE-0002 | Et le non-validator node lui-même peut quand même nous servir | `docs/decisions/SUPERSEDED_DECISIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0028 | Ça devient même utile pour vérifier les données | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-HWC-0025 | Et il y a un lien direct avec HOT / WARM / COLD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0052 | Donc ma décision serait : | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0034 | 1. Le cœur Rust | `docs/16_VALIDATION_MATRIX.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REPLAY-0005 | 2. Pourquoi même le Replay doit être Rust | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0035 | 3. Python sert à être intelligent, pas rapide | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0004 | 4. Queue Model : les deux langages | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0026 | 5. HOT/WARM/COLD en Rust | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0029 | 6. Le PnL reste également dans le core | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0053 | 7. Recorder : finalement Rust aussi | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0011 | 8. Sur ton Mac mini M4 | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0021 | 9. En production : Tokyo | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0022 | 10. Mais je séparerais le node du bot | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0054 | 11. C | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0036 | Par contre, avant de coder certains modules, j’en approfondirais 3 | `docs/README.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0012 | Les autres, je les garderais comme validation scientifique | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0055 | La priorité devrait maintenant changer | `docs/_analysis/OPEN_ITEMS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0025 | Taille dynamique selon la profondeur | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0056 | À mettre | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0030 | Fee Engine centralisé | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0037 | À mettre | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0016 | Invalider les routes lorsque les règles changent | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0038 | À mettre | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0023 | WebSocket natif plutôt que REST | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0024 | À mettre | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0039 | Resynchronisation du carnet | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0004 | À mettre | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0006 | Top-K / cercle actif | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0057 | À mettre | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0026 | Logs de latence détaillés | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0025 | À mettre | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0026 | CPU pour le hot path | `docs/15_SECURITY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0027 | CPU | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0040 | GPU | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0028 | FPGA | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0029 | À mettre | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0058 | 1. asyncio → Tokio | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-PRODUCT-0002 | 2. uvloop → plus nécessaire | `docs/17_IMPLEMENTATION_ROADMAP.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CLOCK-0003 | 3. Parsing rapide → toujours extrêmement important | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0059 | 4. Keep-alive → toujours indispensable | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0030 | 5. “Parallélisation” : là il faut être beaucoup plus subtil | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0060 | Concurrence | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0017 | Parallélisme du hot path | `docs/_analysis/TRACEABILITY_MATRIX.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0018 | Ce que je veux concrètement pour notre hot path | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0041 | Architecture de threads que j'imagine | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0005 | Et notre Queue / volatilité ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0042 | Et Python dans tout ça ? | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0043 | Et surtout, ce que Rust ne règle PAS magiquement | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0027 | Et notre objectif +0,5 ms s'applique précisément ici | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0061 | Donc pour corriger précisément le point 22 | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0062 | Source preamble | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0063 | Deuxième raison : comparer simulation et réalité | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0031 | Troisième raison : le marché change | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0064 | Mais ça ne signifie PAS qu’on doit garder 20 Go/jour éternellement | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0065 | Donc le stockage prod pourrait être nettement plus petit | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0044 | 1. Architecture commune | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0019 | 2. TEST / R&D : objectif = construire notre historique propriétaire | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0066 | On enregistre quasiment tout le spot pertinent | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0001 | 3. Donnée RAW de test | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REC-0002 | 4. Le RAW est découpé en petits chunks | `docs/12_RECORDER_AND_REPLAY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0005 | 5. Ensuite le RAW produit un dataset NORMALIZED | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0032 | 6. Puis on génère les données DERIVED | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0067 | 7. Comment les données s'accumulent en phase test | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0006 | 8. Ton SSD 1 To en TEST | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0003 | 9. iCloud en phase TEST | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0045 | SSD | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0046 | iCloud | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0006 | Mac | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0068 | 10. Mais ne jamais écrire directement vers iCloud | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0010 | 11. La rétention pendant la recherche | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0047 | RAW | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0048 | NORMALIZED | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0049 | DERIVED | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0007 | GOLDEN DATASETS | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0028 | 12. Puis on développe et teste le bot sur ces données | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0008 | 13. En TEST, on peut rejouer le même marché 100 fois | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0050 | Run A | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0051 | Run B | `docs/specs/RouteEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0031 | Run C | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0009 | 14. TEST : le dataset grossit jusqu'à ce qu'on possède assez de régimes | `docs/16_VALIDATION_MATRIX.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PRODUCT-0003 | 15. Puis passage en PRODUCTION | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0004 | 16. Pourquoi continuer à enregistrer le marché en production | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0005 | 17. Production : beaucoup plus sélectif sur la rétention | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0006 | 18. Ce qu'on garde longtemps en production | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0069 | Executions | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0020 | Opportunities | `docs/18_OPERATIONS_AND_MONITORING.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-INV-0008 | Inventory | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0052 | Latencies | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0053 | Derived features | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OPS-0002 | Incidents | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0054 | 19. Market windows autour des vrais ordres | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0007 | 20. Exemple production | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PRODUCT-0008 | 21. Production : structure physique | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0004 | 22. Ensuite archive | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PRODUCT-0009 | 23. Object storage production | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0005 | 24. Donc on automatise la suppression | `docs/12_RECORDER_AND_REPLAY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0070 | 25. Production : le Recorder ne doit jamais remplir le disque | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0021 | 26. On sépare encore le hot path | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0071 | 27. Account/Execution data a priorité sur Market RAW | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0055 | P0 | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OPS-0003 | P1 | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0056 | P2 | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0057 | P3 | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PRODUCT-0010 | 28. Production sert aussi à améliorer notre simulateur | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ATLAS-0002 | 29. Production enrichit donc continuellement notre Market Atlas | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0072 | 30. Synchronisation TEST ↔ PROD | `docs/12_RECORDER_AND_REPLAY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OPS-0004 | 31. Exemple d'incident | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0006 | 32. Structure globale TEST | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0073 | 33. Structure globale PROD | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0007 | 34. Rétention que je choisirais comme point de départ | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0058 | 35. Avec ton matériel actuellement | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0059 | SSD Mac 1 To | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0060 | iCloud 2 To | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0032 | 36. La première métrique qu'on programme | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0061 | La règle finale | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0011 | Pendant la recherche | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0011 | Pendant la production | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0074 | Et dans les deux cas | `docs/_analysis/extracted/deployment.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0075 | Exemple | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0027 | On pourra même tester ton idée HOT/WARM/COLD proprement | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0033 | Sans optimisation | `docs/_analysis/extracted/quant.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0076 | Notre version | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0007 | Idem pour les bridges | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0062 | Policy A | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0063 | Policy B | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0029 | Policy C | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0030 | Policy D | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0077 | Et on peut tester le temps | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0031 | Limite importante | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0078 | On pourra également améliorer le simulateur lui-même | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0064 | On pourra même tester des idées qu'on n'avait pas encore au moment de l'enregistrement | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0032 | Ce qu'on ne pourra jamais simuler parfaitement | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-EXEC-0079 | Donc notre boucle d'amélioration finale devient très puissante | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0080 | À terme, on pourra quasiment demander au système | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OWA-0001 | 1. Sur un même exchange : ce n’est pas rare du tout | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0033 | 2. Mais d’où vient réellement ce profit ? | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0081 | 3. Pourquoi peut-il y avoir cette incohérence sur LE MÊME exchange ? | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0012 | 4. Les études identifient plusieurs causes concrètes | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0065 | 5. Et il y a une autre source importante : la profondeur | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0066 | Direct BTC → ETH | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0067 | BTC → HYPE | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0033 | HYPE → ETH | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0082 | 6. Et le phénomène est suffisamment fréquent pour être automatisé à très haute vitesse | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0034 | 7. Mais attention : les profits individuels ont énormément diminué | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0035 | 8. Et ça change notre raisonnement sur le PnL | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XEX-0001 | 9. Maintenant : multi-exchange | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XEX-0002 | 10. Est-ce que les écarts multi-exchange arrivent aussi ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0083 | 11. Le problème cross-exchange : le capital doit être présent AVANT l'opportunité | `docs/_analysis/extracted/risk.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0015 | 12. Mais le capital se déséquilibre | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0068 | Hyperliquid | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0034 | Binance | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0035 | 13. Donc quel type produit les plus gros écarts ? | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0005 | 14. Il existe aussi des inefficiences ultra-courtes ENTRE exchanges | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SEC-0002 | 15. Maintenant la question essentielle : lequel pour NOTRE projet ? | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0069 | 16. Mais je ferais une modification architecture MAINTENANT | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-GRAPH-0013 | rendre le graphe venue-aware. | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0036 | 17. Et surtout : je veux maintenant distinguer 3 choses dans notre “2-leg” | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RESEARCH-0013 | 18. Et le papier de 2020 nous donne même une information essentielle sur la concurrence | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0084 | 19. Ils ont même observé comment les bots géraient la perte | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0085 | Ma conclusion pour notre projet | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OWA-0002 | 1. Définition exacte : qu’est-ce qu’un vrai OWA 2-leg ? | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0037 | 2. Première correction importante | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0022 | 3. Fonction fondamentale : NetConvert() | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0012 | 4. Exemple SELL | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-GRAPH-0014 | 5. Exemple BUY | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0023 | 6. Calcul du DIRECT | `docs/_analysis/CONTRADICTIONS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0024 | 7. Calcul de l’INDIRECT | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OWA-0003 | 8. Edge OWA véritable | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0038 | 9. Les fees ne sont jamais ajoutés “à la louche” | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0005 | 10. Le benchmark DIRECT doit être équitable | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0086 | 11. Famille IMMEDIATE_OWA | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0087 | 12. Famille PASSIVE_OWA | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0088 | 13. Plans d’exécution 2-leg que l’on GARDE | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0089 | 14. Plans que l’on N’UTILISE PAS par défaut | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OWA-0004 | 15. Un OWA n’existe PAS sans comparateur | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0008 | 16. Deuxième distinction essentielle : OWA vs relocation | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0025 | 17. ConversionAlpha | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0009 | 18. RelocationValue | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0039 | 19. Pourquoi ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0009 | 20. Classification des assets | `docs/decisions/SUPERSEDED_DECISIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0010 | 21. CORE_INVENTORY | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RECOV-0008 | 22. TRANSIT | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0040 | 23. EXCLUDED | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0010 | 24. Terminal Viability Gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-EXEC-0090 | 25. Cela résout notre problème des “40 opportunités” | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0041 | 26. Inventaire avant/après | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INV-0011 | 27. Inventory bands | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0036 | 28. Effet des limites | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0037 | 29. Flow control | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0026 | 30. Valeur d’une route ajustée à l’inventaire | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0042 | 31. Attention : ce n’est PAS une autorisation de perdre | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0014 | 32. Risque d’exécution entre Leg1 et Leg2 | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0009 | 33. Donc edge > 0 ne suffit jamais | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0091 | 34. Version plus complète | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0010 | 35. Recovery n’est pas forcément X → B coûte que coûte | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0011 | 36. Notre Recovery Engine cherche le minimum de perte | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RESEARCH-0015 | 37. Latence : ce que les papiers nous apprennent réellement | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0092 | 38. Ce qu’on NE fait PAS avec cette information | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-SIZE-0001 | 39. Sizing : une route n’a jamais une rentabilité unique | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0038 | 40. Fonction de capacité | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIZE-0002 | 41. Contraintes du sizing | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0039 | 42. On ne fixe donc PAS 50 € comme taille économique | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SLICE-0001 | 43. Fragmentation : ce qu’on garde | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SLICE-0002 | 44. Ce qu’on ne garde PAS | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-CAP-0016 | 45. Shared Capacity | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INV-0012 | 46. Reservation Engine | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0027 | 47. Le moteur ne sélectionne donc plus “la meilleure route” | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XEX-0003 | 48. Cross-exchange 2-leg : définition séparée | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XEX-0004 | 49. Calcul cross-exchange | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0043 | 50. Mais il existe un coût caché : le déséquilibre de venue | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0013 | 51. On ne doit PAS affecter naïvement un “frais de rebalance complet” à chaque trade | `docs/_analysis/extracted/risk.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0013 | 52. On utilise un InventoryShadowCost | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0014 | 53. Exemple | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-XEX-0005 | 54. Cross-exchange : règle absolument non négociable | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XEX-0006 | 55. Activation cross-exchange dans notre projet | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0044 | 56. Accounting : les PnL qu’il faut stocker séparément | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0045 | 57. Important : ne jamais confondre ConversionAlpha et PortfolioPnL | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0093 | 58. Pipeline exact d’une opportunité same-venue | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0094 | 59. Pseudo-décision | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0012 | 60. Les choses que nous GARDONS définitivement | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0040 | 61. Les choses que nous supprimons/corrigeons définitivement | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0013 | 62. La métrique centrale finale du 2-leg | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0014 | 63. Mais les composantes restent enregistrées séparément | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0095 | 64. Conclusion de l’interrogation n°2 | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0070 | Comment éviter d’être épuisé | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0096 | 1. Des inventaires cibles par exchange | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0041 | 2. Donner une valeur au rééquilibrage | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0014 | 3. L’idéal : attendre les opportunités inverses | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0042 | 4. Si le marché reste dans la même direction trop longtemps | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0015 | Le moteur doit accumuler les besoins de rebalance | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0016 | Donc le vrai calcul du rebalance | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0043 | Attendre | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0017 | Rebalancer | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0018 | Il nous faut donc un Venue Inventory Engine | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0034 | On peut même réserver une capacité dans chaque direction | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ATLAS-0003 | Et notre Market Atlas doit mesurer le biais directionnel | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0071 | Et si le déséquilibre devient dangereux très rapidement ? | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0013 | A. Stopper cette direction | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0044 | B. Réduire les tailles | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0072 | C. Favoriser fortement la direction inverse | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0019 | D. Rebalance physique | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0015 | E. Éventuellement utiliser des dérivés comme hedge temporaire | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0045 | Et il ne faut surtout pas attendre d’être à zéro | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CAP-0017 | Exemple complet | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PRODUCT-0014 | Opportunités 1–10 | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0046 | Opportunité 11 | `docs/decisions/ADR-006-capital-aware-compute.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0047 | Opportunité 20 | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0048 | Puis opportunité inverse | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0097 | C'est ce qui empêche réellement l'épuisement | `docs/README.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0098 | 1. Objectif | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0099 | 2. Principe fondamental : la stratégie ne contrôle jamais directement l’exchange | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0100 | 3. Les cinq automates distincts | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0101 | 4. EngineState — état global du bot | `docs/_analysis/extracted/execution.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0102 | 5. BOOTING | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0103 | 6. SYNCING | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0104 | 7. RECONCILING | `docs/specs/ReconciliationEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0105 | 8. READY | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0106 | 9. DEGRADED | `docs/README.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0107 | 10. RECOVERY_ONLY | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0108 | 11. HALTED | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0109 | 12. RouteExecutionState | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0110 | 13. DETECTED | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0111 | 14. VALIDATING | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0112 | 15. RESERVING | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0113 | 16. Pourquoi réserver avant d’envoyer | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0114 | 17. PLANNED | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0115 | 18. EXECUTING | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0116 | 19. OrderIntent | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0117 | 20. Pourquoi le CLOID est fondamental | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0118 | 21. Règle fondamentale : NO BLIND RETRY | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0119 | 22. OrderState | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | CHECK REGISTER | NO |
| REQ-EXEC-0120 | 23. CREATED | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0121 | 24. NONCE_ASSIGNED | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0122 | 25. NonceManager | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0123 | 26. SIGNED | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0124 | 27. SENT | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0125 | 28. PENDING_RESOLUTION | `docs/_analysis/extracted/execution.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0126 | 29. Event reducer plutôt que logique impérative fragile | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0127 | 30. Fills = événements économiques immuables | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0128 | 31. RESTING | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0129 | 32. PARTIALLY_FILLED | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0130 | 33. FILLED | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0131 | 34. REJECTED | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-EXEC-0132 | 35. UNKNOWN | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0133 | 36. CANCEL_REQUESTED | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0134 | 37. Cancel race | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0135 | 38. CANCELED | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0136 | 39. Terminal states | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0137 | 40. Source of truth | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0138 | 41. TT — 2-leg execution | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0139 | 42. Leg 1 TT | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0140 | 43. Leg 1 : zéro fill | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0141 | 44. Leg 1 : full fill | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0142 | 45. Revalidation avant Leg 2 | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0143 | 46. Continuation Decision | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0144 | 47. Si continuation reste optimale | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0145 | 48. Si continuation n’est plus optimale | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0146 | 49. Leg 1 partial fill | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0147 | 50. Partial continuation | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0148 | 51. Dust problem | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0149 | 52. Leg 2 partial fill | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0150 | 53. Quand une route TT est COMPLETED | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0151 | 54. MT — Maker/Taker | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0152 | 55. Maker leg lifecycle | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0153 | 56. Tant que maker repose | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0154 | 57. Maker stale condition | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0155 | 58. Maker partial fill | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0156 | 59. Politique recommandée pour MT | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0157 | 60. Small partial below minimum | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0158 | 61. Maker cancellation after partial | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0159 | 62. TTT — triangle taker | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0160 | 63. Important : triangle non atomique | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0161 | 64. Après chaque jambe TTT | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0162 | 65. MTT | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0163 | 66. TM et MM | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0164 | 67. Recovery State Machine | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0165 | 68. RECOVERY_REQUIRED | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0166 | 69. Recovery objective | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0167 | 70. Candidate exits | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0168 | 71. Recovery orders | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0169 | 72. Ne pas confondre perte et permission illimitée | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0170 | 73. Recovery split | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0171 | 74. Recovery failure | `docs/specs/Deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0172 | 75. RECONCILIATION State Machine | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0173 | 76. Sources utilisées | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0174 | 77. Reconciliation algorithm | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0175 | 78. Balance reconciliation | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0176 | 79. Startup after crash | `docs/specs/ExecutionCoordinator.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0177 | 80. Persistent Execution Journal | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0178 | 81. Crash consistency | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0179 | 82. Disconnect market feed | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0180 | 83. Disconnect account/order feed | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0181 | 84. Reconnect | `docs/_analysis/extracted/risk.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0182 | 85. Dead Man's Switch | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0183 | 86. Fonctionnement recommandé | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0184 | 87. Pourquoi pas pour IOC | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0185 | 88. Timers | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0186 | 89. ACK timeout | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0187 | 90. Maker maximum age | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0188 | 91. Route timeout | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0189 | 92. Protected price | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0190 | 93. Exchange ACK ≠ economic success | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0191 | 94. Actual fill accounting | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0192 | 95. Leg accounting | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0193 | 96. Route accounting | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0194 | 97. Execution ownership | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0195 | 98. Idempotency | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0196 | 99. Monotonicity | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0197 | 100. Important : état économique séparé de l’état transport | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0198 | 101. Reservations lifecycle | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0199 | 102. Never spend unknown capital | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0200 | 103. Risk reduction always has priority | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0201 | 104. Global PnL cannot alter execution safety | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0202 | 105. Rust modules | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0203 | 106. Structures principales | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0204 | 107. ExecutionState | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0205 | 108. LegExecutionState | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0206 | 109. OrderRecord | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0207 | 110. RejectReason taxonomy | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0208 | 111. Pourquoi stocker tous les rejects | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0209 | 112. Test obligatoire n°1 — Full IOC success | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0210 | 113. Test n°2 — Leg1 zero fill | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0211 | 114. Test n°3 — Leg1 partial | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0212 | 115. Test n°4 — Leg2 edge dies | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0213 | 116. Test n°5 — network timeout after submit | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0214 | 117. Test n°6 — duplicate WebSocket fill | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0215 | 118. Test n°7 — fill during cancellation | `docs/_analysis/extracted/execution.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0216 | 119. Test n°8 — process crash | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0217 | 120. Test n°9 — balance mismatch | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0218 | 121. Test n°10 — stale feed while maker resting | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0219 | 122. Property tests | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0220 | 123. Replay determinism requirement | `docs/specs/CounterfactualSimulator.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0221 | 124. Logging | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0222 | 125. Metrics | `docs/specs/InfrastructureMonitor.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0223 | 126. State transition latency | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0224 | 127. Interaction avec le Participant Model | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0225 | 128. Interaction avec le Simulator | `docs/REVIEW_REQUIRED.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0226 | 129. Interaction avec le Risk Engine | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0227 | 130. Interaction avec Inventory Engine | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0228 | 131. Interaction avec HOT/WARM/COLD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0229 | 132. Batching Hyperliquid | `docs/_analysis/extracted/execution.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0230 | 133. WebSocket POST vs HTTP POST | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0231 | 134. Execution State Machine — règle absolue | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0232 | 135. Deuxième règle absolue | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0233 | 136. Troisième règle absolue | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0234 | 137. Quatrième règle absolue | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0235 | 138. Cinquième règle absolue | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0236 | 139. Sixième règle absolue | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0237 | 140. Definition of Done de l’Execution State Machine | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0238 | 141. Architecture finale de cette brique | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0239 | 142. Conclusion | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0003 | 1. Statuts des formules | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0004 | 2. Conventions générales | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0005 | Prix | `docs/02_DOMAIN_MODEL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0006 | 3. Quantité | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0007 | 4. Convention PnL | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0008 | 5. Basis points | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0009 | 6. FORMULA QF-001 — Mid Price | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0010 | Où | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0011 | Utilisation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0012 | Cas invalide | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0013 | 7. QF-002 — Absolute Spread | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0014 | 8. QF-003 — Relative Spread | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0015 | Pourquoi | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0016 | 9. QF-004 — Cumulative Base Depth | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0017 | 10. QF-005 — Cumulative Quote Depth | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0018 | Utilisation | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0019 | 11. QF-006 — Depth Within Price Band | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0020 | 12. QF-007 — Hyperliquid Size Quantization | `docs/specs/PrecisionEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0021 | 13. QF-008 — Hyperliquid Price Validity | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0022 | 14. QF-009 — Book Walk Base → Quote | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0023 | 15. QF-010 — Book Walk Quote → Base | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0024 | 16. QF-011 — VWAP | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0025 | 17. QF-012 — Mechanical Slippage BUY | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0026 | 18. QF-013 — Mechanical Slippage SELL | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0027 | 19. QF-014 — Fee Rate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0028 | 20. QF-015 — Fee Amount | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0029 | 21. QF-016 — NetConvert | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0030 | 22. QF-017 — Direct Route Output | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0031 | 23. QF-018 — 2-Leg Indirect Output | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0032 | 24. QF-019 — OWA Relative Edge | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0033 | 25. QF-020 — OWA Absolute Gain | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0034 | 26. QF-021 — Triangular Output | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0035 | 27. QF-022 — Triangle Return | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0036 | 28. QF-023 — Triangle PnL | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0037 | 29. QF-024 — Conversion Alpha | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0038 | 30. QF-025 — Execution Alpha | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0039 | 31. QF-026 — Edge Curve | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0040 | 32. QF-027 — Maximum Profitable Size | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0041 | 33. QF-028 — Queue Imbalance | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0042 | 34. QF-029 — Multi-Level Imbalance | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0043 | 35. QF-030 — Event-Level Bid OFI Contribution | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0044 | 36. QF-031 — Ask OFI Contribution | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0045 | 37. QF-032 — OFI | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0046 | Important | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0047 | 38. QF-033 — Multi-Level OFI | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0048 | 39. QF-034 — Microprice | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0049 | 40. QF-035 — Microprice Dislocation | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0050 | 41. QF-036 — Log Return | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0051 | 42. QF-037 — Realized Variance | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0052 | 43. QF-038 — Realized Volatility | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0053 | 44. QF-039 — Robust Jump Score | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0054 | 45. QF-040 — Depth Participation | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0055 | 46. QF-041 — Volume Participation | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0056 | Pourquoi | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0057 | 47. QF-042 — Mechanical Impact | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0058 | 48. QF-043 — Liquidity Resilience | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0059 | 49. QF-044 — Survival Function | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0060 | 50. QF-045 — Discrete Hazard | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0061 | 51. QF-046 — Survival from Discrete Hazard | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0062 | 52. QF-047 — Edge Half-Life | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0063 | 53. QF-048 — Capture Probability | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0064 | 54. QF-049 — Expected Edge at Arrival | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0065 | 55. QF-050 — Probability Above Execution Threshold | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0066 | 56. QF-051 — Maker Fill Survival | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0067 | 57. QF-052 — Maker Fill CDF | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0068 | 58. QF-053 — Expected Fill Time | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0069 | 59. QF-054 — Adverse Selection BUY | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0070 | 60. QF-055 — Adverse Selection SELL | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0071 | 61. QF-056 — Expected Value | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0072 | 62. QF-057 — Execution EV | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0073 | 63. QF-058 — MT EV | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0074 | 64. QF-059 — Probability of Positive PnL | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0075 | 65. QF-060 — Loss Variable | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0076 | 66. QF-061 — VaR | `docs/_analysis/extracted/execution.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0077 | 67. QF-062 — CVaR / Expected Shortfall | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0078 | 68. QF-063 — Risk-Adjusted EV | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0079 | 69. QF-064 — Normalized Inventory Deviation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0080 | 70. QF-065 — Soft Inventory Penalty | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0081 | 71. QF-066 — Hard Inventory Gate | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0082 | 72. QF-067 — Net Flow | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0083 | 73. QF-068 — Expected Exit Cost | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0084 | 74. QF-069 — Stranded Capital Penalty | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0085 | 75. QF-070 — Bridge Cost | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0086 | 76. QF-071 — Bridge Break-Even Cycles | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0087 | 77. QF-072 — Capital Relocation Value | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0088 | 78. QF-073 — Available Balance | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0089 | 79. QF-074 — Available Book Capacity | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0090 | 80. QF-075 — Position Sizing Objective | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0091 | 81. QF-076 — Validated Capacity | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0092 | 82. QF-077 — Sizing Search | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0093 | 83. QF-078 — Multi-Opportunity Allocation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0094 | 84. QF-079 — Recovery Objective | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0095 | 85. QF-080 — Recovery Loss | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0096 | 86. QF-081 — Cross-Market Response | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0097 | 87. QF-082 — Correction Velocity | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0098 | 88. QF-083 — Competition Hazard | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0099 | 89. QF-084 — Infrastructure Latency | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0100 | 90. QF-085 — Opportunity Capture vs Infrastructure | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0101 | 91. QF-086 — Infrastructure Gross PnL Difference | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0102 | 92. QF-087 — Incremental Infrastructure Cost | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0103 | 93. QF-088 — Net Upgrade Value | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0104 | 94. QF-089 — Infrastructure ROI | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0105 | 95. QF-090 — Infrastructure Net PnL | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0106 | 96. QF-091 — Infrastructure Upgrade Gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0107 | 97. QF-092 — Infrastructure Efficiency | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0108 | 98. QF-093 — Capture Ratio | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0109 | 99. QF-094 — Opportunity Survival Rate Empirique | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0110 | 100. QF-095 — Brier Score | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0111 | 101. QF-096 — Log Loss | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0112 | 102. QF-097 — Prediction Error PnL | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0113 | 103. QF-098 — Slippage Prediction Error | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0114 | 104. QF-099 — Fill Calibration Error | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0115 | 105. QF-100 — Model Economic Lift | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0116 | 106. QF-101 — Quant Model Value After Latency Cost | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0117 | 107. QF-102 — Model Disagreement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0118 | 108. QF-103 — OOD Distance | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0119 | 109. QF-104 — Simulation Confidence | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0120 | 110. QF-105 — Expected Idle Capital Cost | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0121 | 111. QF-106 — Economic PnL global | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0122 | 112. QF-107 — Inventory Mark-to-Market | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0123 | 113. QF-108 — Total Strategy PnL | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0124 | 114. QF-109 — Drawdown | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0125 | 115. QF-110 — Maximum Drawdown | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-FORMULA-0126 | 116. Les formules volontairement NON intégrées | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0127 | 117. Ce qui est mathématiquement figé | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0128 | 118. Ce qui DOIT attendre les données | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0129 | 119. Principe important : paramètres ≠ architecture | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0130 | 120. Formula Registry | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0131 | 121. Golden Formula Tests | `docs/_analysis/extracted/quant.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0132 | 122. Golden Book-Walk Test | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0133 | 123. Precision Golden Tests | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0134 | 124. Python/Rust Parity | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0135 | 125. Calculs monétaires critiques | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0136 | 126. Ordre exact des calculs d’une route | `docs/_analysis/extracted/quant.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0137 | 127. Formule conceptuelle finale du bot | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0138 | 128. Principe final du Formula Book | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0139 | 129. Résumé des objets mathématiques centraux | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0046 | 1. Objectif | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0047 | 2. Principe constitutionnel principal | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0048 | HARD INVARIANT | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0049 | CALIBRATED POLICY | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0050 | 4. Ordre de priorité du système | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0051 | 5. Risk Layers | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0052 | 6. Principe : Global PnL ne relaxe jamais Leg Risk | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0053 | 7. INV-001 — No Trade Without Valid Market State | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0054 | 8. INV-002 — No Trade On Stale Book | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0055 | 9. INV-003 — Route Freshness = Worst Leg Freshness | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0056 | 10. INV-004 — No Unknown Metadata | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0057 | 11. INV-005 — Fees Must Be Known | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0058 | 12. INV-006 — Exchange Precision Is Mandatory | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0059 | 13. INV-007 — No Negative Available Balance | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0060 | 14. INV-008 — Unknown Capital Is Reserved Capital | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0061 | 15. INV-009 — No Double Spending | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0062 | 16. INV-010 — Reservations Before Orders | `docs/09_RISK_CONSTITUTION.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-RISK-0063 | 17. INV-011 — Shared Depth Cannot Be Double Counted | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0064 | 18. INV-012 — Actual Fill Beats Expected Fill | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0065 | 19. INV-013 — Next Leg Uses Actual Previous Fill | `docs/09_RISK_CONSTITUTION.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-RISK-0066 | 20. INV-014 — No Blind Retry | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0067 | 21. INV-015 — Cancel Sent ≠ Canceled | `docs/_analysis/extracted/execution.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0068 | 22. INV-016 — Partial Fill Creates Real Exposure | `docs/09_RISK_CONSTITUTION.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-RISK-0069 | 23. INV-017 — Existing Exposure Has Priority | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0070 | 24. INV-018 — Recovery May Be Negative EV | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0071 | 25. INV-019 — Recovery Is Not Unlimited | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0072 | 26. INV-020 — Sunk Costs Are Sunk | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0073 | 27. INV-021 — No Averaging Down By Default | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0074 | 28. INV-022 — No Martingale | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0075 | 29. INV-023 — No New Risk In RECOVERY_ONLY | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0076 | 30. INV-024 — No New Risk In HALTED | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0077 | 31. INV-025 — No Trading While Account State Is Unreconciled | `docs/09_RISK_CONSTITUTION.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-RISK-0078 | 32. INV-026 — Clock Must Be Healthy | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0079 | 33. INV-027 — Required Feeds Must Be Healthy | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0080 | 34. INV-028 — Trading Requires InfraHealth == ACCEPTABLE | `docs/09_RISK_CONSTITUTION.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-RISK-0081 | 35. Infra Health Inputs | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0082 | 36. INV-029 — Slow Compute Can Become a Risk Event | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0083 | 37. INV-030 — Recorder Must Never Block Execution | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0084 | 38. Market Risk Gates | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0085 | 39. Spread Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0086 | 40. Liquidity Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0087 | 41. Impact Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0088 | 42. Volume Participation Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0089 | 43. Jump Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0090 | 44. Volatility Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-RISK-0091 | 45. Competition / Survival Gates | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0092 | 46. Survival Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0093 | 47. Expected Arrival Edge Gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0094 | 48. Model Confidence Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0095 | 49. OOD Gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0096 | 50. Hard OOD | `docs/specs/SizingEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0097 | 51. Soft OOD | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0098 | 52. Model Disagreement Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0099 | 53. Simulation Gate | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0100 | 54. Positive PnL Probability Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0101 | 55. Expected PnL Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0102 | 56. Tail Risk Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0103 | 57. Max Single-Route Loss | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0104 | 58. Recovery Tail Risk | `docs/01_PRODUCT_AND_SCOPE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0105 | 59. Position Sizing Risk Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0106 | 60. No Fixed Universal Trade Size | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0107 | 61. Probe Mode | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0108 | 62. Inventory Constitution | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0109 | 63. Soft Inventory Region | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0110 | 64. Outside Soft Band | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0111 | 65. Hard Inventory Region | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0112 | 66. Risk-Reducing Exception | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0113 | 67. Net Flow Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0114 | 68. Inventory Concentration | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0115 | 69. Transit Asset Risk | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0116 | 70. Stranded Asset Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0117 | 71. Terminal Viability Gate | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0118 | 72. Bridge Risk | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0119 | 73. Bridge Cannot Hide Arbitrage Loss | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0120 | 74. Relocation Hysteresis | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0121 | 75. Maker Risk Constitution | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0122 | 76. Maker Must Be ALO | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0123 | 77. Maker Maximum Exposure | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0124 | 78. Maker Maximum Age | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0125 | 79. Maker Edge Death | `docs/_analysis/TRACEABILITY_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0126 | 80. Maker Toxicity Gate | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0127 | 81. Maker Fill Must Trigger Immediate Reassessment | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0128 | 82. Taker Risk Constitution | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0129 | 83. Maximum Taker Slippage | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0130 | 84. Multi-Leg Risk | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0131 | 85. Continuation Gate | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0132 | 86. No Route Loyalty | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0133 | 87. Dust Risk | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0134 | 88. Global Capital Risk | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0135 | 89. Concurrent Execution Limit | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0136 | 90. Route Correlation / Dependency | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0137 | 91. Portfolio Tail Risk | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0138 | 92. Drawdown Constitution | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0139 | 93. Drawdown Bands | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0140 | 94. CAUTION | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0141 | 95. RISK_OFF | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0142 | 96. HALT Drawdown | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0143 | 97. Drawdown Cannot Trigger Martingale | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0144 | 98. Daily/Session Loss Limits | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0145 | 99. Why Multiple Windows | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0146 | 100. Loss Velocity | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0147 | 101. Consecutive Failure Monitor | `docs/14_DEPLOYMENT_AND_DOCKER.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0148 | 102. Execution Quality Kill Switch | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0149 | 103. Simulator Calibration Kill Switch | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0150 | 104. Participant Model Drift Kill Switch | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0151 | 105. Fallback Risk Principle | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0152 | 106. Fee Change Kill Switch | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0153 | 107. Metadata Change Kill Switch | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0154 | 108. Feed Sequence Integrity | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0155 | 109. No Silent Data Repair | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0156 | 110. Cross-Market Consistency | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0157 | 111. Opportunity Outlier Gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0158 | 112. “Too Good To Be True” Rule | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0159 | 113. Infrastructure Risk | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0160 | Level 0 | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0161 | Level 1 | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0162 | Level 2 | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0163 | Level 3 | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0164 | 115. API Rate Limit Risk | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0165 | 116. Rate-Limit Reservation | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0166 | 117. Cancels Have Priority Over New Orders | `docs/specs/OrderSlicingEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0167 | 118. Risk Budget Architecture | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0168 | 119. Risk Budget Consumption | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0169 | 120. Per-Market Limits | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0170 | 121. Per-Asset Limits | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0171 | 122. Per-Strategy Limits | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0172 | 123. Maker/Taker Limits Are Separate | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0173 | 124. Per-Client Risk Profile | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0174 | 125. Constitutional Floor | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0175 | 126. Safe Direction of Configuration | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0176 | 127. Config Validation | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0177 | 128. Runtime Config Changes | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0178 | 129. No Risk Change During Critical Transition | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0179 | 130. Kill Switch Taxonomy | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0180 | 131. GLOBAL_KILL | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0181 | 132. MARKET_KILL | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0182 | 133. ASSET_KILL | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0183 | 134. STRATEGY_KILL | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0184 | 135. MODEL_KILL | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0185 | 136. Dependency-Aware Risk | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0186 | 137. Fail-Closed Principle | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0187 | 138. Fail-Open Exception | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0188 | 139. Risk Decision Object | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0189 | 140. Risk Action | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0190 | 141. Reject Reasons Must Be Machine-Readable | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-RISK-0191 | 142. Risk Decision Audit | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0192 | 143. Risk Is Re-Evaluated At Multiple Times | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0193 | T0 | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0194 | T1 | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0195 | T2 | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0196 | T3 | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0197 | T4 | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0198 | T5 | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0199 | 144. Time-of-Check / Time-of-Use Protection | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0200 | 145. Risk Snapshot | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0201 | 146. Route-Level Expected Loss Budget | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0202 | 147. Portfolio Optimization Is Subordinate To Hard Gates | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-RISK-0203 | 148. Risk Cannot Be Overridden By Optimizer | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0204 | 149. Capital Scaling | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0205 | 150. Auto-Compounding | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0206 | 151. Scaling Gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0207 | 152. Capital Bands | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0208 | 153. Infrastructure Scaling | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0209 | 154. Production Deployment Risk | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0210 | 155. Startup Risk Sequence | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0211 | 156. Shutdown Risk Sequence | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0212 | 157. Crash Restart | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0213 | 158. Secrets Failure | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0214 | 159. API Wallet Safety | `docs/_analysis/FINAL_AUDIT.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0215 | 160. Client Secret Isolation | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0216 | 161. Telemetry Secret Rule | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0217 | 162. Panic Policy | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0218 | 163. Memory/State Corruption | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0219 | 164. Numerical Risk | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0220 | 165. Zero Division | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0221 | 166. Accounting Invariants | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0222 | 167. PnL Separation | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0223 | 168. Risk Metrics By Source | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0224 | 169. Global Kill Trigger Examples | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0225 | 170. Market Kill Trigger Examples | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0226 | 171. Strategy Kill Examples | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0227 | 172. Automatic Restart Is Not Automatic Re-Trading | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0228 | 173. Manual Override | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0229 | 174. Dangerous Manual Override | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0230 | CONSTITUTIONAL | `docs/specs/RiskEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0231 | TUNABLE | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0232 | 176. Parameter Governance | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0233 | 177. No Magic Numbers | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0234 | 178. Parameter Provenance | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0235 | 179. Safety Defaults | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0236 | 180. Model Promotion Risk | `docs/specs/ParticipantEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0237 | 181. Champion Failure | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0238 | 182. Research Features Cannot Leak Into Production Unvalidated | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0239 | 183. Backtest Cannot Override Live Evidence | `docs/specs/CounterfactualSimulator.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0240 | 184. Live Evidence Needs Statistical Support | `docs/specs/InfrastructureBenchmark.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0241 | 185. Incident Mode | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0242 | 186. Risk Constitution Testing | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0243 | 187. Property Test — No Overspend | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0244 | 188. Property Test — No Overfill | `docs/_analysis/TRACEABILITY_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0245 | 189. Property Test — Hard Inventory | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0246 | 190. Property Test — No New Risk During Unknown | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0247 | 191. Property Test — Stale Feed | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0248 | 192. Property Test — Risk Reduction Exception | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0249 | 193. Fault Injection — Lost HTTP Response | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0250 | 194. Fault Injection — Market Feed Loss | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0251 | 195. Fault Injection — Account Feed Loss | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0252 | 196. Fault Injection — Clock Failure | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0253 | 197. Fault Injection — Model NaN | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0254 | 198. Fault Injection — Disk Full | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0255 | 199. Fault Injection — CPU Saturation | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0256 | 200. Definition of Constitutional Compliance | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0257 | 201. Architecture du Risk Engine | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0258 | 202. Risk Gate Ordering | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0259 | 203. Fast Reject Path | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0260 | 204. Risk Engine Hot Path | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0261 | 205. Risk Snapshot Immutability | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0262 | 206. Risk Config Versioning | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0263 | 207. Risk Replay | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0264 | 208. Reject Dataset | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0265 | 209. Why Store Rejects | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0266 | 210. Risk Threshold Optimization | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0267 | 211. Risk Budget Must Match Capital | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0268 | 212. Risk Budget Must Match Capacity | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0269 | 213. Minimum Economic Significance | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0270 | 214. Risk vs Economic Gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0271 | 215. Risk Accounting | `docs/specs/AccountingEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | CHECK REGISTER | NO |
| REQ-RISK-0272 | 216. Constitution Principle — Risk Is Observable | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0273 | 217. Constitution Principle — Risk Is Deterministic Given Inputs | `docs/specs/ClockAndRng.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0274 | 218. Constitution Principle — Risk Is Reproducible | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-RISK-0275 | 219. Constitution Principle — Risk Does Not Predict Profit | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0276 | 220. Constitution Principle — Uncertainty Is Risk | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0277 | 221. Constitution Principle — Complexity Must Fail Safe | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0278 | 222. Constitution Principle — Existing Exposure Beats New Alpha | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0279 | 223. Constitution Principle — Exchange Truth Beats Model Truth | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0280 | 224. Constitution Principle — Hard Rules Beat EV | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0281 | 225. Constitution Principle — No Hidden Leverage | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0282 | 226. Constitution Principle — No Unlimited Recovery Loop | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0283 | 227. Constitution Principle — Model Confidence Cannot Be Purchased With Size | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0284 | 228. Constitution Principle — Low Liquidity Cannot Be Fixed With Faster VPS | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0285 | 229. Constitution Principle — Profitability Must Survive Real Costs | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0286 | 230. Constitution Principle — Every Risk Increase Is Explicit | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0287 | 231. Risk-Increasing Action | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0288 | 232. Risk-Neutral Action | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0289 | 233. Risk-Reducing Action | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0290 | 234. Final RiskDecision Contract | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0291 | 235. Defense in Depth | `docs/_analysis/extracted/quant.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0292 | 236. Risk Constitution in Docker Client | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0293 | 237. Unsupported Risk Configuration | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0294 | 238. Risk Profile Levels | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0295 | 239. Final Architecture | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0296 | 240. Résumé des invariants majeurs | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0297 | 241. Definition of Constitutional Success | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0298 | 242. Principe final | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0010 | 1. Objectif | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0011 | 2. Principe fondamental | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0012 | L0 — Raw | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0013 | L1 — Normalized Events | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0014 | L2 — State | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0015 | L3 — Derived Features | `docs/_analysis/extracted/participants.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0016 | L4 — Decisions / Results | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0017 | 4. Règle RAW | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0018 | 5. RawEvent | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0019 | 6. event_id | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REC-0008 | 7. recorder_seq | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0020 | 8. exchange_ts | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0004 | 9. recv_wallclock_ts | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0005 | 10. recv_monotonic_ns | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0021 | 11. Source | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0022 | 12. Source quality | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0023 | 13. Normalized MarketEvent | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0024 | 14. BookSnapshot | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0025 | 15. PriceLevel | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0026 | 16. Pourquoi ticks/lots | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0027 | 17. BookDiff | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0028 | 18. TradeEvent | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0029 | 19. Side | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0030 | 20. MarketId | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0031 | 21. AssetId | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0032 | 22. MarketDefinition | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0033 | 23. MetadataVersion | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0034 | 24. BookState | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0035 | 25. BookVersion | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0036 | 26. Book invariants | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0037 | 27. Invalid Book | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0038 | 28. BookSnapshotId | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0039 | 29. AccountEvent | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0040 | 30. OrderUpdate | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0041 | 31. FillEvent | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0042 | 32. FillId | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0043 | 33. Balance | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0044 | 34. AccountState | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0045 | 35. AccountVersion | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0046 | 36. InventoryState | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0047 | 37. AssetClassification | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0048 | 38. InventoryPosition | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0049 | 39. ReservationState | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0050 | 40. BalanceReservation | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0051 | 41. BookCapacityReservation | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0052 | 42. Pourquoi book_version | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0053 | 43. RouteDefinition | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0054 | 44. RouteType | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0055 | 45. RouteLeg | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0056 | 46. ConversionDirection | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0057 | 47. RouteDependencies | `docs/02_DOMAIN_MODEL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0058 | 48. pair_to_routes | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0059 | 49. Opportunity | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0060 | 50. Opportunity ≠ ExecutionPlan | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0061 | 51. OpportunityId | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0062 | 52. OpportunityEpisode | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0063 | 53. FeatureSnapshot | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0064 | 54. Pourquoi immutable | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0065 | 55. ModelForecast | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0066 | 56. EdgeSurvivalForecast | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0067 | 57. LiquidityForecast | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0068 | 58. MakerForecast | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0069 | 59. CrossMarketForecast | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0070 | 60. ResponseForecast | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0071 | 61. ExecutionForecast | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0072 | 62. RiskSnapshot | `docs/_analysis/extracted/data.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-DATA-0073 | 63. RiskDecision | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0074 | 64. ExecutionPlan | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0075 | 65. ExecutionPlan immutability | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0076 | 66. ExecutionMode | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0077 | 67. ExecutionLegPlan | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0078 | 68. Role | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0079 | 69. OrderPolicy | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0080 | 70. OrderIntent | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0081 | 71. OrderIntent lifecycle | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0082 | 72. SignedOrderIntent | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0083 | 73. TransportRequest | `docs/_analysis/extracted/data.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-DATA-0084 | 74. Pourquoi séparer transport | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0085 | 75. ExecutionTransport trait | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0086 | 76. NullShadowTransport | `docs/specs/ExecutionTransport.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-REPLAY-0007 | 77. ReplayTransport | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0087 | 78. Principe majeur | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0088 | 79. EngineInputEvent | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0089 | 80. InfraEvent | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0090 | 81. TimerEvent | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0091 | 82. Pourquoi timers comme événements | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0092 | 83. ControlEvent | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0093 | 84. DecisionEvent | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0094 | 85. RejectEvent | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0095 | 86. RejectReason | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0096 | 87. Pourquoi enum versionné | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0097 | 88. InfraState | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0098 | 89. InfraStateVersion | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0099 | 90. ConfigVersion | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0100 | 91. ResolvedConfig | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0101 | 92. Pas de configuration implicite | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0102 | 93. RunManifest | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0103 | 94. RunMode | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0104 | 95. RunMode cannot alter strategy logic | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0008 | 96. Replay exactness principle | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0001 | 97. Determinism identity | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0105 | 98. DecisionTrace | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DET-0002 | 99. Deterministic ordering | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0106 | 100. Pourquoi ordre explicite | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0107 | 101. EventTime vs ReceiveTime | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0108 | 102. No Look-Ahead | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0109 | EXACT RECEIVE-TIME | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-REPLAY-0009 | ACCELERATED | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0110 | COUNTERFACTUAL LATENCY | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0111 | INTERACTIVE | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0006 | 104. Replay clock | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLOCK-0007 | 105. Clock implementations | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLOCK-0008 | 106. Why Clock abstraction | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0009 | 107. RNG abstraction | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0010 | 108. Replay RNG | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLOCK-0011 | 109. Live RNG | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0112 | 110. De préférence : peu de stochasticité live | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0113 | 111. Model interface | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0114 | 112. Model inputs immutable | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0115 | 113. ModelVersion | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0116 | 114. FeatureSchemaVersion | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0117 | 115. FormulaSchemaVersion | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0118 | 116. DatasetId | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0119 | 117. GoldenDataset | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0120 | 118. Data partitions | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0121 | 119. Raw manifest | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0122 | 120. Checksum | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0123 | 121. Immutable RAW | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0124 | 122. Normalization schema | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0009 | 123. Recorder thread | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0010 | 124. Recorder priority | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0125 | 125. Backpressure policy | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0126 | 126. Event completeness metrics | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0127 | 127. Dataset quality contract | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0128 | 128. Invalid dataset regions | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0129 | 129. Account data priority | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0130 | 130. ExecutionJournal | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0131 | 131. Journal events | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0132 | 132. Journal replay | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0133 | 133. EventReducer | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0134 | 134. Reducer purity | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0135 | 135. Effects | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0136 | 136. Effect executor | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0137 | 137. Example | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0138 | 138. Command/Event separation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0139 | 139. Why | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0003 | 140. State hashes | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DET-0004 | 141. Determinism test | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0140 | 142. Divergence detector | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0141 | 143. Python/Rust contracts | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0142 | 144. Parquet schemas | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0143 | 145. Units mandatory | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0144 | 146. Naming convention | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0145 | 147. Never ambiguous money | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0146 | 148. Numeraire | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0147 | 149. EconomicValue | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLOCK-0012 | 150. Conversion timestamp | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0148 | 151. PnL schema | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0149 | 152. No double accounting | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0150 | 153. Recommended convention | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0151 | 154. ExternalFlows | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0152 | 155. CapitalState | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0153 | 156. HOT/WARM/COLD schema | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0154 | 157. Tier | `docs/specs/FeeEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0155 | 158. Tier transitions | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0156 | 159. MarketAtlasRecord | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0157 | 160. Research vs live schemas | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0158 | 161. Schema evolution | `docs/README.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0159 | 162. Unknown fields | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0160 | 163. Removed fields | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0161 | 164. Schema registry | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0162 | 165. Internal Rust types are source of truth | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0163 | 166. Serialization | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0164 | 167. No giant JSON RAW | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REPLAY-0010 | 168. Replay fidelity field | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0165 | 169. Why fidelity explicit | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0166 | 170. SimulationMode | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0011 | 171. ExogenousReplay | `docs/_analysis/extracted/simulator.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0167 | 172. InteractiveCounterfactual | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0168 | 173. BranchId | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0169 | 174. MonteCarloPathId | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0170 | 175. Rejoin event | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0171 | 176. Confidence schema | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0172 | 177. Why decomposed confidence | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0173 | 178. LatencyTrace | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0174 | 179. InfraInstanceId | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0175 | 180. BenchmarkRun | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0176 | 181. FirstArrivalRecord | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0177 | 182. InfraLostPnLRecord | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0178 | 183. Attribution must not double count | `docs/specs/InfrastructureROI.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0179 | 184. ModelPredictionRecord | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0180 | 185. CalibrationDataset | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0181 | 186. Champion / Challenger | `docs/_analysis/TRACEABILITY_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0182 | 187. Challenger never alters decision | `docs/specs/ParticipantEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0183 | 188. PromotionEvent | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0184 | 189. DeploymentVersion | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0185 | 190. Why digest | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0186 | 191. ClientInstallationId | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0187 | 192. Local-only by default | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0188 | 193. Logs vs events | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0189 | 194. StructuredEvent envelope | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0190 | 195. Correlation IDs | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0191 | 196. Complete trace | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0192 | 197. This trace is mandatory | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0005 | 198. Deterministic numeric rules | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0193 | 199. No duplicated formula implementations | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0194 | 200. Same FeeEngine | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0195 | 201. Same PrecisionEngine | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0196 | 202. Same RouteEngine | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0197 | 203. Same RiskEngine | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0198 | 204. Same Execution State Machine | `docs/REVIEW_REQUIRED.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0199 | 205. Same RecoveryEngine | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0200 | 206. Same InventoryEngine | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0201 | 207. Same ReservationEngine | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-REPLAY-0012 | 208. Replay account state | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0202 | 209. Shadow account state | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0203 | 210. Important distinction Shadow | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0204 | 211. Paper mode | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0205 | 212. Micro-live | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0206 | 213. Live | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0207 | 214. Environment flag cannot change math | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0208 | 215. Data contract tests | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0013 | 216. Golden replay test | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0006 | 217. Replay determinism test | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DET-0007 | 218. Multi-thread determinism | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0209 | 219. Single-writer principle | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0210 | 220. Why | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0211 | 221. Parallel readers | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0212 | 222. Snapshot publication | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0213 | 223. Atomic snapshot version | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0214 | 224. TOCTOU protection | `docs/specs/NetConvert.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0215 | 225. Critical changes | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0216 | 226. Not every market tick forces restart | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0217 | 227. Plan validity envelope | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0218 | 228. If envelope violated | `docs/specs/CapabilityRegistry.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0219 | 229. Storage separation | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0220 | 230. Persistent state | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0221 | 231. Ephemeral state | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0222 | 232. State checkpoint | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0223 | 233. Checkpoint is not source of truth | `docs/specs/ReconciliationEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0224 | 234. Checkpoint version | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0225 | 235. Migration | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0226 | 236. No silent state discard | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REC-0011 | 237. Event retention classes | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0227 | 238. Permanent | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0228 | 239. Short | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0229 | 240. Trade windows | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0230 | 241. Why | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0231 | 242. Incident windows | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0232 | 243. Schema validation on ingestion | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0233 | 244. Unknown event type | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0234 | 245. Forward compatibility | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0235 | 246. Latency measurement contract | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0236 | 247. Cross-machine latency | `docs/02_DOMAIN_MODEL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLOCK-0013 | 248. ClockQualityRecord | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0237 | 249. Timing validity | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0238 | 250. Benchmark data contract | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0239 | 251. Formula input traceability | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0240 | 252. Why | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0241 | 253. Data lineage | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0242 | 254. Every link traceable | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0243 | 255. Dataset contamination prevention | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0244 | 256. Model artifact stores training range | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0245 | 257. Point-in-time correctness | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0014 | Historical truth replay | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0246 | Research counterfactual | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0247 | 259. No mixing without label | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0248 | 260. Config provenance | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0249 | 261. Client overrides | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0250 | 262. Invalid override | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | CHECK REGISTER | NO |
| REQ-DATA-0251 | 263. Test fixtures | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0252 | 264. Builders | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0253 | 265. Property-based tests | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0254 | 266. Fuzzing | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0255 | 267. Serialization fuzzing | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0256 | 268. API adapters cannot mutate core state directly | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0257 | 269. Core state mutations happen through reducers | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0258 | 270. Strategy cannot mutate AccountState | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0259 | 271. Risk cannot mutate AccountState | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0260 | 272. ExecutionCoordinator can request effects | `docs/specs/ExecutionCoordinator.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0261 | 273. Why event-driven | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0262 | 274. State transition schema | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0263 | 275. Reason mandatory | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0264 | 276. IncidentId | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0265 | 277. IncidentRecord | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0266 | 278. Severity | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0267 | 279. Incident does not equal log error | `docs/18_OPERATIONS_AND_MONITORING.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DET-0008 | 280. Deterministic risk snapshot creation | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0009 | 281. Canonical ordering | `docs/specs/ReplayEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DET-0010 | 282. Hash canonicalization | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0268 | 283. Float canonicalization | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0011 | 284. Model deterministic inference | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0012 | 285. Hardware nondeterminism | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0269 | 286. Numerical epsilon contract | `docs/_analysis/extracted/quant.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0270 | 287. Exchange boundary exactness | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0271 | 288. PnL tolerance | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0015 | 289. Replay performance | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0016 | 290. Event batching Replay | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0272 | 291. Live event concurrency | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0273 | 292. Event bus | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0274 | 293. Priority | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0275 | 294. Separate buses possible | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0276 | 295. Recommendation | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0277 | 296. Parallel workers | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0278 | 297. Stale worker result | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0279 | 298. No stale prediction commit | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0280 | 299. Prediction TTL | `docs/18_OPERATIONS_AND_MONITORING.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0281 | 300. Dataset version in every experiment | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0282 | 301. ExperimentResult | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0283 | 302. No notebook-only result | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DET-0013 | 303. Research reproducibility | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0284 | 304. Python environment | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0014 | 305. Production build reproducibility | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0285 | 306. Schema compatibility gate on startup | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0286 | 307. Incompatible model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0287 | 308. Incompatible state | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0288 | 309. Incompatible config | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0289 | 310. No silent migration live | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0290 | 311. Data contracts form part of API | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0291 | 312. Module boundaries | `docs/specs/MODULE_INDEX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0292 | 313. RouteEngine | `docs/specs/OpportunityEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0293 | 314. ParticipantEngine | `docs/specs/CrossMarketResponseEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0294 | 315. Simulator | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0295 | 316. RiskEngine | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0296 | 317. ExecutionCoordinator | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0297 | 318. InventoryEngine | `docs/specs/CapitalReachabilityEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0298 | 319. No cyclic hidden dependencies | `docs/specs/BridgeEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0299 | 320. Dependency direction | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0300 | 321. Domain types package | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0301 | 322. Suggested structure | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0302 | 323. Domain layer has no external APIs | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0303 | 324. Adapter layer | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0304 | 325. Exchange schema changes isolated | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0305 | 326. Data contract acceptance tests | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0306 | 327. Parser regression corpus | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0307 | 328. Unknown fields tolerant | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0308 | 329. Missing required field strict | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-0015 | 330. Final Determinism Contract | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0309 | 331. Final Data Contract Principle | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0310 | 332. Final State Principle | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0017 | 333. Final Replay Principle | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0311 | 334. Final Shadow Principle | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0312 | 335. Final Micro-Live Principle | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0313 | 336. Final Production Principle | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DATA-0314 | 337. Definition of Done — Data Contracts | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0315 | 338. Principe final | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0002 | 1. Objectif | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0003 | 2. Principe fondamental | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0001 | 3. Architecture cible client | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0004 | 4. Une seule image principale | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0005 | 5. Pourquoi un container principal | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0006 | 6. Architecture logique ≠ architecture physique | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0007 | 7. Processus principal | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0008 | 8. Pas de processus critique externe | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0009 | 9. OCI image | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0010 | 10. Architecture CPU de référence | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0011 | 11. Pas de multi-architecture non testée | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0012 | 12. Dockerfile multi-stage | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0013 | 13. Runtime image minimale | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0014 | 14. Pas d’optimisation build aveugle | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0015 | 15. CPU feature baseline | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0016 | 16. Release build reproducible | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0017 | 17. Image identification | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0018 | 18. Le digest est l’identité réelle | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0019 | 19. Pas de latest en production | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0020 | 20. Pourquoi | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0021 | 21. Registry | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0022 | 22. Accès registry | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0023 | 23. Image signing | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0003 | 24. Supply-chain security | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0004 | 25. SBOM | `docs/14_DEPLOYMENT_AND_DOCKER.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0024 | 26. Vulnerability scanning | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0025 | 27. Container user | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0026 | 28. Root filesystem | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0027 | 29. Writable paths | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0028 | 30. Linux capabilities | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0005 | 31. Pas de --privileged | `docs/14_DEPLOYMENT_AND_DOCKER.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0029 | 32. Pas de Docker socket | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0030 | 33. No host filesystem mount | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0031 | 34. PID namespace | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0032 | 35. Clock | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0005 | 36. Clock health | `docs/specs/ClockAndRng.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0033 | 37. Network mode | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0034 | 38. Pourquoi host peut être intéressant | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0035 | 39. Décision par benchmark | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0036 | 40. Docker overhead gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0037 | 41. Resource limits | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0038 | 42. Pourquoi | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0039 | 43. Recommended CPU pinning | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0040 | 44. Hot-path priority | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0041 | 45. Swap | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0042 | 46. OOM handling | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0043 | 47. Configuration hors image | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0044 | 48. Configuration layout | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0045 | 49. bot.toml | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0046 | 50. risk.toml | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0047 | 51. markets.toml | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0048 | 52. ResolvedConfig | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0049 | 53. Invalid config | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0050 | 54. Config schema version | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0051 | 55. Config migrations | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0006 | 56. Secrets séparés | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0007 | 57. Secret principal | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0008 | 58. Secret mount | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0052 | 59. Pourquoi fichier plutôt qu’environnement | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SEC-0009 | 60. Secret permissions host | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0010 | 61. Secret lifetime | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0053 | 62. Memory handling | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SEC-0011 | 63. Secret redaction | `docs/15_SECURITY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0054 | 64. Panic protection | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0002 | 65. Support bundle | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0003 | 66. Support bundle contents | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0055 | 67. Private by default | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0056 | 68. Persistent volumes | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0057 | 69. /data/state | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0058 | 70. /data/journal | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0059 | 71. /data/recorder | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0060 | 72. /data/models | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0061 | 73. Modèles : image ou volume ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0062 | Stable models | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0063 | Frequently updated calibrated models | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0064 | 74. Règle modèle | `docs/README.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0065 | 75. /logs | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0066 | 76. Log rotation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0067 | 77. Log levels | `docs/specs/NetConvert.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0068 | 78. Pas de TRACE permanent | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0069 | 79. Structured logs | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0070 | 80. Disk budget | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0071 | 81. Disk thresholds | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0072 | 82. LOW disk | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0073 | 83. CRITICAL disk | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0074 | 84. Jamais supprimer les données critiques au hasard | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0006 | 85. Backup | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0075 | 86. Pas besoin de sauvegarder l’image | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0012 | 87. Backup secret | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0076 | 88. Recovery kit | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0007 | 89. Backup consistency | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0008 | 90. Restart contract | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0077 | 91. Docker restart policy | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0078 | 92. Healthcheck Docker | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0009 | 93. Liveness | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0010 | 94. Readiness | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0011 | 95. Trading health | `docs/_analysis/extracted/deployment.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-DEPLOY-0079 | 96. Docker healthcheck ne doit pas provoquer une boucle dangereuse | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0012 | 97. Donc liveness ≠ readiness | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0080 | 98. Metrics endpoint | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0081 | 99. Metrics listener | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0082 | 100. Admin API | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0083 | 101. Pas de panneau admin public | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0084 | 102. Remote dashboard futur | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0013 | 103. Firewall VPS | `docs/_analysis/extracted/deployment.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0085 | 104. SSH | `docs/_analysis/CONTRADICTIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0004 | 105. Client responsibility | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0086 | 106. Installer | `docs/17_IMPLEMENTATION_ROADMAP.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0087 | 107. Ce que fait l’installer | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0088 | 108. Ce que l’installer ne fait jamais | `docs/specs/Deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0089 | 109. First boot wizard | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0090 | 110. Configuration steps | `docs/specs/ExecutionCoordinator.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0005 | 111. Pas de Live immédiat pour nouveau client | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0006 | 112. Client onboarding gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0091 | 113. Infra diagnostic intégré | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0092 | 114. Tests diagnostic | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0093 | 115. Output | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0094 | 116. Unsupported infrastructure | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0095 | 117. Provider independence | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0096 | 118. Provider profile | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0097 | 119. VPS standard minimum | `docs/specs/PrecisionEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0098 | 120. Recommended profile | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0099 | 121. Performance profile | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0100 | 122. Pas de VPS premium obligatoire | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0007 | 123. Infra ROI client | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0101 | 124. Jamais upgrade automatique du VPS | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0008 | 125. Distribution aux 30–50 clients | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0001 | 126. Licence | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0102 | 127. Interdit | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0103 | 128. Pourquoi | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0002 | 129. Licence startup | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0003 | 130. Signed entitlement | `docs/specs/Deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0104 | 131. Le bot vérifie localement | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0105 | 132. Grace period | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0106 | 133. Expiration et trading actif | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0107 | 134. Principe commercial important | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0108 | 135. Pas de remote kill dangereux | `docs/15_SECURITY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0109 | 136. Révocation | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0110 | 137. Installation binding | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0111 | 138. Ne pas binder trop fortement au hardware | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0004 | 139. Licence ≠ clé client | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0112 | 140. Telemetry | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0113 | 141. Données potentiellement utiles | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0114 | 142. Pas besoin d’envoyer | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0115 | 143. Update channels | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0116 | 144. Stable | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0117 | 145. Candidate | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0118 | 146. Development | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0119 | 147. Release process | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0009 | 148. Pas de release directe main → clients | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0120 | 149. Canary deployment | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0010 | 150. Client updates | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0121 | 151. Safe Update State | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0122 | 152. Update sequence | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0123 | 153. Blue/green ? | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0124 | 154. No dual-active update | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0125 | 155. Pre-start validation container | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0126 | 156. Rollback | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0127 | 157. Rollback sequence | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0128 | 158. Pas de rollback de state aveugle | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0129 | 159. Backward-compatible storage | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0130 | 160. Destructive migration | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0131 | 161. Database | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0132 | 162. State persistence | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0133 | 163. Embedded database candidate | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0134 | 164. Hot path rule | `docs/specs/ExecutionCoordinator.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0135 | 165. Config hot reload | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0136 | 166. Risk config reload | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0137 | 167. Software update ≠ config update | `docs/specs/botctl.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0138 | 168. Model update | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0139 | 169. Model rollout | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0140 | 170. Pas de remplacer Champion à chaud sans validation | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0013 | 171. Crash handling | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0014 | 172. Crash loop | `docs/specs/BookEngine.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0141 | 173. Core dump | `docs/_analysis/CONTRADICTIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0142 | 174. Panic logs | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0143 | 175. Signal handling | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0144 | 176. Graceful shutdown | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0145 | 177. Docker stop timeout | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0146 | 178. SIGKILL | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0147 | 179. Host reboot | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0148 | 180. VPS replacement | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0149 | 181. Migration VPS | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0150 | 182. No overlap | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0151 | 183. Instance lock | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0152 | 184. Exchange-side protection | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0153 | 185. Nonce isolation | `docs/_analysis/FINAL_AUDIT.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0011 | 186. Client clones | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0154 | 187. Network egress | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0155 | 188. Trading independence | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0156 | 189. Update independence | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0157 | 190. Local dashboard éventuel | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0012 | 191. CLI botctl | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0158 | 192. Pourquoi CLI | `docs/specs/Deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0013 | 193. botctl status | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0014 | 194. botctl health | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0015 | 195. botctl reconcile | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0016 | 196. botctl update | `docs/specs/botctl.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0017 | 197. botctl rollback | `docs/01_PRODUCT_AND_SCOPE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0018 | 198. botctl emergency-stop | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-CLIENT-0019 | 199. Client modes | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0159 | 200. Mode stored in config | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0160 | 201. Mode transition | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0161 | 202. Production profiles | `docs/decisions/SUPERSEDED_DECISIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0162 | 203. Pas de profil “YOLO” | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0020 | 204. Customer data ownership | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0163 | 205. No mandatory central ingestion | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0164 | 206. Optional diagnostics telemetry | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0165 | 207. Remote support | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0166 | 208. No embedded backdoor | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0014 | 209. Security updates | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0167 | 210. Emergency release | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0168 | 211. Rollout metrics | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0169 | 212. Automatic rollback central ? | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0021 | 213. Version pinning client | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0170 | 214. Minimum supported version | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0171 | 215. Breaking exchange change | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0172 | 216. Exchange compatibility | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0173 | 217. Unknown exchange version/rule | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0015 | 218. Secret rotation | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0016 | 219. Pas de signer swap entre deux jambes | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0174 | 220. Credential revocation | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0017 | 221. Host security baseline | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0175 | 222. Automatic host updates | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0176 | 223. Reboot maintenance window | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0177 | 224. VPS provider maintenance | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OPS-0015 | 225. Backup VPS | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0178 | 226. Cold recovery > hot standby initialement | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0179 | 227. Hot standby futur | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0180 | 228. Split-brain prevention | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0016 | 229. Failover architecture | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0022 | 230. Package vendu au client | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0181 | 231. Pas de code source obligatoire | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0182 | 232. Protection intellectuelle | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0183 | 233. Obfuscation | `docs/decisions/ADR-016-no-saas-hot-path.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0184 | 234. Critical IP | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0185 | 235. Mais pas de dépendance serveur pour cacher l’algo | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0005 | 236. Licence client max | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0023 | 237. Customer registry | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0018 | 238. No customer secrets | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0186 | 239. Documentation package | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0187 | 240. Release notes | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0188 | 241. Risk change visibility | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0189 | 242. Migration notes | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0190 | 243. Supported upgrade path | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0191 | 244. Version compatibility matrix | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0192 | 245. Deployment manifest | `docs/specs/Deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OPS-0017 | 246. Incident correlation | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0193 | 247. Reproduction | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0194 | 248. No silent auto-update | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0195 | 249. No cloud dependency in execution | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SEC-0019 | 250. Deployment security hierarchy | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0196 | 251. Important consequence | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0197 | 252. Installation Definition of Done | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0198 | 253. Micro-live activation DoD | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0199 | 254. Live activation DoD | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0200 | 255. Upgrade DoD | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0201 | 256. Rollback DoD | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0020 | 257. Security DoD | `docs/15_SECURITY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0202 | 258. Production simplicity principle | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0203 | 259. Pas de Kubernetes | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0204 | 260. Pas de central orchestration obligatoire | `docs/_analysis/extracted/risk.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0205 | 261. Future fleet management | `docs/14_DEPLOYMENT_AND_DOCKER.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0206 | 262. Fleet metadata | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0024 | 263. Final client deployment | `docs/REVIEW_REQUIRED.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0207 | 264. Update architecture | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0006 | 265. Licence architecture | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0208 | 266. Failure architecture | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0209 | 267. Principe final de distribution | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0210 | 268. Principe final de packaging | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0211 | 269. Principe final de mise à jour | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIC-0007 | 270. Principe final de licence | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0212 | 271. Principe final de sécurité | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0213 | 272. Principe final d’exploitation | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0214 | 273. Definition of Done du Dossier 5 | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0215 | 274. Conclusion | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0015 | DOSSIER 6/6 — DEFINITION OF DONE & VALIDATION MATRIX | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0016 | 1. Objectif | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0017 | 2. Les 6 niveaux de maturité | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0018 | 3. M0 — SPECIFIED | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0019 | 4. M1 — UNIT VALIDATED | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0020 | 5. M2 — REPLAY VALIDATED | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0021 | 6. M3 — SHADOW VALIDATED | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0022 | 7. M4 — MICRO-LIVE VALIDATED | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0023 | 8. M5 — LIVE VALIDATED | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0024 | 9. Principe de progression | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0025 | 10. Exceptions | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0026 | 11. Validation par dépendance | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0027 | 12. Dependency Gate | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0028 | 13. Matrice globale des modules | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0029 | 14. FEED ADAPTER — Definition of Done | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0030 | 15. Feed schema tests | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0031 | 16. Feed corruption | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0032 | 17. Feed reconnect | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0033 | 18. Feed freshness | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0034 | 19. Feed DoD M2 | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0035 | 20. Feed DoD M3 | `docs/_analysis/OPEN_ITEMS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0036 | 21. Feed performance | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0037 | 22. NORMALIZER — DoD | `docs/specs/Normalizer.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0038 | 23. Roundtrip / normalization tests | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0039 | 24. BOOK ENGINE — Correctness | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0040 | 25. Book reconstruction test | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0041 | 26. Book gap test | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0042 | 27. No silent repair | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0043 | 28. Book performance | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0044 | 29. Book memory | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0045 | 30. METADATA ENGINE — DoD | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0046 | 31. Metadata change | `docs/decisions/ADR-004-precomputed-routes.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0047 | 32. Fee Engine — DoD | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0048 | 33. Fee historical replay | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0049 | 34. Fee unknown | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0050 | 35. PRICE/SIZE QUANTIZER — DoD | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0051 | 36. Golden exchange boundary tests | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0052 | 37. NETCONVERT — DoD | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0053 | 38. Golden NetConvert | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0054 | 39. NetConvert parity | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0055 | 40. ROUTE ENGINE — DoD | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0056 | 41. Route graph validation | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0057 | 42. Cycle validation | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0058 | 43. OWA validation | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0059 | 44. pair_to_routes validation | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0060 | 45. Route performance | `docs/specs/RouteEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0061 | 46. QUANT MICROSTRUCTURE — DoD | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0062 | 47. Invalid inputs | `docs/specs/PrecisionEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0063 | 48. Rolling calculations | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0064 | 49. Incremental error test | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0065 | 50. MARKET ATLAS — DoD | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0066 | 51. Atlas missing data | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0067 | 52. HOT/WARM/COLD — DoD | `docs/_analysis/CONTRADICTIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0068 | 53. HOT/WARM/COLD resource test | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0069 | 54. PARTICIPANT MODEL — Baseline DoD | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0070 | 55. Survival calibration | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0071 | 56. Survival metrics | `docs/specs/EdgeSurvivalEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0072 | 57. Economic validation | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0073 | 58. Participant model OOD | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0074 | 59. Participant fallback | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0075 | 60. CROSS-MARKET MODEL — DoD | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0076 | 61. No pure correlation adoption | `docs/_analysis/extracted/participants.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0077 | 62. Cross-market ablation | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0078 | 63. If no lift | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0079 | 64. MAKER FILL MODEL — DoD | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0080 | 65. Fill calibration | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0081 | 66. Adverse selection model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0082 | 67. Maker strategy activation | `docs/_analysis/TRACEABILITY_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0083 | 68. SIMULATOR — DoD F0 | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0084 | 69. Simulator F1 | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0085 | 70. F1 validation | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0086 | 71. Simulator F2 | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0087 | 72. Simulator F3 | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0088 | 73. F4 | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0089 | 74. Simulator requirement | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0090 | 75. Simulator outputs validation | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0091 | 76. Coverage validation | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0092 | 77. Simulator OOD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0093 | 78. POSITION SIZING — DoD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0094 | 79. Sizing monotonic assumptions | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0095 | 80. Sizing grid validation | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0096 | 81. ValidatedCapacity DoD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0097 | 82. Sizing safety | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0098 | 83. ORDER SLICING — DoD | `docs/decisions/SUPERSEDED_DECISIONS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0099 | 84. Fragmentation validation | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0100 | 85. Temporal slicing | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0101 | 86. No gain | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0102 | 87. INVENTORY ENGINE — DoD | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0103 | 88. Inventory reconciliation | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0104 | 89. Inventory band tests | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0105 | 90. Hard gate property | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0106 | 91. NetFlow | `docs/specs/MarketAtlas.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0107 | 92. TERMINAL VIABILITY — DoD | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0108 | 93. BRIDGE ENGINE — DoD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0109 | 94. Bridge path validation | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0110 | 95. Bridge accounting | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0111 | 96. Hysteresis test | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0112 | 97. PORTFOLIO OPTIMIZER — DoD | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0113 | 98. Shared-book test | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0114 | 99. Shared-balance test | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0115 | 100. Optimizer correctness | `docs/specs/ReconciliationEngine.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0116 | 101. Optimizer performance | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0117 | 102. RISK ENGINE — DoD | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0118 | 103. No stale trade test | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0119 | 104. Unknown state test | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0120 | 105. Hard inventory test | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0121 | 106. CVaR gate test | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0122 | 107. OOD gate test | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0123 | 108. Infra unsafe test | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0124 | 109. Risk determinism | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0125 | 110. Risk performance | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0126 | 111. EXECUTION STATE MACHINE — DoD | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0127 | 112. No blind retry property | `docs/_analysis/TRACEABILITY_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0128 | 113. Actual fill property | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0129 | 114. Execution event ordering | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0130 | 115. Execution determinism | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0131 | 116. Execution throughput | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0132 | 117. RECOVERY ENGINE — DoD | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0133 | 118. Recovery objective | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0134 | 119. Recovery limit | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0135 | 120. Recovery loss accounting | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0136 | 121. RECONCILIATION ENGINE — DoD | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0137 | 122. Reconciliation success | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0138 | 123. Reconciliation failure | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0139 | 124. RECORDER — DoD | `docs/01_PRODUCT_AND_SCOPE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0140 | 125. Recorder nonblocking | `docs/specs/InfrastructureMonitor.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0141 | 126. Recorder priority | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0142 | 127. Checksum | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0143 | 128. Replay roundtrip | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0144 | 129. REPLAY ENGINE — DoD | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0145 | 130. Hash test | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0146 | 131. No lookahead | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0147 | 132. Receive-time replay | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0148 | 133. Counterfactual replay | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0149 | 134. SHADOW MODE — DoD | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0150 | 135. Shadow stability | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0151 | 136. Shadow decisions | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0152 | 137. Shadow false-positive analysis | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0153 | 138. MICRO-LIVE — DoD | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0154 | 139. Micro-live initial size | `docs/decisions/SUPERSEDED_DECISIONS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0155 | 140. Micro-live frequency | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0156 | 141. Micro-live metrics | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0157 | 142. Minimum observations | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0158 | 143. Statistical stopping rule | `docs/decisions/ADR_INDEX.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0159 | 144. Micro-live acceptance | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0160 | 145. LIVE SCALING — principe | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0161 | 146. Capital ladder | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0162 | 147. Scaling gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0163 | 148. Maximum increase | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0164 | 149. No automatic compounding | `docs/specs/ReconciliationEngine.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0165 | 150. INFRASTRUCTURE — DoD | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0166 | 151. Benchmark metrics | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0167 | 152. Screening | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0168 | 153. Finalists | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0169 | 154. Provider selection | `docs/specs/InfrastructureBenchmark.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0170 | 155. Infra economic validation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0171 | 156. Infra downgrade validation | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0172 | 157. VPS failure test | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0173 | 158. DOCKER — DoD | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0174 | 159. Security tests | `docs/15_SECURITY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0175 | 160. Docker restart | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0176 | 161. Update test | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0177 | 162. Rollback test | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0178 | 163. Licence failure test | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0179 | 164. ACCOUNTING — DoD | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0180 | 165. Route PnL | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0181 | 166. No double counting | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0182 | 167. External flow | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0183 | 168. Portfolio equity | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0184 | 169. PnL reconciliation | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0185 | 170. MONITORING — DoD | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0186 | 171. Minimum metrics | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0187 | 172. Alerts | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0188 | 173. Alert quality | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0189 | 174. Incident recording | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0190 | 175. PERFORMANCE BUDGET — principe | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0191 | 176. Budget global interne | `docs/_analysis/CONTRADICTIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0192 | 177. Important | `docs/specs/InventoryEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0193 | 178. Performance regression test | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0194 | 179. Regression threshold | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0195 | 180. Economic performance regression | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0196 | 181. New feature gate | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0197 | 182. Feature ablation | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0198 | 183. If feature doesn't help | `docs/specs/OFIEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0199 | 184. Quant Model ROI | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0200 | 185. Promotion gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0201 | 186. TEST CATEGORIES | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0202 | 187. UNIT TEST | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0203 | 188. GOLDEN TEST | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0204 | 189. PROPERTY TEST | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0205 | 190. INTEGRATION TEST | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0206 | 191. REPLAY TEST | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0207 | 192. FAULT INJECTION | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0208 | 193. LOAD TEST | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0209 | 194. PERFORMANCE TEST | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0210 | 195. SHADOW TEST | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0211 | 196. MICRO-LIVE TEST | `docs/_analysis/OPEN_ITEMS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0212 | 197. CHAOS TESTS | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0213 | 198. Golden Dataset permanent | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0214 | 199. Golden incidents | `docs/decisions/SUPERSEDED_DECISIONS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0215 | 200. Dataset diversity | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0216 | 201. Out-of-sample | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0217 | 202. Walk-forward | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0218 | 203. No random train/test leakage | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0219 | 204. MARKET REGIME VALIDATION | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0220 | 205. Regime unsupported | `docs/specs/EdgeSurvivalEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0221 | 206. STRATEGY VALIDATION — OWA TT | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0222 | 207. OWA TT key metrics | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0223 | 208. OWA MT validation | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0224 | 209. TRIANGLE TTT | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0225 | 210. Triangle critical metric | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0226 | 211. Triangle MTT | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0227 | 212. BRIDGE strategy | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0228 | 213. RECOVERY strategy | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0229 | 214. VALIDATION PAR TAILLE | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0230 | 215. Une validation à 50 € n’autorise pas 5000 € | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0231 | 216. Size support | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0232 | 217. MARKET SUPPORT | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0233 | 218. Route support | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0234 | 219. CALIBRATION REPORT | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0235 | 220. VALIDATION REPORT | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0236 | 221. RELEASE GATE | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0237 | 222. If trading logic changed | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0238 | 223. If only documentation changed | `docs/README.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0239 | 224. If dependency security patch | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0240 | 225. BUILD GATE | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0241 | 226. Static analysis | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0242 | 227. Unsafe Rust | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0243 | 228. No unsafe for theoretical speed | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0244 | 229. MEMORY SAFETY / LOAD | `docs/specs/OFIEngine.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0245 | 230. Leak test | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0246 | 231. File descriptor leak | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0247 | 232. CPU runaway | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0248 | 233. BACKPRESSURE | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0249 | 234. Core event lag | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0250 | 235. Lag threshold | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0251 | 236. FAILURE MODE VALIDATION | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0252 | 237. Feed | `docs/specs/FeedAdapter.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0253 | 238. Account feed | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0254 | 239. Exchange submit | `docs/specs/ExecutionTransport.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0255 | 240. Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0256 | 241. Disk | `docs/_analysis/FINAL_AUDIT.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0257 | 242. Clock | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0258 | 243. Config | `docs/specs/ReplayEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0259 | 244. Docker | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0260 | 245. SECURITY VALIDATION | `docs/15_SECURITY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0261 | 246. Secret scanning source repo | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0262 | 247. Runtime secret test | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0263 | 248. Logs secret test | `docs/15_SECURITY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0264 | 249. Admin API exposure | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0265 | 250. REGRESSION MATRIX | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0266 | 251. A change can improve one metric and fail overall | `docs/specs/CapabilityRegistry.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0267 | 252. Multi-objective acceptance | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0268 | 253. COMPLEXITY BUDGET | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0269 | 254. Complexity penalty | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0270 | 255. Technical debt gate | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0271 | 256. Documentation DoD | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0272 | 257. Code is not documentation | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0273 | 258. IMPLEMENTATION ORDER VALIDATION | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0274 | 259. Pourquoi Recorder très tôt | `docs/_analysis/FINAL_AUDIT.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0275 | 260. Pourquoi Replay avant stratégie sophistiquée | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0276 | 261. Pourquoi TT avant MT | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0277 | 262. Pourquoi OWA/triangle simples avant Participant Models | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0278 | 263. NO “BIG BANG” | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0279 | 264. Vertical slices | `docs/17_IMPLEMENTATION_ROADMAP.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-VALID-0280 | 265. Première milestone | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0281 | 266. Deuxième milestone | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0282 | 267. Troisième milestone | `docs/specs/MarketAtlas.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0283 | 268. Quatrième milestone | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0284 | 269. Cinquième milestone | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0285 | 270. Sixième milestone | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0286 | 271. Puis intelligence avancée | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0287 | 272. LIVE CAPITAL LADDER | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0288 | 273. Chaque palier | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0289 | 274. DOWN-SCALING | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0290 | 275. Capacity is dynamic | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0291 | 276. MARKET REGIME DOWNGRADE | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0292 | 277. Model drift can reduce capital automatically | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0293 | 278. Promotion vs demotion | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0294 | 279. Strategy status | `docs/README.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0295 | 280. Market status interne | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0296 | 281. Model status | `docs/specs/ParticipantEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0297 | 282. Infrastructure status | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-VALID-0298 | 283. CLIENT RELEASE VALIDATION | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0299 | 284. Feature flags | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0300 | 285. Default production config | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0301 | 286. Default = conservative | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0302 | 287. CLIENT VPS VALIDATION | `docs/_analysis/TRACEABILITY_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0303 | 288. Minimum profile not met | `docs/specs/CapabilityRegistry.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0304 | 289. Different VPS → revalidation | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0305 | 290. Different region | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0306 | 291. INFRA UPGRADE VALIDATION | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0307 | 292. Compare same events | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0308 | 293. Upgrade decision | `docs/specs/InfrastructureROI.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0309 | 294. SYSTEM-WIDE VALIDATION | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0310 | 295. End-to-end test | `docs/15_SECURITY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0311 | 296. End-to-end fault test | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0312 | 297. End-to-end crash test | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0313 | 298. End-to-end feed failure | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0314 | 299. End-to-end disk failure | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0315 | 300. End-to-end config update | `docs/18_OPERATIONS_AND_MONITORING.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0316 | 301. ACCEPTANCE MATRIX — CORE | `docs/16_VALIDATION_MATRIX.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0317 | 302. RELEASE BLOCKERS | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0318 | 303. MICRO-LIVE BLOCKERS | `docs/_analysis/FINAL_AUDIT.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0319 | 304. SCALING BLOCKERS | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0320 | 305. LIVE AUTO-DOWNGRADE TRIGGERS | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0321 | 306. Validation is continuous | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0322 | 307. Production feedback loop | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0323 | 308. No direct self-learning in production | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0324 | 309. Monthly / periodic validation | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0325 | 310. But no arbitrary calendar dependence | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0326 | 311. Validation Dashboard | `docs/16_VALIDATION_MATRIX.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0327 | 312. ValidatedCapability | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0328 | 313. This is important commercially | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0329 | 314. Feature capability manifest | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0330 | 315. Example | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0331 | 316. Code support ≠ production support | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0332 | 317. Research archive | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0333 | 318. Negative results matter | `docs/_analysis/extracted/data.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0334 | 319. Architecture Decision Records | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0335 | 320. Example ADRs | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0336 | 321. Why ADR | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0337 | 322. Spec hierarchy | `docs/README.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0338 | 323. Priority if conflict | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0339 | 324. Formula conflict | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0340 | 325. Exchange rule conflict | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0341 | 326. Spec update process | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0342 | 327. No silent architecture drift | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0343 | 328. Codex implementation rule | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0344 | 329. But implementation details can be optimized | `docs/specs/ShadowBook.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0345 | 330. Test-first for critical modules | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0346 | 331. Benchmark-before-optimization | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0347 | 332. No optimization by aesthetic preference | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0348 | 333. No model complexity by prestige | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0349 | 334. Final production criteria | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0350 | 335. What “ready” does NOT require | `docs/09_RISK_CONSTITUTION.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0351 | 336. Final architecture can exist before all features active | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0352 | 337. Validation is the feature gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0353 | 338. Master rule | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0354 | 339. Economic acceptance | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0355 | 340. Risk acceptance | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0356 | 341. Calibration acceptance | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0357 | 342. Operational acceptance | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0358 | 343. Therefore | `docs/11_DATA_CONTRACTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0359 | 344. Final lifecycle | `docs/specs/Deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0360 | 345. Final project principle | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0361 | 346. But validation must not become paralysis | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-VALID-0362 | 347. Final scientific loop | `docs/specs/InfrastructureBenchmark.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0363 | 348. Final Definition of Done — PROJECT | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0364 | 349. La phase de développement est terminée lorsque | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0365 | 350. Principe final | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0366 | 351. Règle définitive de scaling | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0367 | 352. Conclusion | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0035 | Source preamble | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0006 | Pourquoi c’est probablement le meilleur modèle | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0036 | Le VPS n’est cependant pas techniquement obligatoire | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0037 | Et chaque client ne doit pas forcément prendre le même VPS | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0216 | Ça pourrait même devenir une fonctionnalité du Docker | `docs/14_DEPLOYMENT_AND_DOCKER.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PRODUCT-0015 | Commercialement | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0240 | 1. Objectif réel de cette partie | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0241 | 2. Principe fondamental | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0242 | 3. Pourquoi cette brique est particulièrement importante pour l’arbitrage | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SURV-0001 | 4. Nouvelle brique centrale : Edge Survival Engine | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0243 | 5. Définition mathématique de la vie d’une opportunité | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0049 | 6. Variable de survie | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0299 | 7. Limite actuelle du feed public Hyperliquid | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FUTURE-0005 | 8. Le node changera énormément cette partie plus tard | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SURV-0002 | 9. La Hazard Function | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SURV-0003 | 10. Pourquoi le hazard est parfait pour les arbitrageurs concurrents | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0038 | 11. Lien direct avec la PARTIE 1 sur les VPS | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0244 | 12. Ne pas confondre disparition de l’edge et concurrence | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0004 | 13. Cause-Specific Hazard | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0005 | 14. Edge Half-Life | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0245 | 15. Les features du modèle de survie | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0246 | 16. Order Flow Imbalance | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0006 | 17. Multi-Level OFI | `docs/_analysis/CONTRADICTIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0007 | 18. Queue Imbalance | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0008 | 19. Microprice | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-0001 | 20. Market Participants : comportement plutôt qu’identité | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-0002 | 21. Hyperliquid nous offre néanmoins une donnée inhabituelle | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0247 | 22. Mais une adresse n’est PAS une identité | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XMARKET-0001 | 23. Address Behaviour Signature | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0016 | 24. Détecter les arbitrageurs sans connaître leur stratégie | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0050 | 25. Le meilleur signal n’est pas « qui », mais « quand » | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XMARKET-0002 | 26. Correction Velocity | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-LIQ-0001 | 27. Liquidity Response Engine | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0248 | 28. Les événements fondamentaux | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0009 | 29. Queue-Reactive Model : rôle chez nous | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-LIQ-0002 | 30. Replenishment | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SLICE-0003 | 31. Pourquoi ça change notre slicing | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0249 | 32. Cancellation/Toxicity Response | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIQ-0003 | 33. Future Depth | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0250 | 34. Market maker adverse selection | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0251 | 35. Maker model complet | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0252 | 36. MT : formulation plus correcte | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0007 | 37. Hawkes Processes : challenger utile | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FUTURE-0006 | 38. Champion vs Challenger | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0006 | Champion initial | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FUTURE-0007 | Challenger | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FUTURE-0008 | Challenger supplémentaire | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FUTURE-0009 | Challenger ML | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RESEARCH-0016 | Research only | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0003 | 39. Cross-Market Response Engine | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0004 | 40. CrossMarketResponseMatrix | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0005 | 41. Ne pas créer une énorme matrice dense | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-XMARKET-0006 | 42. Sparse Cross-Market Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0253 | 43. Attention à la causalité | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XMARKET-0007 | 44. Méthode cross-market recommandée | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0008 | 45. Lead-Lag Discovery | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0009 | 46. Cross-market response et arbitrageurs | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-0003 | 47. Route-level Competition Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0254 | 48. Dominant Decay Leg | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0004 | 49. Route Competition Score | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0039 | 50. Integration avec notre Latency Distribution | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PRODUCT-0017 | 51. Expected Edge at Arrival | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PART-0005 | 52. Route EV avec Competition Model | `docs/18_OPERATIONS_AND_MONITORING.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0007 | 53. On ne doit PAS simplement multiplier edge × survival | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIM-0001 | 54. Intégration exacte avec le Counterfactual Simulator | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0255 | 55. Réaction à notre propre ordre | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0006 | 56. Mechanical Impact vs Participant Response | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0073 | Mechanical | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PART-0007 | Participant response | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0010 | 57. Response Model input principal : OFI shock | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0008 | 58. Impact Ratio | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0300 | 59. OOD Protection | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0008 | 60. Participant Model Confidence | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FUTURE-0010 | 61. Public L2 mode vs future L4 mode | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0256 | 62. Adresse-level modeling : activation secondaire | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0009 | 63. Participant clustering | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DATA-0316 | 64. Privacy / stockage | `docs/_analysis/CONTRADICTIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0301 | 65. Pas de requêtes API individuelles massives | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0257 | 66. Data collection requise | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0317 | 67. Opportunity Dataset | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0074 | 68. Important : stocker aussi les non-opportunités | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-CLOCK-0014 | 69. Edge birth labeling | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0051 | 70. Censoring | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SURV-0008 | 71. Premier modèle : empirical survival | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0009 | 72. Deuxième modèle : discrete hazard | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SURV-0010 | 73. Troisième modèle : survival GBDT | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0011 | 74. Deep survival : seulement si nécessaire | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0368 | 75. Train/Test split | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0369 | 76. Walk-forward validation | `docs/05_MARKET_MICROSTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-QUANT-0009 | 77. Probability calibration | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0052 | 78. Métriques statistiques | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0053 | 79. Economic Lift | `docs/18_OPERATIONS_AND_MONITORING.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-ARCH-0075 | Baseline | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0258 | New | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0370 | 80. Calibration avec Micro-Live | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0040 | 81. Address behaviour calibration en live | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0012 | 82. Model Drift | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0010 | 83. Fast / Recent / Medium / Long | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OPS-0018 | 84. Regime Classifier | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PRODUCT-0018 | 85. Online learning : pas directement dans la production | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0019 | 86. Champion / Challenger production | `docs/_analysis/TRACEABILITY_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0318 | 87. Versionnement des modèles | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0028 | 88. Hot Path : aucune grosse simulation | `docs/_analysis/extracted/data.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SIM-0002 | 89. Monte Carlo reste dans Execution Simulator | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0076 | 90. Architecture Rust | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SIM-0003 | 91. Integration simulator | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0077 | 92. Python R&D | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0006 | 93. Structures live | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-LIQ-0004 | 94. Liquidity forecast | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0259 | 95. Maker forecast | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0010 | 96. Cross-market forecast | `docs/_analysis/extracted/quant.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0011 | 97. Participant address forecast — optionnel | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-HWC-0028 | 98. HOT / WARM / COLD | `docs/REVIEW_REQUIRED.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-HWC-0029 | HOT | `docs/_analysis/extracted/testing.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-HWC-0030 | WARM | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-HWC-0031 | COLD | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0041 | 99. Global Watcher | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0012 | 100. Participant Model et Sizing | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0013 | 101. Participant Model et slicing | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0042 | 102. Participant Model et Infrastructure | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-0014 | 103. Participant Model et Market Atlas | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0015 | 104. Participant Model et Bridge Engine | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0016 | 105. Participant Model et Recovery | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0260 | 106. Ce qu’il ne faut SURTOUT PAS construire | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-0016 | 107. Agent-based simulation : véritable rôle | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIM-0004 | 108. Architecture finale : Fidelity Levels | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0017 | P0 — Historical participants | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0013 | P1 — Edge Survival | `docs/06_MARKET_PARTICIPANTS.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-EXEC-0261 | P2 — Aggregate Response | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-XMARKET-0011 | P3 — Cross Market | `docs/06_MARKET_PARTICIPANTS.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-PART-0018 | P4 — Participant Signatures | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SIM-0005 | P5 — Interactive Research | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0078 | 109. Priorité de développement | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0262 | Première priorité | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0014 | Ensuite | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIQ-0005 | Puis | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0263 | Puis | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-XMARKET-0012 | Puis | `docs/_analysis/OPEN_ITEMS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PART-0019 | Puis seulement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0020 | Enfin | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0015 | 110. Pourquoi Survival avant identification des bots | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-ACCT-0054 | 111. Acceptation d’un nouveau modèle | `docs/_analysis/TRACEABILITY_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0302 | 112. Safety fallback | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0303 | 113. Model disagreement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0304 | 114. Final execution formula | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0264 | 115. Version simplifiée de notre décision | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0265 | 116. Ce que cette partie apporte réellement au projet | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0079 | 117. Les trois modèles réellement fondamentaux | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SURV-0016 | 1 — Edge Survival Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIQ-0006 | 2 — Liquidity Response Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0013 | 3 — Cross-Market Response Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0266 | 118. Conclusion scientifique | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0267 | 119. Direction définitive que je recommande | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0043 | 120. Principe final de la partie 4 | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0010 | 1. Rôle général de la couche Quant | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0011 | 2. Architecture Quant recommandée | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0080 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RECOV-0017 | Contexte | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0305 | Formulation | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0055 | 4. Book Walk | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0012 | Pourquoi ? | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0011 | Où ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0140 | Formule | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0018 | Utilité | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0056 | 6. Fees | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OWA-0005 | 7. OWA 2 jambes | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0029 | Direct | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0030 | Indirect | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OWA-0006 | Edge | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0081 | Gain absolu | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OWA-0007 | 8. Où utiliser l’OWA Edge ? | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0306 | 9. Important : l’edge est une fonction de la taille | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0307 | 10. Edge Curve | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-TRI-0002 | 11. Triangle 3 jambes | `docs/_analysis/CONTRADICTIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0268 | 12. Conversion Alpha vs Execution Alpha | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0308 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0269 | Formulation simple | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0270 | 14. Version plus complète | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0271 | 15. Pourquoi l’EV est supérieure au simple edge | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0021 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SURV-0017 | Question | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0018 | 17. Pourquoi c’est central | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0019 | 18. Hazard Rate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0020 | 19. Edge Half-Life | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0044 | 20. Lien Survival × infrastructure | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0045 | 21. Exemple | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0007 | 22. Expected Edge at Arrival | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0141 | Où ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0272 | 24. Où utiliser QI ? | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0273 | Où ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0012 | 26. Multi-Level OFI | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0013 | 27. Utilisation de l’OFI | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0014 | Où ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0015 | 29. Pourquoi Microprice ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0013 | Où ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0057 | 31. Horizons multiples | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0019 | 32. Pourquoi la volatilité ? | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0309 | 33. Jump Risk | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0014 | 34. Impact | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0015 | Mechanical Impact | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-QUANT-0016 | Response Impact | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0017 | 35. Depth Participation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0274 | 36. Volume Participation | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0020 | 37. Out-of-Distribution | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-LIQ-0007 | 38. Liquidity Resilience | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-LIQ-0008 | 39. Pourquoi ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SLICE-0004 | 40. Optimal Slicing | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0275 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0276 | 42. Fill Probability n’est pas suffisante | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MAKER-0001 | 43. Adverse Selection | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0277 | 44. EV Maker | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0310 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0311 | 46. Pourquoi VaR n’est pas suffisante | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0312 | 47. CVaR | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0313 | 48. Utilisation de CVaR | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0031 | 49. Expected Shortfall par route | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0278 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SIM-0006 | 51. Sorties Monte Carlo | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SIM-0007 | 52. Monte Carlo : optimisation | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0314 | Où ? | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIZE-0003 | 54. Contraintes de sizing | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0018 | 55. Validated Capacity | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0058 | 56. Search de q* | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PORT-0001 | 57. Opportunity Portfolio Optimization | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0315 | 58. Contraintes portefeuille | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0279 | 59. Pourquoi ? | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0020 | 60. Balance Reservation | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0021 | 61. Inventory Penalty | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0082 | 62. Pourquoi quadratique ? | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PORT-0002 | 63. Portfolio Adjusted EV | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INV-0022 | 64. Stranded Capital Penalty | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0011 | 65. Bridge Optimization | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BRIDGE-0012 | 66. Break-even Cycles | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0019 | 67. Capital Relocation EV | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0059 | 68. Opportunity Cost | `docs/08_INVENTORY_AND_CAPITAL.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PART-0022 | Où ? | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-PART-0023 | 70. Usage | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0018 | 71. Cross-impact n’est pas forcément causal | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0019 | Où ? | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0280 | 73. Usage potentiel | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0020 | 74. Quand utiliser Hawkes ? | `docs/02_DOMAIN_MODEL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0016 | 75. Queue-Reactive | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0060 | 76. Pourquoi pas tout de suite ? | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0316 | 77. Drawdown | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0281 | 78. Sharpe Ratio ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0083 | 79. Sortino | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0142 | 80. Kelly Criterion ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0317 | 81. Usage éventuel de Kelly | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0282 | 82. Bayesian Updating | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-0024 | 83. Où ? | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0008 | 84. Confidence Intervals | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0046 | 85. Lower Confidence Bound | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0047 | 86. Infrastructure ROI | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0048 | 87. ROI incrémental | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0049 | 88. Simulation Confidence | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0061 | 89. Exemple | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0021 | 90. Model Disagreement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0318 | 91. Risk Adjusted EV | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0283 | 92. Attention au double comptage | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DATA-0319 | 93. Cela implique un Accounting Schema strict | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0017 | 94. Black-Scholes | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FUTURE-0011 | 95. Si options futures | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INV-0023 | 96. Perps futurs | `docs/_analysis/extracted/quant.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0020 | 97. Funding | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0021 | 98. Hedge Ratio | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0032 | 99. Ce qu’on doit calculer en HOT PATH | `docs/specs/RouteEngine.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0033 | 100. Ce qu’on ne calcule PAS dans le hot path | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0319 | 101. Pré-calculs | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0018 | 102. Incremental computation | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0320 | 103. SIMD / optimisation prématurée | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0084 | 104. Recherche Python | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0021 | 105. Production Rust | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0371 | 106. Golden Tests | `docs/_analysis/extracted/quant.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0021 | 107. Numerical Stability | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RECOV-0022 | 108. Precision / Rounding | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0034 | 109. Route Confidence | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0284 | 110. Décision finale | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0321 | 111. Ce que notre bot devient réellement | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0022 | 112. Les 10 outils Quant réellement CORE | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ROUTE-0035 | 1. NetConvert / L2 Book Walk | `docs/specs/NetConvert.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0023 | 2. Expected Value | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0022 | 3. Edge Survival / Hazard | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0019 | 4. OFI / Queue Imbalance / Microprice | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0322 | 5. Volatility / Jump Risk | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0285 | 6. Fill & Adverse Selection | `docs/06_MARKET_PARTICIPANTS.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-SIM-0008 | 7. Monte Carlo / Outcome Distribution | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0323 | 8. CVaR / Tail Risk | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIZE-0004 | 9. Constrained Position Sizing | `docs/08_INVENTORY_AND_CAPITAL.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PORT-0003 | 10. Portfolio Optimization | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0024 | 113. Les modèles QUANT de deuxième niveau | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PORT-0004 | 114. Les modèles qu’on n’a PAS besoin de construire maintenant | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0143 | 115. Principe d’optimisation général | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | CHECK REGISTER | NO |
| REQ-QUANT-0025 | 116. Quant Model ROI | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0026 | 117. La véritable philosophie Quant du projet | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0324 | 118. Résumé architectural final | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-0144 | 119. La formule conceptuelle ultime | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0145 | 120. Conclusion | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0146 | 1. Formules déjà quasiment définitives | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0147 | 2. Formules dont la structure est définie, mais dont les paramètres doivent être appris | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0148 | 3. Formules volontairement conceptuelles | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0020 | Un exemple très concret : OFI | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-FORMULA-0149 | Même chose pour la volatilité | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0150 | Ce qui manque donc réellement maintenant | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0027 | Et il nous faut faire ça pour environ 25–35 calculs centraux | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ACCT-0062 | Pricing / arbitrage | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0021 | Microstructure | `docs/04_FORMULA_BOOK.md` | FULL | UNVERIFIED | NO/REVIEW | NO/REVIEW | UNVERIFIED | NO |
| REQ-QUANT-0028 | Probability / execution | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0325 | Risk | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INV-0024 | Optimization | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0050 | Infrastructure | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-QUANT-0029 | Source preamble | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0286 | 1. Il faut séparer trois problèmes | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0287 | 2. Première couche : reproduire Hyperliquid lui-même | `docs/10_EXECUTION_STATE_MACHINE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0288 | 3. Timeline exacte d'une décision | `docs/_analysis/OPEN_ITEMS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0051 | 4. C'est déjà une énorme amélioration | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0289 | 5. Taker : Mechanical Impact | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-TRI-0003 | 6. Correction importante pour les triangles | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-VALID-0372 | 7. Notre Shadow State devient donc multi-market | `docs/17_IMPLEMENTATION_ROADMAP.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0373 | 8. Le plus gros problème du Shadow Book | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0018 | 9. C'est le vrai problème scientifique du market replay | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0290 | 10. Donc il faut deux branches bien distinctes | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-REPLAY-0019 | 11. Pourquoi garder le mode historique simple ? | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0291 | 12. Taker impact : le bon indicateur n'est pas seulement la taille | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0292 | 13. Order Flow Imbalance | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-MICRO-0022 | 14. Notre ordre crée donc un OFI shock | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0293 | 15. Et pas uniquement au prix | `docs/specs/ShadowBook.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0023 | 16. Queue-Reactive Model : très pertinent | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0030 | 17. Hawkes : deuxième outil utile | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0031 | 18. Je ne choisirais pourtant PAS directement un énorme modèle Hawkes | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0294 | 19. Donc notre premier Response Model devrait être un Conditional Empirical Model | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0295 | 20. Exemple | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0052 | 21. Ensuite seulement modèle paramétrique | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0296 | 22. Le maker est un problème différent | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0297 | 23. Mais il y a une subtilité importante avec le L2 | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0085 | L2 | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0298 | L4 | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0024 | 25. Avec seulement du L2, je veux trois simulations de queue | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0025 | Pessimistic Queue | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0026 | Optimistic Queue | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0027 | Probabilistic Queue | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0299 | 26. Ça nous donne immédiatement une fourchette | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0300 | 27. Notre Queue Model doit prédire plus qu'un simple fill | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0301 | 28. C'est crucial pour notre stratégie MT | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MAKER-0002 | 29. Adverse selection | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0302 | 30. Maintenant : comment inclure les autres bots ? | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0303 | 31. Les autres traders deviennent des processus de flux | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0304 | 32. Ça peut produire des comportements qui ressemblent naturellement à des bots | `docs/_analysis/extracted/execution.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XMARKET-0014 | 33. Cross-market response : indispensable pour nous | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0036 | 34. Notre pair_to_routes peut devenir aussi un pair_to_response_neighborhood | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-XMARKET-0015 | 35. Comment apprendre ces réactions cross-market ? | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-XMARKET-0016 | 36. Cela nous donne un CrossMarketResponseMatrix | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0032 | 37. Et elle répond directement au problème des autres arbitrage bots | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0305 | 38. Comment représenter le futur ? | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0306 | 39. Résultat attendu | `docs/_analysis/extracted/risk.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-0326 | 40. Il nous faut notamment la CVaR | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0086 | A | `docs/12_RECORDER_AND_REPLAY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RECOV-0023 | B | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0053 | 41. Simulation Confidence : on peut maintenant le définir correctement | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PRODUCT-0022 | 42. Très important : Out-of-Distribution | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0327 | 43. Donc la confiance peut devenir un Risk Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0020 | 44. Capacity = capacité VALIDÉE, pas profondeur brute | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0307 | 45. Ça répond directement au scaling | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SLICE-0005 | 46. Fragmentation : notre simulateur pourra enfin répondre scientifiquement | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0087 | scénario A | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0088 | scénario B | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0089 | scénario C | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0090 | scénario D | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0033 | 47. Même instant, même carnet | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SLICE-0006 | 48. Fragmentation temporelle | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-QUANT-0034 | 49. Le marché Bitcoin lui-même montre que le market impact ne se réduit pas à une simple règle linéaire | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SIM-0009 | 50. Comment gérer le futur historique après notre intervention ? | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0308 | 51. Au moment de l'ordre | `docs/05_MARKET_MICROSTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0309 | 52. Le marché possède une résilience | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0310 | 53. On aura donc une fonction de decay/résilience | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RECOV-0024 | 54. Branch-and-rejoin | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-LIQ-0009 | 55. Horizon variable | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIM-0010 | 56. Cas où on ne rejoin PAS facilement | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0025 | 57. Agent-based simulation : est-ce qu'on la garde ? | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0311 | 58. Ce que je NE veux surtout pas | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0091 | 59. Architecture finale que je construirais | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PRODUCT-0023 | 60. Architecture de fidélité — je modifierais notre V1/V2/V3/V4 | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0063 | F0 — Historical | `docs/17_IMPLEMENTATION_ROADMAP.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0054 | F1 — Latency + Mechanical | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-MICRO-0028 | F2 — Queue | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-LIQ-0010 | F3 — Responsive | `docs/_analysis/extracted/simulator.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SIM-0011 | F4 — Interactive Research | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0312 | 61. Et le simulateur choisit lui-même son niveau de confiance | `docs/06_MARKET_PARTICIPANTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0313 | 62. Données qu'on DOIT absolument enregistrer | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0374 | 63. Micro-live devient absolument indispensable | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0375 | 64. Chaque micro-live produit un datapoint | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0314 | 65. Pour le maker particulièrement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0376 | 66. Validation du slippage | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0377 | 67. Validation de la distribution | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FUTURE-0012 | 68. Champion / Challenger | `docs/06_MARKET_PARTICIPANTS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0092 | 69. Les autres bots seront donc intégrés à trois niveaux | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0093 | Niveau A — implicitement | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-ARCH-0094 | Niveau B — statistiquement | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-PART-0026 | Niveau C — explicitement | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0315 | 70. Ce que je considère comme NON nécessaire au départ | `docs/decisions/SUPERSEDED_DECISIONS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0316 | 71. En revanche certaines choses sont NON négociables dès le départ | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0317 | 72. Décision d'exécution finale | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0318 | 73. Exemple réaliste | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0037 | 74. Même route à 5 000 € | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIZE-0005 | 75. Donc notre sizing pourra utiliser directement le simulateur | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0319 | On garde | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0320 | On corrige | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-0151 | 77. La réponse fondamentale à notre interrogation n°3 | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0321 | 78. Direction que je figerais pour le projet | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0322 | Le principe final | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0323 | 1. TT — Taker → Taker | `docs/_analysis/CONTRADICTIONS.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0324 | 2. MT — Maker → Taker | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0325 | 3. TM — Taker → Maker | `docs/_analysis/SOURCE_INVENTORY.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-EXEC-0326 | 4. MM — Maker → Maker | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OWA-0008 | La subtilité importante pour notre OWA | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0327 | Ce que je corrigerais donc dans l’interrogation n°2 | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0055 | 1. Objectif de l’infrastructure | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0328 | 2. Décomposition de la latence | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0056 | 3. Localisation : Tokyo | `docs/_analysis/FINAL_AUDIT.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0057 | 4. Le node n’est PAS notre infrastructure de départ | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0058 | 5. Infrastructure minimum de départ | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0059 | 6. Pourquoi CPU dédié > beaucoup de vCPU partagés | `docs/specs/GlobalGraph.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0060 | 7. 10 Gb/s n’est pas notre KPI principal | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0061 | TradingFXVPS — VPS standard | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0062 | 9. TradingFXVPS — HFT VPS | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0063 | 10. TradingFXVPS — Semi-Dedicated | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0064 | 11. TradingFXVPS — HFT Dedicated | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0065 | 12. Akamai / Linode Dedicated CPU | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0066 | 13. Kamatera Type B | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0067 | 14. AWS Lightsail Compute Optimized | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0068 | 15. Sakura VPS Tokyo | `docs/05_MARKET_MICROSTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0069 | 16. Cherry Servers Performance VDS | `docs/_analysis/extracted/deployment.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0009 | 17. Shortlist de benchmark initial | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0070 | 18. Pourquoi benchmarker TradingFX Advanced ET HFT | `docs/_analysis/OPEN_ITEMS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0010 | 19. Principe du benchmark | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0095 | Phase A — Screening | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-RISK-0328 | Phase B — Finalistes | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CLOCK-0015 | 21. Synchronisation des horloges | `docs/08_INVENTORY_AND_CAPITAL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0011 | 22. Benchmark n°1 — First Market Data Arrival | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0012 | 23. Benchmark n°2 — Feed Age | `docs/11_DATA_CONTRACTS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0013 | 24. Benchmark n°3 — API / WebSocket RTT | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0014 | 25. Benchmark n°4 — Full Reconnect | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0015 | 26. Benchmark n°5 — Network Stability | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0071 | 27. Benchmark n°6 — Hot-Path CPU | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0072 | 28. Benchmark n°7 — Scheduler Jitter | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0073 | 29. Benchmark n°8 — CPU contention | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0329 | 30. Benchmark n°9 — Recorder Stress | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0016 | 31. Benchmark n°10 — Storage | `docs/decisions/SUPERSEDED_DECISIONS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0074 | 32. Benchmark n°11 — RAM | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-BENCH-0017 | 33. Benchmark n°12 — Docker Overhead | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ARCH-0096 | Native | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0217 | Docker | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ARCH-0097 | 34. Score technique de screening | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0330 | 35. Testnet Hyperliquid | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-VALID-0378 | 36. Micro-live mainnet | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0075 | 37. Test A/B entre deux infrastructures | `docs/16_VALIDATION_MATRIX.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0076 | 38. KPI économique n°1 — Capture Ratio | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SURV-0023 | 39. KPI n°2 — Opportunity Survival | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0077 | 40. KPI n°3 — Missed Opportunity Due To Infra | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0331 | 41. Pourquoi InfraLostPnL est fondamental | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0078 | 42. Shadow Infrastructure | `docs/_analysis/extracted/testing.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0079 | 43. Counterfactual Infra PnL | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0064 | 44. Coût incrémental | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ACCT-0065 | 45. Valeur nette de l’upgrade | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0080 | 46. Mais une valeur attendue positive ne suffit pas | `docs/_analysis/extracted/risk.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0066 | 47. Conservative Lower Bound | `docs/_analysis/SOURCE_INVENTORY.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0081 | 48. Infrastructure ROI Gate | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0082 | 49. Incremental Infra ROI | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ACCT-0067 | 50. PnL net absolu reste le KPI final | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0083 | VPS 40 € | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0084 | Dedicated 500 € | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0085 | 52. Ce que doit créer un serveur 500 € | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0086 | 53. Infrastructure Efficiency | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0087 | 54. Upgrade ET downgrade | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0021 | 55. Le capital n’est pas directement le trigger d’upgrade | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CAP-0022 | 56. Capital Bands : seulement comme résultat empirique | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-NODE-0003 | 57. Quand envisager un node Hyperliquid | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0088 | 58. Architecture logicielle : aucun code provider-specific | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0089 | 59. Modules Rust infrastructure | `docs/00_MASTER_ARCHITECTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-ROUTE-0038 | 60. Instrumentation du hot path | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0090 | 61. Structure LatencyTrace | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-INFRA-0091 | 62. InfraSnapshot | `docs/11_DATA_CONTRACTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0092 | 63. Attribution des pertes infra | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0332 | 64. Il faut éviter le double comptage | `docs/06_MARKET_PARTICIPANTS.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0018 | 65. Benchmark data versioning | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-BENCH-0019 | 66. Benchmark sans tuning d’abord | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-MICRO-0029 | 67. Pas de DPDK/kernel bypass au départ | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0333 | 68. Même règle pour SolarFlare | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-EXEC-0334 | 69. Déploiement de notre bot personnel | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0025 | 70. Déploiement pour les clients | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DEPLOY-0218 | 71. Docker comme contrat de déploiement | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0026 | 72. Configuration client | `docs/14_DEPLOYMENT_AND_DOCKER.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-DEPLOY-0219 | 73. API wallet par processus | `docs/_analysis/extracted/deployment.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-SEC-0021 | 74. Secrets | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-ROUTE-0039 | 75. Pas de service externe dans le hot path | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-0027 | 76. Les clients ne doivent PAS avoir besoin d’un node | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-CLIENT-0028 | 77. Profils matériels clients | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0093 | Minimum validé | `docs/00_MASTER_ARCHITECTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0094 | Recommended | `docs/02_DOMAIN_MODEL.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0020 | Performance | `docs/12_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0095 | 78. Le produit doit faire son propre diagnostic infra | `docs/_analysis/SOURCE_INVENTORY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0019 | 79. Monitoring production | `docs/13_INFRASTRUCTURE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-OPS-0020 | 80. Alertes importantes | `docs/05_MARKET_MICROSTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0329 | 81. La performance infra doit entrer dans le Risk Engine | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0096 | 82. Rolling Infra Model | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0335 | 83. Décision d’upgrade : pipeline complet | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0330 | 84. Conditions finales d’upgrade | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0097 | 85. Condition de downgrade | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0336 | 86. Rapport automatique mensuel | `docs/01_PRODUCT_AND_SCOPE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0098 | 87. Exemple inverse | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-0020 | 88. Relation avec notre Replay Engine | `docs/07_COUNTERFACTUAL_SIMULATOR.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SIZE-0006 | 89. Relation avec le sizing | `docs/00_MASTER_ARCHITECTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0337 | 90. Relation avec maker/taker | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-TRI-0004 | TT / TTT | `docs/09_RISK_CONSTITUTION.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-TRI-0005 | MT / MTT | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-RISK-0331 | 91. Rate limits | `docs/REVIEW_REQUIRED.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0338 | 92. Dead Man’s Switch | `docs/_analysis/extracted/execution.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OPS-0021 | 93. Restart sécurisé | `docs/14_DEPLOYMENT_AND_DOCKER.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0099 | 94. Infrastructure de backup | `docs/13_INFRASTRUCTURE.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OPS-0022 | 95. Expected Downtime Loss | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-OPS-0023 | 96. Le backup peut également commencer cheap | `docs/_analysis/extracted/deployment.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-BENCH-0021 | 97. Budget benchmark | `docs/_analysis/OPEN_ITEMS.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0100 | Wave 1 | `docs/17_IMPLEMENTATION_ROADMAP.md` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-0101 | Wave 2 seulement si nécessaire | `docs/16_VALIDATION_MATRIX.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FUTURE-0013 | Beaucoup plus tard | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-DEPLOY-0220 | 99. Ce qu’on ne fait PAS | `docs/04_FORMULA_BOOK.md` | NONE | UNVERIFIED | YES | NO/REVIEW | CHECK REGISTER | YES |
| REQ-EXEC-0339 | 100. Ce que l’on GARDE définitivement | `docs/_analysis/extracted/deployment.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-INFRA-0102 | 101. Principe final de toute la partie 1 | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-0340 | 102. Direction finale pour notre démarrage | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-OWA-9001 | OWA candidate versus Bridge / Capital Relocation | `docs/03_MARKET_GRAPH_AND_ROUTES.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SIZE-9001 | Position Sizing is economic allocation | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-SLICE-9001 | Order Slicing is mechanical execution | `docs/10_EXECUTION_STATE_MACHINE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-FORMULA-9001 | ConversionAlpha structural route advantage | `docs/04_FORMULA_BOOK.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-FORMULA-9002 | ExecutionAlpha execution-method advantage | `docs/04_FORMULA_BOOK.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-EXEC-9001 | Expected state never overrides exchange truth | `docs/10_EXECUTION_STATE_MACHINE.md` | SUBSTANTIAL | UNVERIFIED | NO/REVIEW | POSSIBLE | UNVERIFIED | NO |
| REQ-RISK-9001 | Unknown means no new risk, not halt everything | `docs/09_RISK_CONSTITUTION.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-REPLAY-9001 | Replay/Live core parity | `docs/08_DATA_RECORDER_AND_REPLAY.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-DET-9001 | Deterministic decision identity | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-SIM-9001 | Calibrated plausible outcomes, not exact alternate universe | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-PART-9001 | Collective participant effects, not synthetic identities as truth | `none` | NONE | UNVERIFIED | YES | NO/REVIEW | UNVERIFIED | YES |
| REQ-INFRA-9001 | Economic upgrade/downgrade gate | `docs/13_INFRASTRUCTURE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |
| REQ-CLIENT-9001 | Per-client non-SaaS deployment | `docs/01_PRODUCT_AND_SCOPE.md` | PARTIAL | UNVERIFIED | YES | YES | UNVERIFIED | NO |

## Summary

- NONE: 521
- PARTIAL: 1479
- SUBSTANTIAL: 560
- FULL: 30
