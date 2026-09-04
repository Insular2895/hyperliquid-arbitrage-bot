# PASS 04 — Execution Strategy Mode Matrix

`DOCUMENTATION STATUS: REBUILD IN PROGRESS — PASS 04 REVIEW COMPLETE`

“Supported,” “initially enabled,” and “capital validated” are independent. This documentation pass validates no capital.

| Mode | Type supported? | Enabled initially? | Capital validated? | Maker legs | Taker legs | Queue dependency | Participant dependency | Recovery branch | Main failure modes | Source authority |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|
| `TT` | yes | target baseline after gates | no | 0 | 2 | no | survival/liquidity/cross-market for continuation | after Leg 1 exposure or Leg 2 partial/failure | zero/partial/unknown, price protection, Leg 2 edge death | SRC-004 §§41–53; QF-057 |
| `MT` | yes | no pending maker activation evidence | no | 1 | 1 | yes | maker fill/adverse selection + survival/liquidity | every invalid/below-minimum partial or taker failure | stale/partial/cancel race, small fill, taker failure | SRC-004 §§54–61; QF-051–058; OPEN-012 |
| `TTT` | yes | target baseline after gates | no | 0 | 3 | no | survival/liquidity/cross-market after each leg | after any prior exposure and invalid later leg | non-atomic independent zero/partial/reject/unknown | SRC-004 §§62–64; QF-057 |
| `MTT` | yes | no pending maker activation evidence | no | 1 | 2 | yes | maker/adverse + survival/cross-market | maker partial and either taker continuation branch | maker cancel race plus two non-atomic taker legs | SRC-004 §65; MT + TT rules; OPEN-012 |
| `TM` | yes, representable | **no** | **no** | 1 | 1 | yes | strong fill/adverse/survival evidence required | mandatory for exposed wait/failure | second-leg maker strands intermediate inventory | SRC-004 §66; SRC-005 `ExecutionMode`; OPEN-012 |
| `MM` | yes, representable | **no** | **no** | 2 | 0 | yes | multiple maker/queue/adverse dependencies | mandatory, potentially multi-residual | compounded resting, partial, cancel, queue uncertainty | SRC-004 §66; SRC-005 `ExecutionMode`; OPEN-012 |

TT/TTT “target baseline” means their mechanics belong in the initial production architecture; it is not authority to enable Live or allocate capital. MT/MTT need explicit maker validation/activation. TM/MM remain supported-disabled and cannot be promoted by this pass.
