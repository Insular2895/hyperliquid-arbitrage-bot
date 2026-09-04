# Risk Parameter Governance

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

No numerical value below is invented. `Atomic only` means an authenticated, validated, logged version switch outside a critical transition; every active ExecutionPlan retains its pinned version. Emergency hard stops are not ordinary hot reloads. All records require `name`, `unit`, `scope`, `owner`, `valid range`, `provenance`, `version`, `effective_at`, evidence, update/rollback procedure, hot-reload policy and plan pinning.

## Parameter-family register

| Class | Name/family | Unit | Scope / owner | Valid range / provenance | Update process | Hot reload | Pinned per plan | Validation requirement |
|---|---|---|---|---|---|---|---|---|
| `CONSTITUTIONAL` | Safe action-set enforcement | boolean rule | Global / Risk | Must remain enabled; SRC-005 | Code/spec promotion | NO | YES semantics | Property: rejected action never resurrected |
| `CONSTITUTIONAL` | Priority hierarchy/action order | ordered enum | Global / Risk+Scheduler | Exact source order only | Constitutional change review | NO | YES semantics | Scheduler/property tests |
| `CONSTITUTIONAL` | Valid-state/no-stale enforcement | boolean rule | Market/route / Risk+Data | Must remain enabled | Constitutional change review | NO | YES semantics | Stale/gap/corrupt tests |
| `CONSTITUTIONAL` | Actual-fill/exchange-truth precedence | boolean rule | Account/execution / Risk+Execution | Must remain enabled | Constitutional change review | NO | YES semantics | Partial/late/duplicate fill tests |
| `CONSTITUTIONAL` | Reservation-before-order/no-double-spend | boolean rule | Account/plan / Risk+Inventory | Must remain enabled | Constitutional change review | NO | YES | Concurrency/property tests |
| `CONSTITUTIONAL` | No blind retry/cancel finality | boolean rule | Order / Risk+Execution | Must remain enabled | Constitutional change review | NO | YES | Lost-response/cancel-race tests |
| `CONSTITUTIONAL` | Reconciliation before new risk/readiness | boolean rule | Account/client / Risk+Reconciliation | Must remain enabled | Constitutional change review | NO | YES semantics | Restart/UNKNOWN tests |
| `CONSTITUTIONAL` | Hard inventory gate | boolean rule | Asset/account / Risk+Inventory | Must remain enabled; reducing exception only | Constitutional change review | NO | YES | Hard-band property |
| `CONSTITUTIONAL` | No martingale/no default averaging down | boolean rule | Strategy/client / Risk | Must remain enabled | Constitutional change review | NO | YES semantics | Loss-sequence property |
| `CONSTITUTIONAL` | Bounded known-exposure recovery | boolean rule | Recovery / Risk+Execution | Must remain bounded | Constitutional change review | NO | YES | Recovery termination property |
| `CONSTITUTIONAL` | Optimizer subordinate to hard eligibility | boolean rule | Portfolio / Risk | Must remain enabled | Constitutional change review | NO | YES semantics | Optimizer resurrection test |
| `CONSTITUTIONAL` | Client/operator constitutional floor | boolean rule | Client / Risk+Deployment | Cannot be weakened | Constitutional change review | NO | YES semantics | Malicious config tests |
| `CALIBRATED` | `stale_age_max` / feed freshness windows | duration | Feed/market / Risk+Data | Positive, within validated clock/feed support | Offline evidence → config review | Atomic only | YES | Regime/latency/stale fault |
| `CALIBRATED` | Clock offset/uncertainty health bounds | time | Infra instance / Risk+Infra | Within measured synchronization support | Benchmark + risk review | Atomic only | YES | Drift/jump/unsync injection |
| `CALIBRATED` | Infra degradation thresholds/windows/hysteresis | metric-specific | Infra/client / Risk+Infra | Ordered HEALTHY→CRITICAL transitions | Benchmark + shadow/micro-live | Atomic only | YES | Fault/soak and false-trigger review |
| `CALIBRATED` | `max_spread` / economic spread support | bps | Market/regime / Risk | Nonnegative, inside validated economics | Replay + micro-live | Atomic only | YES | Boundary/OOS test |
| `CALIBRATED` | Minimum executable depth/band/levels | base/quote | Market/side / Risk+Sizing | Positive within observed support | Replay + market-capacity evidence | Atomic only | YES | Book boundary/adversarial |
| `CALIBRATED` | `max_depth_participation` | ratio | Market/side/regime / Risk | `[0,1]`, validated capacity | Replay + micro-live | Atomic only | YES | Shared-depth/property |
| `CALIBRATED` | `max_volume_participation` and window | ratio + duration | Market/regime / Risk | `[0,1]`; positive supported window | Replay + temporal OOS | Atomic only | YES | Window/boundary |
| `CALIBRATED` | `max_impact` / taker slippage bound | bps/value | Market/mode/size / Risk+Execution | Nonnegative; within validated execution support | Simulator + micro-live | Atomic only | YES | Impact/slippage tails |
| `CALIBRATED` | Realized-volatility windows/limits | annualized/return + duration | Market/regime / Risk+Quant | Valid estimator support; ordered states | Temporal OOS + stress | Atomic only | YES | Boundary/regime test |
| `CALIBRATED` | Robust-jump window/threshold/hysteresis | robust score + duration | Market / Risk+Quant | Positive support-derived bound | Temporal OOS + stress | Atomic only | YES | Synthetic jump/outlier |
| `CALIBRATED` | `p_survive_min` / `p_exec_min` | probability | Route/horizon / Risk+Participants | `[0,1]`, calibrated forecast | Model promotion + monitoring | Atomic only | YES | Calibration/OOD |
| `CALIBRATED` | Expected-arrival-edge threshold | bps/value | Route/size / Risk+Strategy | Covers real costs and supported uncertainty | Replay + micro-live | Atomic only | YES | Economic/tail crosscheck |
| `CALIBRATED` | `model_confidence_min` | score/probability | Model/capability / Risk+Validation | Inside validated calibration semantics | Model promotion | Atomic only | YES | Calibration/fallback |
| `CALIBRATED` | Hard/soft OOD boundaries | model-specific distance | Model/market/regime/size / Risk+Model owner | Ordered nonnegative support bounds | Temporal OOS + stress | Atomic only | YES | OOD boundary/property |
| `CALIBRATED` | Maximum model disagreement | dispersion metric | Model ensemble/capability / Risk | Nonnegative; tied to versioned predictions | Model validation | Atomic only | YES | Challenger disagreement/fallback |
| `CALIBRATED` | `simulation_confidence_min` | score/coverage | Simulator mode/fidelity/size / Risk+Simulator | Within validated fidelity support | Calibration report promotion | Atomic only | YES | Coverage/OOD test |
| `CALIBRATED` | `p_positive_min` | probability | Strategy/route/size / Risk | `[0,1]` | Replay + micro-live | Atomic only | YES | Probability calibration |
| `CALIBRATED` | Minimum ExpectedPnL/economic significance | quote currency/bps | Strategy/route/size / Strategy+Risk boundary | Nonnegative after all costs | Economic validation | Atomic only | YES | Cost/accounting boundary |
| `CALIBRATED` | ES/CVaR confidence level and limit | probability + currency | Route/portfolio/client / Risk | Alpha in `(0,1)`; loss bound within evidence | Stress/replay/micro-live | Atomic only | YES | Mandatory CVaR gate test |
| `CALIBRATED` | Max single-route loss | quote currency/% equity | Route/client / Risk | Nonnegative and within client/global floor | Tail evidence + review | Atomic only | YES | Worst-path/fault |
| `CALIBRATED` | Recovery tail/loss limit | currency/% equity | Recovery/client / Risk | Bounded and stricter than unlimited behavior | Recovery simulation + micro-live | Atomic only | YES | Recovery-loss/termination |
| `CALIBRATED` | Recovery attempts/time/price bounds | count/duration/bps | Recovery/market / Risk+Execution | Finite nonnegative; valid exit support | Replay + fault injection | Atomic only | YES | Exhaustion/escalation |
| `CALIBRATED` | Inventory target/soft/hard bands | base/quote value | Asset/account / Inventory+Risk | `HardMin ≤ SoftMin ≤ Target ≤ SoftMax ≤ HardMax` | Inventory evidence + review | Atomic only | YES | Band/property tests |
| `CALIBRATED` | Net-flow windows/limits | base/quote per duration | Asset/account / Inventory+Risk | Multiple positive windows; support-derived bounds | Replay + rolling reference | Atomic only | YES | Offline parity |
| `CALIBRATED` | Concentration maximum | ratio | Asset/portfolio / Risk+Inventory | `[0,1]`; core-asset exception explicit | Portfolio evidence | Atomic only | YES | Boundary/shared exposure |
| `CALIBRATED` | Transit maximum age/value | duration + currency | Asset class/account / Risk+Inventory | Finite positive support-derived | Replay + recovery evidence | Atomic only | YES | Age/value escalation |
| `CALIBRATED` | Stranded/terminal viability bounds | cost/time/liquidity metrics | Terminal asset/route / Risk+Routing | Exit must be supported; nonnegative costs | Replay + Market Atlas evidence | Atomic only | YES | OWA rejection test |
| `CALIBRATED` | Bridge threshold/risk/hysteresis/cooldown | value/risk/duration | Asset path / Risk+Bridge | Positive advantage and bounded risk | Replay + accounting validation | Atomic only | YES | Flip-flop/accounting test |
| `CALIBRATED` | Maker maximum exposure/age/toxicity | size/value/duration/score | Market/strategy / Risk+Execution | Within fill/adverse-selection support | Maker replay + micro-live | Atomic only | YES | T5/stale/toxic fill |
| `CALIBRATED` | Dust tolerance/pending-buffer bounds | base/quote | Asset/route / Risk+Inventory+Execution | Exchange-valid; bounded residual | Precision/recovery evidence | Atomic only | YES | Partial/dust recovery |
| `CALIBRATED` | Capital-at-risk limit | currency/% equity | Client/global / Risk | Nonnegative, within actual reconciled capital | Portfolio/tail evidence | Atomic only | YES | Reservation/concurrency |
| `CALIBRATED` | Concurrent execution limit | count | Client/market/strategy / Risk | Finite nonnegative; resource/correlation support | Load + portfolio validation | Atomic only | YES | Concurrency/property |
| `CALIBRATED` | Per-market/asset/strategy/mode limits | size/value/loss/rate | Scoped / Risk | Within global/constitutional floor | Evidence + review | Atomic only | YES | Hierarchical limit property |
| `CALIBRATED` | Route expected-loss budget / portfolio ES | currency/% equity | Route/portfolio / Risk+Portfolio | Aggregated within global tail budget | Scenario/stress validation | Atomic only | YES | Correlation/shared-resource |
| `CALIBRATED` | Drawdown bands/hysteresis | currency/%/duration | Client/strategy / Risk | Ordered `NORMAL<CAUTION<RISK_OFF<HALT` | Longitudinal evidence + stress | Atomic only | YES | State transition/no martingale |
| `CALIBRATED` | Session/daily loss windows/limits | currency/% + duration | Client/strategy / Risk | Multiple finite windows, ordered response | Replay/live evidence | Atomic only | YES | Window/velocity test |
| `CALIBRATED` | Loss velocity/consecutive failure limits | loss/time + count | Strategy/market/client / Risk | Finite support-derived | Incident/replay evidence | Atomic only | YES | Burst-failure injection |
| `CALIBRATED` | Execution quality tolerance/windows | error/rate/duration | Mode/market/strategy / Risk+Execution | Calibrated predicted-vs-realized bounds | Micro-live monitoring | Atomic only | YES | Kill/latch/fallback |
| `CALIBRATED` | Simulator calibration tolerances/windows | bias/error/coverage | Simulator/fidelity / Risk+Simulator | Inside promoted calibration support | Validation report | Atomic only | YES | Calibration kill |
| `CALIBRATED` | Participant drift tolerances/windows | drift/calibration metric | Model/capability / Risk+Participants | Within model support | Temporal monitoring/promotion | Atomic only | YES | Drift kill/fallback |
| `CALIBRATED` | API safety reservations/budgets | requests/actions/connections | Client/exchange / Risk+Execution | Reserve cancel/recovery/reconcile before new | Load/rate-limit evidence | Atomic only | YES | Saturation/priority test |
| `CALIBRATED` | `TTL_risk` | duration | Market/regime/fidelity / Risk | Positive; no longer than supported state/edge life | Replay + latency/survival evidence | Atomic only | YES | Expiry/TOCTOU test |
| `CALIBRATED` | Size grid/refinement/runtime budget | size points + duration | Strategy/route / Sizing+Risk | Bounded; finds valid solution in time | Exhaustive small-case comparison | Atomic only | YES | Correctness/performance |
| `CALIBRATED` | Scaling evidence/capital bands | evidence count/capacity | Client/strategy / Risk+Validation | Bounded by `Q_validated`; nondecreasing evidence | Promotion decision | NO intra-run by default | YES | Micro-live/tail/capacity |
| `LEARNED` | Survival/arrival/fill/liquidity forecast parameters | model-specific | Model/market/regime / Participants | Only promoted support domain | Offline train → temporal OOS → promote | Atomic artifact switch | YES | Calibration/lift/OOD/runtime |
| `LEARNED` | OOD representation/distance parameters | model-specific | Model/capability / Model owner | Nonnegative score with declared support | Model promotion | Atomic artifact switch | YES | Held-out OOD/fallback |
| `LEARNED` | Participant/cross-market response and confidence | distributions | Model/market/horizon / Participants | Validated sparse support only | Champion/challenger promotion | Atomic artifact switch | YES | Temporal OOS/ablation |
| `LEARNED` | Simulator response/queue calibration | distributions | Fidelity/market/size / Simulator | Validated coverage/support only | Offline calibration promotion | Atomic artifact switch | YES | Predicted-vs-realized coverage |
| `EXCHANGE_RULE` | Fees/tier/debit-asset rules | currency/bps | Account/market / Fee+Metadata | Exact current exchange rule | External revalidate → atomic metadata version | Atomic outside transition | YES | Fixture/integration/current docs |
| `EXCHANGE_RULE` | Tick/lot/minimum/precision rules | exchange units | Market/asset / Precision+Metadata | Exact current exchange rule | External revalidate → atomic metadata version | Atomic outside transition | YES | Boundary/property/integration |
| `EXCHANGE_RULE` | Order-type/ALO/IOC/FOK semantics | enum/rule | Market/order / Execution+Metadata | Exact current exchange behavior | External revalidate → emulator/contract update | NO unsafe transition | YES | Emulator + micro-live |
| `EXCHANGE_RULE` | Rate-limit schedule and cancel mechanism | request/action budget | Account/IP/exchange / Execution | Exact current exchange rule | External revalidation + load test | Atomic only | YES | Saturation/retry/cancel priority |
| `SAFETY_DEFAULT` | Uncalibrated capability default | capability state | Capability / Risk+Validation | Disabled or most conservative source-supported mode | Replace only with validation evidence | Atomic only | YES | Fail-safe default test |
| `SAFETY_DEFAULT` | Unknown/invalid config behavior | readiness state | Client / Risk+Deployment | Prevent `READY`; no favorable coercion | Fix and revalidate config | NO | N/A | Malformed/missing config test |
| `USER_TIGHTENABLE` | Client max size/capital/loss caps | native units | Client/strategy / Risk | At or below validated/system maximum | Authenticated versioned config | Atomic only | YES | Cannot exceed parent/property |
| `USER_TIGHTENABLE` | Client market/asset/strategy/mode allowlist | set/boolean | Client / Risk+Deployment | Subset of validated capabilities | Authenticated versioned config | Atomic only | YES | No enable beyond manifest |
| `USER_TIGHTENABLE` | Client kill and stricter drawdown/impact bounds | state/native units | Client/scoped / Risk | Only equal or safer than system floor | Authenticated audit + ack | Kill immediate; relaxation atomic | YES | Privilege/bypass tests |
| `OPEN` | Exact risk thresholds, including CVaR limits (`OPEN-007`) | metric-specific | Multi-scope / Risk | Unchosen until strategy/data evidence | Human validation after replay/shadow/micro-live | NO until chosen | YES after promotion | Evidence package required |
| `OPEN` | Exact infra-health limits (`OPEN-004`) | metric-specific | Infra/client / Risk+Infra | Unchosen until distributions measured | Benchmark + Risk review | NO until chosen | YES after promotion | Fault/soak evidence |
| `OPEN` | Inventory penalties/bands (`OPEN-009`) | metric-specific | Asset/account / Inventory+Risk | Unchosen until PASS 07 evidence | Future closure + validation | NO until chosen | YES after promotion | Inventory/portfolio evidence |
| `OPEN` | Maker/TM/MM activation and caps (`OPEN-012`) | capability + metric | Strategy/client / Execution+Risk+Validation | Disabled unless explicitly validated | Human activation decision | NO | YES | Queue/fill/adverse/recovery micro-live |

## Governance invariants

1. `HardMax < SoftMax`, negative bounds, invalid probability or missing required provenance prevent readiness; ordering is validated according to each bound's direction (for inventory: `HardMin ≤ SoftMin ≤ Target ≤ SoftMax ≤ HardMax`).
2. Client values may tighten but never exceed parent validated limits or disable constitutional rules.
3. A config switch creates a new version and RiskSnapshot. Existing exposure is not retroactively declared safe.
4. Threshold optimization uses accepted and rejected cases and considers NetPnL, drawdown, ES and recovery frequency; it does not blindly maximize PnL.
5. Exact external exchange values require revalidation before implementation or Live use.

Source: SRC-005 lines 161–178, 1033–2899, 2985–3224, 3432–3643 and 3945–4089.
