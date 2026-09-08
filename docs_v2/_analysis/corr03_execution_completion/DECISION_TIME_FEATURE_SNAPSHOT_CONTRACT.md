# CORR-03 — Decision-Time Feature Snapshot Contract

DOCUMENTATION STATUS: POINT-IN-TIME / ANTI-LEAKAGE CONTRACT

## Freeze boundary

The immutable snapshot is frozen after final pre-send revalidation and immutable plan basis, and before the first possible risk-increasing transport effect. It is joined to the exact `ExecutionForecast` used by the decision. A legitimate pre-send replan creates a new version; post-send mutation cannot rewrite history.

## Required lineage

`DecisionTimeFeatureSnapshot` (under existing schema-version governance) references ExecutionPlanCandidate/Execution/Opportunity, ordered availability cutoff, book versions, route/graph version, fee/metadata/precision versions, strategy/mode/q, size-depth context, participant forecasts/models, Simulator/fidelity/seed, Risk context/decision, latency/infra profile, Formula/Config/FeatureSchema versions, artifact versions, issue/valid-until times and missing/OOD/support state.

Every feature identifies source events, event/receive availability time, transformation/version and units. Reconstruction must prove no event with later receive time was visible.

## Forbidden decision-time inputs

Actual fills, ACK/fill/route-completion latency, Recovery result, post-send book movement, future volatility/price, final PnL and reconciled outcome are labels or diagnostics. Predicted arrival latency/state may be used; realized arrival evidence may evaluate it but cannot be inserted retrospectively. A rebuilt post-outcome feature vector is `COUNTERFACTUAL_MODEL`, never the frozen prediction input.
