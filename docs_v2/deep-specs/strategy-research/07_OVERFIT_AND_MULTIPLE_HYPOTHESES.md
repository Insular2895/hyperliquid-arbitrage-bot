# 07 — Overfit and Multiple-Hypothesis Control

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / NOT ACTIVE`

Every adaptive choice consumes evidence. The experiment family records hypotheses, features, parameter points, objectives, windows, seeds and manual reruns considered—not only the final winner.

Before search, declare the family and primary metrics. Apply a justified family-wise or false-discovery control where inferential claims are made; otherwise label results exploratory and require independent confirmation. Sequential/adaptive search records the selection path and cannot present naive post-selection intervals as confirmatory.

The family includes every Structure/Hypothesis, StrategyFamily/spec version, feature set,
configuration, route/market/regime scope, objective, split, seed, scenario, manual rerun and
selection-rule variant actually considered. AI proposals and abandoned branches consume the same
selection ledger; they are not invisible “brainstorming” once results influenced the next choice.
Worker failure and infrastructure retry are tracked separately from economic failure, but neither
may disappear from coverage.

Required robustness evidence includes:

- untouched temporal OOS and walk-forward;
- sensitivity/stability surfaces around the candidate;
- comparison with simple and frozen baselines;
- multiple seeds/paths where stochastic;
- realistic fees, liquidity, latency, priority and failure economics exactly once;
- regime and support slices, including worst supported slices;
- failed, censored and invalid attempt coverage;
- effect size and uncertainty, not p-value or peak PnL alone;
- degradation tests and negative controls where feasible.

Red flags include isolated sharp optima, parameter boundary attraction, unstable rankings, high turnover sensitivity, gains confined to one period/asset, unsupported feature availability, result reversal after costs, repeated holdout access and undocumented researcher degrees of freedom.

An experiment report states what was learned even when the candidate loses. Negative evidence is retained and linked to prevent rediscovery loops.

Scheduler completion order cannot define a winner. Deterministic decision boundaries, eligible
result sets and tie rules are frozen; reports present a stable canonical order independent of
worker arrival. Dashboard filtering cannot change the inferential family or overwrite machine
facts. If researcher degrees of freedom or missing selection history are material, the result is
exploratory or `INCONCLUSIVE`, not retrospectively confirmatory.
