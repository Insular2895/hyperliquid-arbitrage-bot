# Recorder Architecture and Hot-path Isolation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Recorder observes adapter/account events and Core decisions through bounded non-blocking capture paths. It owns serialization, compression, chunk lifecycle, disk writes, archive handoff and completeness metrics. Core owns economic order and state; Recorder cannot delay or reorder it.

Forbidden in the hot path: file write, fsync, compression, remote upload, archive wait and unbounded queue wait. A slow-disk fault test compares hot-path latency with normal storage and asserts the documented budget. Cloud/archive failure only creates a retry backlog until local capacity policy escalates.

Recorder health includes process state, queue depth/age, enqueue loss, write latency, bytes/events rates, chunk close latency, disk free, checksum failures and upload backlog. It enters EngineInput as `RecorderHealth`; safety policy is owned by Risk/Operations.

Critical journal/evidence may use an independent durable path, but it must also avoid unbounded blocking and expose inability to preserve P0. The specification does not claim trading can continue indefinitely without critical audit data.

Acceptance requires fault injection for slow/full/corrupt disk, queue saturation, Recorder crash/restart, cloud outage and process shutdown. Each failure produces explicit quality/health state and preserves P0 before lower classes.
