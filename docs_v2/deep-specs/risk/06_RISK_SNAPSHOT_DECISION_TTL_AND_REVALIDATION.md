# RiskSnapshot, RiskDecision, TTL and Revalidation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Point-in-time boundary

A decision reads exactly one immutable `RiskSnapshot`. The frozen Data Contract fields are `risk_snapshot_id`, `market_versions`, `account_version`, `inventory_version`, `reservation_version`, `feature_snapshot_ids`, `model_forecasts`, `infra_state_version`, `risk_config_version`, `created_at`. These IDs resolve books, inventory, balances, reservations, features/models and infra without mixing timestamps.

Every material input event produces a new version. Risk evaluation performs no network or storage I/O and cannot read mutable components piecemeal.

## RiskDecision contract

The frozen fields are `decision_id`, `risk_snapshot_id`, `allowed`, `action`, `max_allowed_size`, `required_price_limits`, `hard_rejects[]`, `warnings[]`, `created_at`.

The exact action enum is:

```text
ALLOW
ALLOW_REDUCED_SIZE
ALLOW_RECOVERY_ONLY
REJECT
HALT_MARKET
HALT_STRATEGY
HALT_GLOBAL
```

Dossier 3's semantic `required_execution_mode`, `risk_config_version` and `model_versions` are enforced through snapshot/ExecutionPlan references because they are not frozen fields in the Dossier 4 RiskDecision schema. This avoids silently expanding the contract. `required_price_limit` in Dossier 3 is normalized to the frozen plural `required_price_limits`.

`hard_rejects[]` and `warnings[]` use the versioned `RejectReason` enum families; free-form strings are explanatory telemetry only. A decision stores enough referenced state and calculated gate evidence to explain an allow/reduce/reject months later.

## TTL and invalidation

`TTL_risk` is calibrated from market regime, edge survival and feed fidelity. Expiry requires revalidation before send. Material book/account/reservation/config/model/infra change invalidates a decision even inside TTL.

| Checkpoint | Required evaluation |
|---|---|
| `T0` | Opportunity detected. |
| `T1` | Before reservation. |
| `T2` | Immediately before order send. |
| `T3` | After each fill. |
| `T4` | Before every next leg. |
| `T5` | While maker rests. |

Each check creates or refers to a new immutable snapshot as needed. Size reduction creates an explicitly bounded decision; it does not mutate the proposal silently.

## Transport defense

Before a real order, ExecutionTransport requires an unexpired, matching decision with `ALLOW` or `ALLOW_REDUCED_SIZE`, verifies `size <= max_allowed_size`, required price limits and immutable plan references, then applies its own safety checks. Other actions cannot transmit a new-risk OrderIntent.

Source: SRC-005 lines 3330–3474, 4459–4484 and 5010–5029; frozen fields SRC-005 Dossier 4 lines 6433–6508.
