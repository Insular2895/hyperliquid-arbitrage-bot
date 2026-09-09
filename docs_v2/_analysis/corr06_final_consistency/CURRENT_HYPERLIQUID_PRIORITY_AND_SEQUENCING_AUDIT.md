# Current Hyperliquid Priority and Sequencing Audit

`EXTERNAL_REVALIDATION — retrieved 2026-09-09`

## Sources and version evidence

| Source | Version evidence | Scope | Revalidate |
|---|---|---|---|
| [Priority fees](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/priority-fees) | live GitBook; retrieval date, no immutable page version | gossip/read and IOC/ALO write priority | before any experiment or activation; on page/network change |
| [Optimizing latency](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/optimizing-latency) | live GitBook; retrieval date | read/write guidance and sequencing | before encoding a latency assumption |
| [Exchange endpoint](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/exchange-endpoint) | live GitBook; retrieval date | TIF, responses and cancel/fast fields | before adapter/emulator implementation |
| [Node repository](https://github.com/hyperliquid-dex/node) | `405cc08b17a727ee51b0f9128918955a84439915` | node outputs and `split_client_blocks` | before node prototype/rental |
| [Foundation non-validating node](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/nodes/foundation-non-validating-node) | live GitBook; retrieval date | Foundation peer scope, limitations and eligibility | before relying on or requesting access |
| [Order-book server repository](https://github.com/hyperliquid-dex/order_book_server) | `8b4f237904f683aca2dba21a07d87e831ead2a97` | local L2/L4 service limits and spot support | before any local-book prototype |
| [Official Python SDK](https://github.com/hyperliquid-dex/hyperliquid-python-sdk) | `2fdb18f9517675ea03695a0962bd19eece9c83f0` | implementation reference only, not protocol authority | before borrowing adapter behavior |
| [WebSocket subscriptions](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/websocket/subscriptions) | live GitBook; retrieval date | public stream schemas | before adapter/release |
| [Order types](https://hyperliquid.gitbook.io/hyperliquid-docs/trading/order-types) | live GitBook; retrieval date | IOC/ALO/GTC user semantics | before emulator/Live |
| [Nonces/API wallets](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/nonces-and-api-wallets) | live GitBook; retrieval date | signer nonces and batching | before execution transport |
| [Rate limits](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/rate-limits-and-user-limits) | live GitBook; retrieval date | IP/address/WS capacity | before transport/load planning |

## Gossip/read priority

- Two independent Dutch slot auctions share a three-minute schedule; results apply to the following auction period.
- Lower slot index is strictly prioritized; multiple won slots for one IP are not additive and the lowest slot controls.
- A node optionally interprets the on-chain ordering for peer sends. The exact on-chain IP must match the peer-seen IP. Every network hop may or may not respect it, so effect has p2p variance.
- It affects all mempool-stream data equally and applies to normal client blocks including responses as well as split client blocks. It is read-only, not order-send priority.
- Charge comes from spot balance, is burned and is denominated in HYPE gas units (`0.00000001 HYPE`). Auction state is queryable with `gossipPriorityAuctionStatus`; bids use `gossipPriorityBid` with slot/IP/maxGas. Reset is ten times the prior winning price with a documented 0.1 HYPE minimum.
- The page currently reports an empirical mainnet effect of about 25 ms per auction slot. This is a dated empirical observation, not a guarantee or a project constant.

## Order/write priority common scope

Grouping is supported only when every order is non-outcome and the group is either all IOC or all non-reduce-only ALO. `{"p":12345}` means rate `p/100000000`. Charge comes from undelegated staking balance, is converted to HYPE using spot mark price and is burned. Read and write mechanisms are independent.

## IOC priority

- Charge basis is filled notional. A true zero-fill IOC therefore has zero priority charge under this mechanism.
- Official docs describe linear end-to-end temporal preference from 0–8 bps (`p=80000`) and about 45 ms empirical mainnet reduction per 1 bp. Both are current-doc semantics/empirics, not guaranteed fill benefit.
- Maximum rate is 100%. From 8 bps to 100%, mempool time preference is identical; for similarly timed IOC in the documented 70 ms Unix bucket, higher fees usually sort first.
- Cancels remain ahead of all immediately executable orders. Effective ordering is described through arrival time plus a decreasing fee-dependent function, with zero adjustment for prioritized cancel actions.
- Paid IOC amount is available in node `user_fills.priorityGas`.

## ALO priority

- Charge basis is resting notional, deducted at placement whether or not the order later fills.
- It reorders only the tail at each price level consisting of orders placed within the prior continuous 400 ms window.
- Unlike IOC, it does not change mempool priority: ALO transactions remain FIFO with end-to-end behavior similar to cancels; priority changes queue position after L1 application.
- The raw-book-diff `insertBefore` field is the official implementation signal cited for reconstructing priority-aware level ordering.

## Cancel / ALO / IOC and split blocks

The latency guide says cancels and ALO sent at the same time almost always execute before IOC/GTC, spanning multiple blocks, and that bundles process ALO/cancels before other transactions. This is current guidance, not a universal fill guarantee. The Node README still says `split_client_blocks:true` streams eager uncommitted mempool transactions without responses, requires the whole peer path to enable it and is random by default unless the node respects auction ordering. It remains `NON-CANONICAL` and cannot authorize a real send or produce actual outcome truth.

The Foundation non-validating-node page still characterizes its service as best effort, gives no availability/latency/performance/completeness guarantee, and says it must not be the sole authoritative source for trading or other time-sensitive activity. The official `order_book_server` HEAD still carries its standalone/as-is warning, lacks spot order books and batches node output by block. These current limitations preserve the public-feed baseline and challenger-only treatment; they do not prevent bounded measurement.

## Consequence

CORR-04's `HF-022` absence finding is superseded. The architecture does not automatically activate priority: typed policy, matched evidence, cost-once accounting, Risk compatibility and human/Validation gates remain mandatory.
