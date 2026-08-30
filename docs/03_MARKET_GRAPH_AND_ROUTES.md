# 03 — Market Graph and Routes

## Graphe

Chaque `Market(base, quote, venue)` crée deux arêtes dirigées : base→quote sur
les bids et quote→base sur les asks. Une arête appelle `NetConvert(amount,
book, fee_state, precision, execution_mode)`; elle ne stocke pas un taux unique.

Le graphe est venue-aware dès V1 (`BTC@Hyperliquid`) afin d'éviter une refonte,
mais seules les arêtes same-venue Hyperliquid sont tradables initialement.

## Routes

- Direct : `A→B`, référence d'une intention de conversion.
- OWA : `A→X→B` comparé au direct `A→B` pour même input et output B.
- Triangle : `A→X→B→A`, PnL dans A.
- Bridge/relocation : chemin vers une destination sans comparateur direct ou
  motivé par la valeur future du capital.
- CrossVenue : arêtes de trade/transfer futures, désactivées.

Sans direct comparable, l'étiquette OWA et son alpha sont interdits.

## Pré-calcul et dépendances

MetadataEngine construit/reconstruit les routes de longueur 2 et cycles de
longueur 3, puis `market_id → route_ids`. Une update recalcule uniquement les
routes touchées. Un changement de metadata/frais/précision invalide les objets
affectés avec nouvelle version; pas de mutation historique.

## Compute policy

Global Watcher connaît toutes les régions. HOT effectue BBO+L2 exact sur les
routes accessibles; WARM confirme une promotion/relocation; COLD conserve une
observation bon marché. Promotion/demotion a hystérésis, et l'inventaire ainsi
que la reachability déterminent la priorité. Paramètres `CALIBRATED`.

## Pipeline route

```text
BookUpdate → affected routes → freshness/validity → BBO bound
→ exact direct and indirect/cycle curves → fees/precision
→ microstructure/survival → simulator → sizing
→ terminal/inventory/shared capacity → risk → execute/reject
```

## Modes d'exécution

- Core : TT, MT, TTT, MTT.
- Future support disabled : TM, MM, et tout maker en jambe terminale sans hedge
  et preuve de risque.
- ConversionAlpha compare structures avec intention temporelle équitable;
  ExecutionAlpha isole l'effet maker/taker.

## Capacité

Les routes partagent balances, niveaux de book et budget risque. Une
`RouteDependency` décrit chaque ressource consommée. Une réservation réduit
immédiatement la capacité visible des autres opportunités. Le futur
OpportunityPortfolio optimise l'ensemble des tailles sous contraintes; une
sélection gloutonne n'est admise que si validée comme approximation.

## Sources

SRC-002/003, SRC-004 QF-016..027 et QF-073..078, SRC-005 invariants.
