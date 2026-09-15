# Source and Traceability Certificate

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Purpose, scope and snapshot

This point-in-time certificate attests physical identity, extraction coverage and canonical destination mapping of the eight original sources. It does not certify semantic correctness, current external facts, human acceptance, implementation, safety, profitability or permission.

| Snapshot field | Value |
|---|---|
| certified commit | `caaa251ada6ad6344de48c318c82913269af02f4` |
| certified tree | `4375c50f2be2f81ed04175150c7a94e29cc59f3f` |
| branch | `codex-docs` |
| generated_at | `2026-09-14` |
| certification basis | PASS00 extraction + PASS15 source no-loss recovery |

The certificate is generated after that immutable input snapshot and references it exactly. Phase-18 and later governance edits are L3 overlays outside this certified tree until a later delta recertification. `CERTIFIED AT SNAPSHOT != CURRENT FOREVER`.

## Certification layers

| Layer | Meaning | Current result |
|---|---|---|
| L0 Physical Source Identity | filename/bytes/lines/SHA-256 of original files | 8/8 hash match |
| L1 Source Extraction Coverage | source intervals/items accounted | PASS00 2,577/2,577 plus disclosed PASS15 recovery |
| L2 Canonical Requirement Mapping | each source item has destination/disposition | 2,590/2,590 destinations; 0 destinationless |
| L3 Post-source overlays | CORR/HDC/EXT/research/async/Phase14–17 refinements with honest provenance | present, not attributed to SRC-001..008 |
| L4 Human review/authorization | documentation approval and implementation/capital decisions | pending / not authorized |

Only L0–L2 support `NO-LOSS VERIFIED`. L3 has its own lineage; L4 is not certified by traceability.

## Physical source identity

Recomputed locally during this correction; all values match `SOURCE_INVENTORY.md`.

| Source | Original filename | Lines | SHA-256 | Result |
|---|---|---:|---|---|
| SRC-001 | `23. Lock-free  ring buffers  zero-copy.md` | 5,255 | `061043598486f7e4fa357e681dfb67e909989945be0b8c82e1070cb7ff559921` | MATCH |
| SRC-002 | `Bot hyperliquid .md` | 6,077 | `d99b2b9354ba39e74dd616206b63bd0a5442be558f78c47c88dea733f056d4a1` | MATCH |
| SRC-003 | `Concrètement, en production on doit garder au moins .md` | 4,272 | `7065fc0dcacbcf87212c3ca0dd9cb204aee347a1984bb85757033aeeade6270a` | MATCH |
| SRC-004 | `DOSSIER 16 — EXECUTION STATE MACHINE.md` | 9,953 | `df5b1720a26889fce2a74fbc380bad4bda2e2aacdb4f02054c7270e5eb04b5b9` | MATCH |
| SRC-005 | `DOSSIER 36 — RISK CONSTITUTION V1.md` | 9,877 | `798a0f60a14397926505b470aeee5ded11507c04c6bb489a4b1f5fe950ecd66f` | MATCH |
| SRC-006 | `DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT.md` | 6,903 | `a535a5fa04feaaf4056ab7b3880f8cbcb803a6b1300d25ed02c96aa14558115d` | MATCH |
| SRC-007 | `Oui, dans le modèle qu’on vient de définir, le plus propre est que….md` | 12,371 | `df2e94843df1e4a28bec4699bf89c9d2f2b8faa91763b3d3e78bff05e8369490` | MATCH |
| SRC-008 | `Oui. Et en creusant le sujet, je corrigerais une chose fondamentale….md` | 6,937 | `8b7924d664bd718e324bc3d7f50f0a461244b2638a69d7601caf132d8a849f50` | MATCH |

Source inventory is evidence for physical identity only, not architecture meaning, implementation scope or current exchange behavior.

## Coverage and count semantics

- `2,577`: historical PASS00 atomic source items, all traced.
- `2,590`: stable final destination rows: the 2,577 source items plus 13 explicit cross-domain anchors. This is a mapping denominator, not a new source count.
- `79`: PASS15 recovered concepts—2 intervals outside initial extraction plus 77 independently implementable concepts hidden in six over-broad ranges. They are disclosed in recovery artifacts and not retroactively inserted into historical PASS00 IDs or silently added to the 2,590 denominator.
- `110`: QF-001..110 are source-covered; source coverage is not mathematical/runtime validation.

`NO-LOSS VERIFIED` means every original source interval/atomic obligation has a traceable extracted representation and canonical destination/disposition, with PASS15 recovery disclosed and zero missing/destinationless source requirement. It does not mean every architecture interpretation is correct, every current document is forever fresh, or every OPEN is closed.

Fixing one canonical overcompression and six PASS00 atomicity/destination issues restored extraction/mapping granularity; it did not create architectural decisions. “No new decisions” applies only to PASS15 source recovery, not later CORR/HDC/external/research overlays.

## Destination mapping and artifact identities

`DOCUMENT_TARGET_MAP` owns source requirement → destination/disposition. `FINAL_SOURCE_ITEM_TRACEABILITY.csv` is the row-level evidence and is not replaced by this summary. Critical artifact SHA-256 identities at the certified snapshot are listed in the [artifact manifest](../_analysis/phase18_traceability/CERTIFIED_ARTIFACT_MANIFEST.md). Any semantic change to target mapping/ledger/traceability requires L2 delta recertification even when source hashes remain identical.

## Post-source overlays, OPEN and external facts

HDC-001..094, CORR passes, async/scientific extensions and external refreshes remain L3 with their actual provenance. They do not become original-source statements. OPEN is classified by Phase 14 and is not synonymous with human decision. External fact snapshots are dated evidence outside L0–L2 and require consumer-specific revalidation.

## Staleness and recertification

Status is `CERTIFIED_AT_SNAPSHOT`, `DELTA_RECERTIFICATION_REQUIRED` after semantic mapping/authority/count/destination changes, or `SUPERSEDED` by a later certificate. Editorial changes that do not alter meaning may be logged without redoing L0/L1; L2 changes require affected-row plus invariant recertification. Source-file changes require L0 onward. Denominators 2,577/2,590/79/110 never change silently.

Future corrections supersede through lineage; they do not rewrite PASS00/PASS15 history. A current certificate always binds exact commit/tree, artifact hashes and generation time.

## Candidate-A delta status

The [Candidate-A delta recertification](../_analysis/phase18_traceability/DELTA_RECERTIFICATION_CANDIDATE_A.md) binds Semantic Candidate A at `4b1b2ea2a2cc179c01707ec6eed175fde898e808`. It confirms unchanged L0 source identities and unchanged critical extraction/mapping artifacts. Review Envelope C at `fd2bca5b4a16263723692d2a9c6536235577af69` separately holds post-freeze L3/L4 audit/governance overlays and attests A without becoming part of A. The human review binds exact A+C; future B preserves that lineage during path relocation. This makes the certificate current for review of A through C; it does not grant semantic approval or implementation authority.

## Acceptance boundaries

Traceability certification != documentation approval. Documentation approval != Phase-1 implementation authorization. Phase-1 authorization != Phase-2 authorization. Source hashes != current external truth. No-loss != semantic correctness. Formula source coverage != formula validation. All approval/implementation/capital/switchover gates remain pending.
