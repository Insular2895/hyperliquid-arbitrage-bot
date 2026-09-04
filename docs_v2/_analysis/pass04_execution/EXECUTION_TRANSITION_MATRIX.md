# PASS 04 — Execution Transition Matrix

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

Legend: `hold` = retain conservative reservation; `convert` = reservation portion becomes actual exposure; `release` only after terminal proof. Every transition is reduced by the single writer and recorded asynchronously. “Recon?” says whether reconciliation is mandatory before resource release/readiness.

## EngineState — 15 transitions

| FROM | EVENT / CONDITION | GUARD | ACTION | TO | RESERVATION EFFECT | INVENTORY EFFECT | RISK EFFECT | PERSISTENCE | RECON? | SOURCE REQUIREMENT |
|---|---|---|---|---|---|---|---|---|---|---|
| `BOOTING` | bootstrap complete | config/local state load valid | start sync | `SYNCING` | reconstruct only | none | no new risk | transition | yes | REQ-EXEC-0102/0103 |
| `BOOTING` | critical bootstrap fail | cannot operate safely | record/halt | `HALTED` | retain reconstructed locks | none | halt | reason+transition | yes | REQ-EXEC-0102/0108 |
| `SYNCING` | required data available | current enough to compare | request reconcile | `RECONCILING` | reconstruct | snapshot only | no new risk | sync evidence | yes | REQ-EXEC-0103/0104 |
| `SYNCING` | bounded dependency impaired | safe degraded policy exists | expose impairment | `DEGRADED` | conservative | none | reduce authority | health event | yes before READY | REQ-EXEC-0103/0106 |
| `RECONCILING` | `CONSISTENT` | all required health/Risk gates | publish snapshots | `READY` | proven state | proven inventory | allow gated new risk | proof+transition | complete | REQ-EXEC-0104/0105 |
| `RECONCILING` | exposure requires reduction | current exposure known enough | prioritize Recovery | `RECOVERY_ONLY` | hold/convert | actual | no new risk | reason+transition | ongoing | REQ-EXEC-0104/0107 |
| `RECONCILING` | critical `UNRESOLVED` | no safe automatic path | escalate | `HALTED` | hold | uncertain/proven | halt | evidence | required | REQ-EXEC-0104/0108 |
| `READY` | noncritical health degradation | bounded policy | stop/reduce admission | `DEGRADED` | active unchanged | actual | reduce | health transition | before READY | REQ-EXEC-0105/0106 |
| `READY` | active exposure safety event | Recovery permitted | prioritize existing exposure | `RECOVERY_ONLY` | hold/convert | actual | no new risk | reason | as needed | REQ-EXEC-0105/0107 |
| `READY` | critical unsafe event | halt condition | stop automated risk | `HALTED` | hold | actual/uncertain | halt | reason | yes | REQ-EXEC-0105/0108 |
| `DEGRADED` | health restored | re-proof required | sync/reconcile | `SYNCING`/`RECONCILING` | hold | actual | no promotion yet | transition | yes | REQ-EXEC-0106 |
| `DEGRADED` | critical deterioration | no safe bounded operation | halt | `HALTED` | hold | actual | halt | reason | yes | REQ-EXEC-0106/0108 |
| `RECOVERY_ONLY` | exposure resolved | recovery verified | request global proof | `RECONCILING` | reconcile | reduced | no new risk yet | completion | yes | REQ-EXEC-0107 |
| `RECOVERY_ONLY` | recovery fails beyond policy | no permitted plan | escalate | `HALTED` | hold | residual | halt/manual | failure | yes | REQ-EXEC-0107/0164 |
| any active | shutdown / safe completion | authorized control + close policy | settle/persist/stop | `SHUTTING_DOWN` -> `STOPPED` | reconcile active | final actual | no new risk | shutdown events | as required | REQ-EXEC-0101; SRC-005 §156 |

## RouteExecutionState — 20 transitions

| FROM | EVENT / CONDITION | GUARD | ACTION | TO | RESERVATION EFFECT | INVENTORY EFFECT | RISK EFFECT | PERSISTENCE | RECON? | SOURCE REQUIREMENT |
|---|---|---|---|---|---|---|---|---|---|---|
| `DETECTED` | candidate admitted to check | Engine permits evaluation | capture current versions | `VALIDATING` | none | none | no effect yet | route detected | no | REQ-EXEC-0110/0111 |
| `VALIDATING` | known reject | no exposure | reasoned abort | `ABORTED` | none | none | rejected | decision | no | REQ-EXEC-0111 |
| `VALIDATING` | current gates pass | Risk/current facts valid | request atomic reservations | `RESERVING` | request | none | proposed | transition | no | REQ-EXEC-0111/0112 |
| `RESERVING` | reservation fails | no send | release acquired safe subset | `ABORTED` | release | none | reject | reason | no | REQ-EXEC-0112/0113 |
| `RESERVING` | all reservations held | versions consistent | freeze plan | `PLANNED` | hold | none | capacity consumed | plan event | no | REQ-EXEC-0112/0114 |
| `PLANNED` | pre-send envelope valid | current check passes | create first intent | `EXECUTING` | hold | none | permitted | intent event | no | REQ-EXEC-0114/0115 |
| `PLANNED` | envelope invalid before possible send | provably no order | abort/replan new version | `ABORTED` | release after proof | none | no new risk | invalid reason | maybe | REQ-EXEC-0114; SRC-005 §228 |
| `EXECUTING` | first leg known zero fill | order terminal | skip remaining legs | `ABORTED` | release after reconcile | none | no new risk | result | yes terminal | REQ-EXEC-0140 |
| `EXECUTING` | actual leg fill + continuation best | next leg current-gated | resize from actual | `EXECUTING` | convert/hold next | actual update | recheck | fill+intent | no if truth known | REQ-EXEC-0141/0142/0144 |
| `EXECUTING` | actual partial + continuation valid | min/price/Risk pass | smaller next leg | `EXECUTING` | convert/resize | actual partial | recheck | fill+plan trace | no if known | REQ-EXEC-0146/0147 |
| `EXECUTING` | exposure + continuation invalid | current recovery preferred | snapshot exposure | `RECOVERY_REQUIRED` | hold/convert | actual | recovery-only same capital | trigger | maybe | REQ-EXEC-0145/0149/0165 |
| `EXECUTING` | send/order ambiguity | economic outcome possible | query truth | `RECONCILING` | hold | possible | block affected new risk | ambiguity | yes | REQ-EXEC-0132/0172 |
| `EXECUTING` | closure criteria all true | terminal orders/fills/dust/reservations/accounting | finalize | `COMPLETED` | release proven remainder | final actual | capacity returned | completion | complete | REQ-EXEC-0150 |
| `RECOVERY_REQUIRED` | exposure known | Recovery starts | transfer context | `RECOVERY_REQUIRED` | hold | actual | recovery gate | recovery started | as needed | REQ-EXEC-0164/0165 |
| `RECOVERY_REQUIRED` | exposure uncertain | cannot size safely | request proof | `RECONCILING` | hold | uncertain | block | request | yes | REQ-EXEC-0132/0172 |
| `RECOVERY_REQUIRED` | `RECOVERED` | route closure criteria | finalize actual route | `COMPLETED` | reconcile/release | reduced/permitted dust | return capacity | completion | yes | REQ-EXEC-0164/0150 |
| `RECOVERY_REQUIRED` | `RECOVERY_FAILED` | limits/no plan | fail conservative | `FAILED_SAFE` | hold as needed | residual | halt affected scope | failure | yes | REQ-EXEC-0171 |
| `RECONCILING` | truth says safe known abort | zero exposure | close | `ABORTED` | release proven | none | no risk | proof | complete | REQ-EXEC-0174 |
| `RECONCILING` | truth permits continuation | plan/current gates valid | resume at proven quantity | `EXECUTING` | reconcile/hold | actual | recheck | proof | complete | REQ-EXEC-0174 |
| `RECONCILING` | exposure remains / unresolved | recover if known; else escalate | conservative branch | `RECOVERY_REQUIRED`/`FAILED_SAFE` | hold | actual/uncertain | no new risk | result | yes | REQ-EXEC-0174/0175 |

## OrderState — 23 transitions

| FROM | EVENT / CONDITION | GUARD | ACTION | TO | RESERVATION EFFECT | INVENTORY EFFECT | RISK EFFECT | PERSISTENCE | RECON? | SOURCE REQUIREMENT |
|---|---|---|---|---|---|---|---|---|---|---|
| `CREATED` | nonce assigned | single NonceManager | bind nonce | `NONCE_ASSIGNED` | hold | none | unchanged | nonce event | no | REQ-EXEC-0120/0121/0122 |
| `NONCE_ASSIGNED` | sign succeeds | intent current/immutable | freeze signature/economics | `SIGNED` | hold | none | unchanged | signed metadata | no | REQ-EXEC-0123 |
| `NONCE_ASSIGNED` | sign fails | definitely unsent | local fail/route abort | no exchange transition | hold/release after route proof | none | reject | reason | no | REQ-EXEC-0123 |
| `SIGNED` | send begins/may transmit | transport request correlated | mark possible effect | `SENT` | hold | possible soon | committed capacity | OrderSent | yes if response absent | REQ-EXEC-0124 |
| `SIGNED` | definite pre-transmission failure | transport proves unsent | local fail | no exchange transition | route decides | none | reject | reason | no | REQ-EXEC-0124 |
| `SENT` | nonterminal/awaiting evidence | no final truth | start resolution | `PENDING_RESOLUTION` | hold | possible | no reuse | state/timer | maybe | REQ-EXEC-0125 |
| `SENT`/`PENDING_RESOLUTION` | resting evidence | exchange says active | start maker monitoring | `RESTING` | hold remainder | none/fills separately | active order limits | update | no | REQ-EXEC-0128 |
| `SENT`/`PENDING_RESOLUTION` | unique partial fill | `0<filled<requested` | apply actual | `PARTIALLY_FILLED` | convert used/hold rest | update | recheck | FillApplied | no if consistent | REQ-EXEC-0127/0129 |
| `SENT`/`PENDING_RESOLUTION` | full cumulative fill | within tolerance | apply all actual | `FILLED` | convert | update | next-leg gate | FillApplied | terminal proof | REQ-EXEC-0130 |
| `SENT`/`PENDING_RESOLUTION` | explicit reject | evidence unambiguous | map reason | `REJECTED` | hold until proof | none for order | reject/recovery if prior | update | yes terminal | REQ-EXEC-0131 |
| `SENT`/`PENDING_RESOLUTION` | timeout/ambiguous | outcome may exist | query | `UNKNOWN` | hold | possible | block affected risk | reason | yes | REQ-EXEC-0118/0132 |
| `RESTING` | unique partial fill | valid cumulative quantity | apply/reevaluate | `PARTIALLY_FILLED` | convert/hold | update | current maker/Risk gate | fill | no if consistent | REQ-EXEC-0129/0155 |
| `RESTING` | full fill | cumulative full | apply | `FILLED` | convert | update | continuation gate | fill | terminal proof | REQ-EXEC-0130 |
| `RESTING`/`PARTIALLY_FILLED` | cancel requested | policy/edge/age/feed trigger | send cancel; assume live | `CANCEL_REQUESTED` | hold remaining | existing actual | no increased risk | CancelRequested | yes if lost | REQ-EXEC-0133/0158 |
| `PARTIALLY_FILLED` | another partial | unique fill | update actual and decisions | `PARTIALLY_FILLED` | convert/hold | update | recheck | fill | no if consistent | REQ-EXEC-0129 |
| `PARTIALLY_FILLED` | cumulative full | tolerance valid | apply/finalize individual order | `FILLED` | convert | update | continuation/recovery | fill | yes terminal | REQ-EXEC-0130 |
| `CANCEL_REQUESTED` | fill races | unique valid fill | apply/recompute residual | `PARTIALLY_FILLED`/`FILLED` | convert/hold | update | hedge/recover | fill | yes final | REQ-EXEC-0134/0158 |
| `CANCEL_REQUESTED` | cancel confirmed, residual inactive | all prior fills considered | mark canceled | `CANCELED` | hold until final proof | actual prior fills | no new order yet | update | yes | REQ-EXEC-0135 |
| `CANCEL_REQUESTED` | response lost/contradictory | inactivity unproved | query | `UNKNOWN` | hold | possible | block | reason | yes | REQ-EXEC-0132/0134 |
| `UNKNOWN` | query proves active | identity matches | resume known lifecycle | `RESTING`/`PARTIALLY_FILLED` | hold/convert | actual | recheck | proof | ongoing | REQ-EXEC-0132/0137 |
| `UNKNOWN` | query proves terminal | all fills fetched | apply actual outcome | `FILLED`/`CANCELED`/`REJECTED` | convert/hold | update | appropriate | proof | yes terminal | REQ-EXEC-0132/0137 |
| `FILLED`/`CANCELED`/`REJECTED` | status+fills+balance agree | no unexplained effect | finalize | `TERMINAL_RECONCILED` | convert/release | final | return capacity | terminal event | complete | REQ-EXEC-0136 |
| any terminal-known | duplicate/late incompatible event | duplicate or monotonicity guard | no-op or flag | same state | unchanged | unchanged | reconcile if conflict | dedupe/error | if conflict | REQ-EXEC-0126/0195/0196 |

## RecoveryState — 11 transitions

| FROM | EVENT / CONDITION | GUARD | ACTION | TO | RESERVATION EFFECT | INVENTORY EFFECT | RISK EFFECT | PERSISTENCE | RECON? | SOURCE REQUIREMENT |
|---|---|---|---|---|---|---|---|---|---|---|
| `RECOVERY_REQUIRED` | actual exposure proven | current state fresh enough | enumerate exits | `RECOVERY_PLANNING` | hold | snapshot actual | no same-capital new risk | trigger | maybe | REQ-EXEC-0165/0167 |
| `RECOVERY_REQUIRED` | exposure uncertain | cannot safely size | query truth | same | hold | possible | block | request | yes | REQ-EXEC-0132/0174 |
| `RECOVERY_PLANNING` | candidate passes Recovery Risk/QF-079 | bounded current plan | reserve | `RECOVERY_RESERVED` | add recovery locks | actual | risk reduction authorized | plan | no | REQ-EXEC-0166/0168 |
| `RECOVERY_PLANNING` | no permitted candidate | all bounded options exhausted | escalate | `RECOVERY_FAILED` | hold | residual | halt/manual | reason | yes | REQ-EXEC-0171 |
| `RECOVERY_RESERVED` | current envelope valid | capacities held | submit child intents | `RECOVERY_EXECUTING` | hold | unchanged until fills | recovery gate | intents | no | REQ-EXEC-0168 |
| `RECOVERY_RESERVED` | stale/fail reservation | no possible send | replan or fail | `RECOVERY_PLANNING`/`RECOVERY_FAILED` | release proven new locks | actual | no expansion | reason | maybe | REQ-EXEC-0171 |
| `RECOVERY_EXECUTING` | known full/zero/partial terminal | actual fills applied | verify remaining | `RECOVERY_VERIFYING` | convert/hold | update | re-evaluate | fills | yes terminal | REQ-EXEC-0171 |
| `RECOVERY_EXECUTING` | unknown outcome | possible exposure change | query/reconcile | same | hold | possible | no new risk | ambiguity | yes | REQ-EXEC-0171 |
| `RECOVERY_VERIFYING` | exposure within policy/account consistent | QF-080 actual loss computed | close | `RECOVERED` | release proven | final | return affected authority through route | completion | complete | REQ-EXEC-0164/0166 |
| `RECOVERY_VERIFYING` | residual with valid alternatives | limits remain | recompute from actual | `RECOVERY_PLANNING` | reconcile/hold | residual | bounded reduction | new version | maybe | REQ-EXEC-0171 |
| `RECOVERY_VERIFYING` | no safe resolution/limits exhausted | no blind retry | escalate | `RECOVERY_FAILED` | hold as needed | residual | halt/manual | failure | yes | REQ-EXEC-0169/0171 |

## ReconciliationState — 9 transitions

| FROM | EVENT / CONDITION | GUARD | ACTION | TO | RESERVATION EFFECT | INVENTORY EFFECT | RISK EFFECT | PERSISTENCE | RECON? | SOURCE REQUIREMENT |
|---|---|---|---|---|---|---|---|---|---|---|
| `RECONCILE_REQUESTED` | scope frozen | affected resources identified | start queries | `FETCHING` | hold | unchanged | block scope | request | active | REQ-EXEC-0172/0173 |
| `FETCHING` | required order/fill/balance data available | snapshot coherent enough | begin comparison | `COMPARING` | hold | unchanged | block | fetch provenance | active | REQ-EXEC-0173/0174 |
| `FETCHING` | timeout/data unavailable | cannot prove truth | record gap | `UNRESOLVED` | hold | uncertain | block/escalate | failure | required later | REQ-EXEC-0174/0180 |
| `COMPARING` | all local/exchange facts agree | fills deduped, balances within tolerance | record proof | `CONSISTENT` | align/release proven | proven | caller may re-gate | proof | complete | REQ-EXEC-0174/0175 |
| `COMPARING` | discrepancies explainable | unique missing facts available | apply through reducer | `RESOLVING` | hold | pending actual | block | diff | active | REQ-EXEC-0174 |
| `COMPARING` | material unexplained mismatch | cannot safely correct | preserve evidence | `UNRESOLVED` | hold | uncertain | block/halt scope | mismatch | required | REQ-EXEC-0175 |
| `RESOLVING` | missing fills/status applied | recompare orders->fills->balances | verify | `COMPARING` | recompute | update actual | block until proof | applied events | active | REQ-EXEC-0174 |
| `RESOLVING` | resolution exhausted | mismatch remains | escalate | `UNRESOLVED` | hold | uncertain/residual | block | failure | required | REQ-EXEC-0174/0175 |
| `UNRESOLVED` | later fresh evidence / authorized retry | scope remains locked | refetch | `FETCHING` | hold | unchanged until evidence | block | retry reason | active | REQ-EXEC-0174 |

## Control total

Canonical transition rows documented: **78** (15 Engine + 20 Route + 23 Order + 11 Recovery + 9 Reconciliation). Composite arrows such as shutdown and multi-target evidence branches are deliberately one guarded row where the source describes one semantic transition family.
