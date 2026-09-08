# CORR-03 — Execution Attempt Cohort Contract

DOCUMENTATION STATUS: ANALYTICAL POPULATION CONTRACT

## Primary target population

The initial completion target is:

`P(full intended strategy-route completion | a real execution attempt began, decision-time information)`.

An attempt begins when the first risk-increasing transmission occurred or may have occurred. A proven pre-transmission abort is excluded as `NOT_ATTEMPTED`; a possible transmission with lost/ambiguous response remains `ATTEMPTED` and unresolved. Risk-rejected, zero-sized, unreserved, Shadow and counterfactual candidates do not have actual fill labels.

## Cohort identity

Every report declares `PopulationId`, strategy family, execution mode, supported q/size-depth scope, markets/route family, RunMode/infra profile, `cohort_start`, `cohort_end`, `observation_cutoff`, resolution policy/version and label version. It emits attempt, resolved, full, non-full, pending, right-censored, invalid and policy-excluded counts.

TT and TTT are separate populations. OWA and Triangle are separate. MT/MTT are not pooled into the initial taker baseline and require maker time/horizon semantics. Recent cohorts are never compared to mature cohorts without showing maturity/resolution differences.

## Denominators

- operational completion at cutoff: full completed attempts divided by all attempts, with unresolved count/rate adjacent;
- resolved binary calibration: full completed resolved attempts divided by resolved valid attempts;
- opportunity-to-attempt selection: a separate CORR-01 funnel denominator, never substituted for the execution cohort.

The dataset retains difficult/negative attempts. No post-hoc exclusion may improve the denominator.
