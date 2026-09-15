# Final Human Decision Form

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Purpose and decision invariants

This form records decisions; it executes none. `DEFAULT STATE = NOT_AUTHORIZED`. Anything without a valid, scope-specific, non-stale DecisionRecord remains not authorized. Decisions are mutually exclusive, exact-commit, non-transitive and non-widening.

## Stage 0 — Review Package Identity

| Field | Value / status |
|---|---|
| Semantic Candidate A SHA/tree | `4b1b2ea2a2cc179c01707ec6eed175fde898e808` / `2b11be1bdcd4f1ac3382fe5683664cb5b432a96b` on `codex-docs`; immutable semantic content |
| Review Envelope C SHA/tree | `65c03b2c2f6dd131a045810f71c9e1aa5c3cf269` / `c6588a09465dca730f39646bec08231eb7df7ede`; never moving HEAD |
| Review Envelope C `docs_v2` tree | `59d67e253380a23d3470747caf257402040d9863`; future switchover source |
| Review Package Manifest | [exact A/C relationship and package](../_analysis/phase19_implementation_authorization/REVIEW_PACKAGE_MANIFEST.md) |
| Phase-18 delta certificate for A | `PRESENT` — [Candidate-A recertification](../_analysis/phase18_traceability/DELTA_RECERTIFICATION_CANDIDATE_A.md) |
| post-freeze attestation status | `A ATTESTED BY C; EXACT C IDENTITY RECORDED BY SEPARATE POST-C ATTESTATION; NOT HUMAN APPROVED` |
| review package completeness | `MECHANICAL CHECK PASS — HUMAN CONFIRMATION PENDING` |
| reviewer / date | `PENDING` |

The exact A/C relationship, manifest and non-stale lineage are mechanically verified. Human review is of semantic content A together with review/governance envelope C. No later authorization stage is available until the human records Stage 1.

## Stage 1 — Documentation Decision

Prerequisite: Stage 0 mechanically complete. Current status: `PENDING`. Choose exactly one in a future DecisionRecord bound to exact A+C:

- `APPROVE(A,C)`;
- `REQUEST_CHANGES(A,C)` — semantic change creates A2+C2; governance-only change creates C2 attesting unchanged A; restart review;
- `REJECT(A,C)`.

There is no “approve with changes.” Documentation approval triggers no switchover, merge, branch, implementation, research or capital action.

## Stage 2 — Genuine Human Policy Decisions

Consume the derived Phase-14 registry, never a fixed HD-01..08 list. Current registry has two genuine scoped families:

| Decision | Blocking scope | Allowed future disposition | Current status |
|---|---|---|---|
| HPD-01 MT/MTT maker-mode activation | Phase 23 bounded MT/MTT maker probe only; not Phase 1, TT/TTT or TM/MM | APPROVE eligible exact MT/MTT scope / NARROW / DEFER / REJECT / REQUEST_EVIDENCE | PENDING POLICY REVIEW; NO CAPABILITY AUTHORITY |
| HPD-02 license/product mechanism | client distribution only | APPROVE eligible mechanism / NARROW / DEFER / REJECT / REQUEST_EVIDENCE | PENDING |

Evidence selects calibrated/learned candidates; policy approval cannot override failed evidence/Risk/OOD/q. Non-blocking Research/Future and deferred Formula/Sizing/Model/Infra/Capital items may remain open when Phase 1 does not consume them.

These HPD rows are policy-review dispositions, not later authorization-gate availability. Among the sequential authorization Gates B–G, only documentation Gate B is currently `PENDING`.

TM/MM are `FUTURE`, outside the current 26-phase activation roadmap and outside HPD-01. Enum/type compatibility means only representable; it does not mean implemented, validated or authorized. TM/MM require a separate future product/safety/evidence specification and approval chain.

`HDC-001..094` is a traced post-source requirement package, not 94 Human Policy Decisions and not one blanket approval. CORR-01..06, scientific and async extensions are review-package components with their own lineage; accepting documentation does not activate their capabilities.

## Stage 3 — Switchover Authorization

Prerequisite: `DocumentationDecision(A,C)=APPROVED`. Current status: `NOT_AVAILABLE`.

Future mutually exclusive decision: `AUTHORIZE_SWITCHOVER(C, semantic_candidate=A)` or `DO_NOT_AUTHORIZE_SWITCHOVER(C,A)`. The record must freeze the approved C artifact manifest, allowed transformations and `_analysis`/`_review` retention policy. Proposed retention is both directories; semantic change creates A2+C2, while governance-only change creates C2; either requires new documentation review.

`SwitchoverAuthorization(C,A) != MergeAuthorization` and does not accept unknown output B or authorize Phase 1.

## Stage 4 — Switchover Result

Prerequisite: Stage 3 authorized and Phase-20 procedure executed. Current status: `NOT_AVAILABLE`; Commit B does not exist.

Future machine/human-prepared evidence records exact B SHA/tree, C→B SwitchoverRecord carrying semantic identity A, normalized artifact/link manifests, semantic-equivalence result, Phase-18 lineage recertification and push ref. No false B SHA is entered now.

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
| MT/MTT | NOT_AUTHORIZED — Later V1 Phase 23 only after HPD-01 and all evidence gates |
| TM/MM | NOT_AUTHORIZED — FUTURE; outside HPD-01 and the current 26-phase activation roadmap |
| Bridge | NOT_AUTHORIZED |
| Scaling / q expansion | NOT_AUTHORIZED |
| Strategy Discovery / Parameter Search / Monte Carlo | NOT_AUTHORIZED |
| model/strategy Champion activation or drift automation | NOT_AUTHORIZED |
| real capital / exchange effects | NOT_AUTHORIZED |
| `docs_v2 -> docs` switchover | NOT_AUTHORIZED / UNEXECUTED |

An empty or unchecked field never means “maybe allowed.” Research documentation promoted to canonical docs is not Research capability authorization. External facts remain freshness-gated per consumer.

## Stage 8 — Decision Status and Supersession

Decision states are `PENDING`, `APPROVED_WITH_EXPLICIT_SCOPE`, `REQUEST_CHANGES`, `REJECTED`, `NOT_AVAILABLE`, `STALE` and `SUPERSEDED`; execution/evidence stages may be `NOT_STARTED`, and capability permission remains `NOT_AUTHORIZED`. Every DecisionRecord includes ID/type/version/status, exact applicable A/C/B commit/tree identities, explicit scope/exclusions, prerequisites/evidence/certificate/manifest links, blocker disposition, reviewer/role/date, validity triggers and supersession lineage.

Semantic change to A, package/governance change to C, or change to approved scope, applicable invariant or certificate makes the affected record `STALE`. A replacement `SUPERSEDES` rather than rewriting history. No decision auto-propagates to the next stage.

## Final status summary

```text
SemanticCandidateA: EXACT / IMMUTABLE
ReviewEnvelopeC: EXACT IDENTITY RECORDED BY POST-C ATTESTATION
ReviewPackageIdentity: A+C MECHANICALLY COMPLETE / HUMAN CONFIRMATION PENDING
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
