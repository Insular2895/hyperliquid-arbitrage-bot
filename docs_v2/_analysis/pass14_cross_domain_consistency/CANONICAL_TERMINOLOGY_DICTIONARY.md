# Canonical Terminology Dictionary

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Canonical term | Exact meaning | Permitted prose alias | Forbidden conflation | Owner |
|---|---|---|---|---|
| `AssetId` | Asset identity independent of venue | asset | `(VenueId, AssetId)` location | Data/Metadata |
| asset location | `VenueId + AssetId` node | venue-aware asset | bare asset as cross-venue node | Graph |
| `MarketId` | One venue market with explicit base/quote roles | market | unordered pair | Metadata |
| directed conversion | Economic input→output operation using bids or asks | edge | exchange side, inverse price or undirected market | Formula/Graph |
| `RouteDefinition` | Ordered directed legs and dependencies | route | current opportunity or execution | Graph/Route |
| OWA | A→X→B compared with a valid direct A→B at matched input/terminal unit | one-way arbitrage | any two-leg path | Route |
| Triangle | Closed A→X→B→A `Cycle3Leg` | three-leg cycle | open three-leg path | Route |
| Bridge / Capital Relocation | Intentional move to a future-useful capital state versus STAY | Bridge | OWA, Rebalance or Recovery | Inventory/Capital |
| Opportunity | Current size-specific economic candidate | candidate | permission, reservation or order | Opportunity |
| `NetConvert(q)` | Canonical exact directed conversion output with depth/fees/precision | conversion | midpoint estimate or second fee/slippage pass | Formula |
| Maximum Profitable Size | QF-027 economic threshold result | profitable capacity | `Q_validated` | Route/Sizing |
| `Q_validated` | QF-076 largest size passing all exact support/safety/evidence gates | validated capacity | visible depth, balance or target q | Validation/Sizing/Risk |
| Position Sizing | Select total proposed exposure `q*` | Sizer | child-order schedule | Inventory/Capital |
| Order Slicing | Decompose fixed validated q into child actions | Slicing | new capacity or sizing | Execution |
| actual | Exchange-observed, deduplicated and reconciled fact | realized | planned, predicted, simulated, would-* | Execution/Data |
| predicted | Model output with artifact/support/provenance | forecast | actual or counterfactual realization | Model owner |
| simulated / counterfactual | Declared branch under stated fidelity and assumptions | scenario | exact alternate universe | Simulator |
| `UNKNOWN` | Scoped inability to prove a required economic/order fact | unresolved | zero, rejected, safe or absent | Execution/Data |
| `RunMode` | `Replay`, `Paper`, `Shadow`, `MicroLive`, `Live` | Micro-live in prose | maturity, execution mode or Replay submode | Data/Execution |
| execution mode | `TT`, `TTT`, `MT`, `MTT`, with `TM`/`MM` type-supported and disabled | leg-role mode | `RunMode` | Execution |
| maturity | Capability-scoped M0–M5 evidence level | validation level | global project state or runtime health | Validation |
| `InfraState` | `HEALTHY`, `DEGRADED`, `UNSAFE` | infrastructure health | P0–P3 severity or EngineState | Infrastructure/Data |
| alert severity | P0–P3 operational urgency | critical alert | `InfraState` enum | Operations |
| `CapabilityManifest` | Release-linked exact validated capability entries/evidence | manifest | installed code, config, license or Risk permission | Validation |
| `RiskDecision` | Current structured permission/reject/limit result | risk permission | economic ranking or operator override | Risk |
| `ExecutionPlan` | Immutable Risk-linked executable plan | plan | intent, order or fill | Execution |
| Accounting | Logical attribution owner documented under Inventory/Capital + Formula/Data boundaries | PnL ledger | a missing standalone master or second fill truth | Accounting logical owner |

Capital action names `STRATEGY`, `BRIDGE/RELOCATION`, `REBALANCE`, `RECOVERY` and `STAY/HOLD` remain disjoint. Casing variants in explanatory prose do not create new enum values.
