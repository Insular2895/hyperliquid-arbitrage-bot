# InventoryEngine

## Purpose

Maintenir balances localisées, reservations, bands, flows and post-trade state.
## Responsibilities

Actual/available/reserved/pending, CORE/TRANSIT/EXCLUDED, MTM and simulations.
## Non-responsibilities

Ne décide pas seul relocation ou recovery.
## Inputs

Account/fill/reservation/external-flow events, prices/atlas/config.
## Outputs

Immutable InventorySnapshot, violations and PortfolioAfter.
## Dependencies

AccountingEngine, ReservationEngine, MarketAtlas, ClockAndRng.
## State

Single-writer ledger by AssetLocation.
## Algorithms / formulas

QF-064..067/073/105..108.
## Invariants

Available≥0; pending unknown unavailable; external flows not PnL.
## Failure modes

Missed/duplicate fill, stale account, price unavailable, band drift.
## Risk interactions

Hard bands gate; soft/flow penalties; unreconciled blocks new risk.
## Performance requirements

Snapshot/read bounded; event apply idempotent.
## Metrics

Balances/bands/flows/reserved/pending/MTM and discrepancies.
## Persistence

Events/checkpoints and classification/config versions.
## Configuration

Targets/bands/classes/numeraire calibrated and approved.
## Tests

Ledger property, duplicate fills, external flows, restart/reconcile.
## Maturity requirement

M2; M3 account shadow; M4 real reconciliation.
## Open calibrated parameters

Classes, targets/bands, flow horizons and penalties.
