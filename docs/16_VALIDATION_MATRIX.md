# 16 — Validation Matrix

## Échelle de maturité

`M0 SPECIFIED → M1 UNIT VALIDATED → M2 REPLAY VALIDATED → M3 SHADOW VALIDATED →
M4 MICRO-LIVE VALIDATED → M5 LIVE VALIDATED`.

Un module n'excède pas la maturité de ses dépendances critiques. « Supporté par
le code » ne signifie pas activé. Les composants touchant ordres, capital, risk
ou fills ne sautent ni Shadow ni Micro-live.

## Matrice minimale

| Domaine | M1 | M2 | M3 | M4 | M5 |
|---|---|---|---|---|---|
| Types/Data | schema/golden/property | deterministic/no-lookahead replay | live contract parity | real event audit | drift/migration proven |
| Books/Metadata | snapshot/update/gap | reconstruction golden | freshness/resync | observed feed anomalies | sustained SLO |
| NetConvert/Quant | unit/golden Rust↔Python | multi-size/regime | shadow quote parity | fill/slippage calibration | stable bias/tails |
| Graph/Opportunity | enumeration/dependency | missed/false candidates | decision logging | real availability | economic contribution |
| Inventory/Reservation/Risk | invariants/concurrency | adversarial paths | account shadow | real reservations/limits | breach-free evidence |
| Execution/Recovery | state/property/fault | emulator outcomes | real events no submit | protected tiny orders/recovery | stable unknown/partial rates |
| Models/Simulator | calibration tests | temporal OOS | shadow outcomes | actual-vs-predicted | drift/lift stable |
| Recorder/Replay | integrity/crash | deterministic manifest | live capture | incident replay | retention/restore proven |
| Infra/Deployment/Security | build/scan/config | replay/soak container | shadow canary | live canary/rollback | operational SLO |

## Test families

Unit, golden, property, integration, replay, fault injection, load, performance,
shadow, micro-live et chaos selon surface. Modules critiques ajoutent
determinism, backpressure, corruption, concurrency et restart.

## Failure injection obligatoire

Feed/account disconnect; gap/stale/crossed book; réponse submit perdue; duplicate
et partial fill; cancel race; exchange reject; process crash/SIGTERM/SIGKILL;
reboot; disk full/slow; recorder queue overflow; cloud outage; CPU saturation;
clock jump/drift; invalid config/schema/model/NaN; nonce contention; secret ou
licence indisponible; update/rollback interrompu.

Chaque test affirme l'état, les reservations, l'inventaire, la permission de
nouveau risque et la preuve persistée — pas seulement « pas de crash ».

## Gates de promotion

- Release : tests critiques, golden/parity, deterministic replay, aucun défaut
  risk/security ouvert, performance/backpressure acceptable.
- M3 : mêmes décisions/plans sur live data, aucun submit, reconciliation testée.
- M4 : unknown/recovery/accounting/kill switches validés; capital et `Q_validated`
  approuvés; rollback prêt.
- Scaling/M5 : slippage/fill/PnL calibration, tails/ES, OOD/drift, recovery,
  infra et operations stables; paliers seulement.
- Modèle : walk-forward/OOS, ablation, calibration, economic lift net de latence,
  risk/complexity acceptables et borne basse positive.
- Infra : même binaire/config/univers, mesure first-arrival/feed-age/jitter/CPU/
  recorder/clock; sélection sur NetPnL robuste.

## Capability Manifest

Pour chaque capability : module/version, strategy/markets/mode, size range,
required fidelity/model/config, maturity, evidence IDs, enabled environments,
restrictions, owner/approval/date. Le runtime fail closed si le manifest ne
couvre pas la demande.

## Validation scientifique

Splits temporels walk-forward, golden datasets couvrant régimes/incidents,
résultats négatifs conservés, aucune optimisation et évaluation sur le même
sample, report versionné avec dataset/config/code/model/capital/risk/fidelity.

## Sources

SRC-006 D6; SRC-005 risk/data; SRC-007/008 calibration.
