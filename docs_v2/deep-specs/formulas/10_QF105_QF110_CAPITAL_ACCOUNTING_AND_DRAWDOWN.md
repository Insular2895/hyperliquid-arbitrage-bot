# QF-105–QF-110 — Capital, Accounting and Drawdown

DOCUMENTATION STATUS:
AWAITING HUMAN REVIEW

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-105 | `IdleCost=C×OpportunityRate×T` | numeraire | C,T≥0; empirical rate in value/(capital·time), aligned horizon | negative/missing/unvalidated rate invalid | zero factor cases and known product |
| QF-106 | `ExecutionPnL+InventoryMTM+RebalancePnL+BridgePnL-InfrastructureCost` | numeraire | same period/numeraire; disjoint reconciled components | overlap, missing component policy or currency mismatch invalid | component isolation and accounting equality |
| QF-107 | `MTM_a=I_aP_a^numeraire`; `ΔMTM=MTM_t-MTM_{t-1}-ExternalFlow_a` | numeraire | point-in-time inventory/prices, valuation policy, external-flow conversion | stale/missing price or unidentified flow invalid | price/inventory change, deposit/withdrawal exclusion |
| QF-108 | `StrategyPnL=ΣRoutePnL+ΣRecoveryPnL+ΣRebalancePnL+InventoryPnL`; `EconomicPnL=StrategyPnL-InfraCost` | numeraire | disjoint strategy attribution, same period and reconciled global total | duplicate route/recovery/inventory attribution invalid | component isolation and QF-106 reconciliation |
| QF-109 | `Peak_t=max_{u≤t}E_u`; `DD_t=Peak_t-E_t`; `DD_rel=DD/Peak` | equity units / ratio | ordered nonempty equity series; Peak>0 for relative | empty/out-of-order invalid; Peak≤0 relative undefined/open | new peak 0 DD, decline, recovery, zero peak invalid |
| QF-110 | `MDD=max_tDD_t` | equity units | valid nonempty QF-109 series and interval | empty interval source-unspecified: invalid/open | monotone up 0, known trough, interval boundary |

SRC-004 supplies these fixed identities but contains no formal status line for QF-106–110; their audit label is `SOURCE_DERIVED_FROM_CONTEXT`. That label preserves source certainty accurately while retaining the equations. PnL components must be mutually reconcilable: QF-108 strategy attribution plus infrastructure cost must equal QF-106 global EconomicPnL under the same scope.

CORR-05 makes that compatibility explicit through disjoint Strategy, Recovery, Rebalance, Bridge/Relocation, InfraCost and InventoryMTM buckets. `StrategyPnL` may be a presentation aggregate, never an overlapping ledger. Each fill/cost is attributed once and infrastructure cost closes once. See [Accounting Reconciliation Map](../../_analysis/corr05_economic_integration/ACCOUNTING_RECONCILIATION_MAP.md).
