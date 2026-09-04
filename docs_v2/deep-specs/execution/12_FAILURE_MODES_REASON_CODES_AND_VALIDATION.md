# 12 — Failure modes, reason codes, and validation

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Failure semantics

Failures are classified by what is known about economic exposure. A known pre-transmission validation/reservation/signing failure can abort safely. Anything after possible transmission that lacks exchange proof becomes pending/unknown and keeps resources locked. Later-leg failure with prior fill is a Recovery trigger, not an order-only error.

The full 26-case table is [EXECUTION_FAILURE_MATRIX](../../_analysis/pass04_execution/EXECUTION_FAILURE_MATRIX.md). No path maps every problem to `ORDER_FAILED`.

## Reason codes

The canonical family vocabulary is `MARKET_DATA`, `RISK`, `INVENTORY`, `LIQUIDITY`, `SIMULATION`, `INFRA`, `EXCHANGE`, `EXECUTION`, `RECONCILIATION`, and `MODEL`. Source examples include `EXCHANGE_MIN_NOTIONAL`, `EXCHANGE_INVALID_TICK`, `EXCHANGE_BAD_ALO`, `BOOK_STALE`, `CAPACITY_RESERVED`, `INVENTORY_HARD_LIMIT`, `EDGE_DIED`, `SIMULATION_LOW_CONFIDENCE`, `ORDER_UNKNOWN`, and `BALANCE_MISMATCH`.

Current exchange strings may map, for example, from minimum-notional/bad-ALO/insufficient-balance rejects, but exact current spelling is external. PASS 04 preserves source examples and does not declare a final exhaustive enum.

Distinguish local validation reject, Risk reject, precision/quantization reject, reservation/capacity reject, protected-price zero fill, exchange reject, transport uncertainty, stale plan, and reconciliation mismatch. Every rejected candidate is retained to avoid selection bias.

## Observability contract

Each transition emits a structured record with entity, from/to, reason, timestamp, and correlation identity. Execution exposes counts/rates and latency distributions for executions/orders, zero/full/partial, send-to-ACK/fill, cancel/races, unknown resolution, reconciliation, recovery/loss, dust/buffer, rejection reasons, and time in Engine states. Metrics/log delivery must not block the hot path; PASS 10 owns the backend.

## Validation layers

1. Unit tests: reducer transitions, guards, quantization interfaces, reservation arithmetic, fill dedupe, reason mapping.
2. Property tests: non-negative/conservative quantities, terminal monotonicity, idempotence, no unknown-capital reuse.
3. Deterministic Replay: ordered events, timers, modes, restart/journal, same trace identity.
4. Fault injection: network response loss, duplicate/out-of-order events, feed/clock/process failure, persistence lag.
5. Shadow: would-submit plans, freshness, forecasts, state timings, no actual effect.
6. Micro-live: real send/ACK/fill/partial/fees/cancel/recovery/reconciliation under calibrated tiny authority.

## Required scenarios

- full IOC TT success and exact route actuals;
- first-leg zero fill and no next leg;
- every-leg partial with actual-size propagation;
- later-leg edge death/reject/zero and Recovery;
- order filled but submit/ACK response lost, resolved by CLOID without duplicate;
- duplicate fill and incompatible late/out-of-order event;
- fill during cancellation and cancellation after partial;
- crash after send, after fill, and during Recovery;
- local/exchange balance mismatch preventing `READY`;
- market-feed and account-feed loss/reconnect;
- stale maker, maker partial below minimum, dust/buffer expiry;
- protected-price refusal without widening;
- recovery partial/failure/split and reconciliation timeout.

## Promotion/failure criteria

Capabilities advance only when required lower-layer evidence passes and observed Micro-live behaviour remains calibrated. Failure includes invariant violation, duplicate economic application, terminal regression, theoretical-size continuation, false zero/cancel, reservation leak/reuse, unresolved mismatch admitted to `READY`, mode divergence, or missing provenance. Numeric tolerances/maturity gates are set by Validation/Risk/Data owners and are not invented here.
