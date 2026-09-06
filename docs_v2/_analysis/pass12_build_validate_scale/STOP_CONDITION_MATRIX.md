# PASS 12 — Stop Condition Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

A stop prevents promotion of the affected capability; it does not necessarily stop independent safe research. Risk Constitution remains authoritative.

| Stop ID | Condition | Default scope | Immediate consequence | Evidence needed to resume |
|---|---|---|---|---|
| `STOP-01` | Ambiguous critical specification/authority | Affected phase/domain | Do not implement/promote | Human-resolved contract/ADR and affected test plan |
| `STOP-02` | Unverified exchange rule blocks claimed capability | Market/mode/adapter | Block affected implementation/activation | Current official rule snapshot + conformance evidence |
| `STOP-03` | Data gap invalidates Replay | Dataset/market/time | Reject historical claim | Corrected/qualified DatasetId and quality proof |
| `STOP-04` | Non-deterministic DecisionTrace | Core/capability | No M2 or downstream promotion | Root cause, repeated identical hash/state proof |
| `STOP-05` | Book reconstruction failure | Market/feed | Invalidate state; no affected new risk | Snapshot/diff/resync proof |
| `STOP-06` | Formula parity/unit/sign/rounding failure | Formula consumers | No economic decision | Corrected golden/parity report under governance |
| `STOP-07` | Risk invariant failure | Smallest safe scope or global | New risk off | Fix + property/fault/replay proof + approval |
| `STOP-08` | UNKNOWN exposure/order unresolved | Execution/account/capital | Freeze affected reservations; no retry/new risk | Exchange query, fill dedupe, reconciliation |
| `STOP-09` | Recovery failure/exhaustion | Exposure/market/global as required | Escalate/halt affected action | Current state, bounded resolution/manual approval |
| `STOP-10` | Reconciliation mismatch | Account or affected scope | Cannot reach READY | Orders→fills→balances consistency |
| `STOP-11` | Critical Recorder/evidence loss | Affected live capability | No new risk if auditability compromised | Durability/quality restored and invalid interval recorded |
| `STOP-12` | Simulation bias outside validated support | Model/fidelity/size/regime | Fallback, shrink or reject | Supported recalibration/coverage evidence |
| `STOP-13` | Severe model miscalibration/drift/disagreement | Model consumers | Demote Champion or disable consumer | Temporal OOS + Shadow/Micro-live as needed |
| `STOP-14` | OOD beyond permitted support | Exact slice | q=0, fallback or no new risk | Evidence-supported scope extension |
| `STOP-15` | Security/signer/supply-chain defect | Installation/release/global | Fence authority; new risk off | Containment, trusted artifact, rotation, audit |
| `STOP-16` | Update/rollback/migration defect | Installation/release | Stay/return non-ready | Known digest, compatibility and reconciliation proof |
| `STOP-17` | Split-brain/owner ambiguity | Installation/account | Fence all new risk | Single-owner proof and reconciliation |
| `STOP-18` | Infra/clock/feed/runtime health failure | Host/market/mode | Degrade or no new risk | Current benchmark/health stability evidence |
| `STOP-19` | `Q_validated` unsupported at requested q | Size/route/mode | Shrink to supported q or reject | All-gates next-band evidence |
| `STOP-20` | Incident requires demotion | Affected capability | Immediate scoped demotion | Containment, fix/rollback, replay/shadow/probe and re-promotion |

Failure scopes are `global`, `market`, `strategy`, `mode`, `model`, `size` or `infrastructure`. Cancel, reconciliation and bounded risk-reducing Recovery remain available whenever safely possible.
