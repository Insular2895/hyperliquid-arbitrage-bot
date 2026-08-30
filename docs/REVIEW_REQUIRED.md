# Review required

## Summary of what was consolidated

Huit sources ont été inventoriées et séparées en historique, notes transverses
et six dossiers de fermeture. La documentation couvre produit, architecture,
routes/formules, microstructure/participants/simulation, capital/risk/exécution,
données/replay, infrastructure/déploiement/sécurité, validation, roadmap,
operations, specs et ADR.

## Major locked decisions

Rust live/replay; Python research; venue-aware graph et routes 2/3 pré-calculées;
HOT/WARM/COLD; OWA exige direct; NetConvert unique; TT/MT/TTT/MTT core; protected
IOC/ALO; actual fills/no blind retry; recovery/reconciliation first-class; hard
risk constitution; one VPS/client/container/process; no SaaS hot-path; feed
public initial; distribution contrefactuelle et modèles participants agrégés.

## Remaining calibrated parameters

Freshness/timeouts, thresholds EV/P+/ES/confidence, tailles/capital/bandes,
inventaire/stranded penalties, OFI/volatility/hazard/maker/cross-market models,
HOT policy, recorder retention, health/SLO, infra safety factor and resources.

## Remaining open questions

Voir `_analysis/OPEN_ITEMS.md`, notamment règles exchange courantes, meilleur VPS
et réseau Docker, node ROI, modèle champion, maker support et capital micro-live.

## External facts requiring revalidation

Prix/precision/frais/nonce/rate limits/endpoints/permissions Hyperliquid; région
et node; SDK/runtime/Docker/Ubuntu/security versions; fournisseurs et tarifs.
Aucun de ces faits n'a été vérifié sur Internet pendant cette mission.

## Recommended review order

1. MASTER ARCHITECTURE
2. PRODUCT/SCOPE
3. FORMULA BOOK
4. RISK CONSTITUTION
5. EXECUTION STATE MACHINE
6. DATA CONTRACTS
7. COUNTERFACTUAL SIMULATOR
8. MARKET PARTICIPANTS
9. INVENTORY / CAPITAL
10. INFRASTRUCTURE
11. DEPLOYMENT
12. VALIDATION MATRIX
13. IMPLEMENTATION ROADMAP
14. MODULE SPECS
15. ADR / Open Items / Traceability

## Review decisions requested

Valider ou amender l'autorité documentaire, les décisions LOCKED proposées, les
frontières V1/FUTURE, la hiérarchie de risk, les états d'exécution, la roadmap
et le traitement des external rules. Ne pas lancer l'implémentation avant cette
revue.

`DOCUMENTATION STATUS: REVIEW REQUIRED`
