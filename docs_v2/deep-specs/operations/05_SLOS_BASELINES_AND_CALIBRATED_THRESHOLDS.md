# 05 — SLOs, Baselines and Calibrated Thresholds

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

SLOs cover correctness/readiness, not merely uptime: Feed/Book validity, account reconciliation, decision integrity, execution safety, Recovery, Recorder/evidence, latency distributions, model/Simulator calibration, Risk enforcement and deployment/security authority.

Each SLO declares indicator/event population, numerator/denominator, scope, missing/invalid handling, window, target/error budget, measurement version, owner and breach action. Hard Risk, no-duplicate-effect, no-unknown-capital-reuse, single-owner and secret boundaries have no spendable error budget.

Baselines come from valid comparable measurements with count, distribution and regime. Threshold provenance is exchange rule, safety default, user tightening or calibrated evidence; magic constants are forbidden. Recovery thresholds use hysteresis and often reconciliation.

Error-budget review may slow promotion or demote a capability. It never authorizes continuation across a hard safety failure. A process may meet uptime while failing every economically relevant SLO.
