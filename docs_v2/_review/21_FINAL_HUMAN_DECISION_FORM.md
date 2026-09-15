# Final Human Decision Form

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Purpose and decision invariants

This form records decisions; it executes none. `DEFAULT STATE = NOT_AUTHORIZED`. Anything without a valid, scope-specific, non-stale DecisionRecord remains not authorized. Decisions are mutually exclusive, exact-commit, non-transitive and non-widening.

## Stage 0 — Review Package Identity

| Field | Value / status |
|---|---|
| Candidate commit A | `4b1b2ea2a2cc179c01707ec6eed175fde898e808` on `codex-docs` — immutable content snapshot, never moving HEAD |
| Candidate tree / manifest | tree `2b11be1bdcd4f1ac3382fe5683664cb5b432a96b`; [review manifest](../_analysis/phase19_implementation_authorization/REVIEW_PACKAGE_MANIFEST.md) |
| Phase-18 delta certificate for A | `PRESENT` — [Candidate-A recertification](../_analysis/phase18_traceability/DELTA_RECERTIFICATION_CANDIDATE_A.md) |
| review package completeness | `MECHANICAL CHECK PASS — HUMAN CONFIRMATION PENDING` |
| reviewer / date | `PENDING` |

The exact A/tree/manifest and non-stale certificate are mechanically verified. No later stage is available until a human confirms Stage 0 and records Stage 1.

## Stage 1 — Documentation Decision

Prerequisite: Stage 0 complete. Current status: `PENDING` once Stage 0 is complete. Choose exactly one in a future DecisionRecord:

- `APPROVE(A)`;
- `REQUEST_CHANGES(A)` — A is not approved; create A2 and restart review;
- `REJECT(A)`.

There is no “approve with changes.” Documentation approval triggers no switchover, merge, branch, implementation, research or capital action.

## Stage 2 — Genuine Human Policy Decisions

Consume the derived Phase-14 registry, never a fixed HD-01..08 list. Current registry has two genuine scoped families:

| Decision | Blocking scope | Allowed future disposition | Current status |
|---|---|---|---|
| HPD-01 Maker/TM/MM activation | Phase 23/maker only; not Phase 1 or conservative TT | APPROVE eligible exact scope / NARROW / DEFER / REJECT / REQUEST_EVIDENCE | PENDING |
| HPD-02 license/product mechanism | client distribution only | APPROVE eligible mechanism / NARROW / DEFER / REJECT / REQUEST_EVIDENCE | PENDING |

Evidence selects calibrated/learned candidates; policy approval cannot override failed evidence/Risk/OOD/q. Non-blocking Research/Future and deferred Formula/Sizing/Model/Infra/Capital items may remain open when Phase 1 does not consume them.

`HDC-001..094` is a traced post-source requirement package, not 94 Human Policy Decisions and not one blanket approval. CORR-01..06, scientific and async extensions are review-package components with their own lineage; accepting documentation does not activate their capabilities.

## Stage 3 — Switchover Authorization

Prerequisite: `DocumentationDecision(A)=APPROVED`. Current status: `NOT_AVAILABLE`.

Future mutually exclusive decision: `AUTHORIZE_SWITCHOVER(A)` or `DO_NOT_AUTHORIZE(A)`. The record must freeze the approved artifact manifest, allowed transformations and `_analysis`/`_review` retention policy. Proposed retention is both directories; any change creates A2 and new documentation review.

`SwitchoverAuthorization(A) != MergeAuthorization` and does not accept unknown output B or authorize Phase 1.

## Stage 4 — Switchover Result

Prerequisite: Stage 3 authorized and Phase-20 procedure executed. Current status: `NOT_AVAILABLE`; Commit B does not exist.

Future machine/human-prepared evidence records exact B SHA/tree, A→B SwitchoverRecord, normalized artifact/link manifests, semantic-equivalence result, Phase-18 delta recertification and push ref. No false B SHA is entered now.

## Stage 5 — Switchover Acceptance

Prerequisites: B exists; every Phase-20 validation passes; B is pushed/reviewable. Current status: `NOT_AVAILABLE`.

Future mutually exclusive decision: `ACCEPT(B)`, `REQUEST_CHANGES(B)` or `REJECT(B)`. Successful transformation/push is not acceptance. Acceptance is distinct from any Git merge mechanism and does not start implementation.

## Stage 6 — Phase 1 Authorization

Prerequisite: `SwitchoverAcceptance(B)=ACCEPTED`. Current status: `NOT_AVAILABLE`.

Future mutually exclusive decision: `AUTHORIZE_PHASE1(B, exact_scope)` or `DO_NOT_AUTHORIZE_PHASE1(B)`. The branch may be created only from exact B after this record.

Exact possible scope: strong IDs/units; event envelopes; schema/snapshot versions; deterministic ordering foundations; Clock/RNG/RunManifest foundations; serialization/compatibility; unit/property/misuse tests. It excludes network/adapters, books, Formula implementation, opportunity/strategy, Risk behavior, order transport/signing/effects, capital, deployment and Phase 2+. After Phase-1 DoD, STOP; Phase 2 requires a new authorization.

## Stage 7 — Explicit Non-Authorizations

| Scope | Current status |
|---|---|
| Phase 1 | NOT_AUTHORIZED / prerequisite unavailable |
| Phase 2+ | NOT_AUTHORIZED |
| Shadow | NOT_AUTHORIZED |
| Micro-live | NOT_AUTHORIZED |
| Live | NOT_AUTHORIZED |
| MT/MTT/TM/MM | NOT_AUTHORIZED |
| Bridge | NOT_AUTHORIZED |
| Scaling / q expansion | NOT_AUTHORIZED |
| Strategy Discovery / Parameter Search / Monte Carlo | NOT_AUTHORIZED |
| model/strategy Champion activation or drift automation | NOT_AUTHORIZED |
| real capital / exchange effects | NOT_AUTHORIZED |
| `docs_v2 -> docs` switchover | NOT_AUTHORIZED / UNEXECUTED |

An empty or unchecked field never means “maybe allowed.” Research documentation promoted to canonical docs is not Research capability authorization. External facts remain freshness-gated per consumer.

## Stage 8 — Decision Status and Supersession

Decision states are `PENDING`, `APPROVED_WITH_EXPLICIT_SCOPE`, `REQUEST_CHANGES`, `REJECTED`, `NOT_AVAILABLE`, `STALE` and `SUPERSEDED`. Every DecisionRecord includes ID/type/version/status, exact commit/tree, explicit scope/exclusions, prerequisites/evidence/certificate/manifest links, blocker disposition, reviewer/role/date, validity triggers and supersession lineage.

Semantic change to the approved commit, scope, applicable invariant or certificate makes the affected record `STALE`. A replacement `SUPERSEDES` rather than rewriting history. No decision auto-propagates to the next stage.

## Final status summary

```text
ReviewPackageIdentity: EXACT CANDIDATE RECORDED / HUMAN CONFIRMATION PENDING
DocumentationDecision: PENDING
HumanPolicyDecisions: PENDING / MAY BE DEFERRED BY SCOPE
SwitchoverAuthorization: NOT_AVAILABLE
SwitchoverResultB: NOT_AVAILABLE
SwitchoverAcceptance: NOT_AVAILABLE
Phase1Authorization: NOT_AVAILABLE
Implementation: NOT_STARTED
ResearchRuntime: NOT_AUTHORIZED
RealCapital: NOT_AUTHORIZED
```
