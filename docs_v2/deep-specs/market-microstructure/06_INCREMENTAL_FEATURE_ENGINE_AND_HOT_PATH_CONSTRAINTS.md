# Incremental Feature Engine and Hot-Path Constraints

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Ownership

Book Engine owns canonical books. Feature Engine owns deterministic incremental QF measurements. Route Engine owns topology. Opportunity Engine owns current route economics. Participants owns forecasts; Simulator owns distributions/counterfactuals; Risk owns eligibility; PASS07 owns sizing/allocation.

## Update model

Accepted book/trade events update only the relevant market accumulators and publish immutable FeatureSnapshot versions. BBO, depth, imbalance, OFI and rolling return/volatility aggregates use bounded state. Static metadata/route transforms are precomputed. Resets/gaps invalidate dependent accumulators until reconstructed.

## Hot path

Allowed: bounded in-memory lookups, incremental arithmetic, preallocated/bounded buffers, affected-route lookup and exact L2 walks over configured depth. Forbidden: blocking I/O, REST/service/database calls, full-history rescans, unbounded allocations, global graph search, model training or large Monte Carlo.

Production semantics live in Rust. Python is the reference/research/calibration/parity environment. A C++ layer is not a baseline; profiling and an explicit governed decision are prerequisites.

## Publication and backpressure

Single logical owners publish immutable snapshots/generations. Recorder remains off the decision path under PASS06 backpressure priorities. If required features are stale/unknown or publication is inconsistent, consumers fail conservatively rather than reading partial mutable state.

## Performance evidence

Latency, allocation and update-cost budgets are calibrated through benchmark distributions, not documentation constants. Performance optimization cannot alter Formula semantics, numeric determinism, provenance or Risk checks.
