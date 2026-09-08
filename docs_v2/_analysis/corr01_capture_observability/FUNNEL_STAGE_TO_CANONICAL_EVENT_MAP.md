# CORR-01 — Funnel Stage to Canonical Event Map

DOCUMENTATION STATUS: DESIGN CONTRACT — IMPLEMENTATION NOT AUTHORIZED

The names below specify evidence roles, not new frozen Rust enum variants. Where the baseline schema already has a record/event, it is reused. A future implementation may represent projection markers as typed linked records or derive them from `DecisionTrace`, provided replay equivalence is proven.

| Funnel stage | Baseline canonical evidence | Minimum added projection evidence | Forbidden inference |
|---|---|---|---|
| `CF-00` | normalized/ordered market event, published `BookVersion` | observation validity and source-quality link | count raw packets as usable observations |
| `CF-01` | affected-route lookup / worker dispatch trace | `ReevaluationId`, trigger reason | infer from later Opportunity only |
| `CF-02`–`CF-03` | BBO comparator inputs/result | stable evaluation ID, pass/reject reason | treat missing exact dispatch as BBO reject |
| `CF-04`–`CF-05` | exact route/L2/formula trace | validity disposition and exact input-version set | treat positive theoretical edge as valid executable candidate |
| `CF-06` | `Opportunity` | immutable `OpportunityId` attached to evaluation | collapse repeated observations into one event |
| `CF-07` | `ExecutionForecast`, participant forecasts, confidence | forecast bundle/frozen label version | use latest model output after the decision |
| `CF-08` | candidate/strategy/capital context | candidate disposition and reason | infer eligibility from eventual send |
| `CF-09` | `RiskDecision` | funnel projection link | infer Risk allow from no reject |
| `CF-10` | sizing decision | positive/zero/invalid reason | use requested unquantized size |
| `CF-11` | reservation records | atomic set commit marker | infer reservation from plan existence |
| `CF-12` | immutable `ExecutionPlan` | plan commit time/hash | treat candidate plan as committed |
| `CF-13` | `OrderIntent`, order reducer/transport evidence | possible-transmission classification | classify proven pre-send failure as attempt; drop ambiguous sends |
| `CF-20`–`CF-25` | route/leg/order transitions and unique `FillEvent`s | outcome projection with target/tolerance version | planned or simulated fill as actual |
| `CF-26` | canonical `UNKNOWN` | first/last unresolved timestamps and reason | label failure or no-fill before resolution |
| `CF-27` | route transition history, leg actuals, `COMPLETED` | original-route/no-Recovery predicate result | equate safe closure after Recovery to original-route full completion |
| `CF-28`–`CF-29` | Recovery machine records | originating execution linkage | hide recovery legs in original route fills |
| `CF-30` | Reconciliation record | attempt-scope completeness | use terminal order status alone |
| `CF-31`–`CF-32` | accounting records | economic completeness, horizon, numeraire and sign | declare profit before complete valuation |

## Projection conformance

A conforming projector is deterministic from ordered canonical evidence plus `FunnelDefinitionVersion`, `EpisodeSegmentationVersion` and label versions. It produces identical stage/disposition records in Replay for identical manifests. Projector failure cannot block Risk-reducing actions or mutate owner states.
