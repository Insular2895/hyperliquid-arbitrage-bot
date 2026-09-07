# Capital, Bridge and Sizing Review

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

## State and classifications

Inventory is updated only by unique actual fills and reconciled balance facts. `CORE_INVENTORY`, `TRANSIT` and `EXCLUDED` classify economic purpose; venue/location is separate. Available balance subtracts open reservations and other unavailable claims. Pending intermediate exposure remains explicit.

Capital Reachability projects what capital can be used after balances, locations, reservations and path costs. Terminal Viability tests whether the resulting inventory has permitted holdings, exits, stranded/dust and hard-band behavior. The structural Graph does not answer either question, and Atlas support does not create capital.

## Position Sizing versus Slicing

Position Sizing chooses total exposure `q` from a nonlinear risk-adjusted expected-value curve inside every book, balance, inventory, Risk, capability and evidence constraint. `Q_validated` caps only the exact supported market/route/mode/version band. More balance cannot increase it automatically.

Order Slicing decomposes an already validated `q`; it may not enlarge it or bypass reservation/Risk. Candidate-grid/refinement and ties must be deterministic and versioned (`OPEN-022`).

## Portfolio and Bridge

The Portfolio Allocator selects among already eligible opportunities under shared constraints. It cannot double-reserve, own Risk or promote a candidate. Complexity must beat a simple baseline.

Bridge/Capital Relocation compares `STAY` with all permitted destination, exit and relocation paths, including fees, impact, latency, future opportunity value, stranded risk and hysteresis. It is distinct from OWA and requires its own evidence and capital authorization.

## Action taxonomy and accounting

`Strategy`, `Bridge/Relocation`, `Rebalance`, `Recovery`, Inventory MTM and infrastructure/idle-capital effects remain separately classified and reconciled. A transient route edge cannot be counted simultaneously as strategy alpha and relocation value. Exact risk thresholds, inventory bands/penalties and support sizes remain evidence-calibrated before the affected Micro-live/Live scope.
