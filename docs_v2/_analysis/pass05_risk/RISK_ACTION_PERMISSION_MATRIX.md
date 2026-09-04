# Risk Action Permission Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Legend: `YES` permitted subject to ordinary checks; `CHECK` only after a fresh contextual RiskDecision; `REDUCE` only if strictly reducing known exposure under RecoveryRiskPolicy; `NO` forbidden; `REVIEW` exact deployment/operator procedure requires future owner decision. A cancel is not assumed neutral: racing fills and market validity still matter.

| Context | New route | Increase existing risk | Continue existing leg | Maker rest | Cancel | Reconcile | Recovery | Rebalance | Risk-reducing exit | Manual action |
|---|---|---|---|---|---|---|---|---|---|---|
| `READY` | CHECK | CHECK | CHECK | CHECK/T5 | YES | YES | CHECK | CHECK | CHECK | Tighten/kill only |
| `DEGRADED` | CHECK reduced capability | CHECK reduced | CHECK | CHECK or cancel | YES | YES | CHECK | CHECK | CHECK | Tighten/kill only |
| `RECOVERY_ONLY` | NO | NO | CHECK only if safer than recovery | NO/new rest | YES | YES | CHECK | CHECK if reducing | REDUCE | Tighten/kill/escalate |
| `HALTED` | NO | NO | NO unless emergency policy explicitly permits | NO | CHECK | YES | REDUCE | NO unless reducing | REDUCE | Tighten/kill/escalate |
| `UNKNOWN ORDER` | NO on affected capacity | NO affected | NO blind continuation | NO affected | CHECK/query first | YES | CHECK after truth bound | NO affected | REDUCE only known portion | No bypass |
| `ACCOUNT UNRECONCILED` | NO affected account | NO | CHECK only proven state | NO/new rest | CHECK | YES | REDUCE only known exposure | NO | REDUCE | No bypass |
| `BOOK STALE` | NO affected route | NO | NO affected leg until valid | CANCEL unsafe rest | YES | YES/resync | CHECK only with valid exit state | NO affected route | CHECK with valid exit book | No bypass |
| `MODEL OOD` | NO if hard/mandatory; reduced only inside soft support | NO unsupported | CHECK fallback/support | CHECK or cancel | YES | YES | CHECK conservative fallback | CHECK | REDUCE | Disable/tighten |
| `INFRA UNSAFE` | NO | NO | CHECK only safety path | CANCEL | YES | YES | REDUCE | NO unless reducing | REDUCE | Infra/global kill |
| `GLOBAL_KILL` | NO | NO | NO new continuation; safety policy only | CANCEL | YES | YES | REDUCE | NO unless reducing | REDUCE | Ack/tighten; no bypass |
| `MARKET_KILL` | NO if route depends on market | NO affected | CHECK exit dependency | CANCEL affected | YES | YES | REDUCE | CHECK outside killed market | REDUCE | Ack/tighten; no bypass |
| `ASSET_KILL` | NO if route touches asset | NO affected | CHECK exit only | CANCEL affected | YES | YES | REDUCE | REDUCE | REDUCE | Ack/tighten; no bypass |
| `STRATEGY_KILL` | NO for strategy | NO for strategy | CHECK safety completion | CANCEL affected maker | YES | YES | REDUCE | CHECK independent capability | REDUCE | Ack/tighten; no bypass |
| `INCIDENT_HOLD` | NO affected scope | NO | CHECK by incident policy | CANCEL/CHECK | YES | YES | REDUCE | REVIEW | REDUCE | Investigation/ack only |

## Enforcement rules

1. `RISK_INCREASING` always requires all applicable gates.
2. Unknown classification defaults to `NO NEW RISK`.
3. `RISK_REDUCING` never means unlimited: known exposure, valid executable state, price protection and recovery bounds still apply.
4. Kill/reset or process restart does not imply `READY`; reconciliation and risk-health checks follow.
5. Client/operator actions can only tighten, kill or perform explicitly authorized safety operations.

Source: SRC-005 lines 179–242, 708–883, 2985–3329, 3875–3944 and 4762–5029; PASS 04 execution states provide the context names.
