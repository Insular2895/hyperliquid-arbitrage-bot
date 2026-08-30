# Recorder

## Purpose

Créer une preuve append-only complète sans bloquer le hot path.
## Responsibilities

Priority queues, chunks/manifests/checksums, gaps, retention tags and upload handoff.
## Non-responsibilities

Ne transforme pas RAW et n'écrit pas cloud synchronously.
## Inputs

Raw/normalized/domain/health events.
## Outputs

Durable chunks/manifests and RecorderHealth.
## Dependencies

ClockAndRng, Deployment storage.
## State

Bounded queues, open chunk, sequence, upload/retention status.
## Algorithms / formulas

Append/rotate/checksum/verify; P0→P3 degradation order.
## Invariants

P0 protected; loss/backpressure explicit; closed chunks immutable.
## Failure modes

Disk full/slow, queue overflow, corruption, crash, archive outage.
## Risk interactions

Threat to account/audit data disables new risk; lower priorities may degrade.
## Performance requirements

Nonblocking producer; sustained rate and crash-safe writes.
## Metrics

Bytes/events/rates, queue/drop by priority, write/upload/backlog/disk.
## Persistence

Is the persistence boundary; manifests/checksums/schema versions.
## Configuration

Chunk/retention/watermarks/upload calibrated.
## Tests

Crash/corruption/disk/full/backpressure/restore/checksum/load.
## Maturity requirement

M1 early; soak before M3; prod retention M4.
## Open calibrated parameters

Chunk sizes, queues, watermarks and retention.
