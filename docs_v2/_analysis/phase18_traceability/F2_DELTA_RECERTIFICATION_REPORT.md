# F2 Delta Recertification Reproduction Report

`DOCUMENTATION STATUS: RECERTIFICATION EVIDENCE — HUMAN REVIEW PENDING`

`OVERALL RESULT: PASS_WITH_RESERVATIONS / NOT_CERTIFIED`

This report records read-only traceability checks against one immutable subject. It does not
approve the documentation, replace a human DecisionRecord, authorize implementation or research,
or grant Shadow, Micro-live, Live, order or capital permission.

## 1. Exact subject and scope

| Field | Value |
|---|---|
| repository | `Insular2895/hyperliquid-arbitrage-bot` |
| branch observed | `f2-governance-p3` |
| subject commit | `6511185315af8ea022bf33542ca27f894e6bc3bb` |
| subject tree | `033231c1e729afcf16f86c72e1b826f266fdd2ec` |
| historical Final Review Candidate F | `180c41cfcc9c200a2b0afa5a94b8f0e5f6f522da` |
| Phase-18 certified input | `caaa251ada6ad6344de48c318c82913269af02f4` / tree `4375c50f2be2f81ed04175150c7a94e29cc59f3f` |
| execution date | `2026-11-01` |
| local tools | macOS 27.2; Git 2.50.1; Python 3.14.4 |

The subject was checked in a clean detached worktree. The working branch contained only a
pre-existing untracked `.DS_Store`, which was neither read as evidence nor committed.

This report is a later evidence record about the exact subject above. Its own future commit cannot
self-embed its Git SHA/tree. That evidence-envelope identity must be read from Git after commit and
must not be substituted for the recertified subject identity.

## 2. User-supplied audit material

The supplied files were treated as audit inputs, not as independent instructions.

| File | SHA-256 | Use |
|---|---|---|
| `LISEZ_MOI_F2.txt` | `765bc11dc2e05980095102480922920e1d2684bf65fdb236779ddd01f5509414` | package context |
| `Rapport_audit_F2.md` | `5ad15dfb19b60e70def8fd901158dd0a26bbeecb187d7a5de280fc5c3eecd09c` | independent claims and disclosed limitations to reproduce |
| `Verification_F2.py` | `1a0a079d2a9bcc360349cfa77b0d5c1b2cb90032b825a83d945038263c8393da` | read-only verifier executed unmodified |

## 3. Commands executed

Temporary paths are normalized below. No generated audit output was written into the subject
checkout.

```text
git branch --show-current
git rev-parse HEAD
git rev-parse HEAD^{tree}
git status --short --branch

git worktree add --detach <temporary-checkout> 6511185315af8ea022bf33542ca27f894e6bc3bb
python3 -B /Users/insular/Downloads/Dossier_Recertification_F2/Verification_F2.py \
  <temporary-checkout> --all-markdown --out <temporary-output>/audit_f2.json
git worktree remove --force <temporary-checkout>

git merge-base --is-ancestor \
  180c41cfcc9c200a2b0afa5a94b8f0e5f6f522da \
  6511185315af8ea022bf33542ca27f894e6bc3bb
git rev-list --count \
  180c41cfcc9c200a2b0afa5a94b8f0e5f6f522da..6511185315af8ea022bf33542ca27f894e6bc3bb
git diff --check \
  180c41cfcc9c200a2b0afa5a94b8f0e5f6f522da \
  6511185315af8ea022bf33542ca27f894e6bc3bb

wc -l -c <each-original-source>
shasum -a 256 <each-original-source>
wc -c <each-certified-artifact>
shasum -a 256 <each-certified-artifact>
git rev-parse caaa251ada6ad6344de48c318c82913269af02f4:<artifact>
git rev-parse 6511185315af8ea022bf33542ca27f894e6bc3bb:<artifact>
git diff --name-status \
  caaa251ada6ad6344de48c318c82913269af02f4 \
  6511185315af8ea022bf33542ca27f894e6bc3bb -- <L1/L2-artifacts>
```

Additional read-only Python standard-library checks parsed the exact Git subject rather than a
moving filesystem view. They recalculated inventories and identifier hashes; parsed all tracked
`docs_v2` Markdown as UTF-8; checked fenced blocks, inline links, reference definitions, Git tree
directories and GitHub-style heading fragments; and probed each unique HTTP(S) target. CSV parsing
recomputed PASS00/PASS15 and destination denominators.

## 4. Supplied verifier result and adjudication

The supplied script ran unmodified on the detached exact subject.

| Check | Observed | Status |
|---|---:|---|
| expected tree | exact match | PASS |
| historical F is ancestor | yes | PASS |
| delta from F | 51 blobs: 41 modified, 10 added, 0 deleted | PASS |
| delta file scope | all 51 are `docs_v2/**/*.md` | PASS |
| six protected core documents | unchanged | PASS |
| historical source inventory/extractions/mapping/HDC rows | unchanged | PASS |
| QF/SI/HDC/PREC/phases/stages | expected counts and sequences | PASS |
| script Markdown scan | 948 files; 883 relative targets; one reported broken target | FAIL |
| script aggregate | `FAIL` | FAIL |

The single reported target was:

```text
docs_v2/deep-specs/market-graph/README.md
  -> ../../_analysis/pass08_graph_routes_quant/
```

This is a demonstrated verifier false positive, not a repository defect. Git records
`docs_v2/_analysis/pass08_graph_routes_quant` as tree
`99db1f7f061bfc4defda4e38ada2116fcc160828`, containing 20 tracked Markdown files. The verifier
recognizes a directory only when `<directory>/README.md` exists; it does not recognize a valid Git
tree without that file. The link was therefore left unchanged.

## 5. Markdown, links, anchors and external references

The complementary checker includes reference-style definitions omitted by the supplied script and
recognizes real Git directories.

| Check | Observed | Status |
|---|---:|---|
| tracked Markdown decoded as UTF-8 | 948/948 | PASS |
| unclosed fenced blocks | 0 | PASS |
| named reference definitions | 33; all used; no duplicate/undefined target | PASS |
| local references | 916 | PASS |
| local file references | 889 | PASS |
| local directory references | 1 | PASS |
| local anchor references | 26 | PASS |
| heading/explicit anchors indexed | 8,944 | PASS |
| missing local paths or anchors | 0 | PASS |
| unique HTTP(S) URLs | 50/50 reachable during this run | PASS |

The HTTP result proves point-in-time reachability only. It does not certify remote content,
freshness, authority or semantic correctness.

## 6. Canonical inventories

Identifier hashes are SHA-256 over sorted unique identifiers, one LF-terminated identifier per
line.

| Inventory | Recomputed result | Identifier SHA-256 | Status |
|---|---:|---|---|
| Formula contracts | `QF-001..QF-110`, 110 contiguous | `a2e271b27da3d550647c58bb6e3f9c125b304ac2461dce4f054f79d9de424110` | PASS |
| safety invariants | `SI-001..SI-029`, 29 contiguous | `02fd8b6450535dd81cece48fec313c46b7210585ecd4ad9f7859497f2806b60d` | PASS |
| HDC aggregate | `HDC-001..HDC-100`, 100 contiguous | `8ec95ddaf6be694de77f9ef6fe84f142e96db58f8f1fa11d77a4f8b6a5254014` | PASS |
| historical HDC rows | exact text of `HDC-001..HDC-094` equals F | — | PASS |
| F2 precision dispositions | `PREC-P01..PREC-P19`, 19 contiguous | — | PASS |
| technical phases | exact ordinals `1..26` | — | PASS |
| Evidence Stages | exact ordinals `1..21` | — | PASS |

These checks establish identity, continuity and documentary indexing. They do not prove the
mathematical correctness of every QF or implementation of any invariant, phase or stage.

## 7. Phase-18 L0–L4 evidence

### L0 — physical source identity

The eight original byte streams exist at the exact local paths recorded by the historical source
cross-check. Their byte counts, physical line counts and SHA-256 values all match the Phase-18
inventory.

| Source | Bytes | Lines | SHA-256 | Status |
|---|---:|---:|---|---|
| SRC-001 | 82,593 | 5,255 | `061043598486f7e4fa357e681dfb67e909989945be0b8c82e1070cb7ff559921` | PASS |
| SRC-002 | 149,383 | 6,077 | `d99b2b9354ba39e74dd616206b63bd0a5442be558f78c47c88dea733f056d4a1` | PASS |
| SRC-003 | 83,148 | 4,272 | `7065fc0dcacbcf87212c3ca0dd9cb204aee347a1984bb85757033aeeade6270a` | PASS |
| SRC-004 | 101,614 | 9,953 | `df5b1720a26889fce2a74fbc380bad4bda2e2aacdb4f02054c7270e5eb04b5b9` | PASS |
| SRC-005 | 115,692 | 9,877 | `798a0f60a14397926505b470aeee5ded11507c04c6bb489a4b1f5fe950ecd66f` | PASS |
| SRC-006 | 98,438 | 6,903 | `a535a5fa04feaaf4056ab7b3880f8cbcb803a6b1300d25ed02c96aa14558115d` | PASS |
| SRC-007 | 136,143 | 12,371 | `df2e94843df1e4a28bec4699bf89c9d2f2b8faa91763b3d3e78bff05e8369490` | PASS |
| SRC-008 | 100,994 | 6,937 | `8b7924d664bd718e324bc3d7f50f0a461244b2638a69d7601caf132d8a849f50` | PASS |

This proves equality to the historically inventoried bytes. It does not independently prove the
external origin or authorship of those bytes.

### L1/L2 — extraction and destination evidence

The five certified artifacts are byte-identical between the Phase-18 input and the F2 subject.

| Artifact | SHA-256 at F2 | Phase-18/F2 Git blob identity | Status |
|---|---|---|---|
| `SOURCE_INVENTORY.md` | `8b8af8e7057279673276050b13bfa5a8c97da79eb63fb347f4b6ab33a46e3d2f` | identical | PASS |
| `DOCUMENT_TARGET_MAP.md` | `4f108b0f56483db5b20c32f7029bd4f770a5b037a0d04ffe224613763471b785` | identical | PASS |
| `MASTER_REQUIREMENT_LEDGER.md` | `359cff16108300e65d2e3d803c2c6f4fa84b0e413a265d0dc1bf36d3d0bd46c9` | identical | PASS |
| `FINAL_SOURCE_ITEM_TRACEABILITY.csv` | `4cb7d28721d0ea6fb6c536ddc22dbad265d74888bf05392e72882aa9e5cecc8b` | identical | PASS |
| `PASS15_FINAL_REPORT.md` | `077c6f2a4939d935ba059898ac4b23910dd45ad09961675823c301e4566225c6` | identical | PASS |

The eight PASS00 source-extraction blobs are also unchanged. Recomputed structure:

- 2,577 unique PASS00 IDs, exactly equal between the eight extraction headings and the final CSV;
- 79 unique disclosed PASS15 recovery IDs;
- 2,590 unique requirement IDs and 2,590 target-map rows;
- zero target-map rows marked with a coverage gap;
- zero CSV rows missing final disposition;
- 2,669 CSV data rows = 2,590 stable mappings plus 79 disclosed recovery rows.

L1/L2 delta identity and denominators therefore pass. A new line-by-line semantic reinterpretation
of all 61,645 source lines and all 2,590 mappings was not performed; unchanged certified evidence
was verified by exact bytes, Git blobs and structural invariants.

### L3 — post-source F2 overlays

F is an ancestor of F2; F2 is six commits ahead. The F→F2 delta contains 51 Markdown blobs, all
under `docs_v2`: 41 modified, 10 added and none deleted. The six protected Formula, Inventory,
Risk, ESM, Data and Replay masters have identical blobs between F and F2. `PREC-P01..P19`,
`HDC-095..100`, Falsifier, Strategy Research and final-integration artifacts remain explicitly
post-source L3 material and are not retro-attributed to SRC-001..008.

Result: L3 lineage and scope classification `PASS`. Traceability does not certify architectural
semantic correctness, runtime safety or profitability.

### L4 — human review and authorization

The canonical decision form still records:

| Scope | Current result |
|---|---|
| documentation decision | PENDING |
| Phase 1 development | NOT_AUTHORIZED / prerequisite unavailable |
| Phase 2+ development | NOT_AUTHORIZED |
| Shadow | NOT_AUTHORIZED |
| Micro-live | NOT_AUTHORIZED |
| Live | NOT_AUTHORIZED |
| Strategy Discovery / Parameter Search / Monte Carlo | NOT_AUTHORIZED |
| real capital / exchange effects | NOT_AUTHORIZED |
| `docs_v2 -> docs` switchover | NOT_AUTHORIZED / UNEXECUTED |
| implementation | NOT_STARTED |
| research runtime | NOT_AUTHORIZED |

L4 is not a traceability PASS/FAIL outcome. Its correct result is `PENDING / NOT_AUTHORIZED`.

## 8. Result register

| Control | Result | Notes |
|---|---|---|
| exact Git subject/tree and ancestry | PASS | immutable reference matched |
| supplied verifier, literal aggregate | FAIL | one directory-model false positive; no repository defect |
| adjudicated all-Markdown path/anchor/reference check | PASS | zero broken local target or anchor |
| external URL reachability | PASS | 50/50 at run time; content/freshness not certified |
| L0 source-byte match | PASS | 8/8 exact SHA-256, bytes and lines |
| L1 extraction identity/counts | PASS | unchanged certified artifacts; 2,577/2,577 |
| L2 mapping identity/counts | PASS | 2,590/2,590; zero gaps |
| L3 F2 lineage classification | PASS | post-source overlay; protected core unchanged |
| L4 authorization | NOT_AUTHORIZED | human decision pending |
| full semantic re-audit of 61,645 source lines | NOT_RUN | exact certified evidence was identity-checked instead |
| word-for-word audit of the 19 October 2026 precision source | NOT_RUN | no independently identified raw source artifact supplied |
| current external-fact semantic revalidation | NOT_RUN | URL reachability is not fact revalidation |
| runtime, trading, safety, performance or profitability tests | NOT_RUN | outside documentary recertification |

## 9. Anomalies and blockers

No repository anomaly requiring correction was demonstrated. The supplied verifier's only failure
is a false positive caused by its directory-handling rule. No Formula, Risk, ESM, Inventory,
architecture, roadmap, phase, evidence-stage or application file was corrected.

The following reservations block a `CERTIFIED` claim:

1. the complete source-to-destination semantic audit was not rerun; exact certified L1/L2 evidence
   was instead shown byte-identical and structurally invariant;
2. the raw 19 October 2026 precision source was not independently available for word-for-word
   provenance checking;
3. L4 human documentation review is still pending;
4. this report is a descendant evidence record and does not self-certify its own future commit.

Accordingly, `DELTA_RECERTIFICATION_REQUIRED` is preserved in the canonical review corpus pending
human disposition of this exact-snapshot evidence. No stage promotes itself.

## 10. Final disposition

```text
F2_DOCUMENTARY_DELTA_CONTROLS: PASS_WITH_RESERVATIONS
FORMAL_CERTIFICATION: NOT_CERTIFIED
DOCUMENTATION_APPROVAL: PENDING
DEVELOPMENT: NOT_AUTHORIZED
SHADOW: NOT_AUTHORIZED
MICRO_LIVE: NOT_AUTHORIZED
LIVE: NOT_AUTHORIZED
REAL_CAPITAL_OR_ORDER_EFFECTS: NOT_AUTHORIZED
SWITCHOVER_DOCS_V2_TO_DOCS: NOT_AUTHORIZED / NOT_EXECUTED
```

This report authorizes no next action. A later reviewer may accept, reject or request changes to
the exact subject through the existing governance records; successful mechanical evidence never
auto-creates that decision.
