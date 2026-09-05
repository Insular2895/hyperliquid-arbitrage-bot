# Schema Version Compatibility Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Family/change | Read old? | Write behavior | Startup/replay action |
|---|---|---|---|
| Optional additive field with default-free semantics | Yes when declared | Writer may retain major version | Ignore safely; roundtrip/golden test |
| New event variant unknown to reader | RAW yes; normalized no | New schema version | Record RAW, alert, upgrade normalizer |
| Missing required field | No | Reject/quarantine | No state mutation |
| Field type/unit/meaning change | No implicit | Major version increment | Explicit converter or fail |
| Deprecated field | Yes during window | Preserve/read until migration | Warn/track compatibility |
| Feature schema mismatch | No | New FeatureSchemaVersion | Model-dependent capability disabled |
| Formula/fee/rounding semantic change | No silent | New FormulaSchemaVersion | Pin matching version |
| Model artifact/hash mismatch | No | New ModelVersion/artifact | Reject/disable dependent model |
| Dataset normalization/filter change | Separate dataset | New DatasetId | Distinct experiment/run |
| Config schema/value provenance invalid | No | New validated ResolvedConfig | Boot/config update rejected |
| Compatible checkpoint | Yes | Preserve schema/cursor/hash | Load, replay suffix, reconcile |
| Incompatible checkpoint | Only explicit migration | Versioned migrated output | Rebuild/reconcile; no READY |

Every serialized schema documents exact fields/types/nullability/units. Readers do not invent missing source data. Important state migrations are explicit, tested and versioned; full replay and migrated/checkpoint replay compare canonical results.

## Required family relationships

| Schema family | Depends on / pins | Breaking mismatch action |
|---|---|---|
| Raw schema | Capture envelope, Source enum, payload codec | Reader upgrade; original bytes remain preserved |
| Normalized schema | Raw ID + normalizer/parser version | Re-normalize from RAW or reject dataset |
| Domain event schema | Normalized envelope + typed Market/Account/Infra/Timer/Control variants | Capability disabled/replay rejected until supported |
| Feature schema | Domain state/event schema + formula inputs | Model input rejected |
| Formula schema | Precision/fee/rounding/economic definitions | Distinct run/version; no cross-version equality claim |
| Model schema | Feature schema + artifact/training DatasetId | Dependent strategy disabled |
| Config schema | ResolvedConfig validation/provenance/Risk bounds | Boot/update failure |
| Checkpoint schema | State schemas + last event/journal cursors | Explicit migration or rebuild; no READY |
| Journal schema | Execution/state event variants and identifiers | Replay/reconciliation migration required |
