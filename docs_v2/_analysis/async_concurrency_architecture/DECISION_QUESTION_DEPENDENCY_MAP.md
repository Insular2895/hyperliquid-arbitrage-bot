# Decision-Question Dependency Map

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

| Decision question | Required facts | May be precomputed/parallel | Must be current/ordered | If unavailable |
|---|---|---|---|---|
| Is the source state usable? | sequence integrity, freshness, metadata/rules | rolling health counters | committed Book/metadata/account validity | reject affected scope/resync |
| Which routes are affected? | Graph/index generation, changed pair | immutable reverse index | current committed generation | rebuild/reject affected work |
| Can BBO safely reject? | current BBO, q/rules/fees, proved bound | bound constants | exact input tuple | fall through to full L2 |
| What is executable output? | ordered L2 levels, directions, fees, rounding | pure route jobs | accepted matching versions | inline fallback or reject candidate |
| Is it an Opportunity? | exact route result/comparator/closure | bounded features | deterministic comparator/order | typed rejection |
| What may happen during execution? | feature/model/infra snapshots | Participant and F0–F3 proposals | snapshot validity and support checked | simple supported fallback/shrink/reject |
| Which q is feasible? | economics, tails, terminal viability, `Q_validated` support | independent q proposals | deterministic selection over accepted set | smaller inline grid/zero |
| Which candidates share capital? | candidate curves, Book capacity, balances | curve generation/optimization proposal | allocation and shared-capacity commit | deterministic conservative allocation |
| May this plan increase risk now? | current account/inventory/reservations/infra/Risk | stale Risk evidence may explain only | final Risk `ALLOW` must be current in C0 | deny/recompute; stale ALLOW never reused |
| Can resources be claimed? | current balance/book/risk budgets | none authoritative | atomic ordered Reservation | reject/resize |
| What is sent? | immutable plan, current rules/nonce/signer | pure serialization prep | actual intent/nonce/plan commit | do not send |
| Did the exchange accept/fill? | authoritative response/account/fill evidence | async query I/O | ordered event application/dedupe | `UNKNOWN`, lock resources, reconcile |
| May the next leg execute? | actual prior fill, current state, protection/Risk | pure template/scenario prep | actual-fill-driven size and T3 check | wait/cancel/recover |
| Is Recovery required/safe? | actual exposure and current executable exits | bounded exit proposals | Recovery choice and state transition | contain/reconcile/manual escalation |
| Is the account consistent? | orders → fills → balances | queries concurrently where semantics allow | ordered reconciliation decision | NON-READY/no new risk |
| May background work degrade? | evidence priority and dependency health | aggregation/compression/archive | health transition by owner | shed optional work; halt new risk if P0 threatened |

## Dependency rule

Optional intelligence cannot block the simple supported baseline. A worker/cached result can improve a decision only while its complete input tuple and capability remain valid; it cannot manufacture current state or override a current hard gate.

## Selection policy dependency

`BATCH_SELECT` requires a declared candidate population boundary and waits only to bounded deadlines before deterministic selection. `EARLY_COMMIT` may consider an early candidate only under a declared deterministic ordering/admissibility rule and current shared-capacity revalidation. Neither policy means first completion wins. The current repository does not select one; Replay + Shadow must compare them before human approval.
