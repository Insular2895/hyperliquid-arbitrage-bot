# Opportunity Detection and Size-Dependent Economics

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Pipeline

`BookUpdate → canonical book publication → affected active RouteIds → BBO prefilter → exact L2 survivors → fees/precision/minimums → route economics → Participants/Simulator → Risk → PASS07 Sizing/Capital`.

The BBO stage is a cheap rejector only. Exact opportunity proof uses current valid books and sequential QF-016 conversions. Common false arbitrage causes are midpoint multiplication, wrong side, stale leg, wrong fee, precision/minimum error, unavailable depth and inconsistent snapshots.

## Outputs by family

- Direct: QF-017 in terminal B.
- Route2Leg: QF-018 with real first output feeding the second.
- OWA: QF-019/020 against a valid Direct output at same q.
- Triangle: QF-021–023 in start asset A.
- Structural advantage: QF-024 ConversionAlpha.
- Execution-method advantage: QF-025 ExecutionAlpha interface.

## Size curve

Every evaluation is bound to `q`. Deeper levels, precision, minimums and fee treatment cause nonlinear/discontinuous economics. QF-026 is Edge Curve; QF-027 is Maximum Profitable Size. The latter is not book capacity, account balance or PASS07 QF-076 all-gates Validated Capacity.

Multi-size evaluation must use the same state or explicitly attributable snapshots. Larger q cannot assume untouched depth, and concurrent opportunities share reservations under PASS07.

## Ownership

Opportunity Engine owns deterministic current conversion outputs. Participants owns survival/response/competition. Simulator owns execution outcome distributions and counterfactual branches. Risk removes unsafe actions. PASS07 owns total position sizing, inventory/terminal effects and allocation. Execution owns actual orders/fills/recovery.

## Provenance

Each candidate records RouteId/Version, GraphVersion, BookVersions, Metadata/Fee/Formula/Model versions, q/unit, direct/indirect/cycle outputs, classification and freshness. Stale results are not sent onward as current opportunities.
