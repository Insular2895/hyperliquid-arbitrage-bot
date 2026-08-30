# Extraction — Deployment and security

## Source d'autorité

- SRC-006, Dossier 5/6, lignes 1–3594 environ.
- Statut documentaire : final / normatif.

## Produit et topologie LOCKED

- Ce n'est pas un SaaS central : environ 30–50 installations clientes envisagées.
  Chaque client garde compte, capital, signer, VPS, données et risque.
- Topologie initiale : un VPS Tokyo recommandé, Docker Engine/Compose, une image,
  un processus de trading et un signer. Modules logiques internes, pas de
  microservices/Kafka/Redis/Postgres/Kubernetes sans preuve.
- Le hot path reste `Client VPS ↔ Hyperliquid`; registry, licence, dashboard et
  API commerciale ne sont jamais des dépendances d'exécution.
- Container remplaçable; config/journal/state/models/history persistants hors
  container. Secrets externes et client-side.

## Packaging et supply chain

- OCI `linux/amd64` d'abord; autres architectures après validation complète.
- Build multi-stage reproductible; runtime minimal stable; CPU baseline,
  LTO/PGO/native, libc et image de base décidés par compatibilité/benchmark.
- Version, git commit, digest OCI et schema versions; jamais `latest`; pin digest,
  signature, SBOM, scans dépendances/container; credential registry read-only.

## Sécurité runtime

- non-root, root FS read-only si pratique, chemins writable minimaux,
  `cap_drop: ALL`, jamais privileged/Docker socket/root mount/host PID.
- Clock gérée par host/chrony, sans capability time.
- Secrets par fichier read-only strict, jamais config/env/log/serialization;
  zeroize si raisonnable; support bundle redacted et local par défaut.
- Firewall, SSH keys, password/root login désactivés selon baseline; admin et
  metrics local-only, aucune backdoor ou API publique par défaut.

## État, santé et opérations

- Volumes state/journal/recorder/models/logs, rétention et rotation; événements
  critiques prioritaires en disk pressure.
- Liveness, readiness et trading health sont distincts. `RECOVERY_ONLY` doit
  rester vivant.
- Tout démarrage/redémarrage/migration suit `BOOTING → SYNCING → RECONCILING →
  READY`; un restart système n'autorise pas automatiquement le trading.
- Un writer actif par compte/signer; pas de blue/green dual-active ni overlap de
  migration. Un hot standby futur exige ownership et prévention split-brain.

## Licence, update et rollback

- Entitlement signé vérifié localement, avec grace appropriée; aucune validation
  par trade. Licence expirée/révoquée peut fermer `NEW_RISK`, jamais cancel,
  recovery ou reconciliation.
- Update : download, digest/signature/compatibility, stop new risk, résoudre,
  checkpoint, stop ancien, start nouveau, migrate, reconcile, health, ready.
- Rollback au digest précédent, puis reconciliation. Jamais restaurer un vieux
  checkpoint comme vérité exchange. Migrations destructives explicitement
  sauvegardées/testées.
- Releases : unit/integration/golden replay/benchmark/shadow/micro-live,
  candidate, canary, stable; aucun pull/restart silencieux.

## `botctl`

Contrat conceptuel : `status`, `health`, `benchmark`, `config validate`, `start`,
`stop`, `reconcile`, `update check`, `update`, `rollback`, `support-bundle`,
`emergency-stop`. L'installation/configuration n'active jamais Live directement.

## CALIBRATED / OPEN

Profil CPU/RAM/disk, VPS fournisseur, bridge vs host networking, Docker overhead,
resource/cpuset/swap, persistence embedded éventuelle, telemetry opt-in,
licensing provider, rétention et politique backup/standby. Tous sont soumis à
benchmarks et/ou choix commercial; aucune valeur de profil n'est finalisée.

## Faits externes à revalider

`EXTERNAL_RULE_REQUIRES_REVALIDATION` : Ubuntu/Docker versions supportées,
capabilities/OCI/registry, Hyperliquid endpoints et permissions API wallet,
compatibilité CPU des fournisseurs, règles de sécurité et vulnérabilités au jour
du build.
