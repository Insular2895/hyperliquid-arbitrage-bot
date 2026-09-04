# RiskDecision Contract Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Authority resolution

SRC-005 Dossier 3 section 139 defines semantic requirements; Dossier 4 sections 62–64 freeze exact fields. The frozen contract wins for field shape.

| Frozen field | Producer/source | Meaning and enforcement |
|---|---|---|
| `decision_id` | Risk | Stable decision identity for plan/audit. |
| `risk_snapshot_id` | RiskSnapshot | Exact immutable input snapshot. |
| `allowed` | Risk | Boolean compatibility field; action remains authoritative for mode. |
| `action` | Risk | One exact canonical action enum. |
| `max_allowed_size` | Risk/Sizing boundary | Upper bound; ExecutionTransport verifies actual plan size. |
| `required_price_limits` | Risk/Execution | Protected price bounds; plural frozen spelling wins over Dossier 3 singular. |
| `hard_rejects[]` | Gate pipeline | Versioned closed `RejectReason` enum entries. |
| `warnings[]` | Gate pipeline | Non-bypassing warnings; cannot neutralize hard rejects. |
| `created_at` | Clock/Data | Decision creation time used with calibrated TTL policy. |

## Exact action enum

`ALLOW`, `ALLOW_REDUCED_SIZE`, `ALLOW_RECOVERY_ONLY`, `REJECT`, `HALT_MARKET`, `HALT_STRATEGY`, `HALT_GLOBAL`.

No additional canonical action was found. Taxonomy-specific asset/mode/model/infra kills are scoped kill events whose RiskDecision may use the closest canonical halt action plus reason/dependency state; exact encoding is a Data Contracts follow-up, not a new enum invented by PASS 05.

## Semantic-to-frozen mapping

| Dossier 3 semantic | Frozen representation |
|---|---|
| `required_execution_mode` | `ExecutionPlan.execution_mode`, constrained by decision/action and referenced by `risk_decision_id`. |
| `risk_config_version` | `RiskSnapshot.risk_config_version`; plan pins under `config_versions`. |
| `model_versions` | `RiskSnapshot.model_forecasts` and `feature_snapshot_ids`; `ExecutionPlan.model_versions`. |
| Calculated metrics / market hash | Referenced snapshots, audit record/DecisionTrace; exact extra schema deferred to Data closure. |

## Transport acceptance

ExecutionTransport may send a real new-risk OrderIntent only for current `ALLOW` or `ALLOW_REDUCED_SIZE`; the latter must respect the size cap. It verifies snapshot/plan linkage, TTL/invalidation state, required price limits and pinned config. `ALLOW_RECOVERY_ONLY` authorizes only the separately classified recovery path, not a normal OrderIntent.

## Reject reason authority

Known exact examples in SRC-005 are `RISK_BOOK_STALE`, `RISK_INVENTORY_HARD_LIMIT`, `RISK_CVAR`, `RISK_MODEL_OOD`, `RISK_INFRA_UNSAFE`, `RISK_BALANCE_UNKNOWN`, `RISK_ACCOUNT_UNRECONCILED`. Dossier 4 defines closed families `MarketData`, `Economic`, `Risk`, `Inventory`, `Model`, `Execution`, `Infra`, `Exchange`, `Reconciliation`. PASS 05 does not fabricate missing enum members.

Sources: SRC-005 lines 3330–3474 and 5010–5029; Dossier 4 lines 6433–6508; PASS 04 ExecutionTransport enforcement.
