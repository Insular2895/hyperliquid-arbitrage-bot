# External Revalidation Checklist

`DOCUMENTATION STATUS: AWAITING HUMAN REVIEW`

Reconstruction/PASS16 performed no Internet check. CORR-04 created a dated snapshot and CORR-06 refreshed priority/sequencing/node/API facts on **2026-09-09**. A dated documentary refresh is not runtime conformance or activation evidence; each consumer still revalidates current official sources and observed fixtures. No EXT item blocks Phase 1 domain types/schemas.

| Check | ID | Fact family | Earliest technical phase | Coding / Replay / Shadow / Micro-live / Live effect | Required artifact and later official source |
|---:|---|---|---:|---|---|
| [ ] | EXT-001 | order types, matching, batching | 12 (exchange-bound details; emulator may need earlier) | affected transport/emulator / conditional / yes / yes / yes | dated official order-semantics capture + fixtures |
| [ ] | EXT-002 | API/WS endpoints, subscriptions, snapshots, reconnect | 2 | adapter yes / captured-schema only / yes / yes / yes | official API docs + payload/reconnect fixtures |
| [ ] | EXT-003 | fees, tiers, debit asset | 5 | exact economics yes / point-in-time snapshot / economic yes / yes / yes | official fee schedule/account evidence |
| [ ] | EXT-004 | metadata, precision, lot/tick/minimum | 5 | boundary coding yes / snapshot only / yes / yes / yes | official metadata/rule docs + golden fixtures |
| [ ] | EXT-005 | public feed cadence/fields/trade identity | 2 | adapter/data yes / captured-schema only / yes / yes / yes | official feed docs + observed capture |
| [ ] | EXT-006 | node requirements, flags, outputs, region | 26 for activation | public-feed path no / no / node scope / node scope / node scope | official node docs/release + benchmark |
| [ ] | EXT-007 | order_book_server L2/L4/spot support | 18/22/26 as consumed | baseline L2 no / fidelity claim / maker-node scope / same / same | official repository/release and conformance capture |
| [ ] | EXT-008 | rate limits, CLOID/nonce, `scheduleCancel` | 13 | transport yes / no / integration yes / yes / yes | official API docs + rate/idempotence fixtures |
| [ ] | EXT-009 | TradingFX plan/price/OS/network | 19/26 | no / no / host admission / affected profile / affected profile | dated vendor offer + controlled benchmark |
| [ ] | EXT-010 | Akamai/Linode G7 specs/price/region | 19/26 | no / no / host admission / affected profile / affected profile | dated vendor offer + controlled benchmark |
| [ ] | EXT-011 | Kamatera Type B specs/price/reservation | 19/26 | no / no / host admission / affected profile / affected profile | dated vendor offer + controlled benchmark |
| [ ] | EXT-012 | AWS Lightsail specs/price/AZ rationale | 19/26 | no / no / host admission / affected profile / affected profile | dated AWS documentation/pricing + benchmark |
| [ ] | EXT-013 | Sakura specs/price/trial | 19/26 | no / no / host admission / affected profile / affected profile | dated vendor offer + controlled benchmark |
| [ ] | EXT-014 | Cherry VDS specs/price/availability | 19/26 | no / no / host admission / affected profile / affected profile | dated vendor offer + controlled benchmark |
| [ ] | EXT-015 | SDK/library/runtime official support | 2 or chosen implementation phase | affected dependency yes / compatibility / host readiness / yes / yes | official release/support/security matrix |
| [ ] | EXT-016 | academic claims/dataset statistics | 21 when consumed | baseline no / research allowed / model-dependent only / same / same | primary paper provenance + local temporal OOS report |
| [ ] | EXT-017 | `split_client_blocks` uncommitted/no-response/all-peer-path/default-order semantics | 3/8/19/26 | no canonical mutation / speculative replay / node Shadow only / separately promoted source only / same | node commit + configuration/capture conformance |
| [ ] | EXT-018 | gossip/read auction and IOC/ALO write priority | 2/3/8/13/18/19/20 | schema/evidence only / counterfactual / policy Shadow / actual Micro-live separately authorized / promoted scope only | official priority page + matched HP fixtures + actual charge evidence |
| [ ] | EXT-019 | fast-cancel guidance versus endpoint current-effect statement | 13 | preserve verified field / no assumed advantage / observe / actual controlled evidence / revalidated promotion only | both official pages + dated conflict disposition |

An unverified fact blocks only its consumer. Public-feed TT is not blocked by an unselected node when current public-feed contracts are separately verified. Revalidation cannot itself promote a capability; it only removes a current-fact uncertainty.
