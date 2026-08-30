# Extraction — simulateur contrefactuel

## Source

SRC-008; SRC-004 Formula Book et SRC-005 Data Contracts priment.

## Contrats retenus

- Aucun futur alternatif exact : distribution calibrée de scénarios plausibles.
- Arrivée `t0+compute+sign+network+exchange`, composantes mesurées.
- Impact mécanique local séparé de participant/cross-market response.
- `EXOGENOUS_REPLAY` distinct d'`INTERACTIVE_COUNTERFACTUAL`.
- L2 donne bounds de queue; L4 seulement si réellement disponible.
- F0 historique, F1 latency+mechanical, F2 queue, F3 responsive, F4 interactive
  research; une architecture progressive.
- Monte Carlo produit mean/median/P+/VaR/ES/partials/recovery/confidence, mais
  reste hors hot path lourd.
- Micro-live calibre slippage/fill/latency/response; `Q_validated` déclare sa
  fidelity et confidence.
