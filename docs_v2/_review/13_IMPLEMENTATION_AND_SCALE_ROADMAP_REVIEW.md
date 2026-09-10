# Implementation and Scale Roadmap Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

The technical build order and scientific evidence journey remain separate. Completing a technical phase does not authorize the next phase or capital.

## Technical phases — 26/26

| Phase | Exact capability | Exit | Capital |
|---:|---|---|---:|
| 1 | Domain Types / Schemas | M1 foundations | None |
| 2 | Hyperliquid Adapters | M1 conformance | None |
| 3 | Recorder | M1 + continuous soak | None |
| 4 | Book Engine | M1 reconstruction | None |
| 5 | Metadata / Fee / Precision | M1 boundary rules | None |
| 6 | Graph / Routes | M1 structural routes | None |
| 7 | NetConvert / Formula Core | M1 golden parity | None |
| 8 | Replay Engine | M2 deterministic Core | None |
| 9 | Basic Opportunity Engine | M2 episodes | None |
| 10 | Account / Inventory / Reservations | M2 economic state | None |
| 11 | Risk Core | M2 constitutional gate | None |
| 12 | Execution State Machine | M2 emulated execution | None |
| 13 | Hyperliquid Execution Transport | M2 conformance; later M3 in Shadow | None |
| 14 | Recovery / Reconciliation | M2 replay; later M3 in Shadow | None |
| 15 | Quant Microstructure | M2 point-in-time features | None |
| 16 | Market Atlas | M2 structural/empirical map | None |
| 17 | Sizing | M2 supported q curves | None |
| 18 | Simulator F0 / Simulator F1 | M2 distributions | None |
| 19 | Shadow | M3 full no-effect chain | None |
| 20 | Micro-live TT | M4 TT probe | Probe only |
| 21 | Survival / Participant Models | M2/M3 model support | None directly |
| 22 | Advanced Simulator | F2/F3 M2/M3; F4 Research | None directly |
| 23 | MT / MTT | M4 per maker mode | Separate probes |
| 24 | Opportunity Portfolio | M2 then M4 | Promoted bounded only |
| 25 | Bridge / Capital Relocation | M2 then M4 | Separate probe/promotion |
| 26 | Scaling | M5 scoped/reversible | Scaled validated only |

## Phase 1 authorization boundary

Implement only strong venue/asset/market/route/execution/order/fill/evidence IDs; typed price, quantity, notional and time units; event envelopes; schema/snapshot versions; deterministic canonical ordering helpers; `Clock`; explicit `RngProvider`; `RunManifest` foundations; serialization/compatibility and property/unit/misuse tests.

Do not implement network access, Hyperliquid parsing, books, formulas, opportunity logic, strategy, Risk behavior, order transport/signing, execution effects, capital or deployment automation. Inputs are approved specs and small canonical fixtures. Phase 1 ends only when unit types cannot be mixed, schemas round-trip/version correctly, hidden time/randomness and incompatible/invalid/overflow inputs fail, and a versioned domain-contract M1 test report exists. Any ambiguous unit, owner or schema blocks the affected type.

Phase 1 is implementable from the reviewed documents: **YES, pending explicit human authorization of the exact reviewed commit.** Approval of Phase 1 does not approve Phase 2.

## Evidence journey

The 21 stages are: SPECIFY; OBSERVE/RECORD; RECONSTRUCT; MAP; IDENTIFY; REPLAY; SIMULATE; SHADOW LIVE; PREDICTED VS ACTUAL PREPARATION; LEARN COMPETITION/SURVIVAL; MICRO-LIVE; VALIDATE TT; VALIDATE TTT; MAKER INTELLIGENCE; VALIDATE MT/MTT; CAPITAL INTELLIGENCE; PORTFOLIO ALLOCATION; BRIDGE/CAPITAL RELOCATION; HORIZONTAL SCALE; VERTICAL SCALE; INFRASTRUCTURE SCALE.

The governing chain remains `SPECIFICATION → IMPLEMENTATION → EVIDENCE → VALIDATED CAPABILITY → CAPITAL`. See the two canonical [roadmaps](../17_IMPLEMENTATION_ROADMAP.md) and [evidence journey](../19_BUILD_VALIDATE_SCALE_ROADMAP.md).

CORR-06 adds no Phase 27 or evidence stage. Phase 3 records multi-VPS/priority evidence, Phase 8 applies stored profiles, Phase 19 compares without effects, Phase 20 obtains actual priority/fill/completion evidence only after separate authorization, and Phase 26 selects/revalidates the winner. Permanent challenger rental is not required; profiles are reusable but freshness-gated.

Async/concurrency adds no Phase 27 and changes no responsibility. The first baseline is mostly inline and ordered; async adapters/effects, bounded Recorder/background work and scheduler-permuted Replay are integrated into their existing phases. Worker fanout, parallel q-grid, pool sizing and route policy remain profiling/Replay/Shadow candidates. Phase 1 remains types/schemas only and is still unauthorized.
