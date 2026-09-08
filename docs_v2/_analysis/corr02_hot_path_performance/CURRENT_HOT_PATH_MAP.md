# Current Hot-Path Map

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Step | Input → output | Current canonical work | Potential cost to measure | Immutable authority |
|---|---|---|---|---|
| HP-01 ingest | venue bytes → received event | receive, timestamp, validate envelope | parsing/copy/queue wait | Data / adapter |
| HP-02 normalize | received → typed market event | identity/rules/source mapping | lookup/string/hash/allocation | Data Contracts |
| HP-03 book commit | event → `BookState` generation | ordered reducer, validity/version | level update/layout/publication | Book / Data |
| HP-04 dependents | `MarketId` → routes | `pair_to_routes` affected-only lookup | hash/locality/route degree | Graph / Route |
| HP-05 BBO classify | route/state/q → disposition | C1 validity, C2 proven reject, C3 FastL1 eligibility, C4 priority | branch/work amplification | Graph / Opportunity |
| HP-06 exact economics | survivor → leg results | sequential QF-016 full L2 or exact eligible FastL1 | levels walked/copies/fees/quantization | Formula / NetConvert |
| HP-07 candidate | exact route result → candidate/reason | comparator, closure, edge, bounded features | duplicate work/stale output | Opportunity |
| HP-08 downstream | candidate → Risk/sizing/forecast | only capability-required bounded work | model/Monte Carlo/queue delay | Participants / Simulator / Risk / Capital |
| HP-09 commit | proposal → state/plan/effect | ordered version recheck, reservations, plan | stale discard/contention | State owners / Execution |
| HP-10 evidence | typed event → async recorder/metrics | bounded handoff and priority | queue saturation/copy/allocation | Recorder / Operations |

## Boundaries

Critical state mutation is ordered and single-writer. Workers may compute against immutable snapshots, but their output is a proposal tagged with the complete input generation and cannot commit stale. Blocking network/storage/license/model-training work remains outside evaluation.

The map is architectural, not a latency claim. Every component duration uses the CORR-01 timing-point contract; scheduler/queue wait is separated from execution. Only a measured bottleneck advances to an optimization hypothesis.
