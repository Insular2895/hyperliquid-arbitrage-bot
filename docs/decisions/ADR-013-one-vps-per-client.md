# ADR-013 — One VPS per client

## Context

Le modèle commercial exige isolation comptes, secrets, données et risque.
## Decision

Une installation/VPS dédiée par client initialement.
## Alternatives considered

SaaS multi-tenant; VPS partagé; client local desktop production.
## Why selected

Réduit blast radius et conserve contrôle client/hot-path direct.
## Consequences

Fleet/update/support doivent fonctionner sans accès permanent ni shared signer.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-006 D5.
