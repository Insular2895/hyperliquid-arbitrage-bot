# Schema, Model, Formula and Dataset Versioning

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Version families

| Family | Minimum identity | Compatibility gate |
|---|---|---|
| Event/schema | family + schema version | reader understands required fields/types/units |
| Feature | `feature_schema_version` | model input exactly supported |
| Formula | `formula_schema_version` | calculation/fee/rounding semantics pinned |
| Model | id, semantic version, training dataset, feature schema, artifact hash | artifact/hash/schema/support valid |
| Dataset | date ranges, RAW manifests, normalization version, filters | chunks and quality regions resolve |
| Config | resolved version/hash and provenance | constitution bounds and schema valid |
| Checkpoint | checkpoint schema and covered cursor | reader/migration explicitly supports it |

Additive optional changes may be backward compatible. A required-field/type/meaning change is breaking and increments the major version. Permanent fields are deprecated before explicit removal. No live component silently guesses a migration.

## Failure behavior

An incompatible model disables its dependent capability. Invalid configuration fails boot. Incompatible checkpoint/state requires tested migration or rebuild/reconciliation and prevents READY. Unknown exchange types remain RAW-only until a new normalizer/schema exists.

## Cross-language parity

Rust domain types own internal semantics; dataset contracts remain language-neutral and list exact field types, units, nullability and versions. Generated/exported schemas or golden fixtures prove Python/Rust parity. Float and collection serialization used in hashes is canonical.
