# Formula Crosscheck

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

SRC-004 and `../FORMULA_INDEX.md` remain authoritative. PASS08 crosschecked names, direction, semantic inputs/outputs and consumers; it did not alter equations. PASS11 must audit exact rendering, variables and units, especially entries whose generated Formula Index locator is incomplete.

## QF-001–QF-043

| Range | Locked semantic family | Source locator | PASS08 use/check |
|---|---|---|---|
| QF-001–003 | Mid Price; Absolute/Relative Spread | SRC-004 3519–3640 | price vs ratio/bps distinct; mid never proves arbitrage |
| QF-004–006 | cumulative base/quote depth; band depth | 3651–3792 | units and side/band retained |
| QF-007–008 | size quantization; price validity | 3793–3847 | exchange-dependent metadata; revalidate |
| QF-009 | Book Walk Base → Quote | 3848–3913 | bids, base input to quote output |
| QF-010 | Book Walk Quote → Base | 3914–3971 | asks, quote input to base output |
| QF-011 | VWAP | 3972–4012 | derived from actual walk, not midpoint |
| QF-012–013 | BUY/SELL mechanical slippage | 4013–4120 | direction/sign conventions remain distinct |
| QF-014–015 | Fee Rate; Fee Amount | 4121–4181 | rate is not value; dynamic state and debit asset |
| QF-016 | NetConvert | 4182–4325 | one canonical economic output primitive |
| QF-017–018 | direct; sequential 2-leg output | 4326–4415 | same terminal unit; leg output feeds next leg |
| QF-019–020 | OWA relative edge; absolute gain | 4416–4493 | valid direct comparator required |
| QF-021–023 | triangular output/return/PnL | 4494–4616 | exact start-asset closure |
| QF-024–025 | Conversion Alpha; Execution Alpha | 4617–4739 | structural conversion vs execution-method advantage |
| QF-026–027 | Edge Curve; Maximum Profitable Size | 4740–4803 | size-dependent; not QF-076 |
| QF-028–029 | Queue/Multi-Level Imbalance | 4804–4925 | canonical measurements; predictive interpretation PASS02 |
| QF-030–033 | bid/ask OFI, OFI, MLOFI | 4926–5094 | true event flow distinct from snapshot proxy |
| QF-034–035 | Microprice; dislocation | 5095–5232 | feature, not guaranteed future fair value |
| QF-036–039 | log return; realized variance/volatility; jump score | 5233–5363 | clock/window provenance; threshold calibrated |
| QF-040–041 | depth and volume participation | 5364–5446 | ratios use explicit denominators/windows |
| QF-042 | Mechanical Impact | 5460–5515 | immediate book mechanics, not response forecast |
| QF-043 | Liquidity Resilience | 5516–5583 | response/recovery measure; predictive ownership PASS02 |

## Required cross-domain references

| QF | Meaning/status | PASS08 interface |
|---|---|---|
| QF-048 | Capture Probability, `LOCKED` | Atlas may store forecast evidence; PASS02 owns survival |
| QF-067 | Net Flow, `LOCKED` | Capital reachability/HWC context; PASS07 owns inventory use |
| QF-068 | Expected Exit Cost, `LOCKED` | Atlas may expose; PASS07 owns terminal/stranded semantics |
| QF-070 | Bridge Cost, `LOCKED` | route paths provide NetConvert; PASS07 owns relocation decision |
| QF-073 | Available Balance, `LOCKED` | activation/sizing consumer; Execution/PASS07 owns reservation truth |
| QF-074 | Available Book Capacity, `LOCKED` | route capacity input; PASS07 owns reservation allocation |
| QF-076 | Validated Capacity, `LOCKED` | may be displayed in Atlas; PASS07 owns all-gates capacity |
| QF-081 | Cross-Market Response, `LEARNED` | response graph is not conversion graph; PASS02 owns it |
| QF-082 | Correction Velocity, `LOCKED` | Atlas consumer; PASS02 owns predictive interpretation |
| QF-083 | Competition Hazard, `LEARNED` | Atlas consumer; PASS02 owns competition model |

## PASS11 flags

- QF-011's generated Formula Index currently shows an undefined expression locator although SRC-004 contains the authoritative section.
- QF-026 and other vertically rendered expressions are deliberately routed to PASS11 for exact reconstruction.
- Explicit unit auditing remains pending for all QF entries; PASS08 preserves semantic units and never substitutes a new expression.
- Current Hyperliquid fee, precision, minimum and L2 mechanics remain external revalidation items.

Crosschecked: **43/43** primary Quant formulas and **10/10** required cross-domain references. Formula changes: **0**.
