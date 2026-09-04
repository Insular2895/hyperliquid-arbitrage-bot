# 05 — Taker execution, TT, and TTT

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Protected taker contract

Every taker leg is a protected IOC/marketable limit: it can match immediately only inside the approved worst-price bound and its residual is canceled rather than left resting. BUY limit is bounded by the maximum acceptable price; SELL by the minimum. Unbounded market execution is rejected by the canonical design.

Before intent creation, size/price pass QF-007/008 quantization/validity. Expected book walk uses QF-009/010; actual fills determine QF-011 VWAP, QF-012/013 slippage, QF-014/015 fees, and QF-016 net conversion. The Simulator forecast is not execution truth.

## Per-leg decision algorithm

```text
current snapshot + RiskDecision + reservations + immutable plan
-> current pre-send validation
-> protected intent -> nonce/sign/send
-> resolve actual fills/order terminality
-> update inventory/reservations/accounting
-> classify zero / full / partial
-> refresh book + forecasts + Risk from actual quantity
-> continue, abort, or recover
```

| Outcome | Known exposure | Next action | Prohibited |
|---|---|---|---|
| zero fill, terminal-known | none from this leg | first leg: `ABORTED`; later leg: Recovery for prior exposure | sending next leg |
| full fill | actual output less fees/rounding | recompute and revalidate next leg | theoretical planned-size continuation |
| partial fill | actual partial output | continue smaller if executable/best/permitted; otherwise recover | pretending full or zero |
| reject/no-fill from price protection | no new fill in this leg, prior legs may exist | abort if first; recover if later | widening limit outside approval |
| unknown submit/status | exposure may exist | lock, query, reconcile | resend/new use of funds |

## TT

TT is `A -> X` taker then `X -> B` taker.

1. Leg 1 zero fill: route `ABORTED`, no Leg 2, all proven-unused reservations released after terminal reconciliation.
2. Leg 1 full: compute actual X from fill prices, quantities, fees, and rounding; refresh Leg 2 arrival state and compare continuation with current recovery alternatives.
3. Leg 1 partial: repeat step 2 only for actual X. If below Leg 2 minimum, enter dust/buffer/recovery policy.
4. Leg 2 full: close only after all order/fill/inventory/reservation/PnL conditions.
5. Leg 2 partial: completed fraction reaches B; residual X enters Recovery.
6. Leg 2 zero/reject/unknown: prior X remains real or potentially real; Recovery/Reconciliation is mandatory as appropriate.

## TTT

TTT is `A -> X -> B -> A`, all protected taker legs. It is not atomic even when requests are sent rapidly or batch-compatible.

After Leg 1 and again after Leg 2, Execution uses actual acquired inventory to compare `EV_continue` with `EV_recovery`, current protection, minimum notional, book depth, survival/response forecasts, and Risk. Any zero, partial, reject, timeout, or unknown is classified independently.

Leg 3 full does not alone prove route completion: all fills, fees, residual assets/dust, reservations, inventory, and accounting must reconcile. Leg 3 partial or failure produces residual intermediate/final asset handled from current portfolio state.

## Price-protection failure

An IOC unable to match inside its limit is a safe known no-fill only when exchange evidence proves the outcome and no ambiguous transport remains. It must not be “fixed” by silently increasing the bound. A new price bound requires current simulation/Risk and a new plan/intent version.

## Validation obligations

Golden/fault tests cover every leg position with zero/full/partial/reject/unknown, actual-fill size propagation, fee/rounding effects, price-bound preservation, duplicate fills, lost response after real fill, and terminal route closure. The three-leg cross-product is sampled with invariant/property tests rather than assuming only happy-path order.
