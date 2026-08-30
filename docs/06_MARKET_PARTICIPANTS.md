# 06 — Market Participants

## Direction principale

Prédire la distribution de réponse agrégée conditionnelle du marché et la
survie d'une opportunité. Ne pas inventer des centaines d'agents présentés
comme la vérité.

## Données et épisodes

`OpportunityEpisode` conserve features au départ, edge curve, horizon, event de
fin, censure, réponse de liquidité, marché voisin, mode/taille et outcome. Garder
opportunités exécutées, rejetées, proches du seuil et périodes normales pour
éviter le biais de sélection.

## Modèles progressifs

1. Survie empirique stratifiée : champion initial.
2. Hazard discret calibré : challenger interprétable.
3. GBDT/survival ML : seulement si lift OOS.
4. Hawkes, queue-reactive et agent simulation : `RESEARCH`/stress tests.

Training Python offline; artefact signé/versionné; inférence Rust bornée. Un
challenger n'est promu que si calibration, tail risk, economic lift et coût de
latence satisfont la matrice de validation.

## Niveaux de fidélité participants

- P0 Historical participants : seulement les événements observés.
- P1 Edge Survival : durée/hazard/capture.
- P2 Aggregate Response : liquidité conditionnelle.
- P3 Cross Market : voisinages de réponse clairsemés.
- P4 Participant Signatures : pseudonymes/clusters validés.
- P5 Interactive Research : agents/scénarios, jamais vérité live par défaut.

P0→P5 est distinct de F0→F4 du simulateur; le RunManifest déclare les deux
capacités si elles sont utilisées.

## Participant pseudonyme

`ParticipantAddress`, `BehaviourSignature`, `BehaviourCluster` peuvent être
dérivés si les données le permettent. Une adresse est un pseudonyme observable,
pas une identité prouvée. La feature reste désactivée sans support suffisant,
stabilité temporelle et lift prédictif OOS.

## Cross-market

Apprendre des voisinages clairsemés `i→j` par horizon/régime. Lead-lag et event
study produisent des candidats; seules les distributions validées alimentent le
simulateur. Pas de matrice dense globale naïve ni d'inférence causale automatique.

## Maker

Estimer fill CDF/survival, partial probability, time-to-fill, adverse selection,
edge survival après fill et recovery. Avec L2, queue position est un intervalle
pessimiste/optimiste/probabiliste; avec L4, utiliser seulement la fidélité
réellement observée. Maker expiry est calibrée.

## Fallback

OOD, désaccord, drift ou données insuffisantes → confiance LOW/REJECT, modèle
empirique conservateur ou mode taker; jamais extrapolation silencieuse.

## Sources

SRC-007 et QF-044..058, 081..104.
