# Architecture Legacy Comparison

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Legacy file reviewed after V2/source-first reconstruction: `docs/00_MASTER_ARCHITECTURE.md`. It remains `LEGACY_REFERENCE_ONLY` and was not edited.

| Legacy statement/area | Classification | PASS 13 result |
|---|---|---|
| Product vision, ten principles and Risk priority | STILL_CANONICAL / RECOVERED | retained with explicit domain authority and status boundaries |
| One high-level logical diagram | OVER_COMPRESSED | replaced by focused context, decision, execution, data, capital and deployment diagrams |
| Market→decision path | OVER_COMPRESSED | staged Risk, version checks, terminal viability, q curve and allocation made explicit |
| Execution happy path | MISSING_FAILURE_SEMANTICS | SENT/UNKNOWN/cancel race/partial/dust/reservation/reconciliation boundaries recovered |
| Risk hierarchy | STILL_CANONICAL | retained, plus T0–T5 and structured decisions |
| HWC summary | MISSING_BOUNDARY | Graph, Atlas, HWC, Watcher, Capital Reachability and Risk ownership separated |
| Research/live table | OVER_COMPRESSED | full RunMode matrix, Simulator fidelity and model promotion recovered |
| Deployment paragraph | MISSING_BOUNDARY | OCI, trust, mounts, license, active owner and update transaction detailed |
| Module dependency sketch | MISSING_STATE_OWNERSHIP | component catalog, state writers, interfaces and event/effect model added |
| Broad safety properties | OVER_COMPRESSED | 27 cross-domain invariants with owners/responses cataloged |
| Replay/Simulator relation | MISSING_BOUNDARY | reconstruction and counterfactual distributions separated |
| Capital actions | MISSING_BOUNDARY | Strategy/Bridge/Rebalance/Recovery/STAY and Sizing/Slicing separated |
| Capability/evidence | MISSING_BOUNDARY | implementation/config/license/readiness/Risk intersection and M0–M5 added |
| Failure/incident flow | MISSING_FAILURE_SEMANTICS | scoped containment, demotion and revalidation flow added |
| Component-specific mutable state | MISSING_STATE_OWNERSHIP | all required state families assigned one logical writer |
| Source link to absent `TRACEABILITY_MATRIX.md` | LEGACY_UNTRACED | replaced by PASS00/PASS13 ledgers and exact source locator evidence |
| Any implication all drawn modules are active | CONTRADICTED | explicit Current/Progressive/Future classifications added |
| Exact serialized evidence integration | ROUTED_TO_PASS14 | `ARCH-GAP-001` |
| Accounting documentation authority | ROUTED_TO_PASS14 | `ARCH-GAP-002` |

Material omission/boundary groups recovered: **15**. Legacy-only architecture decisions imported without V2/original-source support: **0**.
