# PASS 07 — INVENTORY / CAPITAL / BRIDGE / SIZING COMPLETE

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Inventory/Capital requirements reviewed: **545/545** unique PASS00 domain-index requirements across SRC-001–008; unique IDs: **545**; source locator failures: **0**.

Original source sections reopened: **YES** — all 545 indexed ranges were reopened from the eight original source files; high-authority/detail blocks for SRC-003 inventory/OWA/Bridge/Sizing/Rebalance, SRC-004 QF formulas, SRC-005 Risk/Data closures, SRC-006 validation and SRC-007/SRC-008 sizing/capital reasoning were reread contextually.

Asset classes reconstructed: **3/3** — `CORE_INVENTORY` (`CoreInventory` frozen enum), `TRANSIT` (`Transit`), `EXCLUDED` (`Excluded`). Venue/location is a separate dimension; no fourth class was invented.

Inventory bands reconstructed: **YES** — Target, SoftMin, SoftMax, HardMin, HardMax with locked ordering and future-state evaluation. Exact class assignments, bands and thresholds remain calibrated/learned under OPEN-009.

NetFlow: **YES** — QF-067, actual-fill deltas over multiple calibrated windows, offline-reference validation and pre-hard-limit directional control.

Terminal Viability: **YES** — post-action hard/soft inventory, class, exit path/cost/liquidity, stranded risk, future utility, Risk and confidence/OOD are explicit. Positive route edge alone cannot pass.

Stranded Capital: **YES** — QF-068 Expected Exit Cost and QF-069 exit/idle/risk components, size-aware and separately calibrated/accounted.

Bridge semantics: **YES** — proactive intentional Capital Relocation toward supported future utility; STAY is mandatory; path selection is economic through NetConvert, not shortest-hop.

OWA/Bridge distinction: **YES** — OWA requires a fair direct A-to-B comparator; without one A-to-X-to-B is Bridge/relocation. Conversion Alpha and relocation value remain separate even when both exist.

Bridge/Rebalance distinction: **YES** — Bridge seeks future destination utility; Rebalance restores inventory/capacity and compares waiting/natural reversal with action. Rebalance loss is separate from Strategy alpha.

Bridge/Recovery distinction: **YES** — Bridge starts intentionally from controlled state; Recovery addresses existing unwanted/unsafe exposure with constitutional priority. Partial failed Bridge exposure becomes actual Recovery input.

Bridge formulas crosschecked: **5/5** — QF-068 through QF-072, including positive-cycle/infinity branch, destination-versus-stay comparison, expected exit and relocation risk.

Position Sizing: **YES** — nonlinear RAEV curve inside the intersection of available balance, book, `Q_validated`, Risk, future inventory and capability constraints. Risk maximum is a ceiling, not a target.

Sizing/Slicing boundary: **YES** — Position Sizing chooses total exposure; Order Slicing executes the fixed validated quantity. TT/MT/TTT/MTT examples and same-time fragmentation limits are explicit.

Q_validated: **YES** — QF-076 is largest all-gates-valid quantity, distinct from QF-027 Maximum Profitable Size and raw visible depth; state/mode/regime/evidence dependent and reversible.

Shared capacity: **YES** — QF-073/QF-074, distinct balance/book/Risk reservations, `UNKNOWN` retention, shared balance and L2 double-count prevention.

Multi-opportunity allocation: **YES** — QF-078 acts after individual viability and Risk eligibility, jointly constrains capital, shared book, future inventory and Risk, and remains subordinate to action priority.

PnL classification: **YES** — Route/Strategy, execution cost, Recovery, Inventory MTM, Rebalance, Bridge/Relocation, Infrastructure and idle-capital components remain attributable; expected penalties remain distinct from realized accounting and external flows.

Formula refs checked: **32/32 minimum direct references** — QF-016, 026, 027, 040–042, 056–057, 059, 062–080 and 105–108; additionally QF-019–023 and QF-104 consumer interfaces. No alternative formula was created.

Status corrections: **19** reviewed closure/keyword false positives documented. Original PASS00 status remains visible; prior PASS04/PASS05 closure is not downgraded.

Conflicts found: **16** source-evolution classes.

Conflicts resolved: **16/16** by later closure/source authority.

Conflicts remaining: **0 documentary conflicts**. Calibrations and future owner work are explicit dependencies, not hidden conflicts.

Cross-domain gaps: **4 families** — PASS08 route/Market Graph/Atlas/HOT-WARM-COLD fields; PASS11 Formula Index expression/unit audit; Data-governed Inventory/Capital/PnL schema expansion; validation evidence for exact calibrated/learned parameters.

Master created: **1/1** — `docs_v2/08_INVENTORY_AND_CAPITAL.md` with all 33 required sections.

Deep specs created: **11/11 plus README** under `docs_v2/deep-specs/inventory-capital/`.

Analysis artifacts created: **19/19 including this report**.

Legacy omissions recovered: **12 material families**; fixed examples, shortest-hop/fake-fragmentation and positive-edge-only assumptions are superseded or rejected; legacy files edited: **NO**.

Coverage gaps: **0**. The no-loss vocabulary/formula search passes; every reviewed requirement retains one allowed disposition and a destination.

Requirement disposition: MASTER **24**; DEEP_SPEC **246**; CROSS_DOMAIN_PASS08 **37**; FORMULA_REFERENCE **39**; OPEN_ITEM **1**; SUPERSEDED **0**; REJECTED **2**; RESEARCH/FUTURE **196**; total **545**.

Destinationless requirements:
0

Files created under `docs_v2`: **32**. Existing `docs_v2` files updated: **6**.

Files modified outside docs_v2: **0**. Pre-existing untracked `.DS_Store` is unrelated and excluded.

PASS 08 started:
NO

Human review required: **YES**. This reconstruction does not authorize implementation, Live capital, asset classifications, inventory values, Bridge movement, strategy activation, schema migration or scaling.
