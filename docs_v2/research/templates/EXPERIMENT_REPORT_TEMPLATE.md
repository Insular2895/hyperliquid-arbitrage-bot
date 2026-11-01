---
artifact_type: experiment_report
experiment_id: EXP-XXXX
title: UNSET
version: 1
status: PLANNED
hypothesis_ids: []
strategy_ids: []
strategy_versions: []
strategy_family: UNSET
dataset_ids: []
run_ids: []
evidence_ids: []
created_at: YYYY-MM-DDThh:mm:ssZ
owner: UNSET
reviewer: UNSET
producer: HUMAN_OR_GENERATOR
machine_facts_hash: UNSET
supersedes: null
---

# Experiment Report — EXP-XXXX

## Machine-populated facts — immutable after generation

- Git commit, build/image, ConfigVersion, FormulaVersion and model versions:
- Fee/Metadata/Book/Graph/Replay/Simulator/feature versions:
- DatasetId/hash/split, RunManifest/RunMode/ReplayMode/fidelity/FALSIFIER_T*, InfraProfileId and FeedProfileId:
- protocol/config-space hash; temporal splits; population; Structure/class/mode/intent; market/route/regime scope:
- deterministic job/config ordinals, exact config hashes, seed tree, budget and stopping rule:
- sample and attempt counts; clock/data validity; missingness; failures; censoring; duplicates/manual reruns; invalid runs:
- primary/secondary/guardrail metrics, uncertainty, tails and artifact hashes:

## Hypothesis, rationale, falsifier and expected outcome

## Baseline, treatment and controlled change

- exact changed variable:
- explicitly unchanged variables:
- unavoidable compound changes and attribution limit:

## Method, stop/decision rules and leakage/multiplicity controls

- protocol frozen before any data-dependent T0:
- parameter domains, selection/region rules and decision boundaries:
- T2 plan and final untouched holdout access policy:
- deterministic result order independent of worker completion:

## Results, sensitivity, OOS and stress evidence

- Discovery versus validation-supported versus final robust maturity:
- OOS/walk-forward/T2/final holdout result and access audit:
- zero/partial/full/Recovery populations; actual/replay/simulated provenance:

## Failures, contradictions and negative evidence

- compute failures/timeouts versus scientific/economic failure:
- invalid/unsupported/censored/negative/duplicate/manual-rerun/later-invalidated outcomes:

## Economic and operating-cost impact

## Human/AI interpretation

Classify every material claim: `FACT`, `MEASURED`, `DERIVED`, `MODELLED`, `COUNTERFACTUAL`, `HYPOTHESIS`, `INTERPRETATION`, or `DECISION`.

## Limits, next experiment and linked artifacts

## Disposition and required approval

`PROMOTE`, `REJECT`, `HOLD`, or `INCONCLUSIVE`; none grants Live/Risk permission by itself.

For documentary clarity, `PROMOTE` means “forward for separate review,” never automatic capability
promotion.
