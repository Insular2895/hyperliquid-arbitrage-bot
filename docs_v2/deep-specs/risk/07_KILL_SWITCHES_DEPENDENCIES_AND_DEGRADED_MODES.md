# Kill Switches, Dependencies and Degraded Modes

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Scope taxonomy

The exact minimum taxonomy is `GLOBAL_KILL`, `MARKET_KILL`, `ASSET_KILL`, `STRATEGY_KILL`, `EXECUTION_MODE_KILL`, `MODEL_KILL`, `INFRA_KILL`. A switch is latched, reason-coded, timestamped and auditable. Dependency mapping selects the smallest scope that restores safety; a global halt is not the default when safe isolation exists.

| Scope | Core effect |
|---|---|
| `GLOBAL_KILL` | New risk off everywhere; cancel maker; reconcile; recover only by policy. |
| `MARKET_KILL` | Disable market and all routes in `pair_to_routes`; preserve permitted exits. |
| `ASSET_KILL` | Disable all routes touching suspect asset except permitted risk-reducing exits. |
| `STRATEGY_KILL` | Disable one strategy while independent validated strategies may continue. |
| `EXECUTION_MODE_KILL` | Disable one mode such as maker while other modes remain separately eligible. |
| `MODEL_KILL` | Disable model-dependent capabilities or use their validated conservative fallback. |
| `INFRA_KILL` | Remove new-risk permission at the affected infrastructure scope. |

## Specialized trigger families

- Execution quality: persistent actual slippage/partial/recovery divergence.
- Simulator calibration: PnL bias, coverage or fill calibration outside tolerance.
- Participant model drift: survival/calibration/features materially outside support.
- Fee change: invalidate cached economics before new risk.
- Metadata change: invalidate routes and rebuild precision/rules before orders.

Triggers select a taxonomy scope; they are not alternative action enums.

## Dependencies and fallbacks

Each capability declares mandatory dependencies, optional dependencies and validated fallbacks. Missing mandatory input disables the dependent capability. A fallback must be equally or more conservative and separately validated; otherwise the dependent strategy/mode is killed. Risk-reducing exits cannot be trapped merely because the asset/market is killed, but still require known exposure and executable protected state.

## Degraded infrastructure

`HEALTHY` imposes no independent restriction; `DEGRADED` may reduce size or require more economic margin; `UNSAFE` forbids new risk; `CRITICAL` invokes cancel/recovery/halt behavior. Feed age, clock, network, processing lag, scheduler, API, WebSocket, recorder and storage contribute. Exact thresholds, windows and hysteresis are calibrated.

## Reset

Reset requires trigger clearance, dependency health, required state rebuild/reconciliation, configuration/model validation, and manual acknowledgement where severity/policy requires. Resetting a latch does not enter `READY`; startup/readiness gates run again. No remote or operator override bypasses constitutional checks.

Source: SRC-005 lines 2812–2899, 2985–3070, 3225–3317 and 3875–3944.
