# Participation, Impact and Liquidity Resilience

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Distinct concepts

| QF | Meaning | Boundary |
|---|---|---|
| QF-040 Depth Participation | order relative to explicitly defined current depth | current book capacity, size-specific |
| QF-041 Volume Participation | order relative to observed market volume/window | historical activity, not current depth |
| QF-042 Mechanical Impact | direct price/VWAP effect of walking a chosen arrival book | deterministic mechanics for that state |
| QF-043 Liquidity Resilience | depth/liquidity recovery after shock over time | response measurement/model interface |

Depth and volume denominators, sides, bands/windows and units are mandatory. A percentage without those identifiers is invalid. Participation ratios do not create capacity.

Mechanical Impact is already embodied by the exact walk and must not be charged again as a generic linear penalty. It differs from Participant Response, replenishment and Cross-Market Response, which are future distributions and belong to PASS02/Simulator.

Liquidity Resilience keeps the canonical QF-043 measurement here; predictive curves, horizon support, confidence/OOD and calibration remain Participant-owned. Atlas can store empirical rolling resilience with versioned evidence.

Validation uses golden book walks, multiple q values, denominator-zero/insufficient-volume cases, shock/recovery episodes and Rust/Python parity. Square-root/linear impact research is not substituted when exact L2 mechanics exist.
