# CORR-03 — Empirical Baseline Fallback Policy

DOCUMENTATION STATUS: CONSERVATIVE FALLBACK CONTRACT

The requested estimate uses the most specific validated slice with adequate support. Otherwise it walks a versioned hierarchy toward broader compatible strategy/mode/size-depth/regime scopes. If no supported level exists, return `OOD/INSUFFICIENT_SUPPORT`; never fabricate an exact-route probability.

Every output reports selected level, support counts, interval, reason and artifact version. Fallback cannot cross TT/TTT or taker/maker boundaries, capital/size support, materially different infra regimes or incompatible label versions without explicit validation.

Permissible final actions remain: broader validated empirical prior, existing conservative Simulator fallback, or no prediction influence. Missing prediction is `MISSING_PREDICTION`, not zero; missing actual is `UNRESOLVED`, not zero. Absence of model support never grants permission to trade. Exact support thresholds and smoothing are calibrated and promoted offline.
