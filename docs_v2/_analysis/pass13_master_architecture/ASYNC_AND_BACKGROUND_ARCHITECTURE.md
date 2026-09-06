# Async and Background Architecture

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Responsibility | Class | Input/output | Failure isolation | Re-entry to production |
|---|---|---|---|---|
| Recorder write/rotation | near-line/background | ordered queue → chunks/quality | backlog/loss visible; P0 protected; may degrade scope | recorded facts only; no decision mutation |
| Compression/archive | background | closed chunks → archive | pause/retry within storage policy; preserve manifest | dataset availability record |
| Replay jobs | background/offline | immutable dataset/manifest → report/trace | isolated from Live state | `EvidenceId`, never direct mutation |
| Atlas slow aggregates | near-line/background | point-in-time evidence → Atlas candidate | last valid version retained or UNKNOWN | atomic validated AtlasVersion |
| Research export | background | client-selected/redacted evidence → dataset | explicit consent; no secret/raw leakage by default | offline only |
| Python training/calibration | offline | dataset → candidate artifact/report | no signer or Live memory | Validation/promotion pipeline |
| Challenger evaluation | offline/shadow | predictions/actuals → comparison | Champion remains/fallback | promoted immutable model only |
| Infrastructure analytics | background | timing/health/economics → benchmark | invalid clock/run excludes evidence | validated InfraProfile/capability |
| Diagnostics/support bundle | control/background | local evidence → redacted bundle | remains local until export | operator action only |
| Licensing refresh | control/background | cached entitlement ↔ service | outage blocks new commercial risk, not safety | signed license-state event |
| Release/update checks | control/background | registry metadata → verified candidate | current digest retained on failure | transactional update workflow |
| Telemetry | background opt-in | bounded/redacted metrics → backend | never mandatory for safety/hot path | operations evidence only |

Queues are bounded and expose backlog/quality. No background worker commits mutable decision state directly: outputs carry input versions and enter through a state-owner command/event or explicit Model/Config/Capability promotion. Async ordering never determines canonical Core ordering.
