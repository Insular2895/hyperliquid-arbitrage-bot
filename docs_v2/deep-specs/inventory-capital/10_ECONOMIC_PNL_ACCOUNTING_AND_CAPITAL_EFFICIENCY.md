# 10 — Economic PnL, Accounting and Capital Efficiency

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Attribution buckets

| Bucket | Expected/realized | Primary evidence | Must not be hidden inside |
|---|---|---|---|
| Route / Strategy PnL | Both | executable forecast; FillLedger | global aggregate only |
| Execution costs | Predicted then actual | NetConvert/fees; fills | a second cost deduction |
| Recovery PnL/Loss | Both | Recovery trace/fills, QF-079/080 | route alpha |
| Inventory MTM | Realized valuation change | inventory + point-in-time marks, QF-107 | route PnL |
| Rebalance PnL | Both | action/fills | OWA/Bridge |
| Bridge / Relocation PnL | Both | move decision/fills/exit | route or Rebalance |
| Infrastructure Cost | Realized/allocated policy | infrastructure accounting | Strategy PnL |
| Idle Capital Cost | Expected/calibrated economic cost | reservation/capital availability, QF-105 | realized cash without policy |
| Global Economic PnL | Aggregate | QF-106/QF-108 reconciliation | component detail |

QF-106 Global Economic PnL includes execution, inventory MTM, Rebalance, Bridge and infrastructure components according to the Formula Book. QF-108 separately defines Total Strategy PnL and its relationship to global economics. The Formula Index's compact QF-108 locator is incomplete; SRC-004 §113 is the authority and PASS11 must preserve both source equalities.

## Accounting convention

Actual RoutePnL is after exchange fees/execution costs under SRC-005's recommended convention, while fee breakdown remains analytical. Therefore fees are not subtracted again from Economic PnL. External deposits/withdrawals are `ExternalFlow`, not profit, and QF-107 excludes them from MTM change.

Expected InventoryPenalty, StrandedPenalty, RebalanceValue and relocation value support decisions. They become realized accounting only through actual fills, holding/mark changes, exits or an explicitly defined economic-cost policy. Predicted values are never substituted for actual values after execution.

## Lineage and reconciliation

Every component links to run/config/formula/model versions, action/route/execution IDs, fill ledger, inventory/account version, valuation timestamp and numeraire. Portfolio equity is reconstructed from balances, marks and external flows and reconciled with exchange-equivalent evidence where available.

## Capital efficiency

Capital efficiency is assessed with attributable capture, validated utilization, missed opportunity and idle cost—not forced 100% deployment. Surplus capital may remain idle when no valid capacity exists. A route can profit while portfolio economics worsen; a relocation can lose immediately while improving future utility. Both facts remain visible.

Sources: SRC-001/002 hierarchical PnL reasoning; SRC-003 §§56–63; SRC-004 QF-105–108; SRC-005 §§167–168/Data §§148–155; SRC-006 §§165–169; SRC-007 §§91–93.
