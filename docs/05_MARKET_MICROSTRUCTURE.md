# 05 — Market Microstructure

## Objet

Mesurer la fragilité d'un edge entre observation et arrivée/exécution. Ces
features ne créent pas une permission d'exécuter; elles alimentent prévision,
simulation et risk gates.

## État incrémental

Pour chaque marché : spread/mid, profondeurs par bandes, QI/MLOFI, OFI par
niveaux/fenêtres, microprice/dislocation, log returns/RV/volatility/jump score,
trades, depth/volume participation, freshness et data-quality. L'état est mis à
jour au fil des events, pas recalculé lourdement à la détection.

## OFI

Utiliser QF-030/031 pour les contributions bid/ask, QF-032/033 pour agrégation.
Fenêtres, niveaux et weights sont `CALIBRATED`. L'OFI reste `OBSERVE_ONLY` tant
qu'un lift hors échantillon et économique n'est pas démontré; il ne devient pas
un hard filter par intuition.

## Liquidité et impact

- L'impact mécanique est le book walk de notre ordre sur le marché concerné.
- Resilience mesure la reconstruction de profondeur après shock.
- Add/cancel/market buy/market sell/replenishment sont des réponses distinctes.
- La réponse des autres marchés appartient au modèle cross-market, jamais à
  l'impact mécanique local.

## Volatilité et jumps

Calcul point-in-time sur plusieurs horizons explicites. Les données futures,
fenêtres centrées et régimes calculés après coup sont interdits au moment de la
décision. JumpScore est un diagnostic calibré, pas un threshold universel.

## Qualité et fallbacks

Book stale/crossed/incomplet, gap sequence, horloge incohérente ou metadata
unknown invalident le marché affecté. En absence de support modèle, fallback
conservateur ou reject; jamais une valeur neutre optimiste.

## Validation

Walk-forward temporel, calibration par horizon/régime/taille, ablation de chaque
feature, economic lift après coût de latence, drift monitoring. Formules :
QF-001..006, 028..043, 094..104.

## Sources

SRC-002/007, SRC-004 Formula Book, SRC-005 Risk/Data.
