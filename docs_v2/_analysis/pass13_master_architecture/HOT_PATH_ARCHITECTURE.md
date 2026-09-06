# Hot Path Architecture

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Exact path

1. Adapter accepts and timestamps a market/account payload.
2. Normalizer emits a typed event or rejects it without state mutation.
3. Ordered Coordinator commits relevant Book/rule/account reducer updates.
4. `pair_to_routes` selects only affected active routes.
5. Cheap freshness/BBO/structural/eligibility filters may reject.
6. Formula Core computes exact L2 `NetConvert(q)` for bounded candidates.
7. Required incremental features, promoted bounded forecasts and configured Simulator fidelity produce versioned distributions.
8. Terminal/Inventory projection, Sizer and optional bounded Allocator produce feasible proposals.
9. Risk T1 authorizes a maximum envelope; Reservation atomically claims resources.
10. Risk T2 revalidates immediately before the immutable plan requests an order effect.

During execution, ordered ACK/fill/timeout/cancel events re-enter the same coordinator. Actual fills update state before T3/T4/T5 continuation decisions.

## Required in-memory data

Book, Metadata, Fee, Precision, Graph/Route definitions, reverse dependencies, active HWC scope, features, approved model artifacts, Atlas snapshot, Account/Inventory/Reservations, Risk config/snapshot, CapabilityManifest and InfraHealth.

## Bounded-work rules

- fixed 2/3-leg definitions and affected routes only;
- deterministic finite q grid/refinement and scenario budget;
- incremental features and bounded production inference;
- input-version checks at worker completion and pre-send;
- deterministic tie order; reject/zero-size on empty feasible set.

## Prohibited

Synchronous disk/database/object store/log flush, license/registry/admin calls, training, historical scans, whole-universe graph search, large/unbounded Monte Carlo, uncontrolled allocation/loops and speculative external retry.

## Instrumentation and failure

Stage durations map to QF-084 without double counting and carry run/event/opportunity versions. Invalid/stale inputs reject affected new risk; stale worker output is discarded/revalidated. Recorder enqueue and metrics must be non-blocking under explicit degradation policy.
