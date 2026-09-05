# Checkpoints, Persistence, Compatibility and Migration

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Persistence classes

Economic state, journal, Recorder manifests, configs and artifacts survive container replacement. Route lookup caches and temporary feature buffers may be rebuilt. Physical separation between raw, normalized, state, journal, models and logs protects lifecycle and recovery responsibilities.

## Checkpoint contract

A checkpoint identifies its schema version, run/context, canonical state versions, last covered event/journal cursor, creation time and integrity hash. It may contain AccountState, InventoryState, ReservationState and execution summaries. Exact interval is calibrated.

Restart is `compatible checkpoint + subsequent journal + exchange reconciliation`. The exchange is authoritative for present external facts; journal provides intent/history; checkpoint provides an acceleration baseline. None alone is sufficient.

## Compatibility and migration

Startup validates schema, checksum and cursor continuity. A compatible checkpoint is loaded then replayed forward. An incompatible one is rejected, explicitly migrated with tested version-to-version tooling, or bypassed for a full evidence rebuild. Silent field defaults, state discard and READY-before-reconciliation are forbidden.

## Replay equivalence

For the same terminal cursor, full replay from origin and checkpoint-assisted replay must produce the same canonical state and DecisionTrace suffix/hash. Corrupt checkpoint, missing journal range, duplicate event and exchange mismatch tests must fail closed and enter reconciliation/rebuild rather than READY.
