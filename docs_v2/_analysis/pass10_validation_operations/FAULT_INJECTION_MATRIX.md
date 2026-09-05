# Fault Injection Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Injection | Expected safe behavior | Required proof |
|---|---|---|
| stale/gapped/corrupt/crossed book | affected new risk off; rebuild from valid snapshot | stale state never admitted; book versions/quality logged |
| market feed loss/reconnect loop | maker policy, no new risk, resubscribe/rebuild | healthy feed criterion and downstream reconciliation |
| account/order/fill feed loss | no new risk; query-based reconciliation | orders→fills→balances consistency |
| lost submit/HTTP response | UNKNOWN; CLOID query; no blind resend | exactly one economic effect or unresolved lock |
| duplicate/out-of-order fill/event | idempotent apply; incompatible transition rejected | fill ledger and state hash unchanged after duplicate |
| cancel/fill race | apply fill truth, cancel remainder state | no false terminal/no released filled capacity |
| process/container/host crash at each journal boundary | restart non-ready; reconstruct/reconcile | no duplicate order, missing exposure or stale READY |
| crash during Recovery/update/migration | preserve exposure/step markers; resume/compensate safely | current exchange truth wins |
| reservation/balance mismatch | block affected capacity/new risk | reconciliation proof before release |
| model unavailable/corrupt/NaN/OOD/disagreement/drift | fallback/reduce/reject; dependent capability degrade | no unsafe model output enters RiskDecision |
| Simulator miscalibration | confidence/size reduction or dependent kill | Q_validated demotion and evidence retained |
| clock offset/uncertainty/failure | disable latency-sensitive decisions; possible recovery-only | alert, benchmark invalidity and stable resync proof |
| CPU saturation/scheduler jitter | reduce new risk before uncontrolled lag | tail latency and state transition evidence |
| memory pressure | degrade/fail safely without corrupting state | resource, queue and restart/reconcile evidence |
| disk low/full/write/fsync failure | hot path safe; recorder degrade; escalate if critical persistence fails | no silent loss; pinned incident evidence protected |
| recorder backlog/backpressure | priority policy; no hot-path block | loss/invalid-region accounting and drain behavior |
| network route loss/API errors/rate limit | bounded retry only for safe idempotent operations | no duplicate order; degraded state |
| signer/secret unavailable or compromised | no new signing; fence/rotate/escalate | secret-free artifacts and clean authority proof |
| invalid config/schema/model/formula compatibility | fail preflight/READY | exact reject reason and previous safe state retained |
| license outage/revocation | no new risk; cancel/reconcile/Recovery/read access retained | commercial control cannot trap exposure |
| interrupted download/update/rollback | reject incomplete artifact; transactional recovery | verified current/previous digest and reconciled startup |
| split-brain/ambiguous owner | fence; no new risk | single active owner before readiness |
| exchange-rule/metadata change | suspend affected market/mode | external revalidation and regression evidence |

Every injection asserts economic state, permissions, records, alerts, operator action and recovery—not just process survival.

Literal catalog coverage: feed disconnect, account disconnect, gap, stale or crossed book; lost submit; duplicate fill or partial fill; cancel race; exchange reject; SIGTERM, SIGKILL or reboot; disk full or slow disk; Recorder overflow; CPU saturation; clock drift; invalid config, invalid schema or invalid model; nonce contention; secret or license failure; interrupted update or rollback.
