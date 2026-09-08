# Dirty Generation and Epoch Analysis

DOCUMENTATION STATUS: CANDIDATE MECHANISMS — AWAITING FINAL HUMAN REVIEW

| Mechanism | Candidate use | Correctness key | Open choice |
|---|---|---|---|
| per-market dirty generation | mark new committed book version | monotonic; cannot erase an unevaluated version silently | counter width/wrap policy |
| per-route last-input tuple | avoid same-tuple recomputation | exact tuple equality, not timestamp/hash approximation | storage/layout |
| index generation | bind dense mappings/activation | no mixed generation reads | reclamation/publication |
| work epoch | bound scratch reuse within one evaluation batch | epoch is not economic identity | batch boundary |
| cancellation token | stop already-stale worker effort | cancellation cannot suppress a newer unique state | polling/granularity |

A dirty flag without generation can lose the sequence dirty→processed→dirty under concurrency. Any chosen representation therefore preserves monotonic evidence or the complete latest-work identity and documents wrap/reclamation. It may reduce wasted computation; it does not authorize cross-event collapse, state reordering or blind latest-value semantics.
