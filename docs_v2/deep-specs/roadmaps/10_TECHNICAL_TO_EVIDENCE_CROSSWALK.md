# Technical-to-Evidence Crosswalk

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

## Why the axes differ

Technical phases order producer/consumer implementation. Evidence stages order what claims become defensible. A many-to-many mapping is unavoidable:

- Recorder starts in Technical Phase 3 / Evidence Stage 2 and serves every later stage.
- Replay starts in Technical Phase 8 / Evidence Stage 6 and remains the regression, incident, model and capacity instrument.
- Execution phases 12–14 progress from M1 deterministic tests through M2 Replay, M3 Shadow, M4 probes and M5 scoped Live.
- Participant Phase 21 consumes data collected by phases/stages much earlier.
- Scaling Phase 26 uses evidence generated across nearly the entire system.

## Key crosswalk

| Technical chain | Evidence progression | Claim unlocked |
|---|---|---|
| 1–3 types/adapters/Recorder | SPECIFY→OBSERVE | Auditable source data exists |
| 4–5 book/rules | RECONSTRUCT | Point-in-time state is trustworthy |
| 6–7 graph/formulas | MAP→IDENTIFY | Exact candidate economics exists |
| 8–12 Replay/opportunity/account/Risk/ESM | REPLAY | Same-Core decisions/failures reproduce |
| 13–19 transport/recovery/quant/Atlas/sizing/sim/Shadow | SIMULATE→SHADOW→PREDECLARE | Real-time system and predictions are ready for bounded test |
| 20 | MICRO-LIVE→VALIDATE TT/TTT | Actual execution calibration and narrow taker capability |
| 21–23 | LEARN→MAKER INTELLIGENCE→VALIDATE MT/MTT | Supported learned/maker capabilities |
| 24–25 | CAPITAL INTELLIGENCE→PORTFOLIO→BRIDGE | Supported shared allocation/relocation |
| 26 | HORIZONTAL→VERTICAL→INFRA SCALE | Wider/deeper/infra scopes only where earned |

F2 methods reuse these rows rather than adding ordinals:

| F2 method/capability | Technical support consumed | Existing evidence stages consumed | Restriction |
|---|---|---|---|
| T0 + narrow Bounded Sweep | 5–8 initially; each evaluated cell inherits its real dependencies | SPECIFY through REPLAY as applicable | fixed hypothesis/domain; diagnostic only |
| full T1 | 8–14 plus supported 18 | REPLAY and SIMULATE | no invented mechanics, fills or permission |
| T2 + final holdout | supported T1 plus point-in-time 15–18 evidence where consumed | SIMULATE plus existing temporal validation work; no new stage | T2 precedes holdout; holdout used once |
| first DRAFT OWA/TT baseline | 8–20 in ordinary dependency order | REPLAY → SHADOW LIVE → MICRO-LIVE → VALIDATE TT | each transition separately reviewed/authorized |
| Factory and generalized research | complete bounded validated baseline first | reuse relevant stages 1–21 per Challenger | inactive before full gate; no auto-promotion |
| local/distributed workers | dependencies of the exact job | inherit the job's evidence stage | local optional; distributed deferred; neither owns truth |
| Structure Discovery | no current activation phase | none added | Future human Architecture Review |

## Persistent feedback

```text
PREDICT → EXECUTE/OBSERVE → COMPARE → CALIBRATE
→ VALIDATE → PROMOTE/HOLD/DEMOTE → RECORD → REPLAY
```

The authoritative row-level 26-phase mapping is [TECHNICAL_PHASE_TO_EVIDENCE_STAGE_MAP.md](../../_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_TO_EVIDENCE_STAGE_MAP.md). Maturity mapping is [TECHNICAL_PHASE_TO_MATURITY_MAP.md](../../_analysis/pass12_build_validate_scale/TECHNICAL_PHASE_TO_MATURITY_MAP.md).

The F2 owner/gate/STOP details are in the [F2 Technical and Evidence Crosswalk](../../_analysis/f2_final_integration/F2_TECHNICAL_EVIDENCE_CROSSWALK.md). No Phase 27, Evidence Stage 22 or new M-level is created.
