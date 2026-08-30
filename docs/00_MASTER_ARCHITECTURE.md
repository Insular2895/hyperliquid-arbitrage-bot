# 00 — Master Architecture

## Vision

Construire un moteur spot Hyperliquid venue-aware qui connaît l'univers entier,
mais consacre le calcul coûteux aux routes accessibles au capital. Il mesure les
opportunités exécutables — carnet, frais, précision, latence, exécution, risque
et inventaire inclus — et refuse toute exposition dont l'état n'est pas sûr et
reconstructible.

## Principes LOCKED

1. Safety > StateConsistency > ExistingExposure > RiskLimits > ExpectedPnL >
   Opportunity.
2. `NetConvert` est l'unique primitive de conversion exécutable.
3. L'edge est une fonction de la taille; la profondeur visible n'est pas la
   capacité validée.
4. Connaître tout; calcul cher là où se trouve le capital.
5. Réserver balances, profondeur et risque avant tout ordre.
6. L'état exchange est la vérité; aucun retry aveugle; actual fills seulement.
7. Recovery et reconciliation sont des sous-systèmes de premier rang.
8. Même core et mêmes contrats en replay, paper, shadow, micro-live et live.
9. L'observation et l'enregistrement ne bloquent jamais le hot path.
10. Activation progressive d'une architecture finale; pas de MVP jetable.

## Architecture logique

```text
Exchange / Replay
       │
       ▼
FeedAdapter → Normalizer → BookEngine ───────────────→ Recorder
                              │                         │
                              ▼                         ▼
                    MarketState / Features        RAW / events
                              │
                              ▼
          Metadata/Fee/Precision + GlobalGraph
                              │
                              ▼
              affected RouteEngine candidates
                              │
                    HOT / WARM / COLD
                              │
                              ▼
                    OpportunityEngine
                              │
              Participant / Survival forecasts
                              │
                              ▼
                  CounterfactualSimulator
                              │
                    Sizing / Portfolio
                              │
                 Inventory / Reachability
                              │
                              ▼
                         RiskEngine
                              │
                    ReservationEngine
                              │
                              ▼
                  ExecutionCoordinator
                    │       │        │
                    ▼       ▼        ▼
                  Orders   Fills   Recovery
                    │       │        │
                    └───────┴────────┘
                              │
                  Reconciliation/Accounting
                    │                    │
                    ▼                    ▼
                Inventory           Calibration
```

## Flux de décision

```text
valid/fresh book
→ affected precomputed routes
→ cheap BBO rejection
→ exact L2 NetConvert at candidate sizes
→ direct/indirect/cycle comparison
→ survival/arrival/execution distribution
→ Terminal Viability + post-trade inventory
→ RAEV, P+, ES/CVaR, confidence
→ shared capacity allocation
→ hard risk gates
→ reserve
→ ExecutionPlan or typed RejectReason
```

Une décision conserve les inputs/version IDs, les composantes économiques et
chaque gate. `EXECUTE` n'est jamais déduit d'un score opaque.

## Flux d'exécution

```text
PLANNED → reserve → submit protected order → ACK/FILL/UNKNOWN
      actual filled amount only → reprice remaining plan
      compare EV_continue vs EV_recovery after each material event
      complete OR recovery → reconciliation → release reservation
```

Cancel envoyé ≠ cancel confirmé. `SENT` peut être rempli. Une incertitude stoppe
le nouveau risque, jamais la récupération d'une exposition existante.

## Hiérarchie de risque

```text
Global Risk
  └─ Inventory / Allocation Risk
       └─ Route Risk
            └─ Leg Risk
                 └─ Order Risk
```

Le niveau global peut réduire l'activité, pas relâcher un niveau inférieur.
Les hard invariants sont des gates, non des coûts économiques.

## HOT / WARM / COLD

- `HOT`: routes proches du capital et candidates; calcul exact et incrémental.
- `WARM`: confirmation plus poussée et promotion possible.
- `COLD`: surveillance structurelle/cheap BBO par Global Watcher.
- `CapitalReachabilityEngine` calcule les régions atteignables et coûts de
  bridge. Hystérésis/cooldown évitent le flip-flop; seuils `CALIBRATED`.
- Le recorder conserve la fidélité utile à la recherche indépendamment de cette
  classification de compute.

## Séparation research/live

| Plan | Rôle |
|---|---|
| Rust core | feed, books, graph, quant, risk, execution, recorder, replay |
| Python lab | Parquet/DuckDB, recherche, calibration, rapports, challengers |
| Replay | événements historiques via les interfaces du core |
| Shadow | marché live, vrais plans, aucun ordre envoyé |
| Micro-live | faible capital validé, calibration fills/latence |

Python ne prend aucune décision synchrone du hot path. C++ n'entre que si un
profil et un benchmark prouvent une valeur nette.

## Déploiement initial

Un VPS isolé par client, un compte/signer, un process/container non-root,
secrets externes, stockage local borné et archive asynchrone. Aucun SaaS partagé
sur le hot path. Feed public initial; node seulement si l'InfrastructureROI le
justifie. Licence/updates ne doivent jamais bloquer recovery/reconciliation.

## Graphe de dépendances modules

```text
Adapters → Books ─┬→ Features/Participants/Survival ─┐
Metadata ─────────┼→ Graph/Routes → Opportunities ───┼→ Simulator
Fees/Precision ───┘                                  │
Simulator → Sizing/Portfolio → Inventory/Capital → Risk/Reservation
Risk/Reservation → Execution → Recovery/Reconciliation → Accounting
All events → Recorder → Replay/Research → calibrated/versioned artifacts
Infrastructure/Deployment/Monitoring support every live boundary
```

Les cycles de données sont autorisés via événements immuables/versionnés; les
dépendances d'appel du hot path restent acycliques.

## Propriétés de sûreté transverses

NO STALE BOOK; NO UNKNOWN FEES; NO DOUBLE SPENDING; RESERVE BEFORE ORDER; NO
BLIND RETRY; ACTUAL FILL ONLY; RECONCILE BEFORE NEW RISK; NO MARTINGALE; NO NEW
RISK WHEN UNRECONCILED; NO EV OVERRIDES HARD SAFETY.

## Sources

SRC-001..008; autorité détaillée dans `_analysis/SOURCE_INVENTORY.md` et
`TRACEABILITY_MATRIX.md`.
