# 06 — Maker execution, MT/MTT, and disabled modes

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

## Maker lifecycle

The canonical machine does not add a special `SUBMITTED` enum: intent progresses through `SENT`, known `RESTING`, `PARTIALLY_FILLED`, `FILLED`, `CANCEL_REQUESTED`, `CANCELED`, `REJECTED`, `UNKNOWN`, and `TERMINAL_RECONCILED` as evidence allows.

A maker policy is ALO/post-only subject to current exchange revalidation. While `RESTING`, Execution consumes:

- current route edge and Edge Survival forecast;
- QF-051/052 fill survival/CDF and QF-053 expected fill time;
- QF-054/055 adverse selection;
- queue observability/model confidence from Participants/Simulator;
- inventory hard/soft limits and current reservations;
- market/account feed freshness and regime.

The maker order is canceled when continued resting is no longer permitted or economically supported. “Maker stale” is the result of these gates, not a fixed duration.

## Maker maximum age

`MAKER_MAX_AGE` is calibrated as a function of fill distribution, edge survival, adverse selection, and regime. A timer merely initiates current evaluation/cancel; it does not prove cancellation or permit reservation release. Universal constants such as 500 ms are examples, not requirements.

## MT

MT is maker `A -> X`, then taker `X -> B`.

- A full maker fill produces actual X and a current taker-continuation/recovery decision.
- Each economically executable partial produces actual X immediately and is evaluated for the taker hedge/continuation; it is not left unmanaged until the maker finishes.
- The unfilled maker remainder may continue resting only if route/Risk/age/freshness remain valid.
- A below-minimum partial enters `PendingIntermediateBuffer`, dust, or recovery policy with explicit exposure.
- On edge deterioration, cancel the maker remainder while assuming it may still fill; concurrently manage already filled exposure.

QF-058 expresses MT EV. Execution consumes it without rewriting or treating a point estimate as exchange truth.

## MTT

MTT is maker `A -> X`, then two protected taker legs. Every maker partial/full becomes an actual-size TT continuation. Both later taker legs repeat current-state validation and independently branch on zero/full/partial/reject/unknown. A canceling maker remainder can create additional fills, each deduplicated and added to current exposure before any new taker intent.

## TM/MM boundary

| Mode | Type representable | Enabled initially | Capital validated | Reason |
|---|---:|---:|---:|---|
| `TM` | yes | no | no | second maker wait follows real first-leg exposure |
| `MM` | yes | no | no | multiple resting/partial/cancel races compound exposure |

Activation requires explicit human/strategy enablement, calibrated queue/fill and adverse-selection models, dedicated Risk limits, partial/dust/cancel/recovery tests, and Shadow/Micro-live evidence. Passing type checks or Replay mechanics is not capital validation.

## Feed and Dead Man’s Switch response

Market-feed staleness stops new maker risk and requests cancellation under policy. Account/order/fill-feed loss is more severe: stop new risk, keep remaining quantity economically possible, use HTTP/query reconciliation, and do not release reservations. The Dead Man’s Switch is supplemental protection for resting orders only; its current exchange rules remain external.
