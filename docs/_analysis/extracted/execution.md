# Extraction — Execution

## Source d'autorité

- SRC-004, Dossier 1/6, lignes 1–3225 environ.
- Statut documentaire : final / normatif.

## Décisions LOCKED

- La stratégie ne contacte jamais l'exchange. Elle produit un `ExecutionPlan`;
  `ExecutionCoordinator`, `OrderStateMachine` et `ExecutionTransport` possèdent
  l'exécution.
- Cinq automates coordonnés restent séparés : `EngineState`,
  `RouteExecutionState`, `OrderState`, `RecoveryState`,
  `ReconciliationState`.
- `EngineState` : `BOOTING → SYNCING → RECONCILING → READY`, plus
  `DEGRADED`, `RECOVERY_ONLY`, `HALTED`, `SHUTTING_DOWN`, `STOPPED`.
  `HALTED` ne revient jamais directement à `READY`.
- `RouteExecutionState` : `DETECTED → VALIDATING → RESERVING → PLANNED →
  EXECUTING → COMPLETED`, avec `ABORTED`, `RECOVERY_REQUIRED`,
  `RECONCILING`, `FAILED_SAFE`.
- Réserver soldes, profondeur et budgets avant l'ordre. Toute ressource touchée
  par un ordre `UNKNOWN` reste réservée.
- Un `ExecutionPlan` planifié est immuable; toute révision est versionnée.
- Chaque intention reçoit avant envoi un CLOID stable. `timeout → UNKNOWN →
  query/reconcile`; aucun blind retry.
- `OrderState` couvre au minimum `CREATED`, `NONCE_ASSIGNED`, `SIGNED`, `SENT`,
  `PENDING_RESOLUTION`, `RESTING`, `PARTIALLY_FILLED`, `FILLED`,
  `CANCEL_REQUESTED`, `CANCELED`, `REJECTED`, `UNKNOWN`, puis
  `TERMINAL_RECONCILED`.
- Après `SENT`, l'ordre est potentiellement exécuté jusqu'à preuve contraire.
  `cancel sent ≠ canceled`; les cancel races sont normales.
- Les fills sont des événements économiques immuables, append-only et
  dédupliqués. L'état se réduit depuis plusieurs canaux exchange, pas depuis le
  seul ACK HTTP.
- Toute jambe suivante consomme la sortie réelle précédente après fills, frais
  et rounding. Jamais la sortie théorique.
- TT/TTT utilisent des IOC limit protégés. MT/MTT utilisent ALO pour la première
  jambe maker. TM/MM sont représentables mais désactivés jusqu'à validation.
- Après chaque fill/partial, comparer `EV_continue` et `EV_recovery`. La route
  d'origine n'a aucun privilège.
- Recovery peut être négative en EV, mais conserve freshness, prix/notional
  d'urgence et limites. Elle peut choisir plusieurs sorties ou un split.
- Reconciliation compare ordres, fills, soldes et état local à la vérité
  exchange. Aucun nouveau risque tant que la différence n'est pas résolue.
- Un processus live utilise un signer et un `NonceManager` unique; la génération
  de nonces n'est pas distribuée entre threads.
- Transport HTTP, WebSocket et Replay sont interchangeables derrière
  `ExecutionTransport`; le benchmark sélectionne le transport live.
- Priorité scheduler : cancel/safety, recovery, reconciliation, continuation
  existante, puis nouvelles opportunités.

## CALIBRATED

- `ACK_TIMEOUT`, `UNKNOWN_RESOLUTION_TIMEOUT`, `MAKER_MAX_AGE`,
  `RECONCILE_TIMEOUT`, `RECOVERY_TIMEOUT`, route timeout et tolérance dust.
- Transport direct ou batché; HTTP ou WebSocket; compromis exact journal
  durable/latence.
- Maker max age dépend de la distribution de fill, de la survie de l'edge et de
  l'adverse selection.

## Cas limites obligatoires

- zero fill, partial fill, partial sous min-notional/dust, partial maker,
  cancellation après partial, leg suivante non viable;
- ACK perdu après exécution, fill dupliqué, fill pendant cancellation, ordre
  inconnu, balance mismatch, crash après send et avant ACK persisté;
- perte du feed marché ou compte, reconnect, ordre terminal avec fills tardifs;
- recovery order échoué : reconcile, refresh, recompute, nouveau plan — jamais
  resoumission aveugle.

## Tests prescrits

- Scénarios déterministes full/zero/partial, edge death, timeout, duplication,
  cancel race, crash, mismatch, stale feed.
- Properties : quantités et réservations non négatives, fill borné, état terminal
  monotone, idempotence d'un fill, verrouillage du capital inconnu, impossibilité
  de nouveau risque hors des états autorisés.
- Même stream d'événements/config/modèles produit les mêmes transitions,
  intentions et résultats comptables.

## Faits externes à revalider

`EXTERNAL_RULE_REQUIRES_REVALIDATION` : CLOID/nonce, endpoints et statuts
Hyperliquid, semantics IOC/ALO, `scheduleCancel`, cadence/batching recommandé,
limites quotidiennes du dead-man switch et capacités HTTP/WS.
