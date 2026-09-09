# Cross-Recorder Event Alignment Audit

Identity precedence is:

```text
authoritative event/block/order/trade identity
> deterministic semantic fingerprint
> explicitly bounded use-specific fallback
> UNMATCHED / AMBIGUOUS
```

Nearest timestamp alone is never sufficient to claim two observations are the same event. A fingerprint binds source/schema, market/channel, event type, canonicalized payload fields and relevant sequence/block context. Collisions, repeated identical payloads, missing context and incompatible schemas are rejected or labeled ambiguous.

Each paired observation stores recorder IDs, source identities, local receive monotonic/wall times, offset/uncertainty, fingerprint method/version and match status. Monotonic clocks measure local stages; synchronized wall clocks with combined uncertainty support cross-machine comparisons. A claimed lead smaller than uncertainty is `INCONCLUSIVE`.

Alignment cannot reorder either recorder's canonical stream, fuse Books, backfill gaps or make speculative data committed. Matched, unmatched, ambiguous, duplicate and invalid-clock populations are all reported.
