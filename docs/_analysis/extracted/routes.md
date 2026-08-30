# Extraction — routes et sizing

## Sources

SRC-002/SRC-003 pour l'évolution; SRC-004 Formula Book et SRC-005 Risk priment.

## Contrats retenus

- Direct `A→B`; OWA `A→X→B` seulement avec direct comparable; triangle
  `A→X→B→A`; sinon bridge/relocation.
- `NetConvert` marche L2, frais dynamiques et précision à chaque jambe;
  `Edge=Edge(q)`.
- ConversionAlpha compare route TT/direct T; ExecutionAlpha compare modes.
- Core TT/MT/TTT/MTT; TM/MM disabled.
- Position sizing décide le total; order slicing le découpage.
- `Q_validated` exige EV, P+, ES/CVaR, impact, inventory, confidence et support.
- Balances, book capacity et risk ne peuvent être double-comptés; réservation
  avant ordre.
- OpportunityPortfolio suit QF-078; approximations à valider.
- Graphe venue-aware V1; cross-venue trading `FUTURE` disabled.
