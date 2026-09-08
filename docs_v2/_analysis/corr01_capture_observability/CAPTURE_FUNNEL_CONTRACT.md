# CORR-01 — Canonical Capture Funnel Contract

DOCUMENTATION STATUS: POST-RECONSTRUCTION CORRECTION — AWAITING HUMAN REVIEW

## Doctrine

```text
DETECTED != EXECUTABLE != ELIGIBLE != ATTEMPTED
         != FILLED != COMPLETED != RECONCILED
         != ECONOMICALLY_POSITIVE
```

The funnel is a derived, replayable evidence projection. It neither commands runtime work nor duplicates Market Graph, Risk, Execution, Recovery, Reconciliation or Accounting state. A stage is true only when its canonical producer evidence exists and passes the declared validity rules.

## Pre-execution funnel

| Stage | Canonical name | Meaning | Required evidence | Owner | Explicit non-equivalence |
|---|---|---|---|---|---|
| `CF-00` | `MARKET_OBSERVATION_PUBLISHED` | one admissible ordered market observation produced a usable published market state | `MarketEventId`, ordered admission, `BookVersion`, source/mode/time validity | Market Data / Data | not a route evaluation |
| `CF-01` | `ROUTE_REEVALUATION_TRIGGERED` | the observation selected an affected route for cheap reevaluation | `ReevaluationId`, `RouteId`, triggering event/version | Market Graph | not an economic opportunity |
| `CF-02` | `CHEAP_EVALUATION_COMPLETED` | the declared BBO/cheap comparator completed validly | `RouteEvaluationId`, comparator version and result | Market Graph | completed does not mean passed |
| `CF-03` | `CHEAP_SCREEN_PASSED` | cheap result crossed its versioned dispatch criterion | evaluation result with pass decision | Market Graph | not exact executable economics |
| `CF-04` | `EXACT_EVALUATION_COMPLETED` | exact L2/economic evaluation completed at explicit versions/size candidate | exact trace, input versions and validity | Market Graph / Formula | completed does not mean valid or positive |
| `CF-05` | `EXACT_CANDIDATE_VALID` | exact result is finite, fresh, precision/fee valid and above its defined candidate condition | exact evaluation plus validity record | Market Graph / Formula | not Risk eligible |
| `CF-06` | `OPPORTUNITY_DETECTED` | immutable event-level `OpportunityId` is emitted for an exact-valid candidate | `Opportunity` record | Market Graph | not continuous episode; not attempt |
| `CF-07` | `FORECAST_BUNDLE_VALID` | required Simulator/Participant forecasts exist, are supported and version-compatible | immutable forecast bundle, confidence/validity | Simulator / Participants | not Risk allow |
| `CF-08` | `EXECUTION_CANDIDATE_VALID` | strategy, capital reachability, size-domain and execution-mode prerequisites form a candidate | candidate ID, route/capital/mode versions | Strategy / Capital / Sizing | not positive executable size or permission |
| `CF-09` | `RISK_ELIGIBLE` | current immutable `RiskDecision` permits a bounded action | allowed decision, snapshot/version/scope | Risk | not reservation or send |
| `CF-10` | `POSITIVE_SIZE_SELECTED` | Sizer returns strictly positive quantized size within all current bounds | sizing decision and input versions | Sizing | not reserved capacity |
| `CF-11` | `RESERVATION_COMMITTED` | full required balance/book/Risk reservations are atomically committed | reservation set and `ExecutionId` | Execution / Inventory / Risk | not an order attempt |
| `CF-12` | `EXECUTION_PLAN_COMMITTED` | immutable, version-compatible execution plan is frozen | `ExecutionPlanId`, plan hash, lineage | Execution | not attempted; transmission may still be impossible |
| `CF-13` | `EXECUTION_ATTEMPTED` | first risk-increasing intent may have been transmitted | intent enters `SENT`, or transport result is ambiguous after possible transmission | Execution | not ACK, accepted order or fill |

The canonical attempted boundary is conservative. A local failure proven to occur before any possible transmission is not an attempt. A timeout/exception after possible transmission is an attempt and may become `UNKNOWN`; it is never removed from the denominator.

## Execution outcome DAG

Execution is a DAG, not a single narrowing line: attempts may branch to known reject, zero fill, partial fill, full fill, ambiguity, recovery and reconciliation.

| Stage | Canonical name | Meaning | Required evidence |
|---|---|---|---|
| `CF-20` | `LEG_REACHED` | control reached an intended leg after current-state revalidation | leg transition/decision trace |
| `CF-21` | `LEG_ATTEMPTED` | an intent for that leg may have transmitted | intent `SENT` or post-possible-send ambiguity |
| `CF-22` | `ANY_ACTUAL_FILL` | at least one unique actual fill exists for the execution | canonical `FillEvent` |
| `CF-23` | `LEG_FULLY_FILLED` | one leg’s actual filled quantity satisfies its frozen/revalidated target within declared tolerance | fills plus leg target/tolerance |
| `CF-24` | `ORDER_PARTIAL_FILL_OBSERVED` | an order has nonzero fill below its terminal requested quantity | order reducer truth |
| `CF-25` | `INTERMEDIATE_EXPOSURE_CREATED` | actual fills leave a non-final asset exposure relative to the route objective | inventory deltas plus route objective |
| `CF-26` | `EXECUTION_TRUTH_UNKNOWN` | possible effects cannot yet be resolved | canonical `UNKNOWN` evidence |
| `CF-27` | `FULL_ROUTE_COMPLETED` | every intended route objective completed under the original route execution without entering Recovery, and route state reached `COMPLETED` | route/leg actuals, transition history |
| `CF-28` | `RECOVERY_ENTERED` | canonical Recovery owns an actual or possible residual exposure | recovery transition and `RecoveryId` |
| `CF-29` | `RECOVERY_TERMINAL` | Recovery ended `RECOVERED` or `RECOVERY_FAILED` | recovery terminal record |
| `CF-30` | `TERMINAL_RECONCILED` | orders, fills, balances, inventory, fees and reservations agree for the attempt scope | reconciliation record and terminal evidence |
| `CF-31` | `ECONOMIC_OUTCOME_COMPLETE` | attempt-level actual PnL components are complete at the declared valuation horizon | accounting records and completeness status |
| `CF-32` | `ECONOMICALLY_POSITIVE` | complete attempt-level actual PnL is strictly greater than zero in the declared numeraire | `CF-31` plus PnL value |

`RouteExecutionState.COMPLETED` after successful Recovery is a safe canonical closure but is not re-labelled `CF-27 FULL_ROUTE_COMPLETED`; it is represented through Recovery, reconciliation and economic outcome. This analytical distinction changes no state transition.

## Monotonicity and revision

- Positive pre-execution stages are append-only facts for one lineage; later invalidation creates a reasoned terminal disposition, not deletion.
- Stage counts may be recomputed when projection logic changes only under a new `FunnelDefinitionVersion`.
- Exchange corrections, deduplication or reconciliation may revise actual labels. Revisions are append-only, reasoned and versioned; prior labels remain auditable.
- `UNKNOWN` is neither failure nor success until canonical resolution. Window reports expose unresolved/censored cohorts.
- A dashboard counter without join-complete canonical records is invalid evidence.

## Mode truth

Replay, Paper, Shadow, MicroLive and Live use the same stage semantics but never share populations without a declared comparison. Shadow can reach “would attempt” evidence but cannot truthfully emit actual-send, actual-fill, actual-reconciliation or realized-PnL stages. Simulator outcomes are simulated truth inside their run only.
