# P0 Durability and Backpressure Audit

| Condition | P0 | P1 | P2 | P3 | Risk response | Core block? |
|---|---|---|---|---|---|---:|
| healthy | preserve | preserve | preserve | preserve | normal gates | no |
| elevated | preserve | preserve | preserve/degrade visibly | suppress optional | narrow only | no |
| optional saturation | preserve | preserve | degrade visibly | drop/sample visibly | no widening | no |
| P0 threatened | apply received truth; integrity alert | best effort/pin | degrade | stop | no new risk; safety remains | no |

Exact lane/buffer design is an implementation choice; detection and fail-safe behavior are locked.
