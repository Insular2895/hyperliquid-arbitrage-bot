# Execution PnL Distribution Contract

`Π_exec(q,state)` denotes the one versioned execution-outcome distribution for a frozen candidate. It records label/scope, q, state/features, formula/model/fee/book/infra versions, F/P/R/X probability mass, scenario cashflows, support/OOD/confidence and unresolved coverage.

Required properties:

1. probabilities are nonnegative and sum to one only under the declared exhaustive resolved profile;
2. unresolved/censored/invalid coverage is disclosed outside F/P/R/X;
3. fees, slippage/book walk, partial-path effects and Recovery execution economics occur once inside scenario cashflows;
4. QF-056 EV, QF-059 positive-PnL probability and tail measures derive from the same distribution;
5. point estimates never erase distribution tails;
6. actual outcomes later reconcile against, but never rewrite, the frozen forecast.

If support is absent or OOD, the artifact is unavailable/restricted rather than silently replaced by certainty or a favorable fallback.
