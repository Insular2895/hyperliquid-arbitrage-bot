# Contradiction report

## RESOLVED

| ID | Tension | Résolution | Autorité |
|---|---|---|---|
| C-001 | Python live puis Rust live | Rust core live/replay; Python offline | SRC-004/006, chronologie |
| C-002 | Triangle-first vs 2-leg-first | les deux sont connus; OWA TT/MT et triangle TT/MTT sont core, priorité mesurée | SRC-003/004 |
| C-003 | OWA sans direct | sans direct = bridge/relocation | SRC-003/004 |
| C-004 | Edge constant vs fonction de taille | `Edge(q)` | SRC-004 QF-026 |
| C-005 | Taille fixe vs sizing | sizing dynamique et `Q_validated`; petites tailles réservées au micro-live | SRC-004/006 |
| C-006 | Maker second leg | TM/MM supportés architecturalement mais disabled | SRC-004 |
| C-007 | FOK/market/TWAP vs IOC | protected IOC taker, ALO maker; aucun market aveugle | SRC-004 |
| C-008 | Retry timeout | unknown puis reconciliation; no blind retry | SRC-004 |
| C-009 | Route initiale prioritaire en recovery | aucune priorité; optimiser depuis l'état courant | SRC-004/005 |
| C-010 | Profit global comme budget de risque | jamais de relaxation d'un hard gate | SRC-005 |
| C-011 | RAW exhaustif prod vs stockage borné | collecte R&D large; prod sélective et priorisée | SRC-003/005 |
| C-012 | Node immédiat vs VPS public | public feed initial, node soumis au ROI | SRC-006/008 |
| C-013 | SaaS mutualisé vs installations client | VPS/client isolé | SRC-006 |

## LIKELY_RESOLVED

| ID | Sujet | Position de consolidation | Validation requise |
|---|---|---|---|
| C-014 | HOT/WARM/COLD « routes » ou « assets/clusters » | état de calcul applicable aux régions et routes; IDs et transitions à spécifier | oui |
| C-015 | Un ou plusieurs ordres dans une action/batch | batch transport possible mais aucune atomicité présumée | oui, règle exchange externe |
| C-016 | One signer/process | invariant opérationnel initial; extensions multi-worker nécessitent ADR futur | oui |

## UNRESOLVED

Aucune contradiction architecturale critique n'est laissée sans traitement. Les
incertitudes empiriques figurent dans `OPEN_ITEMS.md`; elles ne sont pas des
contradictions.

## SOURCE_ERROR

- Attribuer un PnL OWA à une route sans comparateur direct.
- Compter le slicing comme création de profondeur.
- Utiliser une annulation envoyée comme preuve d'annulation.
- Traiter `SENT` ou un timeout comme « non rempli ».
- Utiliser des règles, tarifs ou performances externes datés comme constantes.
