# PASS 03 — Simulator Source Crosscheck

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Locator audit

All **231** PASS 00 Simulator-index locators were reopened from the eight original files: 5,775 locator lines read; 0 empty/invalid ranges. Continuous SRC-008 lines 1–2620 were additionally read for reasoning context rather than headings alone. The Formula authority sections for all 42 referenced QFs and the SRC-005/SRC-006 contract blocks were reopened separately.

| Source | Indexed locators | Contribution reviewed | Authority/disposition |
|---|---:|---|---|
| SRC-001 | 23 | Replay/live parity, Recorder, latency replay, multi-size, Micro-live/scientific workflow | Supporting history; later closure wins. |
| SRC-002 | 13 | queue continuity, shared architecture, Rust Replay, fee centralization, future hardware | Supporting; rejected/future items preserved. |
| SRC-003 | 15 | Replay/production loop, test/prod synchronization, time testing, imperfect simulation | Supporting; Data/Risk closure wins. |
| SRC-004 | 7 indexed + 42 QF refs | execution/replay determinism, Simulator interface, authoritative math | Formula/Execution closure authority. |
| SRC-005 | 75 | Risk kill switches, transports, RunMode, determinism, clocks/RNG, SimulationMode/fidelity, rejoin/confidence, forecasts/manifests/hashes | Data/Risk/Replay closure authority. |
| SRC-006 | 42 | M0–M5, F0–F4 DoD, distributions/OOD, slicing, Replay/Shadow/Micro-live/release gates | Validation closure authority. |
| SRC-007 | 30 | survival/liquidity/maker/cross-market forecasts, Monte Carlo ownership, research models | PASS 02/SRC-007 Participant semantics. |
| SRC-008 | 26 | exact-world limitation, three layers, arrival/mechanics, incompatibility, response, queue bounds, branches, confidence, fidelity, calibration | Primary detailed Simulator source. |

## Primary-source reasoning recovered

SRC-008 explicitly establishes that perfect pre-intervention book knowledge still cannot reveal how every other participant would have responded. The scientific target is a calibrated plausible distribution. It distinguishes deterministic exchange mechanics, historical interference/compatibility, and probabilistic response; requires execution at `t_arrival`; confines direct mechanical mutation to the traded market; and explains why a changed book can make later cancels/trades incompatible.

It specifies `ExogenousReplay` and `InteractiveCounterfactual`, a Conditional Empirical response baseline before Queue-Reactive/Hawkes, aggregate participant flow before explicit agents, sparse cross-market response, three L2 queue modes, scenario PnL/tails, size-dependent confidence/capacity, temporal fragmentation/resilience, branch-and-rejoin, F0–F4, and Predicted-versus-Actual Micro-live calibration.

## Closure crosscheck

- SRC-004 replaces earlier formula variants and supplies exact mechanics, survival/fill, EV/tail, recovery, cross-market, latency, and confidence semantics.
- SRC-005 prevents hidden Replay/Live forks and fixes serialized mode/fidelity names, events, clocks/RNG, manifests, trace/hashes, and decomposed confidence.
- SRC-006 prevents architecture-only claims from becoming validation: F1 mechanics, F2 queue, F3 response, and F4 Research have distinct evidence.
- PASS 02 prevents duplicate Participant models: forecasts are inputs, Monte Carlo/branching remain Simulator-owned.

## Conflicting/superseded source evolution

Naive exact historical continuation, mechanical mutation of every triangle book, one deterministic future, complex-agent/Hawkes-first design, exact L2 queue, and fixed rejoin horizon are not canonical. The final sources either reject them explicitly or constrain them as Research/calibrated assumptions.

## External material

Source hyperlinks and claims were treated as historical source snapshots. No web query was made. Current exchange/order/feed/L4 facts and academic transferability remain in the External Revalidation Register.
