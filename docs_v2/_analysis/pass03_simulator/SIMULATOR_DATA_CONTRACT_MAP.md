# PASS 03 — Simulator Data Contract Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

PASS 03 maps semantic contracts only. PASS 06 owns exact fields, types, units, serialization, compatibility, and migrations. Names below follow SRC-005.

| Contract | Producer/authority | Simulator use | Required invariant / provenance |
|---|---|---|---|
| `RunMode` | Runtime/Data | Replay/Paper/Shadow/MicroLive/Live environment | Cannot silently alter strategy logic or formulas. |
| `SimulationMode` | Data/Simulator | `ExogenousReplay` vs `InteractiveCounterfactual` | Explicit in every result; modes not mixed silently. |
| `ReplayFidelity` | Data/Validation | `F0Historical`…`F4Interactive` | Explicit capability/limitation label. |
| `ExogenousReplay` | Data | Historical future unchanged; own fills/inventory simulated | No market-feedback claim. |
| `InteractiveCounterfactual` | Data/Simulator | Baseline + mechanical + participant response | Calibrated scenarios, never exact alternate reality. |
| `BranchId` / `MonteCarloPathId` | Simulator/Data | Identify branch and seeded path | Linked to run, seed, inputs/models. |
| `CounterfactualRejoinEvent` | Simulator/Data | Explicit return to compatible baseline | No silent snap; reason/horizon/compatibility trace deferred to PASS 06. |
| `ConfidenceState` | Models/Simulator | decomposed confidence | level, data fidelity, freshness, support, OOD, disagreement, latency uncertainty semantics retained. |
| `ExecutionForecast` | Simulator | consolidated output to Risk | plan candidate; full/partial/recovery/failure, PnL/quantiles/P+, ES, fees/slippage, confidence, simulator version. |
| `EdgeSurvivalForecast` | Participant | arrival survival/edge scenarios | version, input lineage, support/horizon/confidence. |
| `LiquidityForecast` | Participant | arrival depth/replenishment/spread scenarios | Mechanical consumption excluded; confidence/support explicit. |
| `MakerForecast` | Participant | fill/time/partial/adverse input | Queue observability/fidelity must not be hidden. |
| `CrossMarketForecast` / `ResponseForecast` | Participant | sparse target response distributions | source/target/horizon/model/confidence; association not false identity/causality. |
| `LatencyTrace` | Infrastructure/runtime | measured latency distribution and calibration | receive/compute/sign/send/ack/fill lineage, infra instance, run. |
| `TimerEvent` | Clock/runtime | expiry, Risk recheck, recovery/reconciliation timing | Recorded and replayed, no hidden wall-clock effects. |
| `GoldenDataset` | Data/Validation | deterministic fixture | exact expected opportunities/rejects/intents/PnL/hash. |
| `DecisionTrace` | Core | deterministic replay output | ordered decisions/intents/transitions/Risk decisions. |
| `RunManifest` | Runtime/Data | top-level provenance | run/mode/build/config/dataset/models/formula/schema/start/seed. |
| `ModelArtifact` / `ModelVersion` | Model registry | exact response/queue/survival model | training range, feature schema, point-in-time availability, support, approval role. |
| RNG seed / `RngProvider` | RunManifest/runtime | reproduce stochastic sample paths | Same inputs/artifacts/seed → same contractual paths. |
| State hashes / snapshot versions | State/core | compare runs/checkpoints, reject stale work | immutable input state; mismatch invalidates/revalidates. |
| `EngineInputEvent` | Data/core | Market/Account/Infra/Timer/Control union | deterministic explicit ordering. |
| `OrderIntent`, `OrderEvents`, `FillEvents` | Execution/Data | same emulator/live interface | Core cannot distinguish origin from schema. |
| `ActualAccountState` / `ShadowCounterfactualState` | Account/Simulator | separate real and hypothetical truth | Never commingle balances/inventory. |

## Reproduction minimum

A reproducible run needs ordered event/input identity, event-time and receive-time semantics, resolved config/hash, exact dataset/invalid-region policy, model artifacts/versions/training ranges, Formula version, fee/precision/rule versions, all three mode/fidelity axes, seed/stream, timers, build/git/schema versions, initial/checkpoint state hashes, branch/path/rejoin events, and the final `DecisionTrace`/forecast hash.

## Concurrency boundary

Parallel Simulator/model workers consume immutable versioned snapshots and return `input_state_version` plus validity/TTL. Results against materially changed state are discarded or revalidated. Only the ordered coordinator commits economic state transitions.
