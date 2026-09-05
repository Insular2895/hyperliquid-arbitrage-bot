# Economic PnL Classification

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Component | Expected / realized | Formula/ref | Event source | Timing | Consumer | Must not be hidden inside |
|---|---|---|---|---|---|---|
| Strategy / Route PnL | both | QF-057/QF-108 | candidate + FillLedger | forecast then terminal fills | Strategy/accounting | Global-only scalar |
| Execution costs | both | QF-016/fees | quote then actual fills/fees | replace forecast after fill | Route/accounting | duplicate fee/slippage deduction |
| Recovery | both | QF-079/080 | Recovery trace/fills | Recovery boundary/terminal | Risk/accounting | Route alpha |
| Inventory MTM | realized valuation | QF-107 | inventory + marks + external flows | valuation cutoffs | accounting/Risk | Route execution PnL |
| Rebalance | both | action/fills | Rebalance action/fills | terminal/period | capital/accounting | OWA or Bridge |
| Bridge / Relocation | both | QF-070–072 | decision/reservation/fills/exit | decision and realized move | capital/accounting | Route/Rebalance |
| Infrastructure | realized/allocated | infra QFs | infra cost records | period | Global economics | Strategy PnL |
| Idle Capital Cost | expected/calibrated | QF-105 | availability/opportunity evidence | holding interval | allocation/research | cash PnL by default |
| Global Economic PnL | aggregate | QF-106/QF-108 | component ledger | period close | reporting/Risk | loss of component lineage |

Decision penalties are not realized PnL. ExternalFlow is never profit. Every component carries action/execution/inventory/config/formula/model versions, numeraire and valuation time.
