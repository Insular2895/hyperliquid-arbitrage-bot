# Recorder Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This is the Recorder-focused obligation view. Row-level disposition for all 661 PASS 00 entries remains in `DATA_REQUIREMENT_LEDGER.md`.

| Requirement/evidence | Source | Canonical resolution | Destination |
|---|---|---|---|
| `REQ-REC-0001` RAW test contract | SRC-003:219–245 | Preserve original payload and capture timestamps/source | Master §4–5; deep 02 |
| `REQ-REC-0002` chunking | SRC-003:246–287 | Small independent ZSTD chunks; 5–15 min calibrated | Recorder Master §5 |
| `REQ-REC-0003` iCloud archive | SRC-003:427–450 | Archive only after local close/checksum; direct capture forbidden | Deep 04 |
| `REQ-REC-0004` archive handoff | SRC-003:811–827 | Closed verified chunk → provider-neutral object storage | Deep 04 |
| `REQ-REC-0005` retention automation | SRC-003:868–900 | Metadata/holds/checksum govern auditable cleanup | Retention matrix |
| `REQ-REC-0006` research topology | SRC-003:1126–1147 | Local active data and Replay cache; archive separate | Deep 04 |
| `REQ-REC-0007` example retention | SRC-003:1177–1194 | Durations are calibrated examples | Retention matrix |
| `REQ-REC-0008` recorder sequence | SRC-005:5549–5565 | Strictly increasing per Recorder; definitive local observation order | Data Master §5/18 |
| `REQ-REC-0009` Recorder thread | SRC-005:7405–7419 | Non-blocking channel; no disk/compress in Core | Recorder Master §2–3 |
| `REQ-REC-0010` priority | SRC-005:7420–7436 | P0 execution/account; P1 windows; P2 general market; P3 derived | Priority matrix |
| `REQ-REC-0011` retention classes | SRC-005:8726–8734 | PERMANENT/LONG/MEDIUM/SHORT | Retention matrix |
| RAW append-only/immutable/versioned | SRC-005:5493–5530 | Never rewrite source history | Data Master §4–5 |
| Original payload retained | SRC-003:219–245; SRC-005:5504–5530 | Enables corrected re-normalization | Deep data 02 |
| RawChunkManifest/checksum | SRC-005:7354–7380 | Verify every closed chunk | Recorder Master §5 |
| Normalization separation | SRC-005:7381–7404 | New normalized dataset version, same RAW | Recorder Master §6 |
| Explicit saturation policy | SRC-005:7437–7460 | Bounded, visible lower-priority degradation | Recorder Master §8 |
| Completeness metrics | SRC-005:7449–7460 | received/written/dropped/gaps | Priority matrix |
| Dataset quality regions | SRC-005:7461–7490 | Coverage/clock/markets; INVALID/LOW_FIDELITY | Recorder Master §9–10 |
| Account evidence protected | SRC-005:7491–7500 | P0 first | Priority matrix |
| ExecutionJournal | SRC-005:7501–7537 | Separate append-only critical evidence/rebuild | Recorder Master §14 |
| Local storage separation | SRC-005:8658–8681 | Persistent evidence separate from ephemeral caches | Deep data 08 |
| Checkpoints not truth | SRC-005:8682–8725 | checkpoint + journal + exchange reconciliation | Recovery matrix |
| Trade/incident windows | SRC-005:8754–8776 | Longer retention, duration calibrated | Retention matrix |
| Unknown input type | SRC-005:8777–8802 | RAW + alert; no guessed normalization | Data Master §8 |
| Storage telemetry | SRC-003:1212–1245 | bytes/rates/compression/disk/backlog measured | Recorder Master §25 |
| Recorder DoD | SRC-006:4660–4688 | throughput/compression/drop/backlog/disk/nonblocking/priority/checksum/roundtrip | Validation map |

Recorder-owned PASS 00 IDs: **11/11 covered**. Closure/supporting Recorder obligations above: **26/26 destinationed**. Destinationless: **0**.
