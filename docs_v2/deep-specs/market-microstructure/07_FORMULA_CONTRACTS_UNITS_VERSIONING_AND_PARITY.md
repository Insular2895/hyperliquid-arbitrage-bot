# Formula Contracts, Units, Versioning and Parity

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Authority

SRC-004 QF-001–QF-043 is the only formula authority for this layer. PASS08 defines inputs, outputs, consumers and runtime provenance. PASS11 audits exact expression rendering and formal units. No formula is copied into configuration or learned by Atlas.

## Unit contract

Every quantity is tagged conceptually as base units, quote units, price (quote/base), notional/value, dimensionless ratio, bps, time, volatility/variance or model score. Market/side/window must accompany contextual values. Conversions between units occur only through explicit formula/data contracts.

## Version contract

Feature and route results identify FormulaVersion, BookVersion, MetadataVersion and window/config version; fee-consuming results also identify FeeVersion. Learned consumers identify ModelVersion and Dataset/RunManifest. A material version mismatch invalidates cache/result and forces recomputation/revalidation.

## Golden tests

Formula-owned test vectors cover normal, boundary, invalid, rounding/minimum and direction/sign cases. QF-009/010 prove book-side asymmetry; QF-016 proves fee/precision treatment; QF-017–023 prove sequential/comparator/cycle units; QF-028–043 prove event/window semantics.

Rust production and Python reference execute identical vectors under the canonical fixed/exact numeric contract. Differences are failures, not tolerated floating-point noise unless PASS11/Data Contracts explicitly define a bounded comparison for a given feature.

## Point in time

Replay selects the formula version and inputs available at decision T. Later corrected formulas require an explicit alternate research run; they cannot rewrite historical DecisionTrace. See [Formula crosscheck](../../_analysis/pass08_graph_routes_quant/FORMULA_CROSSCHECK.md).
