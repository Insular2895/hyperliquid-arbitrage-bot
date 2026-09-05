# Data / Recorder / Replay Conflict Resolution

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| # | Conflict | Older/exploratory position | Canonical resolution | Authority/result |
|---:|---|---|---|---|
| 1 | Recorder P2/P3 | SRC-003: P2 derived/opportunities; P3 general RAW | P2 general market; P3 derived diagnostics | SRC-005 closure; older order superseded |
| 2 | Replay implementation | Simplified/separate backtest logic implied in legacy/exploration | Replay is the bot; same Core/reducers/formulas/risk/execution | SRC-005 closure |
| 3 | Historical evidence | Normalized/edge tables can appear sufficient | RAW exact payload remains immutable source evidence | SRC-005 + compatible SRC-003 |
| 4 | Time/order | Exchange timestamp can look like event order | Receive chronology + local Recorder sequence represents knowledge; exchange time is research chronology | SRC-005 closure |
| 5 | Checkpoint truth | Snapshot may appear to restore complete truth | Checkpoint + journal + exchange reconciliation; no READY before consistency | SRC-005 closure |
| 6 | Queue priority/order | Higher priority may imply earlier processing | Capture/retention priority cannot reorder dependent economic evidence | SRC-005 closure |
| 7 | Concurrency | Worker completion can commit opportunistically | One ordered coordinator; result carries input version; stale discard/revalidate | SRC-005 closure |
| 8 | Persistence path | Recorder/storage work may run inline | No write/fsync/compress/archive in hot path; bounded non-blocking handoff | SRC-005 closure + SRC-003 |
| 9 | Run-mode behavior | Replay/Paper/Live-specific strategy shortcuts | RunMode changes source/transport/effects/config only, never math/business logic | SRC-005 closure |
| 10 | Historical model use | Later model can be mixed into old replay | Historical truth uses point-in-time artifacts; later model requires `COUNTERFACTUAL_MODEL` | SRC-005 closure |

PASS 00 status heuristics marked 10 closure rows as RESEARCH/FUTURE/CALIBRATED/REJECTED. Their Dossier 4 requirements are now routed to `MASTER` under closure authority: `REQ-DATA-0107`, `REQ-DATA-0127`, `REQ-DATA-0157`, `REQ-REPLAY-0011`, `REQ-DATA-0244`, `REQ-DATA-0246`, `REQ-DATA-0248`, `REQ-DATA-0250`, `REQ-DET-0013`, `REQ-DATA-0312`. This does not turn example durations, thresholds or provider choices into locked constants.

Conflicts found: **10**. Resolved by authority: **10**. Remaining documentary conflicts: **0**. Open implementation/calibration decisions are recorded separately and do not alter these contracts.
