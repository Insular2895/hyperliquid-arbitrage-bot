# ADR-014 — One container/process initially

## Context

Microservices ajoutent réseau, coordination et split-brain sans preuve.
## Decision

Un process/container avec modules logiques internes et un signer.
## Alternatives considered

Microservices, Kafka/Redis, dual-active, Kubernetes.
## Why selected

Ownership simple et latence/operations réduites.
## Consequences

Scale-up d'abord; multi-process futur exige ownership/ADR/validation.
## Status

PROPOSED FOR REVIEW — LOCKED initial topology.
## Sources

SRC-006 D5.
