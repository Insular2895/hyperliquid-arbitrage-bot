# 05 — Market Microstructure

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## 1. Purpose

This master defines the semantic and runtime contracts for the canonical QF-001–QF-043 market/microstructure feature family. It tells future engines what inputs, units, provenance and ownership are required without recreating the Formula Book.

## 2. Formula authority

SRC-004 QF-001–QF-043 is authoritative. [`FORMULA_INDEX.md`](./_analysis/FORMULA_INDEX.md) provides stable locators and [`FORMULA_CROSSCHECK.md`](./_analysis/pass08_graph_routes_quant/FORMULA_CROSSCHECK.md) records PASS08 review. Equations, variables and formal units remain PASS11 audit scope. Earlier divergent expressions are superseded; a model or Atlas update cannot rewrite locked formulas.

## 3. Market state inputs

Quant consumes canonical immutable `BookSnapshot`/`BookState`, explicit market/base/quote identities, fixed/exact numeric values, event/exchange/receive/process times, source quality/freshness, metadata/fee/formula versions and configured windows. PASS06 owns schemas and point-in-time state. Missing, stale, gapped or incoherent inputs remain invalid/unknown rather than being imputed as current truth.

## 4. Mid / Spread

QF-001 Mid Price is a descriptive BBO reference. QF-002 Absolute Spread returns price-unit distance; QF-003 Relative Spread returns a dimensionless/bps representation. Mid is not executable price and must not prove arbitrage. Cross-market comparison must preserve quote/unit compatibility.

## 5. Depth

QF-004 Cumulative Base Depth measures summed base quantity through selected levels. QF-005 Cumulative Quote Depth expresses notional depth. QF-006 measures depth inside an explicit price band and side. Level count/band/horizon are parameters with provenance, never unlabeled universal constants. Depth cannot be reused after its BookVersion is stale.

## 6. Exact book walk

QF-009 walks Base→Quote through bids; QF-010 walks Quote→Base through asks. Walks start at best price and consume only displayed valid depth until input, protection boundary or book capacity is exhausted. Input/output units, filled/residual quantities and consumed levels remain explicit. An inverse or midpoint approximation is invalid.

## 7. VWAP

QF-011 is derived from actual book-walk fills. It is undefined/invalid when the authoritative contract has insufficient fill evidence; it is not silently replaced by midpoint. VWAP carries side, quantity and BookVersion because it is size/state-specific.

## 8. Slippage

QF-012 Mechanical Slippage BUY and QF-013 SELL preserve their distinct reference/sign conventions. Slippage describes the realized book walk relative to the appropriate best-side reference; it is not an extra cost subtracted after `NetConvert` has already used those prices.

## 9. Fees

QF-014 produces a fee **rate** from point-in-time account/market/mode state. QF-015 produces a fee **amount/value** in an explicit asset. These concepts cannot be interchanged. Fee tiers, discounts, quote treatment and debit asset change over time and require external revalidation. One versioned Fee Engine supplies Graph, Execution, Replay and Accounting.

## 10. Precision / validity

QF-007 size quantization and QF-008 price validity use exchange metadata. Rounding must be conservative and reproducible; size/price digits, lot/tick and minimum quantity/notional cannot be guessed or hardcoded from examples. The output legal for one leg becomes the exact input considered for the next. Current Hyperliquid rules are external dependencies.

## 11. NetConvert link

QF-016 combines directed L2 conversion, fees and validity into economic output. It is the only canonical conversion primitive. All direct, indirect, Triangle, Bridge, Rebalance and Recovery economics call the same semantic contract and avoid double-counting. See [NetConvert](./_analysis/pass08_graph_routes_quant/NETCONVERT_CONTRACT.md).

## 12. Imbalance

QF-028 Queue Imbalance is the canonical BBO quantity imbalance; QF-029 extends measurement over multiple levels/weights. The Feature Engine owns measurement. Levels/weights are calibrated and versioned. Predictive meaning, horizon, signs of pressure and confidence belong to PASS02 Participants and may not be inferred as certainty.

## 13. OFI / MLOFI

QF-030 and QF-031 define event-level bid/ask contributions; QF-032 aggregates OFI; QF-033 extends it across levels. True OFI requires ordered event/change evidence. A calculation from two snapshots is labelled `Snapshot OFI proxy`, carries reduced fidelity and is never presented as true event-level OFI. Feed fidelity and gaps determine validity.

## 14. Microprice

QF-034 Microprice combines BBO prices/sizes according to the locked Formula Book definition; QF-035 measures dislocation from its specified reference. Microprice is a feature, not guaranteed future fair value, an executable quote or automatic direction. PASS02 owns any learned predictive use.

## 15. Returns / volatility

QF-036 Log Return requires an explicit price series and time ordering. QF-037 Realized Variance and QF-038 Realized Volatility require an identified sampling/window convention. Values from different horizons/scaling are not interchangeable. Incremental rolling state must reproduce offline reference results.

## 16. Jump score

QF-039 Robust Jump Score compares a return/shock with its robust scale under the authoritative definition. Threshold and response policy are calibrated, not invented here. Jump evidence feeds Atlas/HWC/Risk but does not itself authorize execution.

## 17. Depth participation

QF-040 measures proposed/actual order quantity against explicitly defined available depth. The denominator, side, band, quantity and BookVersion are mandatory. It is size-specific and supports route/Risk/Sizing; it cannot enlarge available capacity.

## 18. Volume participation

QF-041 measures order quantity/value relative to market volume over a declared window. Historical volume is not current L2 capacity. Window, aggregation and source quality are calibrated/provenanced, and Execution owns order slicing behavior.

## 19. Mechanical impact

QF-042 measures immediate impact caused mechanically by walking a selected book. It is deterministic for the chosen immutable arrival state/order assumptions. It is not a forecast of replenishment, other traders or future cross-market response.

## 20. Liquidity resilience interface

QF-043 measures recovery of liquidity/depth after shock under its locked definition. The canonical measurement belongs here; learned horizon, replenishment distribution and predictive confidence belong to Participants. Simulator consumes those predictions for counterfactual branches. Mechanical Impact and Liquidity Resilience remain separate to prevent double-counting.

## 21. Incremental computation

Production Rust maintains bounded current/rolling features incrementally where appropriate: BBO/spread/depth, imbalance, OFI, returns/variance/volatility and window aggregates. It does not rescan full history for each opportunity. Static/semi-static metadata transforms are precomputed. Heavy calibration, causal analysis and large simulation remain off the hot path.

No blocking network/storage/service call, unbounded allocation or global route search is permitted during opportunity evaluation. Python is the research/reference/parity environment; it is not a second live semantic truth. C++ is not introduced absent profiling evidence and a governed decision.

## 22. State/version provenance

Every feature snapshot identifies MarketId, side where relevant, exchange/receive times, BookVersion, MetadataVersion, FormulaVersion, window/config version, source quality and valid/unknown status. Route calculations record every leg's versions under an explicit coherent snapshot/skew policy. Stale worker output is discarded or revalidated under Data Contracts.

## 23. Participants interface

Participants consumes QF-028–043 plus event/market context to estimate edge survival, replenishment, maker fill/adverse selection, cross-market response and competition. It owns prediction, uncertainty, support/OOD and QF-081/QF-083 models. Quant owns reproducible feature measurement, not participant intent or causal certainty.

## 24. Simulator interface

Simulator consumes exact arrival books, QF-009–016 and QF-042 for deterministic mechanical conversion/impact, then Participant distributions for future response and recovery scenarios. It cannot relabel exogenous Replay as counterfactual truth. Predicted and actual outputs remain distinct and versioned.

## 25. Atlas interface

Atlas receives versioned aggregates for spread, depth, liquidity, volatility, jumps, impact and resilience across governed horizons. It records support/confidence and distinguishes current state from historical/learned aggregate. Current BookState—not Atlas—is execution truth. Atlas scores guide activation/research but never override exact `NetConvert`, Risk or structural validity.

## 26. Validation / parity

Each QF family needs Formula Book golden tests, unit/sign/direction examples, boundary/invalid input tests and Rust/Python parity. Incremental state is compared to offline batch reference. Replay verifies deterministic versions and no lookahead; Shadow/Micro-live compare predictions and mechanics with actual exchange evidence where needed. Failures include wrong book side, unavailable-depth use, fee double-counting, silent precision loss, proxy OFI mislabeled true, state/version mismatch and linear-size assumptions.

## 27. Deep-spec links

- [Microstructure deep specs](./deep-specs/market-microstructure/README.md)
- [Quant Feature Catalog](./_analysis/pass08_graph_routes_quant/QUANT_FEATURE_CATALOG.md)
- [Formula Crosscheck](./_analysis/pass08_graph_routes_quant/FORMULA_CROSSCHECK.md)
- [Market Graph and Routes](./03_MARKET_GRAPH_AND_ROUTES.md)
- [Market Participants](./06_MARKET_PARTICIPANTS.md)
- [Counterfactual Simulator](./07_COUNTERFACTUAL_SIMULATOR.md)
- [Data Contracts](./11_DATA_CONTRACTS.md)

## Sources

Original sources SRC-001–SRC-008 as inventoried in [`_analysis/SOURCE_INVENTORY.md`](./_analysis/SOURCE_INVENTORY.md). No external web research was performed in PASS08.
