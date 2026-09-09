# 07 — Overfit and Multiple-Hypothesis Control

STATUS: FUTURE SPECIFIED / NOT ACTIVE

Every adaptive choice consumes evidence. The experiment family records hypotheses, features, parameter points, objectives, windows, seeds and manual reruns considered—not only the final winner.

Before search, declare the family and primary metrics. Apply a justified family-wise or false-discovery control where inferential claims are made; otherwise label results exploratory and require independent confirmation. Sequential/adaptive search records the selection path and cannot present naive post-selection intervals as confirmatory.

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
