# PASS 03 — Counterfactual Simulator Final Report

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Scope and result

PASS 03 rebuilt the Counterfactual Simulator from the original eight-source corpus. The canonical specification explicitly rejects exact alternate-world claims and defines one progressively activated Simulator that combines historical reality, exchange mechanics, arrival latency, our intervention, calibrated response, queue uncertainty, multi-market response, recovery, risk distributions, confidence, and reproducibility.

## Review totals

- Simulator requirements reviewed: **271 unique**.
- PASS 00 Simulator-index requirements: **231/231**.
- Additional unique Formula requirement dependencies: **40**.
- Formula references checked: **42 QFs**.
- Original source sections reopened: **231 locators**, **5,775 locator lines**, `YES` 271/271 including formula dependencies, `NO` 0.
- Original sources reopened: **8/8**.
- Continuous primary context: SRC-008 lines **1–2620** plus its indexed later cross-domain locators.
- Requirements canonicalized/routed: **231 indexed dispositions + 40 recovered dependencies**; destinationless 0; renumbered 0.
- PASS 00 status corrections: **15 requirement IDs** receive PASS 03 reviewed overlays; original status metadata remains traceable.

## Sources and authority

- SRC-008: primary detailed Simulator reconstruction.
- SRC-004: authoritative Formula and Execution definitions.
- SRC-005: authoritative Data/Risk/Replay contracts, modes, determinism, fidelity, rejoin, confidence, and forecast semantics.
- SRC-006: authoritative validation maturity and F0–F4 DoD.
- SRC-007/PASS 02: authoritative Participant forecast boundaries.
- SRC-001–003: supporting historical requirements where uncontradicted.
- Legacy `/docs`: comparison only, read after V2 reconstruction.

## Canonical architecture recovered

The first rule is: **we cannot reconstruct the exact alternate world**. The Simulator produces a calibrated plausible distribution. Exchange Mechanics, Historical Compatibility, and Market Response are distinct layers. Mechanical Impact is local to the traded book; `World_cf = HistoricalBaseline + Δour + Δresponse` preserves known intervention versus modeled reaction.

## Simulation modes reconstructed

- `ExogenousReplay`: historical future remains externally given; own fills/inventory/economics change; no feedback claim.
- `InteractiveCounterfactual`: explicit branch with mechanical, queue, calibrated local/cross-market response and rejoin/non-rejoin semantics.
- `RunMode`, `SimulationMode`, and `ReplayFidelity` are independent and recorded.

## Fidelity F0–F4 reconstructed

`F0Historical → F1LatencyMechanical → F2Queue → F3Responsive → F4Interactive` is verified against SRC-005/006/008. F4 remains Research. Higher fidelity never implies higher confidence or capital authority.

## Queue models reconstructed

L2 queue uncertainty is explicit:

- `PESSIMISTIC`: cancellations never advance `queue_ahead`;
- `OPTIMISTIC`: all same-level cancellations are favourable, as upper-bound sensitivity only;
- `PROBABILISTIC`: calibrated state-conditional cancellation/flow allocation.

Maker outputs include fill survival/CDF, time/quantity/partial distributions, cancellation, adverse selection, second-leg, and recovery outcomes. L4 compatibility is retained without assuming current spot availability.

## Counterfactual branch semantics reconstructed

Historical incompatibility is detected rather than clamped away. Branch-and-rejoin uses an explicit `CounterfactualRejoinEvent`, calibrated variable horizon, compatibility/confidence evidence, and a valid non-rejoin/conservative outcome. No universal rejoin time is invented.

## Formula references checked

QF-009–016, 026/027, 040–063, 076, 079–082, 084/085, and 104 were reopened (**42**). Adjacent QF-007/008, 083, and 094–103 were routed as dependencies. No authoritative mathematical contradiction was found. PASS 00 expression-summary truncation and full unit/metadata audit remain PASS 11.

## Data and determinism recovered

Same core/different transport, deterministic receive-time order/no look-ahead, `ReplayClock`, `TimerEvent`, seeded `RngProvider`, `RunManifest`, `DecisionTrace`, state hashes, point-in-time artifacts, explicit mode/fidelity, immutable snapshots, and stale-worker rejection are specified. Exact schema implementation remains PASS 06.

## Validation rules recovered

The validation map covers **13 capability rows**: latency, taker mechanics, partial fills, queue, maker fill, adverse selection, liquidity response, cross-market response, recovery, PnL distribution, VaR/CVaR, confidence, and branch/rejoin. M0–M5, temporal OOS, Golden/Replay/Shadow/Micro-live, Predicted-versus-Actual, distribution coverage, Champion/Challenger, OOD/drift, live-evidence precedence, and Simulator Calibration Kill Switch interfaces are restored without numerical thresholds.

## Conflicts

- Conflicts found/reviewed in PASS 03: **8** (`CONFLICT-010`, `CONFLICT-017`–`023`).
- Conflicts resolved: **8**.
- Conflicts remaining: **0 blocking**.
- Resolutions cover exact-world/continuation, local multi-market mechanics, distribution output, empirical-first response, L2 queue uncertainty, variable rejoin, and live-evidence precedence.

## Open and calibrated decisions

No new permanent architecture question was created. Relevant existing opens remain `OPEN-004`, `OPEN-007`, `OPEN-008`, `OPEN-010`, and `OPEN-012` under their owning passes. Rejoin rule, probabilistic queue allocation, response estimator/horizons, scenario count/dependence, confidence thresholds, size grid, and calibration tolerances remain `CALIBRATED / LEARNED`, not falsely locked.

## Cross-domain requirements routed

Formula/PASS 11; Data/Replay/PASS 06; Execution/Recovery/PASS 04; Risk/PASS 05; Sizing/Slicing/PASS 07; Graph/PASS 08; Participant forecasts/PASS 02. Cross-domain gaps: **0 blocking**. These deliberate ownership boundaries are explicit and do not require an engineer to invent Simulator semantics.

## External revalidation facts

Current Hyperliquid price-time priority, IOC/ALO/GTC, block/action ordering, feed timestamps/sequences/L2 granularity, precision/fees/API schemas, L4 availability, and `order_book_server` spot support remain unverified snapshots (`EXT-001/002/004/005/007`). Academic claims/transferability remain `EXT-016`. External web revalidation performed: **0**.

## Artifacts

- Master created: `docs_v2/07_COUNTERFACTUAL_SIMULATOR.md`.
- Deep specs created: **12 plus README** under `docs_v2/deep-specs/simulator/`.
- PASS 03 analysis artifacts created: **9**, including this report.
- PASS 00/README overlays updated: **8 existing files** under `docs_v2`.
- Files modified outside `docs_v2`: **0**.

## Legacy comparison

Legacy correctly captured the headline limitation, pipeline, two modes, F0–F4 and compact distributions, but over-compressed the three layers, incompatibility policy, response Champion, aggregate participants, queue modes, resilience, fragmentation, rejoin/non-rejoin, Data provenance and capability validation. All source-supported omissions are recovered. Legacy-only untraced imports accepted: **0**. Legacy files modified: **0**.

## Coverage

- Required no-loss concepts present in canonical master/deep specs: **all; missing 0**.
- Required master sections: **32/32**.
- Required deep specs: **12/12**.
- Required analysis files: **9/9**.
- Final-success questions answerable from `docs_v2`: **55/55**, subject to human review.
- Intentional future-pass details: exact Data schema fields, Execution/Recovery transitions, Risk thresholds, Sizing policy, Graph construction, and Formula metadata/unit audit.

## Boundary

- Source code, Cargo, Dockerfile, application config: unchanged.
- `docs/**`: unchanged.
- PASS 01 and PASS 02 canonical masters/deep specs: unchanged.
- PASS 04 started: **NO**.

## Gate

PASS 03 COMPLETE

BUT

HUMAN REVIEW REQUIRED

No implementation or capital activation is approved by this report.
