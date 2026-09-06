# Control Plane vs Data Plane

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Plane | Contents | Latency relation | Authority |
|---|---|---|---|
| Trading/data plane | market/account events, ordered reducers, Book/rules, Graph/routes, features, decisions, Risk, reservations, execution, fills | bounded hot/near-line | owns current economic facts and per-action permission |
| Evidence/model plane | Recorder, Replay, datasets, training, Atlas aggregates, predicted/actual, validation reports | async/offline | produces evidence and candidate artifacts, not immediate permission |
| Control/operations plane | resolved config, model/capability promotion, readiness/health, deployment, license, update, diagnostics, operator commands | atomic snapshot reads; no synchronous remote dependency | narrows or changes future permitted scope under governance |

## Allowed interactions

- Control → trading: immutable resolved config, signed model/capability/license state, health and lifecycle events through the ordered boundary.
- Trading → evidence: non-blocking event/metric enqueue and immutable snapshots.
- Evidence → control: reports, artifacts and explicit promotion/demotion proposals.
- Operations → trading: scoped halt/risk-off/shutdown commands; never direct state writes or `ALLOW` bypass.
- Trading → external: only transport effects after Risk/reservation; observations return as events.

## Forbidden interactions

Remote license/telemetry/registry/admin/database calls in the hot path; model trainer mutating Live weights; operator editing memory; Deployment setting READY without reconciliation; control-plane failure disabling Recovery or data access; health service inventing economic state.

Control-plane versions are pinned into plans/traces. A material update invalidates or revalidates future authorization; it never rewrites prior intent or exchange facts.
