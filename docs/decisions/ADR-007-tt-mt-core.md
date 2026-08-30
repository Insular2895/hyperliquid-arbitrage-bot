# ADR-007 — TT/MT/TTT/MTT core

## Context

Maker en jambe terminale laisse une exposition intermédiaire non bornée.
## Decision

Core : TT, MT, TTT, MTT. TM/MM support futur disabled.
## Alternatives considered

Taker-only; tous mixes maker/taker; maker terminal par défaut.
## Why selected

Mesure le bénéfice maker initial tout en limitant le leg risk terminal.
## Consequences

MT exige fill/queue/adverse/expiry calibrés avant activation.
## Status

PROPOSED FOR REVIEW — modes LOCKED, MT activation CALIBRATED.
## Sources

SRC-003, SRC-004 D1/D2.
