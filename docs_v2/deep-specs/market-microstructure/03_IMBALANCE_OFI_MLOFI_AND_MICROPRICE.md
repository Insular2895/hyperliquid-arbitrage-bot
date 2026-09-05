# Imbalance, OFI, MLOFI and Microprice

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Canonical measurements

QF-028 Queue Imbalance uses current best-level prices/sizes; QF-029 aggregates defined levels/weights. QF-030 and QF-031 define event-level bid/ask OFI contributions, QF-032 OFI and QF-033 MLOFI. QF-034 defines Microprice and QF-035 its dislocation. Expressions and sign conventions remain SRC-004-owned.

## Event fidelity

True OFI requires consecutive ordered market events/book changes with known fidelity. A two-snapshot approximation is explicitly named `Snapshot OFI proxy`, records its interval/source quality and cannot claim event-level semantics. Gaps, reorder, reset or snapshot replacement reset/invalidate incremental flow state according to PASS06.

## Runtime state

Feature Engine owns bounded per-market accumulators and immutable FeatureSnapshot publication. Level counts, weights, windows and sampling conventions are configuration/model versions. No full-history scan occurs per opportunity.

## Epistemic boundary

Imbalance, OFI and Microprice are features—not instructions, participant identity or guaranteed fair value. PASS02 Participants owns predictive horizon, survival/response association, confidence/OOD and fallback. Risk consumes only supported, fresh versions.

## Validation

Golden sequences cover bid/ask price increases/decreases, size changes, unchanged states, reset/gap, sign conventions, symmetric books and empty/invalid sides. Batch/reference and incremental Rust outputs match Python exactly under the numeric contract.
