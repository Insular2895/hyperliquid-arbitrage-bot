# Risk Kill-Switch Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

The seven exact scope names come from SRC-005 lines 3225–3237. Specialized quality/change switches choose one of these scopes. Exact quantitative triggers, reset windows and most final enum reason members are calibrated/Data-owned rather than invented here.

| Exact name | Scope | Trigger classes | Auto/manual | Action / affected capability | New risk | Existing execution / maker | Recovery / reconciliation | Reset condition | Reason / telemetry | Required test | Source |
|---|---|---|---|---|---|---|---|---|---|---|---|
| `GLOBAL_KILL` | Whole client engine | Account mismatch, multiple unknown orders, persistent critical feed, signer, severe drawdown, invariant failure, exchange-model inconsistency | Auto + manual trigger; manual ack by policy | Stop all new risk; cancel maker | OFF | Safety-only; maker cancel | Recovery by policy; reconcile required | Cause cleared + rebuild/reconcile + health + ack when required | Versioned global Risk reason; kill event/incident | Inject each trigger; latch/restart/reset | 3225–3247, 3875–3887 |
| `MARKET_KILL` | One market and `pair_to_routes` dependants | Book corruption, extreme unsupported volatility, slippage error, liquidity collapse, metadata anomaly | Auto/manual | Disable affected market/routes | OFF affected | Cancel/check affected maker; safe exit only | Reducing exit may use valid path; resync/reconcile | Market valid/current + dependencies + policy reset | Market/Risk reason; affected route list | Dependency propagation and safe-exit test | 3225–3260, 3888–3897 |
| `ASSET_KILL` | All routes touching asset | Suspect asset, invalid asset state/metadata or exposure condition | Auto/manual | Disable affected routes except reducing exits | OFF affected | No risk increase; cancel affected rest | Strict reducing exit; reconcile inventory/account | Asset/state valid + exposure accounted + ack as required | Asset/Risk reason; route dependency telemetry | Route graph propagation + non-trapping exit | 3225–3237, 3261–3272 |
| `STRATEGY_KILL` | One strategy | Strategy-specific recovery, profitability, adverse selection or model failure | Auto/manual | Disable only strategy; independent strategies may remain | OFF strategy | Finish/cancel only if safer/current | Reducing recovery; reconcile as needed | Cause/calibration cleared + strategy revalidated | Strategy/Risk reason; quality metrics | Isolation + no cross-strategy bypass | 3225–3237, 3273–3281, 3898–3906 |
| `EXECUTION_MODE_KILL` | Maker/taker/mode capability | Mode-specific quality, order semantics or dependency failure | Auto/manual | Disable mode; separately validated modes reevaluate | OFF mode | Cancel affected resting mode; safe current-leg policy | Reducing recovery via permitted mode | Mode dependency/quality recovered and revalidated | Execution/Risk reason; mode metrics | Mode isolation + transport refusal | 3225–3237; taxonomy authority |
| `MODEL_KILL` | Model and dependent capabilities | Invalid/NaN/OOD/drift/miscalibration/artifact/schema failure | Auto/manual | Conservative validated fallback or disable dependants | OFF if no valid fallback | Existing work reevaluates; maker may cancel | Conservative reducing policy | Artifact/support/calibration validated; atomic promotion | `RISK_MODEL_OOD` where applicable; model/version metrics | OOD/NaN/drift/fallback/isolation | 2826–2874, 3225–3300 |
| `INFRA_KILL` | Infrastructure instance or dependent capability | Feed/clock/network/processing/scheduler/API/recorder critical health | Auto/manual | No new risk at affected scope; possibly global | OFF affected | Cancel/check using available safe channel | Reducing recovery + reconciliation as feasible | Infra health acceptable across calibrated window + reconcile | `RISK_INFRA_UNSAFE`; InfraState/incident | Feed/clock/CPU/network/storage faults | 2985–3070, 3225–3237 |

## Specialized trigger-to-scope switches

| Switch family | Trigger | Possible minimum safe scope | Required response | Source |
|---|---|---|---|---|
| Execution Quality | Actual slippage/partial/recovery persistently exceeds prediction/tolerance | Execution mode, route, market or strategy | Reduce, disable affected capability, recalibrate | 2812–2825 |
| Simulator Calibration | PnL bias/fill/coverage outside validated tolerance | Simulator-dependent strategy/model | Reduce or disable dependent strategy | 2826–2848 |
| Participant Model Drift | Survival/calibration/features materially drift | Model/strategy | Conservative fallback or disable | 2849–2874 |
| Fee Change | Applicable fees differ/change | Affected markets/routes | Invalidate cached economics; recompute before new risk | 2875–2883 |
| Metadata Change | Precision/rules/asset metadata differs/change | Affected markets/assets/routes | Invalidate and rebuild state before new order | 2884–2899 |

No reset bypasses startup readiness. Switch effects and acknowledgement are persisted as kill/incident events; exact event schemas remain Data/Operations authority.
