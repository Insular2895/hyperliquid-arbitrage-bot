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

## PASS 03 — Counterfactual Simulator disposition

- `EXT-001`: current price-time priority, IOC, ALO/Post Only, GTC, batching/action ordering and matching details must be revalidated before Exchange Emulator implementation/claim.
- `EXT-002`, `EXT-004`, `EXT-005`: current payloads, timestamps, sequence/block semantics, L2 granularity, metadata, precision, fees and reconnect/gap behaviour affect arrival/mechanics/Data contracts.
- `EXT-007`: current L4 availability and `order_book_server` spot support remain unverified; F2 initial capability must work from L2 uncertainty.
- `EXT-016`: Queue-Reactive/Hawkes/OFI/resilience/ABIDES/square-root-impact literature motivates Research candidates only; transferability requires primary-source review and Hyperliquid temporal OOS evidence.
- No web revalidation occurred in PASS 03. These snapshots do not block documentation reconstruction; they can block implementation assumptions, fidelity claims, model promotion, or production activation.

## PASS 04 — Execution disposition

- `EXT-001`: revalidate current IOC/FOK/ALO/GTC and marketable-limit semantics, price-time/order status behaviour, batching/action ordering, and reject/status values before encoding transport/emulator rules.
- `EXT-002`: revalidate current HTTP/WS submit/query/cancel paths, order/open-order/fill/balance sources, subscription names, snapshots/gap recovery, and reconnect behaviour.
- `EXT-004`: revalidate tick/lot/price/significant-figure/minimum-notional/rounding rules used by QF-007/008 and next-leg/dust decisions.
- `EXT-008`: revalidate CLOID lookup/cancel behaviour, nonce/signer/API-wallet/subaccount constraints, rate limits, and `scheduleCancel` deadlines/trigger limits/scope.
- `EXT-003`: revalidate fee schedule and debit asset for actual leg/route accounting.
- No web research occurred in PASS 04. Internal fail-conservative semantics are locked, but these facts can block implementation, emulator fidelity, Micro-live, or Live activation.

## PASS 05 — Risk disposition

- `EXT-001`: current ALO/Post Only, IOC/FOK, protected-limit and order-state semantics affect maker/taker/transport gates.
- `EXT-002`, `EXT-005`: current feed payloads, timestamp/sequence/gap/reconnect semantics determine whether market state and freshness can be valid.
- `EXT-003`: current fees/tier/debit-asset behavior must be known before economic or Risk permission.
- `EXT-004`: current tick/lot/minimum/precision and metadata-change behavior are mandatory inputs.
- `EXT-008`: current rate-limit budgets, CLOID lookup/cancel and `scheduleCancel` behavior affect safety-capacity reservations and recovery.
- `EXT-006`, `EXT-007`: node/L4 capability remains future-gated; Risk cannot assume a fidelity not supplied by the validated feed.
- `EXT-015`, `EXT-016`: runtime/library status and external research can motivate validation but cannot create risk permission.
- No external browsing/revalidation occurred in PASS 05. These facts do not block documentation reconstruction; they block encoding current exchange constants, emulator claims or Live activation without verification.

## PASS 06 — Data / Recorder / Replay disposition

- `EXT-002`/`EXT-005`: verify current Hyperliquid public/account payload fields, timestamp provenance/units, sequence guarantees, block identifiers, snapshot/diff behavior, reconnect/resubscribe and gap-recovery semantics.
- `EXT-003`/`EXT-004`: verify current fees/debit asset, metadata, tick/lot/precision/minimum rules and historical availability needed for point-in-time replay.
- `EXT-006`/`EXT-007`: verify current node/order-book-server data fields, ordering, completeness, spot/L2/L4 support before declaring higher-fidelity Source behavior.
- Historical archive completeness and official dataset cadence/retention must be verified before using them as a replacement or supplement for proprietary RAW.
- No web/external revalidation occurred in PASS 06 by explicit mission rule. These facts do not block documentation reconstruction; they can block adapter schemas, dataset fidelity claims, emulator validity or Live activation.

## PASS 08 — Market Graph / Routes / Atlas / Quant disposition

- `EXT-003`: verify current spot fee schedule, account tiers/discounts, maker/taker treatment, pair/quote-specific treatment and fee debit asset before implementing QF-014–016 or evaluating Live route economics.
- `EXT-004`: verify current spot metadata schema, market/base/quote identifiers, `szDecimals`, tick/lot/significant-figure/price rules, minimum quantity/notional, rounding and market status/change semantics.
- `EXT-002`/`EXT-005`: verify public L2 subscription/payload, depth/aggregation, snapshot/diff/update ordering, timestamps, sequencing, gap/reconnect behavior and available spot-market discovery before BookVersion/freshness assumptions.
- `EXT-001`: verify current matching/marketable-limit and protected-order mechanics needed by exact book-walk-to-execution parity.
- `EXT-016`: academic examples/statistics remain research motivation; they do not calibrate Hyperliquid HWC, competition, survival, latency or route profitability.
- No web research occurred in PASS08 by explicit mission rule. These items do not block documentary reconstruction, but they can block exact adapters, Formula golden vectors tied to exchange behavior, Shadow/Micro-live claims or Live activation.
