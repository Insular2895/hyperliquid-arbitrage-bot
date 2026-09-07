# Data–Replay–Live Consistency Audit

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

| Invariant | Replay | Shadow | MicroLive/Live | Result |
|---|---|---|---|---|
| same normalized event schemas | recorded source | live source | live source | PASS |
| same reducers/Core | YES | YES | YES | PASS |
| same formula/config/model identity rules | manifest-bound | manifest-bound | manifest-bound | PASS |
| explicit clock | ReplayClock | live clocks | live clocks | PASS |
| explicit RNG | manifest seed | recorded/versioned outputs as material | recorded/versioned outputs as material | PASS |
| account state separation | simulated | shadow separate from actual | actual exchange account | PASS |
| transport/effects | emulator | no-effect | real protected | PASS |
| actual claim | simulated-labeled | would-* only | exchange-observed/reconciled | PASS |
| invalid/gap handling | reject/low-fidelity by claim | no optimistic state | no new risk in affected scope | PASS |
| trace/evidence | DecisionTrace/hash | would-decision plus observed future | intent/fill/fee/recovery/PnL | PASS |

L0 RAW remains immutable historical evidence; L1–L4 cannot replace it. A compatible checkpoint accelerates reconstruction but never overrides the journal or exchange truth. Evidence binding now uses typed references without changing frozen RunManifest fields. Replay-only strategy shortcuts: **0**. Hidden future-state consumption: **0**.
