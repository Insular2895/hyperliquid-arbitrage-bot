# Node Deployment Topology Study

`STATUS: RESEARCH — NO DEPLOYMENT`

| Topology | Candidate benefit | Main cost/risk | Disposition |
|---|---|---|---|
| `N-A` node + bot same host | minimal local hop, one clock | severe CPU/RAM/disk/network contention; large host; wider attack surface | benchmark only after gate |
| `N-B` dedicated node near bot | resource/security isolation | second host/link/clock, cost and failure surface | preferred serious challenger pattern |
| `N-C` remote region-local node | operational separation/peer choice | route and clock confounding; latency not assured | compare as end-to-end topology |
| `N-D` public feed | lightweight, supported initial path | public cadence/route limitations | canonical baseline |

For N-A measure engine alone, node alone, engine+node, Recorder alone and relevant combinations. For N-B/N-C authenticate the link, bound queues, record link RTT/gaps/reconnect and deny signer access to the node by default. No shared node service or multi-tenant trust model is implied.

The node’s published minimums materially exceed the initial trading VPS. Combining roles is therefore never inferred from the 4 GB baseline.
