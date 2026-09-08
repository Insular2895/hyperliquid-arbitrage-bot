# CORR-01 — Observability Storage and Cardinality Policy

DOCUMENTATION STATUS: DESIGN CONTRACT — IMPLEMENTATION NOT AUTHORIZED

## Three evidence planes

| Plane | Content | Cardinality | Retention authority | Runtime rule |
|---|---|---:|---|---|
| metrics | bounded counters, gauges and versioned histograms | low/bounded | Operations policy | asynchronous export; no IDs as labels |
| traces / analytical facts | per-evaluation, opportunity, attempt and timing lineage | high | Recorder/Data retention | non-blocking bounded capture with declared sampling/loss |
| critical journal | Risk decisions, intents, order/fill/state/Recovery/Reconciliation/accounting evidence | high but safety-critical | Recorder/Execution/Data | highest priority; never sampled for metric convenience |

## Allowed metric dimensions

Bounded dimensions may include `RunMode`, venue, strategy family, route-length class, market family, stage/reason family, capability/model/config major version, infrastructure instance class and validity state. Their value dictionaries and maximum series budget are versioned.

Forbidden metric labels include raw `OpportunityId`, `OpportunityEpisodeId`, `ExecutionId`, `IntentId`, `CLOID`, `OID`, `FillId`, client/account identifiers, arbitrary error text and unbounded market/route combinations. Those belong in access-controlled traces/journal records and may appear only as sampled exemplars where policy permits.

## Sampling

- counts and denominator facts are unsampled or carry an exact sampling-weight contract; silent trace-derived counting is forbidden;
- critical execution/safety evidence is never probabilistically sampled;
- high-volume rejected evaluations may use deterministic, versioned trace sampling after their aggregate counters and reason counts are secured;
- sampling decision, probability/rule, stratum, version and loss reason are stored with each retained trace;
- tail-triggered or error-triggered exemplars may supplement but never replace unbiased samples.

Exact rates, strata and retention durations are `CALIBRATED`. Any sampled estimator declares weighting and uncertainty. Data lost before the sampling decision is telemetry loss, not sampling.

## Retention and access

Retention follows existing hot/warm/archive and incident-window policy. Metric aggregates never replace RAW or critical journal retention requirements. Client/account/order data is isolated, least-privilege and redacted in exported review artifacts. Secrets, signatures and private keys are prohibited in every observability plane.

## Backend status

Metric, trace and storage backends remain an implementation choice and inherit `OPEN-015` for final telemetry tooling. CORR-01 defines semantic portability: changing a backend may not change IDs, populations, timing boundaries, loss accounting or truth precedence.
