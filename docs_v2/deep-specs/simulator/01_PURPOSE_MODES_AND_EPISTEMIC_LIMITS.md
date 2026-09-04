# 01 — Purpose, Modes, and Epistemic Limits

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Contract

The Simulator estimates how a candidate execution could distribute fills, partials, recovery, and PnL under declared assumptions. It cannot reconstruct the exact alternate world: after our hypothetical action, observed history may be incompatible and unobserved participant reactions are unknowable. Its valid claim is a **plausible distribution calibrated against supported historical, Shadow, and Micro-live evidence**.

The three non-collapsible layers are Exchange Mechanics, Historical Compatibility, and Market Response. Deterministic mechanics are applied before stochastic response.

## The three axes

| Axis | Values | Meaning |
|---|---|---|
| `RunMode` | `Replay`, `Paper`, `Shadow`, `MicroLive`, `Live` | Event source, execution transport, and declared environment. |
| `SimulationMode` | `ExogenousReplay`, `InteractiveCounterfactual` | Whether future market data remains external or a response branch is modeled. |
| `ReplayFidelity` | `F0Historical` … `F4Interactive` | Which mechanics/models are active. |

These axes never imply one another. Participant P0–P5 and validation M0–M5 are two additional, separate classifications.

## Exogenous versus interactive

`ExogenousReplay` preserves historical future data and changes only our simulated fills/account consequences. It is a strong baseline for small interventions and deterministic comparison, with no feedback claim.

`InteractiveCounterfactual` applies `HistoricalBaseline + Δour + Δresponse`, detects branch incompatibility, and samples calibrated local/cross-market response. It is appropriate when participation, queue, response, or cross-market divergence matters. It is still not exact reality.

## Replay, Shadow, Counterfactual, Micro-live

- Replay uses recorded events and `ReplayClock`.
- Shadow uses live events and `NullShadowTransport`; it cannot validate our actual impact.
- Counterfactual adds a simulated intervention to recorded/live-derived state.
- Micro-live sends real small orders under strict Risk configuration to calibrate intervention effects.

## Non-goals and research boundary

No exact competitor identities, exact queue from L2, deterministic one-path future, unlabelled mixing of modes, arbitrary response noise, or automatic sizing decision. Hawkes, Queue-Reactive, deep models, and explicit agents remain governed Challengers/Research. They can support stress and sensitivity; they are not truth by construction.

## Failure semantics

Unsupported data/fidelity/model support produces explicit `LOW`, `OOD`, or `REJECT`, never optimistic extrapolation. A result always declares mode, fidelity, data/model/config/formula versions, seed, confidence causes, and known limitations.

## Authority

SRC-005 fixes mode/provenance semantics; SRC-008 fixes the epistemic correction and simulator decomposition; SRC-006 fixes evidence maturity. Exact schemas remain PASS 06.
