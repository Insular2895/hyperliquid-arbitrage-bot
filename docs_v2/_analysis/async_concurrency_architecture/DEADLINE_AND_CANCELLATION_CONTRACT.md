# Deadline and Cancellation Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

No hot-path family has `WAIT_FOREVER`. Exact numeric deadlines, worker counts and capacities are calibrated from representative workload, tail latency, scheduler pressure and economic evidence.

## Allowed timeout dispositions

`WAIT_BOUNDED`, `USE_VALID_CACHED`, `FALLBACK_SIMPLER_MODEL`, `REDUCE_CAPABILITY`, `REJECT_CANDIDATE`.

| Family | May wait? | Bound | Cancel/supersede | Late result | Safe fallback |
|---|---|---|---|---|---|
| route fanout/full-L2 challenger | yes | candidate decision deadline | cooperative; newer exact generation may supersede | discard/revalidate only under declared equivalence | inline full L2 or reject candidate |
| parallel q-grid | yes | sizing deadline | cancel remaining q jobs after policy closure | discard | smaller inline grid/zero |
| Participant inference | yes if capability consumes it | forecast validity/deadline | supersede by newer feature/model generation | discard | valid simple/cached baseline, shrink or reject |
| Simulator F2/F3 | yes | decision deadline | cooperative | discard | supported F1/F2, shrink or reject |
| portfolio proposal | yes | allocation-cycle deadline | cancel closed candidate-set work | discard | deterministic conservative allocator/reject |
| Recovery route search | only bounded; safety priority | Recovery policy deadline | preempts optional compute | discard stale; current revalidate | safe bounded exit/contain/reconcile |
| Submit/Cancel/Query | async only | transport/state-machine timer | cancellation only with transmission semantics | response still becomes ordered event | `UNKNOWN`/query/reconcile; never blind retry |
| reconciliation query | async only | state-machine deadline | bounded retry/cancel | preserve as-of; may still record | remain NON-READY/escalate |
| Recorder enqueue | bounded handoff only | queue policy | no cancellation of P0 evidence | n/a | health degradation/no new risk before loss |
| Recorder/background job | not on Core path | maintenance deadline | yes where artifact remains valid | retry/postpone/mark incomplete | retain journal/local artifact |
| Replay/training/search | offline | campaign resource/time budget | yes | retain partial/inconclusive evidence | no promotion |

## Correctness rules

- Timeout does not prove non-transmission, no fill, cancel success or task termination.
- Cooperative cancellation is an optimization; state safety depends on generation/version checks.
- A deadline miss is visible evidence and participates in capability/health evaluation.
- Safety/account/fill processing preempts or bypasses optional compute pressure.
- A fallback is declared by capability/config and recorded. It may contract scope; it cannot silently change formula or truth semantics.
