# CORR-01 — Final Report

DOCUMENTATION STATUS: COMPLETE — AWAITING HUMAN REVIEW

## Result

CORR-01 adds a canonical Capture Funnel, Opportunity lifecycle/episode identity, per-stage latency attribution, exact metric populations, multi-axis actual outcomes and immutable predicted-versus-actual calibration. It is documentation-only and creates no execution authority.

| Control | Result |
|---|---|
| Baseline commit | `fdb4a25588670fb245edebc0650d262c7f536b4c` |
| Branch | `codex-docs` |
| Harjus research | `COMPLETE` |
| Harjus repository commit | `09816b3da2a393795250e38c8b49869b57ba4d6f` |
| Current Masters reviewed | `15/15` |
| Relevant deep-spec Markdown files fully reviewed | `105` |
| Post-reconstruction human decisions registered | `6` (`HDC-001..006`) |
| Capture collision families resolved | `4` |
| Pre-execution funnel stages | `14` (`CF-00..CF-13`) |
| Outcome DAG stage labels | `13` (`CF-20..CF-32`) |
| Named timing points | `23` |
| Capture/economic metric families | `43` |
| Latency metric families | `28` |
| QF changes | `0` |
| Execution/Risk transition changes | `0` |
| Source-inventory changes | `0` |
| Implementation/benchmark/optimization executed | `NO` |

## Final semantics

- `OpportunityId`: one immutable exact-valid opportunity observation.
- `OpportunityEpisodeId`: deterministic offline/near-line grouping under one calibrated/versioned segmentation policy; not exchange truth or hot-path state.
- `EXECUTION_ATTEMPTED`: first risk-increasing intent may have transmitted; a post-possible-send ambiguity remains attempted/`UNKNOWN`.
- `FULL_ROUTE_COMPLETED`: actual original route objectives satisfied, canonical route `COMPLETED`, no Recovery entry.
- recovered safe closure: valid existing Execution closure, reported separately from original-route full completion.
- `TERMINAL_RECONCILED`: account/order/fill/balance/inventory/fee/reservation truth agrees.
- `ECONOMICALLY_POSITIVE`: complete attempt-level actual PnL is strictly positive at declared horizon/numeraire.

## Terminology audit

QF-048 and QF-085 remain survival-at-arrival probabilities. `ExecutionForecast.p_full` remains a versioned prediction. `FullRouteCompletionRate` is empirical attempt-cohort evidence. QF-093 remains the ratio of realized-PnL sums to expected-executable-PnL sums. Bare “capture rate” and “success rate” are prohibited in canonical metrics.

## External evidence disposition

Harjus’s public repository, author write-ups and production log were used only as comparative methodology evidence. The reported gap between opportunities, partial fills, complete executions and a latency benchmark supports explicit populations and endpoints, but it does not prove causality or justify importing Binance/FIX/FOK/C++/F-Stack/AWS choices. It is `COMPARATIVE_EXTERNAL_EVIDENCE`, never `SRC-009`.

## Validation performed

- Git whitespace/error check: clean;
- local Markdown links in every changed/new Markdown file: resolved;
- changed review files: exactly `00_REVIEW_START_HERE.md` and `21_FINAL_HUMAN_DECISION_FORM.md`;
- checked approval boxes: `0`;
- formula files changed: `0`;
- legacy `docs/**` files changed: `0`;
- CORR-01 analysis artifact count including this report: `20`;
- all modifications restricted to `docs_v2/**`; pre-existing `.DS_Store` remains excluded.

## Review and authorization state

The PASS16 review package is stale and prominently marked: do not approve until the package is refreshed after CORR-06. Human approval is `PENDING`. Phase 1, implementation, switchover, MicroLive, Live, capital and all optimization remain `NOT AUTHORIZED`. CORR-02 was not started.

## Remaining calibration / future work

Episode segmentation numbers, instrumentation representation, analytical trace sampling, percentile/bucket estimator, sample minima and overhead thresholds remain calibrated or implementation choices. Telemetry/backend remains `OPEN-015`. Any future `p_full` decision threshold remains Risk-owned and absent today. Detailed attempt-level accounting integration remains deferred to CORR-05.

## Vault / graph

The vault was used for workflow and architecture/observability guidance. No durable vault file was changed because this correction is project-specific and already captured canonically in `docs_v2`. The coding knowledge graph was not regenerated. A later validated general reflex card may be proposed after human review; no project decision was silently classified.
