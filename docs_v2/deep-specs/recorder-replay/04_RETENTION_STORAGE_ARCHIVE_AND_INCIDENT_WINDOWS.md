# Retention, Storage, Archive and Incident Windows

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Classes

`PERMANENT`, `LONG`, `MEDIUM`, `SHORT` are semantic lifecycle classes. Exact day counts are calibrated. Permanent evidence includes executions, orders/fills/fees, risk decisions, configs, model/formula versions, incidents, GoldenDatasets and validation records. General market RAW may be SHORT; normalized and derived lifetimes depend on reproducibility value and measured cost.

Every execution/incident pins relevant pre-, active- and post-windows. Window duration is calibrated, not copied from exploratory 5s/10s or 10s/20s examples. A window contains market/account/infra/order/decision evidence sufficient for predicted-versus-actual and Recovery reconstruction.

## Storage roles

Local NVMe is a bounded working buffer for open/recent chunks, journal, state and checkpoints. Durable object storage is provider-neutral archive. Research workstation/iCloud may be a later cold copy but never the direct capture target. Server is not the only archive.

Deletion eligibility requires: chunk closed, checksum valid, upload complete, remote checksum verified, retention class evaluated, no execution/incident/golden hold, and required dependent manifests indexed. Lifecycle actions are auditable. Disk warning/cleanup thresholds and local/archive periods are calibrated from `raw_bytes_per_hour`, compression ratio, free space and backlog.

Archive outage does not enter the hot path. It increases backlog and may reduce lower-priority retention. If protected capacity is threatened, safety policy escalates visibly.
