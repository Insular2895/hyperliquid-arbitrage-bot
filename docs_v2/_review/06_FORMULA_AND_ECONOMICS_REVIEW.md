# Formula and Economics Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

The [Formula Book](../04_FORMULA_BOOK.md) owns 110/110 uniquely identified contracts. Each contract binds notation, units, signs, failure behavior, consumers, provenance and golden/parity expectations. This review highlights decision-sensitive blocks; it is not a second equation authority.

| Formula block | Core question | Required unit/sign discipline | Main consumers | Review hot spots |
|---|---|---|---|---|
| QF-001–013 | price, quantity, rounding, L2 walks | explicit base/quote units; no extrapolation | Book, Precision, Formula | current precision rules; partial walk vs full-route acceptance |
| QF-014–027 | fees, `NetConvert`, edge, capacity | economic value distinct from debit asset; costs once | Opportunity, Risk, Accounting | `EXT-003/004`; cost attribution; `QF-027` capacity |
| QF-028–043 | microstructure features | explicit reference/window/epsilon | Features, Participants, Risk | QF-041 zero volume; QF-043 zero resilience denominator |
| QF-044–055 | survival, response, maker timing | probability/support/horizon and censor labels | Participants, Simulator, Execution | QF-047/053 time grid, censor/tail convention |
| QF-056–063 | scenarios and tail Risk | exhaustive probability mass; loss-positive convention | Simulator, Risk | empirical QF-061/062 quantile/ES convention |
| QF-064–080 | inventory, Sizing, Portfolio, Recovery | asset/location units; deterministic ties | Capital, Risk, Execution | zero band; QF-077 search; QF-078 solver; Recovery objective |
| QF-081–104 | model quality, OOD, infra economics | prediction vs actual separation; invalid denominator typed | Validation, Participants, Infra | QF-091 LCB; QF-092/093 diagnostics; QF-094/096 |
| QF-105–110 | PnL, capital efficiency, drawdown | disjoint attribution; valuation/version explicit | Accounting, Ops, Validation | zero peak and empty interval |

## Canonical economic chain

`NetConvert(route, q, point-in-time books/rules)` walks exact L2, applies precision/minimum/fee rules in canonical order and returns typed output, residuals, costs and validity. `Edge(q)` compares like-for-like terminal economic value. `QF-027` finds profitable capacity from economics; `QF-076` (within the Sizing block) limits permitted exposure after all constraints and evidence. Profitable capacity is therefore not permission and not `Q_validated`.

Risk-adjusted expected value combines explicit scenario outcomes and costs; it does not conceal a magic score. Bridge compares `STAY` with permitted destination/exit/relocation paths after all costs, Risk and terminal constraints. Recovery may deliberately accept negative immediate economic value to reduce current exposure safely.

## Double-counting controls

- Fee economic value and actual debit-asset delta are recorded separately but charged once.
- Forecast slippage/adverse penalties are decision inputs, not realized PnL.
- Strategy, Execution cost, Recovery, Inventory MTM, Rebalance, Bridge/Relocation, Infrastructure and idle-capital attribution remain disjoint.
- Actual PnL consumes unique fills, actual fees and explicit valuations; predicted and actual ledgers reconcile but never merge silently.

## Human-gated conventions

`OPEN-017..028` preserve source-omitted invalid-denominator, finite-sample, censoring, deterministic search/solver, clipping and drawdown conventions. The affected formula must fail closed until its versioned convention and golden vectors are approved. These do not block Phase 1; they block the consuming formula/capability phase.
