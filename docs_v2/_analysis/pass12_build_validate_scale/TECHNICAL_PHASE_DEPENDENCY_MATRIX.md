# PASS 12 — Technical Phase Dependency Matrix

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

The canonical order is fixed, but the order is not a ban on safe parallel work. “Hard” means the consumer cannot meet its declared DoD without the producer contract/evidence. “Soft/parallel” means work may start against frozen interfaces while activation still waits.

| Phase | Capability | Hard dependencies | Soft / parallel work | Contract crossing the boundary | Exit maturity | External / open gate | Principal downstream consumer |
|---:|---|---|---|---|---|---|---|
| 1 | Domain Types / Schemas | Approved specs only | Formula golden-vector design | Strong IDs, units, envelopes, versions, Clock/RNG/RunManifest | M1 | Integer/codec choices open | All phases |
| 2 | Hyperliquid Adapters | 1 | Recorder fixtures | RawEvent→typed event/error; no Core mutation | M1 | Current wire/API rules | 3–5, 13 |
| 3 | Recorder | 1–2 | 4–5 using fixtures | Immutable RAW, sequence, quality, chunks, priority/backpressure | M1 + soak | Codec/capacity calibrated | 4, 8, all evidence |
| 4 | Book Engine | 1–3 | 5 metadata fixtures | Ordered snapshot/diff→versioned valid BookState | M1 | Current sequencing/snapshot semantics | 6–9, 15–22 |
| 5 | Metadata / Fee / Precision | 1–3 | 4 | Point-in-time rules, quantizers, invalidation | M1 | Current fees/precision/minimums | 6–9, 12–26 |
| 6 | Graph / Routes | 1, 4–5 | Atlas schema | GraphVersion, fixed route definitions, `pair_to_routes` | M1 | Market/status metadata | 7, 9, 14–26 |
| 7 | NetConvert / Formula Core | 1, 4–6, PASS11 | Replay harness design | Versioned exact QF implementation with parity | M1 | External fee/precision rules | 8–26 |
| 8 | Replay Engine | 1, 3–7 | Opportunity fixtures | Ordered same-Core execution, ReplayClock/RNG/RunManifest/trace | M2 | Dataset validity | 9–26 |
| 9 | Basic Opportunity Engine | 4–8 | 10–11 schemas | Affected route→BBO reject→exact L2 Opportunity/reject | M2 | None beyond inputs | 10–26 |
| 10 | Account / Inventory / Reservations | 1–3, 8–9 | Risk rules | Actual account/inventory plus distinct bounded reservations | M2 | Exchange account semantics | 11–26 |
| 11 | Risk Core | 1, 4–10, PASS05 | ESM tests | RiskSnapshot→RiskDecision; hard gates/kills/fallback | M2 | Calibrated limits | 12–26 |
| 12 | Execution State Machine | 1, 7–11, PASS04 | 13 transport adapter | Five deterministic machines, actual-fill plan evolution | M2 | Timer/dust policies calibrated | 13–26 |
| 13 | Hyperliquid Execution Transport | 2, 5, 11–12 | 14 reconciliation fixtures | Intent↔submit/cancel/ACK/fill translation; signer/nonce ownership | M2 conformance; M3 later in Shadow | Current order/signing/nonce rules | 14, 19–26 |
| 14 | Recovery / Reconciliation | 6–13 | 15–18 research | Exchange truth→resolved exposure/state; bounded best exit | M2 replay; M3 later in Shadow | Current query/account semantics | 19–26 |
| 15 | Quant Microstructure | 3–8 | 9/16 in observe-only mode | Point-in-time QF-028–043 feature snapshot | M2 | Windows calibrated | 16–26 |
| 16 | Market Atlas | 3, 6–9, 15 | Later survival enrichment | Versioned structural/empirical support map | M2 | Support/windows calibrated | 17, 21, 24–26 |
| 17 | Sizing | 7–11, 14–16 | 18 simulator curves | Feasible q curve bounded by Q_validated/all gates | M2 | Grid/support calibrated | 18–26 |
| 18 | Simulator F0 / F1 | 4–17 | Phase-21 model interface | Historical + latency/mechanical distributions | M2 | Calibration/support | 19–26 |
| 19 | Shadow | Phases 2–18 at required M2/M1 technical exits + deployment/ops/rollback | Phase 21 observe-only | Same Core, live inputs, no strategy submit, full evidence | M3 for the integrated live-input scope | Host/exchange readiness | 20–26 |
| 20 | Micro-live TT | 3, 10–14, 17–19 + Risk/Ops/rollback | Phase 21 data capture | Protected bounded TT with predicted↔actual chain | M4 (TT scope) | Explicit approval; current exchange facts | 21–26 |
| 21 | Survival / Participant Models | 3, 8–9, 15–16, 19–20 data as available | May begin with pre-capital episodes | Calibrated simple Champion plus governed challengers | M2/M3 | Horizon/support/economic lift | 22–26 |
| 22 | Advanced Simulator | 18, 21; 20 for calibration | F4 research isolated | F2 queue / F3 response; F4 research only | M2/M3 by fidelity | Model calibration/OOD | 23–26 |
| 23 | MT / MTT | 12–14, 17, 19–22 | TTT taker validation separate | Maker fill→actual output→taker continuation/recovery | M4 per mode | ALO/queue/fill/adverse evidence | 24–26 |
| 24 | Opportunity Portfolio | 10–11, 16–18, validated single opportunities | Bridge research | QF-078 joint allocation under shared constraints | M2 then M4 | EconomicLift vs simple baseline | 25–26 |
| 25 | Bridge / Capital Relocation | 6–8, 10–11, 14, 16–17, 24 | Research before activation | STAY vs destination, exit, relocation, hysteresis evidence | M2 then M4 | Opportunity-history support | 26 |
| 26 | Scaling | Validated target capability + 3, 10–25 as relevant | Independent capabilities progress separately | CapabilityManifest, Q_validated, Risk/economic/ops gates | M5 scoped/reversible | Current support and explicit promotion | Continuous operation |

## Hard dependency rules

- Phase 13 cannot bypass Phase 12: transport observes intentions; it does not own execution state.
- Phase 20 cannot bypass Recorder, Risk, actual-fill state, reservations, Recovery, Reconciliation, operations, Shadow, safe deployment or rollback; Phase 19 must first raise every capital-critical live-input dependency to M3.
- Phase 23 cannot use ALO support as proof of maker behavior.
- Phase 25 cannot precede terminal viability, Atlas history, sizing, Risk and exit evidence.
- Phase 26 is evidence governance, not a larger configuration value.

Bootstrap cycles are resolved in `ROADMAP_CONFLICT_RESOLUTION.md`; no hard dependency cycle remains.
