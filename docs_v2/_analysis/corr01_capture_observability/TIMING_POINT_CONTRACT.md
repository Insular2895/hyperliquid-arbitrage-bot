# CORR-01 — Timing Point Contract

DOCUMENTATION STATUS: DESIGN CONTRACT — IMPLEMENTATION NOT AUTHORIZED

## Clock rule

Local elapsed durations use one monotonic clock domain per process/host. Wall clock is recorded for audit and cross-system correlation, never substituted for monotonic elapsed time. Exchange timestamps are separately named source observations; subtracting them from local time is invalid unless their semantics, units and clock uncertainty are proven for that use.

## Named points

`M` = mandatory when the corresponding path occurs; `O` = optional/conditional. Replay synthesizes the same semantic points from `ReplayClock` where the recorded evidence supports them.

| ID | Semantic boundary | Scope | Req. | Modes / external semantics | Missing-point treatment |
|---|---|---|---:|---|---|
| `T_RX` | first local byte/message availability at the declared adapter boundary | event/source/host | M | all modes; local monotonic | invalidates inbound/end-to-end local interval |
| `T_NORMALIZED` | normalized event validation completes | event | M | all | mark normalization interval missing/invalid |
| `T_ORDERED_ADMISSION` | event enters definitive local ordered stream | event/run | M | all | projection invalid; ordering not provable |
| `T_BOOK_PUBLISHED` | immutable valid/invalid Book snapshot version is published | event/market | M | market-state events | no decision-latency claim for that observation |
| `T_ROUTE_LOOKUP_DONE` | affected-route lookup finishes | reevaluation | M | when reevaluation occurs | route-lookup interval unavailable |
| `T_BBO_DONE` | cheap comparator finishes | route evaluation | M | when cheap evaluation occurs | cheap funnel disposition invalid |
| `T_EXACT_ECON_DONE` | exact L2/formula result and validity finish | route evaluation | M | only dispatched exact work | exact stage unavailable |
| `T_FEATURES_DONE` | required feature snapshot is complete | candidate | O | when features are required | dependent forecast timing/validity unavailable |
| `T_PARTICIPANT_DONE` | required participant forecasts complete | candidate | O | when required | dependent bundle invalid/unavailable |
| `T_SIMULATION_DONE` | candidate ExecutionForecast freezes | candidate | O | when Simulator is required | dependent bundle invalid/unavailable |
| `T_SIZING_DONE` | quantized sizing disposition freezes | candidate/execution | O | eligible sizing path | sizing interval unavailable |
| `T_RISK_DONE` | immutable RiskDecision freezes | candidate/execution | O | Risk-evaluated path | eligibility cannot be inferred |
| `T_RESERVATION_DONE` | atomic reservation set commits/fails | execution | O | reservation path | reservation interval unavailable |
| `T_PLAN_COMMITTED` | immutable ExecutionPlan commits | execution | O | planned path | no committed-plan timing claim |
| `T_INTENT_FROZEN` | first risk-increasing OrderIntent freezes | intent/execution | O | attempted candidate path | sign/send path unavailable |
| `T_SIGNED` | signed exchange request is ready at signer boundary | intent | O | real/simulated transport as declared | sign interval unavailable |
| `T_SEND_HANDOFF` | signed request handed to effect/transport boundary; possible transmission begins | intent/attempt | O | actual transport or explicitly simulated equivalent | attempt classification needs transport evidence |
| `T_LOCAL_SEND_COMPLETE` | declared local transport write/enqueue completes | intent | O | boundary must state userspace/kernel semantics | local-send interval unavailable; never infer exchange receipt |
| `T_ACK_RX` | acknowledgement first becomes locally available | order | O | actual ACK or simulated ACK, separately scoped | ACK interval censored/missing; may be `UNKNOWN` |
| `T_FIRST_FILL_RX` | first unique fill first becomes locally available | order/execution | O | actual/simulated truth kept separate | no first-fill duration; zero-fill remains outcome evidence |
| `T_LAST_FILL_RX` | last unique fill known at outcome cutoff | order/leg/execution | O | provisional until terminal/reconciled | last-fill duration censored until finality |
| `T_ROUTE_TERMINAL` | route enters terminal canonical state for this lifecycle | execution | O | route-machine truth | route-duration unresolved/censored |
| `T_RECONCILED` | attempt-scope reconciliation becomes consistent/terminal | execution | O | canonical Reconciliation truth | outcome not terminal-reconciled |

Every point record also carries `run_id`, `run_mode`, correlation ID, host/process/clock-domain ID, monotonic timestamp, optional wall timestamp, build/config/schema versions and validity/reason.

## External source timestamps

If an exchange event supplies `exchange_ts`, it is stored as `source_exchange_ts` with endpoint/message semantic, documented precision and current external-validation status. It is not one of the local `T_*` points. Feed age or one-way network latency is `UNAVAILABLE` when source clock semantics/uncertainty do not support subtraction. ACK/fill durations measured between local send and local receive include unknown network/exchange composition.

## Clock discontinuity

Negative, non-finite, cross-domain or overflowed intervals are invalid. Host migration, process restart or clock-domain change prevents direct monotonic subtraction unless a separately validated mapping exists. Reports retain invalid counts and reason codes.
