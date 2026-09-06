# PASS 12 — Implementation Blocker Register

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Blocker ID | Domain | Phase | Evidence stage | Class / severity | Why blocking | Source | Owner | Required before |
|---|---|---:|---:|---|---|---|---|---|
| `RB-001` | Governance | 1 | 0 | `BLOCKING/HIGH` | Critical contract ambiguity would force invented architecture | SRC-006 6175–6181; PASS 12 | Human architecture owner | Affected implementation |
| `RB-002` | Formula/numeric | 1, 7 | 0/4 | `BLOCKING/HIGH` | `OPEN-017..028` must be resolved where a formula implementation needs the omitted convention | PASS11 | Formula owner | Specific formula coding/promotion |
| `RB-003` | Exchange wire | 2 | 1 | `BLOCKING/HIGH` | Current payload/event semantics define parser truth | External register | Adapter/Data owner | Adapter conformance |
| `RB-004` | Recorder | 3 | 1 | `BLOCKING/HIGH` | No trusted dataset/evidence if critical capture ordering/durability fails | PASS06/10 | Recorder owner | M2 and capital |
| `RB-005` | Book | 4 | 2 | `BLOCKING/HIGH` | Unknown snapshot/diff/sequence semantics can corrupt state | External register | Book/Adapter owner | Trusted reconstruction |
| `RB-006` | Fees/precision | 5, 7 | 2/4 | `BLOCKING/HIGH` | Wrong rules create false economics/orders | External register | Metadata/Fee/Precision owner | Exact opportunity/transport |
| `RB-007` | Risk parameters | 11, 17, 20 | 5/10 | `BLOCKING/HIGH for capital` | Mechanism is fixed, exact limits need evidence/approval | `OPEN-007/009` | Risk/Capital owner | Micro-live/size promotion |
| `RB-008` | Execution transport | 13 | 7/10 | `BLOCKING/HIGH` | Signing/nonce/order/cancel/lookup semantics are current external facts | External register | Execution/Security owner | Shadow integration/Micro-live |
| `RB-009` | Recovery/Reconciliation | 14 | 10 | `BLOCKING/CRITICAL` | No real capital with unresolved actual exposure/account truth | PASS04/05/10 | Execution/Risk owner | Any Micro-live |
| `RB-010` | Deployment/Ops | 19–20 | 7/10 | `BLOCKING/CRITICAL` | Safe startup/shutdown/rollback/alerts/ownership must exist before probes | PASS09/10 | Deployment/Ops owner | Micro-live |
| `RB-011` | Evidence | 20 | 8/10 | `BLOCKING/HIGH` | Prediction↔actual joins/stops must be declared before intervention | PASS10 | Validation owner | First probe |
| `RB-012` | Participants | 21 | 9 | `NON-BLOCKING RESEARCH` | Exact horizons/models remain learned; conservative/no-model baseline permits TT evidence | `OPEN-008/010/016` | Model owner | Model-dependent promotion only |
| `RB-013` | Advanced Simulator | 22 | 13 | `FUTURE` | F4 lacks required truth/calibration and must not block TT | PASS03/10 | Simulator owner | Any F4 decision authority |
| `RB-014` | Maker modes | 23 | 13/14 | `BLOCKING for MT/MTT` | Queue/fill/adverse/cancel/recovery evidence absent initially | `OPEN-012` | Maker/Execution/Risk | MT/MTT probe |
| `RB-015` | Portfolio | 24 | 16 | `NON-BLOCKING RESEARCH` | Complex optimizer must beat simple allocation; irrelevant to first route | PASS07/10 | Capital owner | Portfolio promotion |
| `RB-016` | Bridge | 25 | 15/17 | `BLOCKING for Bridge` | Future utility/exit history and STAY comparison unavailable initially | PASS07 | Capital/Atlas owner | Bridge probe |
| `RB-017` | Infrastructure | 26 | 20 | `NON-BLOCKING RESEARCH` | Node/private/high-end host needs economic evidence, not prestige | PASS01/10 | Infra owner | Infra promotion only |
| `RB-018` | Cross-exchange | — | — | `FUTURE` | Settlement/transfer/venue Risk/Data/ops not specified for V1 | PASS08 | PASS13/Future owner | Cross-exchange capability |

`BLOCKING` is scoped: unresolved maker evidence does not block initial TT; unresolved F4, node, hot standby or cross-exchange work does not block V1 TT.
