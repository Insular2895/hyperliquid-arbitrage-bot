# 10 — Execution State Machine

## Machines distinctes

Fusionner ces machines est interdit : `EngineState`, `RouteExecutionState`,
`OrderState`, `RecoveryState`, `ReconciliationState`. Chaque transition produit
un événement persistable/idempotent et dispose d'un reason code.

## EngineState

```text
BOOTING → SYNCING → RECONCILING → READY
                         │         ├→ DEGRADED
                         │         ├→ RECOVERY_ONLY
                         │         └→ HALTED
SHUTTING_DOWN → STOPPED
```

`READY` seul autorise un nouveau risque. `DEGRADED` suit une matrice de
capabilities explicite; jamais « un peu sûr ». `RECOVERY_ONLY` autorise actions
réductrices et reconciliation. Restart repasse toujours par sync/reconcile.
`HALTED` ne retourne jamais directement à `READY`.

## RouteExecutionState

```text
DETECTED → VALIDATING → RESERVING → PLANNED → EXECUTING → COMPLETED
                └──────────────→ ABORTED
EXECUTING → RECOVERY_REQUIRED → RECONCILING → COMPLETED/FAILED_SAFE
                         └────────────────────→ FAILED_SAFE
```

`COMPLETED` signifie fills/accounting/inventory reconciliés, pas seulement
« tous les submit sont partis ».

## OrderState

États canoniques du dossier de fermeture : `CREATED → NONCE_ASSIGNED → SIGNED →
SENT → PENDING_RESOLUTION`, puis branches `RESTING`, `PARTIALLY_FILLED`,
`FILLED`, `CANCEL_REQUESTED`, `CANCELED`, `REJECTED`, `UNKNOWN`; tous les états
finaux convergent vers `TERMINAL_RECONCILED` après preuve exchange.

Règles :

- CLOID stable par intention; retry transport ne crée pas une nouvelle intention.
- `SENT`, timeout, disconnect ou réponse perdue peuvent cacher un fill.
- `CANCEL_REQUESTED` ne libère aucune réservation.
- FillLedger append-only/dédupliqué; chaque fill appliqué une fois.
- Exchange order/account stream prime sur supposition locale.

## Modes et ordres

- TT/TTT: protected IOC limit taker.
- MT/MTT: première jambe ALO/Post Only avec expiry calibrée, reste protected IOC.
- TM/MM: disabled.
- Batch éventuel ne signifie jamais atomicité des fills.
- La jambe N+1 utilise la somme réelle dédupliquée des fills de N, quantifiée.

## Boucle après événement

```text
ingest order/fill/account event
→ dedupe and append
→ recompute actual exposure/reservations
→ refresh point-in-time books/fees/risk
→ compare completion, wait/cancel, EV_continue, EV_recovery
→ act only within current permissions
```

La route originale n'a aucun privilège. Recovery peut aller vers intended B,
original A, CORE asset ou split, selon QF-079.

## RecoveryState

`RECOVERY_REQUIRED → RECOVERY_PLANNING → RECOVERY_RESERVED →
RECOVERY_EXECUTING → RECOVERY_VERIFYING → RECOVERED`; échec :
`RECOVERY_FAILED → MANUAL/HARD HALT`. Un échec d'ordre recovery conduit à
reconcile, refresh, recompute exposure, nouveau plan — jamais même-paramètres
rejoués aveuglément.

## ReconciliationState

`RECONCILE_REQUESTED → FETCHING → COMPARING → RESOLVING → CONSISTENT`; ou
`UNRESOLVED`. Vérifier open orders, order status, user fills, balances, local
OrderLedger/FillLedger et reservations. Tant que non `CONSISTENT` : aucune
nouvelle exposition.

## Nonce et signer

Un signer/NonceManager par process/account initialement. Nonces monotones,
persistés/reconciliés selon règle exchange revalidée. Secret hors mémoire/logs
au strict minimum; aucune concurrence non coordonnée sur le même wallet.

## Timers

ACK timeout, cancel timeout, maker max age, stale thresholds et backoffs sont
`CALIBRATED`. Ils ne changent pas les axiomes no-blind-retry/unknown/reconcile.

## Sources

SRC-004 D1, SRC-005 Risk/Data, SRC-006 failure injection.
