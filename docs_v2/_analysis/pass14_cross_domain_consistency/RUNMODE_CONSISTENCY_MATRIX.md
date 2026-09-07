# RunMode Consistency Matrix

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| `RunMode` | Market/account source | Effect transport | Real account mutation | Clock | Same Core/Risk/reducers? | Claim limit |
|---|---|---|---:|---|---:|---|
| `Replay` | recorded ordered events | emulator/simulated | NO | `ReplayClock` | YES | historical/counterfactual only as declared |
| `Paper` | live or replay market, synthetic account | paper | NO | source-appropriate | YES | no real fill/fee/impact claim |
| `Shadow` | live inputs, separate shadow projection | no-effect `NullShadowTransport` | NO | live clocks | YES | no real queue/fill/causal impact |
| `MicroLive` | live market/account | real protected transport | YES, probe scope only | live clocks | YES | exact calibrated probe scope |
| `Live` | live market/account | real protected transport | YES, promoted bound | live clocks | YES | exact current manifest/readiness/Risk scope |

`Micro-live` and `MICRO-LIVE` are narrative/maturity labels; the serialized `RunMode` value is `MicroLive`. `EXACT RECEIVE-TIME`, `ACCELERATED`, `COUNTERFACTUAL LATENCY`, `INTERACTIVE` are Replay submodes, not RunModes. F0–F4 is Simulator fidelity. TT/TTT/MT/MTT/TM/MM is execution mode. M0–M5 is maturity.

RunMode-specific risk bypasses: **0**. Alternate strategy equations or state machines by RunMode: **0**.
