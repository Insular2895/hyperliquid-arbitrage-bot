# Implementation Authorization Checklist

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Authorization invariants

Default deny: anything not explicitly authorized remains unauthorized. Authorization is exact-scope, exact-commit, non-transitive and non-widening. Documentation approval, switchover authorization, switchover acceptance, Phase-1 authorization, Phase-1 exit, Phase-2 authorization and capital authorization are different records.

No gate below is approved. `PENDING` means a decision is currently eligible but unmade. `NOT_AVAILABLE` means a prerequisite is unsatisfied. `NOT_STARTED` describes an execution/evidence stage that has not begun. `NOT_AUTHORIZED` describes capability permission. None is implicit approval.

## Review package identity

| Field | Current value |
|---|---|
| Final Review Candidate | exact immutable Git commit selected for review as F |
| Candidate identity location | future human `DocumentationDecision` / `ReviewRecord`: exact F commit SHA, tree SHA and `codex-docs` branch |
| branch | `codex-docs` |
| review manifest | `_analysis/phase19_implementation_authorization/REVIEW_PACKAGE_MANIFEST.md` |
| review subject | complete exact F corpus; moving HEAD or the latest branch tip is never sufficient identity |
| historical lineage | A/C/post-C preserved in `_analysis`; superseded for current review identity |
| traceability | Phase-18 source certificate plus explicit historical and post-certificate L3/L4 lineage through F |
| human-policy count | 2 as derived by Phase 14; HPD-01 is MT/MTT-only; never hard-coded as permanent |
| safety-invariant set | all applicable `SI-*` resolved from exact F (currently 29 unique IDs), never hard-coded as permanent |

## Independent gates

| Gate | Decision | Required record/evidence | Current status |
|---|---|---|---|
| A — Review Package Completeness | package is internally complete and exact-snapshot traceable | manifest, cross-audit, non-stale traceability lineage | MECHANICAL CHECK PASS / HUMAN CONFIRMATION PENDING |
| B — Documentation Approval | human accepts exact Final Review Candidate F | reviewer/time/F SHA/tree/branch/scope/decision | PENDING |
| C — Switchover Authorization | human permits procedural `docs_v2 -> docs` transformation from exact approved F | separate exact-scope record bound to F | NOT_AVAILABLE |
| D — Canonical Switchover Acceptance | human accepts generated Commit B after manifest/diff/link/rollback proof | F→B evidence and separate reviewer record bound to B | NOT_AVAILABLE |
| E — Phase 1 Implementation Authorization | human permits exact Phase-1 scope from accepted Commit B | AuthorizationRecord bound to Commit B SHA/tree | NOT_AVAILABLE |
| F — Phase 1 Exit | Phase-1 DoD evidence is accepted | versioned M1 report and deviations | NOT_STARTED |
| G — Phase 2 Authorization | human separately permits Phase 2 after Gate F | new exact-scope AuthorizationRecord | NOT_AVAILABLE |

Completing one row does not change any other row. No checkbox or blanket signature can cover multiple decision types.

Gate A's remaining human confirmation is a package-completeness check, not an authorization decision. Among Gates B–G, Gate B alone is currently decision-eligible. HPD policy review is separately scoped and grants no capability permission.

Transitions are explicit and non-automatic: Gate-B approval makes Gate C `PENDING`; Gate-C approval plus generated/validated B makes Gate D `PENDING`; Gate-D acceptance makes Gate E `PENDING`; Gate-E authorization permits Phase 1 to start; completed Phase 1 plus accepted Gate-F evidence makes Gate G `PENDING`. A predecessor record alone never executes the transition or approves its successor.

## Human decisions, HDC and invariants

Phase 14 recomputes genuine human-policy families; Phase 19 consumes that result rather than “exactly eight.” Each applicable family receives its own scoped disposition. HDC-001..094 are a traced post-source requirements package, not 94 policy decisions and not blanket-approved through documentation acceptance; any per-item activation/promotion boundary remains governed by its owner.

The invariant review enumerates all applicable `SI-*` resolved from exact F. Historical C corrected SI-022's summary wording to distinguish the validated-q set from QF-076's scalar supremum; F includes that correction. The current set contains 29, but the gate stores IDs/hash/count derived from exact F, not a permanent “29” assumption. Source no-loss is necessary evidence, not sufficient semantic approval.

## Phase 1 exact authorized scope

If Gate E is later approved, it may cover only strong domain/evidence IDs; typed price, quantity, notional and time units; event envelopes; schema/snapshot versions; deterministic ordering foundations; `Clock`; `RngProvider`; `RunManifest` foundations; serialization/compatibility; and unit/property/misuse tests.

Phase-1 DoD: strong units cannot mix; schemas round-trip and versions are explicit; invalid/incompatible/overflow inputs fail; hidden clock/randomness is absent; deterministic ordering foundations pass; and a versioned M1 evidence report exists.

Explicitly unauthorized: adapters/network/Hyperliquid parsing, books, formulas, opportunity/strategy, Risk behavior, execution transport/signing/effects, capital, deployment automation, Phase 2+, Shadow, Micro-live, Live, maker, Bridge, scaling, parameter search, Monte Carlo and any research runtime. Final-capable interfaces do not authorize future behavior.

## Blocking rule and external/calibration scope

An unresolved item blocks Phase 1 only if Phase 1 consumes it, no canonical conservative fallback exists, and proceeding would force semantic invention. Research/Future, Maker, Bridge, model, infra-ranking and capital questions remain non-blocking when independent. Phase-1 types assume no current exchange behavior; external facts gate their later consumers. Calibrated/learned values remain candidate evidence, not authorization.

## AuthorizationRecord

Required fields: `decision_id`; `decision_type`; exact `subject_commit_sha`; exact `subject_tree_sha`; `branch`; `status`; `authorized_scope`; `explicitly_excluded_scope`; `prerequisites`; `evidence_refs`; applicable SI IDs/hash; human-policy dispositions consumed; external freshness assumptions; start/stop conditions; required exit evidence; `reviewer`; `decision_timestamp`; `validity`; `supersedes`; and `notes`. Decision states include `PENDING`, `NOT_AVAILABLE`, `APPROVED_WITH_EXPLICIT_SCOPE`, `REJECTED`, `STALE` and `SUPERSEDED`; execution evidence may additionally be `NOT_STARTED`.

For `DOCUMENTATION_APPROVAL`, `subject_commit_sha` and `subject_tree_sha` identify exact F. For `PHASE1_AUTHORIZATION`, they identify exact accepted B. These identities are supplied by the applicable record; no documentation file needs to know or embed its own future subject SHA.

An AuthorizationRecord cannot interpret itself beyond `authorized_scope`. A semantic commit/scope/invariant/traceability change makes affected approval stale. A proven-independent Research/Future edit need not invalidate Phase 1, but that independence must be recorded.

## Mandatory stop and later phases

After Phase 1 reaches its DoD, stop. Do not merge, start Phase 2, deploy or use capital. Gate F review and a new Gate-G authorization are required. Shared helpers created within Phase 1 cannot leak authorization to a Phase-2 consumer.

Implementation authorization never grants capital. Capital requires separately validated exact capability, readiness, Risk and a capital-specific authorization. Research documentation acceptance permits no research runtime. No automatic merge, branch creation, coding, switchover or deployment follows any documentation decision.
