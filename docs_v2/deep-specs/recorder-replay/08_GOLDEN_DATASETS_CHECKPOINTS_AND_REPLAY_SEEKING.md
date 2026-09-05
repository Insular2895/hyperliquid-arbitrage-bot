# Golden Datasets, Checkpoints and Replay Seeking

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

GoldenDatasets are small, permanent, versioned and checksummed. The corpus covers normal, volatile, thin, opportunity-rich, empty, gap, book anomaly, partial/cancel race, recovery, reconnect and incident periods. Each fixture specifies input manifests, expected normalized stream, final books/state, decisions/rejects/intents and economically tolerated PnL.

Checkpoint seeking loads a compatible checkpoint at or before the target, verifies integrity/cursors, then replays every journal/input event after its covered sequence. It cannot expose future data to the engine. The exact checkpoint interval and materialized contents are calibrated by seek performance, storage and recovery needs.

Required equivalence test:

```text
full replay from origin to N
== checkpoint at K + ordered replay K+1..N
```

Equality covers canonical state versions/contents and trace suffix/hash. A missing range, corrupt checksum, incompatible schema or ambiguous cursor invalidates the checkpoint path. The engine falls back to earlier evidence/rebuild and reconciliation; it does not guess.

Golden replay also proves RAW→normalize roundtrip, Rust/Python schema parity, No Lookahead and repeated-run hash identity.
