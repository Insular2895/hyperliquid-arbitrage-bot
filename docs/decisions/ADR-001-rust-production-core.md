# ADR-001 — Rust production core

## Context

Le hot path exige types, travail borné, concurrence I/O et replay parity.
## Decision

Utiliser Rust pour le core production, replay et décisions économiques.
## Alternatives considered

Python live; Python+C++; C++ complet.
## Why selected

Une seule implémentation typée et performante réduit divergence et complexité.
## Consequences

Python sort du hot path; optimisation bas niveau seulement après profil.
## Status

PROPOSED FOR REVIEW — LOCKED candidate.
## Sources

SRC-001, SRC-002, SRC-004, SRC-006.
