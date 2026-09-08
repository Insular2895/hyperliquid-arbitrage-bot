# CORR-03 — HJ Failure Suite Validation Matrix

DOCUMENTATION STATUS: M0–M5 EVIDENCE PLAN

| Scenario | M0 specification | M1 unit/property/integration | M2 Replay/fault injection | M3 Shadow | M4 Micro-live | M5 production observation |
|---|---|---|---|---|---|---|
| HJ-001 | zero/pre-send distinctions | zero delta, no next leg, release proof | deterministic reject/zero fixtures | would-attempt only | natural IOC zero retained | rate/reason monitoring |
| HJ-002 | partial algorithm/dust | fill-once, actual-q propagation, minima | multiple partial/dust sequences | counterfactual mechanics only | natural small partial retained | slice rates/economics |
| HJ-003 | later-leg exposure/Recovery | no rollback, affected lock | TT/TTT later-leg failures | observe forecast only | natural failure under stop limits | incident/recovery evidence |
| HJ-004 | later partial ownership | no double routing/reservation | split continuation/recovery fixtures | no actual labels | natural only | accounting/ownership audit |
| HJ-005 | no-blind-retry | identity/lock/query transitions | lost ACK/timeout injection | transport diagnostics | do not induce; retain natural | UNKNOWN spike/resolution |
| HJ-006 | cancel truth | fill-during-cancel ordering permutations | delayed cancel/fill fault injection | would-cancel only | natural only | late-fill/reconcile audit |
| HJ-007 | maker partial/cancel | maker remainder ownership | queue/cancel emulator | maker observability only | required natural/probe evidence before MT | promoted-maker observation |
| HJ-008 | restart protocol | checkpoint/journal crash points | kill/restart at A–D, no capital | restart drills | do not induce active-capital crash | natural incident/postmortem |
| HJ-009 | idempotence | `Reduce(Reduce(S,e),e)=Reduce(S,e)` | stream/snapshot order permutations | duplicate ingestion only | safe transport duplicate if natural | dedupe counters/audit |
| HJ-010 | Recovery bounds/failure | partial/unknown/replan/exhaustion | deterministic constrained-depth Recovery | counterfactual only | do not intentionally fail Recovery | natural evidence/manual escalation |

Maturity is the existing M0–M5 ladder. This table does not create a second ladder. No scenario requires reckless real-capital failure injection.
