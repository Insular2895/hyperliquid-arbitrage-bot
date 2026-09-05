# OWA Comparator Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

An indirect A→X→B route is an OWA candidate only when a valid direct A→B conversion exists. The comparison asks whether the indirect route produces more **B** than the direct route for the same starting amount of **A**.

## Validity conditions

| Dimension | Required condition |
|---|---|
| Input | same asset A, same exact input amount `q`, same unit |
| Terminal | same asset B and terminal unit; no raw intermediate comparison |
| Direction | all direct and indirect legs resolve explicit directed conversions |
| Books | current, valid snapshots under an explicit coherent snapshot policy |
| Metadata | compatible market/precision/minimum versions |
| Fees | same point-in-time Fee Engine and correct per-leg fee treatment |
| Precision | same canonical quantization/rounding conventions; no hidden extra rounding |
| Output | QF-017 direct output vs QF-018 sequential indirect output |
| Edge | QF-019 relative and QF-020 absolute, both in comparator semantics |
| Replay | exact Graph/Route/Book/Metadata/Fee/Formula versions available at decision time T |

## Failure behavior

- Missing, disabled, stale or invalid direct market: reject the `OWA` classification.
- An otherwise valid A→X→B path may be offered to PASS07 as a Bridge candidate; it does not receive a synthetic direct price.
- A comparator becoming unavailable invalidates/deactivates the OWA candidate. Reclassification is explicit and versioned.
- Midpoint, oracle, external venue price or mark-to-market is not a replacement unless a later authoritative specification creates a distinct strategy and formula family.

The comparator proves conversion advantage only. Terminal viability, inventory, execution outcome, Risk and sizing remain independent gates.
