# Risk Data Contract Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Frozen fields below come from SRC-005 Dossier 4. Where Dossier 3 requires semantics but Dossier 4 has no dedicated frozen object, PASS 05 records the owner/reference and does not invent fields.

| Contract | Exact frozen fields or exact source representation | Risk role | Authority / unresolved boundary |
|---|---|---|---|
| `RiskSnapshot` | `risk_snapshot_id`, `market_versions`, `account_version`, `inventory_version`, `reservation_version`, `feature_snapshot_ids`, `model_forecasts`, `infra_state_version`, `risk_config_version`, `created_at` | Immutable point-in-time input | Dossier 4 lines 6433–6455 |
| `RiskDecision` | `decision_id`, `risk_snapshot_id`, `allowed`, `action`, `max_allowed_size`, `required_price_limits`, `hard_rejects[]`, `warnings[]`, `created_at` | Authorization/bounds/result | Dossier 4 lines 6456–6478; semantic extras map through references |
| `ExecutionPlan` | `execution_id`, `opportunity_id`, `route_id`, `size`, `legs[]`, `execution_mode`, `reservations[]`, `risk_decision_id`, `model_versions`, `config_versions`, `created_at`, `plan_version` | Immutable executable plan after favorable decision | Dossier 4 lines 6479–6508; pins config/model/risk linkage |
| `RiskConfig` | No dedicated frozen `RiskConfig {}` found; `ResolvedConfig` plus `config_hash`, `config_version`, and `RiskSnapshot.risk_config_version` | Effective policy/version | Do not invent schema; Data/config closure to finalize |
| `RejectReason` | Closed/versioned enum families: `MarketData`, `Economic`, `Risk`, `Inventory`, `Model`, `Execution`, `Infra`, `Exchange`, `Reconciliation` | Machine-readable hard/warning/audit reason | Dossier 4 lines 6827–6857; exact member set future Data closure |
| `RejectEvent` / rejected opportunity | `opportunity_id?`, `route_id`, `reason_codes[]`, `snapshot_ids`, `timestamp`; Dossier 3 also requires later `counterfactual future outcome` | Reject dataset/calibration | Event frozen at 6805–6826; outcome-link schema not frozen |
| `AccountState` | `balances`, `open_orders`, `fills_ledger`, `fee_state`, `reconciled`, `state_version` | Account consistency/exchange truth | Dossier 4 lines 5991–6013 |
| `InventoryState` | `positions_by_asset`, `targets`, `bands`, `net_flows`, `classifications`, `version` | Inventory/capital gates | Dossier 4 lines 6014–6035 |
| `InventoryPosition` | `asset_id`, `quantity`, `mark_value`, `target`, `soft_min`, `soft_max`, `hard_min`, `hard_max` | Asset band evaluation | Dossier 4 lines 6040–6060 |
| `ReservationState` | `balance_reservations`, `book_reservations`, `risk_reservations`, `version` | Atomic resource ownership | Dossier 4 lines 6061–6074 |
| `FeatureSnapshot` | `snapshot_id`, `market_features`, `route_features`, `volatility`, `ofi`, `imbalance`, `microprice`, `timestamp`, `feature_schema_version` | Immutable model input | Dossier 4 lines 6276–6304 |
| `ModelForecast` | `model_id`, `model_version`, `input_snapshot_id`, `prediction`, `confidence`, `ood_state`, `produced_at` | Generic model evidence | Dossier 4 lines 6305–6324 |
| `EdgeSurvivalForecast` | `p_survive_horizons[]`, `p_survive_arrival`, `edge_half_life`, `expected_edge_arrival`, `edge_quantiles`, `confidence` | Survival/arrival gates | Dossier 4 lines 6325–6341 |
| `LiquidityForecast` | `expected_depth_arrival`, `depth_quantiles`, `p_depth_loss`, `expected_replenishment`, `spread_forecast`, `confidence` | Liquidity/execution risk | Dossier 4 lines 6342–6359 |
| `MakerForecast` | `fill_probability_by_horizon`, `expected_fill_time`, `partial_probability`, `adverse_selection_by_horizon`, `confidence` | Maker risk/quality | Dossier 4 lines 6360–6375 |
| `CrossMarketForecast` / `ResponseForecast` | `source_market`, `responses[]`, `confidence`; response: `target_market`, `horizon`, `expected_move`, `quantiles`, `probability_directional_move` | Consistency/response support | Dossier 4 lines 6376–6403 |
| `ExecutionForecast` | `execution_plan_candidate_id`, `p_full`, `p_partial`, `p_recovery`, `p_failure`, `expected_pnl`, `pnl_quantiles`, `probability_positive`, `expected_shortfall`, `expected_fees`, `expected_slippage`, `confidence`, `simulation_version` | Execution/tail/economic gates | Dossier 4 lines 6404–6432 |
| `InfraState` | `clock_health`, `feed_health`, `api_latency_distribution`, `compute_latency_distribution`, `scheduler_jitter`, `packet_loss`, `recorder_health`, `state`, `version` | Infra eligibility/degradation | Dossier 4 lines 6858–6889 |
| `ModelVersion` | `model_id`, `semantic_version`, `training_dataset_id`, `feature_schema_version`, `artifact_hash` | Model provenance/support | Dossier 4 lines 7270–7292 |
| `DecisionTrace` | `ordered_decisions[]`, `order_intents[]`, `state_transitions[]`, `risk_decisions[]` | Deterministic replay/audit | Dossier 4 lines 7078–7091 |
| `RunManifest` | `run_id`, `mode`, `git_commit`, `build_hash`, `config_hash`, `dataset_id?`, `model_versions`, `formula_schema_version`, `event_schema_version`, `start_time`, `random_seed?` | Run provenance | Dossier 4 lines 6933–6968 |
| Kill-switch events | `ControlEvent { Start, Stop, KillMarket, KillStrategy, KillGlobal, ConfigUpdate }` | Control-plane evidence | Dossier 4 lines 6785–6804; asset/mode/model/infra event encoding not frozen |
| Incident event | `IncidentRecord { incident_id, severity, affected_markets, affected_executions, start, end?, triggers[], actions[], resolution? }` | Grouped anomaly/escalation | Dossier 4 lines 9094–9128 |
| State hashes | Exact hash fields exist across state/checkpoint/run validation; no single frozen `StateHashes {}` located | Replay integrity | Reference snapshot IDs/versions; Data closure owns consolidated schema |

## Contract corrections

1. Frozen `required_price_limits` plural wins over Dossier 3 `required_price_limit` singular.
2. `required_execution_mode`, `risk_config_version` and `model_versions` are mandatory semantics but not extra frozen RiskDecision fields; they are linked through RiskSnapshot/ExecutionPlan.
3. Asset/mode/model/infra kill names are constitutional taxonomy entries, but Dossier 4 `ControlEvent` freezes only market/strategy/global variants. Exact event-schema expansion remains Data closure work.
4. `RiskConfig`, consolidated state hashes and counterfactual-outcome linkage are semantic requirements without frozen standalone schemas. They are not fabricated here.

Data contracts mapped: 23. Schema gaps explicitly routed: 4; destinationless: 0.
