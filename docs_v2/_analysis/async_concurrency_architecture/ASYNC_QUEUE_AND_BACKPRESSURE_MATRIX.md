# Async Queue and Backpressure Matrix

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

All capacities, worker counts and numeric waits are calibrated. Every queue is bounded and instrumented. “Drop” always means an explicit, counted policy disposition; it never means silent loss.

| Boundary | Producer → consumer | Content / ordering | Full behavior | Supersede/drop eligibility | Priority | Coordinator may block? | Shutdown |
|---|---|---|---|---|---|---|---|
| market ingress | C3 feed → C0 orderer | source observations; source order retained | bounded upstream pressure or invalidate affected Book and resync | no causal drop followed by valid claim; derived latest-value views only | canonical source | no indefinite wait | stop intake, preserve/invalidate explicitly |
| account/fill ingress | C3 account → C0 orderer | orders/fills/balances; causally ordered/deduped | declare unhealthy, no new risk, reconcile | never drop unique account/fill evidence | highest | no indefinite wait | drain critical evidence or mark unresolved |
| metadata ingress | C3 adapter → C0 | versioned rules | affected capability NON-READY if not preserved | supersede only with proved version semantics | high | bounded only | persist last valid + missingness |
| timer/control | clock/admin → C0 | explicit ordered events | reject new optional command; preserve safety timers | no safety-timer loss | high | bounded only | process safe-stop controls |
| C2 request | C0/C1 → worker pool | immutable job + versions/deadline/generation | do inline/simple fallback, reject optional work or supersede older job | stale/older derived jobs may be canceled | below safety events | no | cancel/cooperative drain |
| C2 result | workers → C0 | proposal; deterministic identity | discard late/stale/duplicate proposal | yes, by identity/generation | below source/account events | no | discard after closure unless required evidence |
| effect request | C0 → C3 executor | immutable Submit/Cancel/Query effect | fail effect explicitly; `UNKNOWN` when transmission ambiguous | Submit never silently replaced; queries may dedup if exact | cancel/query safety above new submit | no | stop new submits; continue bounded safety effects |
| effect result | C3 → C0 | normalized ACK/status/fill/error | account unhealthy/UNKNOWN/reconcile if unavailable | never lose unique result/fill | highest | no | drain or persist unresolved |
| Recorder P0 | Core → C4 Recorder | execution/account/fill/journal | Recorder critical health; block new risk by owned policy before silent loss | never shed | critical | enqueue bounded; disk never | drain/finalize or mark incomplete |
| Recorder P1 | Core → C4 Recorder | market RAW needed for reconstruction | invalidate dataset/scope; controlled degradation | only explicit policy with missingness | high | enqueue bounded | close manifest with quality state |
| Recorder P2/P3 | Core → C4 Recorder | analytics/diagnostics | sample/coarsen/drop with counters | yes, declared | lower | no | best-effort bounded drain |
| checkpoint handoff | C0 snapshot capture → C4 | coherent cursor + immutable snapshot handle | skip/supersede checkpoint; journal remains truth | older unstarted checkpoint may supersede | medium | only bounded capture | last complete checkpoint only |
| metrics/traces | Core → C4 exporter | counters/spans/structured events | aggregate/sample/drop optional detail | yes, never hide missingness | lower | no | bounded flush |
| archive | C4 writer → remote archive | closed verified chunks | retry/backoff locally; retain manifest/health | never relabel unavailable as archived | background | no | persist pending state |
| admin/report | local control → C4/C5 | bounded request/job | reject busy/queue full | optional jobs may cancel | below safety | no | reject/finish bounded work |

## Queue contract fields

An implementation specification must add: calibrated capacity source, producer/consumer cardinality, exact progress guarantee, ordering, overflow result, retry/spin/park behavior, memory-order proof if lock-free, cache-line layout if material, priority inversion analysis, lifecycle/drain and failure injection. Unbounded spawn, unbounded queue growth and `WAIT_FOREVER` are prohibited.
