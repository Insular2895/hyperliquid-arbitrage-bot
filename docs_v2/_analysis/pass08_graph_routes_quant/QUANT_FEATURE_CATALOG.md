# Quant Feature Catalog

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

All expressions are authoritative in SRC-004 and `../FORMULA_INDEX.md`; this catalog specifies runtime semantics and interfaces only. `I` = incrementally maintained where applicable, `D` = derived on request, and hot-path `Yes` always means bounded in-memory computation.

| QF | Feature | Inputs → output units | Update/store | Hot | Consumers | Calibration/external |
|---|---|---|---|---:|---|---|
| 001 | Mid Price | bid/ask price → price | D/current | Yes | features, Atlas | none |
| 002 | Absolute Spread | prices → price | D/current | Yes | HWC, Risk | none |
| 003 | Relative Spread | prices → ratio/bps | D/current | Yes | routes, Atlas | convention locked |
| 004 | Cumulative Base Depth | levels → base units | I/derived | Yes | routes, sizing | K selection calibrated |
| 005 | Cumulative Quote Depth | levels → quote units | I/derived | Yes | routes, sizing | K selection calibrated |
| 006 | Depth Within Price Band | levels/band → quote/base depth | I/derived | Yes | Risk, Atlas | band calibrated |
| 007 | Size Quantization | size/metadata → valid size | D | Yes | NetConvert, Execution | exchange metadata revalidate |
| 008 | Price Validity | price/metadata → validity | D | Yes | NetConvert, Execution | exchange rule revalidate |
| 009 | Book Walk Base → Quote | base input/bids → quote output | D | Yes | NetConvert | L2 semantics revalidate |
| 010 | Book Walk Quote → Base | quote input/asks → base output | D | Yes | NetConvert | L2 semantics revalidate |
| 011 | VWAP | walk fills → price | D | Yes | slippage, impact | undefined on no fill per source contract |
| 012 | Mechanical Slippage BUY | ask walk/reference → ratio/bps | D | Yes | route/Risk | BUY convention locked |
| 013 | Mechanical Slippage SELL | bid walk/reference → ratio/bps | D | Yes | route/Risk | SELL convention locked |
| 014 | Fee Rate | fee/account/market/mode state → rate | state lookup | Yes | NetConvert | current schedule revalidate |
| 015 | Fee Amount | notional/rate → value/fee asset | D | Yes | accounting, route | debit asset revalidate |
| 016 | NetConvert | directed amount/book/fees/metadata → economic output | D | Yes | every conversion | central locked primitive |
| 017 | Direct Route Output | A amount/direct conversion → B | D | Yes | OWA comparator | state/version bound |
| 018 | 2-Leg Indirect Output | A→X→B sequential → B | D | Yes | OWA/Bridge | no intermediate approximation |
| 019 | OWA Relative Edge | indirect/direct B outputs → ratio/bps | D | Yes | OWA | comparator required |
| 020 | OWA Absolute Gain | indirect/direct B outputs → B | D | Yes | OWA/accounting | comparator required |
| 021 | Triangular Output | A→X→B→A → A | D | Yes | Triangle | exact closure |
| 022 | Triangle Return | start/end A → ratio | D | Yes | Triangle | size/state bound |
| 023 | Triangle PnL | start/end A → A units | D | Yes | accounting | reporting conversion separate |
| 024 | Conversion Alpha | indirect taker/direct taker outputs → ratio | D | Yes | Strategy | structural conversion advantage |
| 025 | Execution Alpha | execution-mode/baseline outputs → ratio | forecast interface | bounded | Execution/Simulator | model/mode dependent |
| 026 | Edge Curve | q grid/current economics → edge by q | D/cache by version | bounded | sizing, Atlas | grid calibrated |
| 027 | Maximum Profitable Size | Edge(q)/threshold → input units | search | bounded | sizing | threshold/search calibrated; not QF-076 |
| 028 | Queue Imbalance | best quantities → bounded ratio | I/current | Yes | Participants | predictive use PASS02 |
| 029 | Multi-Level Imbalance | weighted levels → bounded ratio | I/current | Yes | Participants/Risk | levels/weights calibrated |
| 030 | Event-Level Bid OFI Contribution | consecutive bid events → flow units | I/window | Yes | Participants | requires event fidelity |
| 031 | Ask OFI Contribution | consecutive ask events → flow units | I/window | Yes | Participants | sign convention locked |
| 032 | OFI | bid/ask contributions → flow units | I/window | Yes | Participants | not snapshot proxy |
| 033 | MLOFI | multi-level OFI → vector/aggregate | I/window | supported | Participants | levels/weights calibrated |
| 034 | Microprice | BBO prices/sizes → price | I/current | Yes | Participants, Atlas | feature, not fair-value guarantee |
| 035 | Microprice Dislocation | microprice/reference → price/ratio | I/current | Yes | Participants | horizon interpretation learned |
| 036 | Log Return | price series → log ratio | I/window | Yes | volatility/regime | sampling clock explicit |
| 037 | Realized Variance | returns/window → squared-return measure | I/window | Yes | Risk, Atlas | window calibrated |
| 038 | Realized Volatility | variance → volatility | I/window | Yes | Risk, HWC | window/scaling calibrated |
| 039 | Robust Jump Score | return/robust scale → score | I/window | bounded | Risk, HWC | threshold calibrated |
| 040 | Depth Participation | order/depth → ratio | D | Yes | Route/Risk/Sizing | band/depth definition bound |
| 041 | Volume Participation | order/market volume → ratio | D/window | bounded | Execution/Risk | window calibrated |
| 042 | Mechanical Impact | pre-book/walk VWAP → ratio | D | Yes | Simulator/Risk | not participant response |
| 043 | Liquidity Resilience | shocked/recovered depth/time → ratio | I/episode | forecast off fast path | Participants/Atlas | learned horizons/support |

QF-048, 067, 068, 070, 073, 074, 076, 081, 082 and 083 are cross-domain consumers/interfaces, catalogued in `FORMULA_CROSSCHECK.md`; they are not redefined here.
