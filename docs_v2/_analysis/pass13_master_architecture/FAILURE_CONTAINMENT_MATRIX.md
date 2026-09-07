# Failure Containment Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

`Existing exposure` means cancel/Recovery/safe shutdown remain where inputs are valid; it never authorizes new risk.

| Failure | Detection owner | Scope | New risk | Existing exposure / Recovery / Reconcile | Data / auto action / manual / capability |
|---|---|---|---|---|---|
| Public feed stale/gap | Adapter/Book/Infra | market→venue | Off affected | cancel/recover if account truth; resync Book | preserve RAW; auto disable; escalate persistent; demote data scope |
| Book invalid | Book | market/routes | Off | active-order safety + reconcile as needed | preserve gap; auto invalidate dependencies; manual if unresolved |
| Metadata stale/unknown | Metadata | market/routes | Off | protected cancel/recovery under known rules only | retain raw/version; no default; revalidate capability |
| Fee unknown | Fee/Risk | market/route | Off | risk-reducing action only with conservative valid policy | typed invalid; revalidate external facts |
| Participant model OOD | Model/Ops | model/capability | fallback/shrink/off | execution follows pinned safe plan or revalidates | prediction evidence; auto fallback; demote model scope |
| Simulator low confidence | Simulator/Risk | route/mode/q | shrink/off | current exposure to Recovery policy | retain scenarios; auto narrow; validation review |
| Account feed loss | Account/Reconciliation | account/client | Off | cancel/query/reconcile; Recovery only on known state | P0 evidence; auto RECOVERY_ONLY/HALT; manual if unresolved |
| Order `UNKNOWN` | Execution | order/resources→account | Off affected | reservation locked; query/reconcile; no blind retry | journal preserved; automatic reconcile; manual timeout |
| Recovery failure/exhaustion | Recovery/Risk | exposure/account | Off | contain, reconcile, safe remaining actions | full evidence; halt/escalate; capability demotion |
| Reconciliation mismatch | Reconciliation | affected account/client | Off | query orders→fills→balances; no READY | report preserved; automatic non-ready; manual resolution |
| Recorder degradation | Recorder/Ops | evidence class/system | governed degradation; off if critical truth threatened | preserve P0, cancel/recover available | backpressure/quality event; isolate/drop only by policy; evidence demotion |
| Disk pressure | Infra/Recorder | host | reduce/stop before evidence loss threatens safety | safe stop/recovery | rotate/archive by policy; manual capacity action |
| Clock unhealthy | Clock/Infra | host/measurement | off or restricted by dependency | local safe actions with valid deadlines; reconcile timing ambiguity | flag intervals; auto DEGRADED/UNSAFE; revalidate infra |
| CPU/jitter unsafe | Infra/Ops | host/capability | shrink/off | safety actions prioritized | traces preserved; auto degrade; benchmark/remediate |
| License loss | License/Deployment | commercial scope | Off new commercial risk | cancel/Recovery/reconcile/shutdown/data access remain | audit; cached policy; client/vendor escalation; no safety demotion |
| Secret/signer issue | Security/Execution | signer/client | Off | revoke/rotate; cancel/query if safe credential path; reconcile | redact/preserve incident; halt; manual security review |
| Deployment/update failure | Deployment | client release | Off | prior safe artifact or risk-off/reconcile | logs/evidence; automatic rollback if validated; explicit re-promotion |
| Split brain/owner ambiguity | Deployment/Execution | account/client | Off globally for context | fence; cancel/reconcile only under proven owner | ownership evidence; automatic halt; manual fencing; demote |
| Security incident | Security/Ops/Risk | smallest proven, often client | Off affected/global | revoke/fence/reconcile/recover if trustworthy | immutable incident package; contain; manual incident process |

No healthy sample, restart, rollback or alert acknowledgement automatically restores capability. Resumption requires state consistency and explicit current evidence.
