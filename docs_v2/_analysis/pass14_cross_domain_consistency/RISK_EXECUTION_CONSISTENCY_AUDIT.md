# Risk–Execution Consistency Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Boundary | Risk responsibility | Execution responsibility | Invariant/result |
|---|---|---|---|
| candidate eligibility | remove hard-invalid actions before optimization | no order yet | PASS |
| sizing | ceiling/gates and later permission | consume approved total q only | PASS; Sizer owner clarified |
| T0 | evaluate detection state | retain candidate/trace | PASS |
| T1 | revalidate before reservation | request atomic claim | PASS |
| T2 | immediate pre-send check | create/send current immutable intent | PASS |
| T3 | decide after each actual fill | apply fill immediately | PASS |
| T4 | authorize every next leg | use actual prior output/fees/rounding | PASS |
| T5 | continuously gate resting maker | manage rest/reprice/cancel/fills | PASS |
| `UNKNOWN` | block affected new risk; permit scoped safe actions | query/cancel/reconcile, retain reservations | PASS |
| Recovery | authorize bounded risk reduction | execute only new approved plan | PASS |
| kill switch | choose scoped safe set | cancel/reconcile/recover/halt as commanded | PASS |
| `InfraState=UNSAFE` | no new risk | keep safe exits/evidence available | PASS AFTER FIX |
| capability loss | reject/shrink dependent action | never infer permission from code/transport | PASS |

Risk action enum remains `ALLOW`, `ALLOW_REDUCED_SIZE`, `ALLOW_RECOVERY_ONLY`, `REJECT`, `HALT_MARKET`, `HALT_STRATEGY`, `HALT_GLOBAL`. An operator, transport, optimizer, model, HOT tier or positive PnL cannot restore an action removed by a hard gate. Risk bypasses: **0**. Execution-truth ambiguities left unclassified: **0**.
