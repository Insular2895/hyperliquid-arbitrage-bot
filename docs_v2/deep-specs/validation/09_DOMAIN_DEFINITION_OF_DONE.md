# 09 — Domain Definition of Done

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Each domain DoD combines:

1. complete M0 contract and owners;
2. required local invariants/golden/property/contract evidence;
3. deterministic Replay and no-lookahead where behavior is time/state dependent;
4. Shadow and Micro-live where live decision/effect claims exist;
5. fault, performance, recovery and operational evidence;
6. current dependency maturity and zero unresolved critical deviation;
7. reproducible EvidenceIds and explicit acceptance.

Domain specifics are frozen in [DOMAIN_DEFINITION_OF_DONE_MATRIX.md](../../_analysis/pass10_validation_operations/DOMAIN_DEFINITION_OF_DONE_MATRIX.md). Not applicable stages require a written causal argument; they cannot be omitted for convenience.

DoD is scoped. Graph correctness does not validate execution; execution mechanics do not validate economic model quality; a validated release does not validate all strategies/sizes; a validated model does not validate new data or infrastructure. Integration DoD proves the intersections.
