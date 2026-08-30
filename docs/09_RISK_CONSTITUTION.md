# 09 — Risk Constitution

## Autorité

Ce document condense SRC-005 Dossier 3/6. En cas d'écart, l'extraction
`_analysis/extracted/risk.md` et la source spécialisée priment jusqu'à revue.

## Ordre constitutionnel

```text
Safety
  > StateConsistency
  > ExistingExposure
  > RiskLimits
  > ExpectedPnL
  > Opportunity
```

L'EV aide à classer des actions autorisées. Elle n'autorise jamais à violer un
invariant. Les profits accumulés ne créent aucun droit au risque supplémentaire.

## Invariants hard INV-001 à INV-030

| ID | Invariant canonique |
|---|---|
| INV-001 | No Trade Without Valid Market State |
| INV-002 | No Trade On Stale Book |
| INV-003 | Route Freshness = Worst Leg Freshness |
| INV-004 | No Unknown Metadata |
| INV-005 | Fees Must Be Known |
| INV-006 | Exchange Precision Is Mandatory |
| INV-007 | No Negative Available Balance |
| INV-008 | Unknown Capital Is Reserved Capital |
| INV-009 | No Double Spending |
| INV-010 | Reservations Before Orders |
| INV-011 | Shared Depth Cannot Be Double Counted |
| INV-012 | Actual Fill Beats Expected Fill |
| INV-013 | Next Leg Uses Actual Previous Fill |
| INV-014 | No Blind Retry |
| INV-015 | Cancel Sent ≠ Canceled |
| INV-016 | Partial Fill Creates Real Exposure |
| INV-017 | Existing Exposure Has Priority |
| INV-018 | Recovery May Be Negative EV |
| INV-019 | Recovery Is Not Unlimited |
| INV-020 | Sunk Costs Are Sunk |
| INV-021 | No Averaging Down By Default |
| INV-022 | No Martingale |
| INV-023 | No New Risk In RECOVERY_ONLY |
| INV-024 | No New Risk In HALTED |
| INV-025 | No Trading While Account State Is Unreconciled |
| INV-026 | Clock Must Be Healthy |
| INV-027 | Required Feeds Must Be Healthy |
| INV-028 | Trading Requires InfraHealth == ACCEPTABLE |
| INV-029 | Slow Compute Can Become a Risk Event |
| INV-030 | Recorder Must Never Block Execution |

Ces invariants sont indivisibles. Licence, optimisation, profit antérieur,
commande manuelle ou fallback ne les relâchent pas. Les actions strictement
réductrices de risque suivent une permission dédiée sans devenir illimitées.

## Gates avant réservation

Engine READY; feed/books valides; clock sain; metadata/fees/precision connus;
route/version cohérentes; direct comparator pour OWA; balances/capacités
disponibles; terminal viable; hard inventory bands; size/notional/impact;
`RAEV`, P+, ES/CVaR et confidence; route/asset/global limits; no kill switch.

## Gates avant submit et jambe suivante

Réservation encore valide, book/price limit frais, nonce/signer/transport sains,
ordre normalisé. Après un fill, recomposer inventory et quote avec quantité
réelle, revalider gates, puis comparer `EV_continue` et `EV_recovery`. Aucun
output pré-trade ne traverse cette frontière.

## Hiérarchie opérationnelle

- Order: price limit, size, normalization, duplicate/CLOID.
- Leg: fill/partial/unknown, latency, exposure instantanée.
- Route: completion/recovery distribution et shared depth.
- Inventory/allocation: bands, flow, stranded/reachability.
- Global: drawdown, data/system health, correlated exposure, strategy halt.

## Kill switches

Taxonomie : `GLOBAL_KILL`, `MARKET_KILL`, `ASSET_KILL`, `STRATEGY_KILL`,
`EXECUTION_MODE_KILL`, `MODEL_KILL`, `INFRA_KILL`. Déclencheurs typés :
feed/clock/book corruption, reconciliation failure,
unknown exposure, repeated execution mismatch, abnormal slippage/latency,
reservation invariant, drawdown/tail breach, disk/recorder failure selon niveau,
secret/signer/nonce anomaly. Action : disable new risk, cancel si sûr, préserver
account events, recover/reconcile, alerter et exiger acknowledgement selon classe.
Seuils `CALIBRATED`.

## Limites

Par order/leg/route/asset/location/global; notional, intermediate exposure,
concurrency, pending unknown, loss, recovery reserve, drawdown, P+, ES/CVaR et
confidence. Valeurs absentes dans `OPEN_ITEMS.md`; aucune valeur par défaut
implicite.

## Changement et preuve

Config versionnée, four-eyes pour limites sensibles, replay + failure injection
avant promotion, rollback atomique. Chaque reject/kill porte reason code, input
versions et invariant/gate responsable.

## Sources

SRC-005 D3, SRC-004 exécution/Formula Book, SRC-006 validation.
