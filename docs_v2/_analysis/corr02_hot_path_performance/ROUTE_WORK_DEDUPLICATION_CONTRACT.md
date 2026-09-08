# Route Work Deduplication Contract

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

Route evaluation may be skipped as a duplicate only when the complete economic input identity is equal:

`(RouteId, RouteVersion, relevant ordered BookVersions, FeeVersion, MetadataVersion, Graph/index generation, FormulaVersion, execution/protection context, q, required model/feature/config versions)`.

The tuple expands when a consumer uses another versioned input. Equality must be exact and collision-safe; a hash alone cannot authorize skipping. Route membership duplicates inside one `pair_to_routes` generation are invalid and removed at generation build, not tolerated in runtime dedup.

## Non-duplicates

Distinct ordered events/states are not duplicates even if BBO values, a lossy fingerprint or final prices match. A transient opportunity can exist between them. Different `q`, fee, rule, model, route, book or scheduling version is different work.

## Transparent dedup

A transparent implementation produces the same canonical evaluations, decisions, reasons and `DecisionTrace` as evaluating every unique tuple in order. Counters may report avoided mechanical invocations, but cannot alter the canonical evidence population. Cross-event coalescing is outside this transparent contract.
