# CORR-03 — HJ Failure Suite

DOCUMENTATION STATUS: VALIDATION SCENARIOS — IMPLEMENTATION NOT AUTHORIZED

`HJ-001..010` are project scenario IDs. Only `HJ-001` and `HJ-003` have direct primary Harjus incident support; all others are project scenarios inspired by real-world failure families.

| ID | Injection | Required invariant/result |
|---|---|---|
| `HJ-001` | first risk-increasing order known zero fill/known reject; variant proves pre-transmission failure | no inventory or later leg; reconcile before release; no Recovery without exposure; no blind retry; pre-send-provable failure is not an attempt |
| `HJ-002` | Leg1 `0<filled<requested`, including below-minimum dust | apply FillEvent once; actual output—not planned q—feeds revalidation/next leg; residual explicit; Recovery/buffer policy when continuation invalid |
| `HJ-003` | Leg1 filled, later leg zero/reject/stale/edge-lost; TTT Leg3 variant | exposure remains actual; no rollback/completion; affected capital blocked; Recovery from current exposure/books |
| `HJ-004` | Leg2/3 partial | apply completed fraction; continue actual valid fraction; separately own residual/Recovery; never double-route one quantity |
| `HJ-005` | submit may have transmitted but response is lost | SENT/PENDING/UNKNOWN path; reservations lock; query/reconcile; no duplicate intent; final no-fill/fill variants retain UNKNOWN flag |
| `HJ-006` | fill arrives while cancel requested | `CANCEL_REQUESTED != CANCELED`; dedupe/apply fill; keep remainder reserved until exchange truth; reconcile final state |
| `HJ-007` | maker partial then cancel remainder | filled quantity creates exposure and drives taker continuation; canceling remainder may still fill; Recovery if continuation fails; does not validate maker Live |
| `HJ-008` | crash after SENT, after partial, during cancel or Recovery | restart `BOOTING→SYNCING→RECONCILING`; rebuild from journal+CLOID/OID+orders+fills+balances+reservations+Recovery; no new affected risk |
| `HJ-009` | duplicate/late/out-of-order fill from stream/snapshot/reconciliation | stable FillId applied once; no duplicate inventory/fee/PnL/reservation; monotonic state; incompatible evidence triggers reconciliation |
| `HJ-010` | Recovery depth constrained, order partial/unknown/failed, residual remains | actual current exposure; bounded candidates; actual fills; new plan after recompute; no blind retry; `RECOVERY_FAILED`/manual/halt on exhausted policy |

Every fixture must emit canonical transitions, Inventory/Reservation deltas, Recovery/Reconciliation evidence, funnel classification and reason codes. Dangerous failures are exercised in emulator/fault-injection/Replay, not intentionally with real capital.
