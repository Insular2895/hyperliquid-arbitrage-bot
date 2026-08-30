# 11 — Data Contracts

## Pipeline canonique

```text
RAW immutable → NORMALIZED typed events → STATE projections
→ FEATURES point-in-time → OPPORTUNITY/DECISION → EXECUTION/ACCOUNTING
```

Chaque frontière porte `schema_version`, source, provenance, timestamps et IDs.
Une migration produit une nouvelle version; elle ne réécrit pas silencieusement
l'historique.

## RawEvent

Champs minimaux : `event_id`, `recorder_sequence`, source/connection, venue,
market/account scope, event type, exchange timestamp/sequence si disponibles,
local wall-clock, monotonic time, original payload bytes, checksum/schema. Le
payload original permet de reparsing; RAW n'implique pas que le feed soit vrai,
seulement que c'est ce qui a été reçu.

## Normalized events

- Market/BookSnapshot/BookUpdate/Trade/MetadataChanged.
- AccountSnapshot/Balance/OrderUpdate/Fill/Fee/Nonce evidence.
- Opportunity/Decision/Reservation/ExecutionPlan/Recovery/Accounting.
- Health/DataGap/ClockAnomaly/ConfigOrModelActivated.

Chaque événement a un ID stable et une clé de déduplication documentée. Les
updates sans séquence fiable portent explicitement la limite de qualité.

## Snapshots et ownership

BookState, AccountState, GraphState, InventoryState, RiskState et FeatureState
sont snapshots immuables publiés par un single writer logique. Les lecteurs ne
mutent pas l'état; les références/version IDs empêchent les mélanges temporels.

## Décision et plan

`OpportunitySnapshot` contient route/version, state cutoff, candidate sizes,
direct/indirect curves et features. `DecisionRecord` conserve chaque gate,
reason code, formules/modèles/config versions et decomposed EV. `ExecutionPlan`
contient intentions, limits, modes, expiry, CLOIDs et reservations; aucune
quantité de jambe suivante n'est une promesse de fill.

## Orders, fills and accounting

`OrderIntent` est distinct d'`ExchangeOrder`; `Fill` est append-only. FillLedger
déduplique par FillId/clé exchange. Accounting entries équilibrées et
versionnées séparent route, fees, recovery, rebalance, inventory MTM, external
flows et infra costs.

## Clock et RNG

Interfaces injectées `Clock` (wall, monotonic, exchange mapping) et `Rng`.
Aucun appel direct non déterministe dans le core replay. `RunManifest` enregistre
seed/algorithm, clock mode, timezone, code/config/model/schema/dataset hashes,
fidelity et feature availability.

## No lookahead

À décision `t`, seules les données dont l'ordre d'arrivée enregistré est ≤ cutoff
sont visibles. Labels, fills futurs et révisions offline sont séparés des
features online. Un audit reconstruit chaque feature à partir de son lineage.

## Compatibilité

Writers/readers déclarent versions supportées. Unknown required field/version →
fail closed pour live; outil de migration offline pour historical. Le même
normalized contract entre dans LiveFeed et ReplayFeed.

## Sources

SRC-005 D4; exécution SRC-004; stockage SRC-003.
