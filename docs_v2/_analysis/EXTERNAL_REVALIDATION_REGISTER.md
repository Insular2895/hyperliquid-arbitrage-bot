# External Revalidation Register

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| ID | Fact family | Source(s) | Why date-sensitive | Future pass | Blocks reconstruction? |
|---|---|---|---|---|---|
| EXT-001 | Hyperliquid order types/matching/batching mechanics | SRC-002/004/008 | Exchange behavior can change | PASS 04/11 | NO |
| EXT-002 | API/WS endpoints, subscriptions, snapshots and reconnect behavior | SRC-002/004/006 | API contracts evolve | PASS 04/06/09 | NO |
| EXT-003 | Fees, tiers and debit asset behavior | SRC-002/003/004 | Commercial rules evolve | PASS 08/11 | NO |
| EXT-004 | Metadata, precision, lot/tick/minimum rules | SRC-001/002/004 | Exchange rules evolve | PASS 06/08 | NO |
| EXT-005 | Public feed cadence/fields and trade identities | SRC-002/007/008 | Feed schemas/cadence evolve | PASS 02/06 | NO |
| EXT-006 | Node requirements, flags, outputs and region recommendation | SRC-002/007/008 | Node software/docs evolve | PASS 01/06 | NO |
| EXT-007 | order_book_server L2/L4/spot support | SRC-002/007/008 | Repository capability can change | PASS 01/03 | NO |
| EXT-008 | Hyperliquid rate limits and scheduleCancel | SRC-004/006/008 | Limits and features evolve | PASS 04/09 | NO |
| EXT-009 | TradingFX plans/prices/OS/network claims | SRC-008 | Commercial snapshot | PASS 01 | NO |
| EXT-010 | Akamai/Linode G7 specs/price/region | SRC-008 | Commercial snapshot | PASS 01 | NO |
| EXT-011 | Kamatera Type B specs/price/reservation | SRC-008 | Commercial snapshot | PASS 01 | NO |
| EXT-012 | AWS Lightsail specs/price/AZ rationale | SRC-008 | Commercial snapshot/inference | PASS 01 | NO |
| EXT-013 | Sakura specs/price/trial | SRC-008 | Commercial snapshot | PASS 01 | NO |
| EXT-014 | Cherry VDS specs/price/availability | SRC-008 | Commercial snapshot | PASS 01 | NO |
| EXT-015 | SDK/library versions and official support status | SRC-002/006 | Software versions evolve | implementation planning | NO |
| EXT-016 | Academic paper claims and dataset statistics | SRC-002/003/007/008 | Citation/application verification | PASS 02/03/08 | NO |

## PASS 01 — Infrastructure disposition

- `EXT-002`, `EXT-005`, `EXT-006`, `EXT-007`, `EXT-008`, `EXT-009`–`EXT-015` were reviewed for Infrastructure dependencies.
- No live external verification was performed during PASS 01.
- Provider prices/specifications, Tokyo availability, OS/allocation/network claims, feed timestamp semantics and node/order-book-server capabilities remain historical source snapshots.
- These facts do not block documentation reconstruction; they can block candidate admission, purchase, benchmark validity, implementation assumptions or production deployment.
- The per-fact register is `pass01_infrastructure/INFRA_EXTERNAL_SNAPSHOTS.md`.

## PASS 02 — Market Participants disposition

- `EXT-005`: current public book/trade cadence, timestamp semantics, buyer/seller counterparty fields and completeness remain unverified source snapshots. Address behaviour and fine response horizons cannot depend on them until revalidated.
- `EXT-006`: node raw-book-diff, order lifecycle and output semantics remain future/external-dependent.
- `EXT-007`: current L2/L4 and spot support remains unverified; no exact L4 queue or fine reaction-time claim is made.
- `EXT-016`: academic results motivate candidates only. Their dataset claims and transferability to Hyperliquid require source verification and local temporal OOS evidence.
- No live external query was performed in PASS 02. These facts do not block documentation reconstruction but can block data collection, model fidelity, activation or production claims.
