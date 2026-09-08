# CORR-01 — Baseline and Scope

DOCUMENTATION STATUS: POST-RECONSTRUCTION CORRECTION — AWAITING HUMAN REVIEW

## Frozen baseline

| Field | Value |
|---|---|
| Baseline commit | `fdb4a25588670fb245edebc0650d262c7f536b4c` |
| Branch | `codex-docs` |
| Inspection date | 2026-09-08 |
| PASS 16 | complete; human approval `PENDING` |
| Implementation | `NOT AUTHORIZED` |
| Legacy switchover | `NOT AUTHORIZED` |
| Human decision origin | `HUMAN_POST_RECONSTRUCTION` |

The correction strengthens the V2 documentation after reconstruction. It does not claim that capture instrumentation exists, does not authorize implementation or capital, and does not alter the eight-source PASS 00 inventory.

## In scope

- a canonical analytical funnel from market observation through reconciled economic outcome;
- exact separation of evaluation, opportunity, eligibility, attempt, fill, completion, reconciliation and positive PnL;
- an offline/near-line `OpportunityEpisodeId` grouping contract;
- correlation from market evidence to route, execution, order, fill, recovery, reconciliation and PnL;
- named timing points, derived stage latencies and measurement validity;
- metric numerator, denominator, population, exclusions, scope, time basis and missing-data policy;
- immutable predicted-versus-actual pairing;
- evidence requirements before an optimization or infrastructure change is promoted.

## Out of scope

- implementation, telemetry backend selection, tracing library selection or database schema migration;
- benchmark execution, production tuning or infrastructure selection;
- any new Runtime Capture Engine or sixth execution state machine;
- changes to QF-001 through QF-110, Risk hierarchy, execution transitions or exchange semantics;
- CORR-02 through CORR-06;
- legacy `docs/**`, code, tests, CI, Cargo, Docker or runtime configuration.

## Authority and compatibility

The canonical runtime owners remain Market Graph, Simulator, Risk, Execution, Data, Recorder/Replay and Accounting. The Capture Funnel is a derived evidence projection over their events and states. When a dashboard conflicts with canonical records, canonical records win and the projection is invalidated.

The six explicit post-reconstruction decisions are registered in [`POST_RECONSTRUCTION_HUMAN_DECISIONS.md`](../POST_RECONSTRUCTION_HUMAN_DECISIONS.md). Existing formula semantics and safety contracts remain unchanged.
