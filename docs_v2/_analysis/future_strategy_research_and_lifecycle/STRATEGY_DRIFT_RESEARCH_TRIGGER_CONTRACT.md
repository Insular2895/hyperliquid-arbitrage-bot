# Strategy Drift and Research-Trigger Contract

Drift classes include input/data, feature/support, market/regime, execution/completion, calibration, economic, infrastructure, schema/external-fact and operational drift.

Each detector declares population, window, baseline, uncertainty, minimum support, hysteresis, severity, owner and failure behavior. Thresholds are calibrated rather than invented. A trigger creates evidence and can reduce scope, demote to a supported artifact, mark NON-READY or open research. It cannot change q, Risk, capital, features or model parameters in place.

Actual outcomes remain reconciliation-derived. Drift research is activated only after the baseline and reporting pipeline, and after Champion/Challenger mechanics exist; it is the last strategy layer. Full details: [Drift and Research Triggers](../../deep-specs/strategy-research/10_DRIFT_AND_RESEARCH_TRIGGERS.md).
