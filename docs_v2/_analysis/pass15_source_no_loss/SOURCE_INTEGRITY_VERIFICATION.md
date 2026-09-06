# Source Integrity Verification

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

All eight source byte streams were reopened from the first byte through EOF, decoded line-sequentially, hashed, and joined to their PASS00 extraction before semantic review. “Read completely” below means the sequential scanner consumed every physical line and the audit reviewed every logical extraction interval plus every uncovered interval; it does not mean keyword-only search.

| SRC ID | Filename | Expected SHA-256 | Actual SHA-256 | Expected approximate lines | Actual lines | Hash match? | Read completely? | Audit complete? | PASS00 extraction exists? |
|---|---|---|---|---:|---:|---|---|---|---|
| SRC-001 | `23. Lock-free  ring buffers  zero-copy.md` | `061043598486f7e4fa357e681dfb67e909989945be0b8c82e1070cb7ff559921` | `061043598486f7e4fa357e681dfb67e909989945be0b8c82e1070cb7ff559921` | ≈5256 | 5255 | YES | YES | YES | YES |
| SRC-002 | `Bot hyperliquid .md` | `d99b2b9354ba39e74dd616206b63bd0a5442be558f78c47c88dea733f056d4a1` | `d99b2b9354ba39e74dd616206b63bd0a5442be558f78c47c88dea733f056d4a1` | ≈6144 | 6077 | YES | YES | YES | YES |
| SRC-003 | `Concrètement, en production on doit garder au moins .md` | `7065fc0dcacbcf87212c3ca0dd9cb204aee347a1984bb85757033aeeade6270a` | `7065fc0dcacbcf87212c3ca0dd9cb204aee347a1984bb85757033aeeade6270a` | ≈4277 | 4272 | YES | YES | YES | YES |
| SRC-004 | `DOSSIER 16 — EXECUTION STATE MACHINE.md` | `df5b1720a26889fce2a74fbc380bad4bda2e2aacdb4f02054c7270e5eb04b5b9` | `df5b1720a26889fce2a74fbc380bad4bda2e2aacdb4f02054c7270e5eb04b5b9` | ≈9953 | 9953 | YES | YES | YES | YES |
| SRC-005 | `DOSSIER 36 — RISK CONSTITUTION V1.md` | `798a0f60a14397926505b470aeee5ded11507c04c6bb489a4b1f5fe950ecd66f` | `798a0f60a14397926505b470aeee5ded11507c04c6bb489a4b1f5fe950ecd66f` | ≈9877 | 9877 | YES | YES | YES | YES |
| SRC-006 | `DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT.md` | `a535a5fa04feaaf4056ab7b3880f8cbcb803a6b1300d25ed02c96aa14558115d` | `a535a5fa04feaaf4056ab7b3880f8cbcb803a6b1300d25ed02c96aa14558115d` | ≈6903 | 6903 | YES | YES | YES | YES |
| SRC-007 | `Oui, dans le modèle qu’on vient de définir, le plus propre est que….md` | `df2e94843df1e4a28bec4699bf89c9d2f2b8faa91763b3d3e78bff05e8369490` | `df2e94843df1e4a28bec4699bf89c9d2f2b8faa91763b3d3e78bff05e8369490` | ≈12377 | 12371 | YES | YES | YES | YES |
| SRC-008 | `Oui. Et en creusant le sujet, je corrigerais une chose fondamentale….md` | `8b7924d664bd718e324bc3d7f50f0a461244b2638a69d7601caf132d8a849f50` | `8b7924d664bd718e324bc3d7f50f0a461244b2638a69d7601caf132d8a849f50` | ≈6937 | 6937 | YES | YES | YES | YES |

Result: **8/8 hashes match; 8/8 sources read; 61 645 physical lines audited; 8/8 extractions present.** Integrity gate: PASS.
