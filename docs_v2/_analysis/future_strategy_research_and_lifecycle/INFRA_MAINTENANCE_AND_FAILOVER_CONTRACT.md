# Infrastructure Maintenance and Failover Contract

Maintenance watches evidence freshness, host/kernel/container/build/network/feed changes, clock quality, tails, gaps, reconnects, Recorder loss and outcome degradation. Material drift makes the affected `InfraProfile` `REVALIDATION_REQUIRED`, `STALE` or `INVALID`; it does not retune the strategy automatically.

Failover must preserve exactly one active economic execution owner. A standby boots NON-READY, restores durable state, reconnects, reconciles exchange/account truth, proves fencing/ownership and passes readiness before any risk-increasing action. Naive active-active and dual writers are forbidden. Uncertain ownership or reconciliation remains fail-safe/NON-READY.

Release/rollback evidence binds build, config, schema, migrations, signatures, tests, Replay/Shadow evidence and observation window. Emergency rollback still reconciles before resuming.
