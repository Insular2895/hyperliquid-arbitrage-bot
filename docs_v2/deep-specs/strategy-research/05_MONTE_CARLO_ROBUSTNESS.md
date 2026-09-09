# 05 — Monte Carlo Robustness

STATUS: FUTURE SPECIFIED / NOT ACTIVE

Monte Carlo is an ensemble driver over the existing canonical Simulator and its one versioned `Π_exec(q,state)` economic truth. It is not a second fill engine, PnL formula book, accounting ledger or Risk authority.

## Inputs

Each run pins `RunManifest`, Dataset and temporal scope, `StrategySpec`, Simulator fidelity, Formula/fee/metadata/Book/model/InfraProfile versions, seed tree, path count, sampling method, conditioning variables, fallback policy and software build. Replay precedes Monte Carlo and proves deterministic reconstruction.

Distributions are empirical/bootstrap or otherwise calibrated from real supported observations. Arbitrary Gaussian noise is forbidden. Sampling respects domain support, censoring, tails and dependence. Measured correlated vectors are resampled coherently; independent marginals may be used only with validated independence or an explicit sensitivity-only label. Sparse/OOD strata fall back, abstain or remain `UNAVAILABLE`.

Potential stochastic dimensions—only with evidence—include feed/local/scheduler latency, jitter, Opportunity lifetime, market/participant response, liquidity withdrawal/refill, cancel timing, slippage, F/P/R/X outcomes and costs, priority effect/charge, lead-lag and volatility/liquidity/regime transitions. Conditioning complexity backs off visibly when support is insufficient. Historical, alternative plausible and stress-heavy regime mixtures/sequences remain distinct scenario assumptions.

## Economics and failures

Every path invokes canonical Simulator scenario composition. Fees, executable book walk, priority charges, Recovery, inventory and external penalties are included exactly once under existing ownership. Zero-fill, partial, Recovery, negative, unresolved/censored and invalid paths remain in coverage and diagnostics; they are not silently dropped.

## Outputs

Required outputs include path count/effective support, seed lineage, expected and median outcome, quantiles and confidence intervals, loss probability, tail loss/shortfall measures, completion/Recovery partitions, drawdown or path-dependent risks when meaningful, sensitivity, correlation assumptions, failure/censoring rates, convergence diagnostics and scope limits.

Model outputs are uncertain estimates, not constants. Parameter uncertainty, calibration error and plausible misspecification are perturbed explicitly where supported. More simulated paths cannot create missing evidence: one hundred million paths through a bad fill model remain wrong.

Stress/adversarial suites include latency/jitter/feed degradation, Opportunity-lifetime collapse, partials, Recovery probability/cost, priority benefit/cost, volatility/liquidity/correlation/regime change, lagging markets and VPS degradation. These are robustness tests, not predictions. A mild plausible stress with catastrophic behavior rejects or narrows the candidate.

Same Dataset, `StrategySpec`, config, models, seed, sampling implementation, FormulaVersion and declared numerical policy reproduce the same path trace/output distribution. Monte Carlo cannot raise `Q_validated`, establish actual fills or replace Shadow/Micro-live.
