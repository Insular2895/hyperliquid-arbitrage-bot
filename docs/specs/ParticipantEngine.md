# ParticipantEngine

## Purpose

Fournir contexte de réponse agrégée et signatures pseudonymes validées.
## Responsibilities

Feature assembly, champion/challenger inference, OOD/agreement and artifact loading.
## Non-responsibilities

Ne revendique aucune identité et ne simule pas des agents comme vérité.
## Inputs

Point-in-time microstructure, trades, optional addresses, model artifact.
## Outputs

ParticipantResponseContext with confidence/provenance.
## Dependencies

OFIEngine, VolatilityEngine, Recorder, ClockAndRng.
## State

Approved model/version and bounded online summaries.
## Algorithms / formulas

Aggregate statistical inference; QF-102/103 confidence inputs.
## Invariants

Address≠identity; no unsupported feature; fallback conservative.
## Failure modes

OOD, drift, model NaN, feature mismatch, privacy leakage.
## Risk interactions

LOW/REJECT blocks dependent capability, never hard safety.
## Performance requirements

Small bounded Rust inference; training offline.
## Metrics

Calibration/lift/OOD/disagreement/latency/feature coverage.
## Persistence

Model/feature/schema manifests and predictions.
## Configuration

Champion version, enabled feature groups, fallback.
## Tests

Feature parity, OOS, model corruption/NaN, latency and privacy.
## Maturity requirement

M2 offline; M3 observe; decision after lift; agents research only.
## Open calibrated parameters

Champion class, clusters, OOD and promotion gates.
