# 12 — Recorder and Replay

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

Recorder preserves sufficient source, decision and execution evidence to reproduce the bot's knowledge and calibrate simulation against reality. Replay feeds that evidence into the same production Core. Research prioritizes return to the past; production prioritizes explanation of every real decision while retaining representative market evidence.

## 2. Recorder architecture

```text
Feed/Account adapters ──→ ordered Core
          └─────────────→ bounded non-blocking capture queue → Recorder → local chunks
Core decisions/effects ─→ critical journal/evidence path
closed verified chunks ─→ asynchronous archive
```

Recorder is parallel to Core and has explicit health, queue, disk and upload state. Structured events, not text logs, own reconstruction.

## 3. Non-blocking requirement

Core never performs file writes, fsync, compression or cloud upload in the decision path. Enqueue behavior is bounded and observable. Slow disk or cloud cannot silently add material hot-path latency. If Recorder health loss compromises mandatory auditability, Risk receives `RecorderHealth` and applies the configured fail-safe policy; this does not justify blocking the core loop.

## 4. RAW storage

L0 stores the exact `payload_bytes` plus RawEvent envelope, append-only and immutable. Compact binary serialization plus ZSTD is the locked architectural direction; the exact binary codec is an implementation decision gated by roundtrip, compatibility and performance evidence. JSON is limited to debugging/human exports, not giant RAW streams.

## 5. chunks/checksums

RAW is segmented into small independently closeable chunks. The exploratory 5–15 minute duration is `CALIBRATED`, not a constant. Each closed chunk has:

```text
RawChunkManifest {
  file_id, start_ts, end_ts, event_count,
  checksum, compressed_size, schema_version
}
```

The cryptographic checksum is verified before archive acceptance or local cleanup. Chunk order and boundary metadata preserve all Recorder sequences.

## 6. normalized/derived data

Normalization is asynchronous and reproducible: `RAW → versioned NormalizedEvent → Parquet + ZSTD` for analytics. The canonical partitioning direction is date/hour/market, adjusted only by measured workload. Derived features, forecasts, opportunities and research tables are versioned and trace back to RAW; none can become the sole historical source of a decision.

## 7. priorities

The closure hierarchy is exact:

| Priority | Evidence |
|---|---|
| P0 | fills, account and execution |
| P1 | market windows around executions/incidents |
| P2 | general market events |
| P3 | derived diagnostics |

SRC-003's older P2-derived/P3-general-RAW ordering is superseded by SRC-005. Priority is a retention/backpressure class; it cannot reorder canonical economic events.

## 8. backpressure

Saturation never silently blocks the hot path. P0 is preserved first, then P1. Lower-priority capture degrades explicitly from P3 upward according to a versioned policy; dropping, sampling or suspending P2/P3 emits counters, health events and alerts. No loss is relabeled as complete data. If critical P0 cannot be durably preserved, the state is critical and new-risk policy must react.

## 9. dataset quality

Every dataset/run reports coverage, sequence gaps, clock quality, missing markets, events received/written/dropped and applicable source fidelity. `INVALID_FOR_REPLAY` marks a region that cannot support claimed replay semantics; `LOW_FIDELITY` permits only explicitly compatible uses. Selection filters and exclusions are stored in DatasetId lineage.

## 10. invalid regions

Feed gap, corrupted clock, invalid book, checksum failure, missing required market or ambiguous ordering creates a bounded region with reason, start/end sequences/times and affected markets/contracts. It is never silently imputed. Historical-truth replay must reject an invalid region; research may use low-fidelity input only with manifest labeling and bounded claims.

## 11. retention classes

`PERMANENT`, `LONG`, `MEDIUM`, `SHORT` are locked classes; exact days are calibrated by measured volume, legal/business needs and reconstruction value. Permanent includes fills, orders, executions, risk decisions, configs, model versions, incidents, GoldenDatasets and validation evidence. General market RAW may be SHORT. Class changes are explicit metadata, not ad hoc deletion.

## 12. trade/incident windows

Every real execution and incident pins pre-, execution- and post-windows of relevant RAW market/account/infra evidence to a longer class. Exploratory examples such as 5 seconds before/10 after or 10 before/20 after are calibration candidates only. The retained window must support predicted-versus-actual fill, slippage, latency, participant response, recovery and PnL reconstruction.

These **trade windows** and incident windows are retention evidence, not a new event-ordering mechanism.

## 13. local buffer/archive

Local NVMe is the working buffer for active chunks, journals, checkpoints and recent datasets. Object storage is the provider-neutral durable archive. Cloud outage builds an observable upload backlog without entering the hot path. Direct recording to synchronization services such as iCloud is forbidden. Local deletion requires closed chunk, successful upload, checksum verification, applied retention metadata and no preservation tag.

## 14. ExecutionJournal

The journal is separate, append-only critical evidence:

```text
ExecutionJournalEvent { journal_seq, event, timestamp, checksum? }
```

The minimum event set is `ExecutionCreated`, `ReservationCreated`, `OrderIntentCreated`, `OrderSent`, `FillApplied`, `CancelRequested`, `RecoveryStarted`, `ExecutionCompleted`. PASS 04 owns full execution transitions. Journal records and exchange reconciliation rebuild state; logging alone cannot.

## 15. checkpoints

Versioned checkpoints accelerate seeking and restart. They store compatible canonical state and the exact journal/Recorder cursor they cover. They never override later journal entries or exchange truth. Corrupt/incompatible checkpoint means reject, migrate explicitly, or rebuild from earlier evidence; never boot READY by discarding it silently.

## 16. Replay architecture

```text
historical Raw/Normalized source → ReplayClock → ordered EngineInputEvents
→ same reducers/engines/risk/execution state machine
→ ReplayTransport/ExchangeEmulator → same AccountEvents
```

Replay does not fork formulas, strategy, risk, recovery, inventory, reservation or state-machine logic. SimulatedAccountState conforms to AccountState. Shadow keeps actual and counterfactual account states strictly separate.

## 17. Replay modes

| Mode | Ordering/time | Market response |
|---|---|---|
| `EXACT RECEIVE-TIME` | Recorded receive order and intervals | Historical baseline |
| `ACCELERATED` | Same order and relative timing under faster ReplayClock | Historical baseline |
| `COUNTERFACTUAL LATENCY` | Historical market events; versioned own-path timing changes | Own fills/inventory counterfactual |
| `INTERACTIVE` | Versioned branch clock/order policy | Simulator may change market response |

These Replay modes are separate from RunMode and Simulator fidelity. Claims must name all three where material.

## 18. receive-time correctness

Exchange/EventTime supports market chronology research. ReceiveTime answers what the bot knew. `EXACT RECEIVE-TIME` therefore schedules by the recorded local observation order and reproduces timer events under ReplayClock. Late exchange events remain late; they are not moved backward because their exchange timestamp is older.

## 19. no lookahead

At replay time T, no event with receive time later than T may influence state, features, model input, decisions, fills or timers. Preloading for I/O is allowed only behind an isolation boundary inaccessible to decision code. Tests inject future information and assert no earlier DecisionTrace change.

## 20. determinism

Equal ordered events, ResolvedConfig, artifacts, formula version and seed yield identical DecisionTrace and hash. The canonical coordinator commits state in total order. Collection serialization is canonical; thread completion, wall clock, random hash-map order and hidden global state cannot affect results. A divergence report identifies the first event/transition/hash mismatch.

## 21. ReplayClock/RNG

Core obtains now/timers from `ReplayClock` and randomness from seeded `RngProvider`. Acceleration changes wall-clock execution speed, not domain intervals. Counterfactual timing policies and seeds are versioned. Live nondeterministic outputs that matter to later audit are recorded.

## 22. Golden datasets

GoldenDatasets are small, permanent, checksum-verified and diverse: normal, volatile, thin, opportunity-rich, empty, partial/failure-like and incident periods. Tests cover RAW→normalize equality, book reconstruction, exact decisions/rejects/intents/final state, DecisionTrace hash equality, Rust/Python parity and checkpoint-assisted replay equivalence.

## 23. Shadow/Micro-live evidence recording

Shadow records would-trade, would-size, would-submit, snapshots, model/risk output and the subsequent observed market without changing actual account state. Micro-live records predicted versus actual fill, slippage, latency, PnL and recovery at each validated size. Challenger output is recorded but cannot alter decisions before promotion.

## 24. incident reconstruction

An incident bundle resolves RunManifest, ResolvedConfig, image/build, schemas/models/formulas, DecisionTrace, journal, fills/orders/fees, canonical state versions, latency/infra records, alerts/logs, and pinned RAW windows. Reconstruction answers what was received, in which order, why it was allowed/rejected, what was intended, what the exchange did and the resulting PnL.

## 25. validation/DoD

Recorder DoD measures throughput, compression, drops, backlog and disk; proves slow disk does not materially affect hot-path latency; proves saturation preserves execution/account first; verifies every closed checksum; and proves RAW→normalize→replay reconstructs the same normalized stream. Replay DoD proves identical DecisionTrace/hash for identical dataset/config/model/seed, explicit no-lookahead and receive-time tests, and versioned counterfactual assumptions.

## 26. open/calibrated decisions

Still calibrated/open: binary RAW codec; chunk duration; batching; queue capacities; disk thresholds; archive provider; exact local/archive days; trade/incident window lengths; checkpoint interval; checksum algorithm; partition sizing; cross-recorder merge policy; and current Hyperliquid timestamp/sequence guarantees. None is silently fixed by an example in an exploratory source.

## 27. deep-spec links

- [Recorder/Replay deep specifications](deep-specs/recorder-replay/README.md)
- [Recorder Priority and Backpressure Matrix](_analysis/pass06_data_recorder_replay/RECORDER_PRIORITY_AND_BACKPRESSURE_MATRIX.md)
- [Retention and Storage Matrix](_analysis/pass06_data_recorder_replay/RETENTION_AND_STORAGE_MATRIX.md)
- [Replay Mode Matrix](_analysis/pass06_data_recorder_replay/REPLAY_MODE_MATRIX.md)
- [Replay Determinism Contract](_analysis/pass06_data_recorder_replay/REPLAY_DETERMINISM_CONTRACT.md)
- [Data Contracts](11_DATA_CONTRACTS.md)
