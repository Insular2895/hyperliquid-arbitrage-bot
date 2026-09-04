# 07 — Partial fills, dust, and intermediate buffers

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Non-loss rule

Partial fills are expected execution outcomes, not exceptions. For each order:

```text
q_remaining = q_requested - q_filled
```

within declared lot/rounding tolerance. Every new unique fill immediately updates cumulative filled quantity, actual VWAP, fees, asset delta, account/inventory versions, reservation consumption, and route/recovery inputs. The route never waits for “full” before acknowledging exposure.

## Universal partial algorithm

1. Deduplicate `FillEvent.fill_id`; duplicates produce no economic change.
2. Validate monotonic cumulative quantity and units; incompatible excess/out-of-order evidence triggers reconciliation.
3. Apply actual input/output, fee, and rounding to order, leg, inventory, and accounting.
4. Convert the corresponding reservation portion to actual exposure; keep the live/unknown remainder reserved.
5. Refresh relevant book/account/feed/clock state.
6. Quantize actual downstream quantity and test next-leg minimum notional.
7. Recompute price protection, depth, fees, edge, survival/participant/simulator inputs, and current Risk.
8. Compare best continuation with current Recovery alternatives.
9. Continue only the actual executable quantity; otherwise route current exposure to dust/buffer/recovery.
10. Persist transition/evidence asynchronously and expose structured metrics.

## Branch inventory

| Location | Partial outcome | Continuation | Residual |
|---|---|---|---|
| TT Leg 1 | actual X acquired; IOC residual canceled | Leg 2 on actual X if still best/valid | dust/buffer/recovery |
| TT Leg 2 | part becomes B | completed portion accounted | remaining X to Recovery |
| TTT Leg 1 | actual X acquired | Leg 2 on actual X | residual route exposure handled now |
| TTT Leg 2 | actual B acquired | Leg 3 on actual B | remaining X/B resolved separately |
| TTT Leg 3 | part returns to A | account actual A | residual B to Recovery |
| MT maker Leg 1 | actual X while remainder may rest | prompt taker hedge/continuation when executable | maker remainder still reserved/live |
| MTT maker Leg 1 | actual X | actual-size TT continuation | maker remainder plus later residuals tracked |
| recovery order | exposure reduced partly | recompute from new actual exposure | new recovery plan; no blind retry |
| fill during cancel | fill is real despite cancel request | manage new actual amount | only confirmed-unfilled remainder may release |
| fill observed after restart | exchange event supersedes incomplete journal | rebuild current continuation/recovery | reconcile all balances |

## Zero/full/partial distinctions

Zero fill means `q_filled = 0` with terminal exchange proof. First-leg zero aborts without later leg. A timeout, lost ACK, or missing order is not proof of zero.

Full means cumulative fill equals requested size within declared tolerance. It completes one order, not the route. Partial means strictly between; no generic `ORDER_FAILED` may erase it.

## Below-minimum partial

When quantized actual output is below the next order’s current minimum notional, the bot must not send an invalid next leg, round upward into unowned inventory, reuse theoretical output, or call the route complete. It records `DUST_EXPOSURE` and chooses among policy-permitted actions:

- retain as explicitly permitted minimal inventory/dust;
- aggregate in `PendingIntermediateBuffer`;
- convert/rebalance through another currently valid route;
- execute a bounded Recovery exit if possible.

Current minimum-notional, tick, lot, and rounding rules are exchange facts marked `EXTERNAL_REVALIDATION`; the internal response to a failed constraint is locked.

## `PendingIntermediateBuffer`

The buffer is temporary exposure storage, not a hidden balance pool. Aggregation requires all of:

- identical intermediate asset and compatible direction/settlement objective;
- compatible route/strategy context and Risk treatment;
- traceable contributing `ExecutionId`/`LegId`/`FillId` and cost basis;
- no cross-client/account/source mixing;
- current balance/inventory truth and no `UNKNOWN` constituent;
- compatible fee, rounding, minimum-order, and recovery policy;
- calibrated maximum age, total inventory, and adverse-move gates.

If any compatibility or bound fails, the entries stay separately attributable and route to recovery/rebalance/manual policy. Aggregation cannot net away a hard inventory breach or release reservations prematurely.

## Maker-specific accumulation

A 120-unit maker fill from a 500-unit order is 120 units of real exposure; the remaining 380 may still fill. If 120 is executable, evaluate its taker leg promptly. If it is not, buffer it only under the compatibility/bounds above while monitoring the resting/canceling maker remainder. Every additional fill re-runs the algorithm; it is not assumed to share the original edge.

When cancel is sent after partial fill, two activities coexist: manage already-filled exposure and resolve potentially live remainder. A later fill enlarges actual exposure and consumes reservation; a later cancel confirmation applies only to the residual then unfilled.

## Multi-asset residuals

A partial TTT path can leave X and B simultaneously. Recovery planning receives a vector of actual asset positions, not one “failed route amount.” Candidate exits may split by asset and destination. Inventory marks every residual immediately; Accounting keeps original route, recovery, inventory MTM, fees, and later rebalance distinct.

## Completion and tolerance

Route completion requires all orders terminal-reconciled, all fills known/applied, no unresolved buffer, intermediate exposure below an explicitly permitted per-asset dust tolerance, reservations reconciled, inventory updated, and actual PnL computed. “Below minimum order” alone is not permission to discard exposure.

Dust tolerance, buffer limits, age, adverse-move bound, compatible-context predicate, and recovery threshold are calibrated/open under Risk/Inventory/Data ownership. This pass locks the state semantics and evidence requirements, not numeric values.

## Required tests

Cover first/middle/final-leg partials for TT/TTT/MT/MTT, multiple partial events, duplicates, partial then full, partial then cancel, fill during cancel, partial below minimum, compatible/incompatible aggregation, buffer expiry, inventory-limit breach, fee/rounding-created dust, restart with buffered exposure, recovery partial, and simultaneous multi-asset residuals. Assert actual—not planned—quantity propagation at every boundary.
