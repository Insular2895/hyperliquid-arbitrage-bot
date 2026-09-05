# Incident Reconstruction and Research Feedback Loop

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

An `IncidentRecord` identifies severity, affected markets/executions, start/end, triggers, actions and resolution. It is a domain object, not merely an error log. Creating an incident pins relevant P0/P1 evidence and a calibrated market pre/post window.

A self-contained reconstruction resolves:

- RunManifest, build/image identity, ResolvedConfig and dependency locks;
- RAW chunk manifests/checksums, normalized schema and quality regions;
- ordered market/account/infra/timer/control events and state versions;
- FeatureSnapshots, model/simulator forecasts and formula inputs;
- Opportunity, Reject/RiskDecision, ExecutionPlan, intents and journal;
- exchange orders/fills/fees, inventory/account reconciliation and PnL;
- latency/clock quality, alerts and supplemental text logs.

Replay then compares the original trace with current/candidate configurations. Historical-truth reproduction uses original point-in-time artifacts; later-model experiments are labeled `COUNTERFACTUAL_MODEL`. Negative results and rejects are retained to avoid selection bias.

The feedback loop is `observe → record → replay → compare predicted/actual → calibrate in research → validate out-of-sample → Shadow → MicroLive → promote/demote`. No notebook-only conclusion or direct production self-learning changes a decision contract.

Acceptance starts from an incident or Fill ID and reconstructs every provenance edge to checksummed RAW, then reproduces the original decision and distinguishes any candidate counterfactual.
