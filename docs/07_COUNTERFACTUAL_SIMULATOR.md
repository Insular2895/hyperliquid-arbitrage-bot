# 07 — Counterfactual Simulator

## Limite fondamentale

Le dataset historique ne révèle pas exactement ce que le marché aurait fait si
notre ordre avait existé. Le simulateur produit une distribution calibrée de
scénarios plausibles, jamais un « futur exact ».

## Architecture

```text
ReplayFeed + PointInTimeState + ExecutionPlan + RunManifest
  → latency arrival
  → ExchangeEmulator
  → ShadowBook mechanical consumption
  → queue/fill scenarios
  → optional aggregate/cross-market response
  → fills, residual exposure, recovery, accounting
  → outcome distribution + confidence gates
```

## Temps d'arrivée

`t_arrival=t0+L_compute+L_sign+L_network+L_exchange`. Chaque composante est une
distribution mesurée, conditionnée si utile; pas une constante empruntée à un
autre exchange. Clock et RNG sont injectés et leurs seeds/version dans le run.

## Deux modes

- `EXOGENOUS_REPLAY`: le futur historique demeure exogène; notre ordre subit le
  book mais ne prétend pas modifier le flux enregistré. Baseline/audit.
- `INTERACTIVE_COUNTERFACTUAL`: branche ShadowBook, consomme mécaniquement,
  génère réponse agrégée et cross-market pendant un horizon borné, puis rejoin
  policy explicite. `RESEARCH` avant calibration.

## Mécanique vs réponse

Notre ordre modifie mécaniquement seulement le book qu'il consomme. Tout effet
sur d'autres marchés ou ordres futurs appartient au modèle de réponse, avec
incertitude séparée. Une même profondeur ne peut pas être consommée par notre
shadow order et rester disponible sans règle de rejoin.

## Fidélités

| Niveau | Contenu | Usage |
|---|---|---|
| F0 | historique, aucune intervention | determinism/baseline |
| F1 | latence + consommation mécanique | taker validation initiale |
| F2 | queue/fill maker | MT après calibration |
| F3 | réponse agrégée/cross-market | capacité/impact avancés |
| F4 | interactif/agents | recherche/stress uniquement |

Une seule architecture et des composants activables; le RunManifest déclare la
fidelity. Une sortie ne peut revendiquer une fidélité supérieure à ses données.

## Monte Carlo et sorties

Scénarios : latence, survie, fill/partial, adverse selection, réponse, recovery.
Sorties : mean, median, quantiles, `P(PnL>0)`, VaR/ES, partial/recovery rates,
confidence intervals, calibration error et OOD. Le hot path consomme de petits
résumés versionnés; pas de Monte Carlo lourd synchrone.

## Validation

- Determinism même seed/run.
- No-lookahead audit et event-order preservation.
- Golden fills mécaniques.
- Calibration replay/shadow/micro-live par taille/régime/mode.
- Coverage des tails, partials et recovery; challenger vs baseline.
- Toute capacité `Q_validated` déclare fidelity et confidence.

## Sources

SRC-008 simulateur, SRC-007 participants, SRC-004 Formula Book, SRC-005 Data.
