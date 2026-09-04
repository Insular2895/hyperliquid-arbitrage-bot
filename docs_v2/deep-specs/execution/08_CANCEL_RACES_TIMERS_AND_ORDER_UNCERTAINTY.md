# 08 — Cancel races, timers, and order uncertainty

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Cancel is a request, not truth

```text
cancel sent != canceled
```

From `RESTING` or `PARTIALLY_FILLED`, a cancel effect produces `CANCEL_REQUESTED`. It does not release the remaining reservation or assert zero future fills. Only exchange evidence that the order is inactive, combined with all known fills and balance effect, permits `CANCELED` then `TERMINAL_RECONCILED`.

## Canonical race

```text
T0 cancel sent
T1 another participant matches remaining order
T2 fill observed/applied
T3 cancel response says already filled or only residual canceled
```

The reducer accepts either arrival order. Stable fill identity prevents double application. The fill updates exposure and may launch continuation/recovery even while cancel resolution continues. Cancel confirmation applies to the then-unfilled remainder only.

Lost cancel response moves resolution toward `UNKNOWN`/reconciliation; it does not justify another cancel/order sequence that assumes inactivity. Cancel by OID/CLOID support is an external exchange fact.

## Send and ACK uncertainty

| Boundary | What is known | Safe response |
|---|---|---|
| signing fails | nothing transmitted if effect layer proves it | local structured failure/replan |
| transport fails before transmission is provably possible | no exchange order | safe abort/new version |
| send began or transmission may have occurred | economic effect possible | `SENT`; retain reservations |
| ACK lost/timeout | outcome unknown | `PENDING_RESOLUTION` then query/reconcile/`UNKNOWN` |
| HTTP status OK | request envelope processed only | wait for economic events/status |
| exchange explicit reject | no fill for that order unless conflicting evidence | map reason and reconcile |

The protocol is CLOID lookup, order/open-order/fill queries, balance comparison, then resolution. `NO BLIND RETRY` is absolute.

## Timers as deterministic events

SRC-005 exact `TimerEvent` values are `RiskRecheck`, `MakerExpiry`, `UnknownResolutionTimeout`, `ReconciliationTrigger`, and `MetricsFlush`. ACK, route, recovery, and reconciliation deadlines may be represented through the Data-owned event schema; this pass does not add enum fields.

Timer values come from observed/calibrated distributions and risk context:

- ACK: observed ACK latency tail plus validated margin;
- maker maximum age: fill distribution, edge survival, adverse selection, regime;
- route: edge lifetime, execution mode, inventory risk;
- unknown/reconciliation/recovery: operational evidence and risk policy.

Timer firing is a condition to evaluate, not proof of reject, cancel, or zero fill.

## Dead Man’s Switch

While relevant resting orders exist, a schedule may be refreshed so complete bot death causes future cancel-all. It is supplemental safety, mainly for maker/resting orders, not IOC and not normal cancellation. A trigger itself still requires subsequent reconciliation of fills/orders/balances. Exact current deadlines, limits, scope, and API semantics remain `EXTERNAL_REVALIDATION`.

## Finality

`FILLED`, `CANCELED`, and `REJECTED` describe known order outcomes; none releases all resources until `TERMINAL_RECONCILED`. Finality requires final exchange status, all known unique fills, balance/account effect, inventory, fees, and reservation conversion/release to agree. Any contradiction sends the order/route to reconciliation and blocks affected new risk.
