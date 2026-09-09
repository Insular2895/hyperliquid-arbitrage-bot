# Size-Dependent Completion Contract

Completion is modeled as `p_full(q,state,scope)` where evidence supports that resolution. Reports bind q, size/depth ratios, route and market family, mode, latency/infra profile, regime, label version, observation cutoff and support counts.

Small probes do not validate larger orders. Missing support at q yields `UNSUPPORTED`/OOD and can contract `Q_validated`; it does not create a new numeric `p_full` Risk threshold. Neither monotonic completion decay nor monotonic economics is assumed. QF-077 must evaluate the declared search set with all gates at every candidate q.

Calibration may use supported bins, transparent smoothing or a promoted model, but extrapolation policy is explicit, conservative and versioned. Slicing an order cannot borrow the completion history of independent smaller routes without modeling shared state, sequencing and aggregate impact.
