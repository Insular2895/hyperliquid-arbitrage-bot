# Survival versus Completion Separation

QF-048 and QF-085 answer whether acceptable edge survives to arrival (E1). `p_full` answers whether an attempted original route eventually completes (E4) within a declared label/scope. The former is opportunity-to-arrival; the latter is attempt-to-terminal outcome.

The historical attempt cohort is selected by the deployed survival, Risk, sizing and infrastructure policy. Its `p_full` may therefore statistically embed survival-related selection or features. The default integration is a single jointly calibrated Simulator distribution using survival evidence as an input.

A product such as `QF-048 × p_full` is allowed only after a separately versioned factored model proves that `p_full` is conditional on E1 and E2 in a compatible population, that no survival information is counted twice, and that the resulting joint forecast is calibrated. No such product is canonical in CORR-05.
