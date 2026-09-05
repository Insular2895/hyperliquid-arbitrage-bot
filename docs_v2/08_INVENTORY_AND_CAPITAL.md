# 08 — Inventory and Capital

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

This specification defines the economic state and allocation rules for inventory, capital, Bridge/Capital Relocation, Position Sizing and portfolio allocation. It turns actual fills into an auditable capital state and decides how much already-eligible exposure is economically useful. It does not authorize unsafe actions, execute orders, invent routes, or replace the Formula Book.

## 2. Authority

SRC-004 is authoritative for QF formulas and Execution closure; SRC-005 for Risk and frozen Data contracts; SRC-006 for validation gates. SRC-003 and SRC-007 provide the detailed economic reasoning; SRC-001, SRC-002 and SRC-008 preserve earlier exploration and calibration context. Later closure overrides earlier variants. Formula expressions remain owned by `docs_v2/_analysis/FORMULA_INDEX.md` and SRC-004; this document references, but does not fork, them.

## 3. Core principles

1. Actual fills, not plans or forecasts, change actual inventory.
2. Account balance, economic inventory, reservations, pending exposure and MTM are distinct views.
3. Hard Risk gates define the feasible set; economic objectives optimize only inside it.
4. Every intentional terminal asset needs a credible, size-aware exit.
5. Positive immediate route edge does not prove terminal or portfolio value.
6. Bridge, OWA, Rebalance and Recovery are different capital actions with different purposes and accounting.
7. Position Sizing chooses exposure; Order Slicing executes a validated exposure.
8. Balance, book and Risk capacity are shared and reserved once.
9. More capital does not create validated market capacity.
10. Expected decision penalties never masquerade as realized cash PnL.

## 4. Actual inventory / actual fills

The canonical economic transition occurs after every deduplicated `FillEvent`: `Inventory_new = Inventory_old + AssetDelta`, including fee and rounding effects according to the Data/Execution contracts. Partial fills create real exposure immediately. A planned route, simulated `PortfolioAfter`, expected fill or submitted order never updates actual inventory.

The single-writer reducer materializes actual account balances and `InventoryState`; reservations remain separate claims. `UNKNOWN` order state keeps affected capital reserved. Reconciliation compares local fill-derived state with exchange truth and blocks affected new risk on an unresolved mismatch.

## 5. Asset classification

The canonical source enum is `CoreInventory`, `Transit`, `Excluded`; searchable economic labels are `CORE_INVENTORY`, `TRANSIT`, `EXCLUDED`.

| Class | Meaning | Intentional accumulation | Normal terminal | Required behavior |
|---|---|---|---|---|
| `CORE_INVENTORY` | Capital may intentionally live here inside validated bands. | Yes, bounded; never unlimited. | Permitted only when Terminal Viability passes. | Target/bands, exitability and capital utility must be evidenced. |
| `TRANSIT` | Temporary intermediate needed to complete a path. | No, unless a controlled reclassification occurs. | Not a normal destination. | Short holding age/value; residual exposure enters Rebalance/Recovery as policy requires. |
| `EXCLUDED` | Unsupported or economically unsafe asset. | No. | No. | Reject intentional use; existing accidental exposure is handled as Recovery, not ignored. |

Classification is versioned, point-in-time, evidence-driven and stable under calibrated hysteresis. Examples such as BTC/ETH/HYPE/USDC are candidates, not predetermined classifications.

## 6. Inventory bands

Each tradable asset has `Target`, `SoftMin`, `SoftMax`, `HardMin`, `HardMax`, ordered as required by the Risk Constitution. Exact values are `CALIBRATED`/`LEARNED` and remain OPEN-009 until evidence supports them.

The inventory target is a policy input, not a balance forecast or fixed universal percentage.

- Inside the soft band, inventory alone causes no hard reject; QF-065 may affect economics.
- Outside the soft band, directionally harmful actions may be penalized or size-reduced.
- A future state beyond a hard band is rejected by QF-066 for new risk.
- A strictly risk-reducing action may use the constitutional exception; it cannot worsen the violation.

QF-064 normalizes deviation; QF-065 is a calibrated soft decision penalty; QF-066 is the locked hard boundary. Fixed percentage examples in earlier sources are illustrative, never defaults.

## 7. NetFlow

QF-067 measures signed inventory change over a window. Multiple horizons detect directional accumulation before the hard band is reached. Exact horizons and thresholds are calibrated. NetFlow can reduce size or attractiveness but cannot manufacture a hard-limit override. It is computed from actual fill-derived deltas and checked against an offline reference in validation.

## 8. Inventory Graph / capital reachability

The Inventory Graph is the economic view of where capital actually exists, which permitted conversions can redeploy it, and which credible exits exist. Capital Reachability distinguishes:

- structural reachability in the Market Graph;
- reachability from the current available inventory;
- economically valid, Risk-eligible and size-supported reachability;
- future reachability after a Bridge or completed route.

PASS08 owns Market Graph topology, route definitions, HOT/WARM/COLD and Market Atlas. PASS07 consumes their point-in-time outputs and does not define a parallel graph.

## 9. Terminal Viability

Before accepting a candidate terminal state, evaluate future hard inventory, soft deviation, asset classification, exit path, size-dependent exit cost, exit liquidity, stranded risk, future capital utility, volatility/Risk and model confidence. Failure can reject an otherwise profitable OWA with `REJECT_TERMINAL_ASSET` or the appropriate machine-readable Risk reason.

Terminal Viability uses the state that would exist after the candidate execution. A valid terminal is not merely a holdable token; it is a supported capital state with a credible exit and acceptable bounds.

## 10. Exit cost / stranded capital

QF-068 defines Expected Exit Cost from current value and the best executable exit value, including the authoritative NetConvert path effects. It is quantity-, state- and path-dependent. QF-069 defines Stranded Capital Penalty as separately stored expected exit, idle and risk components. The structure of QF-068 is locked; QF-069 coefficients/components are calibrated.

Capital is stranded when it exists but cannot be redeployed or exited efficiently enough for the intended horizon. A nominal wallet balance is therefore not proof of useful capital.

## 11. Capital utility / opportunity cost

Capital utility is empirical: validated opportunity frequency, executable capacity, capture probability, exitability, competition, risk and expected utilization. Raw route count is not utility. Structural routes, capital-reachable routes and validated active opportunities remain distinct.

Opportunity Cost applies when a Bridge, resting maker order, reservation or unwanted inventory prevents the best supported alternative. QF-105 Expected Idle Capital Cost uses an empirical opportunity rate and duration; it is not an arbitrary interest rate and cannot justify violating Risk.

## 12. Bridge definition

A Bridge is an intentional conversion path used to relocate capital into a more useful future state. It can pay an immediate cost for positive future utility and is not automatically an arbitrage. Candidate paths are compared by economic output/cost through QF-016 and QF-070, not by hop count.

## 13. Bridge vs OWA

OWA compares `A -> X -> B` with a valid, temporally fair direct `A -> B` comparator in the same terminal asset. Without that comparator, the path is Bridge/Capital Relocation, never OWA. A path may simultaneously have Conversion Alpha and support a separate relocation decision, but those values and accounting labels remain separate.

## 14. Bridge vs Rebalance

Bridge proactively seeks a more useful future capital location. Rebalance restores inventory toward validated targets/bands, often after accumulated drift. Rebalance may accept negative immediate PnL for risk/capacity restoration, but that loss is recorded separately and never hidden inside route alpha. The choice to wait for a naturally rebalancing opportunity is valid.

## 15. Bridge vs Recovery

Bridge starts from a controlled state and intentionally creates a destination exposure. Recovery responds to existing unwanted, partial or unsafe exposure and follows the Risk/Execution priority. A partially executed or failed Bridge produces actual exposure and may transition into Recovery. Recovery may be negative EV because safety dominates; Bridge receives no such exemption.

## 16. Bridge economics

The relocation pipeline compares current capital state, point-in-time Atlas evidence, candidate destinations/paths, QF-070 Bridge Cost, QF-068 Expected Exit Cost, relocation risk, destination value and the STAY alternative. QF-070 uses NetConvert so spread, fees and slippage are not manually subtracted twice. Risk, time and terminal exit remain explicit.

## 17. Break-even cycles

QF-071 measures how many positive expected future cycles are required to amortize Bridge Cost plus Expected Exit Cost. It is infinite when expected cycle PnL is non-positive. The future-cycle estimate is learned by regime and point-in-time evidence; predicted and realized break-even must be compared. A stale average cannot authorize relocation.

## 18. Capital Relocation Value

QF-072 compares `EV_destination` with `EV_stay`, then accounts for `BridgeCost`, `ExpectedExitCost` and `RelocationRiskCost`. `STAY` is always a candidate. Movement requires the locked positive-advantage structure plus calibrated threshold, hysteresis/cooldown and Risk approval. A destination's single transient edge is insufficient evidence.

## 19. Hysteresis / cooldown

Existence of anti-flip-flop governance is locked; threshold, cooldown, persistence horizon and evidence windows are calibrated. Relocation and dynamic asset reclassification require persistent evidence across suitable horizons. Decisions are reversible: adverse calibration, OOD or changed utility may demote a destination or shrink allocated capital.

## 20. Position Sizing

Position Sizing answers: how much exposure should an already eligible opportunity receive? QF-075 maximizes Risk-Adjusted EV over the feasible quantity region. The size curve is nonlinear because L2 levels, rounding, fees, impact, completion probability, P+, CVaR, confidence, inventory and Recovery change with quantity.

The feasible region is the intersection of available balance, available book capacity, `Q_validated`, Risk maximum, future inventory capacity and strategy/mode capability. `max_allowed_size` is a ceiling, not a target. If no size passes, `q*=0`.

## 21. Q_validated

QF-076 defines `Q_validated` as the largest quantity for which all required gates remain true. It is not visible depth and is not QF-027 Maximum Profitable Size. `Q_validated` is route-, state-, execution-mode-, regime-, liquidity-, model-, inventory- and Risk-dependent. It can increase or decrease as evidence changes; more account capital alone does not increase it.

## 22. Sizing search

QF-077 locks a candidate-grid, best-region, local-refinement method because book/rounding economics can be discontinuous. Candidate sizes are evaluated with the same NetConvert, Simulator distributions and Risk gates. Grid values and refinement density are calibrated, and small cases are compared with exhaustive search.

## 23. Sizing vs Slicing

Position Sizing outputs total validated quantity. Order Slicing takes that fixed upper bound and chooses child timing/shape under Execution rules. Splitting one simultaneous order does not create liquidity; same-time children must consume approximately the same mechanical depth as the equivalent total size.

TT, MT, TTT and MTT have different size curves because fill, latency, intermediate exposure and Recovery differ. Slicing cannot enlarge `Q_validated`, bypass reservations, or turn a calibration probe into strategic size.

## 24. Shared balance/book capacity

QF-073 derives Available Balance from actual minus reserved balance. QF-074 derives Available Book Capacity from observed minus reserved capacity for a book resource. Balance, book and Risk reservations are distinct, versioned claims.

Two routes sharing a balance or L2 side cannot both consume the full resource. Ranking reserves nothing; only accepted allocation followed by canonical reservation changes deployable capacity. Stale/expired candidates release only according to Execution/Risk rules; `UNKNOWN` keeps affected claims locked.

Shared book capacity is always computed jointly for routes that consume the same market side/depth band.

## 25. Multi-opportunity allocation

After individual viability, Risk eligibility and size-curve construction, QF-078 chooses quantities jointly to maximize the sum of Risk-Adjusted EV inside shared capital, book, inventory and Risk constraints. The optimizer is subordinate to hard gates and action priority. It cannot select a Risk-rejected route.

The final sequence is: individual viability -> Risk eligibility -> size curves -> portfolio allocation -> reservation -> final pre-send revalidation. Recovery and protection of existing exposure receive constitutional priority over Bridge, Rebalance and new opportunities.

## 26. Horizontal / vertical scaling

Horizontal scale allocates capital across genuinely independent validated opportunities; vertical scale increases quantity on one opportunity. Horizontal scaling is generally preferred before forcing larger quantity into the same nonlinear book, but it is not an absolute rule. Correlated routes sharing asset, market, capital, terminal inventory or Risk budget are not independent.

The 40–50 EUR source example is a Micro-live probe only. Scaling uses evidence-gated steps, never a direct 10x jump or fixed percent-of-capital rule. Surplus capital may remain idle.

## 27. PnL classification

The accounting layer keeps at least Route/Strategy PnL, execution costs, Recovery PnL/Loss, Inventory MTM, Rebalance PnL, Bridge/Relocation PnL, Infrastructure Cost and Idle Capital Cost attributable and reconcilable.

QF-106 defines Global Economic PnL; QF-107 defines Inventory Mark-to-Market excluding external flows; QF-108 distinguishes Total Strategy PnL from global economics. Actual fees/fills replace forecasts after execution. Expected inventory/stranded/relocation penalties are decision economics, not realized PnL. A component already included in executable conversion or PnL distribution is not subtracted again.

## 28. Risk interfaces

Risk owns hard inventory, maximum size, participation/impact, P+, CVaR/tail, OOD/model confidence, capital-at-risk and new-risk permission. PASS07 supplies future inventory, size curves, resource demand and economic ranking, then obeys Risk. QF-066 cannot be softened by the optimizer. `ALLOW_REDUCED_SIZE` applies only when the reduced point is independently valid.

## 29. Execution interfaces

Execution owns actual fills, reservation mechanics, orders, partials, `UNKNOWN`, Recovery execution, reconciliation and release. PASS07 provides requested resource quantities and economic action classification. Execution returns fill/account facts that update actual inventory and realized accounting. No hidden or locally inferred balance substitutes for exchange truth.

## 30. Market Atlas interfaces

PASS08 must provide point-in-time, versioned structural reachability, candidate paths, validated route/activity evidence, opportunity frequency, size-supported capacity, liquidity/exit metrics, survival, competition and capital utility signals. PASS07 never uses today's completed Atlas in a historical decision and never equates raw route count with validated opportunity count.

## 31. Replay / evidence

Replay must reconstruct inventory, reservations, allocation, Bridge state and accounting from canonical events/config. Alternative bands, hysteresis, sizing and allocation policies are counterfactual configurations in the RunManifest. It records candidate/rejected Bridges, STAY comparator, full candidate size curves, rejection reasons and predicted-vs-actual outcomes.

Promotion proceeds Replay -> Shadow -> Micro-live -> stepped Live capacity. Required blocking tests include no overspend, no shared-depth double count, future-inventory evaluation, action classification and PnL reconciliation. No-lookahead applies to forecasts and Atlas state.

## 32. Calibrated / learned items

`CALIBRATED`: targets/bands, QF-065 coefficient/form if revisable under Formula governance, NetFlow windows/limits, stranded components, relocation threshold, hysteresis/cooldown/persistence, search grid, reservation tolerances, allocation limits and probe/scale gates.

`LEARNED/VALIDATED`: asset classification, opportunity/capital utility, future cycle PnL, exit/idle behavior, size-specific distributions, `Q_validated`, model confidence and capacity drift. Exact formulas remain governed by their QF status; PASS11 audits unit/expression consistency.

## 33. Deep-spec links

- [Inventory state, asset classes and bands](deep-specs/inventory-capital/01_INVENTORY_STATE_ASSET_CLASSES_AND_BANDS.md)
- [NetFlow, reachability and terminal viability](deep-specs/inventory-capital/02_NETFLOW_CAPITAL_REACHABILITY_AND_TERMINAL_VIABILITY.md)
- [Exit, stranded capital and inventory economics](deep-specs/inventory-capital/03_EXIT_COST_STRANDED_CAPITAL_AND_INVENTORY_ECONOMICS.md)
- [Bridge and relocation engine](deep-specs/inventory-capital/04_BRIDGE_AND_CAPITAL_RELOCATION_ENGINE.md)
- [Relocation governance](deep-specs/inventory-capital/05_HYSTERESIS_COOLDOWN_AND_RELOCATION_GOVERNANCE.md)
- [Position Sizing and validated capacity](deep-specs/inventory-capital/06_POSITION_SIZING_VALIDATED_CAPACITY_AND_SEARCH.md)
- [Sizing vs Slicing](deep-specs/inventory-capital/07_POSITION_SIZING_VS_ORDER_SLICING.md)
- [Shared capacity and portfolio allocation](deep-specs/inventory-capital/08_SHARED_CAPACITY_RESERVATIONS_AND_MULTI_OP_ALLOCATION.md)
- [Capital action boundaries](deep-specs/inventory-capital/09_REBALANCE_RECOVERY_AND_CAPITAL_ACTION_BOUNDARIES.md)
- [PnL and capital efficiency](deep-specs/inventory-capital/10_ECONOMIC_PNL_ACCOUNTING_AND_CAPITAL_EFFICIENCY.md)
- [Validation and scaling](deep-specs/inventory-capital/11_VALIDATION_REPLAY_SHADOW_MICROLIVE_AND_SCALING.md)
