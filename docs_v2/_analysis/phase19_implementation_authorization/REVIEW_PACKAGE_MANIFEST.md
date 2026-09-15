# Review Package Manifest

`STATUS: READY FOR HUMAN DOCUMENTATION REVIEW — NOT APPROVED`

## Semantic Candidate A identity

| Field | Exact value |
|---|---|
| semantic_candidate_A_sha | `4b1b2ea2a2cc179c01707ec6eed175fde898e808` |
| semantic_candidate_A_tree | `2b11be1bdcd4f1ac3382fe5683664cb5b432a96b` |
| branch | `codex-docs` |
| `docs_v2` tree | `6d5c9bb15425720450bd29ebe54c8d0d14e15c51` |
| `_review` tree | `f379e82ea05d121c600592dbde467024fdc612b9` |
| `_analysis` tree | `55761a52349e67f7de0665a6d9d667d155070fe5` |
| A file counts | `docs_v2=931`; `_review=22` including Start Here; `_analysis=676` |
| delta certificate | `_analysis/phase18_traceability/DELTA_RECERTIFICATION_CANDIDATE_A.md` |

Candidate A is the immutable semantic content snapshot. No review-package commit, attestation or later path move silently redefines A.

## Review Envelope C identity

| Field | Exact value |
|---|---|
| verified pre-alignment envelope/input HEAD | `b6c03d10867ccef180518424ffc311bfc8a55fa4` / tree `92d0b53070e749ac98877fafdb7ccd14f9af3ed8` |
| review_envelope_C_sha | `PENDING_POST_ALIGNMENT_FREEZE — populated by post-C identity attestation` |
| review_envelope_C_tree | `PENDING_POST_ALIGNMENT_FREEZE — populated by post-C identity attestation` |
| review_envelope_C_docs_v2_tree | `PENDING_POST_ALIGNMENT_FREEZE — populated by post-C identity attestation` |
| relationship | C attests immutable A and adds review/audit/governance metadata only; C does not redefine A |
| future_switchover_source | exact human-approved C |
| future_semantic_candidate | A |
| future Commit B | `ABSENT` |

The human documentation decision binds `semantic_candidate_sha=A` together with `review_package_sha=C`. The future Phase-20 transformation reads C:`docs_v2/**`, not A:`docs_v2/**`, so required post-A review and governance artifacts cannot disappear.

## Derived sets and evidence identities

| Set/artifact | Result |
|---|---|
| review passages | `01..21`: 21/21 present in the package; `00_REVIEW_START_HERE.md` is the additional entrypoint |
| supplied formal correction prompts | 17/17 executed sequentially for Phases 05–21; duplicated Phase 21 executed once |
| safety invariants | 29 unique IDs; normalized-ID SHA-256 `02fd8b6450535dd81cece48fec313c46b7210585ecd4ad9f7859497f2806b60d` |
| OPEN dispositions | 28/28; normalized expanded-ID SHA-256 `977b3f25e856e9c7ba6c4e6daee8889562277fef33123cc947aa18a1a74c8685` |
| HDC mapping | 94/94, 0 unmapped; normalized expanded-ID SHA-256 `f549a2e256aae09af8967fd993ddf86f70f968a8087ace8c02ce6ff7a2401e9d` |
| external revalidation | 23/23 unique EXT IDs; normalized-ID SHA-256 `c1e75a761154c2c8fc3256b275b088eee1330f271a4d0b851e25d71a722a99d6` |
| genuine human-policy families | 2, derived by Phase 14; C narrows HPD-01 to MT/MTT only without changing the count; not a permanent fixed count |
| source identity | 8/8 local SHA-256 matches at Phase 18 and Candidate-A recertification |

## Required review artifacts

- `_review/00_REVIEW_START_HERE.md` and review passages `01..21`;
- `_analysis/master_correction_run/MASTER_RUN_REPORT.md` and `PROMPT_COVERAGE.md`;
- `_analysis/master_correction_run/POST_RUN_GOVERNANCE_ALIGNMENT.md`;
- Phase-14 OPEN/HDC disposition ledgers;
- Phase-15 calibration and learned-item ledger;
- Phase-16 external revalidation checklist;
- Phase-17 scope audit;
- Phase-18 certificate and Candidate-A delta recertification;
- Phase-19 authorization gates, Phase-20 switchover procedure and Phase-21 decision form;
- all applicable `SI-*` enumerated in Candidate A.

Mechanical completeness is `PASS`; human Gate-A confirmation remains `PENDING`. Gate B is the only currently decision-eligible authorization gate. Documentation approval is pending; switchover authorization/acceptance and Phase-1/Phase-2 authorization are `NOT_AVAILABLE`; implementation is `NOT_STARTED`/`NOT_AUTHORIZED`; research runtime, deployment and real capital remain unauthorized.
