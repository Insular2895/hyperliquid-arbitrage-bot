# Legacy Comparison

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Comparison was performed only after V2 reconstruction. Files under `docs/**` remain unmodified and non-authoritative.

| Legacy area | Classification | V2 disposition |
|---|---|---|
| `docs/03_MARKET_GRAPH_AND_ROUTES.md` basic directed graph, OWA/Triangle/Bridge | `RECOVERED` but `OVER_COMPRESSED` | expanded venue-aware model, versions, classification and contracts |
| same file precompute/reverse lookup | `RECOVERED` but `OVER_COMPRESSED` | deterministic generation/invalidation and stale-worker semantics added |
| same file HWC/Watcher | `RECOVERED` but `OVER_COMPRESSED` | tier capability matrix, hysteresis, Recorder/exploration boundaries added |
| Market Atlas schema/evidence/confidence | `MISSING` materially | field catalog, dependencies, horizons, versions and no-lookahead added |
| GraphVersion/RouteVersion/AtlasVersion point-in-time | `MISSING` materially | dedicated deep spec and Replay contracts added |
| `docs/04_FORMULA_BOOK.md` QF-001–043 summary | `LEGACY_UNTRACED` for expression authority | SRC-004 Formula Index remains authority; routed to PASS11 |
| `docs/05_MARKET_MICROSTRUCTURE.md` feature families | `OVER_COMPRESSED` | all QF-001–043 semantics, units, incremental/provenance/parity added |
| `docs/06_MARKET_PARTICIPANTS.md` predictions | `RECOVERED` boundary | PASS02 remains predictive owner; no duplication |
| `docs/08_INVENTORY_AND_CAPITAL.md` OWA/Bridge/capacity | `RECOVERED` boundary | PASS07 remains capital owner; graph interface completed |
| `docs/09_RISK_CONSTITUTION.md` versions/comparator | `RECOVERED` boundary | PASS05 remains eligibility owner |
| `docs/16_VALIDATION_MATRIX.md` high-level validation | `OVER_COMPRESSED` | direction, comparator, invalidation, point-in-time and property cases expanded |
| `docs/specs/GlobalGraph.md`, `RouteEngine.md` | `RECOVERED` concepts | consolidated into master/deep specs with source authority |
| `docs/specs/NetConvert.md`, `QuantEngine.md`, `OFIEngine.md` | `RECOVERED`/`LEGACY_UNTRACED` details | semantic contracts retained; equations route to PASS11 |
| `docs/specs/MarketAtlas.md` | `OVER_COMPRESSED` | evidence classes, support, versions and feedback-loop controls added |
| static liquidity whitelist | `SUPERSEDED`/`REFINED` | global awareness plus dynamic HWC/Atlas/Risk filtering |
| general graph search per update | `CONTRADICTED` | forbidden from V1 hot path; fixed route precomputation |
| fixed fee, midpoint edge, linear slippage | `CONTRADICTED` | dynamic fees and exact L2 NetConvert(q) |
| cross-exchange active design | `ROUTED_TO_PASS12/13` | venue-aware representation only; execution disabled V1 |
| exact Formula Book expression/unit verification | `ROUTED_TO_PASS11` | flags retained in Formula Crosscheck |

Legacy omissions recovered: directed identity/units, valid comparator failure behavior, semantic class independent of leg count, route/index invalidation, HWC capabilities, broad Watcher/Recorder, Atlas support/provenance, size curve, state coherence, stale-result handling, point-in-time topology/Atlas and full QF catalog.

Legacy changes: **0**. V2 never inherits a legacy claim solely because it was concise or implementation-shaped.
