# Open Human Decisions

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## Canonical governance rule

`OPEN` is an unresolved question, not a synonym for human choice. Apply, in order:

1. source resolves it → `SOURCE_RESOLVED`;
2. changing external fact → `EXTERNAL_REVALIDATION`;
3. empirical data selects it → `CALIBRATED` or `LEARNED`;
4. semantics-preserving engineering selects it → `IMPLEMENTATION_CHOICE`;
5. later capability owns it → `DEFERRED`;
6. multiple valid policy choices materially change intended behavior → `HUMAN_POLICY_DECISION`.

Every item has one primary semantic owner. Other domains are consulted/consumers and cannot issue a competing decision.

## Recomputed current result

The historical grouping of 28 OPEN IDs into exactly eight HD families is superseded as current governance, while its traceability is preserved in the Phase-14 analysis. Current dispositions are: 13 `CALIBRATED`, 3 `LEARNED`, 8 `IMPLEMENTATION_CHOICE`, 2 `HUMAN_POLICY_DECISION`, and 2 `DEFERRED`. Zero OPEN is a documentation-baseline or Phase-1 blocker.

Only two current genuine policy families remain:

| ID | Policy question | OPEN | Earliest scope | Evidence ceiling | Safe fallback |
|---|---|---|---|---|---|
| `HPD-01` | authorize a specific MT/MTT maker-mode scope after evidence | 012 | Technical Phase 23 / bounded MT or MTT probe | queue/fill/adverse/cancel/recovery plus Risk/readiness | MT/MTT disabled; TT/TTT unaffected |
| `HPD-02` | accept a license/product mechanism and its policy envelope | 014 | client distribution | threat model, outage/revocation and safe-exit proof | local isolated Core; distribution disabled |

TM/MM remain `FUTURE`, outside Technical Phase 23 and outside HPD-01. Their presence in an enum/interface establishes compatibility only: representable does not mean implemented, validated or authorized. They require a separate future product/safety/evidence specification. Node activation and cross-exchange product scope are deferred, not current decisions. Infrastructure/model/grid/threshold winners are selected by evidence; a human may approve, narrow, defer or reject promotion but may not substitute preferences for failed evidence.

## Human approval ceiling

```text
EvidenceEligibility ∩ HumanPolicyApproval ∩ CapabilityManifest
∩ Readiness ∩ Risk
```

Human approval cannot override failed evidence, hard Risk, stale/invalid state, OOD, unsupported q, missing calibration, invalid mathematics or exchange facts. Data selects learned/calibrated candidates; humans govern promotion and policy boundaries. Promotion approval is a scoped/versioned/evidence-linked governance record, not manual parameter selection.

## Specific corrected doctrines

- `HD-01`/`HD-02` historical overlap is removed: infrastructure measurements, health limits and InfraROI methods have one primary evidence/calibration owner; their consumers do not decide them independently.
- Historical `HD-03`: Data/Participants selects the candidate artifact, horizons, coefficients and internals through temporal OOS evidence. Human authority is limited to approve/narrow/defer/reject promotion.
- Historical `HD-07`: undefined mathematical semantics, statistical estimator choice and typed representation are separate. No reviewer invents a number for undefined division.
- Historical `HD-08`: grid/refinement and solver representation are calibrated or implementation choices. A complex optimizer requires evidence eligibility plus human promotion approval; simple deterministic enumeration remains the fallback.
- `HDC-001..094` are mapped as one post-reconstruction review package with per-item deterministic dispositions. They do not require 94 independent policy decisions.

## Blocker scope

MT/MTT maker activation pending under HPD-01 does not block TT/TTT. TM/MM are Future and cannot be activated by HPD-01. Bridge or cross-exchange pending does not block same-venue V1. Scaling policy does not block Phase 1. Deferred decisions remain disabled in their exact capability scope. Documentation acceptance, Phase-1 authorization, Micro-live authorization, Live authorization and `docs_v2 -> docs` switchover are all separate gates and remain ungranted.

See [Phase-14 governance analysis](../_analysis/phase14_human_decision_governance/FINAL_PHASE14_REPORT.md) for the complete 28-OPEN and 94-HDC mappings.
