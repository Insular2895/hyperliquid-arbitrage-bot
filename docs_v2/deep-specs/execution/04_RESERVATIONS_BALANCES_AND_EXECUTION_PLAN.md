# 04 — Reservations, balances, and immutable execution plan

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Reservation-before-order invariant

```text
VALIDATING -> RESERVING -> PLANNED -> intent -> nonce -> sign -> send
```

No order intent may consume unreserved economic or operational capacity. The reservation operation is atomic as a set: partial acquisition followed by failure releases only what is proven safe to release.

## Three capacity classes

| Reservation | Protects | Required provenance | Revalidation |
|---|---|---|---|
| `BalanceReservation` | actual asset funds from double-spend | `reservation_id`, `execution_id`, `asset_id`, `amount`, `created_at`, `state` | account/reservation version |
| `BookCapacityReservation` | observed liquidity/depth from concurrent overcommit | `reservation_id`, `execution_id`, `market_id`, `side`, `notional`, `depth_band`, `book_version` | current book/validity envelope |
| `RiskReservation` | route/order/portfolio and API capacity budget | Data-owned exact schema | current Risk/config/infra state |

The first two field lists are SRC-005 exact. `ReservationState` contains `balance_reservations`, `book_reservations`, `risk_reservations`, and `version`. This pass does not invent a field layout for `RiskReservation`.

## Balance equations and concurrency

QF-073 closes `AvailableBalance[a] = ActualBalance[a] - ReservedBalance[a]`. QF-074 closes available book capacity as observed capacity minus already reserved capacity. Both are derived, never independently writable. Shared balance/book capacity is admitted by the single owner against one current version so two routes cannot pass on the same units.

Invariants:

- available cannot exceed actual;
- reserved/available cannot be negative under valid units;
- sum of active reservations cannot exceed proven current capacity;
- a stale book reservation cannot justify send on a materially changed book;
- affected unknown capital is unavailable to allocation/sizing/new routes.

## `ExecutionPlan` construction

After a favourable current `RiskDecision` and complete reservation set, Execution builds the exact SRC-005 plan contract: `execution_id`, `opportunity_id`, `route_id`, `size`, `legs[]`, `execution_mode`, `reservations[]`, `risk_decision_id`, `model_versions`, `config_versions`, `created_at`, `plan_version`.

Each `ExecutionLegPlan` has `leg_id`, `market_id`, `input_asset`, `output_asset`, `role`, `order_policy`, `expected_input`, `expected_output`, `protected_price`, `max_slippage`. These are planning facts. Actual fills must populate separate actual state; they never mutate the expected fields into false history.

## Immutability/versioning

At `PLANNED`, economic fields freeze. A change to size, protected price/slippage envelope, route/leg ordering, role, policy, Risk decision, model/config basis, or reservations yields a new linked version such as the source’s `ExecutionPlanV2`; it is not an in-place patch.

Immediately before send, the coordinator checks current state against the plan validity envelope. The source permits concepts such as maximum book-version age, price bounds, and maximum edge deterioration, but exact gates are calibrated/owned by the relevant passes. Envelope breach produces replan/new version or abort.

## Lifecycle accounting

| Outcome | Used portion | Unused portion | Release condition |
|---|---|---|---|
| definite zero fill/reject before exposure | none | all | order/route terminal reconciliation |
| partial fill | converted to actual exposure | held for live/uncertain remainder | cancel/final fill + reconciliation |
| full fill | converted to actual exposure | rounding remainder if any | final reconciliation |
| cancel requested | fills may still consume | held | confirmed cancel plus fill/balance reconciliation |
| `UNKNOWN` | potentially consumed | all affected remains locked | exchange truth resolved |
| recovery | converted/held according to actual recovery fills | conservative remainder | recovery verification + reconciliation |

Reservations are not released from a local timeout, send exception after possible transmission, or cancel request alone.
