# CORR-03 — Model Selection Bias and Censoring Analysis

DOCUMENTATION STATUS: REQUIRED VALIDITY ANALYSIS

Actual fill labels exist only for candidates selected by the historical strategy, Risk, capital, sizing, market universe, latency and infrastructure policy. Therefore completion estimates are conditional on that policy. A Risk-rejected or unattempted candidate has no actual no-fill label; Simulator/Shadow evidence is counterfactual and remains separate.

Key biases and controls:

| Threat | Effect | Required control |
|---|---|---|
| policy selection | attempted set differs from detected opportunities | report funnel selection and deployment scope |
| maturity/censoring | recent cohorts contain more unresolved outcomes | cutoff/maturity tables; no `UNKNOWN=0` |
| q/capital scale | small probes overstate support for larger q | explicit q/size-depth support and `Q_validated` separation |
| infra/policy change | latency/selection distribution shifts | artifact provenance, drift/revalidation trigger |
| episode leakage | correlated observations cross train/test | chronological episode-aware boundaries |
| route memorization | apparent lift from repeated exact IDs | route/market holdout diagnostics where relevant |
| evidence gaps | guessed terminal labels bias results | `INVALID_EVIDENCE`; exclude from fit but report |

Changing markets, q, fees, execution mode, selection rules or infrastructure can invalidate calibration. Shadow may quantify opportunity-policy behavior but cannot repair missing actual fill labels.
