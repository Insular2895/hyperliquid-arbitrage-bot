# PASS 12 — Technical Phase Definition-of-Done Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

PASS 10 remains the authority for evidence sufficiency. These are phase exits, not authorization to start the next capital-bearing mode.

| Phase | DoD evidence | Mandatory failure proof | Exit artifact |
|---:|---|---|---|
| 1 | Typed IDs/units cannot be mixed; schemas round-trip/version; Clock/RNG/RunManifest interfaces tested | Invalid unit, overflow, incompatible schema, hidden time/randomness rejected | Domain contract + M1 evidence |
| 2 | Known payload fixtures parse deterministically; reconnect/error mapping proven | Malformed/unknown payload never mutates Core | Adapter fixture report |
| 3 | RAW append-only, ordered, checksummed; throughput/backpressure/priority/crash recovery measured | Slow/full disk and loss produce explicit quality/Risk evidence | RawChunkManifest + soak report |
| 4 | Snapshot+diff rebuild equals golden book; sorted sides/version/freshness hold | Gap/cross/invalid state fails closed until resync | Book reconstruction report |
| 5 | Metadata/fees/precision are versioned, point-in-time and parity tested | Unknown/change/invalid rule rejects and invalidates dependents | Boundary golden report |
| 6 | Direct/Route2/Cycle3 continuity and reverse indexes are exact/deterministic | Missing comparator, invalid topology, stale route rejected | Graph/route generation report |
| 7 | QF-001–027 relevant outputs match golden vectors across Rust/Python contract | Non-finite, unit/sign, rounding, insufficient depth fail typed | Formula parity report |
| 8 | Same manifest/events/config/models/formulas/seed yields identical DecisionTrace/hash | No-lookahead, invalid region, checkpoint mismatch rejected | ReplayReport + DatasetId |
| 9 | Affected-only route evaluation and exact candidate/reject outputs replay reproducibly | BBO cannot accept; stale/incoherent inputs reject | Opportunity episode dataset |
| 10 | Actual fills reconcile inventory; reservations prevent shared overcommit and survive UNKNOWN | Duplicate fill, mismatch, overspend and premature release blocked | Account/inventory replay report |
| 11 | All constitutional hard gates/kills/action classes deterministic under property/fault tests | Stale, OOD, unsafe infra, hard inventory and tail breaches fail closed | Risk validation report |
| 12 | Five machines cover zero/full/partial/failure/cancel/UNKNOWN/restart deterministically | Blind retry, planned-fill propagation, unbounded Recovery impossible | Execution trace suite |
| 13 | Submit/cancel/ACK/fill translation and signer ownership pass fixtures, integration and deterministic replay | Ambiguous submit/nonces/rejects never create blind duplicate | M2 transport conformance report; Shadow later supplies M3 |
| 14 | Replay/emulated startup reconciliation resolves orders→fills→balances; Recovery chooses bounded current best exit | Unresolved exposure/mismatch cannot reach READY even in emulation | M2 Recovery/Reconciliation report; Shadow later supplies M3 |
| 15 | Incremental QF-028–043 equals offline reference within governed tolerance | NaN/Inf/stale features rejected | Feature parity report |
| 16 | Atlas can emit versioned structure/liquidity/opportunity/support fields point-in-time | Missing evidence is UNKNOWN/LOW, never zero/truth | Atlas evidence report |
| 17 | Candidate-grid/refinement matches exhaustive small cases; q obeys all constraints | Unsupported size returns zero/reject; slicing cannot enlarge q | Sizing validation report |
| 18 | F0 history and F1 arrival/mechanics emit reproducible distributions | Fidelity claims cannot exceed modeled/calibrated mechanisms | Simulator F0/F1 report |
| 19 | Sustained live-input Shadow uses same Core and records would-decide/execute with zero strategy effects | Leak, instability, stale state, incomplete trace or account mutation blocks exit | ShadowRun + M3 report |
| 20 | Bounded TT probes reconcile every intent/fill/fee/recovery/PnL and predicted↔actual comparison | Any safety incident, unresolved UNKNOWN, bad accounting or unsupported tail stops | MicroLiveRun + M4 TT report |
| 21 | Simple empirical Champion beats naive baseline OOS with calibration and positive EconomicLift | OOD/drift/miscalibration falls back or rejects | ModelReport |
| 22 | F2/F3 outputs calibrated by supported slices; F4 labeled Research | Unsupported response/queue cannot increase confidence/capital | Fidelity validation report |
| 23 | Maker fill/time/adverse/cancel/expiry/partial/recovery predictions calibrated per mode | ALO availability alone cannot pass; actual maker output controls later legs | MT/MTT scoped M4 report |
| 24 | Joint allocation respects shared balance/depth/inventory/Risk and beats simple baseline | Double reservation or no lift rejects complex optimizer | Portfolio ModelReport |
| 25 | STAY and all permitted paths compare with realized utilization/exit/relocation evidence | Transient edge, flip-flop, unsafe terminal or unsupported future EV rejects | Bridge validation report |
| 26 | Each promoted scope has current CapabilityManifest, Q_validated, operations and economic evidence | Drift/incident/OOD/capacity/infra failure demotes or shrinks | Scoped M5 ValidationReport |
