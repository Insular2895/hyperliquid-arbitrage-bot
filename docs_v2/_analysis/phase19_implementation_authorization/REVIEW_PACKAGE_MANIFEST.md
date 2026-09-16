# Review Package Manifest

`STATUS: READY FOR HUMAN DOCUMENTATION REVIEW — NOT APPROVED`

## Final Review Candidate F identity contract

| Field | Value / rule |
|---|---|
| candidate | complete final corrected `docs_v2` corpus selected as Final Review Candidate F |
| subject_commit_sha | exact F commit selected and recorded externally by the human `DocumentationDecision` / `ReviewRecord` |
| subject_tree_sha | corresponding exact F tree recorded by the same record |
| branch | `codex-docs` |
| current identity rule | exact immutable commit from the applicable DecisionRecord; never moving HEAD or latest branch tip |
| self-reference rule | F never embeds or requires its own commit/tree identity; no post-F attestation commit is needed |
| traceability | Phase-18 certificate plus historical A/C and later classified L3/L4 lineage through F |
| future_switchover_source | exact human-reviewed and approved F |
| future Commit B | `ABSENT` |

The Git object selected at review time supplies immutable physical identity. The documentation supplies the identity contract. Recording `subject_commit_sha=F` and `subject_tree_sha=F tree` after F exists does not mutate F.

## Historical / superseded review-package lineage

| Historical identity | Exact value / classification |
|---|---|
| Semantic Candidate A | `4b1b2ea2a2cc179c01707ec6eed175fde898e808` / tree `2b11be1bdcd4f1ac3382fe5683664cb5b432a96b` |
| first aligned envelope / attestation | `fd2bca5b4a16263723692d2a9c6536235577af69` / `bf5fa0e13ff4b0cc4f3107b94c1e728fc6096efa` |
| Review Envelope C | `65c03b2c2f6dd131a045810f71c9e1aa5c3cf269` / tree `c6588a09465dca730f39646bec08231eb7df7ede` / `docs_v2` tree `59d67e253380a23d3470747caf257402040d9863` |
| post-C attestation child | `6812b53ed087129582795beb1ed9239c58d0c050` |
| current classification | `HISTORICAL / SUPERSEDED REVIEW-PACKAGE LINEAGE` |

A/C/post-C explain how F was reached and remain valid audit evidence. They are not the active review subject, future switchover source or Phase-1 authorization source. The post-master-run corrections changed current normative review/governance wording, so the final corpus cannot be represented as A plus external metadata alone.

## Derived sets and evidence identities

| Set/artifact | Result |
|---|---|
| review passages | `01..21`: 21/21 present in the package; `00_REVIEW_START_HERE.md` is the additional entrypoint |
| supplied formal correction prompts | 17/17 executed sequentially for Phases 05–21; duplicated Phase 21 executed once |
| safety invariants | 29 unique IDs; SI-022 wording is aligned to QF-076 without adding/removing an ID; normalized ID-list SHA-256 `02fd8b6450535dd81cece48fec313c46b7210585ecd4ad9f7859497f2806b60d` |
| OPEN dispositions | 28/28; normalized expanded-ID SHA-256 `977b3f25e856e9c7ba6c4e6daee8889562277fef33123cc947aa18a1a74c8685` |
| HDC mapping | 94/94, 0 unmapped; normalized expanded-ID SHA-256 `f549a2e256aae09af8967fd993ddf86f70f968a8087ace8c02ce6ff7a2401e9d` |
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
- all applicable `SI-*` enumerated in exact F.

Mechanical completeness is `PASS`; human Gate-A confirmation remains `PENDING`. Gate B is the only currently decision-eligible authorization gate. Documentation approval must record exact F externally. Switchover authorization/acceptance and Phase-1/Phase-2 authorization are `NOT_AVAILABLE`; implementation is `NOT_STARTED`/`NOT_AUTHORIZED`; research runtime, deployment and real capital remain unauthorized.
