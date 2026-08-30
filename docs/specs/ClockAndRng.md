# ClockAndRng

## Purpose

Centraliser temps et hasard pour déterminisme et mesure correcte.
## Responsibilities

Wall/monotonic/simulated clocks, exchange mapping, seeded RNG and manifests.
## Non-responsibilities

Ne corrige pas silencieusement une horloge host défaillante.
## Inputs

Host/exchange timestamps or Replay scheduler; seed/algorithm.
## Outputs

Typed times/durations/random draws and ClockHealth.
## Dependencies

Host time service; Recorder.
## State

Offsets/quality, replay time, RNG state/version.
## Algorithms / formulas

Monotonic durations; explicit mappings and deterministic PRNG.
## Invariants

No direct time/random in core; same manifest same draws/order.
## Failure modes

Clock jump/drift, overflow, timezone misuse, unseeded randomness.
## Risk interactions

Clock unhealthy disables new risk; uncertainty enters latency confidence.
## Performance requirements

Cheap local reads; no sync network lookup in hot path.
## Metrics

Offset/drift/jumps/read latency and seed/version.
## Persistence

Clock anomalies/mappings and RunManifest RNG details.
## Configuration

Source/health thresholds calibrated; timezone output not business logic.
## Tests

Frozen/advanced/jump clocks, deterministic seeds, concurrent ordering.
## Maturity requirement

M1 prerequisite; M2 deterministic replay; M3 clock monitoring.
## Open calibrated parameters

Health/drift thresholds and sync implementation.
