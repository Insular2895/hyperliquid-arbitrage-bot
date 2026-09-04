# PASS 05 — RISK CONSTITUTION COMPLETE

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Risk-related requirements reviewed: **752/752** unique PASS 00 Risk-index requirements; source locator failures: **0**.

SRC-005 Risk Constitution fully reviewed: **YES** — Dossier 3/6 lines 1–5373, sections 1–242, sequentially.

Constitutional principles recovered: **YES** — exact priority hierarchy, safe-action-set optimization, exact seven-action priority, five Risk layers, global PnL non-relaxation, exchange truth, uncertainty/failure reduction, observability, determinism and reproducibility.

`INV-*` invariants found: **30** — exact contiguous set `INV-001..INV-030`.

`INV-*` invariants documented: **30/30**; exact name mismatches: **0**; superseded: **0**; destinationless: **0**.

Hard invariants: **30 structural invariants**. Seven explicitly contain calibrated bound/health policy while preserving hard fail-safe direction.

Calibrated policies: **44 parameter families** cataloged; exact values invented: **0**. Total governed parameter families: **73** — 12 constitutional, 44 calibrated, 4 learned, 4 exchange-rule, 2 safety-default, 3 user-tightenable, 4 open.

Risk gates: **13 canonical ordered pipeline stages**; 26 named eligibility/market/model/outcome gate families plus explicit soft-inventory/portfolio/sizing controls and final pre-send revalidation.

RiskDecision actions: **7/7** — `ALLOW`, `ALLOW_REDUCED_SIZE`, `ALLOW_RECOVERY_ONLY`, `REJECT`, `HALT_MARKET`, `HALT_STRATEGY`, `HALT_GLOBAL`.

Revalidation points: **6/6** — T0 opportunity detection; T1 before reservation; T2 immediately before send; T3 after each fill; T4 before each next leg; T5 while maker rests. `TTL_risk` remains calibrated and material version change invalidates earlier.

Kill switches: **7 exact scope names** plus **5 specialized quality/change trigger families**. Scope, action, dependency effect, recovery/reconciliation, reset, telemetry and validation are mapped.

Action classes: **3/3** — `RISK_INCREASING`, `RISK_NEUTRAL`, `RISK_REDUCING`.

Config-governance rules: **YES** — constitutional/tunable separation, seven provenance classes, no magic numbers, atomic/versioned updates, plan pinning, client tightening and no dangerous override.

Recovery Risk rules: **YES** — negative EV allowed only to reduce known exposure; current valid execution state, protection and reservations required; attempt/time/loss/tail/inventory/capacity bounds; no route loyalty, sunk-cost widening or unlimited loop; halt/manual escalation on exhaustion.

Tail-risk rules: **YES** — P positive, loss, VaR diagnostic, ES/CVaR, worst-route loss, recovery tail, portfolio expected-loss contribution, no EV override and no double counting.

Capital-scaling rules: **YES** — `Q_validated` and the intersection of all gates bound size; profit/capital/premium infrastructure do not raise limits automatically; scaling requires replay/shadow/micro-live/tail/capacity/recovery/infra evidence.

Status corrections from PASS 00: **14** false keyword-heuristic statuses inside SRC-005 corrected under closure authority; exact IDs listed in `RISK_CONFLICT_RESOLUTION.md`.

Formula references checked: **30 required concept groups**, spanning QF-002–006, QF-038–042, QF-044–050, QF-059–066, QF-068–069, QF-073–080, QF-084–091, QF-102–104 and QF-109–110. Formula definitions changed: **0**.

Data contracts mapped: **23** exact contracts/representations. Frozen RiskSnapshot/RiskDecision/ExecutionPlan fields were reconciled against semantic Risk requirements.

Conflicts found: **8** PASS 05 conflict classes.

Conflicts resolved: **8** by source/closure authority.

Conflicts remaining: **0 constitutional/documentary conflicts**.

Cross-domain gaps: **4 explicit Data-schema encodings** — standalone RiskConfig, consolidated state hashes, asset/mode/model/infra kill-event variants, and rejected-opportunity counterfactual-outcome linkage. They are routed to Data/Operations closure; no fields were invented. Formula values, inventory/portfolio parameters and operational runbooks retain their owning future passes.

External revalidation items: **42 indexed requirements** routed to the external register; 10 existing external fact families are Risk-relevant (`EXT-001/002/003/004/005/006/007/008/015/016`). External/web revalidation performed: **NO**.

Master created: **YES** — `docs_v2/09_RISK_CONSTITUTION.md`, exact 32-section structure.

Deep specs created: **11/11 plus README**.

Analysis artifacts created: **14/14 including this report**.

Legacy omissions recovered: **16 material areas**. Legacy files edited: **NO**.

Coverage gaps: **0 uncovered requirements**. Explicit cross-domain/open/calibrated items remain traceable rather than treated as coverage loss.

Destinationless requirements: **0**.

Files modified outside `docs_v2`: **0**. Pre-existing untracked `.DS_Store` is unrelated and excluded.

PASS 06 started:
NO

Human review required: **YES**. This reconstruction does not authorize implementation, capability activation, parameter promotion or Live capital.
