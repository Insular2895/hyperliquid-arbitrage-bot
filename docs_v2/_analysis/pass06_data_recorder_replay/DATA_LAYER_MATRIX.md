# Data Layer Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Layer | Inputs | Canonical outputs | Owner | Rebuildability | Forbidden substitution |
|---|---|---|---|---|---|
| L0 RAW | Source bytes at local receipt | RawEvent + chunk manifest | Recorder | Original evidence; not regenerated | Normalized/derived/log data cannot replace it |
| L1 NORMALIZED EVENTS | L0 + schema/normalizer version | Typed EngineInputEvents | Adapters/Normalizer | Deterministically regenerable from L0 | Parser guesses, mutable state, invented source fields |
| L2 STATE | Total ordered L1 events | Versioned canonical states | Single logical state owner | Replay from event/journal evidence | Checkpoint/exchange/worker as unqualified sole truth |
| L3 DERIVED FEATURES | Immutable L2 snapshots | Features, forecasts, economics | Quant/Models/Simulator | Recomputable with artifacts/formulas | Sole historical source; hidden notebook transform |
| L4 DECISIONS / RESULTS | L2/L3 + config/risk/execution | Opportunities, decisions, intents, outcomes/PnL | Ordered coordinator and owning modules | Reproducible through DecisionTrace | Intent as fact; expected state over exchange truth |

Boundary invariants:

- L0 is append-only, immutable, timestamped and versioned.
- Every L1 event points to source RAW; every L2 mutation points to its trigger event.
- L3 identifies inputs and schema/model/formula versions.
- L4 separates Opportunity, authorization, command/effect, observed event and result.
- No important decision lacks provenance, version, time and source.

## Major-object placement and lifecycle

| Object/family | L0 | L1 | L2 | L3 | L4 | Source truth? | Immutable? | Reconstructable? | Persisted / retention | Versioned? | Replay input? | Derived from | Consumers |
|---|:---:|:---:|:---:|:---:|:---:|---|---|---|---|---|---|---|---|
| RawEvent/payload | ✓ | | | | | Receipt evidence | Yes | No | RAW / SHORT→holds | Yes | Yes | External payload | Normalizer, audit |
| RawChunkManifest | ✓ | | | | | Integrity evidence | Yes after close | Re-indexable only with proof | Manifest / LONG | Yes | Yes | RAW chunk | Replay, archive |
| MarketEvent | | ✓ | | | | Typed event truth | Yes | From RAW | Normalized / MEDIUM-LONG | Yes | Yes | RawEvent | Book, Strategy |
| AccountEvent | | ✓ | | | | Observed account event | Yes | From RAW/journal/source | P0 / PERMANENT | Yes | Yes | Raw/account source | Account, Execution |
| Infra/Timer/Control | | ✓ | | | | Run input evidence | Yes | From structured source/policy | LONG/PERMANENT by materiality | Yes | Yes | Clock/infra/control | Core, Risk |
| BookState | | | ✓ | | | Run-canonical projection | Snapshot yes | From ordered market events | Checkpoint optional | Version | State input | MarketEvents | Features, Risk |
| AccountState | | | ✓ | | | Run-canonical projection; exchange reconciles current fact | Snapshot yes | Events+journal+exchange | Checkpoint + P0 evidence | Version | State input | AccountEvents | Risk, Execution |
| InventoryState | | | ✓ | | | Run-canonical projection | Snapshot yes | Fills/balances | Checkpoint + permanent deltas | Version | State input | Actual fills | Risk, Portfolio |
| ReservationState | | | ✓ | | | Run-canonical projection | Snapshot yes | Journal/events | Checkpoint + journal | Version | State input | Plans/effects/events | Risk, Execution |
| ExecutionState | | | ✓ | | | Run-canonical projection | Snapshot yes | Journal+exchange | Journal / PERMANENT | Version | State input | Execution events | Recovery, Risk |
| FeatureSnapshot | | | | ✓ | | No; recomputable | Yes | From exact state/artifacts | LONG by research value | Feature schema | Input to decisions | State snapshot | Models, Strategy |
| ModelForecast | | | | ✓ | | No; artifact output | Yes | From feature+model | LONG/PERMANENT evidence | Model version | Yes | FeatureSnapshot | Simulator, Risk |
| Opportunity | | | | | ✓ | Decision candidate | Yes | From state/features/formulas | LONG/PERMANENT | IDs/versions | Expected output | L2/L3 | Simulator, Risk |
| ExecutionForecast | | | | ✓ | ✓ | No; scenario output | Yes | From candidate/state/models/seed | LONG/PERMANENT evidence | Simulation version | Expected output | L2/L3 | Risk, Sizing |
| RiskDecision | | | | | ✓ | Authorization record | Yes | From RiskSnapshot/config | PERMANENT | Snapshot/config | Expected output | L2/L3 | Execution, audit |
| ExecutionPlan/Intent | | | | | ✓ | Intent, not exchange fact | Yes after boundary | From allowed decision | PERMANENT | Plan/risk/config | Expected output | RiskDecision | Transport, journal |
| OrderUpdate/Fill | | ✓ | | | ✓ | Exchange/account evidence | Yes | Source/journal recovery | P0 / PERMANENT | IDs/schema | Yes | Exchange/ReplayTransport | State, PnL |
| DecisionTrace | | | | | ✓ | Run audit output | Yes | From complete run inputs | PERMANENT validation | RunManifest | Expected output | L1–L4 chain | Replay, Validation |
| Checkpoint | | | ✓ | | | No | Yes once closed | From earlier events | State / MEDIUM-LONG | Checkpoint schema | Seek aid only | L2 at cursor | Restart, Replay |
| ExperimentResult | | | | | ✓ | Research evidence | Yes | From RunManifest/run | PERMANENT if decision-bearing | Dataset/run versions | Output | DecisionTrace/metrics | Validation |
