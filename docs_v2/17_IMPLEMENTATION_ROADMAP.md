# 17 — Technical Implementation Roadmap

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## 1. Purpose

This roadmap fixes **what to build, in which dependency order, and what evidence ends each technical phase**. It is documentation, not implementation authorization. No phase may be implemented before PASS 13–16 and explicit human approval.

## 2. Authority

The 26-phase order comes from SRC-006 Dossier 6, lines 5657–5710. Completed PASS 01–11 masters own their domain contracts: Formula Book owns equations; Risk Constitution owns permission; Execution owns state; Data/Recorder/Replay owns truth and determinism; Validation owns M0–M5/evidence; Operations owns readiness/incidents. Current Hyperliquid facts remain external gates. Later narrow closure overrides earlier suggestions; legacy `docs/**` is comparison-only.

## 3. Roadmap philosophy

```text
SPECIFICATION → IMPLEMENTATION → EVIDENCE
→ VALIDATED CAPABILITY → CAPITAL
```

Build in vertical slices, produce evidence at every boundary, retain negative results, and use simple conservative baselines before learned complexity. Never build everything and test at the end. Never translate a deposited balance into a phase or size.

## 4. Final-capable architecture / progressive activation

Every early implementation uses final identities, events, versions, state ownership and interfaces. A baseline is a conservative implementation inside those contracts; it is not a disposable MVP. Production Core is Rust; Python is for research/calibration/parity. Replay, Shadow, Micro-live and Live use the same Core and differ only through declared sources, effect transports, capital permission and provenance.

## 5. Phase model

Every phase below states: ID/name, why now, objective, input/output contracts, implementation scope, explicit non-scope, dependencies, Formula IDs, data, tests, entering/exit maturity, evidence, stop conditions, open/external gates and downstream consumers. Phase exit means its DoD is evidenced; it does not imply capital permission.

## 6. Parallelism versus hard dependencies

Canonical order governs integration and exit gates. Work may overlap when a producer interface is frozen: Recorder work can proceed with adapter fixtures; Book and Metadata can advance together; quant/Atlas research can observe data while execution integration matures; participant research can start once episodes exist. A consumer cannot claim maturity above a critical dependency. Transport depends on the state machine. Micro-live depends on Risk, actual-fill state, reservations, Recovery, Reconciliation, Recorder, operations, Shadow and rollback. Maker modes depend on maker evidence; Bridge depends on terminal viability/Atlas/sizing/Risk; scaling depends on current CapabilityManifest and `Q_validated`.

## 7. Phases 1–26 summary

| Phase | Capability | Phase exit | Capital |
|---:|---|---|---|
| 1 | Domain Types / Schemas | M1 foundations | None |
| 2 | Hyperliquid Adapters | M1 conformance | None |
| 3 | Recorder | M1 + continuous soak | None |
| 4 | Book Engine | M1 reconstruction | None |
| 5 | Metadata / Fee / Precision | M1 boundary rules | None |
| 6 | Graph / Routes | M1 structural routes | None |
| 7 | NetConvert / Formula Core | M1 golden parity | None |
| 8 | Replay Engine | M2 deterministic Core | None |
| 9 | Basic Opportunity Engine | M2 episodes | None |
| 10 | Account / Inventory / Reservations | M2 economic state | None |
| 11 | Risk Core | M2 constitutional gate | None |
| 12 | Execution State Machine | M2 emulated execution | None |
| 13 | Hyperliquid Execution Transport | M2 conformance; later M3 in Shadow | None |
| 14 | Recovery / Reconciliation | M2 replay; later M3 in Shadow | None |
| 15 | Quant Microstructure | M2 point-in-time features | None |
| 16 | Market Atlas | M2 structural/empirical map | None |
| 17 | Sizing | M2 supported q curves | None |
| 18 | Simulator F0 / Simulator F1 | M2 distributions | None |
| 19 | Shadow | M3 full no-effect chain | None |
| 20 | Micro-live TT | M4 TT probe | Probe only |
| 21 | Survival / Participant Models | M2/M3 model support | None directly |
| 22 | Advanced Simulator | F2/F3 M2/M3; F4 Research | None directly |
| 23 | MT / MTT | M4 per maker mode | Separate probes |
| 24 | Opportunity Portfolio | M2 then M4 | Promoted bounded only |
| 25 | Bridge / Capital Relocation | M2 then M4 | Separate probe/promotion |
| 26 | Scaling | M5 scoped/reversible | Scaled validated only |

## 8. Phase 1 — Domain Types / Schemas

- **WHY NOW / OBJECTIVE:** every later boundary needs one unambiguous identity, unit, event and version vocabulary before behavior is coded.
- **INPUT CONTRACTS:** PASS06 Data Contracts; PASS11 units/numeric policy; approved M0 specs.
- **OUTPUT CONTRACTS:** strong `VenueId`, `AssetId`, `MarketId`, `RouteId`, execution/order/fill/evidence IDs; typed price/quantity/notional/time units; event envelopes; schema/snapshot versions; `Clock`, `RngProvider`, `RunManifest` foundations.
- **WHAT TO IMPLEMENT:** serialization compatibility, deterministic canonical ordering helpers, exact boundary types, misuse/property/unit tests.
- **WHAT NOT YET:** network, books, route economics, edge, orders, signing, capital effects.
- **DEPENDENCIES / QF:** approved specs; no equation implementation required, but PASS11 notation/units constrain types.
- **DATA / TESTS:** small canonical fixtures; roundtrip, compatibility, invalid field, overflow, compile-time misuse and hidden clock/RNG tests.
- **MATURITY / EVIDENCE:** enter M0; exit M1 with a versioned domain-contract test report.
- **STOP / OPEN / EXTERNAL:** stop on ambiguous unit/owner/schema; integer widths, codec and internal algorithms remain implementation decisions; no exchange fact is assumed.
- **DOWNSTREAM:** all phases.

## 9. Phase 2 — Hyperliquid Adapters

- **WHY NOW / OBJECTIVE:** establish the only external-to-domain translation before recording or state mutation.
- **INPUTS / OUTPUTS:** Phase-1 types; current payload fixtures → `RawEvent`, normalized typed events and typed adapter failures.
- **IMPLEMENT / NOT YET:** transport abstraction, connect/subscribe/reconnect, parse and error mapping; never mutate Core state, calculate edge or submit strategy orders.
- **DEPENDENCIES / QF:** Phase 1; no owned QF.
- **DATA / TESTS:** real/sanitized fixtures for valid, missing, extra, malformed and unknown events; reconnect/resubscribe; unknown remains RAW-only.
- **MATURITY / EVIDENCE:** M0→M1; adapter conformance report.
- **STOP / OPEN / EXTERNAL:** current endpoints, payloads, timestamps, sequences, account events and authentication must be revalidated; malformed data must never mutate state.
- **DOWNSTREAM:** Recorder, Book, Metadata, account, execution transport.

## 10. Phase 3 — Recorder

- **WHY NOW / OBJECTIVE:** accumulate source truth while the rest is built; every model, Replay, calibration and incident depends on it.
- **INPUTS / OUTPUTS:** ordered raw adapter observations and Core evidence → immutable chunks, `RawChunkManifest`, quality intervals, critical journal evidence.
- **IMPLEMENT / NOT YET:** bounded non-blocking queue, `recorder_seq`, checksums, gaps, priorities P0–P3, backpressure and observable durability; do not block Core or silently call loss complete.
- **DEPENDENCIES / QF:** Phases 1–2; no owned QF.
- **DATA / TESTS:** throughput/compression/disk/backlog, slow/full disk, crash/close/checksum, saturation priority and sequence tests.
- **MATURITY / EVIDENCE:** M0→M1 plus continuous soak; Recorder evidence continues through M5 operations.
- **STOP / OPEN / EXTERNAL:** critical loss or ambiguous ordering blocks trusted evidence/capital; codec, chunks and retention values remain calibrated.
- **DOWNSTREAM:** Book reconstruction, Replay, models, Shadow, Micro-live, incidents.

## 11. Phase 4 — Book Engine

- **WHY NOW / OBJECTIVE:** reconstruct current tradable state before route economics.
- **INPUTS / OUTPUTS:** snapshot/diff/heartbeat plus metadata → single-writer immutable `BookState` with version, freshness and validity.
- **IMPLEMENT / NOT YET:** correct ordering, bid/ask sorting, sequence/gap detection, crossed/invalid state, resync; do not infer missing diffs or search alpha.
- **DEPENDENCIES / QF:** 1–3; book inputs support QF-001–013 later.
- **DATA / TESTS:** golden snapshot+diff final state, gap/desync/reconnect, stale/crossed book, one/many-market load and memory.
- **MATURITY / EVIDENCE:** M0→M1; book reconstruction report.
- **STOP / OPEN / EXTERNAL:** snapshot/diff/sequence semantics require current verification; any unexplained divergence invalidates the market.
- **DOWNSTREAM:** Graph economics, NetConvert, Opportunity, microstructure, Simulator.

## 12. Phase 5 — Metadata / Fee / Precision

- **WHY NOW / OBJECTIVE:** prevent false economics and illegal orders before route/formula trust.
- **INPUTS / OUTPUTS:** current/historical exchange rules → versioned metadata, fee state and conservative price/size quantizers with invalidation events.
- **IMPLEMENT / NOT YET:** base/quote/status, tick/lot/decimal/minimums, actual fee context, point-in-time versions; not strategy-specific economic ranking.
- **DEPENDENCIES / QF:** 1–3; QF-007–008 and QF-014–015.
- **DATA / TESTS:** boundary/golden/parity fixtures, historical fee state, rule change and dependent invalidation.
- **MATURITY / EVIDENCE:** M0→M1; exchange-boundary golden report.
- **STOP / OPEN / EXTERNAL:** unknown fee/precision/minimum rule rejects; all current Hyperliquid rules must be revalidated.
- **DOWNSTREAM:** Graph, NetConvert, Replay, execution transport, accounting.

## 13. Phase 6 — Graph / Routes

- **WHY NOW / OBJECTIVE:** enumerate legal, venue-aware conversion structures before evaluating economics.
- **INPUTS / OUTPUTS:** valid metadata + Book identities → `GraphVersion`, fixed Direct/Route2/Cycle3 definitions, comparator links, `pair_to_routes` and invalidation.
- **IMPLEMENT / NOT YET:** precompute bounded routes on topology change; distinguish OWA, Triangle and Bridge; no unbounded hot-path graph search, future venue execution or profitability claim.
- **DEPENDENCIES / QF:** 1, 4–5; QF-017–023 structure.
- **DATA / TESTS:** continuity, direction, exact cycle closure, direct comparator, duplicates, deterministic generation, affected-only lookup.
- **MATURITY / EVIDENCE:** M0→M1; route-generation report.
- **STOP / OPEN / EXTERNAL:** incoherent topology/metadata blocks affected routes; cross-exchange remains FUTURE.
- **DOWNSTREAM:** NetConvert, Opportunity, Recovery paths, Atlas, Bridge.

## 14. Phase 7 — NetConvert / Formula Core

- **WHY NOW / OBJECTIVE:** create one exact, versioned mathematical implementation before any opportunity claim.
- **INPUTS / OUTPUTS:** coherent book/metadata/fee/precision + q → typed QF outputs, failure reasons and provenance.
- **IMPLEMENT / NOT YET:** canonical book walk, fees, rounding, direct/indirect/cycle economics and golden parity; do not fork equations, double-count slippage/fees or authorize Risk.
- **DEPENDENCIES / QF:** 1, 4–6 and PASS11; QF-001–027.
- **DATA / TESTS:** all PASS11 golden families, unit/sign/boundary/insufficient-depth/non-finite cases, Rust/Python parity.
- **MATURITY / EVIDENCE:** M0→M1; FormulaVersion and parity report.
- **STOP / OPEN / EXTERNAL:** any formula/status/unit/rounding disagreement stops consumers; current fee/precision rules are external.
- **DOWNSTREAM:** Replay, Opportunity, Simulator, Sizing, Execution, Accounting.

## 15. Phase 8 — Replay Engine

- **WHY NOW / OBJECTIVE:** let every later component prove behavior immediately on historical and failure streams.
- **INPUTS / OUTPUTS:** DatasetId, ordered events, resolved config, models/formulas/schemas and seed → same-Core state, `DecisionTrace`, `ReplayReport`.
- **IMPLEMENT / NOT YET:** `ReplayClock`, RNG, RunManifest, exact/accelerated/counterfactual modes, checkpoints, no-lookahead and deterministic hashes; never a separate simplified backtester.
- **DEPENDENCIES / QF:** 1, 3–7; consumes any QF used by the configured path.
- **DATA / TESTS:** repeated trace/hash identity, full vs checkpoint/accelerated parity, future-event isolation and invalid-region rejection.
- **MATURITY / EVIDENCE:** M0/M1→M2 for Replay Core.
- **STOP / OPEN / EXTERNAL:** nondeterminism, hidden time/randomness or data gaps invalidate claims; merge/checkpoint tuning remains governed.
- **DOWNSTREAM:** every strategy/model/Risk/execution/capacity/release validation.

## 16. Phase 9 — Basic Opportunity Engine

- **WHY NOW / OBJECTIVE:** produce a measurable deterministic baseline before Participant sophistication.
- **INPUTS / OUTPUTS:** affected active routes + coherent books/formulas → exact `Opportunity` or machine-readable reject episode.
- **IMPLEMENT / NOT YET:** `pair_to_routes`, cheap BBO reject, exact L2/fees/precision/economics and route classification; no live submit or required advanced prediction.
- **DEPENDENCIES / QF:** 4–8; QF-016–027.
- **DATA / TESTS:** affected-only equivalence, BBO false-accept prohibition, direct comparator/triangle closure, replay reproducibility.
- **MATURITY / EVIDENCE:** M1 deps→M2; opportunity/reject episode dataset.
- **STOP / OPEN / EXTERNAL:** stale/incoherent inputs or invalid math reject; thresholds remain calibrated.
- **DOWNSTREAM:** Inventory/Risk, Atlas, survival labels, Simulator.

## 17. Phase 10 — Account / Inventory / Reservations

- **WHY NOW / OBJECTIVE:** represent actual capital and prevent shared resource overcommit before orders.
- **INPUTS / OUTPUTS:** account snapshots/events and deduplicated fills → Account/Inventory/Reservation states, available balance/book/Risk capacity.
- **IMPLEMENT / NOT YET:** actual-fill updates, balances, inventory classes/bands interfaces, reservation create/hold/release, UNKNOWN locks and reconciliation inputs; no Bridge optimizer yet.
- **DEPENDENCIES / QF:** 1–3, 8–9; QF-064–069 and QF-073–074 interfaces.
- **DATA / TESTS:** fill dedupe, account replay, concurrent reservation, overspend/shared-depth, restart and mismatch.
- **MATURITY / EVIDENCE:** M0/M1→M2.
- **STOP / OPEN / EXTERNAL:** unresolved exchange truth blocks affected new risk; bands/tolerances remain calibrated and account semantics external.
- **DOWNSTREAM:** Risk, Execution, Sizing, Portfolio, Bridge.

## 18. Phase 11 — Risk Core

- **WHY NOW / OBJECTIVE:** establish the constitutional safe action set before any transport receives capital.
- **INPUTS / OUTPUTS:** frozen RiskSnapshot, forecasts, inventory/capability/infra/config → deterministic `RiskDecision` and reason/evidence.
- **IMPLEMENT / NOT YET:** hard invariants, ordered gates, TTL/revalidation, action classes, kill switches, conservative fallback and risk-reducing exception; no profit-based bypass or invented limits.
- **DEPENDENCIES / QF:** 1, 4–10 and PASS05; QF-038–042, 044–050, 056–066, 073–080, 084–104, 109–110 as consumed.
- **DATA / TESTS:** unit/property/fault/replay for stale, UNKNOWN, hard inventory, tail, OOD, unsafe infra, kill/reset and determinism.
- **MATURITY / EVIDENCE:** M0/M1→M2.
- **STOP / OPEN / EXTERNAL:** invariant failure stops; thresholds/TTL/recovery limits require evidence (`OPEN-007/009`).
- **DOWNSTREAM:** every capital/effect phase.

## 19. Phase 12 — Execution State Machine

- **WHY NOW / OBJECTIVE:** prove intent, orders, actual fills, partials and uncertainty independently of real transport.
- **INPUTS / OUTPUTS:** current plan/Risk plus ordered order/fill/timer events → five canonical machine states, journal requests and bounded actions.
- **IMPLEMENT / NOT YET:** CLOID, order lifecycle, UNKNOWN, cancel races, actual-output propagation, dust/intermediate exposure and reservations; no direct network/signing ownership.
- **DEPENDENCIES / QF:** 1, 7–11 and PASS04; QF-079–080 Recovery interfaces.
- **DATA / TESTS:** zero/full/partial, leg failure, timeout/lost response, duplicate/late fill, cancel race, restart and event-order property tests.
- **MATURITY / EVIDENCE:** M0/M1→M2 with emulator/replay.
- **STOP / OPEN / EXTERNAL:** blind retry, corrupted state or unbounded Recovery impossible; timers/dust remain calibrated.
- **DOWNSTREAM:** transport, Recovery/Reconciliation, Shadow, every execution mode.

## 20. Phase 13 — Hyperliquid Execution Transport

- **WHY NOW / OBJECTIVE:** bind already-proven intents/state to the real exchange boundary without giving transport business authority.
- **INPUTS / OUTPUTS:** `OrderIntent`/cancel/query effects → typed submit/ACK/reject/order/fill/account events.
- **IMPLEMENT / NOT YET:** protected IOC and permitted forms, signing, nonce, CLOID/OID lookup, ownership and translation; no capital authorization, state mutation shortcut or blind retry.
- **DEPENDENCIES / QF:** 2, 5, 11–12; QF outputs only as pinned plan inputs.
- **DATA / TESTS:** official conformance fixtures, timeout/ambiguity/idempotence, signing scope, Shadow integration and duplicate prevention.
- **MATURITY / EVIDENCE:** M1→M2 with deterministic conformance/replay evidence; later M3 is earned in Phase 19 Shadow.
- **STOP / OPEN / EXTERNAL:** current order types, protection, signing, nonce, batching and account queries are mandatory external gates.
- **DOWNSTREAM:** Recovery/Reconciliation, Shadow, Micro-live, maker modes.

## 21. Phase 14 — Recovery / Reconciliation

- **WHY NOW / OBJECTIVE:** prove the system can determine and reduce actual exposure before any probe.
- **INPUTS / OUTPUTS:** exchange orders→fills→balances, local journal/checkpoint and current routes/Risk → reconciled state or explicit unresolved/halted state; bounded Recovery plan/outcome.
- **IMPLEMENT / NOT YET:** startup/runtime reconciliation, actual-fill residuals, best current exit, split exits only when validated, bounded attempts/time/loss; no route loyalty or optimistic READY.
- **DEPENDENCIES / QF:** 6–13; QF-068, 073–074, 079–080, accounting QF-105–110.
- **DATA / TESTS:** missing fill/order, unexpected order, mismatch, crash boundaries, leg partial/failure, multiple exits, split/replan and exhaustion.
- **MATURITY / EVIDENCE:** M1→M2 through Replay/emulation; Phase 19 raises the live-input Recovery/Reconciliation capability to M3 before capital.
- **STOP / OPEN / EXTERNAL:** unresolved UNKNOWN/mismatch/recovery failure blocks affected READY; exchange query semantics external.
- **DOWNSTREAM:** Shadow, Micro-live, Simulator, all modes and incidents.

## 22. Phase 15 — Quant Microstructure

- **WHY NOW / OBJECTIVE:** observe point-in-time conditions needed for later survival, Simulator and Risk without delaying the deterministic baseline.
- **INPUTS / OUTPUTS:** valid versioned book/trade/time state → immutable feature snapshots with support/provenance.
- **IMPLEMENT / NOT YET:** imbalance, OFI/MLOFI, microprice, returns, volatility, jumps, participation, impact and resilience interfaces; observe/record/validate before decision authority.
- **DEPENDENCIES / QF:** 3–8; QF-028–043.
- **DATA / TESTS:** golden formulas, incremental vs offline recomputation, million-update drift, non-finite/stale/invalid inputs and point-in-time replay.
- **MATURITY / EVIDENCE:** M0/M1→M2.
- **STOP / OPEN / EXTERNAL:** invalid/stale features cannot become zero/confident; windows/weights/support learned/calibrated.
- **DOWNSTREAM:** Atlas, Participants, Simulator, Risk, Sizing, Infra economics.

## 23. Phase 16 — Market Atlas

- **WHY NOW / OBJECTIVE:** map structural and empirical market/route/asset/capital support after evidence exists.
- **INPUTS / OUTPUTS:** Graph, books, opportunities and microstructure → versioned topology/liquidity/opportunity/support/exit/capital-reachability fields.
- **IMPLEMENT / NOT YET:** simple structural/liquidity/opportunity counts and HWC support first; no permanent hand ranking or requirement for every future learned field.
- **DEPENDENCIES / QF:** 3, 6–9, 15; consumes QF-026–050, 067–076, 081–083 as evidence becomes available.
- **DATA / TESTS:** point-in-time rebuild, missing→UNKNOWN/LOW, version/provenance, no-lookahead and support slices.
- **MATURITY / EVIDENCE:** M0/M1→M2, enriched continuously.
- **STOP / OPEN / EXTERNAL:** insufficient support limits fields/capabilities; windows/HWC/score thresholds remain `OPEN-016`.
- **DOWNSTREAM:** Sizing, models, Portfolio, Bridge, scaling.

## 24. Phase 17 — Sizing

- **WHY NOW / OBJECTIVE:** choose total exposure only after exact economics, Risk, inventory and early support exist.
- **INPUTS / OUTPUTS:** candidate q curve, balances/book/reservations, forecasts, inventory and Risk → validated feasible q or zero.
- **IMPLEMENT / NOT YET:** nonlinear RAEV curve, all-gates `Q_validated`, candidate grid/refinement and shared-capacity checks; do not infer q from account capital or use slicing to create capacity.
- **DEPENDENCIES / QF:** 7–11, 14–16; QF-056–063, 073–077.
- **DATA / TESTS:** exhaustive-small-case comparison, discontinuities, boundary/minimums, no-valid-size, shared capacity and OOD.
- **MATURITY / EVIDENCE:** M0/M1→M2; real bands mature in Stages 10–19.
- **STOP / OPEN / EXTERNAL:** unsupported q returns zero/reject; grid/bands/tail/support stay calibrated.
- **DOWNSTREAM:** Simulator scenarios, Micro-live, Portfolio, Bridge, scaling.

## 25. Phase 18 — Simulator F0 / F1

- **WHY NOW / OBJECTIVE:** establish reproducible historical and latency/mechanical outcome distributions before live claims.
- **INPUTS / OUTPUTS:** same Core, Replay data, plans/q, latency/arrival/book mechanics → F0/F1 distributions, confidence and failure/recovery outcomes.
- **IMPLEMENT / NOT YET:** historical book/fees/rounding/simple fills, then arrival latency, mechanical impact and partials; no F4 truth or deterministic single-PnL claim.
- **DEPENDENCIES / QF:** 4–17; QF-009–016, 026–027, 040–043, 056–063, 076, 079–080, 084–085, 095–104.
- **DATA / TESTS:** determinism, mechanics/golden cases, distribution/tail/coverage reporting, fidelity limitations and OOD.
- **MATURITY / EVIDENCE:** M0/M1→M2.
- **STOP / OPEN / EXTERNAL:** unsupported mechanics/bias cannot authorize capital; latency/calibration parameters empirical.
- **DOWNSTREAM:** Shadow forecasts, Risk/Sizing, later F2/F3.

## 26. Phase 19 — Shadow

- **WHY NOW / OBJECTIVE:** prove the complete real-time system on live inputs with no strategy order effect.
- **INPUTS / OUTPUTS:** real feed/account, same Core/Risk/sizing/plans/reconciliation, no-effect transport → `ShadowRun`, would-submit trace and future-outcome observations.
- **IMPLEMENT / NOT YET:** deploy/operate full chain, readiness, safe shutdown/rollback, alerts and complete evidence; no strategy submit or capital mutation.
- **DEPENDENCIES / QF:** 2–18 plus PASS09/10 deployment/operations contracts; all configured formula families.
- **DATA / TESTS:** sustained stability, state/trace completeness, latency/stale/reject paths, zero account mutation and release/rollback rehearsal.
- **MATURITY / EVIDENCE:** M2 deps→M3.
- **STOP / OPEN / EXTERNAL:** instability, leak, stale state, incomplete evidence, owner/security/readiness failure blocks exit.
- **DOWNSTREAM:** Micro-live and every new capability/release/market/size rehearsal.

## 27. Phase 20 — Micro-live TT

- **ACTIVATION RULE:** **TT first** — Taker→Taker is the first normal real execution capability.
- **WHY NOW / OBJECTIVE:** use minimal intentional capital as a measurement instrument for real transport/fills/economics.
- **INPUTS / OUTPUTS:** exact TT opportunity, current Risk, validated probe q, reservations and protected transport → fills, state/recovery/accounting/reconciliation and predicted↔actual evidence.
- **IMPLEMENT / NOT YET:** TT only as first normal mode, bounded frequency/notional/size, explicit stop/rollback; no automatic Live/scaling or fixed monetary rule.
- **DEPENDENCIES / QF:** Recorder, 10–14, 17–19, Risk/Ops/rollback; QF-016–027, 056–063, 073–080, 095–110.
- **DATA / TESTS:** intent→send→ACK→fills→fees→slippage→remaining→Recovery→PnL joins; critical fault drills before probe.
- **MATURITY / EVIDENCE:** M3 deps→M4 TT scope; capital is probe only.
- **STOP / OPEN / EXTERNAL:** any safety, UNKNOWN, recovery, reconciliation, evidence, security or accounting issue stops; `€40–50` is illustrative only; explicit human approval required.
- **DOWNSTREAM:** TT validation, calibration, participant/capture evidence, TTT preparation.

## 28. Phase 21 — Survival / Participant Models

- **WHY NOW / OBJECTIVE:** turn accumulated opportunity/microstructure/shadow/probe episodes into calibrated competition forecasts.
- **INPUTS / OUTPUTS:** labeled point-in-time episodes → survival/capture/liquidity/cross-market/maker-support forecasts with confidence/OOD/version.
- **IMPLEMENT / NOT YET:** naive baseline then simplest empirical Champion and governed challengers; no fictional identity requirement or complex agent prerequisite.
- **DEPENDENCIES / QF:** 3, 8–9, 15–16, 19–20 data as available; QF-044–055, 081–083, 095–104.
- **DATA / TESTS:** temporal OOS, right-censoring, Brier/LogLoss/calibration, ablation, EconomicLift, OOD/drift/fallback/runtime.
- **MATURITY / EVIDENCE:** M0/M1→M2/M3; capital only through a separately promoted consumer.
- **STOP / OPEN / EXTERNAL:** no target/label/support or no lift retains baseline; models/horizons are `OPEN-008/010`.
- **DOWNSTREAM:** Advanced Simulator, maker modes, Sizing, Atlas, Infra ROI.

## 29. Phase 22 — Advanced Simulator

- **WHY NOW / OBJECTIVE:** add only those queue/response mechanisms that collected evidence can calibrate.
- **INPUTS / OUTPUTS:** F0/F1 plus participant/maker evidence → F2 Queue and F3 Responsive distributions; optional isolated F4 Research.
- **IMPLEMENT / NOT YET:** explicit L2 queue uncertainty, calibrated local/sparse response and confidence; F4 agents do not become production truth.
- **DEPENDENCIES / QF:** 18, 21 and Micro-live calibration; QF-040–063, 079–085, 095–104.
- **DATA / TESTS:** pessimistic/optimistic/probabilistic queue bounds, distribution coverage, live contradiction, rejoin/non-rejoin and OOD.
- **MATURITY / EVIDENCE:** F2/F3 M2/M3 then M4 support where proven; F4 Research.
- **STOP / OPEN / EXTERNAL:** higher fidelity without calibration cannot increase confidence/capital; current queue/L4 facts external.
- **DOWNSTREAM:** MT/MTT, advanced sizing/capacity, research.

## 30. Phase 23 — MT / MTT

- **WHY NOW / OBJECTIVE:** activate maker-led execution only after queue/fill/adverse behavior and taker continuations are evidenced.
- **INPUTS / OUTPUTS:** maker opportunity/forecast, current Risk/q and ESM → actual maker fill then TT/TTT continuation or bounded Recovery.
- **IMPLEMENT / NOT YET:** MT and MTT separately, actual-output propagation, cancel/expiry/partial maker handling; TM/MM remain type-supported/default-disabled.
- **DEPENDENCIES / QF:** 12–14, 17, 19–22; QF-025, 044–063, 073–080, 095–104.
- **DATA / TESTS:** fill/time/adverse calibration, cancel race, no-fill/partial, later-leg/recovery, mode-specific predicted↔actual.
- **MATURITY / EVIDENCE:** M3 dependencies→M4 separately per mode/scope.
- **STOP / OPEN / EXTERNAL:** ALO support alone is insufficient; `OPEN-012`, current ALO/queue/order facts and explicit approval gate activation.
- **DOWNSTREAM:** Portfolio, maker scale, M5 scopes.

## 31. Phase 24 — Opportunity Portfolio

- **WHY NOW / OBJECTIVE:** allocate shared resources across multiple already-valid opportunities after one-route behavior is understood.
- **INPUTS / OUTPUTS:** individually eligible q curves, balances/depth/inventory/Risk budgets → joint quantities/reservations or simple baseline choice.
- **IMPLEMENT / NOT YET:** QF-078 constrained allocation, brute-force small-case oracle and greedy/simple Champion; no complex optimizer without lift.
- **DEPENDENCIES / QF:** 10–11, 16–18 and validated opportunities; QF-073–078.
- **DATA / TESTS:** shared book/balance races, inventory/Risk constraints, determinism, performance and EconomicLift vs baseline.
- **MATURITY / EVIDENCE:** M0/M1→M2, then M4/M5 only after live scoped proof.
- **STOP / OPEN / EXTERNAL:** double allocation or no robust lift rejects complexity; solver/limits remain calibrated.
- **DOWNSTREAM:** Bridge/capital placement and horizontal scale.

## 32. Phase 25 — Bridge / Capital Relocation

- **WHY NOW / OBJECTIVE:** decide if moving existing capital to a supported destination beats staying, after reliable opportunity history exists.
- **INPUTS / OUTPUTS:** actual inventory, Atlas/terminal/exit/sizing/Risk/portfolio evidence and candidate paths including STAY → relocation decision/plan/evidence.
- **IMPLEMENT / NOT YET:** BridgeCost, ExpectedExitCost, EV destination/stay, relocation risk, break-even cycles, hysteresis/cooldown/utility; never classify no-comparator path as OWA or use a transient edge.
- **DEPENDENCIES / QF:** 6–8, 10–11, 14, 16–17, 24; QF-068–072, 073–078, 105–108.
- **DATA / TESTS:** point-in-time replay, all paths+STAY, flip-flop, terminal failure, realized future utilization/exit/accounting.
- **MATURITY / EVIDENCE:** M0/M1→M2, separate M4 probe and eventual scoped M5.
- **STOP / OPEN / EXTERNAL:** insufficient Atlas history/support, unsafe terminal or STAY superiority rejects movement; calibration remains open.
- **DOWNSTREAM:** capital intelligence and scaling.

## 33. Phase 26 — Scaling

- **WHY NOW / OBJECTIVE:** expand only capabilities whose evidence, Risk, capacity and operations justify the exact new scope.
- **INPUTS / OUTPUTS:** current CapabilityManifest, Q_validated, economic/operational evidence, incidents and proposals → promote/hold/shrink/demote/revert decision.
- **IMPLEMENT / NOT YET:** horizontal, vertical, market, strategy, maker, relocation and infrastructure expansion governance; never automatic compounding, balance-based q or prestige upgrade.
- **DEPENDENCIES / QF:** every producer required by target scope; QF-056–063, 073–078, 084–110.
- **DATA / TESTS:** next-scope Replay/Shadow/Micro-live, shared constraints, distribution/tails, drift/incidents, rollback and InfraROI.
- **MATURITY / EVIDENCE:** scoped M4→M5, continuously reversible.
- **STOP / OPEN / EXTERNAL:** lost support shrinks permission immediately; every new market/mode/size/host revalidates affected assumptions.
- **DOWNSTREAM:** continuous calibrated operations, not a terminal “finished bot.”

## 34. Cross-phase dependency matrix

The authoritative row-level matrix is [TECHNICAL_PHASE_DEPENDENCY_MATRIX.md](_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_DEPENDENCY_MATRIX.md). Critical chain:

```text
Types → Adapters → Recorder/Book/Rules → Graph → Formula
→ Replay → Opportunity → Account/Reservations → Risk
→ Execution SM → Transport → Recovery/Reconciliation
→ Sizing/Simulator → Shadow → Micro-live TT
→ Models/Advanced Simulator/Maker → Portfolio/Bridge → Scaling
```

Quant/Atlas and evidence work overlap this chain only through frozen contracts and cannot bypass exit gates.

## 35. Validation maturity mapping

Use [TECHNICAL_PHASE_TO_MATURITY_MAP.md](_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_TO_MATURITY_MAP.md) and PASS10. Phase exit, maturity and activation are distinct. Recorder may be M5 operationally while TT is M4, a participant Challenger M2, MT disabled and Bridge M1/M2.

## 36. External revalidation gates

[EXTERNAL_REVALIDATION_GATE_MAP.md](_analysis/pass12_build_validate_scale/EXTERNAL_REVALIDATION_GATE_MAP.md) maps current market metadata, fees, precision, order, signing, nonce, event/feed and platform facts to affected phases and run modes. An unverified fact blocks only the capability that consumes it.

## 37. Stop conditions

[STOP_CONDITION_MATRIX.md](_analysis/pass12_build_validate_scale/STOP_CONDITION_MATRIX.md) owns the 20 global/scoped conditions. A stop means “do not promote this scope,” not “abandon all safe independent research.” Risk-reducing actions remain available where constitutionally safe.

## 38. Implementation blockers

[IMPLEMENTATION_BLOCKER_REGISTER.md](_analysis/pass12_build_validate_scale/IMPLEMENTATION_BLOCKER_REGISTER.md) distinguishes capital-critical blockers, implementation gates, non-blocking research and Future work. F4, cross-exchange, private node, hot standby and a complex portfolio optimizer do not block initial TT.

## 39. Evidence produced by each phase

Each phase emits a versioned contract/test/report artifact; runtime phases emit canonical `RawChunkManifest`, `DatasetId`, `RunManifest`, `DecisionTrace`, `ReplayReport`, `ShadowRun`, `MicroLiveRun`, `ModelReport`, `InfraBenchmark`, `ValidationReport`, `CapabilityManifest` or `IncidentId` as applicable. Evidence is immutable, attributable and negative-result preserving.

Formula dependency families are mapped, never rewritten: NetConvert/route core `QF-001–027`; microstructure `QF-028–043`; survival/maker `QF-044–055`; Simulator/Risk outcomes `QF-056–063`; Inventory/Sizing/Bridge/Recovery `QF-064–080`; competition `QF-081–083`; infrastructure `QF-084–094`; calibration/model value/confidence `QF-095–104`; accounting/drawdown `QF-105–110`.

## 40. Relationship with Build / Validate / Scale Journey

This document says **what to build**. [19_BUILD_VALIDATE_SCALE_ROADMAP.md](19_BUILD_VALIDATE_SCALE_ROADMAP.md) says **what must be learned before a capability may be trusted with capital**. One technical phase can serve many evidence stages; one evidence stage can require many technical phases.

## 41. First executable instruction after human approval

Only after PASS 13, PASS 14, PASS 15, PASS 16 and explicit human approval may a future Codex receive “Implement Phase 1.” That instruction permits only the Phase-1 types/schemas/Clock/RNG/RunManifest foundations and their unit/property/misuse/serialization tests. It excludes network, books, edge, orders, signing and any capital effect. Any remaining ambiguity is reported; it is not invented.

## 42. Deep-spec / source links

- [Roadmap deep specifications](deep-specs/roadmaps/README.md)
- [Technical dependency matrix](_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_DEPENDENCY_MATRIX.md)
- [Phase DoD matrix](_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_DOD_MATRIX.md)
- [Technical/evidence crosswalk](_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_TO_EVIDENCE_STAGE_MAP.md)
- [PASS 12 report](_analysis/pass12_build_validate_scale/PASS12_FINAL_REPORT.md)
- [Validation Matrix](16_VALIDATION_MATRIX.md)
- [Formula Book](04_FORMULA_BOOK.md)
- [Source inventory](_analysis/SOURCE_INVENTORY.md)
