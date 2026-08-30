# Hyperliquid Arbitrage Bot

Documentation canonique d'un moteur spot de routing/arbitrage Hyperliquid.

Le dépôt décrit l'architecture, les contrats, les invariants, les formules, la
gestion du risque, l'exécution, le replay, le déploiement et la validation. Aucun
bot de production n'est encore implémenté : la documentation doit d'abord être
revue et approuvée.

## Commencer ici

1. [Index de la documentation](docs/README.md)
2. [Architecture maîtresse](docs/00_MASTER_ARCHITECTURE.md)
3. [Périmètre produit](docs/01_PRODUCT_AND_SCOPE.md)
4. [Formula Book — QF-001 à QF-110](docs/04_FORMULA_BOOK.md)
5. [Risk Constitution](docs/09_RISK_CONSTITUTION.md)
6. [Execution State Machine](docs/10_EXECUTION_STATE_MACHINE.md)
7. [Roadmap d'implémentation](docs/17_IMPLEMENTATION_ROADMAP.md)
8. [Revue requise](docs/REVIEW_REQUIRED.md)

## Contenu

- 19 documents maîtres numérotés `00` à `18`;
- 46 spécifications de modules;
- 18 Architecture Decision Records proposés pour revue;
- un inventaire sourcé, une matrice de traçabilité et un audit final;
- aucune dépendance ou logique de trading de production.

## Gouvernance

Les décisions architecturales restent `PROPOSED FOR REVIEW`. Les paramètres
marqués `CALIBRATED`, `LEARNED` ou `OPEN` ne doivent pas devenir des constantes
implicites. Les règles Hyperliquid susceptibles d'évoluer doivent être
revalidées contre les sources officielles avant implémentation.

Voir [l'ordre de revue recommandé](docs/REVIEW_REQUIRED.md#recommended-review-order)
et [l'audit documentaire](docs/_analysis/FINAL_AUDIT.md).

`DOCUMENTATION STATUS: REVIEW REQUIRED`
