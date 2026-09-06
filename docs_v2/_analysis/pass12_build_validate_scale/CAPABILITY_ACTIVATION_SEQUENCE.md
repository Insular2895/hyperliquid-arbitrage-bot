# PASS 12 — Capability Activation Sequence

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

“First possible” is not “automatically permitted.” Every transition needs current dependencies, evidence and explicit authorization.

| Capability | Required dependency maturity | First possible RunMode | First capital | Validation gate |
|---|---|---|---|---|
| RAW Recorder | Types/adapters M1 | Live capture / Replay data production | None | Ordered RAW, checksums, quality/backpressure |
| Replay Core | Recorder/book/formulas M1 | Replay | None | Deterministic DecisionTrace, no-lookahead |
| Opportunity Detection | Graph/NetConvert M1, Replay M2 | Replay | None | Reproducible exact candidates/rejects |
| TT OWA Shadow | Opportunity/Risk/ESM/Recovery M2; transport/ops ready | Shadow | None | Same Core, valid direct comparator, complete traces |
| TT OWA Micro-live | Critical dependencies M3 and rollback/reconcile proven | MicroLive | Probe | Predeclared bounds/stops and actual reconciliation |
| TT OWA Live | TT M4 and current capability scope | Live | Validated bounded | M5 evidence for exact market/mode/size/version |
| TTT | Taker ESM/Recovery plus TT proof and TTT-specific three-leg evidence | Replay→Shadow→MicroLive | Separate probe | Actual output per leg; intermediate/tail/recovery proof |
| Participant Survival | Episodes + microstructure + point-in-time Replay | Replay/Shadow | None directly | Simple baseline, temporal OOS, calibration, lift |
| Advanced Simulator | F0/F1 M2 + participant/maker data | Replay/Research | None | F2/F3 calibration; F4 Research-only |
| Maker Shadow | Maker forecast and queue mechanics M2/M3 | Shadow | None | Fill/time/adverse/cancel/expiry support |
| MT | Maker Shadow + execution/recovery M3 | MicroLive | Separate probe | MT-specific predicted↔actual and Risk gate |
| MTT | MT/TTT dependencies plus three-leg maker evidence | MicroLive | Separate probe | MTT-specific fill/continuation/recovery gate |
| Portfolio Allocation | Individually valid candidates + shared constraints | Replay/Shadow | None initially | QF-078 correctness and lift vs baseline |
| Bridge | Atlas history, terminal viability, sizing, Risk, STAY comparator | Replay/Shadow | Separate probe | Relocation/exit/utilization evidence |
| Horizontal Scale | Each added capability validated; shared constraints proven | Live | Scaled validated | Repeat market/route evidence; independence checked |
| Vertical Scale | Next band supported by Q_validated | Live | Scaled validated | Size-dependent next-band calibration |
| Infrastructure Scale | Comparable benchmark + capture economics | Shadow then Live profile | No direct capital grant | Positive robust NetUpgradeValue/InfraROI |

`TM` and `MM` may remain type-supported but are absent from this initial canonical sequence and default-disabled. Cross-exchange remains `FUTURE`.
