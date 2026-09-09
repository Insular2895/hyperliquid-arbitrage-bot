# Multi-VPS Calibration Protocol

## Design

Run candidate VPS recorders simultaneously over the same market intervals. Sequential weekday/provider comparison is insufficient for primary relative claims because regime, volatility, opportunity density and network topology confound it.

## Required controls

- same build, config, subscriptions, feed mode, workload, instrumentation and capture policy;
- per-host monotonic stage timing plus synchronized wall clock, offset and uncertainty;
- immutable source/feed/infra/build/kernel/container/network identity;
- authoritative event identity or deterministic semantic fingerprint;
- P0/P1 Recorder preservation and explicit drops/backlog/interference;
- enough matched events, regimes, time-of-day, volatility and opportunity support for the claim—no hard calendar duration.

## Outputs

Report paired arrival lead/lag, P50/P95/P99/P99.9 and meaningful max, jitter, ordering, gaps/duplicates, state-publish and compute distributions, CPU steal/scheduler/migrations/memory, reconnect/availability, Recorder penalty and clock-valid/inconclusive/unmatched counts. A result within combined clock uncertainty is `INCONCLUSIVE`.

Create one versioned profile per candidate and preserve the raw campaign Dataset. Economic selection includes tails, reliability, security/operations and incremental cost. A candidate cannot win on mean or advertised ping alone. After selection, challenger rentals may stop; a later candidate is briefly paired against the current winner and produces a new profile version.
