# Module Index

Chaque fiche suit le contrat obligatoire. Les dépendances pointent vers d'autres
modules conceptuels, pas vers une architecture de crates imposée. Tous sont M0
jusqu'à implémentation et preuve. L'activation effective vient du Capability
Manifest.

| Domaine | Modules |
|---|---|
| Market/data | [FeedAdapter](FeedAdapter.md), [Normalizer](Normalizer.md), [BookEngine](BookEngine.md), [MetadataEngine](MetadataEngine.md), [FeeEngine](FeeEngine.md), [PrecisionEngine](PrecisionEngine.md) |
| Routing | [GlobalGraph](GlobalGraph.md), [RouteEngine](RouteEngine.md), [NetConvert](NetConvert.md), [OpportunityEngine](OpportunityEngine.md) |
| Quant | [QuantEngine](QuantEngine.md), [OFIEngine](OFIEngine.md), [VolatilityEngine](VolatilityEngine.md) |
| Learning | [MarketAtlas](MarketAtlas.md), [ParticipantEngine](ParticipantEngine.md), [EdgeSurvivalEngine](EdgeSurvivalEngine.md), [LiquidityResponseEngine](LiquidityResponseEngine.md), [CrossMarketResponseEngine](CrossMarketResponseEngine.md) |
| Simulation | [CounterfactualSimulator](CounterfactualSimulator.md), [ExchangeEmulator](ExchangeEmulator.md), [ShadowBook](ShadowBook.md) |
| Allocation | [SizingEngine](SizingEngine.md), [OrderSlicingEngine](OrderSlicingEngine.md), [OpportunityPortfolioEngine](OpportunityPortfolioEngine.md), [InventoryEngine](InventoryEngine.md), [CapitalReachabilityEngine](CapitalReachabilityEngine.md), [BridgeEngine](BridgeEngine.md) |
| Safety/execution | [RiskEngine](RiskEngine.md), [ReservationEngine](ReservationEngine.md), [ExecutionCoordinator](ExecutionCoordinator.md), [OrderStateMachine](OrderStateMachine.md), [RecoveryEngine](RecoveryEngine.md), [ReconciliationEngine](ReconciliationEngine.md), [NonceManager](NonceManager.md), [Signer](Signer.md), [ExecutionTransport](ExecutionTransport.md) |
| Evidence | [Recorder](Recorder.md), [ReplayEngine](ReplayEngine.md), [AccountingEngine](AccountingEngine.md) |
| Platform | [InfrastructureMonitor](InfrastructureMonitor.md), [InfrastructureBenchmark](InfrastructureBenchmark.md), [InfrastructureROI](InfrastructureROI.md), [Deployment](Deployment.md), [botctl](botctl.md) |
| Cross-cutting added | [ClockAndRng](ClockAndRng.md), [CapabilityRegistry](CapabilityRegistry.md) |

## Universal constraints

Strong IDs/units, immutable snapshots, typed errors, no lookahead, versioned
configuration/models, reason codes, bounded work, hard risk gates and replay/live
parity apply everywhere. External Hyperliquid rules must be verified before the
module leaves M0/M1 as applicable.
