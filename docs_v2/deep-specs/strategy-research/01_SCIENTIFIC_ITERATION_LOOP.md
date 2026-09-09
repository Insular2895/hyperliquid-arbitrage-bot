# 01 — Scientific Iteration Loop

STATUS: FUTURE SPECIFIED / NOT ACTIVE / HUMAN REVIEW PENDING

## Canonical loop

`OBSERVE -> UNDERSTAND -> HYPOTHESIZE -> TEST -> MEASURE -> VALIDATE -> PROMOTE -> MONITOR -> DEMOTE OR RESEARCH`

| Step | Required output | Forbidden shortcut |
|---|---|---|
| Observe | immutable Dataset/Run/Evidence links and declared support | treating a dashboard impression as fact |
| Understand | separated FACT, MEASURED, DERIVED and INTERPRETATION claims | hiding missingness or censoring |
| Hypothesize | `HYP-*`, causal story, falsifier, scope and expected failure modes | tuning before a falsifiable claim |
| Test | predeclared `EXP-*`, frozen split, configuration, seed and stopping rule | moving the goalpost after results |
| Measure | deterministic machine-populated facts plus uncertainty | deleting negative or failed runs |
| Validate | temporal OOS, walk-forward where applicable, sensitivity, multiple-testing controls | selecting on the final holdout |
| Promote | explicit human-controlled evidence decision to a versioned artifact | automatic or AI-only promotion |
| Monitor | support, outcomes, drift, safety and evidence freshness | silent online self-modification |
| Demote/research | safe fallback, scope contraction, incident/research trigger | mutating Live thresholds in place |

Observation, hypothesis, simulation, validation, authorization, actual execution and accounting remain separate layers. A research artifact can inform a candidate; it cannot authorize Risk, capital, q, an execution command or Live state.

## Controlled experiment rule

An experiment freezes baseline, treatment, the exact changed variable, what is held constant, Dataset/population/regime, primary/secondary metrics, guardrails, clock/data validity, support, expected result, stop rule and decision rule. Change one causal variable where practical. A necessary compound operational change is allowed only when labelled non-attributable or decomposed by later experiments.

## Failure decomposition

“The bot is not profitable” is not a diagnosis. Evidence must locate at least one typed cause: invalid opportunity; BBO reject; exact-L2 reject; Risk reject; q zero; Reservation failure; opportunity expired before send; send/arrival delay; exchange reject; zero fill; partial fill; later-leg failure; Recovery; negative realized PnL; infrastructure instability; account/Reconciliation problem; or model/support/OOD problem. The Capture Funnel and actual-outcome lineage turn each cause into a testable hypothesis without collapsing populations.

## Claim classes

Every material statement is exactly one of `FACT`, `MEASURED`, `DERIVED`, `MODELLED`, `COUNTERFACTUAL`, `HYPOTHESIS`, `INTERPRETATION`, or `DECISION`. It carries provenance, author/producer, timestamp, version, support and uncertainty where relevant. `DECISION` requires its named authority; AI output defaults to `HYPOTHESIS` or `INTERPRETATION`.

## Baseline-first gate

Research orchestration remains `DEFERRED_BLOCKED` until all prerequisites in the directory README are evidenced. Documentation and inert templates may exist earlier. Search jobs, strategy portfolios, Champion/Challenger automation, drift-driven selection and capital-bearing trials may not.

## Failure semantics

Invalid, aborted, inconclusive, censored, negative and contradicted outcomes are first-class. Their records are append-only; corrections supersede with lineage. A failed experiment can close a hypothesis, narrow its scope, expose an instrumentation fault, or require an incident. It is never erased to improve the apparent record.
