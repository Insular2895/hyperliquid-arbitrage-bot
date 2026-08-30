# BridgeEngine

## Purpose

Évaluer/planifier une relocation interne de capital économiquement justifiée.
## Responsibilities

Compare stay/destinations/paths, terminal/exit/idle/risk and hysteresis.
## Non-responsibilities

Ne confond pas bridge avec OWA; cross-venue transfers disabled.
## Inputs

Reachability, Atlas, inventory, opportunity forecasts and risk.
## Outputs

RelocationProposal or RejectReason with decomposition.
## Dependencies

CapitalReachabilityEngine, InventoryEngine, QuantEngine, RiskEngine.
## State

Cooldown/hysteresis and pending relocation state.
## Algorithms / formulas

QF-068..072/105.
## Invariants

Bridge costs not double counted; negative cycle expectation gives infinite BE.
## Failure modes

Flip-flop, stranded destination, optimistic future EV, hidden exit.
## Risk interactions

Hard terminal/inventory/risk gates; relocation separate accounting.
## Performance requirements

Candidates precomputed; bounded evaluation.
## Metrics

Proposals/executions, cost, break-even, idle/stranded, realized value.
## Persistence

Decision decomposition, paths and outcomes.
## Configuration

Threshold/hysteresis/cooldown and destinations approved.
## Tests

Alternative bridges, no viable exit, flip-flop, replay policies.
## Maturity requirement

M2 replay; M4 internal relocation only after validation.
## Open calibrated parameters

Forecast horizon, threshold/hysteresis and risk/idle costs.
