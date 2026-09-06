# Overcompression Audit

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

“Headline present” was not accepted as coverage. Each priority family was checked for branches, precedence, fallback, ordering, units, versioning, evidence and negative rules.

| Priority area | Implementation semantics checked | Canonical evidence | Result | Issue |
|---|---|---|---|---|
| Execution/Recovery | zero/full/partial; maker partial; cancel-after-partial; actual-fill-only; dust/buffer; UNKNOWN; Recovery exits/split; startup reconciliation | Execution master §§14–28 and deep 03, 05–10 | FULL | none |
| Risk | hard gates; safety priority; risk-reducing exception; kills; TTL/version; fail-closed | Risk master and deep 01–10 | FULL | none |
| Data/Replay | receive chronology; four clocks; recorder_seq; DecisionTrace; no lookahead; point-in-time; checkpoint not truth; RAW immutable | Data/Recorder masters and deep specs | FULL | none |
| Participants | survival/hazard/half-life/capture; correction; competition; OFI/MLOFI/QI; fill/adverse; P0–P5; drift/OOD | Participants master/deep 01–09 | FULL | none |
| Simulator | Exogenous/Interactive; interference; local mutation; compatibility; three queue modes; branch/rejoin/non-rejoin; F0–F4 | Simulator master/deep 01–12 | FULL | none |
| Capital/Bridge | classes; terminal viability; exit/stranded cost; sizing≠slicing; QF-027≠076; shared capacity; action/accounting taxonomy | Inventory/Capital master/deep 01–10 | FULL | none |
| Graph/Quant | directed conversions; NetConvert; OWA comparator; pair_to_routes; Graph≠Atlas≠HWC; alpha split | Graph/Microstructure/Formula masters and deep specs | FULL | none |
| Infrastructure | public feed first; node optional; storage-role split; 11 benchmark dimensions; economic upgrade/downgrade | Infrastructure master/deep 01–08 | FULL | none |
| Deployment | client isolation; OCI/digest/non-root/read-only/drop caps/no socket; secrets; update/rollback/fencing/license safety | Deployment master/deep 01–12 | FULL | none |
| Validation/Roadmap | M0–M5; scoped maturity; CapabilityManifest; evidence families; predicted-vs-actual; 26 phases; stop/scale gates | Validation/Operations/Roadmap masters/deep specs | FULL | none |
| Recorder production purpose | reconstruct; predicted/simulated-vs-actual; regime/drift; offline point-in-time recalibration data | Recorder master §1 and deep 09/10 | FULL AFTER RECOVERY | OMISSION-P15-002 |

Canonical V2 overcompression issues found: **1**; corrected: **1** (the four Recorder purposes). PASS00 atomicity/destination overcompression findings: **6** broad ranges; corrected: **6** through 77 recovered source-concept rows and manual cross-domain destination overlays. The two outside-range recoveries are extraction omissions, not canonical overcompression. Equal-or-stronger V2 contracts were not duplicated into Masters.
