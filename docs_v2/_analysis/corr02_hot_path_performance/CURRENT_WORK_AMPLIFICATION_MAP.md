# Current Work-Amplification Map

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

| Amplifier | Numerator | Denominator | Safety-preserving reduction candidate | Forbidden shortcut |
|---|---|---|---|---|
| route fan-out | routes selected | valid book commits | contiguous reverse index, activation mask | graph-wide scan or hidden route omission |
| duplicate dependency | selected memberships | unique affected `RouteId` | generation-local exact dedup | hash-only collision skip |
| BBO survivors | full-L2 evaluations | valid BBO-classified evaluations | proven conservative C2 bounds | heuristic permanent reject |
| level walking | levels visited | exact leg evaluation | exact C3 FastL1 when eligible | treating L1 insufficiency as route rejection |
| state rebinding | snapshots/versions loaded | unique economic input tuple | immutable bound evaluation context | mixed versions |
| stale work | stale proposals | worker proposals | cancel/dirty generation/prioritization | committing stale output |
| allocation | allocations/bytes | event, route, exact leg, opportunity, attempt | preallocation/reuse/flat data | truncation or unsafe stale reuse |
| copy | bytes/clones | same denominators | borrowed views/compact IDs/reused scratch | lifetime/alias violation |
| queueing | enqueues/dequeues/waits | event by priority | bounded SPSC where topology fits | silent loss, reorder or unbounded spin |
| instrumentation | instrumented work | baseline work | sampled/off-path detail | hiding missingness or overhead |

Work eliminated counts only when the skipped computation would consume the same complete canonical input tuple. Distinct ordered states are not duplicates merely because prices or a hash appear equal. Capture and economics must be compared using CORR-01 denominators after any scheduling or filtering change.
