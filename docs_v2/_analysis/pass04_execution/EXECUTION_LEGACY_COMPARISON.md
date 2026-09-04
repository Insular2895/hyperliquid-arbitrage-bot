# PASS 04 — Execution Legacy Comparison

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

Compared only after V2 reconstruction: `docs/10_EXECUTION_STATE_MACHINE.md`, `09_RISK_CONSTITUTION.md`, `12_RECORDER_AND_REPLAY.md`, `14_DEPLOYMENT_AND_DOCKER.md`, `16_VALIDATION_MATRIX.md`, and relevant `docs/specs/` execution/recovery/reconciliation/reservation/transport/nonce/signer/replay/inventory files.

| Legacy area | Classification | PASS 04 result |
|---|---|---|
| five machines and exact state names | `RECOVERED` but previously compressed | authoritative inventory + full transition matrices |
| Strategy/effect boundary and single writer | `RECOVERED` | architecture deep spec with version/stale-worker boundary |
| OrderIntent/CLOID/no-blind-retry | `OVER_COMPRESSED` | exact SRC-005 fields, identity chain, lost-response protocol |
| nonce/signing | `OVER_COMPRESSED` | owner per signer/process and external-fact boundary; no invented current rule |
| reservations/available capacity | `OVER_COMPRESSED` | three classes, lifecycle table, unknown/cancel locks |
| zero/full/partial by every TT/TTT leg | `MISSING` in sufficient depth | explicit per-leg and failure branches recovered |
| maker MT/MTT partial and cancel-after-partial | `MISSING` in sufficient depth | immediate exposure, buffer/hedge/recovery logic recovered |
| dust/`DUST_EXPOSURE`/`PendingIntermediateBuffer` | `MISSING` | exceptional-detail deep spec and compatibility rules recovered |
| cancel race/finality | `OVER_COMPRESSED` | event interleavings and reservation consequences recovered |
| Recovery objective/splits/sunk cost | `OVER_COMPRESSED` | full RecoveryState and QF-079/080 semantics recovered |
| Reconciliation algorithm/balance diff | `OVER_COMPRESSED` | orders->fills->balances proof and `UNRESOLVED` semantics recovered |
| crash points/journal boundary | `OVER_COMPRESSED` | crash matrix, async persistence, checkpoint+journal+exchange recovered |
| feed disconnect/reconnect/DMS | `MISSING` or scattered | unified safety sequence; current facts external |
| TT/MT/TTT/MTT/TM/MM enablement distinction | `MISSING` | mode matrix; TM/MM supported-disabled |
| same Replay/Shadow/Micro-live/Live reducer | `RECOVERED` | exact RunMode/effect boundary and parity tests |
| generic Python asyncio/uvloop implementation | `SUPERSEDED` | Rust/Tokio production direction; async I/O principle retained |
| fixed universal latency/timeouts | `REJECTED` | calibrated distributions/timers only |
| Risk thresholds/data schemas/formulas/monitoring backend | `ROUTED_TO_FUTURE_PASS` | PASS 05/06/10/11 owners retained |

## Legacy-untraced audit

No legacy-only execution invariant was promoted without original-source provenance. Legacy implementation details that are not traceable remain non-authoritative. `docs/**` was not edited.
