# PASS 12 — Evidence Stage Matrix

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| Stage | Name | Primary question | Technical center | Capital permission | Maturity relation | Persistent evidence |
|---:|---|---|---|---|---|---|
| 0 | SPECIFY | Are purpose/contracts/invariants/tests unambiguous? | All specs | None | M0 | Specs, requirement ledger, planned tests |
| 1 | OBSERVE / RECORD | Can source truth and quality be captured? | Adapters, Recorder, Clock | None | M1 foundations | RawEvent, RawChunkManifest, quality report |
| 2 | RECONSTRUCT | Can books/metadata/account chronology be reproduced? | Book, metadata, fees, precision | None | M1 | DatasetId, reconstruction report |
| 3 | MAP | What structures and supported places exist? | Graph, routes, early Atlas | None | M1/M2 | GraphVersion, RouteDefinitions, AtlasVersion |
| 4 | IDENTIFY | Which candidates have exact current economics? | NetConvert, Opportunity | None | M1/M2 | Opportunity/reject episodes |
| 5 | REPLAY | Can identical knowledge reproduce identical decisions? | Same Core Replay | None | M2 | RunManifest, DecisionTrace, ReplayReport |
| 6 | SIMULATE | What F0/F1 outcome distributions follow explicit assumptions? | Simulator F0/F1 | None | M2 | Scenario/Simulation report |
| 7 | SHADOW LIVE | Does the real-time system remain correct without effects? | Full Core + Shadow transport | None | M3 | ShadowRun, would-execute traces |
| 8 | PREDICTED VS ACTUAL PREPARATION | Are predictions, joins, slices and stop criteria declared before probes? | Evidence contracts | None | M3 | Pre-registered ValidationPlan |
| 9 | LEARN COMPETITION / SURVIVAL | How long do opportunities survive and why? | Microstructure/Participants | None normally | M2/M3 | ModelReport, episode labels |
| 10 | MICRO-LIVE | What does real execution do under tiny bounded intervention? | TT, Risk, Recovery, Ops | Probe | M4 candidate | MicroLiveRun, fills, reconciliation |
| 11 | VALIDATE TT | Is immediate taker→taker calibrated and safe in scope? | TT | Validated bounded | M4→M5 | ValidationReport, CapabilityManifest |
| 12 | VALIDATE TTT | Is three-leg taker execution separately calibrated? | TTT | Probe→validated bounded | M4→M5 scoped | Legwise actual/predicted report |
| 13 | MAKER INTELLIGENCE | Can queue/fill/adverse selection be learned? | Maker models, F2 | None / dedicated probe only | M2/M3 | Maker ModelReport |
| 14 | VALIDATE MT / MTT | Are maker-led modes safe and calibrated separately? | MT/MTT, F2/F3 | Probe→validated bounded | M4→M5 scoped | Mode-specific ValidationReport |
| 15 | CAPITAL INTELLIGENCE | Where is capital useful and exit-capable? | Inventory, Atlas, Sizing | Existing validated scopes only | M2–M5 by consumer | Utility/terminal/size evidence |
| 16 | PORTFOLIO ALLOCATION | Can multiple opportunities share constraints safely? | QF-078 portfolio | Validated bounded after proof | M2→M4/M5 | Allocation comparison report |
| 17 | BRIDGE / CAPITAL RELOCATION | Does moving beat STAY after all costs and risks? | Bridge/relocation | Separate probe→validated | M2→M4/M5 | Relocation/exit/utilization report |
| 18 | HORIZONTAL SCALE | Can more independent validated opportunities be captured? | Markets/routes/instances | Scaled validated | Scoped M5 | Expansion ValidationReport |
| 19 | VERTICAL SCALE | Can q increase inside a larger supported band? | Q_validated/sizing/Risk | Scaled validated | Scoped M5 | Next-band calibration report |
| 20 | INFRASTRUCTURE SCALE | Does a host/feed upgrade create robust net value? | Benchmark + InfraROI | No direct grant | Infra scope M3–M5 | InfraBenchmark + economic comparison |

Technical work and evidence are not 1:1: Recorder, Replay, Shadow and Micro-live remain reusable evidence instruments after their first stage.
