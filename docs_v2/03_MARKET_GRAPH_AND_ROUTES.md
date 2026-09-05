# 03 — Market Graph and Routes

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

This document specifies how exchange metadata becomes a versioned directed conversion graph, how legal route families are precomputed, and how current books turn an affected route into a size-specific economic candidate. It also defines Global Watcher, HOT/WARM/COLD (HWC), Route Activation and Market Atlas boundaries.

## 2. Authority

SRC-004 is authoritative for QF-009–027 and execution economics; SRC-005 for data, route schemas, versioning and Risk boundaries; SRC-006 for validation closure. SRC-003 provides the later venue-aware OWA/Bridge closure, with SRC-001/002/007/008 supplying Atlas, HWC and implementation detail. Formula expressions are not redefined here. Current Hyperliquid rules remain externally revalidated facts.

Status discipline: directed conversions, venue-aware identity, fixed route families, comparator rule, precomputation, reverse dependency lookup, `NetConvert` and alpha separation are `LOCKED`. V1 is same-venue Hyperliquid spot. Cross-exchange/transfer routing is `FUTURE`. HWC thresholds, windows and Atlas models are `CALIBRATED/LEARNED`.

## 3. Structural Graph

The structural Market Graph answers **what conversions can exist** in the configured product scope. It is built from eligible exchange metadata, not current price profitability, inventory or learned scores. A market creates two separately directed conversion operations.

Structural knowledge is global. Adding/removing a market or changing material metadata rebuilds affected edges/routes and publishes a new GraphVersion. A book update changes economic state, not topology. A positive edge creates an opportunity, not a route.

## 4. Venue-aware domain model

A graph node is an asset location `(VenueId, AssetId)`. `MarketId` binds a venue market with explicit base/quote roles. This makes identical assets at different venues distinct locations while avoiding a V1 redesign later. Active V1 edges are Hyperliquid spot trade conversions only; withdrawals, deposits, transfer states and cross-venue synchronization remain disabled future capabilities.

`RouteId` identifies route family plus ordered, directed legs and endpoints. Reversing direction changes identity. `GraphVersion` identifies topology/metadata publication; `RouteVersion` identifies a route definition. See [domain model](./_analysis/pass08_graph_routes_quant/GRAPH_DOMAIN_MODEL.md).

## 5. Directed conversions

`BaseToQuote` sells base into **bids** and returns quote units (QF-009). `QuoteToBase` spends quote through **asks** and returns base units (QF-010). These are not price inverses: depth, spread, fees, minimums and rounding differ by direction and size. Conversion direction is stored economically; exchange buy/sell intent is derived from it.

Each edge knows its input/output assets, market, venue, conversion direction, book side, metadata/precision context and status through source-owned contracts. The exact serialized schema remains PASS06-owned. See [directed conversion contract](./_analysis/pass08_graph_routes_quant/DIRECTED_CONVERSION_CONTRACT.md).

## 6. Graph versioning

A metadata event is validated, reduced into a new immutable topology state and assigned GraphVersion. Affected edges, routes and reverse indexes are republished consistently; old versions remain addressable for Replay. New markets enter the structural graph but do not automatically become HOT, capital destinations or large-capacity routes. Removed/disabled markets make dependent current routes non-tradable while historical definitions remain recorded.

MetadataVersion is distinct from GraphVersion. FeeVersion may invalidate economic caches without changing topology. DecisionTrace/RunManifest record the versions actually consumed.

## 7. Route types

The V1 hot path uses fixed source-backed structures:

| Structure | Meaning |
|---|---|
| `DirectRoute` | one A→B directed conversion |
| `Route2Leg` | ordered A→X→B conversion possibility |
| OWA | Route2Leg plus a valid DirectRoute comparator A→B |
| `Cycle3Leg` / Triangle | ordered A→X→B→A closed cycle |
| Bridge | intentional capital relocation A→…→B for future utility |
| Recovery path | bounded response to already-unwanted exposure, Execution-owned |

Leg count never determines economic class. See [route matrix](./_analysis/pass08_graph_routes_quant/ROUTE_TYPE_MATRIX.md).

## 8. Direct routes

A DirectRoute is a structural one-leg definition. For current input `q_A`, QF-017 obtains output `D(q_A)` by one QF-016 conversion. In OWA it is the executable comparator; elsewhere it can be an ordinary conversion/exit. It is not presumed profitable and inherits current availability, book, fee and precision checks.

## 9. Route2Leg

A Route2Leg stores ordered A→X and X→B legs. QF-018 feeds the first leg's valid economic output into the second. It is not allowed to feed the original amount, gross output or midpoint estimate. If the first output is below the second market's minimum or cannot be validly quantized, the route is invalid at that `q` and residual exposure remains explicit.

The same structure can support TT or MT. Execution mode alters forecasted outcomes and ExecutionAlpha; it does not mutate the route definition.

## 10. OWA

One-Way Arbitrage compares Direct A→B with Indirect A→X→B. Both begin with the same asset and amount and end in B under coherent versions, fees and precision. QF-019 reports relative edge and QF-020 absolute gain. The result is conversion advantage, not permission to hold B, final EV or accounting sleight-of-hand.

OWA classification is explicit in the candidate/trace. It is never inferred from two legs.

## 11. Direct comparator contract

The comparator must use the same `q`, A input, B terminal unit, formula/fee/precision conventions and explicit coherent book/metadata state. Midpoint, oracle, mark or a synthetic inverse cannot replace an unavailable direct market. If the comparator is missing, disabled, stale or invalid, OWA classification fails. Replay uses the comparator available at time T. See [OWA contract](./_analysis/pass08_graph_routes_quant/OWA_COMPARATOR_CONTRACT.md).

## 12. Triangle

A Triangle is an exact `Cycle3Leg` A→X→B→A. QF-021 produces the final amount in A; QF-022 measures return and QF-023 PnL in A. Each leg consumes the prior leg's valid output. An open three-leg path is not a Triangle. TTT and MTT are execution modes defined by Execution, not separate topology.

## 13. Bridge classification boundary

A structurally valid A→X→B without an executable direct A→B comparator may be a Bridge/Capital Relocation candidate. Bridge asks whether paying the conversion/exit/risk costs to move capital creates greater future utility than STAY; PASS07 owns that decision, terminal viability, QF-068/070/072 and accounting. Multi-leg does not imply arbitrage. Recovery begins from existing unwanted exposure and remains constitutionally distinct.

## 14. Route precomputation

Direct, legal two-leg and closed three-leg definitions plus comparator/dependency relationships are generated on metadata/topology change, not on every tick. Static adjacency and precision transforms may be prepared when source-backed. V1 forbids unbounded Dijkstra/general graph search in the opportunity hot path. A general structural graph remains useful for offline Bridge research and future route families.

Route identity is based on ordered directed structure, not transient edge or score. See [generation matrix](./_analysis/pass08_graph_routes_quant/ROUTE_GENERATION_AND_INVALIDATION_MATRIX.md).

## 15. `pair_to_routes`

The reverse dependency index maps canonical `MarketId` to every dependent `RouteId`, including an OWA's direct comparator. A market update looks up affected routes only. The Route Engine is the logical writer and publishes an immutable, deterministic generation; workers read it without rebuilding topology. See [`pair_to_routes` contract](./_analysis/pass08_graph_routes_quant/PAIR_TO_ROUTES_CONTRACT.md).

## 16. Route invalidation

Market add/remove/status, asset/base/quote, precision, lot/tick/minimum or other material metadata changes invalidate affected definitions. A fee change forces current economics/caches to re-evaluate. Invalidation removes affected active routes atomically, rebuilds their dependencies and increments relevant versions. No restart is architecturally required, but exact exchange change feeds require revalidation.

## 17. Opportunity detection pipeline

```text
Book update
→ publish canonical BookState
→ pair_to_routes lookup
→ active affected routes only
→ cheap BBO rejection filter
→ exact L2 NetConvert(q) for survivors
→ fees, precision, minimums and version checks
→ direct / indirect / cycle economics
→ Participants and Simulator forecasts
→ Risk eligibility
→ PASS07 sizing/capital allocation
→ immutable candidate/decision trace
```

BBO rejects obvious losers cheaply; it never proves executable edge. Current BookState is truth, not a stale Atlas aggregate. All hot-path inputs are bounded and in memory; no blocking REST/service call is allowed.

## 18. NetConvert

QF-016 is the one canonical primitive for an economic directed conversion. It combines correct-side exact L2 walk, QF-007/008 validity, QF-014/015 fees, rounding, minimums and protected limits. Slippage already embodied in the walk is not subtracted twice. Same immutable inputs and versions must yield the same result across production Rust and Python golden validation. See [NetConvert contract](./_analysis/pass08_graph_routes_quant/NETCONVERT_CONTRACT.md).

## 19. Size-dependent economics

Edge is a function of input `q`. Larger size reaches different levels and can cross rounding/minimum discontinuities. QF-026 represents Edge Curve; QF-027 finds the maximum profitable size under its economic threshold. It is distinct from PASS07 QF-076 `Q_validated`, which additionally requires Risk, inventory, model, execution and capacity gates. Larger account capital does not manufacture book depth.

## 20. ConversionAlpha

QF-024 measures the structural conversion advantage of the indirect taker baseline over the direct taker comparator under matched inputs. It belongs to route economics. It does not include predicted maker fills, recovery outcomes or capital utility.

## 21. ExecutionAlpha interface

QF-025 measures execution-method improvement relative to the defined execution baseline, such as MT versus TT on the same route. Execution/Participants/Simulator own fill, latency, adverse-selection and recovery distributions. `ConversionAlpha != ExecutionAlpha`; total EV can be unfavorable even when either point estimate is positive.

## 22. Route activation

Structural validity, activation and opportunity are separate states. Route Activation selects which valid routes receive expensive evaluation based only on source-supported HWC, capital reachability, recent evidence and Risk/strategy/model capability. It is reversible and versioned. A deactivated route remains structurally known.

## 23. HOT/WARM/COLD

HOT receives full supported books/features/routes/forecasts because it is capital-reachable or currently productive. WARM receives deeper observation to confirm adjacency, anomaly or emerging utility. COLD retains cheap global awareness and Recorder coverage. COLD does not mean unsafe or forgotten; HOT does not mean safe or authorized. Promotion/demotion uses governed evidence and hysteresis without hardcoded source examples. See [HWC matrix](./_analysis/pass08_graph_routes_quant/HOT_WARM_COLD_MATRIX.md).

## 24. Global Watcher

Global Watcher monitors the configured structural universe cheaply: metadata/topology, BBO/freshness and bounded signals needed to detect regime/liquidity/opportunity change. It can propose COLD→WARM or route re-evaluation, never a trade or formula change. Thus the system knows broadly while spending expensive compute selectively.

Canonical operating shorthand: **KNOW EVERYTHING / EXPENSIVE COMPUTATION FOLLOWS CAPITAL**. The first clause means global structural/cheap observational awareness; the second is a bounded compute-allocation policy, never permission to ignore other markets or follow capital into unsafe actions.

## 25. Market Atlas

Market Atlas is a rolling, versioned economic map—not the graph and not exchange truth. It aggregates evidence at market, route, asset, capital-location and regime horizons: spread/depth/liquidity/volatility/jumps, replenishment/resilience/competition, opportunity episodes/frequency/edge distributions/survival/capture, route counts/capacity, exit liquidity and capital utility.

Structural and learned fields remain separate. FAST/RECENT/MEDIUM/LONG window identities exist; exact windows and score weights are calibrated. Evidence may come from Recorder, Replay, Shadow, Micro-live and Live but predicted, rejected and actual outcomes remain labelled. Sparse evidence lowers support/confidence. AtlasVersion binds model, dataset, formula and source versions. No universal score overrides current books or Risk. See [field catalog](./_analysis/pass08_graph_routes_quant/MARKET_ATLAS_FIELD_CATALOG.md).

## 26. Capital interfaces

PASS07 supplies actual inventory, capital reachability, Terminal Viability, exit/stranded cost, Bridge decisions, reservations and `Q_validated`. Atlas supplies point-in-time opportunity/exit context; Graph supplies structural paths. Capital can influence HWC/activation but cannot add/remove topology. `structural route count`, `active route count`, `capital-reachable route count` and `validated opportunity count` are never conflated.

## 27. Risk / Execution / Simulator interfaces

Risk consumes route/leg freshness, current versions, liquidity/volatility/impact and downstream forecasts, then returns immutable permission/limits; positive edge or HOT cannot bypass it. Execution owns actual TT/MT/TTT/MTT state, orders, partial fills and Recovery. Simulator owns distributional execution/counterfactual outcomes. Participants owns survival, cross-market response, replenishment and competition. Route economics remains deterministic current-book conversion calculation.

## 28. Point-in-time Replay

Historical event T uses metadata, graph universe, route definitions, Atlas evidence, books, fees, formulas and models available by T. Today's listings, learned windows or fee state cannot leak backward. Worker results carry all consumed versions; stale results are discarded or revalidated. Same manifest, event order and versions reproduce route sets and economics under PASS06 determinism.

## 29. Future venue support

Venue-aware nodes/IDs are locked now; cross-exchange trading, transfer/rebalance edges, venue inventories, settlement, outages and synchronization are `FUTURE`. They require distinct strategy, data, operational, security, Risk and accounting contracts. V1 does not activate them merely because the domain model can represent them.

## 30. Validation

Required properties include bid/ask direction, round-trip spread cost, depth bounds, sequential outputs, comparator rejection, cycle closure, affected-route-only lookup, invalidation, deterministic topology/economics, size sensitivity, version provenance and point-in-time Replay. Formula golden tests and Rust/Python parity cover QF-001–043. Replay, Shadow and Micro-live promotion provide increasing evidence; no numeric threshold is invented here. See [validation map](./_analysis/pass08_graph_routes_quant/VALIDATION_MAP.md).

## 31. Deep-spec links

- [Market Graph deep specs](./deep-specs/market-graph/README.md)
- [Market Microstructure master](./05_MARKET_MICROSTRUCTURE.md)
- [Quant feature catalog](./_analysis/pass08_graph_routes_quant/QUANT_FEATURE_CATALOG.md)
- [Route economics pipeline](./_analysis/pass08_graph_routes_quant/ROUTE_ECONOMICS_PIPELINE.md)
- [Formula crosscheck](./_analysis/pass08_graph_routes_quant/FORMULA_CROSSCHECK.md)
- [Inventory and Capital](./08_INVENTORY_AND_CAPITAL.md)
- [Risk Constitution](./09_RISK_CONSTITUTION.md)
- [Execution State Machine](./10_EXECUTION_STATE_MACHINE.md)
- [Data Contracts](./11_DATA_CONTRACTS.md)

## Sources

Original sources SRC-001–SRC-008 as inventoried in [`_analysis/SOURCE_INVENTORY.md`](./_analysis/SOURCE_INVENTORY.md). No external web research was performed in PASS08.
