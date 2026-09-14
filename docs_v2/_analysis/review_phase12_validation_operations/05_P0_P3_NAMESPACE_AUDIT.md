# P0–P3 Namespace Audit

- `IncidentSeverity.P0..P3`: operational incident urgency.
- `RecorderPriority.P0..P3`: preservation/backpressure class.

There is no numeric, ordinal or automatic mapping between these namespaces. A RecorderPriority.P0 record can occur within an IncidentSeverity.P2 incident; an IncidentSeverity.P0 may contain records of several preservation priorities. Ambiguous prose was qualified in current Phase 12 surfaces.
