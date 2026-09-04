# PASS 03 — Simulator Legacy Comparison

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

Comparison was performed only after the V2 master/deep specifications were written. Legacy is evidence of prior compression, not design authority.

| Topic | Legacy state | PASS 03 result | Classification |
|---|---|---|---|
| Exact alternate-world limitation | Correct one-paragraph warning | Expanded into operational incompatibility, mode, confidence, and non-rejoin semantics | RECOVERED / OVER_COMPRESSED |
| Three distinct problems | Implicit in pipeline | Exchange Mechanics, Historical Compatibility, Market Response explicitly separated | MISSING → RECOVERED |
| Arrival timeline | Compact equation only | QF-084 closure, receive-time, arrival book, measured distributions, no look-ahead | OVER_COMPRESSED → RECOVERED |
| Exchange Emulator | Named in pipeline | Order/effect boundary, mechanics/errors, external-rule revalidation, same event schemas | OVER_COMPRESSED → RECOVERED |
| Mechanical/response separation | Correct high-level statement | `Δour`, local mutation, OFI shock, double-counting invariant | RECOVERED |
| Historical event incompatibility | One sentence about unavailable depth | Negative-depth/cancel/trade/queue conflict and explicit event policy | OVER_COMPRESSED → RECOVERED |
| Exogenous vs Interactive | Correct summary | Exact SRC-005 `SimulationMode`, use cases/limits/provenance and supported combinations | RECOVERED / EXPANDED |
| Multi-market branches | Only other-market distinction | Per-market baseline/deltas, sparse response neighbourhood, per-leg arrival, Dominant Decay Leg boundary | MISSING → RECOVERED |
| Initial response model | “optional aggregate response” only | Conditional Empirical Champion direction; conditioned response vector; advanced challengers | MISSING → RECOVERED |
| Other participants | Not detailed | Aggregate conditional flow; explicit identities/agents Research only | MISSING → RECOVERED |
| Maker queue L2/L4 | Queue mentioned | Exact L2 limitation, L4 external boundary, three queue modes and required outputs | MISSING → RECOVERED |
| Adverse selection/MT | Named as sampled variable | QF-051–055/058 semantics, second-leg/recovery integration, calibration | OVER_COMPRESSED → RECOVERED |
| Fragmentation/slicing | Absent | same-time equivalence vs temporal replenishment/decay; candidate paths only | MISSING → RECOVERED |
| Liquidity resilience | Absent | QF-043 response/rejoin role and stochastic replenishment | MISSING → RECOVERED |
| Branch-and-rejoin | “bounded horizon/rejoin policy” | explicit event, calibrated variable horizon, non-rejoin/conservative terminal | OVER_COMPRESSED → RECOVERED |
| Scenario/Risk outputs | Good compact list | mutually exclusive F/P/R/X, QF-056–063, recovery, Q_validated/multi-size | RECOVERED / EXPANDED |
| SimulationConfidence | confidence gates mentioned | QF-104 decomposed gates/causes, fidelity≠confidence, Risk action | OVER_COMPRESSED → RECOVERED |
| F0–F4 | Correct short table | Exact source names, inputs/models/outputs/limits/promotion/capital matrix | RECOVERED / EXPANDED |
| Determinism/Data contracts | Clock/RNG/manifest mentioned | all axes, events/timers/trace/hashes/artifacts/state versions/stale workers | OVER_COMPRESSED → RECOVERED |
| Validation | Compact bullets | capability map, M0–M5, Predicted/Actual, coverage, live precedence, kill switch | OVER_COMPRESSED → RECOVERED |
| External facts | Not itemized | exchange/feed/L4/API/academic snapshots routed for revalidation | MISSING → RECOVERED |

## Cross-document comparison

- `docs/12_RECORDER_AND_REPLAY.md` correctly preserves recorded-order Replay, Clock/RNG/manifest, invalid gaps, and same core; PASS 03 recovers SimulationMode, fidelity combinations, branch/rejoin, TimerEvent, state version, and forecast contracts.
- `docs/10_EXECUTION_STATE_MACHINE.md` correctly provides order/recovery/timer shapes; exact transition ownership remains PASS 04 rather than imported here.
- `docs/04_FORMULA_BOOK.md` is a compressed formula catalogue; all 42 Simulator formulas were reopened in SRC-004, and Formula Index metadata cleanup is routed to PASS 11.
- `docs/06_MARKET_PARTICIPANTS.md` contains progressive participant/cross-market/maker direction; PASS 02 V2, not legacy, is the consumed interface.
- `docs/16_VALIDATION_MATRIX.md` correctly compresses M0–M5 and scientific gates; PASS 03 restores fidelity-specific and capability-specific validation.

## Legacy-only claims

- Legacy-only untraced imports accepted: **0**.
- Contradicted claims imported: **0**.
- Items routed to future owning passes: exact Data schemas (PASS 06), exact Execution/Recovery states (PASS 04), Risk thresholds (PASS 05), sizing/slicing (PASS 07), graph neighbourhood construction (PASS 08), Formula audit (PASS 11).

No legacy file was modified.
