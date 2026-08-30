# Extraction — Formula Book

## Source d'autorité

- SRC-004, Dossier 2/6, lignes 3310–9808 environ.
- Statut documentaire : final / normatif.

## Conventions

- Prix d'un marché `(B,Q)` en quote par base; quantités typées base/quote.
- `PnL>0` est un gain. `Loss=-PnL`; les tails regardent les grandes pertes
  positives. `1 bp = 10^-4`.
- Calculs exchange/monétaires en ticks/lots/fixed point autant que possible;
  modèles en f64 possibles, puis retour aux unités discrètes.
- Une seule implémentation/version par formule; parity Python/Rust et golden tests.

## Registre canonique

Le Formula Book définit QF-001 à QF-110 : pricing/depth/precision (001–016),
routes/alpha/edge curve (017–027), microstructure (028–043), survival/maker/
execution EV (044–063), inventory/capital/sizing/recovery (064–080), participant/
infra (081–094), calibration/model value (095–105) et accounting/drawdown
(106–110).

Les équations et statuts complets sont consolidés dans `04_FORMULA_BOOK.md`.

## Paramètres explicitement non fixés

Minimum edge, OFI weights, volatility horizons, jump threshold, hazard/maker/
replenishment/cross-market parameters, inventory and uncertainty penalties,
opportunity rate, P_min, CVaR/ES limits, confidence limits, infra safety factor,
maker max age et ACK timeout.

## Formules volontairement hors core V1

Black-Scholes, Greeks, Heston, SABR, CAPM, Markowitz classique et surfaces de
volatilité options. Options/perps restent des extensions futures, pas des
capacités actives.

## Pipeline mathématique LOCKED

Valider freshness; quantifier la taille; walk L2; frais; rounding intermédiaire;
walk jambe suivante; output; conversion edge; forecast arrival/participants;
distribution d'exécution; ExpectedPnL; tail risk; inventory/stranded penalties;
RAEV; sizing; final risk gates. Aucun taux théorique suivi d'un slippage approximé.
