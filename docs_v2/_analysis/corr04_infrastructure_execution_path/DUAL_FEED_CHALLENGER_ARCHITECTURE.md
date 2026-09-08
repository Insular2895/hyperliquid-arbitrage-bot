# Dual-Feed Challenger Architecture

`STATUS: SHADOW / OBSERVE-ONLY`

| Plane | Public baseline | Node challenger |
|---|---|---|
| normalized state | canonical adapter contract | isolated challenger representation |
| writer authority | exactly one canonical `MarketState` writer | no canonical mutation |
| execution authority | existing single Core/Risk/Execution owner | none |
| outputs | canonical events/state/decisions | matched timing, parity, gaps, Shadow opportunities |
| Recorder | canonical source class | separately tagged source/build/epistemic class |

Feed fusion is not authorized. A conflict is evidence, never resolved by last-arrival-wins. Dual-feed pressure must not cause loss of P0/P1 account/execution evidence. A canonical switch is a versioned feed-profile transition followed by state rebuild, readiness and reconciliation; it is not a hot merge.

Real-order A/B from two engines on one account is forbidden. Safer future designs are paired Shadow, alternating canonical intervals or explicitly authorized isolated accounts with independent capital and ownership.
