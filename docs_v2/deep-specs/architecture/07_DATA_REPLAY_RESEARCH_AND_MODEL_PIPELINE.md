# 07 — Data, Replay, Research and Model Pipeline

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

L0 RAW preserves received payload bytes and provenance. L1 contains typed normalized events. L2 contains canonical state. L3 contains derived features/forecasts. L4 contains decisions/results. No later layer replaces L0 evidence.

Recorder consumes the same ordered event stream asynchronously with P0 execution/account/fill evidence first, then incident windows, general market events and derived diagnostics. Execution Journal and checkpoints support restart; checkpoints are compatible acceleration artifacts, never exchange truth.

Replay selects RAW, point-in-time metadata/config/models/formulas and feeds normalized ordered events to the same reducers/Core under `ReplayClock` and explicit RNG seed. It produces a `DecisionTrace`; no later artifact or event can leak into Historical Truth.

```text
evidence → valid point-in-time dataset → Python research/training
→ candidate artifact → temporal OOS/walk-forward validation
→ Challenger → explicit promotion → immutable ModelArtifact/manifest
→ bounded Rust inference → predicted-versus-actual joins
→ drift/OOD/calibration → hold/fallback/demotion/retrain
```

The model feedback loop is asynchronous and version-bounded. A runtime never consumes a newly trained model until Model and Capability owners atomically promote exact scope.
