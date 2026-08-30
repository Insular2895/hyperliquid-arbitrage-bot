# 15 — Security

## Menaces prioritaires

Vol de clé/signer, confusion environnement paper/live, supply-chain image,
commande/admin compromise, logs ou bundles exfiltrants, replay/duplicate orders,
nonce collision, dépendance SaaS, container escape, update malveillante, data
tampering et denial of service conduisant à un état stale/unknown.

## Contrôles

- Principe du moindre privilège; clé dédiée sans retrait si la mécanique
  Hyperliquid le permet et après revalidation officielle.
- Un compte/signer/NonceManager par process; CLOIDs/idempotence/reconciliation.
- Secrets hors code/image/logs; permissions strictes, rotation et révocation.
- Images signées, digest pinning, SBOM, CI hermétique et scans.
- Non-root, read-only, no privileged/socket, capabilities/seccomp minimaux.
- TLS/endpoint allowlist, connexions persistantes vérifiées; aucun webhook tiers
  nécessaire au hot path.
- Config/model/manifest signés ou checksummés, activation auditée et rollback.
- Diagnostics redacted par défaut; séparation des données clients.

## Fail-safe

L'incertitude de sécurité ou d'état désactive le nouveau risque. Les actions
réductrices restent disponibles sous un chemin minimal. Un kill switch de
trading n'efface pas state/logs et n'interrompt pas aveuglément une recovery.

## Dépendances externes

Toute règle de permission API, signature, nonce, endpoint, image base et version
est revalidée. Une source ancienne ne justifie pas un contrôle. Les versions
critiques sont pinées et leur provenance conservée.

## Journal et données

Audit append-only de login/admin/update/config/risk/decision/order/recovery.
Minimisation des PII; pseudonymes participants ne sont pas des identités.
Chiffrement au repos/en transit selon threat model; backups testés; rétention et
effacement client documentés.

## Tests

Secret scanning, image/SBOM verification, permissions, dependency/vulnerability
scan, tampered update, expired/revoked secret, endpoint spoof, nonce contention,
log redaction, backup restore et incident tabletop. Aucune assertion « secure »
sans preuve de test.

## Sources

SRC-006 D5, SRC-004 nonce/signer, SRC-005 invariants.
