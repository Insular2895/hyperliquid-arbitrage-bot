# CORR-01 — Outcome Label Contract

DOCUMENTATION STATUS: CANONICAL ANALYTICAL LABELS — AWAITING HUMAN REVIEW

## Label axes

Outcomes are multi-axis records, not one `success` boolean.

| Axis | Canonical values | Evidence / finality |
|---|---|---|
| attempt | `NOT_ATTEMPTED`, `ATTEMPTED` | possible-transmission boundary |
| acknowledgement | `ACKED`, `KNOWN_REJECT`, `NO_ACK_KNOWN`, `UNKNOWN` | order/exchange evidence |
| fill | `ZERO_FILL`, `PARTIAL_FILL`, `FULL_LEG_FILL`, `MULTI_LEG_MIXED`, `UNRESOLVED` | unique actual fills versus targets |
| original route | `FULL_ROUTE_COMPLETED`, `NOT_COMPLETED`, `UNRESOLVED` | `CF-27` predicate |
| exposure | `NO_EXPOSURE`, `INTERMEDIATE_EXPOSURE`, `RESIDUAL_EXPOSURE`, `UNRESOLVED` | actual Inventory deltas/objective |
| recovery | `NOT_ENTERED`, `RECOVERED`, `RECOVERY_FAILED`, `RECOVERY_UNRESOLVED` | Recovery machine |
| reconciliation | `TERMINAL_RECONCILED`, `NOT_YET_RECONCILED`, `FAILED_SAFE_UNRESOLVED` | Reconciliation truth |
| economic | `POSITIVE`, `ZERO`, `NEGATIVE`, `INCOMPLETE` | complete attempt PnL/horizon/numeraire |

Order partial fill and route intermediate exposure are distinct: an order can fill completely while the multi-leg route has intermediate exposure; an order can fill partially without a terminal route label yet.

## Final label record

An `ExecutionOutcomeLabel` binds:

- `execution_id`, originating Opportunity and optional episode ID/version;
- `OutcomeLabelVersion` and `FunnelDefinitionVersion`;
- route objective, plan/leg target versions and tolerance policy;
- values for every axis above;
- first possible-send, fill, terminal and reconciliation times where available;
- actual quantities/prices/fees, Recovery linkage and PnL record;
- completeness flags, unresolved/censoring reasons, `as_of` and revision lineage;
- mode/source/run/build/config/schema/formula/model provenance.

## Full-route predicate

`FULL_ROUTE_COMPLETED` requires all of:

1. the attempt reached canonical `RouteExecutionState.COMPLETED`;
2. the original intended route’s revalidated leg objectives were achieved within the frozen label tolerance;
3. Recovery was never entered for that execution;
4. actual fills, not planned/simulated fills, prove the quantities;
5. the claim has not been contradicted by later reconciliation.

This analytical predicate does not change the existing state machine, which may use `COMPLETED` for a safely recovered closure.

## Economic outcome

Attempt-level actual PnL declares which components are included: strategy execution, fees, slippage, Recovery cost/loss, inventory realization/mark at a specified horizon and any allocated infrastructure cost. Components remain separately visible and are not double-counted. `POSITIVE` is strict `PnL > 0`; incomplete valuation is never treated as zero or negative.

## Revisions

Labels may progress from unresolved to known as ACK/fill/reconciliation evidence arrives. Corrections append `supersedes_label_id`, reason and new `as_of`; reports use the latest valid label as of their cutoff while retaining revision counts. No later model prediction may overwrite a frozen forecast or actual label.
