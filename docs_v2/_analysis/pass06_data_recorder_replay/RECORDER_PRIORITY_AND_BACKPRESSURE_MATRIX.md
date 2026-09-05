# Recorder Priority and Backpressure Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Priority | Canonical evidence | Preservation | Saturation action | Replay consequence if lost |
|---|---|---|---|---|
| P0 | fills, account, orders/execution, fees, reservations/reconciliation | First; protected journal path | Escalate critical health before loss; preserve over all lower classes | Execution/account reconstruction invalid |
| P1 | market/infra windows around executions and incidents | Second; pin/upgrade retention | Preserve by shedding P3 then P2 | Incident/calibration fidelity invalid/low |
| P2 | general market events | Third | Explicit drop/sample/degrade after P3 | Mark scoped gap/quality region |
| P3 | derived diagnostics | Last | Stop/recompute/degrade first | Recompute from lower layers if lineage complete |

SRC-005 is closure authority. SRC-003's exploratory P2-derived/P3-general-RAW order is `SUPERSEDED`.

Minimum observability: `events_received`, `events_written`, `events_dropped`, `sequence_gaps`, split by priority/source/type; queue depth/age; write latency; disk free; chunk/checksum failures; upload backlog. No drop or quality downgrade is silent.

Backpressure is bounded and non-blocking from Core. Storage priority does not become event-processing priority and cannot corrupt economic order. If critical P0 preservation cannot be guaranteed, RecorderHealth becomes critical and the owning Risk/Operations policy controls new-risk behavior.

## Per-family policy

| Data family | Priority | Can drop? | Can degrade? | Alert? | Long-term retention | Replay critical? | Recovery critical? | Reason/source |
|---|---|---|---|---|---|---|---|---|
| Fills | P0 | No intentional loss | No | Critical | Permanent | Yes | Yes | SRC-005 §124/129/238 |
| Orders/order updates | P0 | No intentional loss | No | Critical | Permanent | Yes | Yes | SRC-005 §124/129/238 |
| Balances/account snapshots | P0 | No intentional loss | No | Critical | Permanent/current snapshots | Yes | Yes | SRC-005 §124/129 |
| Execution events/journal | P0 | No intentional loss | No | Critical | Permanent | Yes | Yes | SRC-005 §124/130–132/238 |
| Risk decisions | P0 | No intentional loss | No | Critical if unavailable | Permanent | Yes | Yes for permission audit | SRC-005 §238/253–254 |
| Execution market windows | P1 | No while pinned | Scope/length only by explicit policy | High | Long/permanent hold | Yes | Yes | SRC-005 §124/240 |
| Incident market windows | P1 | No while pinned | Scope/length only by explicit policy | High | Long/permanent hold | Yes | Yes | SRC-005 §124/242 |
| General market RAW | P2 | Yes only explicitly under pressure | Sample/drop/shorten | Warning/high | Short/calibrated | Yes for claimed exact region | Contextual | SRC-005 §124/239 |
| Derived diagnostics | P3 | Yes first | Stop/recompute | Warning | Long if useful | No if lower lineage complete | No | SRC-005 §124 |
| Analytics exports | P3 | Yes first | Delay/rebuild | Warning | Calibrated | No | No | Derived/supporting evidence |
