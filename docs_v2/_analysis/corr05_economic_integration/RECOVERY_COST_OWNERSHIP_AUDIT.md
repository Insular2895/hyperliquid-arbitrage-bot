# Recovery Cost Ownership Audit

`p_recovery` owns probability of entering the R branch, not Recovery success or loss magnitude. The R scenario cashflow owns all path economics from the original strategy attempt through the terminal Recovery outcome once, including Recovery fees, executable slippage/book walk and QF-080 incremental Recovery loss.

QF-080 is a positive loss measured from immediately before Recovery to immediately after its resolved execution. It excludes losses already sunk before Recovery began. `RecoverySuccessRate = P(E6 | E5)` is operational evidence and never implies zero loss.

Forbidden: subtracting `ExpectedRecoveryLoss` after R-scenario PnL already includes it; treating `p_recovery` as failure probability; putting unresolved Recovery into X; or merging InventoryPenalty with realized Recovery loss.
