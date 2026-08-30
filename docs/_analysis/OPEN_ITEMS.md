# Open items

Seuls les paramètres ou choix qui exigent une mesure sont listés. Aucun n'est
un seuil caché à inventer pendant l'implémentation.

| ID | Question | Pourquoi non résolu / preuve requise | Expérience | Modules | Bloquant |
|---|---|---|---|---|---|
| OPEN-001 | Seuil exact de book stale/desync | dépend du feed et de la survie d'edge | replay + shadow par âge de book | BookEngine, RiskEngine | live |
| OPEN-002 | ACK/unknown timeout et maker max age | distributions réelles requises | micro-live et failure injection | OrderStateMachine | live |
| OPEN-003 | Minimum edge/RAEV, P_min, ES/CVaR | compromis économique et tail risk | walk-forward + Monte Carlo calibré | QuantEngine, RiskEngine | live |
| OPEN-004 | Bandes inventaire et pénalités | dépendent des flux et sorties | replay multi-inventory | InventoryEngine | live |
| OPEN-005 | Recovery reserve et limites par asset/route/global | distribution des partials/recovery | scénarios adversariaux + micro-live | Risk, Recovery | live |
| OPEN-006 | OFI/MLOFI weights, fenêtres et jump threshold | prédictivité Hyperliquid inconnue | walk-forward/OOS | OFIEngine, VolatilityEngine | non |
| OPEN-007 | Champion participants/survival | plusieurs modèles plausibles | benchmark calibration + economic lift OOS | Participant, Survival | non |
| OPEN-008 | Modèle maker et queue bounds | fidélité L2/L4 et fills insuffisants | shadow puis micro-live | Participant, ExchangeEmulator | MT |
| OPEN-009 | Voisinages cross-market | causalité/lift à démontrer | event studies + OOS | CrossMarketResponse | non |
| OPEN-010 | Taille, grille puis raffinement du sizing | courbes discontinues | benchmark exactitude/latence | SizingEngine | live |
| OPEN-011 | Politique HOT/WARM/COLD et hystérésis | coût CPU vs missed edge | replay de politiques | MarketAtlas | non |
| OPEN-012 | Rétention/chunk/checkpoint exacts | débit réel et budget stockage | recorder 24h + recovery test | Recorder, Replay | non |
| OPEN-013 | Fournisseur/région VPS et taille machine | latence/jitter/fiabilité/prix changent | `hl-infra-benchmark` multi-candidats | InfraBenchmark | prod |
| OPEN-014 | Docker host vs bridge networking | impact et sécurité environnementaux | A/B benchmark identique | Deployment, Infra | prod |
| OPEN-015 | Node ou feed alternatif | valeur spot et coût non prouvés | benchmark causal + LCB ROI | InfraROI | non |
| OPEN-016 | Facteur de sécurité ROI infra | tolérance au risque | bootstrap/incertitude coûts | InfraROI | non |
| OPEN-017 | Seuils santé/disque/backpressure | débit et SLO réels requis | soak/failure injection | Recorder, Operations | live |
| OPEN-018 | Mécanique exacte prix/frais/nonce/rate limits Hyperliquid | règle externe évolutive | vérification officielle avant implémentation | Metadata/Fee/Nonce/Transport | phase concernée |
| OPEN-019 | Capital micro-live et paliers | décision propriétaire + résultats | validation M4/M5 | Validation | micro-live |
| OPEN-020 | Cross-venue trading et rebalancing | hors V1 active, risques additionnels | ADR et programme validation futurs | Graph, Inventory, Bridge | non V1 |
