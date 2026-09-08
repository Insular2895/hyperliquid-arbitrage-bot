# Dense Runtime ID Contract

DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW

Canonical `MarketId`, `RouteId`, `AssetId` and other stable IDs remain the only persistent, external, cross-run and human-resolvable identities. A dense runtime index is a compact location inside one immutable published generation.

## Invariants

- Mapping is deterministic for the same canonical topology and ordering rules.
- `CanonicalId ↔ RuntimeIndex` round-trip is total for active generation entries.
- Every index carries or is interpreted only with its `GraphVersion`/index generation.
- An index is never persisted alone, emitted as sole telemetry identity, accepted from an untrusted boundary or reused after generation retirement.
- Width is checked at generation build; overflow fails publication rather than truncating.
- Replay rebuilds the mapping derivable at event time or resolves canonical IDs stored with evidence.
- Serialization and `DecisionTrace` use canonical deterministic identity, not memory address or runtime insertion timing.

Index width, slot reuse, generation reclamation and physical tables remain implementation choices requiring property, Replay, memory and benchmark evidence.
