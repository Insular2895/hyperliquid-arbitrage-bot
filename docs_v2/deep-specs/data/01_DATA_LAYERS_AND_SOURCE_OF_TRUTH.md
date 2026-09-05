# Data Layers and Source of Truth

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Contract

The five-layer boundary is strict:

| Layer | Contains | Must not become |
|---|---|---|
| L0 RAW | Original source bytes and capture envelope | Parsed or corrected history |
| L1 NORMALIZED | Versioned typed interpretation | Mutable state |
| L2 STATE | Ordered reducer result | A second unowned truth |
| L3 DERIVED | Recomputable features/forecasts | Sole historical evidence |
| L4 DECISIONS/RESULTS | Authorization, intent and actual result chain | A substitute for source/account evidence |

L0 is immutable evidence of receipt. It does not assert that an exchange message was timely, valid or true. L1 attaches interpretation and source linkage. L2 is canonical only for a specific run, ordered stream and reconciliation context. L3 is always reproducible from declared inputs/versions. L4 separates opportunity, permission, intention, effect and outcome.

## Prohibitions

- Do not reconstruct a book from an edge/opportunity table when L0/L1 exists.
- Do not overwrite RAW after a parser fix; produce a new normalization version.
- Do not let logs, metrics or a checkpoint replace the event/journal truth.
- Do not merge ActualAccountState and ShadowCounterfactualState.
- Do not duplicate Live, Replay and Paper business engines.

## Acceptance

A lineage query must walk from any DecisionTrace item to RAW source IDs and from any real Fill to intent, risk decision, state versions, formulas/models/config and final PnL. Unknown links fail validation; they are not inferred heuristically.
