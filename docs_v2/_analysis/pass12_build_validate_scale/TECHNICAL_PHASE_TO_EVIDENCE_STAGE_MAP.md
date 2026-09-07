# PASS 12 — Technical Phase to Evidence-Stage Crosswalk

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| Technical phase | Primary evidence stage | Secondary / ongoing stages | First real use | First possible maturity | First capital | Ongoing evidence |
|---:|---|---|---|---|---|---|
| 1 Domain Types / Schemas | 0 SPECIFY | 1–20 | Unit/golden harness | M1 | None | Compatibility/regression |
| 2 Adapters | 1 OBSERVE | 2, 7–20 | Live capture | M1 | None | Feed/account conformance |
| 3 Recorder | 1 OBSERVE/RECORD | Every later stage | Continuous capture | M1 | None | Replay, trade, incident, calibration windows |
| 4 Book Engine | 2 RECONSTRUCT | 3–20 | Book replay then live Shadow | M1 | None | Desync/freshness/rebuild proof |
| 5 Metadata/Fee/Precision | 2 RECONSTRUCT | 3–20 | Boundary replay | M1 | None | Change/revalidation history |
| 6 Graph/Routes | 3 MAP | 4–19 | Structural route map | M1 | None | Topology/activation changes |
| 7 NetConvert/Formula | 4 IDENTIFY | 5–20 | Exact route economics | M1 | None | Golden/parity/economic attribution |
| 8 Replay | 5 REPLAY | 6–20 | Historical same-Core runs | M2 | None | Regression, incidents, research, capacity |
| 9 Opportunity | 4 IDENTIFY | 5–19 | Replay candidate episodes | M2 | None | Accepted/rejected episode outcomes |
| 10 Account/Inventory/Reservations | 5 REPLAY | 7–19 | Replayed then Shadow account | M2 | None | Actual fill/capital consistency |
| 11 Risk | 5 REPLAY | 7–20 | Replayed/Shadow permissions | M2 | None | Rejects, kills, tails, demotion |
| 12 Execution SM | 5 REPLAY | 6–14, 18–19 | Emulated/paper execution | M2 | None | State/failure/recovery traces |
| 13 Execution Transport | 5 REPLAY conformance | 7, 10–14 | Boundary fixtures then live-input no-effect integration | M2, then M3 in Shadow | Probe after all gates | ACK/fill/cancel behavior |
| 14 Recovery/Reconciliation | 5 REPLAY | 7–20 | Failure replay then live-input Shadow | M2, then M3 in Shadow | Required at M3 before probe | Real incidents/restarts |
| 15 Quant Microstructure | 3 MAP / 4 IDENTIFY | 5–20 | Observe-only features | M2 | None | Drift/support/features |
| 16 Market Atlas | 3 MAP | 4–20 | Structural/basic empirical atlas | M2 | None | Survival/capacity/utility enrichment |
| 17 Sizing | 6 SIMULATE | 7–19 | Replay/shadow q curves | M2 | Probe cap at Stage 10 | Q_validated increase/decrease |
| 18 Simulator F0/F1 | 6 SIMULATE | 7–20 | Replay forecasts | M2 | None by itself | Predicted↔actual calibration |
| 19 Shadow | 7 SHADOW LIVE | 8–20 | Full live-input no-effect chain | M3 | None | New release/market/model/size rehearsal |
| 20 Micro-live TT | 10 MICRO-LIVE | 11, 12, 14, 18–20 | First intentional capital | M4 TT | Probe | Reusable real calibration |
| 21 Participants | 9 LEARN COMPETITION | 7–20 | Observe/replay/shadow inference | M2/M3 | Only through separately promoted consumer | OOS/drift/economic lift |
| 22 Advanced Simulator | 13 MAKER INTELLIGENCE | 14–20 | F2/F3 research/forecast | M2/M3 | None by itself | Live contradiction/calibration |
| 23 MT/MTT | 14 VALIDATE MT/MTT | 18–20 | Maker-mode probe | M4 scoped | Probe | Fill/adverse/recovery evidence |
| 24 Portfolio | 16 PORTFOLIO | 18–19 | Multi-op replay then bounded live | M2→M4 | After explicit promotion | Shared-capacity/EconomicLift |
| 25 Bridge | 17 BRIDGE | 15, 18–19 | Relocation replay then probe | M2→M4 | Separate probe | Break-even/utilization/exit evidence |
| 26 Scaling | 18–20 SCALE | Continuous calibration/demotion | Scoped expansion | M5 scoped | Scaled validated | Every trade/release/incident |

TTT is not hidden in Phase 23: its taker state support exists in phases 12–14 and it receives a separate evidence stage after TT. Participant models are not a universal TTT prerequisite; any configured model becomes a critical dependency through the CapabilityManifest.
