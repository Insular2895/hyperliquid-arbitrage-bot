# Extraction — Validation and Definition of Done

## Source d'autorité

- SRC-006, Dossier 6/6, lignes 3595–6903.
- Statut documentaire : final / normatif.

## Maturité

`M0 SPECIFIED → M1 UNIT VALIDATED → M2 REPLAY VALIDATED → M3 SHADOW VALIDATED
→ M4 MICRO-LIVE VALIDATED → M5 LIVE VALIDATED`.

La maturité d'un module ne dépasse pas celle de ses dépendances critiques. Les
composants modifiant capital, ordres, risk ou fills ne sautent pas Shadow/
Micro-live.

## Tests obligatoires selon module

Unit, golden, property, integration, replay, fault injection, load, performance,
shadow, micro-live et chaos lorsque pertinent. Les modules critiques ont en plus
des tests de déterminisme, de backpressure, de corruption et de redémarrage.

Faults minimum : feed/account disconnect, réponse HTTP perdue, partial/duplicate
fill, cancel race, crash, disk full, CPU saturation, clock, invalid config, model
NaN, Docker SIGTERM/SIGKILL/reboot.

## Gates

- Release : tests critiques, golden, replay déterministe, aucune régression risk/
  sécurité critique, performance dans le budget. Changement trading exige Shadow
  et Micro-live.
- Micro-live : Shadow stable, unknown/recovery/reconciliation/accounting validés,
  book fiable.
- Scaling : calibration, tail support, OOD, recovery/slippage/infra stables;
  progression par bands uniquement dans `Q_validated`.
- Modèle/feature : ablation, calibration, economic lift après coût de latence,
  risk/stability/complexity acceptables; `LCB(ModelValue)>0` avec marge.
- Infrastructure : même binaire/config/fenêtres, first-arrival/feed-age/RTT/jitter/
  CPU/Recorder/Docker/clock/reconnect; choix sur NetPnL et stabilité, pas ping seul.

## Validation scientifique

Golden datasets diversifiés, incidents, régimes, out-of-sample temporel,
walk-forward, aucune fuite random train/test. Rapports de calibration et de
validation versionnent dataset, période, features, support OOD, baseline,
résultats replay/shadow/micro-live, risk et performance. Les résultats négatifs
sont conservés.

Le live ne s'auto-entraîne pas : il collecte; Research calibre; Validation promeut
ou rétrograde. Chaque capability porte stratégie, marché, taille, mode, modèles,
niveau, dates et restrictions. Code support n'équivaut pas à production support.

## Roadmap normative extraite

1. Domain types/schemas
2. Hyperliquid adapters
3. Recorder
4. Book Engine
5. Metadata/Fee/Precision
6. Graph/Routes
7. NetConvert/Formula Core
8. Replay Engine
9. Basic Opportunity Engine
10. Account/Inventory/Reservations
11. Risk core
12. Execution State Machine
13. Hyperliquid Execution Transport
14. Recovery/Reconciliation
15. Quant microstructure
16. Market Atlas
17. Sizing
18. Simulator F0/F1
19. Shadow
20. Micro-live TT
21. Survival/Participant Models
22. Advanced Simulator
23. MT/MTT
24. Portfolio Optimizer
25. Bridge/Capital relocation
26. Scaling

Le travail progresse en vertical slices; Recorder tourne tôt et Replay précède les
modèles sophistiqués. Architecture final-capable, activation progressive.
