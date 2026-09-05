# Returns, Volatility, Jumps and Regimes

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Formula references

QF-036 Log Return, QF-037 Realized Variance, QF-038 Realized Volatility and QF-039 Robust Jump Score are locked in SRC-004. Formula expressions are not duplicated here.

## Inputs and clocks

Every series states price source, MarketId, sampling/event clock, interval/window, missing-data behavior and versions. Exchange time and receive time are not interchangeable; Replay uses the same explicit clock policy. Nonpositive/invalid prices, gaps and insufficient windows produce invalid/low-support output rather than fabricated continuity.

## Incremental computation

Rolling returns and variance/volatility state update incrementally with deterministic eviction. The online result must match an offline reference on identical ordered data. Regime records can aggregate multiple horizons (FAST/RECENT/MEDIUM/LONG), but exact windows/scaling are calibrated.

## Jump semantics

Robust Jump Score detects abnormal movement relative to its robust scale. The score is evidence, not a universal event label; trigger thresholds and HWC/Risk reactions are calibrated and versioned. Sparse regimes expose support/confidence.

## Interfaces

Atlas stores point-in-time horizon aggregates. HWC may use persistent changes for promotion/demotion. Risk gates current volatility/jump exposure. Participants/Simulator may condition predictions/scenarios on regime, but cannot silently redefine the measurements.
