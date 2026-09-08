# Infrastructure Capture Attribution Contract

`STATUS: SPECIFIED — CORR-05 ECONOMIC OWNERSHIP DEFERRED`

## Evidence chain

```text
infra/feed treatment -> matched arrival/state validity -> state age at decision
-> EventToSend -> edge survival / would-attempt -> actual fill/completion/recovery
-> reconciled net economic outcome
```

Every link records population, denominator, IDs, time/clock validity, feed/infra/build/config/formula/model versions, missingness and uncertainty. No lower ping or shorter isolated stage implies capture or PnL.

Attribution categories are `FEED_ARRIVAL`, `FEED_GAP`, `RECONNECT`, `NETWORK_SEND`, `SCHEDULER_WAIT`, `CPU_COMPUTE`, `RECORDER_INTERFERENCE`, `CONTAINER_OVERHEAD`, `NODE_INTERFERENCE`, `EXCHANGE_RESOLUTION` and `UNKNOWN_ATTRIBUTION`. Unknown is valid. When causes coexist, use the existing sequential marginal/declared method so one loss is not charged fully to several stages.

QF-085 remains the modeled latency-survival interface. CORR-03 `FullRouteCompletionRate`, Recovery and `UNKNOWN` provide independent actual evidence. Do not multiply QF-085 capture, completion probability and another infrastructure capture factor until CORR-05 audits ownership/double counting. `QF-048` remains distinct from actual FullRouteCompletion.
