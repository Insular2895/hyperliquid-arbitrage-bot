# 11 — Validation, Replay, Shadow, Micro-live and Scaling

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Evidence ladder

1. Unit/property tests prove arithmetic, invariants, classification and reservation safety.
2. Replay evaluates point-in-time inventory, Bridge, size curves and portfolio policies without lookahead.
3. Shadow records what would move/size/reserve/execute and evaluates rejected alternatives.
4. Micro-live uses hard small notional/frequency as a calibration probe.
5. Live capacity expands in evidence-gated steps and can be demoted.

No stage authorizes the next merely by elapsed time or positive aggregate PnL.

## Capability gates

| Capability | Minimum validation |
|---|---|
| Asset classification/bands | version transitions, band ordering, reconciliation, outcome evidence |
| NetFlow | live rolling value equals offline reference across windows |
| Terminal Viability | reject no-exit, hard-band and excessive-stranded cases |
| Exit/stranded economics | predicted-versus-actual exit, idle and risk components |
| Bridge | compare all allowed paths and STAY; no shortest-path shortcut |
| Break-even/relocation | realized cost, opportunity rate, capture/utilization and exit outcome |
| Hysteresis | alternating-rank test balances flip-flop and excessive inertia |
| Position Sizing | every q evaluates EV, ES/CVaR, P+, confidence, impact, inventory |
| Q_validated/search | all gates, `q*=0` if none; grid/refinement vs exhaustive small cases |
| Shared capacity | blocking no-overspend and no-L2-double-count race properties |
| Multi-op allocation | independent/shared balance/book/asset/Risk plus Bridge/Rebalance/Recovery contention |
| PnL attribution | profitable route + losing Recovery + Inventory MTM reconciles separately/global |

## Required datasets

Persist candidate and rejected Bridge decisions with STAY counterfactual; candidate size curves and rejected size points; point-in-time Atlas/model/config; reservations/releases; fills/fees/marks/external flows; predicted/actual fill, slippage, latency, PnL and Recovery; and capacity drift metrics.

## OOD and failure

Unsupported regime/size/horizon, stale Atlas, capacity drift, model disagreement or poor calibration reduces/demotes capability. Blocking failure includes negative available balance, double reservation, new risk past hard inventory, hidden exposure, action misclassification, lookahead, double-counted PnL or inability to reconcile.

## Scaling

The 40–50 EUR example is a Micro-live probe. Scaling requires observations at the current band, Simulator support at the next band, valid impact/tail/inventory behavior and no critical incident. There is no automatic 10x or percent-of-capital rule. `Q_validated` may shrink; horizontal candidates still obey shared constraints.

Sources: SRC-001 Bridge/Replay/Micro-live protocol; SRC-003 Recorder experiments; SRC-005 Risk/Data evidence; SRC-006 §§78–100/138–147/272–277; PASS02/03/04/05/06 contracts.
