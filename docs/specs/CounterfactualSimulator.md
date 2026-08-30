# CounterfactualSimulator

## Purpose

Produire des distributions de scénarios plausibles sous intervention.
## Responsibilities

F0–F4 orchestration, latency sampling, response coupling, outcome aggregation/confidence.
## Non-responsibilities

Ne prétend pas reconstruire le futur exact.
## Inputs

Replay state, plan, manifest, latency/models/fidelity.
## Outputs

OutcomeDistribution and calibration evidence.
## Dependencies

ExchangeEmulator, ShadowBook, response engines, ClockAndRng, AccountingEngine.
## State

Per-run branch state, seed and manifests.
## Algorithms / formulas

QF-048..063/075..080; exogenous vs interactive modes.
## Invariants

Mechanical/response separation; no lookahead; fidelity honestly declared.
## Failure modes

Double consumption, branch inconsistency, model OOD, false certainty.
## Risk interactions

Provides EV/tails/confidence; cannot override hard gates.
## Performance requirements

Offline scalable; hot path uses precomputed summaries only.
## Metrics

Bias/calibration/tail coverage/runtime/scenario convergence.
## Persistence

RunManifest, scenarios/summaries and artifacts.
## Configuration

Fidelity, samples, horizon/rejoin and model versions.
## Tests

Determinism, golden F0/F1, decomposition, no-lookahead, convergence.
## Maturity requirement

F0/F1 M2; F2/F3 calibrated; F4 RESEARCH.
## Open calibrated parameters

Sample count, horizons, rejoin, response models/confidence.
