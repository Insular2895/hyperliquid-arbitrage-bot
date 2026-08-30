# Extraction — Risk

## Source d'autorité

- SRC-005, Dossier 3/6, lignes 1–5373 environ.
- Statut documentaire : final / normatif.

## Constitution LOCKED

Hiérarchie :

`Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL > Opportunity`.

Une optimisation EV ne s'exécute que dans l'ensemble des actions sûres. Les hard
invariants sont des interdictions, pas des pénalités compensables.

Ordre opérationnel : protéger l'exposition, annuler les ordres unsafe, réconcilier
l'inconnu, récupérer l'inventaire indésirable, terminer une route sûre,
rééquilibrer, puis seulement prendre une nouvelle opportunité.

## Hard invariants INV-001 à INV-030

- état marché valide/frais/metadata/précision connus; aucun trade sur book stale;
  freshness route = pire jambe;
- solde disponible jamais négatif; capital inconnu réservé; aucun double spend;
  réservation avant ordre; profondeur partagée non double-comptée;
- fill réel et solde exchange dominent prévisions/local; jambe suivante basée sur
  le fill réel; aucun blind retry; cancel n'est pas canceled; partial = exposition;
- exposition existante prioritaire; recovery négative permise mais bornée; sunk
  costs ignorés; pas d'averaging down ni martingale par défaut;
- aucun nouveau risque en `RECOVERY_ONLY`, `HALTED` ou compte non réconcilié;
- clock, feeds et infrastructure doivent être acceptables; compute trop lent est
  un risque; Recorder ne bloque jamais l'exécution.

## Gates

- System/data/account/resources/hard inventory d'abord, puis market-impact,
  model support/OOD, execution forecast, tail risk, soft inventory/portfolio,
  EV, sizing et revalidation pré-send.
- Market : spread, liquidity/validated capacity, depth et volume participation,
  impact, jump, volatility.
- Competition/model : capture/survival, edge attendu à l'arrivée, confiance
  décomposée, OOD, disagreement, simulation valide.
- Economique/tail : `P(PnL>0)`, ExpectedPnL, Expected Shortfall, worst validated
  loss.
- Sizing : borne minimale par capacité validée, solde, inventaire, impact et
  budget risque; aucune taille universelle.
- Inventory : `Target`, `SoftMin`, `SoftMax`, `HardMin`, `HardMax`; hard band
  infranchissable par `NEW_RISK`, exception uniquement pour réduction stricte.
- Terminal viability et stranded risk conditionnent une OWA même positive.
- Maker : ALO, unhedged exposure, maximum age, edge death, toxicity et
  réévaluation sur chaque fill. Taker : IOC/marketable limit protégé.
- Multi-leg : risk check après chaque jambe, no route loyalty, dust explicite.
- Portfolio : capital at risk, concurrence, dépendances/corrélations et tail risk
  agrégé.

## Kill switches et dégradation

Taxonomie : `GLOBAL_KILL`, `MARKET_KILL`, `ASSET_KILL`, `STRATEGY_KILL`,
`EXECUTION_MODE_KILL`, `MODEL_KILL`, `INFRA_KILL`. Les stratégies déclarent
dépendances obligatoires, optionnelles et fallbacks. Faute d'information : fail
closed pour le nouveau risque; seules les actions réduisant une exposition connue
peuvent utiliser une politique plus large.

Déclencheurs incluent drift, erreurs de calibration fill/PnL/slippage, changement
fees/metadata, feed gaps, anomalies trop belles, rate limits, drawdown/loss
velocity, défaillance infra et violations numériques/état.

## Gouvernance

- Les clients peuvent resserrer les limites, pas désactiver la constitution.
- Chaque paramètre porte valeur, unité, scope, source, version, date effective et
  domaine validé. Aucune magic number.
- Un Challenger ne modifie pas le live avant promotion; un fallback est plus
  conservateur. Le live prime sur le replay, mais les changements demandent un
  support statistique.
- `RiskDecision` est déterministe, auditable, versionné, machine-readable et
  obligatoire avant transport.

## CALIBRATED / LEARNED

Stale thresholds, spread/impact/participation/jump/volatility limits, P_min,
capture/arrival thresholds, Expected Shortfall et per-route loss limits,
inventory bands/penalties, maker exposure/age/cancel/toxicity, drawdown/loss
windows, rate/capital/risk budgets, TTL risk, client profiles et scaling bands.

## Tests

Chaque invariant a unit/property/fault tests pertinents. Faults obligatoires :
lost response, feeds, clock, model NaN, disk full, CPU saturation. Le failure
mode recherché est moins d'activité, jamais plus d'exposition.
