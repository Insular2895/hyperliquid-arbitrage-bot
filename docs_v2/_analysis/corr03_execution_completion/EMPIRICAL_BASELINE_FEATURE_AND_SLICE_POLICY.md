# CORR-03 — Empirical Baseline Feature and Slice Policy

DOCUMENTATION STATUS: CANDIDATE FEATURE POLICY

## Initial minimum

Start with strategy family + execution mode and a coarse size/depth representation where support permits. Keep `OWA+TT` and `Triangle+TTT` separate. Add route family, liquidity/regime or latency bands only when predeclared temporal OOS evidence demonstrates enough support and useful calibration.

Candidate decision-time features include q, q/executable-depth, spread, exact edge, edge age, depth/slope, imbalance/microprice/OFI, volatility/jump regime, participant survival, predicted latency/arrival, infrastructure profile, time/regime and `SimulationConfidence`. They are candidates, not a required initial 100-feature model.

Exact RouteId/MarketId can overfit sparse history. They enter only with stable support and broader fallback. New route/market/size/latency/infra/mode is OOD or uses a validated broader prior. Actual ACK/fill latency, fills, post-send books, Recovery and PnL are forbidden decision-time inputs.

Feature availability and versions follow `DECISION_TIME_FEATURE_SNAPSHOT_CONTRACT.md`. Any feature addition requires point-in-time reconstruction, missingness behavior, runtime measurement and revalidation.
