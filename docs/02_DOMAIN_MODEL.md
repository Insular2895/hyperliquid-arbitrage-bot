# 02 — Domain Model

## Identités fortes

`VenueId`, `AssetId`, `AssetLocationId`, `MarketId`, `RouteId`, `OpportunityId`,
`DecisionId`, `ExecutionPlanId`, `RouteExecutionId`, `OrderIntentId`, `ClOid`,
`ExchangeOrderId`, `FillId`, `ReservationId`, `RecoveryId`, `RunId`, `DatasetId`,
`ModelVersionId`, `ConfigVersionId`, `SchemaVersion` ne sont pas des strings
interchangeables.

## Valeurs typées

`Price`, `BaseQty`, `QuoteQty`, `Notional`, `FeeRate`, `Bps`, `Timestamp`,
`MonotonicNanos`, `Sequence`, `Latency`, `Probability`, `Pnl` portent unité,
asset/market et règles de précision. L'arithmétique exchange utilise unités
discrètes/fixed point quand possible; les modèles peuvent utiliser `f64` à leur
frontière puis repassent par PrecisionEngine.

## Agrégats

- `MarketMetadata`: paire base/quote, statut, précision, minimums et version.
- `BookState`: niveaux, séquence, source, freshness/validity.
- `MarketState`: books + features point-in-time.
- `DirectedEdge`: fonction `NetConvert`, pas prix scalaire.
- `Route`: Direct, OWA, Triangle, Bridge, future CrossVenue.
- `Opportunity`: snapshot immuable d'une route/tailles/features.
- `PortfolioState`: balances actual/available/reserved et inventaire valorisé.
- `ExecutionPlan`: intentions ordonnées, limits, expiries, reserves et versions.
- `FillLedger`: append-only, dédupliqué; source des quantités exécutées.
- `RunManifest`: dataset/config/code/model/clock/RNG/fidelity et hashes.

## États et événements

L'état courant est une projection d'événements normalisés et snapshots
versionnés. Les événements de marché, account, décision, order, fill, recovery,
reconciliation, health, metadata et configuration portent temps exchange,
wall-clock local, monotonic et ordre recorder si disponibles.

## Relations

```text
Venue ─ AssetLocation ─ Asset
Venue ─ Market(base, quote) ─ two DirectedEdges
Route ─ ordered DirectedEdges ─ RouteDependencies
Opportunity ─ Route + PointInTimeState + candidate sizes
Decision ─ Opportunity + gates + versions
ExecutionPlan ─ Decision + Reservations + OrderIntents
Fills ─ Orders ─ RouteExecution ─ Accounting/Inventory
```

## Règles

- Une route et ses versions sont immuables dans un run.
- Un fill dédupliqué modifie inventory/accounting une seule fois.
- Un snapshot publié est immuable; single writer par agrégat mutable.
- Aucun événement futur n'est visible à une décision replay.
- Les conversions entre unités/assets sont explicites.

## Sources

SRC-005 Data Contracts, SRC-004 exécution/Formula Book, SRC-003 venue-aware.
