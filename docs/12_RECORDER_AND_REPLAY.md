# 12 — Recorder and Replay

## Recorder

Le feed fan-out vers BookEngine et une queue bornée non bloquante. Le recorder
écrit localement des chunks append-only; il ne bloque jamais la décision. La
perte/backpressure n'est pas cachée : event/metric/health gate selon priorité.

Priorités en pression : P0 account/orders/fills/inventory/config; P1 fenêtres
autour executions/incidents; P2 opportunities/features; P3 RAW marché général.
P0 n'est jamais sacrifié volontairement.

## Couches

- RAW original, petits chunks indépendants compressés et checksummés.
- NORMALIZED columnar/Parquet pour research.
- DERIVED versionné : features/routes/opportunities/atlas/models.
- EXECUTIONS/LATENCY/INCIDENTS/GOLDEN permanents selon politique.
- CHECKPOINTS accélèrent le replay mais ne remplacent pas les événements.

Formats ZSTD/Parquet et object storage sont des choix architecturaux; taille de
chunk, horizons et rétention sont `CALIBRATED` après mesure. Écriture cloud
directe depuis hot path interdite. Upload après close/checksum/verify; suppression
locale seulement après preuve d'archive et politique.

## Replay

`ReplayFeed` émet le même `NormalizedEvent` que live dans l'ordre recorder. Modes
exact timing, accéléré et contrefactuel utilisent le même core. Le Clock simulé
avance de façon déterministe; RNG/latence/config/model/fidelity viennent du
RunManifest.

## Reconstructibilité

Pour un instant : checkpoint antérieur vérifié + events jusqu'au cutoff. Books,
metadata, fees, account, config et model historiques sont nécessaires. Un gap ou
schema inconnu diminue la data fidelity ou invalide le run; aucune prétention de
replay exact.

## Rétention

R&D collecte largement l'univers pertinent, indépendamment de HOT/WARM/COLD.
Prod garde RAW récent comme buffer, archive/sélectionne les fenêtres utiles et
conserve durablement executions, opportunities, latencies, inventory, incidents,
configs/models et golden datasets. Valeurs de jours/Go dans les sources sont des
exemples, pas des locks.

## Tests

Byte/payload integrity, chunk crash recovery, checksum/event count, gap
detection, queue overload, disk full, cloud outage, determinism same manifest,
live/replay parity, no-lookahead, checkpoint equivalence et parser migration.

## Sources

SRC-003, SRC-005 D4, SRC-001/002 recorder history.
