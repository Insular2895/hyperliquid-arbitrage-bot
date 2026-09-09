# Priority Cost and Outcome Ownership Audit

| Mechanism | Technical effect under current docs | Cost owner | Benefit owner | Forbidden duplication |
|---|---|---|---|---|
| gossip/read | peer propagation/arrival distribution | feed/infrastructure experiment, once | changed profile/arrival inputs to one outcome distribution | infra cost plus execution fee |
| IOC write | effective time/mempool ordering | affected IOC scenario, filled-notional basis | changed `Π_exec(q,state)` | QF fee plus priority charge twice; extra capture multiplier |
| ALO write | recent-tail price-level queue position | affected ALO scenario, resting-notional at placement | changed maker queue/fill outcome distribution | IOC logic; cost only on fill; extra fill multiplier |

Policy, eligibility, requested rate/slot, actual charge, sequencing observation and outcome are distinct. A paid policy can fail to improve outcomes or can cost more than it recovers. QF-048/QF-085 survival, completion evidence and priority are conditioning/calibration evidence for one distribution, not independent products.

No PriorityOptimizer is specified. First use is matched policy A/B/C comparison through existing Replay/Shadow/Micro-live progression. Risk, price protection, Reservations, actual-fill truth and `Q_validated` remain dominant.
