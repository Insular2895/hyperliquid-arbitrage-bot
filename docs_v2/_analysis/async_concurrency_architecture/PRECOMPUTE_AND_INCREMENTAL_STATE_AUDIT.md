# Precompute and Incremental-State Audit

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| Value/work | Initial treatment | Update trigger | Read-time bound | Worker candidate | Correctness condition |
|---|---|---|---|---|---|
| spread/mid/BBO | incremental C1 with Book commit | valid book mutation | O(1) view | no baseline need | exact current BookVersion |
| depth summaries | incremental bounded buckets | changed levels | bounded lookup | deeper alternative benchmark | full L2 remains available |
| imbalance/microprice | incremental C1 | BBO/depth change | O(1) | richer depths C2 | formula/version and freshness |
| OFI/MLOFI | rolling state | ordered trade/book event | bounded | large horizon C2/offline | no history rescan at opportunity |
| realized volatility/jump flags | rolling windows/accumulators | ordered observations/timers | bounded | alternative estimators C2/C5 | point-in-time availability |
| regime | last valid versioned snapshot | rolling feature update | bounded | C2 model | support/OOD/freshness visible |
| survival baseline | incrementally calibrated artifact/cache | offline promotion + current inputs | bounded | C2 richer model | no blind product; exact conditioning |
| market/feed/infra health | rolling counters/state | I/O/state/clock events | bounded | C4 aggregation | health owner commits typed status |
| `pair_to_routes` | prebuilt immutable reverse index | graph generation change | affected membership only | build can be C2/C4 | deterministic canonical IDs |
| Graph topology/routes | precomputed versioned generation | metadata/topology change | immutable lookup | build proposal C2 | C0 version check and publish |
| Atlas summaries | near-line/background version | eligible evidence arrival | bounded snapshot | C4/C5 richer analysis | last valid or UNKNOWN; never future data |
| fee/precision/rule lookup | versioned local state | metadata/rule event | O(1)/bounded | no remote hot-path fetch | current known version required |
| Participant/model artifact | preloaded immutable local artifact | startup/promotion | bounded local inference | C2 inference | artifact/support/OOD/freshness |
| q-grid static candidates | config/versioned templates | capability/config change | bounded iteration | C2 parallel grid | final deterministic C0 selection |
| plan/intent templates | pure preparation | candidate/route snapshot | bounded | C2 possible | no nonce/size/send authority |
| Recorder buffers | preallocated/reused where measured | startup/growth policy | bounded enqueue | C4 consumes | explicit capacity/failure semantics |
| metrics labels/views | bounded registries | startup/config | inline counters only | C4 formatting/export | no raw high-cardinality IDs |

## Finding

No Opportunity evaluation may scan unbounded event history. Incremental maintenance is preferred where it preserves exact semantics and makes invalid/missing state explicit. A cached/precomputed value carries its generation, `as_of`, source state versions, model/config/formula versions where applicable, support/OOD and freshness. Cache hit is not validity.

Precomputation is not speculative authorization. CORR-04 speculative results remain non-canonical and are reusable only after exact canonical fingerprint/version parity.
