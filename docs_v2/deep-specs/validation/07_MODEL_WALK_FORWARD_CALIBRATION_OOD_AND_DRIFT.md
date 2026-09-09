# 07 — Model Walk-forward, Calibration, OOD and Drift

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Random row splits are forbidden for temporal market data. Use chronological train/validation/test and repeated walk-forward windows. Slice later regimes, new assets, volatility/liquidity, size/depth, feed mode, horizons and censoring. Point-in-time feature neighbourhoods are mandatory.

The initial Champion must beat a naive constant-survival baseline OOS. Report Brier, LogLoss, integrated Brier/survival calibration as applicable, calibration curves, ranking support, EconomicLift after identical costs/capital/Risk, drawdown/CVaR/partials/Recovery loss and runtime. Advanced features need ablation.

OOD includes unsupported market, size, regime, horizon, feed fidelity, feature age and latency. Invalid/corrupt/unavailable/NaN, OOD, disagreement and drift invoke conservative fallback, smaller size or reject/disable. No high-confidence extrapolation is allowed.

Champion affects decisions; Challenger is observe-only. A new model has its own DatasetId/artifact/provenance/evidence and never inherits promotion. Production collects outcomes; training/recalibration is offline. Supported persistent live contradiction outranks Replay; isolated outcomes do not establish drift alone.

## CORR-05 economic consumer contract

Completion/survival calibration updates or selects the Simulator outcome distribution; it does not create an independent expected-value multiplier. QF-102 disagreement, QF-103 OOD and QF-104 confidence govern support/uncertainty. Demotion selects only a versioned supported fallback and may contract `Q_validated`; no silent favorable fallback or online self-modification is allowed.
