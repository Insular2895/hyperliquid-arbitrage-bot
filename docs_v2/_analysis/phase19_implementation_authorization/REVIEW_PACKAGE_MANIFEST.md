# Review Package Manifest

`STATUS: READY FOR HUMAN DOCUMENTATION REVIEW — NOT APPROVED`

## Final Review Candidate F2 identity contract

| Field | Value / rule |
|---|---|
| candidate | complete Prompt-3 `docs_v2` corpus selected as Final Review Candidate F2 |
| subject_commit_sha | exact F2 commit selected and recorded externally by the human `DocumentationDecision` / `ReviewRecord` |
| subject_tree_sha | corresponding exact F2 tree recorded by the same record |
| branch | `f2-governance-p3` |
| current identity rule | exact immutable commit from the applicable DecisionRecord; never moving HEAD or latest branch tip |
| self-reference rule | F2 never embeds or requires its own future commit/tree identity; no post-F2 attestation commit is needed |
| traceability | historical Phase-18 certificate plus A/C/F and F2 Prompt-1/2/3 L3/L4 lineage; `DELTA_RECERTIFICATION_REQUIRED` |
| future_switchover_source | exact human-reviewed and approved F2 |
| future Commit B | `ABSENT` |

The Git object selected at review time supplies immutable physical identity. The documentation supplies the identity contract. Recording `subject_commit_sha=F2` and `subject_tree_sha=F2 tree` after F2 exists does not mutate F2.

## Historical / superseded review-package lineage

| Historical identity | Exact value / classification |
|---|---|
| Semantic Candidate A | `4b1b2ea2a2cc179c01707ec6eed175fde898e808` / tree `2b11be1bdcd4f1ac3382fe5683664cb5b432a96b` |
| first aligned envelope / attestation | `fd2bca5b4a16263723692d2a9c6536235577af69` / `bf5fa0e13ff4b0cc4f3107b94c1e728fc6096efa` |
| Review Envelope C | `65c03b2c2f6dd131a045810f71c9e1aa5c3cf269` / tree `c6588a09465dca730f39646bec08231eb7df7ede` / `docs_v2` tree `59d67e253380a23d3470747caf257402040d9863` |
| post-C attestation child | `6812b53ed087129582795beb1ed9239c58d0c050` |
| Final Review Candidate F baseline | `180c41cfcc9c200a2b0afa5a94b8f0e5f6f522da` |
| F2 Prompt 1 / correction | `46ecd4f52cf553332f7879b40d5f285b370f4d91` / `3cce15a8d3ee36a20d3b729cf1e49fc676bfa3b5` |
| F2 Prompt 2 / correction | `197a3a9a672a55c7026b9000301dd88de91e2055` / `994089985e04a8ed66f8a9ebbe05cc3a23e61909` |
| current classification | `HISTORICAL / SUPERSEDED REVIEW-PACKAGE LINEAGE` |

A/C/post-C/F and F2 Prompt-1/2 explain how F2 was reached and remain valid audit evidence. They are not the active review subject, future switchover source or Phase-1 authorization source. The later semantic additions mean F2 cannot be represented as F plus external metadata alone.

## Derived sets and evidence identities

| Set/artifact | Result |
|---|---|
| review passages | `01..21`: 21/21 present in the package; `00_REVIEW_START_HERE.md` is the additional entrypoint |
| supplied formal correction prompts | 17/17 executed sequentially for Phases 05–21; duplicated Phase 21 executed once |
| safety invariants | 29 unique IDs; SI-022 wording is aligned to QF-076 without adding/removing an ID; normalized ID-list SHA-256 `02fd8b6450535dd81cece48fec313c46b7210585ecd4ad9f7859497f2806b60d` |
| OPEN dispositions | 28/28; normalized expanded-ID SHA-256 `977b3f25e856e9c7ba6c4e6daee8889562277fef33123cc947aa18a1a74c8685` |
| HDC mapping | historical 94/94 preserved; proposed F2 inventory 100/100 sequential with `HDC-095..100` overlay; normalized ID-list SHA-256 `8ec95ddaf6be694de77f9ef6fe84f142e96db58f8f1fa11d77a4f8b6a5254014` |
| external revalidation | 23/23 unique EXT IDs; normalized-ID SHA-256 `c1e75a761154c2c8fc3256b275b088eee1330f271a4d0b851e25d71a722a99d6` |
| genuine human-policy families | 2, derived by Phase 14; HPD-01 is MT/MTT-only; not a permanent fixed count |
| source identity | 8/8 local SHA-256 matches at Phase 18 and Candidate-A recertification |

## Required review artifacts

- `_review/00_REVIEW_START_HERE.md` and review passages `01..21`;
- `_analysis/master_correction_run/MASTER_RUN_REPORT.md` and `PROMPT_COVERAGE.md`;
- `_analysis/master_correction_run/POST_RUN_GOVERNANCE_ALIGNMENT.md`;
- Phase-14 OPEN/HDC disposition ledgers;
- Phase-15 calibration and learned-item ledger;
- Phase-16 external revalidation checklist;
- Phase-17 scope audit;
- Phase-18 certificate, historical Candidate-A delta recertification and final-corpus lineage;
- Phase-19 authorization gates, Phase-20 switchover procedure and Phase-21 decision form;
- `_analysis/f2_final_integration/` matrices, crosswalk, five-map atlas, non-regression audit and handoff;
- all applicable `SI-*` enumerated in exact F2.

Mechanical completeness is `PASS`; human Gate-A confirmation remains `PENDING`.
`DELTA_RECERTIFICATION_REQUIRED` does not by itself block mechanical package completeness, but it
blocks a fully recertified F2 claim. Gate B is the only currently decision-eligible authorization
gate. Documentation approval must record exact F2 externally. Switchover authorization/acceptance
and Phase-1/Phase-2 authorization are `NOT_AVAILABLE`; implementation is
`NOT_STARTED`/`NOT_AUTHORIZED`; research runtime, deployment and real capital remain unauthorized.
