# 03 — State Ownership, Events, Commands and Effects

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Single-writer rule

Every critical state family has one logical writer coordinated in deterministic input order. Parallel workers compute proposals against immutable versions; the coordinator discards or revalidates stale output before commit. A database, checkpoint or domain-local cache is not concurrent truth.

## Interaction model

```text
Command/Intent → deterministic validation/reducer → state + EffectRequest
EffectRequest → EffectExecutor/adapter → external system
External observation → Event → ordered reducer → canonical state
```

Submitting is not accepting; accepting is not filling; requesting cancel is not cancel confirmation. A timeout after possible transmission becomes `UNKNOWN`, preserves reservations and invokes query/reconciliation. Adapters and transports may validate and translate but never mutate Book, Inventory, Risk or Execution directly.

## Snapshot contract

Every decision-relevant snapshot carries its family version plus relevant event, config, model, formula, capability and infrastructure identities. Plans pin the versions they consumed. Material change invalidates authorization rather than silently changing the meaning of an existing plan.

## Persistence and Replay

RAW, journal and compatible checkpoints reconstruct states through the same reducers. Checkpoints accelerate; exchange truth plus ordered events decide. Replay must reproduce commit order independently of worker scheduling. See [State Ownership Matrix](../../_analysis/pass13_master_architecture/STATE_OWNERSHIP_MATRIX.md) and [Event/Command Ownership](../../_analysis/pass13_master_architecture/EVENT_AND_COMMAND_OWNERSHIP_MATRIX.md).
