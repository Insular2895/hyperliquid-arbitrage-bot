# Execution deep specifications

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

These specifications expand [10 — Execution State Machine](../../10_EXECUTION_STATE_MACHINE.md). SRC-004 Dossier 1 is the execution-closure authority; SRC-005 controls Risk/Data contracts. They specify documentation, not implementation approval.

| File | Closure question |
|---|---|
| 01 | Who owns effects and how do five machines coordinate? |
| 02 | What are all Engine/Route states and transitions? |
| 03 | How do intent, CLOID, nonce, signing, and OrderState work? |
| 04 | When are capacities reserved, converted, or released? |
| 05 | How do protected taker TT/TTT branches execute? |
| 06 | How do maker MT/MTT and disabled TM/MM behave? |
| 07 | How is every partial/dust/buffer branch handled? |
| 08 | How do cancel races, timers, and ambiguity resolve? |
| 09 | How is the best current recovery exit selected? |
| 10 | How does exchange truth rebuild state after failure? |
| 11 | How do transports preserve Replay/Shadow/Live parity? |
| 12 | How are failures, reason codes, and evidence validated? |

The authoritative cross-document tables are in `_analysis/pass04_execution/`. No deep spec may invent exchange-current facts or numeric thresholds.
