# Participants, Simulator and Models Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## What is modelled

Production models describe collective observable behavior: opportunity-edge survival, replenishment/resilience, competition intensity, maker fill/time/adverse selection and sparse cross-market response. Public data does not justify fabricated competitor identities. Explicit agents are an F4 Research construction, not production truth.

## Fidelity ladder

| Fidelity | Meaning | Initial status | Capital consequence |
|---|---|---|---|
| F0 | historical replay-compatible outcome baseline | build first | no direct permission |
| F1 | latency/mechanical perturbations | build first | no direct permission |
| F2 | queue/fill model with calibrated support | later evidence-gated | may only narrow/qualify supported maker scope |
| F3 | aggregate responsive market behavior | later evidence-gated | may only affect supported scope |
| F4 | interactive agents/worlds | Research | no production authority |

Counterfactual output is a reproducible distribution of plausible outcomes, not an exact alternate universe. Historical compatibility, the mechanical effect of our action and modeled market response remain separately labelled. Unsupported or OOD slices reduce confidence and permission.

## Model governance

Start with transparent empirical baselines. A Champion must beat a naive baseline under temporal walk-forward/OOS evaluation, be calibrated on supported horizons/strata, show stable operational runtime and positive `EconomicLift` after decision costs. Challengers—GBDT, Hawkes, Queue-Reactive, deep survival or richer response models—run without authority until they meet the same promotion bar.

Every forecast carries artifact/version, horizon, support, confidence/OOD, source-state versions and fallback. Drift, disagreement or missing support causes fallback/rejection/demotion, never increased capital.

TT detection, Replay, Shadow and a bounded TT evidence chain do not require F4 or sophisticated Participant models. A Participant artifact is a hard dependency only for a manifest that consumes it. F4 must not block initial TT.
