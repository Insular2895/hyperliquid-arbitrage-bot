# Extraction — infrastructure et ROI

## Sources

SRC-008 infrastructure; SRC-006 prime pour packaging/déploiement client.

## Contrats retenus

- VPS modeste par client, process/container unique, feed public; node-compatible
  sans node requis.
- Choix via benchmark feed age, RTT, jitter P99/P99.9, ack/fill, scheduler/CPU,
  loss/reconnect, recorder/storage et Docker overhead.
- InfrastructureBenchmark reproductible; InfrastructureROI sur gain marginal,
  coûts complets et incertitude.
- Upgrade seulement si LCB du gain couvre coût×facteur de sécurité calibré;
  downscale selon NetPnL, pas prestige.
- Provider/région, host/bridge, resources, node et tarifs restent OPEN/external.

Toutes capacités Hyperliquid, régions, versions, limites, specs/prix sont
`EXTERNAL_RULE_REQUIRES_REVALIDATION`.
