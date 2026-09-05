# Test Family Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Family | Required use | Core assertion/artifact |
|---|---|---|
| Unit | pure calculations, guards, reducers, mappings | exact input/output and reason |
| Golden | formulas, book walk, precision, Replay fixture | stable expected artifact/hash |
| Property | invariants across generated inputs | invariant holds or minimal counterexample |
| Integration/contract | adapters, persistence, transport, signer, schema | boundary compatibility and safe failure |
| Replay | causal ordered historical/failure behavior | RunManifest, no lookahead, repeated trace equality |
| Fault injection | every relevant dependency and state transition | expected state, permission, actions and recovery proof |
| Load | sustainable throughput/resource envelope | no loss/unsafe backlog; headroom and scope |
| Performance | latency and jitter distributions | P50/P95/P99/P99.9/MAX, count, regime and instrumentation |
| Shadow | production core on live data/no effects | would-decide/execute, stability, drift, zero account mutation |
| Micro-live | real execution under strict caps | predicted/actual fills, slippage, latency, recovery, PnL |
| Chaos/drill | multi-failure and operational recovery | safety, containment, evidence and time-to-recovery |

Every test declares owner, requirement IDs, preconditions, oracle, expected permission state, data/version scope, artifacts, repeatability, cleanup and escalation. “Process stayed up” is insufficient because incorrect orders, stale readiness, lost evidence or unreconciled capital may coexist with uptime.
