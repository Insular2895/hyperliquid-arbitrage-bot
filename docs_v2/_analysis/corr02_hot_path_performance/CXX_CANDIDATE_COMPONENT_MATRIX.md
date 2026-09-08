# C++ Candidate Component Matrix

DOCUMENTATION STATUS: FUTURE CANDIDATES — NONE APPROVED

| Component | Initial color | Why | Earliest possible status |
|---|---|---|---|
| bounded parser/decoder | amber | pure byte input may expose a measured kernel | only after Rust/parser profiling and safety gate |
| compression/decompression | amber | bounded off-core/Recorder work, mature foreign libraries possible | only if it affects required critical evidence without hot-path harm |
| checksum/serialization kernel | amber | deterministic pure transform possible | after end-to-end materiality and ABI cost |
| isolated numeric kernel | amber | may be vectorizable if exact numeric contract permits | after Rust/PGO/SIMD evidence |
| BBO conservative rejector | red | false negative silently destroys opportunity population | not a first candidate |
| NetConvert | red | fee/precision/minimum/depth economic authority | not a first candidate |
| Risk | red | safety permission owner | excluded |
| Inventory/capital/reservations | red | shared economic truth | excluded |
| Execution/order/fill state | red | exchange effects and ambiguity | excluded |
| Recovery/reconciliation | red | restores economic truth | excluded |
| Accounting | red | canonical PnL/economic label | excluded |
| signer/nonce/capability | red | authority/security boundary | excluded |

“Amber” means eligible only for future investigation, not recommended or planned. No first C++ component is selected by CORR-02.
