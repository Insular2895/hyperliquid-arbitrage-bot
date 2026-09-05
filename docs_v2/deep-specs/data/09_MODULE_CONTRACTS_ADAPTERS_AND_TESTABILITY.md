# Module Contracts, Adapters and Testability

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Dependency direction

```text
domain types → market/account state → quant/features
→ strategy/models → simulator → risk → execution
```

Controlled interfaces prevent hidden cycles. `BookEngine(MarketEvent) → BookSnapshotRef`; `RouteEngine(BookSnapshotRefs, RouteDefinitions) → RouteEconomics`; `ParticipantEngine(FeatureSnapshot) → ModelForecasts`; `Simulator(candidate, market state, forecasts) → ExecutionForecast`; `RiskEngine(RiskSnapshot, ExecutionForecast) → RiskDecision`; `ExecutionCoordinator(ExecutionPlan) → Effects/ExecutionEvents`; `InventoryEngine(FillEvents, BalanceEvents) → InventoryState`.

Domain types remain light on external APIs and storage libraries. Adapters isolate Hyperliquid schema changes and emit normalized events only. Parser failure cannot mutate state. Execution transport owns submit/cancel/query effects without leaking transport behavior into Core decisions.

## Contract tests

- encode/decode roundtrip and schema compatibility for every serialized type;
- real payload regression fixtures, unknown optional and missing required fields;
- golden ticks/lots/rounding and canonical serialization;
- reducer property tests over duplicates, gaps, partials, cancels and reorderings;
- fuzz payload parsers, serialization, reducer and state-machine boundaries;
- same input across Live-compatible and Replay adapters produces the same normalized/core trace;
- worker results with stale versions never commit.

## Documentation acceptance

Each critical module documents purpose, input, output, invariants, versions, failure behavior, effects, tests and performance budget. Implementation choices may vary only behind these contracts.
