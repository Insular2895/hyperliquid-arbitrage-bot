# CORR-01 — Fix Log

DOCUMENTATION STATUS: COMPLETE — AWAITING HUMAN REVIEW

## Baseline controls

- branch verified: `codex-docs`;
- baseline verified: `fdb4a25588670fb245edebc0650d262c7f536b4c`;
- PASS16 complete, human approval pending, implementation/switchover unauthorized;
- pre-existing untracked `.DS_Store` excluded from all work;
- edits restricted to `docs_v2/**`.

## Review performed

- all 15 mission-specified current Masters reviewed: `00`, `03`, `04`, `06`, `07`, `08`, `09`, `10`, `11`, `12`, `13`, `16`, `17`, `18`, `19`;
- 105 relevant deep-spec Markdown files fully read across Architecture, Market Graph, Participants, Simulator, Execution, Data, Recorder/Replay, Validation, Operations and Roadmaps;
- Harjus primary external materials inspected, including repository commit `09816b3da2a393795250e38c8b49869b57ba4d6f`, author write-ups and production-log artifact;
- external evidence classified `COMPARATIVE_EXTERNAL_EVIDENCE`; source inventory unchanged.

## Canonical fixes

1. Registered `HDC-001..006` as post-reconstruction human decisions pending final review.
2. Defined 14 pre-execution funnel stages and 13 outcome-DAG stage labels.
3. Separated route evaluation, event-level Opportunity, derived episode and execution attempt identities.
4. Selected versioned `OpportunityEpisodeId` as offline/near-line grouping; segmentation values remain calibrated.
5. Defined conservative possible-transmission attempt boundary and explicit `UNKNOWN` cohort treatment.
6. Defined original full-route completion separately from recovered safe closure, terminal reconciliation and economic positivity without changing Execution.
7. Resolved four `capture` collision families without changing QF semantics.
8. Added 23 named timing points, fine/coarse attribution rules and an explicit prohibition on ambiguous `tick-to-trade` labels.
9. Added 43 capture/economic metric families plus 28 latency metric families with population, missingness and bias governance.
10. Added immutable forecast-to-actual label/join/calibration rules.
11. Added storage/cardinality, sampling priority and instrumentation-overhead contracts.
12. Added the technical→funnel→economic optimization evidence chain.
13. Added canonical Operations deep spec 11 and targeted master/deep-spec/global-register overlays.
14. Marked only review files 00 and 21 stale; approval controls remain unchecked.

## Deferred/open

- episode segmentation numbers, trace sampling, percentile estimator/buckets/sample minima and overhead budgets are calibrated;
- telemetry/backend remains `OPEN-015`;
- instrumentation representation is an implementation choice after authorization;
- any future `p_full` decision threshold is Risk-owned and does not exist in CORR-01;
- attempt-level accounting allocation/valuation detail is deferred to CORR-05;
- CORR-02..06 not started.

## Explicit non-changes

No source code, formula, execution transition, Risk gate, external API integration, telemetry backend, optimization, benchmark, legacy doc or switchover was changed or executed.
