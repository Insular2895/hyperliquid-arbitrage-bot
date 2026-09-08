# CORR-03 — Baseline and Scope

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW — IMPLEMENTATION NOT AUTHORIZED

| Control | Value |
|---|---|
| `CORR03_BASELINE_COMMIT` | `705bbe781ad4246ed68262ffca84360a93c0c5e2` |
| Branch | `codex-docs` |
| CORR-02 prerequisite | `VERIFIED` after explicit report-control wording repair |
| Scope | execution outcome evidence, HJ failure fixtures, empirical completion baseline, calibration and promotion contracts |
| Runtime/source code | no change |
| Formula Book | QF-001–110 unchanged; Formula ID additions `0` |
| Execution/Recovery/Risk behavior | unchanged |
| External evidence | comparative only; not `SRC-009` |
| Approval | `PENDING FINAL REVIEW` |

## Authority and boundaries

Execution, Recovery and Reconciliation remain the only authorities for actual order/fill/exposure state. Simulator owns predictions and counterfactual outcomes. Data/Recorder owns immutable lineage; Validation owns evidence judgments; Risk may consume only promoted forecasts. CORR-03 derives analytical labels from authoritative events and creates no sixth state machine, no mutable truth store, no hard `p_full` gate and no sizing rule.

The primary population is a real attempt that crossed the first possible risk-increasing transmission boundary. Proven pre-transmission aborts are not attempts. A possible transmission with `UNKNOWN` outcome remains an attempt and remains unresolved until authoritative evidence closes it.

## Required authorities reviewed

Current Masters 00, 04, 06–12 and 16–19; Execution and Simulator deep specifications; CORR-01 funnel/label/join contracts; CORR-02 performance/parity contracts; source closure `SRC-004` and `SRC-005` for QF-056/057 and `ExecutionForecast`; Harjus primary repository, author write-ups and production log.

## Non-goals

- no implementation, test code or exchange call;
- no new runtime enum or state transition;
- no relabeling `UNKNOWN` as failure/no-fill;
- no simulated or Shadow outcome promoted to actual;
- no naïve multiplication of per-leg rates;
- no online self-modifying model;
- no CORR-04 work.
