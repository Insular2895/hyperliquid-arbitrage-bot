# 04 — Replay Determinism and No-Lookahead Validation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Determinism identity

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig,
                  ModelArtifacts, FormulaVersion, Seed)
```

Run twice and compare canonical ordered events, state transitions, Risk decisions, order intents, final state/PnL and trace hash. StateHash checkpoints locate first divergence. Worker completion order, host wall time, implicit RNG, unordered maps or hidden external reads cannot affect Core commits.

## Point-in-time audit

For each decision T resolve only events, metadata/fees, configs, features, formula/schema and model artifacts available by T. Verify dataset filters and model training/availability boundaries; `training_end < validation_start`. Later artifacts require an explicitly counterfactual manifest and cannot rewrite the historical trace.

## Fidelity and failures

Replay uses the same reducers and typed Order/Fill events as Live through an emulator. It includes zero/partial/full/reject/cancel, timing, UNKNOWN, Recovery, crash/restart/reconciliation and invalid-data paths. Exact accelerated/checkpoint Replay must match full exact Replay. Stochastic Simulator paths are repeatable under stored seeds but remain distributional claims.
