# Public Feed Baseline Contract

`STATUS: INITIAL CANONICAL BASELINE`

The public Hyperliquid feed remains canonical until a challenger clears all applicable promotion gates. Baseline evidence records event arrival, valid feed age, continuity, gaps, duplicate/reorder, reconnect and time-to-healthy; CPU/memory/network; state age at decision/send; CORR-01 `EventToSend` and funnel counts; and CORR-03 attempt, completion, Recovery and `UNKNOWN` outcomes.

Correctness precedes speed. A baseline interval is invalid when identity, ordering, book reconstruction, clock, subscription/reconnect or source quality is unresolved. Missing data is explicit and cannot be treated as healthy.

Public-feed-first is not a claim of permanent superiority. It supplies the known comparator, lightweight V1 path and validated rollback target. Tokyo, provider, AZ and host remain experiment variables.
