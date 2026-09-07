# External Revalidation Propagation Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| External ID | Fact family | Required consumers/gates | Propagation result |
|---|---|---|---|
| `EXT-001` | matching/order types/batching | Formula book-walk mapping, Emulator, Execution transport, Risk | PRESENT; blocks exchange-bound implementation/Live claim |
| `EXT-002` | API/WS endpoints/payload/reconnect | Adapters, Data, Reconciliation, Deployment | PRESENT |
| `EXT-003` | fees/tiers/debit asset | Formula, Inventory, Accounting, Risk | PRESENT; `P14-009` |
| `EXT-004` | metadata/tick/lot/minimum | Precision, Formula, Graph, Execution | PRESENT |
| `EXT-005` | feed cadence/fields/identity | Data quality, Participants, freshness | PRESENT |
| `EXT-006` | node requirements/outputs/region | Infrastructure, Data, Future gate | PRESENT |
| `EXT-007` | order-book-server L2/L4/spot support | Simulator fidelity, Participants, Node gate | PRESENT |
| `EXT-008` | rate limits/CLOID/scheduleCancel | Execution, Recovery, capacity, safe shutdown | PRESENT |
| `EXT-009` | TradingFX snapshot | provider benchmark/purchase | PRESENT |
| `EXT-010` | Akamai/Linode snapshot | provider benchmark/purchase | PRESENT |
| `EXT-011` | Kamatera snapshot | provider benchmark/purchase | PRESENT |
| `EXT-012` | Lightsail snapshot | provider benchmark/purchase | PRESENT |
| `EXT-013` | Sakura snapshot | provider benchmark/purchase | PRESENT |
| `EXT-014` | Cherry snapshot | provider benchmark/purchase | PRESENT |
| `EXT-015` | SDK/runtime/library support | implementation and supported-platform matrix | PRESENT |
| `EXT-016` | academic claims/datasets | model candidate justification and local OOS validation | PRESENT; never production truth |

No external fact was revalidated in PASS 14, by design. Internal fail-closed contracts remain usable for documentation; current external facts can block adapter encoding, emulator fidelity, purchases, deployment support, Micro-live or Live. Missing external-fact destination: **0**.
