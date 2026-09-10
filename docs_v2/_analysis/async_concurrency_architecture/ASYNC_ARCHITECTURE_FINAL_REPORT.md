# ASYNC / CONCURRENCY ARCHITECTURE REVIEW COMPLETE

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| Field | Result |
|---|---|
| Baseline commit | `44b1042371ed996dc97f9fae310a1cd36fe370df` |
| Modular monolith | `PRESERVED` — one client/container/main Rust process |
| Massively parallel redesign | `NO` — queue/scheduler/cache overhead and nondeterministic acceptance would add risk without measured need |
| Ordered commit authority | one logical C0 coordinator/domain-owner sequence |
| Functions classified | `97` |
| C0 functions | `29` — canonical ordering/reducers, current decisions, Risk, Reservation, Execution/Recovery/Reconciliation/Accounting commits |
| C1 functions | `22` — decode/normalize, bounded lookup/BBO/FastL1/full-L2 baseline, rolling features, simple models, local signing, minimal evidence markers |
| C2 functions | `9` — Graph/feature/model/F2–F3/q/sizing/portfolio/Recovery pure snapshot proposals |
| C3 functions | `12` — market/account/metadata I/O and submit/cancel/query/reconciliation/admin external effects |
| C4 functions | `16` — Recorder/checkpoint/archive, telemetry, artifacts, Atlas, health/license/release background work |
| C5 functions | `9` — F4/Monte Carlo, validation, reports, Replay, training, discovery, search and VPS analysis |
| Definitely inline | canonical reducers; `pair_to_routes`; BBO; FastL1; full L2 initially; rolling state; terminal viability; small q-grid; current Risk; Reservation; plan/intent; local signing; minimal Recorder/trace handoff |
| Definitely async | persistent market/account/metadata I/O; submit/cancel/status; orders/fills/balances reconciliation queries; result re-entry |
| Definitely background | Recorder write/flush/serialization/compression/checksum/chunk; checkpoint encode/write; archive/cleanup; metrics formatting/aggregation/export; runtime health/control maintenance |
| Definitely offline | Replay campaigns, F4/Monte Carlo, training/calibration, discovery, parameter search, reporting and comparative VPS analysis |
| Benchmark-only parallel candidates | route fanout/full L2, parallel q-grid, advanced features, Participant inference, F2/F3, sizing curve, portfolio and complex Recovery search, CPU pool topology/count |
| Incrementally maintained/precomputed candidates | spread/mid/depth/imbalance/microprice, OFI/MLOFI, volatility/jumps/regime, survival baseline, market/infra health, Graph/reverse index, Atlas and local immutable artifacts |
| Full L2 baseline | `C1 INLINE_BOUNDED_HOT_PATH` initially; QF-016 oracle; C2 only after profiling/parity |
| Route fanout | inline deterministic baseline; bounded C2 challenger |
| q-grid | small deterministic inline baseline; C2 challenger; final choice C0 |
| Participant inference | optional local C2 snapshot worker or valid simple/cached fallback; never remote-required |
| Simulator | F0/F1 bounded inline baseline; F2/F3 C2 candidates; F4/Monte Carlo C5 |
| Worker stale-result policy | complete versions/generation/deadline; C0 revalidate or discard; no automatic commit |
| Deadline policy | no `WAIT_FOREVER`; bounded wait, valid cache, simpler fallback, capability reduction or reject |
| Queue policy | every queue/task population bounded, prioritized, instrumented and explicit on overflow |
| Worker completion determines trade | `NO` |
| Remote service hot-path dependencies | `0` |
| Unbounded queues | `0` |
| Unbounded per-event task spawning | `0` |
| ACK blocks coordinator | `NO` |
| Recorder disk blocks coordinator | `NO` |
| Reconciliation HTTP blocks coordinator | `NO` |
| Leg 2 may use predicted Leg 1 fill | `NO` |
| Pure Leg 2 preparation before fill | `YES`, only where semantically safe; executable choice waits for actual fill |
| Route decision policies | `BATCH_SELECT` / deterministic `EARLY_COMMIT` |
| Current canonical winner | `NONE — CALIBRATED / REPLAY + SHADOW REQUIRED` |
| Adaptive policy | `RESEARCH` only |
| Two-vCPU concurrency risk | documented; oversubscription/scheduler/I/O starvation are measured treatments |
| Formula changes | `0` |
| Risk changes | `0` |
| Execution semantic changes | `0` |
| `Q_validated` changes | `0` |
| Roadmap phases | `26` |
| Implementation | `NOT AUTHORIZED` |
| Human approval | `PENDING` |

## Final recommendation

Use persistent asynchronous external I/O around one ordered logical coordinator. Apply canonical reducers inline and maintain cheap rolling state incrementally. Start with inline `pair_to_routes`, BBO, FastL1, full-L2 and small q-grid. Permit expensive optional prediction/simulation/allocation as bounded immutable-snapshot proposals only. Final sizing/allocation, current Risk, atomic Reservations and immutable ExecutionPlan/Intent remain ordered. Keep signing local and bounded; execute order/cancel/status/reconciliation as async effects whose observations re-enter the ordered event stream. Move disk, compression, archive and formatted observability to background; keep research outside the Live process.

This is appropriate for a relatively small initial VPS because it minimizes queue handoffs, scheduler contention, locks and cache disruption while preserving a deterministic Core. Async tasks cover network waiting; background tasks isolate disk/telemetry; expensive compute can scale later after evidence. It avoids unnecessary two-vCPU oversubscription and retains clear degradation under worker or background failure.

## Policy disposition

The repository does not prove that waiting for every affected-route result is better than earlier deterministic admission. `BATCH_SELECT` can improve global selection but pays fan-in/state-age cost. `EARLY_COMMIT` can reduce latency but may miss a better later route. Both require explicit population/admissibility, bounded deadlines, deterministic ties, current shared-capacity/Risk/Reservation checks and policy-versioned evidence. First-worker-wins is forbidden. Adaptive switching remains deferred Research.

## Validation and traceability

- required analysis artifacts: `21/21` created and non-empty;
- function classifications: `97` with C0–C5 totals above;
- scheduler/failure fixtures: `CT-001..015` specified;
- new post-reconstruction decisions: `HDC-091..094`, origin `HUMAN_POST_RECONSTRUCTION`, approval pending;
- Formula Book, Risk Constitution and `Q_validated`: unchanged;
- no code, Cargo, Docker, runtime configuration or legacy `docs/` change;
- external web sources used by this pass: `0`.

The review package must record the exact pushed commit before approval. This document authorizes neither Phase 1 nor any implementation, switchover, Shadow, Micro-live, Live or capital.
