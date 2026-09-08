# Speculative Precompute Reuse Contract

`STATUS: ALLOWED ONLY AFTER EXACT CANONICAL PARITY`

Each reusable artifact records speculative input fingerprint, expected canonical fingerprint, formula/model/metadata/fee/route/config versions, economically relevant fields, creation monotonic time, maximum lifetime, structural/economic class and invalidation reason.

## Reuse law

Economic reuse is allowed only when every relevant canonical value and version equals the speculative assumptions. The reused result must equal a fresh canonical recomputation under the normal numeric contract. One-lot quantity, price, ordering, fee, freshness, route, formula, model or config mismatch discards the economic result and recomputes.

Structural artifacts such as stable route IDs, decoded immutable metadata or prepared buffers may survive when their own narrower invariants hold. Structural reuse never implies economic reuse. Canonical computation wins on deadline, ambiguity, expired lifetime, missing fingerprint or parity failure.

Validation runs both paths and compares result, reasons, formula/model versions, route/size and DecisionTrace-visible outputs. “Close enough” is not permitted for exact execution economics.
