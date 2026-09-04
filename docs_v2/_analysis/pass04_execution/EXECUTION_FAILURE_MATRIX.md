# PASS 04 — Execution Failure Matrix

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

| Failure | Known / unknown | Exposure | Allowed next action | New risk | Reservation | Transition | Recovery / reconciliation | Source |
|---|---|---|---|---:|---|---|---|---|
| validation fails | known current reject | none | record reason/abort | unaffected elsewhere | none | Route `VALIDATING->ABORTED` | none | REQ-EXEC-0111 |
| reservation fails | no order sent; acquired subset known | none | atomic release/abort | no for candidate | release proven subset | `RESERVING->ABORTED` | only if state contradiction | REQ-EXEC-0112/0113 |
| signing fails | known if transport never invoked | none | abort/new intent only after current validation | no candidate | hold then route release | local fail before `SIGNED` | no if provably unsent | REQ-EXEC-0123 |
| send fails before transmission | provably unsent | none | abort/replan | no candidate | route-controlled release | no `SENT` economic ambiguity | no | REQ-EXEC-0124 |
| send state uncertain | transmission may have occurred | possible | query by CLOID/orders/fills | no affected | hold | `SENT/PENDING->UNKNOWN` | reconciliation required | REQ-EXEC-0118/0124/0132 |
| ACK timeout/lost | outcome unknown; timeout not reject | possible | status/fill/open-order query | no affected | hold | `PENDING->UNKNOWN` | required | REQ-EXEC-0186/0190 |
| exchange reject | explicit order reject; reconcile conflicting fills | none for this order, prior legs possible | map reason; abort or recover | no route increase | unused only after proof | `...->REJECTED` | terminal reconcile; Recovery if prior exposure | REQ-EXEC-0131 |
| first-leg zero fill | terminal zero known | none | no later leg; abort | no candidate | release after terminal proof | Route `->ABORTED` | reconciliation for release | REQ-EXEC-0140 |
| partial fill | actual amount known; remaining per order evidence | real partial | update inventory; resize/revalidate or recover | no unvalidated increase | convert used/hold rest | Order `PARTIALLY_FILLED`; route continues/recovery | as order state demands | REQ-EXEC-0129/0146/0147 |
| Leg 2 failure | Leg 1 exposure exists; Leg 2 result may vary | intermediate asset | best current Recovery | no same capital | hold/convert | `EXECUTING->RECOVERY_REQUIRED` | Recovery; reconcile uncertainty | REQ-EXEC-0145/0149 |
| Leg 3 failure | earlier actual fills exist | one/more residual assets | vector Recovery | no same capital | hold/convert | `->RECOVERY_REQUIRED` | Recovery | REQ-EXEC-0159/0161 |
| price protection/no match | known zero only with terminal proof | prior legs only | abort/recover; new plan for new bound | no silent widening | reconcile/release | abort or Recovery | reconcile if transport ambiguous | REQ-EXEC-0139/0189 |
| maker stale | age/economics/feed gate fails; maker may remain live | existing fills + possible remainder | request cancel; hedge/recover fills | no maker increase | hold remainder | `RESTING->CANCEL_REQUESTED` | reconcile final status | REQ-EXEC-0153/0154 |
| maker partial | actual fill known; remainder live/possible | real partial | prompt taker evaluation; monitor/cancel rest | only current-gated continuation | convert/hold | `RESTING->PARTIALLY_FILLED` | Recovery if invalid/below policy | REQ-EXEC-0155/0156 |
| cancel race / fill during cancel | cancel not effective proof; fill may occur | actual/possible | apply fill; recompute residual; hedge/recover | no new opportunity | convert/hold | `CANCEL_REQUESTED->PARTIAL/FILLED/...` | terminal reconcile | REQ-EXEC-0134/0158 |
| cancel response lost | order activity unknown | possible | query CLOID/OID/open/fills | no affected | hold | `CANCEL_REQUESTED->UNKNOWN` | required | REQ-EXEC-0132/0133 |
| market-feed loss/stale | market state unknown after freshness bound | active orders/exposure known separately | stop new risk; cancel resting by policy; recover | no | hold | Engine `DEGRADED/RECOVERY_ONLY` | reconnect+reconcile | REQ-EXEC-0179 |
| account/order-feed loss | order/fill truth may be missed | possible | stop risk; query reconciliation | no | hold | Engine safer state; orders may `UNKNOWN` | HTTP/query required | REQ-EXEC-0180 |
| clock unhealthy | ordering/freshness unsafe | active exposure remains | stop admission; safety actions | no | hold | Engine `DEGRADED/HALTED` by policy | sync/reconcile before READY | SRC-005 clock/Risk; closure principle |
| process crash | local journal may be incomplete | possible | restart bootstrap/sync/reconcile | no | reconstruct/hold | Engine restarts `BOOTING` | mandatory | REQ-EXEC-0176/0178 |
| restart after send/fill/recovery | exact crash boundary unknown | possible/actual | journal+exchange reconstruction | no | reconstruct conservative | `BOOTING->SYNCING->RECONCILING` | mandatory | REQ-EXEC-0176/0177 |
| balance mismatch | exchange/local difference material | exposure not explained | stop READY; investigate/resolve | no affected/global policy | hold/recompute | Reconcile `COMPARING/UNRESOLVED` | mandatory | REQ-EXEC-0175 |
| duplicate fill | duplicate ID known | already applied | no-op; retain evidence | unchanged | unchanged | state unchanged | reconcile only if payload conflicts | REQ-EXEC-0127/0195 |
| out-of-order incompatible fill/status | temporal/state conflict | possible actual | flag `OUT_OF_ORDER_EVENT`; fetch truth | no affected | hold | no terminal regression | required | REQ-EXEC-0196 |
| dust | amount known, below executable/policy threshold | real small exposure | retain/buffer/rebalance/recover | no hidden reuse | converted/explicit | `DUST_EXPOSURE` handling; route not falsely complete | policy/reconcile | REQ-EXEC-0148 |
| next-leg minimum-notional failure | actual partial too small | real intermediate | `PendingIntermediateBuffer` or recover | no invalid order | converted/held | continuation blocked | recovery/rebalance as policy | REQ-EXEC-0157 |
| Recovery order partial/fails | remaining exposure recomputed; submit may be unknown | residual | reconcile, refresh, new plan/version | no opportunity risk | convert/hold | Recovery verify->plan or failed | mandatory before retry | REQ-EXEC-0171 |
| reconciliation timeout | truth not proved | possible/actual unexplained | preserve locks; later retry/manual/halt | no affected | hold | `...->UNRESOLVED` | remains required | REQ-EXEC-0172/0174 |

## Result

Failure branches documented: **28**. Each distinguishes proof of no transmission/no fill from possible economic effect. No failure path uses timeout, cancel request, missing ACK, or local journal state as proof of zero exposure.
