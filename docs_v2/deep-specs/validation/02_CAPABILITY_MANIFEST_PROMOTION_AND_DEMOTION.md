# 02 — CapabilityManifest, Promotion and Demotion

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Source-backed entry

```text
ValidatedCapability {
  strategy
  market_scope
  size_range
  execution_mode
  model_versions
  validation_level
  valid_from
  last_review
  restrictions
}
```

The release manifest links entries to immutable validation evidence. Runtime intersects compiled, configured, licensed, channel, validated, ready and Risk-permitted scope. If the request is not a subset of one exact entry, new risk is refused with a reason; no nearest/broader match exists.

Promotion records old/new scope and maturity, EvidenceIds, dependency state, restrictions, reviewer/approver, validity/review trigger, fallback and rollback. A model/version/release does not inherit another artifact’s maturity silently.

Automatic demotion is permitted for locked safety failures. It may shrink size, restrict market/mode, fall back model, suspend strategy/release or block new risk. Clear alerts do not re-promote. Safe cancel, Recovery, reconciliation and read access remain available per Risk.
