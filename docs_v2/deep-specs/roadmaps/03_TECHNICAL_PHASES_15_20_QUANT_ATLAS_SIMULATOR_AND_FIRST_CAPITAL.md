# Technical Phases 15–20 — Quant, Atlas, Simulator and First Capital

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Boundary

These phases move from observe-only microstructure to the first controlled real TT measurement. Phase 20 is not “launch”; it is an M4 calibration instrument.

| Phase | Bootstrap capability | Later enrichment | Capital boundary |
|---:|---|---|---|
| 15 Quant Microstructure | Exact point-in-time QF-028–043 feature snapshots | Survival, response, maker, Risk/Atlas support | None |
| 16 Market Atlas | Structure, liquidity, opportunity counts/support | Survival, Q_validated, competition, execution quality, utility | None |
| 17 Sizing | Conservative q grid inside all known gates | Real fill/tail/capacity calibration | None until probe gate |
| 18 Simulator F0/F1 | History plus arrival/mechanical distributions | F2 queue/F3 response; F4 Research | None by Simulator itself |
| 19 Shadow | Full real-input, no-effect Core | Reused for every new release/market/model/q/host | None |
| 20 Micro-live TT | Tiny protected TT experiment | TT/TTT/model/capacity/infra calibration | Probe only |

## Observe before predict

Microstructure features are recorded and checked against offline recomputation before any model consumes them. The Atlas begins with available evidence and exposes missing support as UNKNOWN/LOW. Sizing may return zero. F0/F1 states exactly what it omits. This lets evidence accumulate without pretending future models already exist.

## Shadow proof boundary

Shadow can prove real-time stability, data freshness, decision consistency, live latency, would-execute behavior, support and evidence completeness. It cannot prove real ACKs, fills, queue priority, own impact, actual fees/cancel races or Recovery. Those become Stage-10 measurements.

## First capital vertical slice

```text
live event → exact TT opportunity → Risk → validated probe q
→ reservation → protected IOC Leg1 → actual fill
→ revalidate → protected IOC Leg2 → actual fills
→ bounded Recovery if required → accounting → reconciliation
→ predicted-versus-actual evidence
```

Every arrow has stable IDs/versions. A planned fill never updates actual inventory. An ambiguous submit never triggers blind retry. Any unresolved exposure freezes the affected resources.

## Probe interpretation

The source's `€40–50` is illustrative only. Probe q comes from current precision/minimum, Risk, inventory, book, preliminary support and explicit experiment limits. A successful probe does not validate larger q, another market, TTT or maker mode. A failed probe is retained and can demote or stop.
