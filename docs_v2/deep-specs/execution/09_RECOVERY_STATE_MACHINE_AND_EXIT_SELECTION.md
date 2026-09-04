# 09 — Recovery state machine and exit selection

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Trigger and invariant

Recovery begins when a partial fill, later-leg reject/zero fill, dead continuation edge, ambiguous order with possible exposure, unexpected balance, maker/cancel race, or recovery-order partial leaves actual or potentially actual exposure outside normal route policy. The affected capital cannot support new opportunity risk.

Recovery is not “finish the original route.” It selects the best permitted action from current inventory and current books. Actual fills, fees, rounding, balances, and exposure vector are inputs; planned output is not.

## Exact `RecoveryState`

| State | Entry | Permitted actions | Exit evidence |
|---|---|---|---|
| `RECOVERY_REQUIRED` | freeze affected new risk; snapshot actual/uncertain exposure | reconcile if truth uncertain; request candidate planning | sufficiently known current state |
| `RECOVERY_PLANNING` | enumerate current valid exits via graph/policy | simulate/compare exits and splits; Risk gate | selected permitted plan or no safe plan |
| `RECOVERY_RESERVED` | reserve recovery balances/book/Risk capacity | current-state pre-send revalidation | valid send or replan/failure |
| `RECOVERY_EXECUTING` | issue recovery intents through normal OrderState/transport | apply actual fills; cancel/query/reconcile | terminal/partial/unknown outcome |
| `RECOVERY_VERIFYING` | recompute remaining exposure and balances | reconcile and test completion | zero/permitted residual or further recovery |
| `RECOVERED` | record completion/loss/provenance | route final reconciliation | terminal success |
| `RECOVERY_FAILED` | no automatic safe plan / limits exhausted / unresolved | retain conservative locks; manual/hard-halt escalation | new explicitly authorized lifecycle only |

## Transition matrix

| From | Condition | Guard/action | To |
|---|---|---|---|
| `RECOVERY_REQUIRED` | current exposure is proven | build candidates from current state | `RECOVERY_PLANNING` |
| `RECOVERY_REQUIRED` | order/exposure uncertain | reconcile before sizing exit | remains required pending reconciliation |
| `RECOVERY_PLANNING` | best plan passes recovery Risk | reserve exact capacity | `RECOVERY_RESERVED` |
| `RECOVERY_PLANNING` | no permitted plan | persist causes/escalate | `RECOVERY_FAILED` |
| `RECOVERY_RESERVED` | capacity/current envelope valid | create immutable recovery intent(s) | `RECOVERY_EXECUTING` |
| `RECOVERY_RESERVED` | state invalid/reservation fails | release proven safe remainder/recompute | `RECOVERY_PLANNING` or `RECOVERY_FAILED` |
| `RECOVERY_EXECUTING` | fill/terminal result known | apply actual exposure change | `RECOVERY_VERIFYING` |
| `RECOVERY_EXECUTING` | outcome unknown | keep locks and reconcile | remains executing/engine reconciliation |
| `RECOVERY_VERIFYING` | exposure within policy and account consistent | finalize QF-080 loss/evidence | `RECOVERED` |
| `RECOVERY_VERIFYING` | material residual remains, limits permit | refresh/recompute new plan | `RECOVERY_PLANNING` |
| `RECOVERY_VERIFYING` | limits exhausted/unresolved | escalate without blind retry | `RECOVERY_FAILED` |

## Objective and sunk costs

QF-079 is authoritative for choosing `arg max ExpectedPortfolioValue_after` (equivalently minimum expected recovery loss) under Risk constraints. QF-080 measures Recovery Loss from the portfolio value at recovery start to after recovery. Loss already incurred before that state is sunk; it cannot justify unlimited slippage or notional.

A risk-reducing recovery may have negative standalone EV because exposure already exists, but must still satisfy dedicated freshness, maximum emergency slippage/notional, time, attempt, inventory, and infrastructure constraints. Exact numeric values are Risk/Calibration-owned.

## Candidate and split exits

For intermediate X, candidates can include intended B, original A, USDC/BTC/other permitted core inventory, or multiple exits. The graph supplies reachable candidates; Routing does not force the original route. Splitting 1,000 X as 600 to one destination and 400 to another is legitimate when it improves bounded expected portfolio value by reducing depth impact/slippage/tail risk.

Every child exit has its own immutable plan/intent identity, reservation, protected price, fill state, and accounting. Split children cannot double-reserve the same X. The combined actual fills determine residual exposure and QF-080.

## Failed/partial recovery

A failed, zero, partial, timed-out, or unknown recovery order never triggers a blind retry with the same assumed quantity. Sequence:

```text
reconcile -> refresh books/account -> recompute remaining actual exposure
-> enumerate candidates -> new recovery plan/version -> re-reserve -> execute
```

Recovery completes only after recovery orders are terminal-reconciled, actual exposure is within policy, reservations and balances agree, and Recovery/route accounting is emitted. Otherwise it remains active or becomes `RECOVERY_FAILED`.
