# Retention and Storage Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Evidence | Default semantic class | Local role | Archive role | Exact duration/status |
|---|---|---|---|---|
| Orders, fills, fees, executions | `PERMANENT` | Recent journal/access | Durable evidence | Permanent class locked |
| Risk decisions/config/model/formula versions | `PERMANENT` | Active run/audit | Durable reproducibility | Permanent class locked |
| Incidents/GoldenDatasets/validation evidence | `PERMANENT` | Active investigation | Durable archive | Permanent class locked |
| Pinned trade/incident RAW windows | `LONG` or `PERMANENT` by hold | Fast reconstruction | Durable selected RAW | Window/duration calibrated |
| Normalized datasets | `LONG`/`MEDIUM` | Active analytics | Reproducible research | Exact months calibrated |
| Derived/opportunities/latency | `LONG`/`PERMANENT` by evidence value | Active calibration | Compact historical evidence | Exact duration calibrated |
| General RAW market | `SHORT` | Recent replay buffer | Selected/temporary archive | Exact days calibrated |
| Rebuildable caches | Ephemeral | Local only | None | Reconstructible |

`PERMANENT`, `LONG`, `MEDIUM`, `SHORT` are locked class names. Source examples of 2–7/3–7/14–60/30–90 days, 5–15-minute chunks, 5s-before/10s-after windows and disk percentages are calibration candidates, not invariants.

Local NVMe is the working buffer. Object storage is vendor-neutral durable archive. Never capture directly to iCloud/cloud synchronization. Cleanup requires closed chunk, verified local checksum, completed upload, verified remote checksum, retention evaluation and no execution/incident/golden hold.

## Environment-specific lifecycle

| Family | R&D collection | Internal production | Client production | Incident retention |
|---|---|---|---|---|
| General market RAW | Broad relevant spot universe; SHORT/MEDIUM working history | SHORT local, selected archive | SHORT bounded local; privacy/local policy | Pin relevant window LONG/PERMANENT |
| Normalized market/account | LONG active research | MEDIUM/LONG for calibration | MEDIUM as support/replay requires | Preserve referenced partitions |
| Derived/features/opportunities | LONG/PERMANENT when experiment-bearing | LONG/PERMANENT compact feedback | Local LONG subject policy | Preserve inputs/outputs used |
| Orders/fills/fees/executions | PERMANENT | PERMANENT | PERMANENT per policy/legal constraints | PERMANENT |
| Risk/decision/config/model/formula evidence | PERMANENT | PERMANENT | PERMANENT | PERMANENT |
| Latency/infra/clock quality | LONG/PERMANENT when decision-bearing | LONG/PERMANENT compact | LONG for diagnosis | Preserve full affected window |
| Checkpoints | Rotating MEDIUM; journal remains | Rotating MEDIUM | Rotating MEDIUM | Preserve relevant checkpoint plus journal |
| GoldenDatasets/validation/negative results | PERMANENT | PERMANENT | Selected validated/support corpus | Promote incident dataset to Golden when useful |
| Logs | SHORT/MEDIUM supplemental | SHORT/MEDIUM | Redacted bounded policy | Preserve redacted relevant logs |

“Client production” remains local-only by default unless the deployment/telemetry pass explicitly authorizes export. Exact duration, capacity and legal/privacy policy require validation; no source example becomes a fixed rule.
