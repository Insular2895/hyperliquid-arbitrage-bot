# Final Switchover Plan

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Purpose and authority boundary

This is a deterministic future procedure only. Phase 19 owns permission; Phase 20 owns procedure and cannot self-authorize or widen scope. No move, deletion, branch, merge, switchover commit, Phase-1 branch or code action has occurred.

## Semantic A / Review Envelope C / future B model

| Identity | Meaning | Current state |
|---|---|---|
| Semantic Candidate A | immutable corrected semantic documentation content | `4b1b2ea2a2cc179c01707ec6eed175fde898e808` / tree `2b11be1bdcd4f1ac3382fe5683664cb5b432a96b` |
| Review Envelope C | exact post-run package that attests A and adds review/audit/governance metadata without new production semantics | exact post-alignment SHA/tree/`docs_v2` tree recorded by the post-C attestation and review manifest |
| Commit B | separate future canonical-path result transformed from exact approved C while retaining semantic identity A | `ABSENT` |

The verified pre-alignment envelope was `b6c03d10867ccef180518424ffc311bfc8a55fa4` / tree `92d0b53070e749ac98877fafdb7ccd14f9af3ed8`. It is historical input to this correction, not moving authority and not the final aligned C.

Target chain:

```text
Semantic Candidate A frozen
 -> exact Review Envelope C attests A
 -> DocumentationApproval(A,C)
 -> SwitchoverAuthorization(C, semantic_candidate=A)
 -> deterministic path-only transformation
 -> Commit B + SwitchoverRecord(C,B; semantic_candidate=A)
 -> push for review (not merge)
 -> SwitchoverAcceptance(B)
 -> STOP
 -> separate Phase1Authorization(B), if later granted
```

Phase 1 is not decided before B exists and is accepted. Acceptance of B does not start coding.

## Preconditions and input identities

Require valid Phase-19 Gates A–C; exact reachable A and C SHA/tree identities; a non-stale Phase-18 Candidate-A certificate plus A→C L3/L4 package lineage; `DocumentationApproval(A,C)`; an `ApprovedDocumentationManifest`; explicit `_analysis`/`_review` retention policy; a clean isolated worktree created at C; allowed-path policy; and recorded pre-state branch/HEAD/status plus C:`docs`, C:`docs_v2` trees/inventories/hashes. Any dirty/unrelated file, missing identity or mismatch is STOP, not “acknowledged.”

The proposed retention policy is `RETAIN _analysis AND _review` because they carry source lineage, OPEN/HDC/EXT dispositions, certificates and authorization evidence. It has no authority until explicitly included in the approved manifest. A governance-only policy change creates C2 attesting unchanged A and requires review; it is never decided during migration.

## Approved transformation and paths

Only:

1. preserve legacy `docs` in an uncommitted unique temporary recovery path;
2. materialize C:`docs_v2/**` as B:`docs/**` so the approved A semantics and C review/governance additions are both retained;
3. apply only manifest-approved relative path/link rewrites caused by this root move;
4. preserve `_analysis`, `_review`, source timestamps and historical provenance according to the approved retention policy;
5. remove the temporary legacy copy only after every validation passes, relying on recorded Git pre-state for recovery.

The B diff may affect only `docs/**` and `docs_v2/**`. No source code, Cargo, Docker, CI, runtime config, tests or semantic documentation edits are allowed. Historical prose mentioning `docs_v2` remains when it describes chronology; only resolvable path/link targets listed in `LinkRewriteManifest` change. Ambiguity is STOP and requires C2 review; any necessary semantic change additionally creates A2.

## Deterministic execution sequence

1. Verify `SwitchoverAuthorization(C, semantic_candidate=A)` and exact approved A+C review package.
2. Create a clean isolated worktree at C and record repository/pre-state identities.
3. Load approved artifact manifest, retention and allowed-path policies.
4. Verify C:`docs_v2` inventory/hashes, C's attested relationship to A and the legacy `docs` tree/hash.
5. Preserve legacy docs at a unique temporary local recovery path.
6. Materialize `docs_v2 -> docs` without semantic editing.
7. Generate and apply only the preclassified `LinkRewriteManifest` mappings.
8. Generate B-side normalized artifact inventory; require set/hash equality after approved path normalization.
9. Run Markdown/referenced-file checks and classify every remaining `docs_v2` occurrence.
10. Compute normalized semantic diff: strip only approved root/link substitutions, compare every file byte/content, list/classify every residual difference, fail on anything not allowlisted.
11. Run Phase-18 lineage recertification mapping A source/traceability evidence through C to B paths.
12. Generate `SwitchoverRecord` with A/C/B identities, manifests, checks and zero-semantic-drift result.
13. Remove temporary legacy tree only after all checks pass.
14. Create separate Commit B; push its branch for human review without merging.
15. Obtain explicit `SwitchoverAcceptance(B)` or reject.
16. If accepted, mark B as canonical baseline and STOP.
17. Phase 1 still requires separate `Phase1Authorization(B)` and a branch based exactly on B.

Counts are diagnostics; the ApprovedDocumentationManifest is primary. Missing file/link, count/tree/hash mismatch, unclassified diff, certificate failure, unreachable A or changed A causes STOP.

## Manifest and semantic-equivalence evidence

- `ApprovedDocumentationManifest`: semantic A SHA/tree, exact review-envelope C SHA/tree/`docs_v2` tree, A→C relationship, every approved C artifact path/hash/class, required review/analysis retention, expected normalized B path, allowed transformations and reviewer decision.
- `LinkRewriteManifest`: source file, old target, new target, reason, transformation class, ambiguity result and verification.
- normalized equivalence: C:`docs_v2/<p>` must equal B:`docs/<p>` after only approved path substitutions; no wording/number/status/authority change. The check separately preserves A semantic content and C-only attestation/governance additions.
- Phase-18 lineage: source hashes may remain L0-equal, but A→C→B L2/L3/L4 path, package and certificate identities must be recertified.
- `SwitchoverRecord`: exact C→B transformation with semantic candidate A retained, pre/post trees/manifests, all checks, author/time, deviations, push ref and acceptance status.

## Push, acceptance, rejection and rollback

Push != merge; successful checks != acceptance; B push != canonical baseline. Before merge/integration, rejection abandons the candidate branch and leaves canonical state unchanged—no revert commit is needed. After integration, rollback restores the exact recorded pre-state (normally by reverting B under review), regenerates/verifies links/manifests/certificate, and never “reconciles links” freely. Exchange truth is unaffected because this is documentation only.

Any semantic correction after A+C approval creates A2 and C2; a governance-only package correction creates C2 attesting unchanged A. Either makes affected approvals stale and restarts review. Nothing is smuggled into B.

## Post-acceptance boundary

Even an accepted B authorizes no implementation, deployment, research runtime, external refresh, capital, Micro-live, Live or exchange effect. Phase 1, if separately authorized, is based exactly on B and stops at its own DoD before Phase 2.
