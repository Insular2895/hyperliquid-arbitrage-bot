# InfrastructureMonitor

## Purpose

Mesurer santé et latence du système sans polluer le hot path.
## Responsibilities

Stage timings, resource/network/clock/storage health, SLO/alerts.
## Non-responsibilities

Ne sélectionne pas un fournisseur et ne modifie pas risk limits seul.
## Inputs

Instrumentation events, OS/container/network/recorder metrics.
## Outputs

Health snapshots, latency distributions and alerts.
## Dependencies

ClockAndRng, Recorder, Deployment.
## State

Rolling bounded histograms/windows and alert latches.
## Algorithms / formulas

QF-084/090/092; quantiles correctly aggregated.
## Invariants

Critical metric loss visible; liveness≠readiness≠trading health.
## Failure modes

Metric backpressure, clock error, cardinality explosion, false health.
## Risk interactions

Critical health controls readiness/kill; telemetry outage conservative.
## Performance requirements

Nonblocking emission, bounded cardinality/storage.
## Metrics

Defines metrics in doc 18 plus own loss/lag.
## Persistence

Time series/incidents/manifests without secrets.
## Configuration

Windows/SLO/alerts calibrated and versioned.
## Tests

Metric loss/load/clock/cardinality/alert action and redaction.
## Maturity requirement

M2 replay/load; M3 shadow; M4 alert drills.
## Open calibrated parameters

SLO thresholds/windows/export backend.
