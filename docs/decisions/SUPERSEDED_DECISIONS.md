# Superseded decisions

Ce registre évite qu'une idée ancienne soit confondue avec une contradiction
active. Le remplacement est documentaire et reste soumis à la revue du
propriétaire.

| Ancienne proposition | Statut | Remplacement canonique | Provenance |
|---|---|---|---|
| Python comme moteur live | SUPERSEDED | Rust production/replay; Python research | SRC-002, SRC-004 |
| Python + C++ hot path | SUPERSEDED | Rust; C++ seulement après benchmark | SRC-002 |
| Python première implémentation jetable | SUPERSEDED | architecture finale activée progressivement | SRC-002, SRC-006 |
| Scanner toutes les routes au même coût | SUPERSEDED | graphe global + HOT/WARM/COLD + watcher | SRC-001/002 |
| Triangle comme stratégie unique | SUPERSEDED | moteur routing 2-leg + triangle | SRC-002/003 |
| OWA sans route directe | SOURCE_ERROR | bridge/relocation, jamais OWA | SRC-003/004 |
| Edge calculé au mid/last | REJECTED | bid/ask et marche L2 exacte | SRC-001/002/004 |
| Fee spot constante codée en dur | REJECTED | FeeEngine dynamique et historisé | SRC-003/004 |
| Thresholds Binance (`0.12%`, `10M`, `35ms`, `120ms`) | SUPERSEDED | calibration Hyperliquid | SRC-001/003 |
| Taille fixe de 40–50 € | SUPERSEDED | sizing dynamique; faible taille seulement micro-live/probe | SRC-001/003 |
| 40 ordres de 50 € créent plus de profondeur | SOURCE_ERROR | slicing ne change pas la capacité mécanique | SRC-003/004 |
| Cinq niveaux L2 fixes | SUPERSEDED | marcher autant de niveaux que la taille exige | SRC-002/004 |
| FOK/TWAP systématique | SUPERSEDED | IOC limité protégé; réduire/rejeter si capacité insuffisante | SRC-001/004 |
| Market order aveugle | REJECTED | protected IOC/ALO selon mode | SRC-001/004 |
| Retry d'ordre sur timeout | REJECTED | état unknown puis reconciliation, jamais blind retry | SRC-001/004 |
| Leg suivante sur output théorique | REJECTED | actual fill seulement | SRC-004 |
| Maker en seconde jambe par défaut (`TM/MM`) | REJECTED FOR CORE | support futur, disabled | SRC-003/004 |
| Continuer la route initiale coûte que coûte | REJECTED | comparer EV_continue et EV_recovery | SRC-003/004 |
| Profit global relâche le risque local | REJECTED | les hard gates locaux dominent | SRC-002/005 |
| White-list statique d'assets | SUPERSEDED | CORE/TRANSIT/EXCLUDED appris et gouverné | SRC-001/003 |
| Écrire directement vers iCloud/object storage | REJECTED | NVMe local, chunks clos, upload asynchrone vérifié | SRC-003/005 |
| Conserver tout le RAW pour toujours | SUPERSEDED | rétention mesurée, priorité executions/incidents/golden | SRC-003 |
| Une instance SaaS mutualisée | REJECTED | un VPS/client, compte/signer isolés | SRC-006 |
| Licence peut stopper la récupération | REJECTED | recovery/reconciliation restent possibles | SRC-006 |
| Node Hyperliquid requis dès le départ | SUPERSEDED | feed public initial; node si ROI prouvé | SRC-002/008 |
| Raspberry Pi production, GPU/FPGA hot path | REJECTED | VPS CPU; accélération seulement si preuve | SRC-001/002 |
| Black-Scholes/Greeks dans le core | REJECTED | hors périmètre spot routing V1 | SRC-004 |
