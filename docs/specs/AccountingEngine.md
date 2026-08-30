# AccountingEngine

## Purpose

Produire des ledgers et PnL auditables sans mélanger sources de valeur.
## Responsibilities

Double-entry-like deltas, fees, route/recovery/rebalance, MTM/external flows, drawdown.
## Non-responsibilities

Ne marque pas un output théorique comme réalisé.
## Inputs

Deduped fills/account events, inventory prices, infra costs.
## Outputs

Accounting entries and PnL views.
## Dependencies

OrderStateMachine, InventoryEngine, FeeEngine, ClockAndRng.
## State

Append-only ledger and derived balances/equity.
## Algorithms / formulas

QF-015, 080, 093, 097/098, 106..110.
## Invariants

Fill once; external flows excluded; components separate; no double fees.
## Failure modes

Duplicate/missing fill, wrong numeraire, stale MTM, unbalanced entries.
## Risk interactions

Provides losses/drawdown; discrepancy triggers reconciliation.
## Performance requirements

Event apply bounded; reports async.
## Metrics

PnL components, reconciliation diff, fee/slippage bias, drawdown.
## Persistence

Immutable ledger/checkpoints/manifests.
## Configuration

Numeraire/valuation sources/cadence versioned.
## Tests

Ledger balance, duplicates, external flows, recovery and restart.
## Maturity requirement

M2; M3 shadow account; M4 real audit.
## Open calibrated parameters

Valuation fallback/cadence and accounting policy review.
