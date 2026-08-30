# 13 — Infrastructure

## Objectif

Maximiser le NetPnL sûr et reproductible, pas la performance brute ni le prestige
du serveur. L'infrastructure n'est promue que si son gain causal et sa borne
basse couvrent son coût.

## Départ

Un VPS/client, CPU, NVMe local, connexions persistantes, feed public, container
unique. Un node ou feed alternatif est compatible par `FeedAdapter` mais non
requis. Le meilleur emplacement/fournisseur reste `OPEN` jusqu'au benchmark;
Tokyo est une hypothèse source à revalider, pas une constante.

## Chemin de latence

QF-084 décompose feed, decode, book, route, simulation, risk, decision, sign,
send et exchange. Mesurer distributions P50/P95/P99/P99.9, jitter, tails,
reconnects et âge des books. Un compute rapide sur un feed stale n'a aucune
valeur.

## InfrastructureBenchmark

Même période/opportunity universe/config/capital/fidelity autant que possible;
horloges saines; manifest machine/kernel/runtime/network/container/feed; warmup;
durée couvrant régimes; raw samples et confidence intervals. Mesurer aussi CPU
steal/scheduler, memory, disk/recorder, packet loss, DNS/TLS/reconnect, send→ack
et send→fill. `hl-infra-benchmark` ne trade pas.

## ROI

Utiliser QF-085..093. Comparaison candidate/current avec stratégie identique,
attribution du delta, coût complet et `LCB_α(ΔGrossPnL)>SF·ΔCost`. `SF` et horizon
sont calibrés. Downscale si NetPnL robuste est supérieur/égal sur moins cher.

## Optimisations

Préallocations, data locality, minimum copies/locks, CPU pinning, host network,
lock-free, kernel tuning et node ne sont activés qu'après profil/benchmark et
revue de risque. Aucun budget µs illustratif n'est un SLO verrouillé.

## Résilience

Service manager restart, health/readiness séparés, NTP/clock monitoring, disk
watermarks, local buffering, backups manifests/configs, incident windows et
rollback. Une panne archive ne stoppe pas nécessairement trading; perte P0,
book/account uncertainty ou clock failure le fait.

## Revalidation externe

Région recommandée, capacités node/feed, rate limits, versions, specs/prix VPS
et comportements réseau : `EXTERNAL_RULE_REQUIRES_REVALIDATION`.

## Sources

SRC-008 infrastructure; SRC-006 deployment; QF-084..093.
