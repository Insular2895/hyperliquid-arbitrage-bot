# Participant Model Dependency Audit

| Consumer | Relation |
|---|---|
| initial conservative TT | PARALLEL/OPTIONAL unless configured to consume model |
| TTT | CONDITIONAL ON CONFIGURED CONSUMER |
| MT / MTT | HARD for configured maker/response model; maker evidence independently required |
| Portfolio | CONDITIONAL ON CONFIGURED CONSUMER |
| Bridge | CONDITIONAL ON CONFIGURED CONSUMER |
| Infra ROI | PARALLEL analytic enrichment; hard only if decision contract consumes it |

Simple empirical baseline comes first. Every configured model version becomes a critical dependency for its exact consumer; no universal Participant gate is created.
