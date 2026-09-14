# QF-071 Break-Even Boundary Audit

Let `U = BridgeCost + ExpectedExitCost` and `C = E[PnL_cycle]`.

| Case | Source-backed result |
|---|---|
| `U>0`, `C>0` | `N_BE=U/C` |
| `C<=0` | conceptual infinity / never break even |
| `U=0`, `C>0` | OPEN; typed unresolved |
| `U<0`, `C>0` | OPEN; typed unresolved; negative cycles forbidden operationally |

The source is silent on clamping, “already ahead” or a signed analytical/operational split. None is invented.
