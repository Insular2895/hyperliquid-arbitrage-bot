# Data / Recorder / Replay Validation Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Validation | Evidence/assertion | Maturity owner |
|---|---|---|
| RawEvent encode/decode | Exact field/value/payload-byte roundtrip | Data M1 |
| RAW append-only | Closed bytes/manifests never mutate; correction creates new normalization | Recorder M1 |
| Schema compatibility | Additive accepted only when declared; breaking rejected/migrated | Data M1/M2 |
| Invalid field | Missing required/impossible values never mutate state | Normalizer M1 |
| Real payload corpus | Normal, edge, unknown and historical fixtures | Adapter/Normalizer M1 |
| Parser fuzz | Corrupt bytes cannot panic/produce undefined state | Normalizer M1 |
| Normalizer determinism | Same RAW/schema → same NormalizedEvent | Normalizer M2 |
| RAW→normalize→replay | Reconstruct identical normalized stream | Recorder/Replay M2 |
| Chunk integrity | Count, sequence range, manifest and checksum verify | Recorder M1/M2 |
| Recorder sequence monotonic | Every appended event has `seq(n+1) > seq(n)` per Recorder | Recorder M1/M2 |
| Chunk crash recovery | Truncated/open chunk cannot masquerade as closed | Recorder M1 |
| Nonblocking slow disk | Storage slowdown stays outside documented hot-path budget | Recorder M1/M3 |
| Backpressure priority | P0/P1 preserved before P2/P3; all loss counted | Recorder M1/M3 |
| Dataset quality | Gaps/clock/missing market produce explicit invalid/low region | Data M2 |
| Book reconstruction | Snapshot+diffs yield reference book or invalid state on gap | Book M2 |
| Dedup/idempotence | Duplicate fill/order/journal event applies once | State/Execution M1/M2 |
| Event ID dedupe | Duplicate stable event identity does not double-apply state | Data/Core M1 |
| Reducer properties | Same ordered stream → same versions/state | Core M1/M2 |
| No Lookahead | Injected future event cannot affect earlier trace | Replay M2 |
| Receive-time order | Late exchange-time event stays at receive position | Replay M2 |
| Equal-time total order | Source priority/Recorder tie-break is stable | Core/Replay M2 |
| Replay repeat hash | Same dataset/config/model/seed → same DecisionTrace hash | Replay M2 |
| Multi-thread determinism | Worker scheduling does not change committed trace | Core M2/load |
| StateHash divergence | First divergent event sequence is identified | Replay M2 |
| Clock abstraction | Live/Replay/Test clocks drive timers consistently | Clock M1/M2 |
| RNG determinism | Seed/version produces same recorded draws/results | Replay/Simulator M2 |
| Golden replay | Exact opportunities/rejects/intents/final state/PnL tolerance | System M2 |
| Point-in-time audit | All artifacts were available at historical T | Research M2 |
| Temporal isolation | training_end < validation_start; no future leakage | Model validation |
| Checkpoint equivalence | Full replay N == checkpoint K + suffix to N | State/Replay M2 |
| Incompatible checkpoint | No READY; explicit migration/rebuild/reconcile | State M1/M2 |
| Journal crash matrix | Intent/send/fill/cancel/recovery crashes reconstruct safely | Execution M2 |
| Incident reconstruction | Fill/incident resolves complete evidence and original trace | Operations M3/M4 |
| Shadow account isolation | Actual and counterfactual balances never mix | Shadow M3 |
| Predicted vs actual | Fill/slippage/latency/PnL/recovery joins are complete | MicroLive M4 |
| Retention restore drill | Permanent/pinned evidence restores with checksums/lineage | Operations M3/M4 |
| Unknown optional field | Ignored only when declared compatible; roundtrip remains valid | Schema M1 |
| Required-field strictness | Missing field rejected with zero state mutation | Schema M1 |
| Schema startup incompatibility | Bad model disables dependency; config fails boot; state blocks READY | System M1/M2 |

Recorder DoD metrics are throughput, compression, dropped events, backlog and disk usage. Replay DoD is identical trace/hash for identical dataset/config/model/seed, explicit receive-time and No-Lookahead tests, and versioned counterfactual assumptions. Release remains blocked by replay nondeterminism.
