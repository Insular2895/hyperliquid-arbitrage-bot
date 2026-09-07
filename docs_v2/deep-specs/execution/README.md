# Execution deep specifications

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW — PASS 04 REVIEW COMPLETE`

These specifications expand [10 — Execution State Machine](../../10_EXECUTION_STATE_MACHINE.md). SRC-004 Dossier 1 is the execution-closure authority; SRC-005 controls Risk/Data contracts. They specify documentation, not implementation approval.

| File | Closure question |
|---|---|
| [01](01_ARCHITECTURE_OWNERSHIP_AND_FIVE_STATE_MACHINES.md) | Who owns effects and how do five machines coordinate? |
| [02](02_ENGINE_AND_ROUTE_EXECUTION_STATE_MACHINES.md) | What are all Engine/Route states and transitions? |
| [03](03_ORDER_INTENT_CLOID_NONCE_AND_ORDER_LIFECYCLE.md) | How do intent, CLOID, nonce, signing, and OrderState work? |
| [04](04_RESERVATIONS_BALANCES_AND_EXECUTION_PLAN.md) | When are capacities reserved, converted, or released? |
| [05](05_TAKER_EXECUTION_TT_AND_TTT.md) | How do protected taker TT/TTT branches execute? |
| [06](06_MAKER_EXECUTION_MT_MTT_AND_DISABLED_MODES.md) | How do maker MT/MTT and disabled TM/MM behave? |
| [07](07_PARTIAL_FILLS_DUST_AND_INTERMEDIATE_BUFFERS.md) | How is every partial/dust/buffer branch handled? |
| [08](08_CANCEL_RACES_TIMERS_AND_ORDER_UNCERTAINTY.md) | How do cancel races, timers, and ambiguity resolve? |
| [09](09_RECOVERY_STATE_MACHINE_AND_EXIT_SELECTION.md) | How is the best current recovery exit selected? |
| [10](10_RECONCILIATION_RESTART_AND_CRASH_CONSISTENCY.md) | How does exchange truth rebuild state after failure? |
| [11](11_EXECUTION_TRANSPORT_REPLAY_SHADOW_AND_LIVE.md) | How do transports preserve Replay/Shadow/Live parity? |
| [12](12_FAILURE_MODES_REASON_CODES_AND_VALIDATION.md) | How are failures, reason codes, and evidence validated? |

The authoritative cross-document tables are in `_analysis/pass04_execution/`. No deep spec may invent exchange-current facts or numeric thresholds.
