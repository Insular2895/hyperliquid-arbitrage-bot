# Hyperliquid Arbitrage — documentation canonique

Cette arborescence consolide la conception d'un bot spot de routing/arbitrage
Hyperliquid. Elle décrit le produit, les contrats, les invariants, les états,
les formules, la validation et l'exploitation. Elle n'implémente rien.

## Autorité documentaire

1. Dossiers de fermeture spécialisés : exécution, Formula Book, Risk
   Constitution, Data Contracts, déploiement, validation.
2. Documents maîtres `00` à `18`.
3. ADR acceptés lors de la revue.
4. Specs modules.
5. Notes historiques et extractions.

En cas d'écart, ouvrir une contradiction; ne pas arbitrer silencieusement. Les
valeurs `CALIBRATED`, les faits externes et toutes les décisions encore en revue
ne doivent pas être transformés en constantes.

## Statuts

- `LOCKED`: règle de conception stabilisée, encore soumise à la revue finale.
- `CALIBRATED`: forme définie, valeur à mesurer.
- `LEARNED`: résultat issu de données/version de modèle.
- `FUTURE`: compatible mais non actif.
- `RESEARCH`: expérimental, hors décision live par défaut.
- `REJECTED` / `SUPERSEDED`: interdit ou remplacé.
- `OPEN`: preuve/choix réellement manquant.

## Lecture

Commencer par [00_MASTER_ARCHITECTURE.md](00_MASTER_ARCHITECTURE.md), puis suivre
l'ordre de [REVIEW_REQUIRED.md](REVIEW_REQUIRED.md). Les développeurs consultent
ensuite [specs/MODULE_INDEX.md](specs/MODULE_INDEX.md); les reviewers suivent
[_analysis/TRACEABILITY_MATRIX.md](_analysis/TRACEABILITY_MATRIX.md).

## Discipline

- Documentation seulement; aucune autorisation d'implémenter n'est donnée.
- Les règles exchange externes doivent être revalidées contre une source
  officielle au moment de la phase concernée.
- Un invariant hard n'est jamais converti en pénalité EV.
- Replay, shadow et live utilisent les mêmes contrats et le même core.

`DOCUMENTATION STATUS: REVIEW REQUIRED`
