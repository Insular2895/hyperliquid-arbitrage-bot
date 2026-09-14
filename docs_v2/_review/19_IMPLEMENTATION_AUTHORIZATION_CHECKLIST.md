# Implementation Authorization Checklist

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Authorization invariants

Default deny: anything not explicitly authorized remains unauthorized. Authorization is exact-scope, exact-commit, non-transitive and non-widening. Documentation approval, switchover authorization, switchover acceptance, Phase-1 authorization, Phase-1 exit, Phase-2 authorization and capital authorization are different records.

No gate below is approved. `PENDING` is a documentary state, not an unchecked implicit approval.

## Review package identity

| Field | Current value |
|---|---|
| Candidate A SHA/tree | `PENDING — freeze after Phase 21; one canonical field only` |
| branch | `codex-docs` |
| review manifest | `_analysis/phase19_implementation_authorization/REVIEW_PACKAGE_MANIFEST.md` |
| traceability | Phase-18 certificate; delta recertification required for final Candidate A |
| human-policy count | derived from Candidate A Phase 14 (currently 2), never hard-coded |
| safety-invariant set | all applicable `SI-*` in Candidate A (currently derived 29), never hard-coded |

## Independent gates

| Gate | Decision | Required record/evidence | Current status |
|---|---|---|---|
| A — Review Package Completeness | package is internally complete and exact-snapshot traceable | manifest, cross-audit, non-stale Phase-18 certificate | PENDING |
| B — Documentation Approval | human accepts Candidate A as documentation baseline | reviewer/time/exact SHA/scope/decision | PENDING |
| C — Switchover Authorization | human permits procedural `docs_v2 -> docs` transformation | separate exact-scope record | PENDING |
| D — Canonical Switchover Acceptance | human accepts generated Commit B after manifest/diff/link/rollback proof | Commit A→B evidence and reviewer record | PENDING; Commit B absent |
| E — Phase 1 Implementation Authorization | human permits exact Phase-1 scope from accepted Commit B | AuthorizationRecord bound to Commit B SHA | PENDING |
| F — Phase 1 Exit | Phase-1 DoD evidence is accepted | versioned M1 report and deviations | NOT STARTED |
| G — Phase 2 Authorization | human separately permits Phase 2 after Gate F | new exact-scope AuthorizationRecord | PENDING / NOT IMPLIED |

Completing one row does not change any other row. No checkbox or blanket signature can cover multiple decision types.

## Human decisions, HDC and invariants

Phase 14 recomputes genuine human-policy families; Phase 19 consumes that result rather than “exactly eight.” Each applicable family receives its own scoped disposition. HDC-001..094 are a traced post-source requirements package, not 94 policy decisions and not blanket-approved through documentation acceptance; any per-item activation/promotion boundary remains governed by its owner.

The invariant review enumerates all applicable `SI-*` resolved from Candidate A. The current set contains 29, but the gate stores IDs/hash/count derived from the exact snapshot, not a permanent “29” assumption. Source no-loss is necessary evidence, not sufficient semantic approval.

## Phase 1 exact authorized scope

If Gate E is later approved, it may cover only strong domain/evidence IDs; typed price, quantity, notional and time units; event envelopes; schema/snapshot versions; deterministic ordering foundations; `Clock`; `RngProvider`; `RunManifest` foundations; serialization/compatibility; and unit/property/misuse tests.

Phase-1 DoD: strong units cannot mix; schemas round-trip and versions are explicit; invalid/incompatible/overflow inputs fail; hidden clock/randomness is absent; deterministic ordering foundations pass; and a versioned M1 evidence report exists.

Explicitly unauthorized: adapters/network/Hyperliquid parsing, books, formulas, opportunity/strategy, Risk behavior, execution transport/signing/effects, capital, deployment automation, Phase 2+, Shadow, Micro-live, Live, maker, Bridge, scaling, parameter search, Monte Carlo and any research runtime. Final-capable interfaces do not authorize future behavior.

## Blocking rule and external/calibration scope

An unresolved item blocks Phase 1 only if Phase 1 consumes it, no canonical conservative fallback exists, and proceeding would force semantic invention. Research/Future, Maker, Bridge, model, infra-ranking and capital questions remain non-blocking when independent. Phase-1 types assume no current exchange behavior; external facts gate their later consumers. Calibrated/learned values remain candidate evidence, not authorization.

## AuthorizationRecord

Required fields: record ID/version/type/status; exact authorized SHA and branch; authorized and explicitly excluded scope; prerequisites/evidence links; applicable SI IDs/hash; human-policy dispositions consumed; external freshness assumptions; start/stop conditions; required exit evidence; reviewer/role/time/signature; validity/supersession triggers; and next action. Allowed states: `PENDING`, `APPROVED_WITH_EXPLICIT_SCOPE`, `REJECTED`, `STALE`, `SUPERSEDED`.

An AuthorizationRecord cannot interpret itself beyond `authorized_scope`. A semantic commit/scope/invariant/traceability change makes affected approval stale. A proven-independent Research/Future edit need not invalidate Phase 1, but that independence must be recorded.

## Mandatory stop and later phases

After Phase 1 reaches its DoD, stop. Do not merge, start Phase 2, deploy or use capital. Gate F review and a new Gate-G authorization are required. Shared helpers created within Phase 1 cannot leak authorization to a Phase-2 consumer.

Implementation authorization never grants capital. Capital requires separately validated exact capability, readiness, Risk and a capital-specific authorization. Research documentation acceptance permits no research runtime. No automatic merge, branch creation, coding, switchover or deployment follows any documentation decision.
