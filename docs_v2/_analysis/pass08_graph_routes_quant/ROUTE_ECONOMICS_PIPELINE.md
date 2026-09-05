# Route Economics Pipeline

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

```text
RouteDefinition + coherent current state + input q
  → NetConvert leg 1
  → validated actual output
  → NetConvert leg 2 [→ leg 3]
  → terminal output
  → direct comparator or cycle reference
  → route output / edge / gain
  → ConversionAlpha
  → Execution forecast interface
  → ExecutionAlpha
  → Edge(q) and QF-027 boundary
  → Participants / Simulator / Risk / PASS07 Sizing & Capital
```

## Stages and owners

| Stage | Output | Owner | Must not do |
|---|---|---|---|
| Structural route | ordered directed legs/dependencies/version | Route Engine | claim current profitability |
| State bind | coherent books/fees/metadata/formula versions | Data/Book/Route | mix future and stale legs silently |
| Exact legs | sequential QF-016 results | Opportunity/Quant | midpoint multiplication or linear depth |
| Direct | QF-017 output in B | Route economics | invent comparator |
| Indirect | QF-018 output in B | Route economics | reuse gross intermediate output |
| OWA | QF-019 relative, QF-020 absolute | OWA | compare different q/terminal units |
| Triangle | QF-021–023 in starting A | Triangle | call open 3-leg path closed |
| Conversion alpha | QF-024 structural conversion advantage | Route economics | include maker-fill forecast |
| Execution alpha | QF-025 execution-method advantage | Execution/Simulator interface | redefine route topology |
| Size curve | QF-026 and QF-027 | Route economics | equate with QF-076 |
| Forecast | full/partial/fail/recovery distribution | Participants/Simulator | authorize action |
| Eligibility/allocation | RiskDecision then `Q_validated`/sizing/capital | Risk/PASS07 | enlarge capacity from positive edge |

## Current-state coherence

Every result records RouteVersion, GraphVersion, each BookVersion, MetadataVersion, FeeVersion and FormulaVersion. The snapshot policy may tolerate different receive times only when freshness/skew constraints are explicit. Superseded worker output is discarded or revalidated under PASS06. Route freshness exposes required-leg/worst-leg evidence to Risk.

## Prefilter versus exact economics

BBO arithmetic is a cheap rejection stage. Survivors require exact L2, dynamic fees, quantization, minimum checks and sequential outputs. A favorable product of mid prices is never an executable opportunity.

## Size dependence

Route edge is `Edge(q)`: depth tiers, fees, precision and minimums create discontinuities. QF-027 is the largest economically profitable quantity under its threshold. QF-076 is the largest quantity passing **all** downstream gates and is owned by PASS07; therefore `Q_validated ≤` the independently applicable constraints and need not equal QF-027.
