# PASS 02 — Market Participants Final Report

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 02 REVIEW COMPLETE`

## Scope and result

PASS 02 rebuilt the Market Participants / Competition domain from original sources. It specifies collective response rather than invented identities, locks final-capable Survival/Liquidity/Maker/Cross-Market interfaces, keeps coefficients and horizons learned/calibrated, and confines advanced models to governed Challenger/Research roles.

## Review totals

- Participant-related requirements reviewed: **282**.
- PASS 00 IDs reviewed: **263** (261 extracted + 2 overlays).
- Recovered Formula dependencies: **19**.
- Original source locator review: **282 YES**, **0 NO**.
- Original sources reopened: **8/8**, SRC-001 through SRC-008.
- Merged requirement locator intervals: **144**.
- Unique original lines in merged locators: **10,441**, plus continuous context reading of SRC-007 Part 4.
- Destinationless requirements: **0**.
- Files modified outside `docs_v2`: **0**.
- PASS 03 started: **NO**.

## Requirements canonicalized

The pass ledger classifies **130** requirements as `CANONICALIZED` and **152** as `REVIEWED_DEPENDENCY`. Dispositions are: `MASTER` 14; `DEEP_SPEC` 93; `CROSS_DOMAIN_FUTURE_PASS` 119; `RESEARCH_REGISTER` 35; `EXTERNAL_REGISTER` 18; `REJECTED` 3. No ID was renumbered.

The status correction is central: `LOCKED_ARCHITECTURE` does not imply fitted coefficients. Survival/capture/fill/response interfaces and safety/governance are fixed where closure supports them; estimators, coefficients, horizons, weights, support and activation remain learned/calibrated.

## Master created

- `docs_v2/06_MARKET_PARTICIPANTS.md`

It covers purpose/scope/non-goals, behaviour-not-identity, architecture, P0–P5, survival/capture, microstructure, liquidity, maker, cross-market, signatures, governance, OOD/disagreement/drift, runtime, all consumers, validation, parameters, Research/Future and external revalidation.

## Deep specs created

1. `01_OBJECTIVE_SCOPE_AND_FIDELITY_LADDER.md`
2. `02_EDGE_SURVIVAL_HAZARD_AND_CAPTURE.md`
3. `03_MICROSTRUCTURE_FEATURES_OFI_AND_MICROPRICE.md`
4. `04_LIQUIDITY_RESPONSE_REPLENISHMENT_AND_RESILIENCE.md`
5. `05_MAKER_FILL_QUEUE_AND_ADVERSE_SELECTION.md`
6. `06_CROSS_MARKET_RESPONSE_AND_CORRECTION.md`
7. `07_PARTICIPANT_SIGNATURES_AND_ADDRESS_BEHAVIOUR.md`
8. `08_MODEL_GOVERNANCE_VALIDATION_OOD_AND_FALLBACK.md`
9. `09_RUNTIME_INFERENCE_AND_CROSS_DOMAIN_CONTRACTS.md`

## Fidelity ladder reconstructed

`P0 Historical Participants → P1 Edge Survival → P2 Aggregate Response → P3 Cross Market → P4 Participant Signatures → P5 Interactive Research` is verified against SRC-007. P5 explicitly contains Queue-Reactive, Hawkes and ABIDES-like agents. Initial production cannot depend on P4/P5. Participant P-level and Simulator F-level are separate.

## Models classified

- Initial Champion direction: simple, interpretable, fast empirical survival; naive constant survival remains validation baseline.
- Production-capable learned candidate: discrete hazard.
- Locked interfaces/not calibrated: Liquidity Response, Maker Fill/Adverse Selection, sparse Cross-Market Response.
- Challengers: survival GBDT; later Queue-Reactive/Hawkes with adequate fidelity.
- Research/Future: deep survival, address clusters and explicit agent worlds; agents are stress scenarios, not production truth.

## Formula references checked

QF-028..035, 043..055, reference-only QF-058, QF-081..083, QF-085, QF-094..096 and QF-099..103 were reopened in SRC-004. No mathematical inconsistency was found. Nineteen missing Participant-index dependencies were restored. Several PASS 00 Formula Index expression summaries are text-extraction truncations; the exact source expressions are preserved in `PARTICIPANT_FORMULA_CROSSCHECK.md` and the global metadata repair remains PASS 11.

## Conflicts

Six source-evolution conflicts were resolved and registered: synthetic agents versus collective response; address versus identity; dense versus sparse response graph; complex versus simple-first models; Monte Carlo versus bounded Participant hot path; and random/live-adaptive learning versus temporal offline governance. No unresolved conflict blocks this domain.

## Open participant decisions

- `OPEN-008`: exact Champion/Challenger variants and coefficients.
- `OPEN-010`: exact survival/hazard horizons, strata, support and parameters.
- `OPEN-012`: maker/TM/MM activation with Execution/Risk.
- Calibrated/learned: feature windows/weights, sparse neighbours, response/fill horizons, OOD/drift methods, promotion thresholds and runtime budgets.

No idea was converted into an execution decision.

## External revalidation facts

`EXT-005`, `EXT-006`, `EXT-007` and `EXT-016` remain unverified source snapshots: feed cadence/fields/counterparties; node raw diffs/order lifecycle; L4/spot support; academic claims and transferability. No live external revalidation occurred. This does not block documentation, but can block data/fidelity/activation claims.

## Validation recovered

Temporal and walk-forward OOS, right-censor handling, calibration by horizon/support, Brier/Log Loss/integrated Brier, fill calibration, cross-market/address ablation, EconomicLift, ModelValue after latency/operations, OOD/disagreement/drift/fallback faults, Python/Rust parity, shadow and micro-live comparisons are specified. No numerical gate was invented.

## Legacy comparison

Legacy correctly captured the high-level direction but compressed the economic death definition, exact formulas, feed-fidelity boundaries, full model governance, cross-domain contracts and activation evidence. All source-supported gaps are recovered. Legacy-only untraced imports: **0**.

## Coverage gaps

- No missing PASS 02 topic or destination was found after no-loss search.
- Exact Data field schemas remain intentionally routed to PASS 06.
- Exact Simulator queue/counterfactual mechanics remain intentionally routed to PASS 03.
- Formula Index global extraction cleanup remains PASS 11.
- Risk/Execution/Sizing activation thresholds remain their owning passes and calibration.

## Repository boundaries

- Modified outside `docs_v2`: **0**.
- `docs/**`: unchanged.
- Source code, Cargo, Dockerfile and application configuration: unchanged.
- PASS 01 Infrastructure master/deep specs: unchanged.
- PASS 03: not started.

## Human-review questions

Human review should confirm the locked-interface/learned-model classification, the decision to preserve address modelling only at optional P4, and the cross-domain routing of Maker/Data/Simulator details. Approval for implementation is not implied.
