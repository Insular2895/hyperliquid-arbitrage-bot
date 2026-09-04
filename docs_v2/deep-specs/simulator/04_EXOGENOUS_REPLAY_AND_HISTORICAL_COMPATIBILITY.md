# 04 — Exogenous Replay and Historical Compatibility

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## The incompatibility problem

Recorded future events describe the world without our hypothetical order. After `Δour`, a trade may consume already-removed liquidity, a cancel may exceed the branch quantity, or an update may assume an impossible queue/order state. Applying all events blindly can produce negative depth and counterfeit certainty.

## `ExogenousReplay`

In `SimulationMode::ExogenousReplay`, historical future market data stays unchanged/external. Our simulated action affects our fills, fees, inventory, recovery, and PnL, but not subsequent market data. This yields a reproducible baseline for small-order, latency, mechanics, and model-ablation studies.

The mode means **feedback omitted**, not “impact proven zero.” Each result states participation/support, fidelity, and the approximation limit.

## Baseline and event policy

The raw/normalized historical stream is immutable. For each future event, the simulator records whether it:

1. applies to the untouched baseline;
2. is representable against the local branch delta;
3. conflicts with branch state;
4. is ignored/reconciled only under an explicit versioned mode rule; or
5. invalidates the branch/result.

No generic clamp-to-zero may masquerade as reconciliation. Exact event/reconciliation fields remain PASS 06; exact fill/order conflicts remain PASS 04.

## Appropriate and inappropriate uses

Appropriate: small participation inside validated support; `t_arrival`/book-walk calibration; deterministic regression; comparison against F1/F3. Inappropriate: material intervention where response/queue/cross-market divergence drives the result, or a branch with repeated incompatibility.

## Fidelity and provenance

Exogenous mode can support F0 historical and F1/F2 mechanics/queue approximations when explicitly defined. It cannot claim F3 participant feedback. Mode, fidelity, dataset regions, event order, config/model/formula versions, seed, and compatibility diagnostics are recorded.

## Invalid data

Recorder gaps, corrupt order, bad checksums, unknown fee/precision state, or invalid book regions are excluded or fail the run under PASS 06 policy. Historical continuity is not evidence if the input region is invalid.
