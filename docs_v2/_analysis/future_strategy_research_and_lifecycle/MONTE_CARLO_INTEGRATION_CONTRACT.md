# Monte Carlo Integration Contract

Monte Carlo repeatedly drives the existing versioned Simulator under a pinned manifest. It neither recreates `Π_exec(q,state)` nor owns formulas, fill truth, accounting or permission. Search selects configurations; the Simulator evaluates one path/scenario; Monte Carlo summarizes coherent ensembles.

Only calibrated support-aware distributions may be used. Empirical/bootstrap methods are preferred; arbitrary Gaussian noise is forbidden; correlations and censoring are preserved. Fees, book walk, priority, Recovery, inventory and penalties remain exact-once. Full details: [Monte Carlo Robustness](../../deep-specs/strategy-research/05_MONTE_CARLO_ROBUSTNESS.md).
