# 01 — Product and Scope

## Produit

Logiciel installé sur le VPS d'un client pour observer, simuler puis exécuter du
routing/arbitrage spot Hyperliquid. V1 porte l'architecture finale mais active
les capacités par maturité M0→M5.

## Objectifs

- Détecter direct, OWA 2-leg et triangle 3-leg sur prix exécutables.
- Estimer la capture après latence, compétition et risque d'exécution.
- Allouer un capital fini sans double compter balances/profondeur/risque.
- Gérer partial fills, unknown states, recovery et restart sans ambiguïté.
- Produire une preuve auditable/rejouable de chaque décision.
- Mesurer la valeur nette de la stratégie et de l'infrastructure.

## Dans le core

- Same-venue Hyperliquid spot.
- TT/MT pour OWA, TTT/MTT pour triangles, protected IOC et ALO.
- Graph venue-aware, inventaire CORE/TRANSIT/EXCLUDED, bridge interne.
- Recorder, replay déterministe, simulateur contrefactuel progressif.
- Déploiement client isolé et opérations sûres.

## Non-objectifs actifs

- Trading cross-exchange, perps/options, hedging dérivés, retraits automatiques.
- Market making généraliste, cycles 4+ génériques.
- Identités réelles de participants ou population d'agents prétendue fidèle.
- Node Hyperliquid, C++, GPU/FPGA, lock-free partout sans ROI/benchmark.
- Mutualisation SaaS du hot path.

Ces points sont `FUTURE` ou `RESEARCH`, pas promesses V1.

## Utilisateurs et frontières

- Propriétaire/reviewer : valide décisions, limites, micro-live et scaling.
- Opérateur client : installe, diagnostique, met à jour et rollback via `botctl`.
- Research : produit des artefacts candidats versionnés; ne modifie pas live
  automatiquement.
- Core : consomme uniquement des artefacts approuvés et vérifiés.

## Critères produit

Une stratégie n'est viable que si elle produit un PnL économique net avec des
erreurs simulation→réel bornées, une tail risk acceptée, une capacité validée et
des opérations sûres. « Le code tourne » n'est pas une validation stratégique.

## Statut

Architecture/scope : `LOCKED FOR REVIEW`. Paramètres, modèles, capital et
infrastructure : `CALIBRATED/LEARNED/OPEN` selon `OPEN_ITEMS.md`.
