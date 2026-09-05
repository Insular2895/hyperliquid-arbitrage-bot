# Validation Map

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

`U` unit, `P` property/fuzz, `G` Formula golden, `R` Replay, `S` Shadow, `M` Micro-live. Micro-live is required only after upstream governance and never implied by this document.

| Contract | Evidence | Expected invariant | Failure condition | Authority |
|---|---|---|---|---|
| Directed conversion | U/P/G | direction and units are identity | ambiguous/inverted edge | SRC-003/004 |
| Base→Quote walk | U/P/G/R | consumes bids only | ask/mid used | QF-009 |
| Quote→Base walk | U/P/G/R | consumes asks only | bid/inverse used | QF-010 |
| Round trip | P/G | spread/fees prevent free zero-impact profit | artificial profit | QF-009–016 |
| Fee application | U/G/R/S/M | point-in-time rate/value/asset, once | missing/double/wrong debit | QF-014–016 |
| Quantization/price | U/P/G/R | legal conservative deterministic value | invalid rounded order | QF-007/008 |
| Minimum size/notional | U/P/G | every leg/output passes metadata | unusable output forwarded | QF-007/008/016 |
| NetConvert | U/P/G/R/S/M | exact side/L2/fee/precision output | unavailable depth or inconsistent result | QF-016 |
| Direct route | U/G/R | QF-017 equals one valid conversion | wrong terminal unit | QF-017 |
| 2-leg route | U/P/G/R | leg2 input equals valid leg1 output | gross/original amount reused | QF-018 |
| OWA comparator | U/P/G/R | same q/input/terminal/conventions | unmatched comparison | QF-017–020 |
| Missing comparator | U/P/R | OWA rejected; optional Bridge review | synthetic OWA created | SRC-003/004 |
| Triangle | U/P/G/R | exact start-asset closure | open path labelled Triangle | QF-021–023 |
| Route generation | U/P/R | same metadata yields same ordered set | nondeterministic/illegal route | SRC-001/005 |
| Route invalidation | U/P/R/S | dependency change removes current route | invalid route remains active | SRC-002/005 |
| `pair_to_routes` | U/P/R | forward/reverse dependencies agree | missing/extra RouteId | SRC-001/005 |
| affected lookup | P/benchmark/R | one update evaluates dependent routes only | graph-wide scan/wrong route | SRC-001/005 |
| Graph/Route versions | U/P/R | immutable consistent generation | mixed generation | PASS06/SRC-005 |
| point-in-time topology | R/checkpoint | listings/metadata as known at T | today's universe leaks back | PASS06 |
| HWC transitions | U/P/R/S | governed reversible transitions/hysteresis | churn/blind COLD/permanent HOT | SRC-001/002 |
| Atlas no-lookahead | R/OOS | evidence timestamp ≤ decision T | future evidence used | PASS06 |
| QF-001–043 | U/P/G/R | canonical units/sign/window semantics | alternative formula | SRC-004 |
| Rust/Python parity | G/R | exact canonical result | unexplained difference | SRC-006 |
| stale book/result | U/P/R/S | discard or revalidate | stale result advances | SRC-005/PASS06 |
| Edge(q) | U/P/G/R | each q walks/reserves actual depth | linear untouched-depth assumption | QF-026/027 |
| Participant boundary | U/R/S | prediction separated from mechanics | forecast embedded in NetConvert | PASS02/03 |
| Risk/Capital boundary | U/R/S/M | positive edge/HOT cannot bypass gates | direct authorization | PASS05/07 |

## Golden datasets

Formula Book cases must include symmetric/asymmetric books, multiple levels, both directions, partial/insufficient depth, fee debit variants, precision/minimum boundaries, sequential 2/3-leg routes and multiple q values. PASS11 owns exact vectors. Dataset manifests bind raw evidence, schema, formula, code/config and expected outputs.

## Property suite

- NetConvert output never uses more depth than present and never changes asset unit silently.
- Reversing a directed edge changes side/economics; a spread round trip is not an identity.
- An invalid comparator cannot produce QF-019/020.
- `Cycle3Leg.end_asset == start_asset` for every Triangle.
- Removing MarketId `m` leaves no active route whose dependency contains `m`.
- Same GraphVersion and generator rules yield identical RouteIds/order/index hashes.
- Route economics record every required BookVersion and reproduce from the manifest.
- Historical Graph/Atlas snapshots contain no observation or listing introduced after T.

## Promotion evidence

Unit/property/golden/parity precede deterministic Replay; temporal OOS precedes Shadow; stable predicted-vs-actual behavior and failure injection precede bounded Micro-live. Any data gap, semantic mismatch, version inconsistency, unexplained parity error or hard invariant failure blocks the affected capability.
