# Checkpoint and State Recovery Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Situation | Checkpoint | Journal/events | Exchange reconciliation | Result |
|---|---|---|---|---|
| Clean compatible restart | Verify/load | Replay after covered cursor | Required before READY | Consistent state or investigate |
| No checkpoint | None | Replay full available history | Required | Rebuilt state |
| Corrupt checksum | Reject | Use earlier/full evidence | Required | No silent recovery |
| Incompatible schema | Reject or explicit tested migration | Replay from supported cursor | Required | No READY until consistent |
| Missing journal/input range | Cannot bridge gap | Mark missing region | Required | Rebuild or unresolved; no READY |
| Duplicate suffix events | Load | Idempotent/deduplicated apply | Compare truth | Same final state |
| Exchange disagrees | Baseline only | Preserve local history | Exchange owns current external fact | Reconcile/Recovery/incident |
| Replay seeking | Verify/load | Replay K+1..N with No Lookahead | Simulated truth per run | Must equal full replay to N |

Checkpoint minimum metadata: checkpoint schema, run/context, creation time, integrity hash, canonical state versions and exact last covered event/journal cursors. It can include AccountState, InventoryState, ReservationState and execution summaries. Interval is calibrated.

Acceptance proves full replay to N equals compatible checkpoint K plus ordered suffix K+1..N for canonical state and trace. Checkpoints accelerate computation; they do not override journal order or exchange truth.

## State-family recovery

| State family | Can checkpoint? | Source of truth? | Journal required? | Exchange reconciliation required? | Schema version? | Safe to restore directly? | Migration? | Rebuild method |
|---|---|---|---|---|---|---|---|---|
| BookState | Yes | Ordered valid market events | Market-event suffix | Fresh source snapshot/resync, not account reconciliation | checkpoint + event schema | No; replay/resync required | Explicit | Snapshot + diffs or fresh snapshot |
| AccountState | Yes | Current exchange/account evidence | Account/journal suffix | Yes before READY | checkpoint/account schema | No | Explicit/tested | Checkpoint + journal + exchange |
| InventoryState | Yes | Actual fills/balances under accounting rules | Fill/balance journal | Yes through AccountState | checkpoint/inventory schema | No | Explicit/tested | Reapply fills/fees + reconcile |
| ReservationState | Yes | Execution owner/journal | Reservation/execution journal | Indirectly for unknown commitments | checkpoint/reservation schema | No | Explicit/tested | Replay plan/order/fill/release events |
| ExecutionState | Yes/summaries | ExecutionJournal + exchange truth | Yes | Yes | checkpoint/journal/state-machine schema | No | Explicit/tested | Replay transitions then reconcile |
| GraphState if materialized | Yes as rebuild optimization | Metadata/route definitions/events | Metadata/config events | No account reconciliation | checkpoint/graph/metadata schema | Only after dependency validation | Explicit or rebuild | Recompute graph/routes from metadata/config |
