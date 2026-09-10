# Async / Concurrency Architecture — Baseline and Scope

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| Field | Value |
|---|---|
| Repository | `Insular2895/hyperliquid-arbitrage-bot` |
| Branch | `codex-docs` |
| `ASYNC_ARCH_BASELINE_COMMIT` | `44b1042371ed996dc97f9fae310a1cd36fe370df` |
| Candidate documentation | `docs_v2/` |
| Legacy documentation | `docs/` — read-only |
| Runtime architecture | one client/container/main Rust process; modular monolith |
| Implementation | `NOT AUTHORIZED` |
| Approval | `PENDING FINAL REVIEW` |

## Audit question

Verify the supplied reference model against the current canonical architecture, keep correctness ownership intact, and distinguish locked safety semantics from performance choices that require measurement. This pass changes documentation only.

## Result

The reference model is compatible with the repository when expressed as:

> async external I/O; incremental state where possible; cheap bounded compute inline; expensive pure compute in bounded snapshot workers only when justified; ordered decision and one logical writer for canonical commit; background durability/observability; offline research.

Or: **parallel to calculate, ordered to decide, single-writer to commit**.

No microservice split, broker, remote database, remote model, second engine or distributed commit system is introduced. Tokio-style asynchronous waiting is not permission to run CPU-heavy work on I/O executors. A worker result, effect response, ACK or background output is evidence/proposal until the ordered owner accepts it.

## Authorities inspected

- Masters 00, 03, 04 and 06–19, with Formula Book QF-001–110 unchanged.
- PASS 06 Data/Recorder/Replay, PASS 13 architecture and PASS 14–16 closure artifacts.
- CORR-01 timing/evidence, CORR-02 hot-path/single-writer/backpressure, CORR-03 execution outcomes, CORR-04 source/infrastructure, CORR-05 economics and CORR-06 closure.
- `HDC-001..090`; new decisions are appended only where this human instruction adds a genuine scheduling/commit contract.
- Graphipy Maxi Brain coding architecture/workflow guidance, used as reference rather than project authority.

## Fixed and calibrated boundaries

| Boundary | Status |
|---|---|
| one ordered canonical mutation authority | `LOCKED` |
| workers/effects do not own canonical state | `LOCKED` |
| actual-fill-driven later-leg execution | `LOCKED` |
| bounded queues and task population | `LOCKED` |
| stale result cannot commit | `LOCKED` |
| worker completion order cannot determine economic priority | `LOCKED` |
| inline full-L2, small q-grid and local signing | initial baseline; challengers benchmarked |
| route fanout worker pool | `BENCHMARK CANDIDATE` |
| `BATCH_SELECT` versus deterministic `EARLY_COMMIT` | `CALIBRATED / REPLAY + SHADOW REQUIRED` |
| worker count, queue capacity and deadlines | `CALIBRATED`; no numeric value frozen |
| adaptive route policy | `RESEARCH` only |

## Explicit non-goals

- no implementation, dependency, build, Docker or runtime-config change;
- no new QF and no formula, Risk, Execution, Recovery, Reconciliation, accounting or `Q_validated` semantic change;
- no Phase 27;
- no claim that parallelism improves latency or economics before evidence;
- no legacy `docs/` mutation.
