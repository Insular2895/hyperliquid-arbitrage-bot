# PASS 12 — Roadmap Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Scope and counting

PASS 12 reviewed **142 roadmap requirement units**: the **95 stable closure requirements** `REQ-VALID-0273..REQ-VALID-0367`, the **26 canonical technical phase profiles**, and the **21 evidence-stage profiles** required by the PASS 12 mission. Stable requirement IDs were not changed. A range below is only a compact display: every ID in that inclusive range inherits the stated disposition and destination.

## Stable closure requirements

| Stable IDs | Requirement subject | Disposition | Canonical destination |
|---|---|---|---|
| `REQ-VALID-0273` | Canonical 26-phase implementation order | `TECHNICAL_ROADMAP` | `17_IMPLEMENTATION_ROADMAP.md`; technical matrices |
| `REQ-VALID-0274..0279` | Recorder-first, Replay-first, TT-first, simple baselines, no big bang, vertical slices | `TECHNICAL_ROADMAP` | masters 17/19; roadmap deep specs 01/05 |
| `REQ-VALID-0280..0286` | Recorder, book Replay, economics, paper ESM, Shadow, Micro-live TT, later intelligence milestones | `BUILD_VALIDATE_SCALE_ROADMAP` | master 19; evidence stages |
| `REQ-VALID-0287..0293` | Capital ladder, evidence at each band, down-scale, dynamic capacity, regime/model demotion | `BUILD_VALIDATE_SCALE_ROADMAP` | master 19; capital/demotion specs |
| `REQ-VALID-0294..0301` | Strategy, market, model and infra statuses; release flags; conservative defaults | `CROSS_DOMAIN_EXISTING_PASS` | PASS 09/10 capability and release contracts; linked by PASS 12 |
| `REQ-VALID-0302..0308` | Host validation/revalidation and economically proven infra upgrade | `BUILD_VALIDATE_SCALE_ROADMAP` | Stage 20; external-gate and capital matrices |
| `REQ-VALID-0309..0316` | System-wide end-to-end, fault/crash/feed/disk/config tests and acceptance matrix | `DEEP_SPEC` | roadmap deep specs 05/09/10; PASS 10 remains DoD owner |
| `REQ-VALID-0317..0320` | Release, Micro-live, scaling blockers and auto-downgrade triggers | `BUILD_VALIDATE_SCALE_ROADMAP` | stop-condition and demotion contracts |
| `REQ-VALID-0321..0325` | Continuous validation, production feedback, offline learning, periodic/event-driven review | `BUILD_VALIDATE_SCALE_ROADMAP` | continuous calibration section; PASS 10 operations |
| `REQ-VALID-0326..0331` | Validation dashboard, ValidatedCapability, CapabilityManifest, code/support separation | `CROSS_DOMAIN_EXISTING_PASS` | PASS 10 CapabilityManifest; activation/capital matrices |
| `REQ-VALID-0332..0336` | Research archive, negative results, ADRs and reasons | `CROSS_DOMAIN_PASS13` | PASS 13 architecture/ADR framing; evidence retention here |
| `REQ-VALID-0337..0340` | Spec hierarchy, conflict priority, formula and current exchange authority | `TECHNICAL_ROADMAP` | authority and external-gate sections |
| `REQ-VALID-0341..0345` | Controlled spec change, no silent drift, ambiguity policy, optimized internals, critical test-first | `TECHNICAL_ROADMAP` | Phase template and first executable instruction |
| `REQ-VALID-0346..0348` | Benchmark before optimization; no aesthetic optimization/model prestige | `BUILD_VALIDATE_SCALE_ROADMAP` | complexity and economic-lift gates |
| `REQ-VALID-0349..0352` | Serious-live criteria, non-required advanced features, final-capable architecture, validation gate | `BUILD_VALIDATE_SCALE_ROADMAP` | final path to scoped M5 |
| `REQ-VALID-0353..0358` | Measurable value plus economic, Risk, calibration and operational acceptance | `BUILD_VALIDATE_SCALE_ROADMAP` | promotion and exit criteria |
| `REQ-VALID-0359..0362` | Lifecycle, conservative learning, non-paralysis and scientific loop | `BUILD_VALIDATE_SCALE_ROADMAP` | philosophy and continuous loop |
| `REQ-VALID-0363..0364` | Project/spec and development DoD | `CROSS_DOMAIN_PASS13` | PASS 13 uses completed domain/roadmap specs; PASS 10 retains validation authority |
| `REQ-VALID-0365..0367` | Specification→Implementation→Evidence→Capital, validated-capital ceiling, no unmeasured scale | `BUILD_VALIDATE_SCALE_ROADMAP` | governing law, capital matrix and final path |

## PASS 12 phase and stage profiles

| Requirement units | Count | Disposition | Destination |
|---|---:|---|---|
| `P12-TP-01..26` technical phase profiles | 26 | `TECHNICAL_ROADMAP` | master 17, matrices, deep specs 01–04/10 |
| `P12-ES-00..20` evidence-stage profiles | 21 | `BUILD_VALIDATE_SCALE_ROADMAP` | master 19, matrices, deep specs 05–10 |

These `P12-*` labels are PASS-local audit handles, not replacements for stable `REQ-*` IDs.

## Cross-domain routing

- Exact equations remain `CROSS_DOMAIN_EXISTING_PASS` under PASS 11; PASS 12 maps QF IDs only.
- M0–M5, test families, evidence sufficiency, promotion/demotion and CapabilityManifest remain `CROSS_DOMAIN_EXISTING_PASS` under PASS 10.
- Definitive module topology remains `CROSS_DOMAIN_PASS13`.
- Cross-domain consistency closure remains `CROSS_DOMAIN_PASS14`.
- Current exchange rules remain `EXTERNAL_REVALIDATION`.
- F4, cross-exchange execution, private node, distributed hot standby and complex models without lift remain `RESEARCH/FUTURE`.

## Result

| Metric | Result |
|---|---:|
| Roadmap requirement units reviewed | 142 |
| Technical phase profiles | 26 |
| Evidence-stage profiles | 21 |
| Stable requirement IDs renumbered | 0 |
| Destinationless requirements | 0 |
