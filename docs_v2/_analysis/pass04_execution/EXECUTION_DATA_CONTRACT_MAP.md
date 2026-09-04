# PASS 04 — Execution Data Contract Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

SRC-005 Data Contracts is authoritative. Field lists below reproduce only fields explicitly present there; `NOT FROZEN IN SRC-005` prevents accidental schema invention.

| Contract | Exact SRC-005 fields/names | Producer / consumer | Execution invariant |
|---|---|---|---|
| `ExecutionPlan` | `execution_id`, `opportunity_id`, `route_id`, `size`, `legs[]`, `execution_mode`, `reservations[]`, `risk_decision_id`, `model_versions`, `config_versions`, `created_at`, `plan_version` | Risk-allowed planning -> Coordinator | economically immutable at `PLANNED` |
| `ExecutionLegPlan` | `leg_id`, `market_id`, `input_asset`, `output_asset`, `role`, `order_policy`, `expected_input`, `expected_output`, `protected_price`, `max_slippage` | Plan -> leg execution | expected fields never overwrite actuals |
| `OrderIntent` | `intent_id`, `execution_id`, `leg_id`, `market_id`, `side`, `price_ticks`, `size_lots`, `tif`, `cloid`, `nonce?`, `risk_decision_id`, `created_at` | Coordinator -> signer/transport | stable logical identity; quantized |
| `SignedOrderIntent` | `intent`, `nonce`, `signature`, `signed_at` | signer -> transport | immutable after signing |
| identifiers | `OpportunityId`, `ExecutionId`, `LegId`, `IntentId`, `Cloid`, `Oid`, `FillIds` | end-to-end trace | distinct types; no heuristic joining |
| `Cloid` | named distinct identifier; no subfields frozen | intent/order/query/fill | stable across ambiguity; exact format external |
| `FillEvent` | `fill_id`, `cloid?`, `oid?`, `market_id`, `side`, `price_ticks`, `size_lots`, `fee_asset?`, `fee_amount`, `exchange_ts?`, `recv_ts`, `source` | live/emulator/reconciliation -> reducer | append/dedupe once; actual exposure truth |
| `ReservationState` | `balance_reservations`, `book_reservations`, `risk_reservations`, `version` | Reservation owner -> Execution/Risk | single owned/versioned state |
| `BalanceReservation` | `reservation_id`, `execution_id`, `asset_id`, `amount`, `created_at`, `state` | Reservation engine | locks balance before order |
| `BookCapacityReservation` | `reservation_id`, `execution_id`, `market_id`, `side`, `notional`, `depth_band`, `book_version` | Reservation engine | stale capacity revalidated |
| `RiskReservation` | `NOT FROZEN IN SRC-005` in reviewed schema excerpts | Risk/Reservation | no fields invented in PASS 04 |
| `ExecutionForecast` | `execution_plan_candidate_id`, `p_full`, `p_partial`, `p_recovery`, `p_failure`, `expected_pnl`, `pnl_quantiles`, `probability_positive`, `expected_shortfall`, `expected_fees`, `expected_slippage`, `confidence`, `simulation_version` | Simulator -> Risk/Execution | forecast never becomes fill truth |
| `RiskDecision` | `decision_id`, `risk_snapshot_id`, `allowed`, `action`, `max_allowed_size`, `required_price_limits`, `hard_rejects[]`, `warnings[]`, `created_at` | Risk -> Execution | current/version-compatible allow required |
| `TimerEvent` | `RiskRecheck`, `MakerExpiry`, `UnknownResolutionTimeout`, `ReconciliationTrigger`, `MetricsFlush` | clock/replay -> reducer | strategic time is replayable input |
| `RunMode` | `Replay`, `Paper`, `Shadow`, `MicroLive`, `Live` | manifest/runtime -> adapters/core | cannot change strategy logic/math |
| `ExecutionTransport` | conceptual `submit(...)`, `cancel(...)`, `query(...)`; implementations `HyperliquidHttpTransport`, `HyperliquidWsTransport`, `ReplayTransport`, `PaperTransport`, `NullShadowTransport` | effect layer | transport separate from economics |
| `TransportRequest` | `signed_intent`, `transport_type`, `request_id`, `send_at?` | Coordinator -> transport | request correlation preserves intent |
| `ReplayTransport` | consumes `OrderIntent`; emulator emits `OrderEvents`, `FillEvents` | Replay adapter -> same reducer | event schema parity |
| `DecisionTrace` | `ordered_decisions[]`, `order_intents[]`, `state_transitions[]`, `risk_decisions[]` | core -> Replay/Validation | deterministic inputs yield same trace |
| `InventoryState` | `positions_by_asset`, `targets`, `bands`, `net_flows`, `classifications`, `version` | Inventory -> Execution/Risk | updated immediately from fills |
| `AccountState` | `balances`, `open_orders`, `fills_ledger`, `fee_state`, `reconciled`, `state_version` | account owner -> core | actual/account truth versioned |
| `ExecutionJournalEvent` | `journal_seq`, `event`, `timestamp`, `checksum?` | reducer -> async journal | append-only, idempotent replay |
| journal event names | `ExecutionCreated`, `ReservationCreated`, `OrderIntentCreated`, `OrderSent`, `FillApplied`, `CancelRequested`, `RecoveryStarted`, `ExecutionCompleted` | core -> persistence | critical lifecycle evidence |
| reconciliation record | `NOT FROZEN IN SRC-005` as a standalone schema | Reconciliation/Data | state names/algorithm fixed; fields PASS 06 |
| recovery record | `NOT FROZEN IN SRC-005` as a standalone schema | Recovery/Data | state semantics fixed; fields PASS 06 |

## Boundary findings

“Inventory snapshot” in this pass maps to the frozen `InventoryState`; no separate `InventorySnapshot` fields were found. Standalone Recovery/Reconciliation record schemas are not frozen in SRC-005, so PASS 04 specifies required semantics/provenance without inventing fields. PASS 06 must close exact schemas and event ordering.
