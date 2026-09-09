# Fee and Priority-Cost Ownership

Exchange/trading fees are applied through QF-016 in each executed scenario path exactly once, including debit-asset and rebate semantics. Infrastructure recurring cost remains the infrastructure/accounting bucket.

Current priority mechanisms revalidated 2026-09-09 have typed owners:

| Cost | Basis | Exact-once owner |
|---|---|---|
| gossip/read auction | winning slot/auction charge in HYPE from spot balance | feed/infrastructure experiment and global infra accounting |
| IOC write priority | grouping rate × filled notional; zero fill therefore zero priority charge | affected IOC execution scenario |
| ALO write priority | grouping rate × resting notional, charged at placement regardless of fill | affected ALO execution scenario |

Do not also label write priority as normal QF-014 exchange fee or gossip auction spend as action fee. Requested policy, actual charge and observed benefit are separate. Benefit changes `Π_exec` only when supported; it is not a cash credit or extra multiplier. Activation still requires bounded policy, current facts, validation, Risk compatibility and human authorization.
