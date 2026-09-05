# PASS07 Validation Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Capability | Unit/property test | Replay | Shadow/Micro-live | Data/metric | OOD/failure | Promotion gate | Authority |
|---|---|---|---|---|---|---|---|
| Asset classification | valid enum/transitions/version | outcome by class/regime | shadow reclass; bounded live evidence | exit/utility/hold outcomes | stale/unsupported class | stable evidence + review | SRC-003/005 |
| Inventory bands | ordering; hard future-state invariant | band/penalty alternatives | fill reconciliation | balances/fills/deviation | mismatch/hard breach | no breach + calibrated cost | SRC-005/006 |
| NetFlow | rolling equals offline | multiple windows | shadow action effect | fill deltas/window error | gap/clock issue | exact reference match | QF-067/SRC-006 |
| Terminal Viability | no-exit/hard/stranded rejection | terminal outcome | rejected/accepted follow-up | exitability/idle/MTM | missing exit/OOD | supported exit + bounds | SRC-005/006 |
| Exit cost | executable path/size cases | predicted vs later executable | small actual exits | cost error by size | no supported book/path | calibrated error bounds | QF-068 |
| Stranded penalty | component separation | predict idle/exit/risk | outcome tracking | component calibration | arbitrary/stale coefficient | economic lift/calibration | QF-069 |
| Bridge | path set + STAY | move/stay counterfactual | bounded actual Bridge | costs/utilization/exit | stale Atlas/no reservation | positive supported QF-072 | QF-070–072 |
| Break-even cycles | zero/non-positive denominator branch | predicted vs realized cycles | bounded move outcomes | cycles/capture/exit | stale regime mean | calibrated realization | QF-071 |
| Relocation value | destination/stay/cost components | point-in-time policies | shadow move/stay | value calibration | lookahead/double count | persistent advantage | QF-072 |
| Hysteresis | alternating-rank property | threshold/cooldown grid | shadow flip rate | moves, missed EV, cost | flip-flop/inertia | balanced calibrated error | SRC-005/006 |
| Position Sizing | all q inputs; q*=0 property | exhaustive small cases | predicted/actual by q | EV/P+/ES/impact/inventory | unsupported q | next-band evidence | SRC-006 §78–82 |
| Q_validated | all gates true below selected boundary | regime/mode curves | size ladder | capacity drift | OOD/drift | current support | QF-076 |
| Sizing search | grid/refinement vs brute force | nonlinear/discrete books | n/a | regret/error/time | misses feasible optimum | bounded error/runtime | QF-077 |
| Shared capacity | no overspend/no double L2 | race schedules | shadow concurrency | reservation violations | negative capacity | zero blocking failures | SRC-005/006 |
| Multi-op allocation | brute force small cases | interaction scenarios | shadow selected sets | portfolio RAEV/capacity | Risk-rejected choice | constraint correctness | QF-078 |
| PnL attribution | component reconciliation/no duplicates | known synthetic sequences | actual fills/marks | attribution residual | external flow as PnL | zero unexplained residual | QF-105–108 |

Every Replay uses point-in-time configs/models/Atlas and a RunManifest. Micro-live is a calibration probe, never an automatic scaling authorization.
