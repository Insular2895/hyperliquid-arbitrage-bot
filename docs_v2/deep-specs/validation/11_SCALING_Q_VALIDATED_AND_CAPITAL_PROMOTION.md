# 11 — Scaling, Q_validated and Capital Promotion

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

Let `S_validated` be the exact set of candidate quantities for which market data, route economics, model/simulator support, Risk, inventory/capital, execution/recovery, infrastructure and operations all pass at the same versioned state. `Q_validated = sup(S_validated)` when that set is non-empty, otherwise zero. The set may have holes: a failed quantity does not invalidate every larger quantity and a passing boundary does not certify every smaller quantity. Every selected q is therefore evaluated independently unless a separate, versioned monotonicity proof applies to the exact scope.

Vertical promotion advances by explicit q bands. Current-band actual observations plus next-band Simulator support, impact/tail/fill/Recovery/inventory calibration and stable operations precede the new manifest entry. Horizontal scale additionally proves shared balance/book/asset/Risk capacity, reservations and portfolio allocation without double counting.

Market expansion repeats metadata/fees/Graph/formulas, liquidity/support, Replay, Shadow and bounded Micro-live. Maker modes require queue/fill/adverse-selection and cancel/Recovery evidence. Bridge requires all permitted paths and STAY, terminal viability, relocation/exit economics and failure handling.

Q_validated may shrink on drift, OOD, regime/liquidity change, dependency demotion, incidents or rule/infrastructure change. More account capital, book depth, elapsed time or profitable aggregate PnL does not increase validated capacity.

An infrastructure/feed profile contributes evidence to `Q_validated` only after its exact N1–N9/P1–P9 scope is validated. Account balance cannot select a node or larger server. The CORR-05 closure below defines how completion/capture evidence is consumed without redefining actual truth or double counting QF-085, completion and infrastructure effects.

## CORR-05 closure

Completion/capture evidence is consumed through the one q/state-specific `Π_exec` distribution and its support domain. QF-085, actual completion and infrastructure attribution are not stacked. QF-027 remains profitable size; QF-076 remains the complete validated-capacity bound evaluated without a monotonicity assumption. Demotion, OOD or missing next-band evidence contracts capacity regardless of account balance.
