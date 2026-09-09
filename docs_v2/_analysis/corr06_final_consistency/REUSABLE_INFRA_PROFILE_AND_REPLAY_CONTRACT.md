# Reusable InfraProfile and Replay Contract

## Purpose and non-authority

`InfraProfile` is an empirical research/benchmark/deployment-selection artifact. It is not market, account, execution or fill truth and is not required for normal Live operation. It cannot promote a feed/host or authorize Risk.

## Conceptual evidence shape

```text
InfraProfile {
  InfraProfileId, schema_version
  provider, region, datacenter_or_AZ, instance_family
  cpu_identity, kernel_profile, container_profile, network_profile, feed_profile
  build_commit, config_version
  measurement_window, sample_count, dataset_reference
  clock_quality, calibration_timestamp, validity_scope
  coherent_latency_sample_vectors
  read, rx_to_normalized, rx_to_book, local_compute,
    sign, send_handoff, ack_if_observed distributions
  scheduler_delay, cpu_utilization, cpu_steal, migrations, memory
  jitter, reconnects, gaps, duplicates, packet_loss_if_valid
  recorder_overhead, stability_metrics
  freshness_status, uncertainty
}
```

Unavailable observations are `UNAVAILABLE`, not zero. Profiles store empirical samples/quantiles/histograms first. If stages correlate, the default resamples coherent event/sample vectors or total latency; independent stage draws require evidence. More complex conditional models require sufficient support.

## Replay binding

Every run pins `DatasetId`, `InfraProfileId`, `ReplayMode`, `RunMode`, `SimulatorFidelity`, build/commit, `ConfigVersion`, `FormulaVersion`, model versions, `FeedProfile`, random seed, clock policy and `CounterfactualPolicyVersion`. The immutable Dataset remains actual recorded observation; the profile is a separate treatment. RAW receive timestamps are never rewritten.

Outputs use exactly one class: `ACTUAL_MEASURED`, `PAIRED_ACTUAL`, `REPLAYED`, `COUNTERFACTUAL`, `SHADOW`, `MICROLIVE_ACTUAL`, `LIVE_ACTUAL`. Counterfactual profiles and `+1/+5/+10/+25/+50/+100 ms` treatments remain modeled evidence.

## Lifecycle and economics

```text
candidate set → simultaneous campaign → profiles
→ Replay/Shadow comparison → robust economic/reliability ranking
→ winner → normal production monitoring
→ occasional short challenger revalidation
```

Continuous rental is not required. Ranking consumes existing QF-084..093 and one CORR-05 outcome distribution, with cost and reliability represented once. Passive Replay cannot calibrate actual IOC/partial/completion/Recovery/priority benefit; Micro-live remains required.
