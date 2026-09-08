# CORR-03 — Completion Model Champion / Challenger Policy

DOCUMENTATION STATUS: OFFLINE MODEL GOVERNANCE

Order of evidence:

1. compatible-scope constant resolved completion rate;
2. transparent hierarchical empirical baseline;
3. optional GBDT or other Challenger;
4. deep/survival/queue-reactive/Hawkes only in the domain and horizon they actually model.

The simple baseline remains Champion/reference unless a Challenger shows robust chronological OOS improvement in calibration, relevant discrimination, QF-100 economic utility when decision-affecting, runtime, stability and OOD/fallback without safety regression. AUC or in-sample accuracy alone is insufficient.

Runtime records P50/P95/P99/P99.9 inference latency, allocation, CPU/cache and batching assumptions under CORR-02 attribution. Production inference is local/Rust-compatible; no synchronous remote model service is permitted on the decision path. Python may prepare data/train/evaluate/artifacts but does not own Live decisions.

Runtime records new evidence only. Weights change offline through versioned candidate artifact, validation and explicit promotion. Drift may demote; no live self-modifying weights or automatic promotion exists.
