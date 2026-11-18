# Opportunity Detection and Size-Dependent Economics

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Pipeline

`BookUpdate → canonical book publication → affected active RouteIds → BBO C1–C4 classification → exact QF-016 FastL1 or full-L2 fallback → fees/precision/minimums → route economics → Risk preliminary eligibility/safe candidate domain → supported PASS07 Sizing/Capital → Risk full authorization → Reservations/Execution`.

Participants and Simulator outputs enter only for a capability that declares and supports them;
they are not unconditional prerequisites of conservative route-economics mechanics. Preliminary
Risk eligibility does not authorize Submit and never replaces full Risk authorization or pre-send
revalidation.

The BBO stage separates C1 state invalidity, C2 proved conservative rejection, C3 exact FastL1 eligibility and C4 heuristic priority. Only C1/C2 may reject permanently; exact opportunity proof uses current valid books and sequential QF-016 conversions. Common false arbitrage causes are midpoint multiplication, wrong side, stale leg, wrong fee, precision/minimum error, unavailable depth and inconsistent snapshots.

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

Opportunity Engine owns deterministic current conversion outputs. Participants owns
survival/response/competition. Simulator owns execution outcome distributions and counterfactual
branches. Risk owns preliminary eligibility and full authorization. PASS07 owns total position
sizing, inventory/terminal effects and allocation inside the safe candidate domain. Reservations
own atomic resource claims. Execution owns actual orders/fills/recovery. No checkpoint is a second
Risk owner.

## Provenance

Each candidate records RouteId/Version, GraphVersion, BookVersions, Metadata/Fee/Formula/Model versions, q/unit, direct/indirect/cycle outputs, classification and freshness. Stale results are not sent onward as current opportunities.

## CORR-01 identities and boundaries

Each route evaluation receives a stable `RouteEvaluationId`. Cheap completion/pass, exact completion/validity and emitted `OpportunityId` are separate stage facts. An `OpportunityId` represents one immutable exact-valid observation, not a continuous duration or attempt. Offline/near-line analytics may group repeated observations into a versioned `OpportunityEpisodeId`; grouping never changes this pipeline or hot-path permission.
