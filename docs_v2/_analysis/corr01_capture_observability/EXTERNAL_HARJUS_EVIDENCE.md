# CORR-01 — Comparative External Evidence: Harjus

DOCUMENTATION STATUS: COMPARATIVE EXTERNAL EVIDENCE — NOT A CANONICAL SOURCE

## Research record

| Field | Value |
|---|---|
| Repository | [ValtteriL/harjus](https://github.com/ValtteriL/harjus) |
| Inspected repository commit | `09816b3da2a393795250e38c8b49869b57ba4d6f` |
| Commit timestamp | 2026-03-04T20:34:31+02:00 |
| Inspection date | 2026-09-08 |
| Author write-up, releases 1–3 | [Binance Triangular Arbitrage](https://shufflingbytes.com/posts/binance-triangular-arbitrage/) |
| Author write-up, release 4 | [Harjus release 4.0.0](https://shufflingbytes.com/posts/harjus-release-4.0.0/) |
| Production log artifact | [Harjus 4.0.0 raw production log](https://gist.github.com/ValtteriL/b438a17c3c0eb61d4000ce93e9f1e39c) |
| Classification | `COMPARATIVE_EXTERNAL_EVIDENCE` |
| Source inventory effect | none; this is not `SRC-009` |

## Observations

| Observation | Evidence | Confidence | Generalizable lesson | Binance/Harjus-specific boundary | CORR-01 relevance |
|---|---|---:|---|---|---|
| The public design precomputes triangular routes, evaluates affected opportunities on BBO updates and submits limit-FOK legs when profitable. | author article plus `Opportunity.cpp`, `Worker.cpp`, `HarjusApplication.cpp` at inspected commit | high | evaluation, selected opportunity and submitted attempt are distinct moments | Binance Spot, FIX/FOK and implementation details are not imported | motivates explicit funnel boundaries |
| The releases 1–3 report says 156 opportunities in 69 hours, one successful execution and unwanted inventory from partial trading. | releases 1–3 author article | high for the reported run | a headline opportunity count and success count are not interpretable without population and partial-outcome definitions | author-run sample, Binance market and period | requires denominators, partial exposure and full-route labels |
| Release 4 reports 84 opportunities in 74 hours, zero successful executions, 18 executions with some fills and 24 filled trades. | release 4 author article and raw log | high for author-reported counts | any-fill, full-route completion and economic outcome must be different metrics | Binance order expiry and FOK behavior | confirms execution-outcome DAG need |
| Release 4 reports roughly 10% lower mean tick-to-trade latency in a 1,000-sample local FIX-server benchmark. | release 4 author article | high for the reported benchmark | a speedup is not evidence of capture or PnL lift; endpoints and tails must be declared | test harness, host, client and protocol are Harjus-specific | supports timing-point and optimization-evidence contracts |
| The benchmark publishes average, median, minimum and maximum but not a precise public start/end contract or P95/P99. | release 4 author article | high | timing labels without endpoints, clock and tail policy are ambiguous | absence in public text is not proof of absence in private instrumentation | requires explicit measurement validity |
| The AWS guide compares RTT, loss and availability zones against a Binance FIX endpoint. | repository `docs/choose-optimal-az.md` | high | infrastructure comparison requires like-for-like population and network evidence | AWS AZ mapping and Binance endpoint only | supports controlled attribution, not provider selection |
| Current code/logs retain execution/order identifiers and partial/failure events, but the public reports do not define an episode identity or conditional per-leg denominator. | inspected code and public artifacts | medium-high | raw IDs are necessary but insufficient for comparable funnel rates | public-material limitation; private semantics may exist | identifies an external semantic ambiguity |

## Reported-run detail retained for audit

| Artifact | Author-reported values | Interpretation limit |
|---|---|---|
| releases 1–3 production | 69 hours; 156 opportunities; 1 successful execution; more than 99% not captured; partial trading created unwanted holdings | “opportunity” and denominator/episode semantics are not precisely defined publicly |
| release 4 production | 74 hours; 84 opportunities; nominal total opportunity profit `0.0000607788 BTC` / `$4.18`; 0 successful executions; 18 executions with some trades; 24 filled trades | counts are author-reported and Binance-specific; they do not establish cause |
| release 4 local FIX-server benchmark | 1,000 samples; v3.2 mean/median/min/max `1165.97/1144.35/956/3836.29 µs`; v4 `1047.65/1008.74/873.67/3834.48 µs` | start/end semantics are not fully specified in public text; no P95/P99; harness may not represent production |

Repository artifacts reviewed at the inspected commit: `README.md`, `docs/choose-optimal-az.md`, `docs/network-performance.md`, `PriceUpdate`, `Opportunity`, `Execution`, `Worker` and `HarjusApplication` headers/implementations. This file summarizes behavior without copying the external source.

## What is not inferred

- “Opportunity” is not assumed to mean evaluation, continuous market episode or attempted execution. The public materials do not define that denominator precisely.
- Harjus’s FOK, FIX, C++, F-Stack/kernel-bypass, AWS placement, fee, asset and regulatory choices are not requirements for this Hyperliquid design.
- The reported runs do not prove that latency caused the execution results, nor that a similar optimization would create economic value here.
- Public logs are evidence of the reported run, not an audited ground-truth dataset.

## Adopted evidence lesson

The only adopted lesson is methodological: preserve counts at every boundary, bind metrics to explicit populations and timing endpoints, retain partial/unknown/reconciled outcomes, and require a full chain from measured technical change to comparable realized economics. No external runtime design is copied.
