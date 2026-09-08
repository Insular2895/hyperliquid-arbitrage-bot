# Feed Semantic Equivalence Audit

`RESULT: NOT GENERALLY EQUIVALENT`

| Dimension | Public WebSocket | Node outputs | Consequence |
|---|---|---|---|
| unit | channel snapshot/update | block/stream/file event | adapters cannot share assumptions silently |
| cadence | channel/block-driven | flag-dependent block batching/streaming | arrival comparisons require profile metadata |
| identity | channel-specific fields | block number/event schema | common ID may be absent |
| book view | public L2/BBO | raw diffs or external reconstruction | state parity must be proved |
| account/order | subscriptions/info | optional fills/statuses/outputs | actual truth still reconciles with exchange/account evidence |
| speculative data | none asserted in canonical public contract | optional uncommitted mempool stream | separate epistemic lane mandatory |
| spot L4 | not public L4 | `order_book_server` currently no spot | no V1 spot L4 assumption |

Equivalent means identical economic interpretation for the claimed event/state, not merely same market and nearby time. Unknown/ambiguous mappings are retained as unmatched. No node field becomes canonical merely because it is richer or earlier.
