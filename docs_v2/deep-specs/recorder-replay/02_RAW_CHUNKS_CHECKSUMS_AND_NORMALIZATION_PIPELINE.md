# RAW Chunks, Checksums and Normalization Pipeline

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

RAW stores exact payload bytes and the full RawEvent envelope. It is written locally in compact binary chunks and compressed with ZSTD. The exact codec and nominal 5–15 minute exploratory chunk range remain implementation/calibration choices; boundaries must be independently recoverable and measured under real event volume.

Each closed `RawChunkManifest` records file ID, start/end time, event count, cryptographic checksum, compressed size and schema version. Operational metadata additionally tracks first/last Recorder sequence, archive state, quality flags and retention class. A reader verifies checksum, manifest/schema and sequence continuity before use.

Normalization is a separately versioned deterministic transform:

```text
checksummed RAW → parser/normalizer version → NormalizedEvent tables
→ Parquet + ZSTD analytics partitions → derived datasets
```

New normalizer logic produces a new normalized dataset; RAW never changes. Unknown source types stay available for later re-normalization. Partitioning by date/hour/market is the canonical direction, subject to file-size/query benchmarks.

Roundtrip acceptance compares the normalized stream produced during capture with one regenerated from stored RAW for the same schema version. Count, order, identities and canonical payloads must match; any excluded invalid event has an explicit reason record.
