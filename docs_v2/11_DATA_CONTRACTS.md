# 11 — Data Contracts

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

This document fixes the contracts that let the system prove what it received, knew, derived, decided and observed. The target identity is one decision engine across Replay, Paper, Shadow, MicroLive and Live; only sources, transports, effects and explicit configuration differ.

## 2. Authority

SRC-005 Dossier 4/6 is the closure authority for schemas, state ownership, time, lineage and determinism. SRC-004 owns formulas and execution semantics. SRC-006 owns validation. SRC-003 supplies uncontradicted Recorder/storage depth. Earlier exploration is retained only where compatible. Current Hyperliquid wire semantics remain externally revalidated.

## 3. Fundamental data principles

The invariant pipeline is:

```text
SOURCE DATA → NORMALIZED EVENTS → DERIVED STATE → DECISIONS → EXECUTION EVENTS
```

No layer may silently substitute for another. Every decision-relevant value has a meaning, unit, time, version and source. Text logs help humans but are never the evidence needed to reconstruct state.

## 4. L0–L4 layers

| Layer | Canonical content | Mutability | Authority |
|---|---|---|---|
| L0 RAW | Payload bytes exactly as locally observed plus capture envelope | Append-only, immutable | Historical source evidence |
| L1 NORMALIZED EVENTS | Typed `MarketEvent`, `AccountEvent`, `InfraEvent`, `TimerEvent`, `ControlEvent` | Immutable | Versioned interpretation of L0 |
| L2 STATE | `BookState`, `AccountState`, `InventoryState`, `ReservationState`, `InfraState`, execution state | Single-writer evolution | Canonical run state |
| L3 DERIVED FEATURES | Features, forecasts, route economics, confidence | Immutable snapshots | Recomputable, versioned derivation |
| L4 DECISIONS / RESULTS | Opportunity, RiskDecision, ExecutionPlan, OrderIntent, effects, fills and PnL evidence | Append-only decisions/results | Audit and outcome chain |

L0 is source evidence, not a claim that the source was correct. L1–L4 are never permitted to erase or rewrite L0.

## 5. RawEvent

The canonical conceptual envelope is:

```text
RawEvent {
  event_id,
  recorder_seq,
  source,
  source_connection_id,
  exchange_ts?,
  recv_wallclock_ts,
  recv_monotonic_ns,
  market?,
  event_type,
  source_seq?,
  block_id?,
  payload_bytes,
  schema_version
}
```

`event_id` supports uniqueness, deduplication, trace and replay. `recorder_seq` is strictly increasing per Recorder and is the definitive local observation order; it is never replaced by exchange time. `payload_bytes` preserves the ability to re-normalize after a parser correction. Optional source fields remain absent when unavailable; they are never fabricated.

## 6. Time semantics

`exchange_ts?` represents chronology asserted by the exchange and may be absent. It is useful for market research, not for proving when the bot learned something. `recv_wallclock_ts` supports historical logs and cross-machine comparison subject to synchronization quality. `recv_monotonic_ns` owns local elapsed-time, timer and internal-latency differences. Cross-machine results attach uncertainty and are valid only under a declared rule. See [Clock and Time Contract](_analysis/pass06_data_recorder_replay/CLOCK_AND_TIME_CONTRACT.md).

## 7. Source / SourceQuality

The closed `Source` enum is:

```text
HyperliquidPublicWs | HyperliquidRest | HyperliquidNode | Replay | SyntheticTest
```

`SourceQuality { fidelity, age, sequence_integrity, clock_quality }` accompanies normalized evidence as applicable. Unknown, stale or gapped is not encoded as zero or healthy. The exact meaning of Hyperliquid timestamps, sequences and block identifiers must be verified against the current official interface before implementation.

## 8. Normalized events

`MarketEvent` is exactly `BookSnapshot`, `BookDiff`, `Trade`, `MetadataUpdate`, `MarketStatus`, or `Heartbeat`. `AccountEvent` is `OrderUpdate`, `Fill`, `BalanceUpdate`, `FeeUpdate`, or `AccountSnapshot`. The central input union adds `Infra`, `Timer` and `Control` events. Strategic timers are explicit events so replay does not depend on scheduler timing.

Every `NormalizedEvent` carries `normalized_schema_version`, `source_raw_event_id` and the typed payload. An unknown exchange event is recorded in RAW, alerted, and left unnormalized until understood. A missing required field or impossible value is rejected and cannot mutate canonical state.

## 9. Exact numeric representation

Exchange-boundary prices and quantities use integer `price_ticks` and `quantity_lots`/`size_lots`, with the same versioned precision and rounding code in every run mode. Identifiers (`MarketId`, `AssetId`, `FillId`, and related IDs) are strong types. Units are explicit through names such as `_ns`, `_ms`, `_bps`, `_ticks`, `_lots`, `_quote`, `_base`, and `_usd`. Statistical models may use floats; exchange-critical comparisons do not.

## 10. Canonical state

Per run/context there is one logical `BookState` per market and one canonical `AccountState`, `InventoryState`, `ReservationState` and execution state. There is no untraceable parallel truth. `BookState` enforces sorted sides, non-negative sizes, valid best prices and monotonic versioning; a gap or impossible state marks it invalid until resynchronization. Fills are deduplicated by `FillId` across stream, snapshot and reconciliation.

## 11. Snapshot/version ownership

Critical mutable state has one logical writer. Readers receive immutable, atomically published snapshots with versions. Decisions refer to exact book/account/inventory/reservation/infra/feature versions. Before send, material version changes are checked against the plan validity envelope; the plan is revalidated, replanned or aborted. A changed tick alone need not abort when the declared envelope remains valid.

This is the **single writer** rule. Every immutable snapshot exposes a **snapshot version**.

## 12. EventReducer / Effects

State evolution follows:

```text
State(n+1) = Reducer(State(n), Event(n))
```

Reducers perform no network access, blocking disk work or hidden randomness. They return new state plus requested effects such as `SubmitOrder`, `CancelOrder`, `Persist`, `EmitMetric` or `RequestReconciliation`. A separate EffectExecutor invokes the environment-specific boundary and returns observed events. A command such as `SubmitOrder` is an intention; `OrderSubmitted`, `OrderRejected` or `FillEvent` is evidence of reality.

## 13. Module contracts

Adapters convert external payloads to normalized events and never mutate Core state. Strategy reads snapshots and emits Opportunities. Risk consumes a frozen RiskSnapshot and ExecutionForecast and emits a RiskDecision. Execution requests effects; state changes only from ordered events. Workers may compute features, inference, route simulation, compression and analytics, but return their `input_state_version` for discard/revalidation if stale. Cyclic hidden dependencies are forbidden.

A **stale worker result** never commits automatically. Forecasts expose `valid_until` or an equivalent explicit validity rule.

## 14. Schema versioning

Every serialized family has a documented version, field types, nullability and units. Additive optional changes may remain backward compatible; breaking changes increment the major version. Permanent fields are deprecated before removal. Old readers may ignore safe unknown optional fields, but missing required fields fail. Rust domain types are the internal source of truth while external/dataset contracts remain independently documented for audit and Python parity.

## 15. Model / Formula / Dataset versions

```text
ModelVersion {
  model_id, semantic_version, training_dataset_id,
  feature_schema_version, artifact_hash
}
```

`FeatureSchemaVersion` prevents silent feature drift. `FormulaSchemaVersion` pins calculation, fee and rounding semantics. `DatasetId` resolves date ranges, RAW manifests, normalization version and filters. A `GoldenDataset` is small, permanent, checksum-verified and used for regression, Rust/Python parity and deterministic replay.

## 16. RunManifest

Every run records the exact closure schema:

```text
RunManifest {
  run_id,
  mode,
  git_commit,
  build_hash,
  config_hash,
  dataset_id?,
  model_versions,
  formula_schema_version,
  event_schema_version,
  start_time,
  random_seed?
}
```

Deployment/image digest and critical environment dependency locks must be associated with the manifest where deployment/research reproducibility requires them. `ResolvedConfig`, never raw user input or hidden defaults, is addressed by `config_hash`.

## 17. DecisionTrace

The frozen trace is:

```text
DecisionTrace {
  ordered_decisions[],
  order_intents[],
  state_transitions[],
  risk_decisions[]
}
```

Correlation IDs link MarketEvent → Opportunity → RiskDecision → ExecutionPlan → Intent → Cloid/Oid → Fill → PnL. Periodic canonical state hashes and the DecisionTrace hash identify the first divergent `recorder_seq` without copying every object into every record.

## 18. Deterministic ordering

For recorded truth, the primary key is local receive chronology. The canonical total-order key is `(recv_monotonic_ns, source_priority, recorder_seq)` within one capture context; `recorder_seq` is the final unique tie-break and definitive local observation order. Cross-recorder merging must first define a versioned merge policy and clock-uncertainty handling; it must not pretend exchange time supplies local knowledge order. Source priority may resolve equal-time concurrency but may never reorder economically dependent evidence across established receive order.

Live adapters publish concurrently into one ordered core coordinator. Replay preserves the recorded order. Workers may run in parallel, but only the ordered coordinator commits decisions and state transitions.

## 19. Clock/RNG

Core code depends on `Clock`, implemented by `LiveClock`, `ReplayClock` and `TestClock`, never directly on wall time. ReplayClock advances with the input schedule and preserves relative durations when accelerated. Randomness comes only from `RngProvider`; replay seeds are stored in RunManifest. Material live stochastic outputs are recorded, and unnecessary live random choices are avoided.

## 20. Data lineage

The minimum chain is:

```text
RawEvent → NormalizedEvent → Book/Account State → FeatureSnapshot
→ Opportunity → ModelForecast/ExecutionForecast → RiskDecision
→ ExecutionPlan → OrderIntent → exchange AccountEvent/Fill → PnL/evidence
```

Each edge is represented with typed IDs, versions and hashes. Formula outputs reference their route/quantity, book versions, fee version, formula version and result. Incorrect source data can therefore identify every dependent decision and outcome.

## 21. Point-in-time correctness

Historical-truth replay uses only metadata, fees, models, configs and artifacts that were available at time T. A modern model may be applied to old data only in a research counterfactual labeled `COUNTERFACTUAL_MODEL` in its manifest/result. Time-series splits require `training_end < validation_start`; random leakage is forbidden. Model artifacts record their training range. Dataset quality and invalid regions are part of admissibility, not hidden preprocessing.

## 22. Checkpoints/state persistence

Persistent economic state survives container replacement. Periodic versioned checkpoints may include AccountState, InventoryState, ReservationState and execution summaries; reconstructible caches remain ephemeral. A checkpoint accelerates recovery but is never truth. Restart uses:

```text
compatible checkpoint + append-only journal + exchange reconciliation
```

No instance reaches READY before reconciliation establishes consistency.

The persisted compatibility discriminator is `checkpoint_schema_version`.

## 23. Compatibility/migrations

Startup gates check event, model-feature, formula, config and checkpoint compatibility. An incompatible model disables its dependent strategy; invalid config fails boot; incompatible state requires an explicit tested migration or rebuild/reconciliation. Live never silently discards or migrates economic state. Migration output must replay to the same decision/state result as the supported source version or document an intentional versioned semantic change.

## 24. Testability

Serialized contracts require encode/decode round trips, compatibility tests and invalid-field rejection. Real payload fixtures cover normal, edge and historical forms. Builders support synthetic market, fill and failure events. Property tests generate event/fill/cancel/partial sequences. Fuzzing targets payload parsers, serialization, reducers, precision and state machines. Golden replay asserts exact opportunities, rejects, intents and state, with economically defined tolerance only after fixed quantization for PnL.

## 25. Final determinism contract

```text
DecisionTrace = F(
  OrderedEvents,
  ResolvedConfig,
  ModelArtifacts,
  FormulaVersion,
  Seed
)
```

Equal events, resolved config, artifacts, formula semantics and seed must produce the same ordered DecisionTrace and hash. Canonical collection ordering and serialization must not depend on `HashMap` iteration, thread completion order, hardware scheduling or non-canonical float bytes. Replay is the bot connected to a historical source and simulated transport; it is not a simplified backtest engine.

## 26. Deep-spec links

- [Data deep specifications](deep-specs/data/README.md)
- [Data Contract Inventory](_analysis/pass06_data_recorder_replay/DATA_CONTRACT_INVENTORY.md)
- [Ordering Contract](_analysis/pass06_data_recorder_replay/EVENT_ORDERING_CONTRACT.md)
- [Replay Determinism Contract](_analysis/pass06_data_recorder_replay/REPLAY_DETERMINISM_CONTRACT.md)
- [Schema Compatibility Matrix](_analysis/pass06_data_recorder_replay/SCHEMA_VERSION_COMPATIBILITY_MATRIX.md)
- [Recorder and Replay](12_RECORDER_AND_REPLAY.md)
