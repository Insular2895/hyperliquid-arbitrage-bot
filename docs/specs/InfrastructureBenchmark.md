# InfrastructureBenchmark

## Purpose

Comparer plateformes/réseaux/container avec une méthode reproductible.
## Responsibilities

Run manifest, controlled probes, first-arrival/RTT/jitter/CPU/disk/feed measurements.
## Non-responsibilities

Ne trade pas et ne choisit pas sur ping seul.
## Inputs

Candidate environment, identical probe/config/window definitions.
## Outputs

BenchmarkReport with raw distributions/confidence.
## Dependencies

InfrastructureMonitor, FeedAdapter, Recorder, ClockAndRng.
## State

Per-run samples and environment manifest.
## Algorithms / formulas

QF-084..087; paired/controlled comparisons when possible.
## Invariants

Comparable universe/config; clock quality declared; no hidden tuning.
## Failure modes

Regime mismatch, insufficient sample, clock skew, provider throttling.
## Risk interactions

No live promotion without stability/security checks.
## Performance requirements

Must not share resources with live trading unless explicitly safe/read-only.
## Metrics

All latency tails, loss/reconnect, CPU/scheduler, disk/recorder/container overhead.
## Persistence

Raw samples/report/environment hashes.
## Configuration

Duration/warmup/probes/candidates versioned.
## Tests

Synthetic latency, reproducibility, clock failure and report integrity.
## Maturity requirement

M2 tool; production decision needs repeated evidence.
## Open calibrated parameters

Duration/sample/support and candidate list.
