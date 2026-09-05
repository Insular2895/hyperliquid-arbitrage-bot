# Evidence Type Catalog

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

An `EvidenceId` is a stable identifier for an immutable evidence package, not a mutable dashboard URL. Every package identifies scope, claim, test/metric version, run/build/config/model/formula/schema, dataset/source interval, infrastructure, start/end, seed where relevant, expected/observed outcome, validity/exclusions, artifact hashes, reviewer/decision and unresolved deviations.

| Evidence type | Proves | Does not prove |
|---|---|---|
| specification review | M0 completeness and ownership | implementation behavior |
| unit/property/golden | local invariants and exact fixtures | realistic market interaction |
| integration/contract | boundary compatibility and effects | historical/live calibration |
| deterministic Replay | same core over ordered point-in-time evidence, failures and counterfactuals | our causal market impact |
| performance/load | distributions, tails, headroom and degradation | economic validity alone |
| Shadow | live-data decisions, support, latency and stability without orders | real fill/queue/impact/account mutation |
| Micro-live | real execution/calibration under small limits | larger size or new-market capacity |
| sustained Live | behavior inside the exact promoted scope | permanent or unbounded validity |
| fault/chaos drill | specified safe state/action/recovery under injected failure | correctness if only non-crash is observed |
| incident reconstruction | what occurred and whether it is reproducible | resolution by itself |
| external-fact validation | current exchange/platform/security semantics | internal code correctness |

Notebook-only results, unversioned screenshots, averages without count/tails, missing negative results and reports whose inputs cannot be resolved are not promotion evidence.
