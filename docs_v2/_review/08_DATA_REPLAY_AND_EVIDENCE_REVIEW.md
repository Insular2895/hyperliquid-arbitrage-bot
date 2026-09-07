# Data, Replay and Evidence Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Truth layers

| Layer | Content | Authority |
|---|---|---|
| L0 | immutable RAW external payload plus receive provenance | audit/reparse source |
| L1 | normalized typed market/account/control events | schema and ordering contract |
| L2 | canonical Book/Account/Inventory/etc. state | ordered reducer output |
| L3 | derived features, forecasts, simulations | versioned artifact output |
| L4 | decisions, effects, observed outcomes, accounting | evidence and operational truth |

Critical execution/account/fill and incident evidence outranks general market data and derived diagnostics under backpressure. Recorder loss or degradation is explicit data-quality/Risk evidence; the Recorder must not synchronously block the trading hot path.

## Determinism contract

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig, ModelArtifacts, FormulaVersion, Seed)
```

For the same ordered inputs and compatible schema, this relation must reproduce the same decisions and hash. It requires explicit wall/monotonic/exchange/Replay clocks, explicit RNG and seed, canonical ordering/serialization, point-in-time config/rules/models, manifest hashes and rejection of hidden time, hidden randomness or future data.

Replay reconstructs recorded history through the same Core. The Simulator instead produces counterfactual distributions under declared assumptions. Replay does not prove what an unobserved alternate action would have caused; simulation does not overwrite recorded truth.

## Evidence chain

`RawEvent → DatasetId/RawChunkManifest → RunManifest → DecisionTrace → Replay/Shadow/MicroLive report → ValidationReport → CapabilityManifest`.

A `CapabilityManifest` must pin exact market, route, strategy mode, size band, code/config/schema/formula/model versions, evidence references and expiry/demotion conditions. Changed semantics invalidate dependent evidence; a new reviewed version and rerun are required.

Evidence maturity is M0 specified, M1 component correct, M2 integrated deterministic Replay, M3 sustained live-input Shadow, M4 bounded real-effect evidence and M5 scoped/reversible validated capability. None is a global “bot safe” certificate.
