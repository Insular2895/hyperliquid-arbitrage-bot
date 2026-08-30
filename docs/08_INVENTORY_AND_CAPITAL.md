# 08 — Inventory and Capital

## États d'actifs

- `CORE_INVENTORY`: destination normale prouvée par liquidité, reachability,
  opportunity density et exit quality.
- `TRANSIT`: intermédiaire accepté pour une durée et exposition bornées.
- `EXCLUDED`: aucune nouvelle exposition; recovery peut toutefois chercher une
  sortie sûre.

Cette classification est versionnée, issue du MarketAtlas et gouvernée; aucun
nom d'asset n'est verrouillé par intuition.

## Ledger

Pour chaque `AssetLocation`: actual, available, reserved, pending/uncertain,
target, soft/hard bands, net flows et valorisation. `Available=Actual-Reserved`
et ne devient jamais négatif. Pending/unknown n'est jamais réputé disponible.

## Bandes et flow

Les soft bands génèrent une pénalité calibrée; les hard bands refusent toute
nouvelle exposition dans le mauvais sens. Le flow sur plusieurs fenêtres peut
réduire la taille avant la hard limit. Recovery/reconciliation suivent leurs
propres permissions et ne sont pas bloquées par un gate conçu pour du nouveau
risque.

## Terminal Viability

Avant OWA : simuler `PortfolioAfter` et vérifier sorties directes/multi-hop,
depth, exit cost, volatilité, idle time, opportunités futures et stranded risk.
Une ConversionAlpha positive peut être rejetée. La destination, le comparateur
et le numéraire sont explicites.

## Bridge / relocation

Comparer tous chemins accessibles via `NetConvert`. `Value(move)` suit QF-072;
BridgeCost, ExpectedExitCost, RelocationRiskCost, `EV_destination` et `EV_stay`
restent séparés. Hystérésis/cooldown empêchent les allers-retours. Une relocation
perdante n'est pas maquillée en OWA.

## Shared capacity et réservations

Réserver balances, book slices et risk budget avant submit; release seulement
sur terminalité/reconciliation prouvée. Les routes dépendantes voient la
capacité résiduelle. Position sizing et order slicing sont distincts.

## Portfolio d'opportunités

Objectif futur/canonique QF-078. Une politique plus simple doit déclarer son
approximation, démontrer qu'elle ne double-compte rien et être comparée OOS.

## Venue-aware

Les balances sont localisées (`BTC@Hyperliquid`). Cross-venue trading et
transferts restent disabled. S'ils sont activés ultérieurement : inventaire
préfinancé, directional capacity, shadow cost, natural reverse flow avant
transfert et ADR/validation dédiés seront obligatoires.

## Accounting

Conserver séparément ConversionAlpha, ExecutionAlpha, route/recovery/rebalance
PnL, inventory MTM, external flows et EconomicPnL. Les dépôts/retraits ne sont
pas du profit.

## Sources

SRC-003; QF-064..080/105..110; Risk Constitution.
