# 18 — Operations and Monitoring

## États observables

Afficher séparément process liveness, readiness for new risk, trading capability,
EngineState, Recovery/Reconciliation state, feed/book/account health, config/model
versions et dernière preuve de sync. « Running » ne veut pas dire « trading ».

## Métriques

- Market/data : messages, drops/gaps, reconnects, feed/book age, invalid books,
  metadata age, recorder sequence/queue/backlog.
- Decision : opportunities/rates, execute/reject par reason, BBO→L2 funnel,
  route/asset/HOT state et decision latency.
- Execution : submit/ack/fill latencies, fill/partial/unknown/cancel/reject rates,
  slippage/fee error, recovery/reconciliation time and loss.
- Risk/capital : actual/available/reserved/pending balances, bands/net flows,
  RAEV/P+/ES, limit utilization, kills, drawdown/MDD.
- Model : survival/fill calibration, Brier/log loss, OOD, disagreement, PnL bias,
  economic lift/drift.
- System/infra : CPU/steal/RAM/PIDs, disk/free/write latency, network/jitter,
  queue depths, container restarts, clock offset, NetPnL/InfraROI.

## Alert classes

- P0: unknown/unreconciled exposure, reservation invariant, signer/nonce/security,
  corrupted account state → new risk off, human page.
- P1: stale/gap/feed/account disconnect, recovery failure, critical disk/clock →
  affected capability off/recovery-only.
- P2: calibration drift, elevated slippage/latency/rejects, recorder backlog →
  degrade/observe and investigate.
- P3: research/storage/archive/report issues without safety impact.

Seuils sont `CALIBRATED`; alert actions sont locked and tested.

## Runbooks

1. Feed/book desync: invalidate → risk-off affected markets → reconnect/snapshot
   → compare sequences → readiness.
2. Unknown order: preserve reservations → query/stream sync → dedupe fills →
   reconcile → recovery if exposed.
3. Crash/reboot: no auto-ready → sync clocks/feed/account → reconcile → explicit
   capability check.
4. Disk pressure: protect P0/P1, rotate/archive verified chunks, degrade recorder,
   halt new risk if auditability/account data threatened.
5. Model drift/OOD: fallback champion/conservative baseline or disable feature.
6. Update failure: risk-off, rollback digest, migrate/restore safely, reconcile.
7. Suspected secret compromise: halt new risk, revoke/rotate, reconcile/audit.

## Incident package

Incident ID, UTC/monotonic timeline, relevant market windows, raw/order/fill/account
events, config/model/image/schema manifests, health/latency, reservations,
decisions/reasons and operator actions. Redacted bundle; hashes and chain of
custody; no secrets.

## SLOs and reviews

Availability alone est insuffisante. SLOs couvrent freshness, state consistency,
execution unknown/partial, recovery time, recorder completeness, prediction
calibration et readiness. Valeurs après baseline mesurée. Daily health/PnL/risk,
weekly calibration/capacity, release review, periodic restore/failure drills.

## Safe shutdown

Stop new risk, finish/cancel where safe, recover exposure, persist checkpoint and
journal, reconcile, then stop. SIGTERM follows ce chemin; SIGKILL/reboot est
traité comme crash au prochain boot.

## Sources

SRC-001/003 observability, SRC-004/005 safety, SRC-006 deployment/validation,
SRC-008 infra.
