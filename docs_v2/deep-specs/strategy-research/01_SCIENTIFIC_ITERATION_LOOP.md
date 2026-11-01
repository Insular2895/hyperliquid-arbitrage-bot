# 01 — Scientific Iteration Loop

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / NOT ACTIVE`

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

For a Bounded Falsifier Sweep, the mandatory order is: Structure/Hypothesis; preliminary
non-empirical structural checks; dataset availability/admissibility assessment; complete protocol
freeze; data-dependent T0 cells; T1 availability; T1 Discovery; robustness plus independent
Validation/walk-forward; T2; final untouched holdout. Pure formula/schema consistency may precede
freeze only when it inspects no outcomes and selects no configuration. See
[Validation 13](../validation/13_ECONOMIC_FALSIFIER_AND_BOUNDED_SWEEP.md).

## Failure decomposition

“The bot is not profitable” is not a diagnosis. Evidence must locate at least one typed cause: invalid opportunity; BBO reject; exact-L2 reject; Risk reject; q zero; Reservation failure; opportunity expired before send; send/arrival delay; exchange reject; zero fill; partial fill; later-leg failure; Recovery; negative realized PnL; infrastructure instability; account/Reconciliation problem; or model/support/OOD problem. The Capture Funnel and actual-outcome lineage turn each cause into a testable hypothesis without collapsing populations.

## Claim classes

Every material statement is exactly one of `FACT`, `MEASURED`, `DERIVED`, `MODELLED`, `COUNTERFACTUAL`, `HYPOTHESIS`, `INTERPRETATION`, or `DECISION`. It carries provenance, author/producer, timestamp, version, support and uncertainty where relevant. `DECISION` requires its named authority; AI output defaults to `HYPOTHESIS` or `INTERPRETATION`.

## Baseline-first gate

Research orchestration remains `DEFERRED_BLOCKED` until all prerequisites in the directory README are evidenced. Documentation and inert templates may exist earlier. Search jobs, strategy portfolios, Champion/Challenger automation, drift-driven selection and capital-bearing trials may not.

A separately authorized bounded local batch may evaluate one predeclared Prompt-1 experiment once
its exact Replay/T1 dependencies exist. It is an evaluation mechanism, not activation of
generalized Parameter Search, the Research Factory, AI discovery, distributed research, Monte
Carlo programs or strategy-level Champion/Challenger.

## Failure semantics

Invalid, aborted, inconclusive, censored, negative and contradicted outcomes are first-class. Their records are append-only; corrections supersede with lineage. A failed experiment can close a hypothesis, narrow its scope, expose an instrumentation fault, or require an incident. It is never erased to improve the apparent record.

## Controlled Strategy Research Factory

The future Factory is a proposal and evidence-production system. It does not require AI or ML; the
initial OWA/TT Falsifier remains simple, declared and deterministic. Human, statistical, incident
or AI inputs may propose claims, but all enter the same frozen evidence chain.

### D8 — Strategy discovery and Challenger evaluation

```text
Canonical Data + reconciled Actual Outcomes
                       |
                       v
          HYP-* Research Hypothesis
                       |
                       v
       StrategyFamily / DRAFT StrategySpec
                       |
                       v
           EXP-* Frozen Experiment Plan
                       |
                       v
        Research Workers (computation only)
                       |
                       v
       Canonical Replay / Simulator / Falsifier
                       |
                       v
     Robustness + temporal OOS + T2 + holdout
                       |
          +------------+-------------+
          |                          |
          v                          v
 negative / invalid retained    Challenger Candidate
                                      |
                                      v
                            Human Evidence Review
                                      |
                                      v
                     Separate capability progression
```

Read top-to-bottom: proposal becomes a frozen experiment; canonical engines generate evidence;
only a surviving candidate reaches human review, and review still does not bypass the separate
capability progression.

Contract — **Inputs:** canonical datasets/actual outcomes, `HYP-*`, optional family/spec and frozen
`EXP-*`. **Operations:** workers invoke canonical Replay/Simulator/Falsifier, then temporal and
adversarial validation. **Outputs:** complete evidence, rejected/inconclusive records or a
non-authorizing Challenger candidate. **Canonical authority:** Data/Replay/Simulator/Validation;
humans govern promotion, while Risk and capability authorities remain final. **Failure/uncertainty:**
all negative, invalid, failed, censored and missing-support outcomes remain visible; AI cannot
repair or promote them. **Activation timing:** full Factory only after the README baseline gate;
initial OWA/TT needs neither AI nor Factory activation.

The Factory may later investigate filters, market/regime scope, route-selection rules, supported
features, parameter regimes, model challengers, separately eligible execution policies and better
falsifiable claims. It cannot self-promote, change Formula/Risk/ESM/Inventory, create ActualFill,
raise q/capital, send an order or mutate Live state.
