# PASS 03 — Simulator Requirement Ledger

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 03 REVIEW COMPLETE`

## Control totals

- PASS 00 Simulator-index requirements reviewed: **231**.
- Recovered simulator-critical Formula references reviewed: **42**, of which 2 were already in the index and 40 are additional stable requirement IDs.
- Unique requirements reviewed: **271**.
- Original-source locator review: **271 YES**, **0 NO**.
- PASS 00 source distribution: SRC-001 23; SRC-002 13; SRC-003 15; SRC-004 7; SRC-005 75; SRC-006 42; SRC-007 30; SRC-008 26.
- PASS 00 statuses retained as historical metadata: `LOCKED` 132; `RESEARCH` 51; `FUTURE` 24; `CALIBRATED` 12; `EXTERNAL_REVALIDATION` 8; `REJECTED` 4.
- Destinationless requirements: **0**.

## Normalized ledger schema

This ledger is normalized to avoid reproducing 231 long PASS 00 records with divergent text. For **every ID in the complete review set below**, the following join is authoritative:

1. `MASTER_REQUIREMENT_LEDGER.md` supplies Requirement ID, canonical source statement, original source/locator, PASS 00 status, authority, dependencies/consumers, Formula references, Risk/Execution/Data/Validation implications, original target/owner, external-revalidation flag, and PASS 00 notes.
2. `domain_indexes/SIMULATOR.md` supplies membership in the PASS 03 review set and repeats source/locator/status.
3. The PASS 03 profile matrix below supplies reviewed status, canonical interpretation, Simulator layer, SimulationMode, fidelity, inputs, outputs, dependencies, target, owner, and disposition.
4. Per-ID overrides below supersede only PASS 00 classification metadata; stable IDs and original provenance never change.

Every ID listed below was reopened at its original locator. `Reviewed against original source = YES`. This relational representation contains every field required by the mission without inventing a second source statement.

## PASS 03 semantic profiles

| Profile | PASS 03 reviewed status | Canonical interpretation | Simulator layer / SimulationMode / Fidelity | Inputs | Outputs | Formula references | Risk / Execution / Participant / Replay / Validation implications | Target / cross-domain owner / external revalidation | Notes |
|---|---|---|---|---|---|---|---|---|---|
| `CORE_MECHANICS` | `CANONICALIZED` | Deterministic exchange/arrival/Shadow mechanics precede stochastic response. | Exchange Mechanics; both modes; F0–F2 | ordered events, arrival book, intent, rules, latency | Order/Fill events, `Δour`, partial/residual | QF-009–016, 040–042, 084 | Risk consumes forecast; Execution owns states; Replay must be deterministic; M1–M4 evidence | Master §§7–11; deep 02/03; Execution/Data owners; exchange facts external | No generic slippage or instant-t0 fill. |
| `HISTORICAL` | `CANONICALIZED` | Detect incompatibility; Exogenous preserves future; interactive branches/rejoins explicitly. | Historical Compatibility; Exogenous/Interactive; F0–F4 | baseline, ordered events, branch delta, fidelity | compatibility decisions, branch/rejoin provenance | QF-043, 104 | Fail invalid branches; Replay/Data owns events/schema; M2+ | Master §§12–14/23; deep 04/09; Data/Replay owner | Exact alternate world rejected. |
| `RESPONSE` | `CANONICALIZED` | `Δresponse` is conditional/calibrated aggregate local and sparse cross-market response. | Market Response; Interactive; F3, F4 Research | `Δour`, state, Participant forecasts, support | response scenarios, confidence/OOD | QF-043–050, 081–083, 104 | Risk gates confidence; Participant owns forecasts; replay seed/version; temporal OOS/Micro-live | Master §§15–16; deep 05/07; Participants/Graph/Data owners | Conditional Empirical Champion direction; advanced models Challengers. |
| `MAKER` | `CANONICALIZED` | Maker uses price-time plus explicit L2 queue uncertainty and adverse-selection paths. | Mechanics + Response; either mode with limits; F2+ | maker intent, L2/L4 label, trades/cancels, MakerForecast | fill/time/partial/adverse distributions | QF-051–055, 058, 099 | Execution owns cancel/race/states; Participant owns forecast; Micro-live required | Master §17; deep 06; Execution/Participants/Data owners; L4 facts external | Pessimistic/Optimistic/Probabilistic modes. |
| `SCENARIO_RISK` | `CANONICALIZED` | Sample only calibrated uncertainties; cover full/partial/recovery/failure and multi-size. | Scenario/Risk; mainly Interactive; F1–F4 | mechanics, forecasts, seed, recovery candidates | PnL/tails/completion/confidence distributions | QF-026/027, 056–063, 076, 079/080, 104 | Risk owns gates; Recovery/Execution states reused; deterministic RNG; M2–M4 | Master §§18–22; deep 08; Risk/Execution/Sizing owners | No single deterministic advanced PnL. |
| `DATA_DETERMINISM` | `REVIEWED_DEPENDENCY` | Same engine/different transport; declared mode/fidelity; reproducible ordering/clock/RNG/state. | Runtime; all modes/fidelities | events/config/models/formulas/seed/state versions | DecisionTrace, manifest, hashes, traceable forecast | references only | RunMode cannot alter logic; stale worker result rejected; PASS 06 schemas | Master §§25–26; deep 12; Data/Replay owner | Exact schema deferred, terminology retained. |
| `VALIDATION` | `REVIEWED_DEPENDENCY` | Capability authority advances M0→M5 with predicted-vs-actual evidence and live precedence. | Validation; all | Golden/Replay/Shadow/Micro-live evidence | calibration/drift/coverage/promotion state | QF-095–104 where applicable | Simulator Calibration Kill Switch; dependent maturity cap | Master §§27–29; deep 11; Validation/Risk owner | No numerical thresholds invented. |
| `CROSS_DOMAIN` | `REVIEWED_DEPENDENCY` | Relevant constraint/input is preserved and routed; PASS 03 does not seize ownership. | Declared by consuming profile | owning-domain contract | Simulator input or downstream forecast | source-defined | Owning pass closes policy/schema/state | Master/deep cross-link + future owning pass | No silent redefinition. |
| `RESEARCH_FUTURE` | `REVIEWED / NOT ACTIVATED` | Optional advanced capability remains Research/Future or explicitly rejected. | F4/Research or future | validated prerequisite data | stress/challenger result only | source-defined | Cannot affect Live before promotion | Master §30; deep 05/10; Research/owning domain | Includes Hawkes/agents/deep models/FPGA. |

## Complete PASS 00 review set

The original source/locator/status for each ID is the exact record in `domain_indexes/SIMULATOR.md`; all are reviewed `YES`.

### SRC-001 — 23

`REQ-RESEARCH-0001`, `REQ-VALID-0002`, `REQ-EXEC-0004`, `REQ-REPLAY-0001`, `REQ-REPLAY-0002`, `REQ-VALID-0003`, `REQ-CAP-0002`, `REQ-BRIDGE-0002`, `REQ-REPLAY-0003`, `REQ-RESEARCH-0005`, `REQ-VALID-0006`, `REQ-DATA-0002`, `REQ-EXEC-0017`, `REQ-EXEC-0019`, `REQ-EXEC-0020`, `REQ-INFRA-0008`, `REQ-RISK-0012`, `REQ-EXEC-0022`, `REQ-DATA-0003`, `REQ-REPLAY-0004`, `REQ-CAP-0006`, `REQ-VALID-0008`, `REQ-EXEC-0025`.

Profile disposition: Replay/Data/Validation items → `DATA_DETERMINISM`/`VALIDATION`; capital/bridge/risk/infra/execution items → `CROSS_DOMAIN`; research/live-evidence items → `RESEARCH_FUTURE` or `VALIDATION`. Original targets remain their owners; Simulator interpretation is in master §§25–29.

### SRC-002 — 13

`REQ-MICRO-0002`, `REQ-EXEC-0030`, `REQ-ARCH-0017`, `REQ-FUTURE-0003`, `REQ-ARCH-0024`, `REQ-EXEC-0049`, `REQ-QUANT-0004`, `REQ-REPLAY-0005`, `REQ-VALID-0011`, `REQ-EXEC-0055`, `REQ-ACCT-0030`, `REQ-INFRA-0028`, `REQ-MICRO-0005`.

Profile disposition: maker/queue → `MAKER`; Replay/core architecture → `DATA_DETERMINISM`; fees/Execution/Quant → `CROSS_DOMAIN`; FPGA/rejected future → `RESEARCH_FUTURE`.

### SRC-003 — 15

`REQ-EXEC-0063`, `REQ-REPLAY-0006`, `REQ-RISK-0028`, `REQ-PRODUCT-0010`, `REQ-EXEC-0072`, `REQ-OPS-0004`, `REQ-REC-0006`, `REQ-EXEC-0074`, `REQ-EXEC-0077`, `REQ-RISK-0031`, `REQ-EXEC-0078`, `REQ-ARCH-0064`, `REQ-RISK-0032`, `REQ-EXEC-0079`, `REQ-INV-0011`.

Profile disposition: Replay/time/improvement loop → `DATA_DETERMINISM`/`VALIDATION`; impossible-perfect-simulation limitation → `HISTORICAL`; Risk/Operations/Recorder/Inventory → `CROSS_DOMAIN`; future enhancements → `RESEARCH_FUTURE`.

### SRC-004 — 7

`REQ-EXEC-0193`, `REQ-EXEC-0220`, `REQ-EXEC-0223`, `REQ-EXEC-0225`, `REQ-FORMULA-0074`, `REQ-FORMULA-0080`, `REQ-FORMULA-0119`.

Profile disposition: deterministic/state/execution interface → `CORE_MECHANICS`/`DATA_DETERMINISM`; QF-059/QF-104 → `SCENARIO_RISK`; inventory penalty remains `CROSS_DOMAIN`. Authority is SRC-004.

### SRC-005 — 75

`REQ-RISK-0049`, `REQ-RISK-0083`, `REQ-RISK-0149`, `REQ-RISK-0199`, `REQ-RISK-0239`, `REQ-RISK-0259`, `REQ-RISK-0263`, `REQ-RISK-0264`, `REQ-RISK-0274`, `REQ-DATA-0010`, `REQ-DATA-0019`, `REQ-DATA-0021`, `REQ-DATA-0022`, `REQ-DATA-0024`, `REQ-DATA-0027`, `REQ-DATA-0071`, `REQ-DATA-0084`, `REQ-DATA-0085`, `REQ-REPLAY-0007`, `REQ-DATA-0087`, `REQ-DATA-0090`, `REQ-DATA-0091`, `REQ-DATA-0103`, `REQ-DATA-0104`, `REQ-REPLAY-0008`, `REQ-DET-0002`, `REQ-DATA-0106`, `REQ-DATA-0107`, `REQ-DATA-0108`, `REQ-REPLAY-0009`, `REQ-DATA-0110`, `REQ-DATA-0111`, `REQ-CLOCK-0006`, `REQ-CLOCK-0007`, `REQ-CLOCK-0008`, `REQ-CLOCK-0010`, `REQ-DATA-0112`, `REQ-DATA-0119`, `REQ-DATA-0128`, `REQ-DATA-0132`, `REQ-DATA-0136`, `REQ-DET-0003`, `REQ-REPLAY-0010`, `REQ-DATA-0165`, `REQ-DATA-0166`, `REQ-REPLAY-0011`, `REQ-DATA-0167`, `REQ-DATA-0170`, `REQ-DATA-0171`, `REQ-DATA-0188`, `REQ-DATA-0192`, `REQ-DET-0005`, `REQ-DATA-0194`, `REQ-DATA-0198`, `REQ-DATA-0200`, `REQ-DATA-0201`, `REQ-REPLAY-0012`, `REQ-DATA-0202`, `REQ-DATA-0203`, `REQ-REPLAY-0013`, `REQ-DET-0006`, `REQ-DATA-0244`, `REQ-DATA-0245`, `REQ-REPLAY-0014`, `REQ-DATA-0246`, `REQ-DATA-0261`, `REQ-REPLAY-0015`, `REQ-REPLAY-0016`, `REQ-DATA-0294`, `REQ-DATA-0299`, `REQ-DATA-0301`, `REQ-REPLAY-0017`, `REQ-DATA-0313`, `REQ-DATA-0314`, `REQ-DATA-0315`.

Profile disposition: Risk kill/live precedence → `VALIDATION`; transport/mode/fidelity/clock/RNG/timer/manifest/trace/hash/same-core → `DATA_DETERMINISM`; Exogenous/Interactive/rejoin/confidence → `HISTORICAL`/`RESPONSE`; `ExecutionForecast` → `SCENARIO_RISK`; exact schemas remain Data-owned. Authority is SRC-005.

### SRC-006 — 42

`REQ-DEPLOY-0004`, `REQ-DEPLOY-0011`, `REQ-DEPLOY-0094`, `REQ-DEPLOY-0119`, `REQ-CLIENT-0019`, `REQ-DEPLOY-0167`, `REQ-VALID-0015`, `REQ-VALID-0017`, `REQ-VALID-0019`, `REQ-VALID-0020`, `REQ-VALID-0026`, `REQ-VALID-0034`, `REQ-VALID-0048`, `REQ-VALID-0083`, `REQ-VALID-0084`, `REQ-VALID-0086`, `REQ-VALID-0087`, `REQ-VALID-0089`, `REQ-VALID-0090`, `REQ-VALID-0092`, `REQ-VALID-0098`, `REQ-VALID-0143`, `REQ-VALID-0144`, `REQ-VALID-0147`, `REQ-VALID-0148`, `REQ-VALID-0162`, `REQ-VALID-0201`, `REQ-VALID-0206`, `REQ-VALID-0235`, `REQ-VALID-0236`, `REQ-VALID-0239`, `REQ-VALID-0265`, `REQ-VALID-0275`, `REQ-VALID-0278`, `REQ-VALID-0279`, `REQ-VALID-0281`, `REQ-VALID-0307`, `REQ-VALID-0316`, `REQ-VALID-0317`, `REQ-VALID-0335`, `REQ-VALID-0359`, `REQ-VALID-0364`.

Profile disposition: F0–F4, Replay/Shadow/Micro-live, distributions, OOD, slicing, release evidence → `VALIDATION`; deploy/client/release dependencies → `CROSS_DOMAIN`. Authority is SRC-006.

### SRC-007 — 30

`REQ-SURV-0001`, `REQ-LIQ-0003`, `REQ-SURV-0007`, `REQ-SIM-0001`, `REQ-PART-0008`, `REQ-CLOCK-0014`, `REQ-SURV-0011`, `REQ-VALID-0370`, `REQ-PRODUCT-0019`, `REQ-ROUTE-0028`, `REQ-SIM-0002`, `REQ-SIM-0003`, `REQ-PART-0016`, `REQ-SIM-0004`, `REQ-SIM-0005`, `REQ-EXEC-0265`, `REQ-EXEC-0267`, `REQ-QUANT-0010`, `REQ-RECOV-0018`, `REQ-EXEC-0278`, `REQ-SIM-0006`, `REQ-SIM-0007`, `REQ-QUANT-0020`, `REQ-BENCH-0008`, `REQ-ROUTE-0033`, `REQ-ARCH-0084`, `REQ-SIM-0008`, `REQ-FORMULA-0143`, `REQ-RISK-0324`, `REQ-FORMULA-0147`.

Profile disposition: Participant forecasts/survival/liquidity/cross-market → `RESPONSE`; Monte Carlo/distribution/recovery → `SCENARIO_RISK`; runtime/hot path → `CROSS_DOMAIN`; Hawkes/agents/deep models → `RESEARCH_FUTURE`; calibration → `VALIDATION`. PASS 02 owns forecast semantics.

### SRC-008 — 26

`REQ-EXEC-0286`, `REQ-INFRA-0051`, `REQ-TRI-0003`, `REQ-VALID-0372`, `REQ-REPLAY-0018`, `REQ-EXEC-0290`, `REQ-REPLAY-0019`, `REQ-INFRA-0053`, `REQ-SIM-0009`, `REQ-RECOV-0024`, `REQ-SIM-0010`, `REQ-ARCH-0091`, `REQ-SIM-0011`, `REQ-VALID-0374`, `REQ-EXEC-0315`, `REQ-EXEC-0316`, `REQ-EXEC-0319`, `REQ-EXEC-0320`, `REQ-FORMULA-0151`, `REQ-EXEC-0321`, `REQ-EXEC-0324`, `REQ-EXEC-0327`, `REQ-INFRA-0079`, `REQ-ACCT-0066`, `REQ-REPLAY-0020`, `REQ-EXEC-0339`.

Profile disposition: three layers/arrival/mechanics → `CORE_MECHANICS`; incompatibility/modes/branch/rejoin → `HISTORICAL`; multi-market/response → `RESPONSE`; confidence/capacity/scenarios → `SCENARIO_RISK`; F4/agents → `RESEARCH_FUTURE`; Micro-live → `VALIDATION`; unrelated later infrastructure/execution depth remains `CROSS_DOMAIN`. SRC-008 is primary detailed Simulator authority where closure does not override it.

## Recovered Formula dependency set — 42

All are `REVIEWED_DEPENDENCY`, authority SRC-004, original status retained, original locator reopened, reviewed `YES`, target `SIMULATOR_FORMULA_CROSSCHECK.md` plus the appropriate master/deep section, cross-domain owner Formula/PASS 11:

`REQ-FORMULA-0022`, `REQ-FORMULA-0023`, `REQ-FORMULA-0024`, `REQ-FORMULA-0025`, `REQ-FORMULA-0026`, `REQ-FORMULA-0027`, `REQ-FORMULA-0028`, `REQ-FORMULA-0029`, `REQ-FORMULA-0039`, `REQ-FORMULA-0040`, `REQ-FORMULA-0054`, `REQ-FORMULA-0055`, `REQ-FORMULA-0057`, `REQ-FORMULA-0058`, `REQ-FORMULA-0059`, `REQ-FORMULA-0060`, `REQ-FORMULA-0061`, `REQ-FORMULA-0062`, `REQ-FORMULA-0063`, `REQ-FORMULA-0064`, `REQ-FORMULA-0065`, `REQ-FORMULA-0066`, `REQ-FORMULA-0067`, `REQ-FORMULA-0068`, `REQ-FORMULA-0069`, `REQ-FORMULA-0070`, `REQ-FORMULA-0071`, `REQ-FORMULA-0072`, `REQ-FORMULA-0073`, `REQ-FORMULA-0074`, `REQ-FORMULA-0075`, `REQ-FORMULA-0076`, `REQ-FORMULA-0077`, `REQ-FORMULA-0078`, `REQ-FORMULA-0091`, `REQ-FORMULA-0094`, `REQ-FORMULA-0095`, `REQ-FORMULA-0096`, `REQ-FORMULA-0097`, `REQ-FORMULA-0099`, `REQ-FORMULA-0100`, `REQ-FORMULA-0119`.

Inputs/outputs and implications resolve by formula family: mechanics QF-009–016/040–043 → `CORE_MECHANICS`; survival/maker QF-044–055 → `RESPONSE`/`MAKER`; economic/tail QF-056–063/076/079/080 → `SCENARIO_RISK`; cross-market QF-081/082 → `RESPONSE`; latency QF-084/085 → `CORE_MECHANICS`; QF-104 → `SCENARIO_RISK`/`VALIDATION`. No expression is redefined.

## PASS 03 status corrections

PASS 00 status is preserved in provenance; these reviewed interpretations control this domain:

| Requirement(s) | PASS 00 | PASS 03 reviewed status | Reason |
|---|---|---|---|
| `REQ-EXEC-0286`, `REQ-REPLAY-0018` | RESEARCH | `LOCKED_ARCHITECTURE` | Three-layer separation and incompatibility are the final scientific correction. |
| `REQ-EXEC-0290`, `REQ-REPLAY-0019` | FUTURE | `LOCKED_MODE_SEMANTICS` | SRC-005 closes both SimulationMode values; activation varies by fidelity. |
| `REQ-SIM-0009`, `REQ-RECOV-0024` | FUTURE / RESEARCH | `LOCKED_ARCHITECTURE` | Perturbation and branch/rejoin are canonical; rejoin threshold remains calibrated. |
| `REQ-SIM-0010` | EXTERNAL_REVALIDATION | `LOCKED_FAIL_CONSERVATIVE_BEHAVIOUR` | Non-rejoin/low-confidence response is internal semantics, not an external fact. |
| `REQ-ARCH-0091`, `REQ-EXEC-0316`, `REQ-EXEC-0319`, `REQ-EXEC-0320`, `REQ-EXEC-0321` | RESEARCH/FUTURE | `LOCKED_TARGET_ARCHITECTURE` | Later SRC-008 architecture plus closure support. This is not implementation approval. |
| `REQ-VALID-0374` | RESEARCH | `LOCKED_VALIDATION_PRINCIPLE` | SRC-006 closes Micro-live as M4 evidence for capital-affecting models. |
| `REQ-SIM-0011` | RESEARCH | `RESEARCH` | F4 explicit-agent fidelity remains Research. |
| `REQ-EXEC-0315` | FUTURE | `FUTURE / NON-BASELINE` | Wallet identity, giant multi-agent RL, and deep simulator are not initial requirements. |

## Global field defaults

- Risk implication: confidence/OOD/calibration can only preserve, reduce, or reject capability; PASS 05 owns exact action.
- Execution implication: same authoritative state machine and Recovery semantics; PASS 04 owns exact transitions.
- Participant dependency: only PASS 02 forecasts and model governance are consumed.
- Replay dependency: ordered inputs, no look-ahead, ReplayClock, deterministic timers, same core, and seed provenance.
- Validation dependency: M0–M5 evidence; no numerical gate invented.
- External revalidation: only exchange/feed/L4/API/academic claims marked in the source/register; internal architecture does not become external.
