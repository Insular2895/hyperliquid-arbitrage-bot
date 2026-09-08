# Cross-Feed Event Alignment Contract

`STATUS: SPECIFIED`

## Match order

1. Prefer a documented common block/sequence/event identity with the same market and semantic type.
2. Otherwise use a versioned deterministic fingerprint over normalized economically relevant fields and source context.
3. Reject ambiguity, many-to-one collisions, snapshots-vs-diffs, incomplete payloads and nearest-time-only matches.

Every pair stores both raw IDs, payload hashes, semantic/fingerprint version, receive wall/monotonic times, clock quality, source/build/flags, match confidence/status and rejection reason. No matched event may be selected using later economic outcome.

Same-host receipt uses one monotonic domain. Cross-host comparison requires synchronized clocks and combined uncertainty. A lead not exceeding uncertainty is neither a win nor loss. Different upstream routes mean the result is an end-to-end delivery-topology effect, not pure protocol latency.
