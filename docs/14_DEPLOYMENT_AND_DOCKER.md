# 14 — Deployment and Docker

## Modèle commercial LOCKED

Installation isolée par client : un VPS, un compte/wallet/signer et un
process/container initial. Pas de service SaaS mutualisé dans le hot path, pas
d'accès opérateur permanent requis. Le client contrôle ses secrets et fonds.

## Image

Build reproductible/multi-stage, artefact minimal, versions et digest épinglés,
SBOM/signature/provenance, scan de vulnérabilités. Runtime non-root, filesystem
read-only autant que possible, capabilities supprimées, limites CPU/RAM/PIDs,
aucun privileged mode ni Docker socket. Volumes explicites pour state/data/logs.

## Configuration et secrets

Config non secrète versionnée et validée au démarrage. Secrets via fichiers
root-only/secret store/env contrôlée selon installation; jamais dans image,
repo, logs, diagnostic bundle ou ligne de commande. Séparer paper/live et
rotation/revocation documentées.

## Lifecycle

```text
install → preflight → sync → reconcile → ready
update: fetch signed digest → verify → backup state/config → stop new risk
       → drain/recover/reconcile → replace → health/readiness → resume
failure: remain risk-off → rollback previous digest → reconcile → resume
```

Un update ne remplace jamais une image mutable `latest`. La compatibilité
schema/config est vérifiée avant activation. Rollback conserve preuve, données
et state; il ne suppose pas que les ordres ont disparu.

## Licence

Contrôle hors hot path, fail behavior explicite. Une licence indisponible peut
empêcher une nouvelle exposition après grace policy validée; elle ne bloque
jamais cancel sûr, recovery, reconciliation, export ou shutdown sûr. Aucun secret
client n'est envoyé pour licencier.

## `botctl`

Commandes minimales : `install`, `preflight`, `start`, `stop --safe`, `status`,
`health`, `logs` redacted, `diagnose`, `update`, `rollback`, `reconcile`,
`risk-off`, `export-incident`, `version`. Idempotence, exit codes, confirmation
pour action sensible et audit local obligatoires.

## Health

Liveness = process répond; readiness = toutes les conditions pour nouveau
risque. Un process peut être live mais non ready/recovery-only. L'orchestrateur
ne doit pas créer une boucle de restart pendant recovery.

## Réseau

Egress limité aux endpoints nécessaires, ports entrants minimaux. Host vs bridge
reste `OPEN` soumis au benchmark et threat model. Aucune dépendance cloud
synchrone dans décision/exécution.

## Sources

SRC-006 D5; faits Docker/exchange courants à revalider lors de l'implémentation.
