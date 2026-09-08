# `split_client_blocks` Current Fact Audit

`EXTERNAL_REVALIDATION_RESULT: FEATURE_CURRENT AT NODE COMMIT 405cc08b17a727ee51b0f9128918955a84439915`

Source: official [hyperliquid-dex/node README](https://github.com/hyperliquid-dex/node), “Streaming mempool transactions”, retrieved 2026-09-08.

| Question | Current evidence |
|---|---|
| exact field | `split_client_blocks: true` |
| config | `~/override_gossip_config.json` |
| output | `~/hl/data/mempool_txs/{date}` |
| content | eagerly broadcast client/mempool transactions |
| committed/final | no; explicitly uncommitted |
| responses | none |
| final ordering | no; default streaming order is random |
| disappear/change | possible by epistemic status; no commitment/response guarantee |
| availability | node/peer path feature; every peer between observer and validating network must enable it |
| priority option | node-side `node_gossip_priority_config.json` can respect on-chain gossip-auction priority ordering |
| future drift | docs say a later upgrade may enable it broadly or remove the option |

This feature is Research-only. Its output is `NON-CANONICAL`, never a committed book/account/fill source. It creates no order-send authority. Revalidate exact behavior, schema, peer coverage and security before any prototype.
