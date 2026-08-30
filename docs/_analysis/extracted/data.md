# Extraction — Data contracts and determinism

## Source d'autorité

- SRC-005, Dossier 4/6, lignes 5374–9877.
- Statut documentaire : final / normatif.

## Contrat central

`RAW → Normalized Events → State → Derived Features → Decisions/Results`.

Le même core traite Replay, Paper, Shadow, Micro-live et Live. Source, transport,
capital et risk config peuvent varier; stratégie, formules, reducers et automates
ne divergent pas.

`DecisionTrace = F(OrderedEvents, ResolvedConfig, ModelArtifacts,
FormulaVersion, Seed)`.

## Règles LOCKED

- RAW append-only, immutable, timestamped, versioned, checksummed; normalization
  régénérable et liée au `RawEvent` source.
- Distinguer `exchange_ts`, `recv_wallclock_ts` et `recv_monotonic_ns`; ne jamais
  inventer un timestamp exchange. Le replay du comportement réel suit l'ordre de
  réception.
- `recorder_seq` strictement croissant et ordre canonique explicite pour les
  égalités/concurrence. No lookahead.
- Types forts pour IDs, assets, markets, ticks/lots, money/unités, versions et
  numéraire. Les valeurs déterminantes portent meaning, unit, timestamp, version,
  source.
- Un propriétaire logique unique pour Account/Reservation/Execution; lecteurs sur
  snapshots immuables/versionnés; reducers purs autant que possible et effects
  exécutés séparément.
- Commande/intention et événement/réalité sont distincts.
- `Clock` (`LiveClock`, `ReplayClock`, `TestClock`) et `RngProvider` abstraits;
  timers stratégiques deviennent des événements rejouables.
- Les forecasts mentionnent version, snapshot d'entrée, confidence/OOD et durée
  de validité. Un résultat worker stale est rejeté ou revalidé.
- Chaque run porte `RunManifest`, hashes code/build/config, datasets, versions de
  modèles/formules/schémas et seed.
- Replay, live et Python/Rust utilisent mêmes Fee/Precision/Route/Risk/Execution/
  Recovery/Inventory/Reservation contracts. Aucune formule dupliquée.
- Checkpoint local n'est jamais source de vérité : checkpoint + journal +
  reconciliation exchange.
- PnL sépare route, recovery, rebalance, bridge, inventory, fees et infra; les
  external flows ne sont pas du profit; aucun double accounting.

## Types centraux

`RawEvent`, `MarketEvent`, `BookSnapshot`, `BookDiff`, `TradeEvent`,
`MarketDefinition`, `BookState`, `AccountEvent`, `OrderUpdate`, `FillEvent`,
`AccountState`, `InventoryState`, `ReservationState`, `RouteDefinition`,
`Opportunity`, `OpportunityEpisode`, `FeatureSnapshot`, `ModelForecast` et ses
spécialisations, `ExecutionForecast`, `RiskSnapshot`, `RiskDecision`,
`ExecutionPlan`, `OrderIntent`, `SignedOrderIntent`, `TransportRequest`,
`EngineInputEvent`, `DecisionEvent`, `RejectEvent`, `InfraState`,
`ResolvedConfig`, `RunManifest`, `LatencyTrace`, `BenchmarkRun`,
`ModelPredictionRecord`, `EventEnvelope`, `StateTransition`, `IncidentRecord`.

## Replay et simulation

- Modes replay : exact receive-time, accelerated, counterfactual latency,
  interactive.
- Fidélités : F0 Historical à F4 Interactive; mode `ExogenousReplay` distinct de
  `InteractiveCounterfactual`; branches et Monte Carlo paths identifiés.
- Shadow conserve `ActualAccountState` séparé du
  `ShadowCounterfactualState`; Micro-live est le live avec limites réduites.

## Recorder et rétention

Recorder asynchrone/non bloquant. Priorités P0 account/execution, P1 windows
autour des trades, P2 général marché, P3 diagnostics. En backpressure, dégrader
les faibles priorités, alerter, préserver le critique. Chaque dataset porte
coverage, gaps, clock quality et régions invalides.

Permanent : fills, orders, executions, risk decisions, configs, versions,
incidents. RAW général plus court; windows trade/incident conservées davantage.

## Tests

Roundtrip/compatibilité des schémas, golden replay, hash déterministe, no
lookahead, multi-thread determinism, reconstruction journal + exchange,
property/fuzz/serialization tests, parser corpus, Python/Rust parity et startup
compatibility gates.
