# CORR-03 — Dataset Schema Requirements

DOCUMENTATION STATUS: REQUIRED RELATIONSHIPS — EXISTING SCHEMA GOVERNANCE APPLIES

This specification does not silently mutate frozen schemas. Missing fields require a version increment, compatibility/migration policy and owner review.

## Attempt relation

`RunId`, `ExecutionId`, `OpportunityId`, optional `EpisodeId`, `ExecutionPlanCandidateId`, `RouteId`/family, strategy/mode, planned/attempted q, q/depth context, decision snapshot/forecast references, `RiskDecisionId`, book/graph/metadata/fee/Formula/Config/Feature/Model/infra versions, attempt time, path flags, terminal outcome, `Y_full_route`, resolution/reconciliation/evidence validity, economic reference and label revision.

## Leg relation

Execution/Leg/Intent/CLOID/OID identities; index/market/side; requested q; attempted state; unique fills; any/full fill; filled q/ratio/VWAP/fee; first/last fill timing; terminal order state; UNKNOWN/cancel flags; downstream actual-q linkage.

## Recovery relation

Origin/Recovery IDs, trigger, actual exposure/books, candidate/selected plan, Risk/reservation/order/fill linkage, cost/loss, attempts/time, final exposure/state/reconciliation.

## Provenance and missingness

`RunMode`, `SimulationMode`, fidelity and seed prevent Replay/counterfactual/Shadow outcomes from becoming actual labels. `missing`, `not_applicable`, `unresolved`, `invalid` and `OOD` are distinct. Dataset manifests include cutoff, extraction code/schema, source coverage, dedupe/conflict counts, train/validation intervals and hashes.
