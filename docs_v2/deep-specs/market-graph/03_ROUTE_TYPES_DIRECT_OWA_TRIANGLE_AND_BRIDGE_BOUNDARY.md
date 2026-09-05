# Route Types: Direct, OWA, Triangle and Bridge Boundary

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Structural families

- `DirectRoute`: one ordered directed leg A→B.
- `Route2Leg`: A→X→B, structural only until classified.
- `Cycle3Leg`: A→X→B→A with exact closure.

Fixed types keep the hot path bounded and auditable. Execution modes TT/MT/TTT/MTT belong to Execution and do not change topology.

## OWA

OWA requires a valid DirectRoute A→B comparator. Direct and indirect start with the same A amount, terminate in B, and use coherent books, fees, precision and FormulaVersion. QF-017–020 produce direct output, indirect output, relative edge and absolute gain. Missing/disabled/invalid comparator rejects OWA; no synthetic comparator is invented.

## Triangle

Triangle requires `Cycle3Leg` closure into the exact starting asset. QF-021–023 express output, return and PnL in that start asset. Three legs without closure are an open path, not Triangle.

## Bridge and Recovery

Without the direct comparator, A→X→B may be submitted as a Bridge/Capital Relocation candidate. PASS07 then compares destination utility against STAY, exit cost, risk and terminal viability. Multi-leg does not imply OWA. Recovery handles existing unwanted exposure and can choose another/split exit under constitutional priority; it is not a retroactive Bridge or strategy gain.

## Accounting

Classification is carried explicitly. OWA/route conversion gain, Triangle PnL, Bridge/Relocation cost/value, Rebalance loss and Recovery loss remain separate. Accounting never guesses the class from the number of legs.

See [classification matrix](../../_analysis/pass08_graph_routes_quant/ROUTE_CLASSIFICATION_MATRIX.md).
