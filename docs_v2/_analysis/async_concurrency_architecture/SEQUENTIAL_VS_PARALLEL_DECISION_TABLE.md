# Sequential versus Parallel Decision Table

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| Work | Final baseline | Parallel status | Ordered boundary | Rationale |
|---|---|---|---|---|
| decode/normalize independent sockets | async per connection | allowed/bounded | canonical ingress order | waiting is I/O; observation provenance retained |
| canonical event application | sequential logical order | forbidden as competing writes | C0 | state truth and Replay |
| Book/Account/Fill/Inventory/Reservation reducers | inline ordered | no mutation workers | C0 | one authority; unique fills/current resources |
| `pair_to_routes` | inline | fanout dispatch benchmark only | current Graph generation | expected cheap lookup/locality |
| BBO/FastL1 | inline | no baseline need | exact state tuple | cheap bounded filter/path |
| full-L2 NetConvert | inline initially | route/q worker challenger | accept proposal in C0 | oracle is bounded; avoid premature queue cost |
| route fanout | deterministic inline order initially | C2 challenger | policy + version recheck | benefit depends on fanout/tails/2-vCPU cost |
| cheap features/F0/F1 | incremental/inline or valid cached | richer variants C2 | support/current version | simple baseline must remain available |
| Participant inference | local bounded snapshot | C2 candidate | accepted only if fresh | optional intelligence; OOD/fallback |
| Simulator F2/F3 | not inline baseline | C2 candidate | deadline + ordered accept | potentially CPU-heavy |
| Simulator F4/large Monte Carlo | offline | C5 only | promotion/evidence workflow | not a Live dependency |
| q-grid | small deterministic inline | C2 challenger | C0 final argmax/tie-break | completion order cannot choose q |
| sizing curves | bounded inline baseline | C2 candidate | current capacity/Risk | pure curve work separable |
| portfolio optimization | proposal may be C2 | allowed/bounded | C0 allocation/reservation | shared capital/book capacity |
| final Risk | inline/current | no stale ALLOW worker | C0 | safety authority must see current state |
| Reservation | ordered/atomic | never worker-owned | C0 | oversubscription prevention |
| local signing | bounded inline baseline | alternative benchmark only | exact immutable intent/nonce | remote signer not baseline |
| order/cancel/status/reconcile network | async | C3 required | response returns through C0 | never block coordinator |
| Recorder enqueue | minimal inline handoff | bounded | evidence-priority policy | no disk work inline |
| write/compress/checksum/archive | background | C4 | state/health event only | durability without hot-path I/O |
| metrics counters | cheap inline | aggregation/export C4 | bounded identifiers | avoid logging stalls |
| Replay/training/search/report | separate/offline | C5 | artifact promotion only | resource isolation/no Live authority |

## Route decision policies

| Policy | Safe definition | Status |
|---|---|---|
| `BATCH_SELECT` | collect the declared relevant set until complete or bounded deadline, apply deterministic fallback for missing jobs, then optimize allocation/order | safe candidate; `CALIBRATED` |
| `EARLY_COMMIT` | consider the earliest candidate in a predeclared deterministic economic priority whose evidence is complete/current; revalidate shared capacity and Risk before commit | safe candidate; `CALIBRATED` |
| first-worker-wins | completion order determines the trade | `FORBIDDEN` |
| adaptive learned policy | policy switches from learned/contextual rule | `RESEARCH`; no Live authorization |

The repository’s allocation contracts require ordered deterministic commit but do not mandate waiting for every worker result. There is therefore no current canonical winner between the two safe policies.
