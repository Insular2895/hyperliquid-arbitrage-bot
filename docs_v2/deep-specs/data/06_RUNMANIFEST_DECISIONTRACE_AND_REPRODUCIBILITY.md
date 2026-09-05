# RunManifest, DecisionTrace and Reproducibility

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Run identity

The closure `RunManifest` fields are `run_id`, `mode`, `git_commit`, `build_hash`, `config_hash`, optional `dataset_id`, `model_versions`, `formula_schema_version`, `event_schema_version`, `start_time`, and optional `random_seed`. Deployment/image digest and language dependency locks are linked when required to reproduce the binary or research environment.

`mode` is one of `Replay`, `Paper`, `Shadow`, `MicroLive`, `Live`. It cannot switch strategy math, formulas, gates or state machines. Differences live at explicit source, transport, effect or feature-flag/config boundaries.

## Trace identity

`DecisionTrace` contains `ordered_decisions[]`, `order_intents[]`, `state_transitions[]`, and `risk_decisions[]`. IDs connect it to exact source events, immutable snapshots, models, formula/config versions, plans, exchange outcomes and PnL.

```text
DecisionTrace = F(OrderedEvents, ResolvedConfig,
                  ModelArtifacts, FormulaVersion, Seed)
```

Equal inputs produce byte/canonical-equivalent trace and hash. StateHash checkpoints allow the first divergent event/transition to be located.

## Reproducible evidence

Every experiment saves a manifest and result containing run_id/dataset_id/strategy/config and metrics. No material conclusion exists only in a notebook cell. A reproducibility test resolves every referenced artifact, replays twice and compares ordered events, transitions, decisions, intents, final state and PnL under declared numeric tolerances.

**No notebook-only result** may support a validation or promotion decision.
