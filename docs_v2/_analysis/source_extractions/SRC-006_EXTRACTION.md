# SRC-006 Extraction

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

- Source ID: `SRC-006`
- Filename: `DOSSIER 56 — DOCKER, DÉPLOIEMENT, SÉCURITÉ ET DISTRIBUTION CLIENT.md`
- SHA-256: `a535a5fa04feaaf4056ab7b3880f8cbcb803a6b1300d25ed02c96aa14558115d`
- Line count: 6903
- Authority profile: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Main domains: VALIDATION, DEPLOYMENT, RISK, INFRA, CLIENT, EXECUTION, ACCOUNTING, ARCH, OPERATIONS, SECURITY, BENCHMARK, PRODUCT
- Extraction completed: YES

> Une unité correspond à une section/règle matériellement identifiable. La formulation reste candidate jusqu’à la passe métier lorsqu’elle ne relève pas d’un dossier de fermeture.

### SRC-006-ITEM-0004 — 1. Objectif

- Source: `SRC-006`
- Location: lines 5–40; heading `1. Objectif`
- Domain tags: DEPLOYMENT, INFRA, SECURITY, CLIENT, CAPITAL, PRODUCT, ARCH
- Source statement: 1. Objectif: Le produit vendu n’est pas un SaaS centralisé. installée dans l’environnement du client.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `1. Objectif` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0002`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, SECURITY, CLIENT, CAPITAL, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0005 — 2. Principe fondamental

- Source: `SRC-006`
- Location: lines 41–76; heading `2. Principe fondamental`
- Domain tags: DEPLOYMENT, DATA
- Source statement: 2. Principe fondamental: Les données importantes sont :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `2. Principe fondamental` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0003`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0006 — 3. Architecture cible client

- Source: `SRC-006`
- Location: lines 77–111; heading `3. Architecture cible client`
- Domain tags: CLIENT, ARCH, EXECUTION, RISK, RECORDER, DATA, CLOCK, INFRA
- Source statement: 3. Architecture cible client: ├── chrony / host clock sync Le container monte uniquement ce dont il a besoin.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `3. Architecture cible client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0001`; supporting items: none found by conservative heading match; domain indexes `CLIENT, ARCH, EXECUTION, RISK, RECORDER, DATA, CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0007 — 4. Une seule image principale

- Source: `SRC-006`
- Location: lines 112–147; heading `4. Une seule image principale`
- Domain tags: DEPLOYMENT, EXECUTION, RISK, RECORDER, INFRA, OPERATIONS, SIMULATOR, PARTICIPANTS
- Source statement: 4. Une seule image principale: Je recommande au départ : Pas une architecture de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `4. Une seule image principale` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0004`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RISK, RECORDER, INFRA, OPERATIONS, SIMULATOR, PARTICIPANTS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0008 — 5. Pourquoi un container principal

- Source: `SRC-006`
- Location: lines 148–175; heading `5. Pourquoi un container principal`
- Domain tags: DEPLOYMENT, RISK, DATA, CLIENT, ARCH
- Source statement: 5. Pourquoi un container principal: dans plusieurs containers introduirait : Les modules restent séparés dans le code, pas nécessairement physiquement.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `5. Pourquoi un container principal` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0005`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, DATA, CLIENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0009 — 6. Architecture logique ≠ architecture physique

- Source: `SRC-006`
- Location: lines 176–189; heading `6. Architecture logique ≠ architecture physique`
- Domain tags: DEPLOYMENT, ARCH
- Source statement: 6. Architecture logique ≠ architecture physique: Le bot peut avoir : tout en tournant dans :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `6. Architecture logique ≠ architecture physique` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0006`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0010 — 7. Processus principal

- Source: `SRC-006`
- Location: lines 190–207; heading `7. Processus principal`
- Domain tags: DEPLOYMENT, EXECUTION, RISK, RECORDER, ARCH
- Source statement: 7. Processus principal: et ce processus héberge :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `7. Processus principal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0007`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RISK, RECORDER, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0011 — 8. Pas de processus critique externe

- Source: `SRC-006`
- Location: lines 208–226; heading `8. Pas de processus critique externe`
- Domain tags: DEPLOYMENT, INFRA, LICENSE, CLIENT, ROUTING, HOT_WARM_COLD, PRODUCT, ARCH
- Source statement: 8. Pas de processus critique externe: Une exécution ne doit jamais dépendre en temps réel de : Le hot path doit rester :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `8. Pas de processus critique externe` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0008`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, LICENSE, CLIENT, ROUTING, HOT_WARM_COLD, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0012 — 9. OCI image

- Source: `SRC-006`
- Location: lines 227–240; heading `9. OCI image`
- Domain tags: DEPLOYMENT
- Source statement: 9. OCI image: L’image doit respecter le standard OCI afin de fonctionner sur : même si notre chemin officiellement supporté reste initialement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `9. OCI image` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0009`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0013 — 10. Architecture CPU de référence

- Source: `SRC-006`
- Location: lines 241–260; heading `10. Architecture CPU de référence`
- Domain tags: DEPLOYMENT, INFRA, ARCH, BENCHMARK, CLIENT, PRODUCT, FUTURE
- Source statement: 10. Architecture CPU de référence: peut être ajoutée plus tard si benchmarks et demande client le justifient.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `10. Architecture CPU de référence` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0010`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, ARCH, BENCHMARK, CLIENT, PRODUCT, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0014 — 11. Pas de multi-architecture non testée

- Source: `SRC-006`
- Location: lines 261–278; heading `11. Pas de multi-architecture non testée`
- Domain tags: DEPLOYMENT, ARCH, EXECUTION, DETERMINISM, INFRA, BENCHMARK, REPLAY
- Source statement: 11. Pas de multi-architecture non testée: Supporter ARM ne signifie pas seulement :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `11. Pas de multi-architecture non testée` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0011`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ARCH, EXECUTION, DETERMINISM, INFRA, BENCHMARK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0015 — 12. Dockerfile multi-stage

- Source: `SRC-006`
- Location: lines 279–293; heading `12. Dockerfile multi-stage`
- Domain tags: DEPLOYMENT, ARCH
- Source statement: 12. Dockerfile multi-stage: Le compilateur Rust, Cargo et les sources ne doivent pas être présents dans l’image runtime.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `12. Dockerfile multi-stage` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0012`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0016 — 13. Runtime image minimale

- Source: `SRC-006`
- Location: lines 294–322; heading `13. Runtime image minimale`
- Domain tags: DEPLOYMENT, BENCHMARK
- Source statement: 13. Runtime image minimale: Mais ne pas choisir une image ultra-minimale au détriment de :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `13. Runtime image minimale` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0013`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0017 — 14. Pas d’optimisation build aveugle

- Source: `SRC-006`
- Location: lines 323–341; heading `14. Pas d’optimisation build aveugle`
- Domain tags: DEPLOYMENT, INFRA, CLIENT
- Source statement: 14. Pas d’optimisation build aveugle: Mais le binaire client doit rester compatible avec la classe CPU supportée. sur notre machine de build pourrait produire un binaire incompatible avec certains VPS clients.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `14. Pas d’optimisation build aveugle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0014`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0018 — 15. CPU feature baseline

- Source: `SRC-006`
- Location: lines 342–351; heading `15. CPU feature baseline`
- Domain tags: DEPLOYMENT, INFRA
- Source statement: 15. CPU feature baseline: Définir une baseline CPU officielle. uniquement après vérification que tous nos fournisseurs recommandés la supportent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `15. CPU feature baseline` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0015`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0019 — 16. Release build reproducible

- Source: `SRC-006`
- Location: lines 352–361; heading `16. Release build reproducible`
- Domain tags: DEPLOYMENT, DETERMINISM, ARCH
- Source statement: 16. Release build reproducible: Chaque build doit être lié à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `16. Release build reproducible` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0016`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DETERMINISM, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0020 — 17. Image identification

- Source: `SRC-006`
- Location: lines 362–378; heading `17. Image identification`
- Domain tags: DEPLOYMENT, DATA, CLOCK
- Source statement: 17. Image identification: Chaque image possède : semantic version
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `17. Image identification` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0017`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0021 — 18. Le digest est l’identité réelle

- Source: `SRC-006`
- Location: lines 379–393; heading `18. Le digest est l’identité réelle`
- Domain tags: DEPLOYMENT
- Source statement: 18. Le digest est l’identité réelle: Chaque installation doit enregistrer le digest exact exécuté.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `18. Le digest est l’identité réelle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0018`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0022 — 19. Pas de latest en production

- Source: `SRC-006`
- Location: lines 394–411; heading `19. Pas de latest en production`
- Domain tags: DEPLOYMENT, PRODUCT, CLIENT
- Source statement: 19. Pas de latest en production: et idéalement digest pinning :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `19. Pas de latest en production` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0019`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, PRODUCT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0023 — 20. Pourquoi

- Source: `SRC-006`
- Location: lines 412–420; heading `20. Pourquoi`
- Domain tags: DEPLOYMENT
- Source statement: 20. Pourquoi: peut changer le logiciel sans changement visible de configuration. Inacceptable pour un moteur financier.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `20. Pourquoi` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0020`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0024 — 21. Registry

- Source: `SRC-006`
- Location: lines 421–437; heading `21. Registry`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 21. Registry: L’image peut être distribuée via : Le fournisseur précis n’est pas une décision architecturale critique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `21. Registry` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0021`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0025 — 22. Accès registry

- Source: `SRC-006`
- Location: lines 438–452; heading `22. Accès registry`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 22. Accès registry: Chaque client reçoit un credential :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `22. Accès registry` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0022`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0026 — 23. Image signing

- Source: `SRC-006`
- Location: lines 453–461; heading `23. Image signing`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 23. Image signing: Les releases doivent idéalement être signées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `23. Image signing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0023`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0027 — 24. Supply-chain security

- Source: `SRC-006`
- Location: lines 462–471; heading `24. Supply-chain security`
- Domain tags: SECURITY, DEPLOYMENT
- Source statement: 24. Supply-chain security: Chaque release devrait progressivement fournir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `24. Supply-chain security` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0003`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0028 — 25. SBOM

- Source: `SRC-006`
- Location: lines 472–487; heading `25. SBOM`
- Domain tags: SECURITY, CLIENT, ARCH
- Source statement: 25. SBOM: Software Bill of Materials :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `25. SBOM` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0004`; supporting items: none found by conservative heading match; domain indexes `SECURITY, CLIENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0029 — 26. Vulnerability scanning

- Source: `SRC-006`
- Location: lines 488–496; heading `26. Vulnerability scanning`
- Domain tags: DEPLOYMENT
- Source statement: 26. Vulnerability scanning: Chaque image avant release : Aucune vulnérabilité critique connue non acceptée explicitement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `26. Vulnerability scanning` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0024`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0030 — 27. Container user

- Source: `SRC-006`
- Location: lines 497–510; heading `27. Container user`
- Domain tags: DEPLOYMENT
- Source statement: 27. Container user: Le processus ne tourne pas en :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `27. Container user` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0025`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0031 — 28. Root filesystem

- Source: `SRC-006`
- Location: lines 511–519; heading `28. Root filesystem`
- Domain tags: DEPLOYMENT
- Source statement: 28. Root filesystem: pour le filesystem du container. Seuls les volumes explicitement nécessaires sont writable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `28. Root filesystem` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0026`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0032 — 29. Writable paths

- Source: `SRC-006`
- Location: lines 520–536; heading `29. Writable paths`
- Domain tags: DEPLOYMENT, EXECUTION, RECORDER, DATA
- Source statement: 29. Writable paths: Aucun besoin d’écrire dans :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `29. Writable paths` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0027`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RECORDER, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0033 — 30. Linux capabilities

- Source: `SRC-006`
- Location: lines 537–550; heading `30. Linux capabilities`
- Domain tags: DEPLOYMENT
- Source statement: 30. Linux capabilities: Puis rajouter uniquement une capability strictement nécessaire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `30. Linux capabilities` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0028`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0034 — 31. Pas de --privileged

- Source: `SRC-006`
- Location: lines 551–559; heading `31. Pas de --privileged`
- Domain tags: SECURITY, DEPLOYMENT
- Source statement: 31. Pas de --privileged: Si le bot demande : la conception doit être remise en question.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `31. Pas de --privileged` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0005`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0035 — 32. Pas de Docker socket

- Source: `SRC-006`
- Location: lines 560–568; heading `32. Pas de Docker socket`
- Domain tags: DEPLOYMENT, RISK
- Source statement: 32. Pas de Docker socket: Cela donnerait pratiquement le contrôle du host.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `32. Pas de Docker socket` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0029`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0036 — 33. No host filesystem mount

- Source: `SRC-006`
- Location: lines 569–577; heading `33. No host filesystem mount`
- Domain tags: DEPLOYMENT, INFRA
- Source statement: 33. No host filesystem mount: Ne pas monter : du VPS.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `33. No host filesystem mount` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0030`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0037 — 34. PID namespace

- Source: `SRC-006`
- Location: lines 578–585; heading `34. PID namespace`
- Domain tags: DEPLOYMENT
- Source statement: 34. PID namespace: Aucune raison de donner :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `34. PID namespace` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0031`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0038 — 35. Clock

- Source: `SRC-006`
- Location: lines 586–599; heading `35. Clock`
- Domain tags: DEPLOYMENT, CLOCK, INFRA
- Source statement: 35. Clock: Le container utilise l’horloge du host. tourne sur le VPS host.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `35. Clock` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0032`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0039 — 36. Clock health

- Source: `SRC-006`
- Location: lines 600–603; heading `36. Clock health`
- Domain tags: OPERATIONS, CLOCK
- Source statement: 36. Clock health: Le bot lit/mesure la qualité temporelle disponible. Il ne modifie pas lui-même l’horloge système.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `36. Clock health` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0005`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0040 — 37. Network mode

- Source: `SRC-006`
- Location: lines 604–615; heading `37. Network mode`
- Domain tags: DEPLOYMENT, BENCHMARK, BRIDGE
- Source statement: 37. Network mode: Deux candidats doivent être benchmarkés :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `37. Network mode` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0033`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK, BRIDGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0041 — 38. Pourquoi host peut être intéressant

- Source: `SRC-006`
- Location: lines 616–626; heading `38. Pourquoi host peut être intéressant`
- Domain tags: DEPLOYMENT
- Source statement: 38. Pourquoi host peut être intéressant: Mais cela réduit une partie de l’isolation réseau.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `38. Pourquoi host peut être intéressant` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0034`; supporting items: SRC-002-ITEM-0024; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0042 — 39. Décision par benchmark

- Source: `SRC-006`
- Location: lines 627–651; heading `39. Décision par benchmark`
- Domain tags: DEPLOYMENT, BENCHMARK, EXECUTION, RECORDER, INFRA, BRIDGE
- Source statement: 39. Décision par benchmark: Nous ne déclarons pas :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `39. Décision par benchmark` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0035`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK, EXECUTION, RECORDER, INFRA, BRIDGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0043 — 40. Docker overhead gate

- Source: `SRC-006`
- Location: lines 652–680; heading `40. Docker overhead gate`
- Domain tags: DEPLOYMENT, BENCHMARK
- Source statement: 40. Docker overhead gate: Docker n’est acceptable comme mode officiel si :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `40. Docker overhead gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0036`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0044 — 41. Resource limits

- Source: `SRC-006`
- Location: lines 681–689; heading `41. Resource limits`
- Domain tags: DEPLOYMENT, RISK, INFRA, CAPITAL
- Source statement: 41. Resource limits: Docker Compose peut définir : mais éviter de trop serrer.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `41. Resource limits` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0037`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, INFRA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0045 — 42. Pourquoi

- Source: `SRC-006`
- Location: lines 690–702; heading `42. Pourquoi`
- Domain tags: DEPLOYMENT, EXECUTION, RISK, INFRA
- Source statement: 42. Pourquoi: alors que le processus utilise occasionnellement 1.1GB peut provoquer : ce qui est pire qu’une RAM légèrement moins contrôlée.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `42. Pourquoi` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0038`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0046 — 43. Recommended CPU pinning

- Source: `SRC-006`
- Location: lines 703–711; heading `43. Recommended CPU pinning`
- Domain tags: DEPLOYMENT, INFRA, BENCHMARK
- Source statement: 43. Recommended CPU pinning: Sur les VPS où c’est utile : peut réserver certains vCPU au bot.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `43. Recommended CPU pinning` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0039`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0047 — 44. Hot-path priority

- Source: `SRC-006`
- Location: lines 712–721; heading `44. Hot-path priority`
- Domain tags: DEPLOYMENT, ROUTING, HOT_WARM_COLD, RECORDER
- Source statement: 44. Hot-path priority: Les threads critiques peuvent être séparés de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `44. Hot-path priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0040`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ROUTING, HOT_WARM_COLD, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0048 — 45. Swap

- Source: `SRC-006`
- Location: lines 722–740; heading `45. Swap`
- Domain tags: DEPLOYMENT, INFRA, BENCHMARK, ROUTING, HOT_WARM_COLD, PRODUCT
- Source statement: 45. Swap: Pour le VPS production : ne doit pas être dépendante du swap.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `45. Swap` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0041`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, BENCHMARK, ROUTING, HOT_WARM_COLD, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0049 — 46. OOM handling

- Source: `SRC-006`
- Location: lines 741–748; heading `46. OOM handling`
- Domain tags: DEPLOYMENT, RISK
- Source statement: 46. OOM handling: Si le bot approche dangereusement de la mémoire disponible :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `46. OOM handling` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0042`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0050 — 47. Configuration hors image

- Source: `SRC-006`
- Location: lines 749–761; heading `47. Configuration hors image`
- Domain tags: DEPLOYMENT, RISK, SECURITY, LICENSE, CLIENT, CAPITAL
- Source statement: 47. Configuration hors image: L’image ne contient pas : Ces éléments sont injectés au runtime.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `47. Configuration hors image` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0043`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, SECURITY, LICENSE, CLIENT, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0051 — 48. Configuration layout

- Source: `SRC-006`
- Location: lines 762–769; heading `48. Configuration layout`
- Domain tags: DEPLOYMENT, RISK
- Source statement: 48. Configuration layout: /config/bot.toml /config/risk.toml
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `48. Configuration layout` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0044`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0052 — 49. bot.toml

- Source: `SRC-006`
- Location: lines 770–781; heading `49. bot.toml`
- Domain tags: DEPLOYMENT, EXECUTION, RECORDER, INFRA, ACCOUNTING
- Source statement: 49. bot.toml: Contient : feed settings
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `49. bot.toml` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0045`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RECORDER, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0053 — 50. risk.toml

- Source: `SRC-006`
- Location: lines 782–792; heading `50. risk.toml`
- Domain tags: DEPLOYMENT, RISK, INFRA, INVENTORY, CAPITAL, ROUTING
- Source statement: 50. risk.toml: Contient les paramètres autorisés par la Risk Constitution :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `50. risk.toml` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0046`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, INFRA, INVENTORY, CAPITAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0054 — 51. markets.toml

- Source: `SRC-006`
- Location: lines 793–801; heading `51. markets.toml`
- Domain tags: DEPLOYMENT, RISK
- Source statement: 51. markets.toml: mais metadata exchange reste récupérée dynamiquement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `51. markets.toml` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0047`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0055 — 52. ResolvedConfig

- Source: `SRC-006`
- Location: lines 802–820; heading `52. ResolvedConfig`
- Domain tags: DEPLOYMENT, DETERMINISM
- Source statement: 52. ResolvedConfig: Les fichiers sont : parsed
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `52. ResolvedConfig` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0048`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0056 — 53. Invalid config

- Source: `SRC-006`
- Location: lines 821–834; heading `53. Invalid config`
- Domain tags: DEPLOYMENT, RECOVERY
- Source statement: 53. Invalid config: Le bot ne démarre pas READY.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `53. Invalid config` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0049`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0057 — 54. Config schema version

- Source: `SRC-006`
- Location: lines 835–841; heading `54. Config schema version`
- Domain tags: DEPLOYMENT, DATA
- Source statement: 54. Config schema version: Chaque configuration contient : schema_version
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `54. Config schema version` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0050`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0058 — 55. Config migrations

- Source: `SRC-006`
- Location: lines 842–854; heading `55. Config migrations`
- Domain tags: DEPLOYMENT
- Source statement: 55. Config migrations: Si version ancienne : explicit migration
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `55. Config migrations` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0051`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0059 — 56. Secrets séparés

- Source: `SRC-006`
- Location: lines 855–861; heading `56. Secrets séparés`
- Domain tags: SECURITY
- Source statement: 56. Secrets séparés: Les secrets ne sont pas dans :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `56. Secrets séparés` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0006`; supporting items: none found by conservative heading match; domain indexes `SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0060 — 57. Secret principal

- Source: `SRC-006`
- Location: lines 862–869; heading `57. Secret principal`
- Domain tags: SECURITY, QUANT
- Source statement: 57. Secret principal: ou matériel de signature équivalent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `57. Secret principal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0007`; supporting items: none found by conservative heading match; domain indexes `SECURITY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0061 — 58. Secret mount

- Source: `SRC-006`
- Location: lines 870–882; heading `58. Secret mount`
- Domain tags: SECURITY
- Source statement: 58. Secret mount: Préférer : read-only file
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `58. Secret mount` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0008`; supporting items: none found by conservative heading match; domain indexes `SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0062 — 59. Pourquoi fichier plutôt qu’environnement

- Source: `SRC-006`
- Location: lines 883–897; heading `59. Pourquoi fichier plutôt qu’environnement`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 59. Pourquoi fichier plutôt qu’environnement: Les variables d’environnement peuvent être :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `59. Pourquoi fichier plutôt qu’environnement` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0052`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0063 — 60. Secret permissions host

- Source: `SRC-006`
- Location: lines 898–906; heading `60. Secret permissions host`
- Domain tags: SECURITY, DEPLOYMENT
- Source statement: 60. Secret permissions host: ou utilisateur d’installation dédié selon notre packaging.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `60. Secret permissions host` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0009`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0064 — 61. Secret lifetime

- Source: `SRC-006`
- Location: lines 907–917; heading `61. Secret lifetime`
- Domain tags: SECURITY
- Source statement: 61. Secret lifetime: Le signer charge le secret en mémoire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `61. Secret lifetime` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0010`; supporting items: none found by conservative heading match; domain indexes `SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0065 — 62. Memory handling

- Source: `SRC-006`
- Location: lines 918–925; heading `62. Memory handling`
- Domain tags: DEPLOYMENT
- Source statement: 62. Memory handling: Quand raisonnablement possible : zeroize sensitive buffers
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `62. Memory handling` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0053`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0066 — 63. Secret redaction

- Source: `SRC-006`
- Location: lines 926–933; heading `63. Secret redaction`
- Domain tags: SECURITY, INFRA
- Source statement: 63. Secret redaction: Le logging framework doit traiter certains champs comme :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `63. Secret redaction` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0011`; supporting items: none found by conservative heading match; domain indexes `SECURITY, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0067 — 64. Panic protection

- Source: `SRC-006`
- Location: lines 934–940; heading `64. Panic protection`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 64. Panic protection: Une erreur ne doit jamais afficher : full config including private key
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `64. Panic protection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0054`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0068 — 65. Support bundle

- Source: `SRC-006`
- Location: lines 941–956; heading `65. Support bundle`
- Domain tags: CLIENT, RECORDER, DEPLOYMENT, SECURITY
- Source statement: 65. Support bundle: Lorsqu’un client demande du support : Elle doit automatiquement exclure :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `65. Support bundle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0002`; supporting items: none found by conservative heading match; domain indexes `CLIENT, RECORDER, DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0069 — 66. Support bundle contents

- Source: `SRC-006`
- Location: lines 957–969; heading `66. Support bundle contents`
- Domain tags: CLIENT, DATA, INFRA, OPERATIONS, MICROSTRUCTURE
- Source statement: 66. Support bundle contents: Peut contenir : software version
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `66. Support bundle contents` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0003`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DATA, INFRA, OPERATIONS, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0070 — 67. Private by default

- Source: `SRC-006`
- Location: lines 970–972; heading `67. Private by default`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 67. Private by default: Le support bundle reste local jusqu’à ce que le client choisisse de nous l’envoyer.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `67. Private by default` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0055`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0071 — 68. Persistent volumes

- Source: `SRC-006`
- Location: lines 973–983; heading `68. Persistent volumes`
- Domain tags: DEPLOYMENT, DATA
- Source statement: 68. Persistent volumes: Minimum : state
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `68. Persistent volumes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0056`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0072 — 69. /data/state

- Source: `SRC-006`
- Location: lines 984–992; heading `69. /data/state`
- Domain tags: DEPLOYMENT
- Source statement: 69. /data/state: Contient : checkpoints
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `69. /data/state` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0057`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0073 — 70. /data/journal

- Source: `SRC-006`
- Location: lines 993–1000; heading `70. /data/journal`
- Domain tags: DEPLOYMENT, DATA
- Source statement: 70. /data/journal: Contient : ExecutionJournal
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `70. /data/journal` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0058`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0074 — 71. /data/recorder

- Source: `SRC-006`
- Location: lines 1001–1008; heading `71. /data/recorder`
- Domain tags: DEPLOYMENT, EXECUTION, RECORDER
- Source statement: 71. /data/recorder: Contient : recent RAW market chunks
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `71. /data/recorder` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0059`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0075 — 72. /data/models

- Source: `SRC-006`
- Location: lines 1009–1017; heading `72. /data/models`
- Domain tags: DEPLOYMENT
- Source statement: 72. /data/models: si les modèles ne sont pas embarqués directement dans l’image.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `72. /data/models` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0060`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0076 — 73. Modèles : image ou volume ?

- Source: `SRC-006`
- Location: lines 1018–1019; heading `73. Modèles : image ou volume ?`
- Domain tags: DEPLOYMENT
- Source statement: 73. Modèles : image ou volume ?: Deux options.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `73. Modèles : image ou volume ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0061`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0077 — Stable models

- Source: `SRC-006`
- Location: lines 1020–1026; heading `Stable models`
- Domain tags: DEPLOYMENT
- Source statement: Stable models: Peuvent être intégrés à l’image release. image = complete validated software artifact
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `Stable models` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0062`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0078 — Frequently updated calibrated models

- Source: `SRC-006`
- Location: lines 1027–1034; heading `Frequently updated calibrated models`
- Domain tags: DEPLOYMENT
- Source statement: Frequently updated calibrated models: Peuvent être distribués comme :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `Frequently updated calibrated models` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-DEPLOY-0063`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0079 — 74. Règle modèle

- Source: `SRC-006`
- Location: lines 1035–1044; heading `74. Règle modèle`
- Domain tags: DEPLOYMENT, DATA, DETERMINISM
- Source statement: 74. Règle modèle: Un modèle n’est jamais remplacé en place silencieusement.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `74. Règle modèle` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0064`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0080 — 75. /logs

- Source: `SRC-006`
- Location: lines 1045–1048; heading `75. /logs`
- Domain tags: DEPLOYMENT
- Source statement: 75. /logs: Pas source primaire de reconstruction.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `75. /logs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0065`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0081 — 76. Log rotation

- Source: `SRC-006`
- Location: lines 1049–1057; heading `76. Log rotation`
- Domain tags: DEPLOYMENT
- Source statement: 76. Log rotation: Obligatoire. Sinon :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `76. Log rotation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0066`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0082 — 77. Log levels

- Source: `SRC-006`
- Location: lines 1058–1073; heading `77. Log levels`
- Domain tags: DEPLOYMENT, PRODUCT
- Source statement: 77. Log levels: ERROR DEBUG
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `77. Log levels` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0067`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0083 — 78. Pas de TRACE permanent

- Source: `SRC-006`
- Location: lines 1074–1082; heading `78. Pas de TRACE permanent`
- Domain tags: DEPLOYMENT
- Source statement: 78. Pas de TRACE permanent: Un tracing excessif peut :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `78. Pas de TRACE permanent` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0068`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0084 — 79. Structured logs

- Source: `SRC-006`
- Location: lines 1083–1091; heading `79. Structured logs`
- Domain tags: DEPLOYMENT, DATA
- Source statement: 79. Structured logs: Mais les événements critiques sont stockés séparément dans le journal.
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `79. Structured logs` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0069`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0085 — 80. Disk budget

- Source: `SRC-006`
- Location: lines 1092–1099; heading `80. Disk budget`
- Domain tags: DEPLOYMENT
- Source statement: 80. Disk budget: Le bot connaît : disk_total
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `80. Disk budget` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0070`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0086 — 81. Disk thresholds

- Source: `SRC-006`
- Location: lines 1100–1109; heading `81. Disk thresholds`
- Domain tags: DEPLOYMENT
- Source statement: 81. Disk thresholds: Exemple conceptuel : NORMAL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `81. Disk thresholds` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0071`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0087 — 82. LOW disk

- Source: `SRC-006`
- Location: lines 1110–1119; heading `82. LOW disk`
- Domain tags: DEPLOYMENT, RECORDER, OPERATIONS
- Source statement: 82. LOW disk: Actions : reduce general RAW retention
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `82. LOW disk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0072`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECORDER, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0088 — 83. CRITICAL disk

- Source: `SRC-006`
- Location: lines 1120–1130; heading `83. CRITICAL disk`
- Domain tags: DEPLOYMENT, EXECUTION, RECORDER, DATA
- Source statement: 83. CRITICAL disk: Le Recorder général peut être stoppé.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `83. CRITICAL disk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0073`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RECORDER, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0089 — 84. Jamais supprimer les données critiques au hasard

- Source: `SRC-006`
- Location: lines 1131–1133; heading `84. Jamais supprimer les données critiques au hasard`
- Domain tags: DEPLOYMENT, RECORDER
- Source statement: 84. Jamais supprimer les données critiques au hasard: Retention classes définies dans le Dossier 4.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `84. Jamais supprimer les données critiques au hasard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0074`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0090 — 85. Backup

- Source: `SRC-006`
- Location: lines 1134–1143; heading `85. Backup`
- Domain tags: OPERATIONS, DATA, CLIENT
- Source statement: 85. Backup: Le client doit pouvoir sauvegarder :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `85. Backup` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0006`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, DATA, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0091 — 86. Pas besoin de sauvegarder l’image

- Source: `SRC-006`
- Location: lines 1144–1146; heading `86. Pas besoin de sauvegarder l’image`
- Domain tags: DEPLOYMENT
- Source statement: 86. Pas besoin de sauvegarder l’image: L’image est récupérable depuis le registry par digest.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `86. Pas besoin de sauvegarder l’image` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0075`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0092 — 87. Backup secret

- Source: `SRC-006`
- Location: lines 1147–1155; heading `87. Backup secret`
- Domain tags: SECURITY, OPERATIONS
- Source statement: 87. Backup secret: Les secrets nécessitent une politique distincte. On ne doit pas automatiquement copier :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `87. Backup secret` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0012`; supporting items: none found by conservative heading match; domain indexes `SECURITY, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0093 — 88. Recovery kit

- Source: `SRC-006`
- Location: lines 1156–1166; heading `88. Recovery kit`
- Domain tags: DEPLOYMENT, RECOVERY, INFRA, SECURITY, CLIENT
- Source statement: 88. Recovery kit: Le client doit idéalement disposer d’un moyen documenté de restaurer : tout en gérant ses secrets séparément.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `88. Recovery kit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0076`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECOVERY, INFRA, SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0094 — 89. Backup consistency

- Source: `SRC-006`
- Location: lines 1167–1174; heading `89. Backup consistency`
- Domain tags: OPERATIONS
- Source statement: 89. Backup consistency: Un backup state doit être : ou issu d’un checkpoint cohérent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `89. Backup consistency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0007`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0095 — 90. Restart contract

- Source: `SRC-006`
- Location: lines 1175–1187; heading `90. Restart contract`
- Domain tags: OPERATIONS, RECONCILIATION, DEPLOYMENT
- Source statement: 90. Restart contract: Le redémarrage d’un container suit toujours :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `90. Restart contract` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0008`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, RECONCILIATION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0096 — 91. Docker restart policy

- Source: `SRC-006`
- Location: lines 1188–1198; heading `91. Docker restart policy`
- Domain tags: DEPLOYMENT, OPERATIONS, RECONCILIATION
- Source statement: 91. Docker restart policy: restart automatique du processus ≠ reprise automatique du trading. La state machine impose reconciliation avant READY.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `91. Docker restart policy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0077`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, OPERATIONS, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0097 — 92. Healthcheck Docker

- Source: `SRC-006`
- Location: lines 1199–1206; heading `92. Healthcheck Docker`
- Domain tags: DEPLOYMENT, OPERATIONS
- Source statement: 92. Healthcheck Docker: Le container expose plusieurs états. Ne pas réduire à :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `92. Healthcheck Docker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0078`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0098 — 93. Liveness

- Source: `SRC-006`
- Location: lines 1207–1215; heading `93. Liveness`
- Domain tags: OPERATIONS
- Source statement: 93. Liveness: Question : le processus fonctionne-t-il ?
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `93. Liveness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0009`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0099 — 94. Readiness

- Source: `SRC-006`
- Location: lines 1216–1228; heading `94. Readiness`
- Domain tags: OPERATIONS
- Source statement: 94. Readiness: le bot peut-il prendre du nouveau risque ? Retour OK uniquement si :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `94. Readiness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0010`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0100 — 95. Trading health

- Source: `SRC-006`
- Location: lines 1229–1238; heading `95. Trading health`
- Domain tags: OPERATIONS, RECOVERY
- Source statement: 95. Trading health: Peut exposer : READY
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `95. Trading health` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0011`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0101 — 96. Docker healthcheck ne doit pas provoquer une boucle dangereuse

- Source: `SRC-006`
- Location: lines 1239–1247; heading `96. Docker healthcheck ne doit pas provoquer une boucle dangereuse`
- Domain tags: DEPLOYMENT, OPERATIONS, RECOVERY, ARCH
- Source statement: 96. Docker healthcheck ne doit pas provoquer une boucle dangereuse: le process est encore très utile. Docker ne doit pas forcément le tuer/restart parce qu’il n’est pas READY.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `96. Docker healthcheck ne doit pas provoquer une boucle dangereuse` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0079`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, OPERATIONS, RECOVERY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0102 — 97. Donc liveness ≠ readiness

- Source: `SRC-006`
- Location: lines 1248–1251; heading `97. Donc liveness ≠ readiness`
- Domain tags: OPERATIONS, RECOVERY
- Source statement: 97. Donc liveness ≠ readiness: Un bot en recovery doit rester vivant.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `97. Donc liveness ≠ readiness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0012`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0103 — 98. Metrics endpoint

- Source: `SRC-006`
- Location: lines 1252–1259; heading `98. Metrics endpoint`
- Domain tags: DEPLOYMENT
- Source statement: 98. Metrics endpoint: Peut exposer localement : Prometheus-compatible metrics
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `98. Metrics endpoint` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0080`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0104 — 99. Metrics listener

- Source: `SRC-006`
- Location: lines 1260–1268; heading `99. Metrics listener`
- Domain tags: DEPLOYMENT
- Source statement: 99. Metrics listener: Par défaut : localhost only
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `99. Metrics listener` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0081`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0105 — 100. Admin API

- Source: `SRC-006`
- Location: lines 1269–1284; heading `100. Admin API`
- Domain tags: DEPLOYMENT, RISK, ARCH
- Source statement: 100. Admin API: Si nous créons une interface de contrôle :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `100. Admin API` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0082`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0106 — 101. Pas de panneau admin public

- Source: `SRC-006`
- Location: lines 1285–1292; heading `101. Pas de panneau admin public`
- Domain tags: DEPLOYMENT
- Source statement: 101. Pas de panneau admin public: Aucun : 0.0.0.0:8080
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `101. Pas de panneau admin public` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0083`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0107 — 102. Remote dashboard futur

- Source: `SRC-006`
- Location: lines 1293–1306; heading `102. Remote dashboard futur`
- Domain tags: DEPLOYMENT, INFRA
- Source statement: 102. Remote dashboard futur: du bot vers un service central. sur chaque VPS par défaut.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `102. Remote dashboard futur` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `OPEN`
- Cross-source references: `REQ-DEPLOY-0084`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0108 — 103. Firewall VPS

- Source: `SRC-006`
- Location: lines 1307–1315; heading `103. Firewall VPS`
- Domain tags: SECURITY, INFRA
- Source statement: 103. Firewall VPS: Pas besoin d’exposer le bot au monde.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `103. Firewall VPS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0013`; supporting items: none found by conservative heading match; domain indexes `SECURITY, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0109 — 104. SSH

- Source: `SRC-006`
- Location: lines 1316–1325; heading `104. SSH`
- Domain tags: DEPLOYMENT
- Source statement: 104. SSH: pour les installations que nous gérons/documentons.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `104. SSH` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0085`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0110 — 105. Client responsibility

- Source: `SRC-006`
- Location: lines 1326–1335; heading `105. Client responsibility`
- Domain tags: CLIENT, INFRA, DEPLOYMENT, SECURITY
- Source statement: 105. Client responsibility: Le VPS appartient au client.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `105. Client responsibility` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0004`; supporting items: none found by conservative heading match; domain indexes `CLIENT, INFRA, DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0111 — 106. Installer

- Source: `SRC-006`
- Location: lines 1336–1347; heading `106. Installer`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 106. Installer: Je recommande de fournir un petit :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `106. Installer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0086`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0112 — 107. Ce que fait l’installer

- Source: `SRC-006`
- Location: lines 1348–1366; heading `107. Ce que fait l’installer`
- Domain tags: DEPLOYMENT, CLOCK, INFRA, ARCH
- Source statement: 107. Ce que fait l’installer: check OS check architecture
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `107. Ce que fait l’installer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0087`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLOCK, INFRA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0113 — 108. Ce que l’installer ne fait jamais

- Source: `SRC-006`
- Location: lines 1367–1375; heading `108. Ce que l’installer ne fait jamais`
- Domain tags: DEPLOYMENT, SECURITY, CLIENT
- Source statement: 108. Ce que l’installer ne fait jamais: generate client private key without clear process modify random host security settings silently
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `108. Ce que l’installer ne fait jamais` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0088`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0114 — 109. First boot wizard

- Source: `SRC-006`
- Location: lines 1376–1382; heading `109. First boot wizard`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 109. First boot wizard: Possible : botctl configure
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `109. First boot wizard` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0089`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0115 — 110. Configuration steps

- Source: `SRC-006`
- Location: lines 1383–1395; heading `110. Configuration steps`
- Domain tags: DEPLOYMENT, RISK, INFRA, BENCHMARK, VALIDATION, MICROSTRUCTURE, GRAPH
- Source statement: 110. Configuration steps: 1. select mode 2. select account
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `110. Configuration steps` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0090`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, INFRA, BENCHMARK, VALIDATION, MICROSTRUCTURE, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0116 — 111. Pas de Live immédiat pour nouveau client

- Source: `SRC-006`
- Location: lines 1396–1410; heading `111. Pas de Live immédiat pour nouveau client`
- Domain tags: CLIENT, DEPLOYMENT, VALIDATION
- Source statement: 111. Pas de Live immédiat pour nouveau client: Le chemin recommandé : INSTALL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `111. Pas de Live immédiat pour nouveau client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0005`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0117 — 112. Client onboarding gate

- Source: `SRC-006`
- Location: lines 1411–1421; heading `112. Client onboarding gate`
- Domain tags: CLIENT, RECONCILIATION, RISK, INFRA, SECURITY, VALIDATION, MICROSTRUCTURE
- Source statement: 112. Client onboarding gate: Le logiciel peut imposer :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `112. Client onboarding gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0006`; supporting items: none found by conservative heading match; domain indexes `CLIENT, RECONCILIATION, RISK, INFRA, SECURITY, VALIDATION, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0118 — 113. Infra diagnostic intégré

- Source: `SRC-006`
- Location: lines 1422–1428; heading `113. Infra diagnostic intégré`
- Domain tags: DEPLOYMENT, INFRA, BENCHMARK, CLIENT
- Source statement: 113. Infra diagnostic intégré: Commande : botctl benchmark
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `113. Infra diagnostic intégré` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0091`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, BENCHMARK, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0119 — 114. Tests diagnostic

- Source: `SRC-006`
- Location: lines 1429–1441; heading `114. Tests diagnostic`
- Domain tags: DEPLOYMENT, CLOCK, INFRA, BENCHMARK, ACCOUNTING, MICROSTRUCTURE
- Source statement: 114. Tests diagnostic: scheduler jitter memory
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `114. Tests diagnostic` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0092`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLOCK, INFRA, BENCHMARK, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0120 — 115. Output

- Source: `SRC-006`
- Location: lines 1442–1456; heading `115. Output`
- Domain tags: DEPLOYMENT, CLOCK, INFRA, MICROSTRUCTURE
- Source statement: 115. Output: INFRA PROFILE CPU GOOD
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `115. Output` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0093`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLOCK, INFRA, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0121 — 116. Unsupported infrastructure

- Source: `SRC-006`
- Location: lines 1457–1477; heading `116. Unsupported infrastructure`
- Domain tags: DEPLOYMENT, INFRA, CLOCK, VALIDATION, REPLAY
- Source statement: 116. Unsupported infrastructure: Si : RAM too low
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `116. Unsupported infrastructure` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0094`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, CLOCK, VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0122 — 117. Provider independence

- Source: `SRC-006`
- Location: lines 1478–1489; heading `117. Provider independence`
- Domain tags: DEPLOYMENT, INFRA
- Source statement: 117. Provider independence: L’image ne contient jamais :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `117. Provider independence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0095`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0123 — 118. Provider profile

- Source: `SRC-006`
- Location: lines 1490–1498; heading `118. Provider profile`
- Domain tags: DEPLOYMENT, INFRA, MICROSTRUCTURE, BENCHMARK
- Source statement: 118. Provider profile: On peut néanmoins enregistrer : Pas pour modifier la stratégie arbitrairement.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `118. Provider profile` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0096`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, MICROSTRUCTURE, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0124 — 119. VPS standard minimum

- Source: `SRC-006`
- Location: lines 1499–1509; heading `119. VPS standard minimum`
- Domain tags: DEPLOYMENT, INFRA, BENCHMARK
- Source statement: 119. VPS standard minimum: Les valeurs finales viendront de nos benchmarks.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `119. VPS standard minimum` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0097`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0125 — 120. Recommended profile

- Source: `SRC-006`
- Location: lines 1510–1519; heading `120. Recommended profile`
- Domain tags: DEPLOYMENT, MICROSTRUCTURE, INFRA, BENCHMARK, QUANT
- Source statement: 120. Recommended profile: mais non figé avant benchmark.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `120. Recommended profile` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0098`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, MICROSTRUCTURE, INFRA, BENCHMARK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0126 — 121. Performance profile

- Source: `SRC-006`
- Location: lines 1520–1529; heading `121. Performance profile`
- Domain tags: DEPLOYMENT, BENCHMARK, MICROSTRUCTURE, INFRA, QUANT
- Source statement: 121. Performance profile: Probablement : 4 dedicated/high-frequency vCPU
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `121. Performance profile` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0099`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK, MICROSTRUCTURE, INFRA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0127 — 122. Pas de VPS premium obligatoire

- Source: `SRC-006`
- Location: lines 1530–1540; heading `122. Pas de VPS premium obligatoire`
- Domain tags: DEPLOYMENT, INFRA, CLIENT, ACCOUNTING
- Source statement: 122. Pas de VPS premium obligatoire: Le client commence avec le niveau qui maximise :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `122. Pas de VPS premium obligatoire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0100`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, CLIENT, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0128 — 123. Infra ROI client

- Source: `SRC-006`
- Location: lines 1541–1557; heading `123. Infra ROI client`
- Domain tags: CLIENT, INFRA, EXECUTION, BENCHMARK, ACCOUNTING
- Source statement: 123. Infra ROI client: Le bot peut calculer :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `123. Infra ROI client` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0007`; supporting items: none found by conservative heading match; domain indexes `CLIENT, INFRA, EXECUTION, BENCHMARK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0129 — 124. Jamais upgrade automatique du VPS

- Source: `SRC-006`
- Location: lines 1558–1561; heading `124. Jamais upgrade automatique du VPS`
- Domain tags: DEPLOYMENT, INFRA, CLIENT
- Source statement: 124. Jamais upgrade automatique du VPS: Le bot recommande. Le client décide.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `124. Jamais upgrade automatique du VPS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0101`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0130 — 125. Distribution aux 30–50 clients

- Source: `SRC-006`
- Location: lines 1562–1573; heading `125. Distribution aux 30–50 clients`
- Domain tags: CLIENT, PRODUCT, DEPLOYMENT, LICENSE, ARCH
- Source statement: 125. Distribution aux 30–50 clients: Pas besoin de plateforme SaaS lourde.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `125. Distribution aux 30–50 clients` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0008`; supporting items: none found by conservative heading match; domain indexes `CLIENT, PRODUCT, DEPLOYMENT, LICENSE, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0131 — 126. Licence

- Source: `SRC-006`
- Location: lines 1574–1581; heading `126. Licence`
- Domain tags: LICENSE, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 126. Licence: Une licence doit contrôler : mais ne doit pas être dans le hot path.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `126. Licence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0001`; supporting items: none found by conservative heading match; domain indexes `LICENSE, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0132 — 127. Interdit

- Source: `SRC-006`
- Location: lines 1582–1588; heading `127. Interdit`
- Domain tags: DEPLOYMENT, LICENSE
- Source statement: 127. Interdit: before every trade: call license.mycompany.com
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `127. Interdit` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0102`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0133 — 128. Pourquoi

- Source: `SRC-006`
- Location: lines 1589–1596; heading `128. Pourquoi`
- Domain tags: DEPLOYMENT, RISK, CLIENT
- Source statement: 128. Pourquoi: Si notre serveur tombe : client cannot manage existing risk
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `128. Pourquoi` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0103`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0134 — 129. Licence startup

- Source: `SRC-006`
- Location: lines 1597–1608; heading `129. Licence startup`
- Domain tags: LICENSE, VALIDATION
- Source statement: 129. Licence startup: Possible : startup validation
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `129. Licence startup` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0002`; supporting items: none found by conservative heading match; domain indexes `LICENSE, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0135 — 130. Signed entitlement

- Source: `SRC-006`
- Location: lines 1609–1619; heading `130. Signed entitlement`
- Domain tags: LICENSE, DEPLOYMENT
- Source statement: 130. Signed entitlement: Concept : license_id
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `130. Signed entitlement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0003`; supporting items: none found by conservative heading match; domain indexes `LICENSE, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0136 — 131. Le bot vérifie localement

- Source: `SRC-006`
- Location: lines 1620–1627; heading `131. Le bot vérifie localement`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 131. Le bot vérifie localement: et non un secret central embarqué.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `131. Le bot vérifie localement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0104`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0137 — 132. Grace period

- Source: `SRC-006`
- Location: lines 1628–1635; heading `132. Grace period`
- Domain tags: DEPLOYMENT, LICENSE, GRAPH
- Source statement: 132. Grace period: Si licence nécessite renouvellement en ligne : ne doit pas immédiatement couper le moteur.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `132. Grace period` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0105`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, LICENSE, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0138 — 133. Expiration et trading actif

- Source: `SRC-006`
- Location: lines 1636–1646; heading `133. Expiration et trading actif`
- Domain tags: DEPLOYMENT, EXECUTION, RECOVERY, RECONCILIATION, RISK, LICENSE
- Source statement: 133. Expiration et trading actif: le bot ne doit jamais abandonner une exposition active. CANCEL / RECOVERY / RECONCILIATION remain enabled
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `133. Expiration et trading actif` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0106`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RECOVERY, RECONCILIATION, RISK, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0139 — 134. Principe commercial important

- Source: `SRC-006`
- Location: lines 1647–1658; heading `134. Principe commercial important`
- Domain tags: DEPLOYMENT, PRODUCT, RISK, LICENSE
- Source statement: 134. Principe commercial important: La licence peut contrôler :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `134. Principe commercial important` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0107`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, PRODUCT, RISK, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0140 — 135. Pas de remote kill dangereux

- Source: `SRC-006`
- Location: lines 1659–1666; heading `135. Pas de remote kill dangereux`
- Domain tags: DEPLOYMENT, RISK, EXECUTION
- Source statement: 135. Pas de remote kill dangereux: Même si nous disposons d’un mécanisme de révocation : ne doit pas brutalement tuer le processus avec maker orders ouverts.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `135. Pas de remote kill dangereux` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0108`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0141 — 136. Révocation

- Source: `SRC-006`
- Location: lines 1667–1679; heading `136. Révocation`
- Domain tags: DEPLOYMENT, RECOVERY, RISK
- Source statement: 136. Révocation: Doit produire : RECOVERY_ONLY
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `136. Révocation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0109`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0142 — 137. Installation binding

- Source: `SRC-006`
- Location: lines 1680–1687; heading `137. Installation binding`
- Domain tags: DEPLOYMENT, RISK, LICENSE
- Source statement: 137. Installation binding: Pour limiter le partage sauvage de licence :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `137. Installation binding` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0110`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0143 — 138. Ne pas binder trop fortement au hardware

- Source: `SRC-006`
- Location: lines 1688–1697; heading `138. Ne pas binder trop fortement au hardware`
- Domain tags: DEPLOYMENT, INFRA, LICENSE, CLIENT
- Source statement: 138. Ne pas binder trop fortement au hardware: Un VPS peut être : Le client doit pouvoir transférer sa licence proprement.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `138. Ne pas binder trop fortement au hardware` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0111`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, LICENSE, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0144 — 139. Licence ≠ clé client

- Source: `SRC-006`
- Location: lines 1698–1704; heading `139. Licence ≠ clé client`
- Domain tags: LICENSE, CLIENT
- Source statement: 139. Licence ≠ clé client: Notre système de licence ne reçoit jamais :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `139. Licence ≠ clé client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0004`; supporting items: none found by conservative heading match; domain indexes `LICENSE, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0145 — 140. Telemetry

- Source: `SRC-006`
- Location: lines 1705–1712; heading `140. Telemetry`
- Domain tags: DEPLOYMENT
- Source statement: 140. Telemetry: Par défaut : minimal / opt-in
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `140. Telemetry` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0112`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0146 — 141. Données potentiellement utiles

- Source: `SRC-006`
- Location: lines 1713–1722; heading `141. Données potentiellement utiles`
- Domain tags: DEPLOYMENT, BENCHMARK, OPERATIONS
- Source statement: 141. Données potentiellement utiles: software version health
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `141. Données potentiellement utiles` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0113`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0147 — 142. Pas besoin d’envoyer

- Source: `SRC-006`
- Location: lines 1723–1732; heading `142. Pas besoin d’envoyer`
- Domain tags: DEPLOYMENT, SECURITY, LICENSE, INVENTORY
- Source statement: 142. Pas besoin d’envoyer: wallet private key raw orders
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `142. Pas besoin d’envoyer` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0114`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY, LICENSE, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0148 — 143. Update channels

- Source: `SRC-006`
- Location: lines 1733–1741; heading `143. Update channels`
- Domain tags: DEPLOYMENT
- Source statement: 143. Update channels: Je recommande : STABLE
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `143. Update channels` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0115`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0149 — 144. Stable

- Source: `SRC-006`
- Location: lines 1742–1744; heading `144. Stable`
- Domain tags: DEPLOYMENT, CLIENT, PRODUCT
- Source statement: 144. Stable: Clients production.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `144. Stable` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0116`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0150 — 145. Candidate

- Source: `SRC-006`
- Location: lines 1745–1747; heading `145. Candidate`
- Domain tags: DEPLOYMENT
- Source statement: 145. Candidate: Notre installation interne et quelques testeurs volontaires.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `145. Candidate` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0117`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0151 — 146. Development

- Source: `SRC-006`
- Location: lines 1748–1750; heading `146. Development`
- Domain tags: DEPLOYMENT, CAPITAL
- Source statement: 146. Development: Jamais pour capital réel standard.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `146. Development` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0118`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0152 — 147. Release process

- Source: `SRC-006`
- Location: lines 1751–1774; heading `147. Release process`
- Domain tags: DEPLOYMENT, BENCHMARK, VALIDATION, REPLAY
- Source statement: 147. Release process: UNIT TEST INTEGRATION TEST
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `147. Release process` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0119`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK, VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0153 — 148. Pas de release directe main → clients

- Source: `SRC-006`
- Location: lines 1775–1777; heading `148. Pas de release directe main → clients`
- Domain tags: CLIENT, VALIDATION
- Source statement: 148. Pas de release directe main → clients: Toute version passe la validation.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `148. Pas de release directe main → clients` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0009`; supporting items: none found by conservative heading match; domain indexes `CLIENT, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0154 — 149. Canary deployment

- Source: `SRC-006`
- Location: lines 1778–1788; heading `149. Canary deployment`
- Domain tags: DEPLOYMENT, INFRA, CLIENT, VALIDATION
- Source statement: 149. Canary deployment: 4. éventuellement 1–3 clients volontaires
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `149. Canary deployment` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0120`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, CLIENT, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0155 — 150. Client updates

- Source: `SRC-006`
- Location: lines 1789–1796; heading `150. Client updates`
- Domain tags: CLIENT, DEPLOYMENT, OPERATIONS
- Source statement: 150. Client updates: Jamais : automatic pull + restart
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `150. Client updates` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0010`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0156 — 151. Safe Update State

- Source: `SRC-006`
- Location: lines 1797–1815; heading `151. Safe Update State`
- Domain tags: DEPLOYMENT, RECOVERY, RECONCILIATION, RISK
- Source statement: 151. Safe Update State: Une update normale nécessite :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `151. Safe Update State` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0121`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECOVERY, RECONCILIATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0157 — 152. Update sequence

- Source: `SRC-006`
- Location: lines 1816–1832; heading `152. Update sequence`
- Domain tags: DEPLOYMENT, RECONCILIATION, RISK, VALIDATION, OPERATIONS
- Source statement: 152. Update sequence: 1. download new image 2. verify digest/signature
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `152. Update sequence` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0122`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION, RISK, VALIDATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0158 — 153. Blue/green ?

- Source: `SRC-006`
- Location: lines 1833–1844; heading `153. Blue/green ?`
- Domain tags: DEPLOYMENT, EXECUTION, CLIENT, OPERATIONS
- Source statement: 153. Blue/green ?: Pour 30–50 clients, inutile au départ pour le moteur de trading. Avoir deux bots connectés au même compte peut créer :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `153. Blue/green ?` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0123`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, CLIENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0159 — 154. No dual-active update

- Source: `SRC-006`
- Location: lines 1845–1854; heading `154. No dual-active update`
- Domain tags: DEPLOYMENT, SECURITY, PRODUCT, FUTURE
- Source statement: 154. No dual-active update: simultanément sur le même signer/account.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `154. No dual-active update` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0124`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY, PRODUCT, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0160 — 155. Pre-start validation container

- Source: `SRC-006`
- Location: lines 1855–1870; heading `155. Pre-start validation container`
- Domain tags: DEPLOYMENT, VALIDATION, DATA
- Source statement: 155. Pre-start validation container: Nouvelle image peut être lancée en : sans trading pour vérifier :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `155. Pre-start validation container` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0125`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, VALIDATION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0161 — 156. Rollback

- Source: `SRC-006`
- Location: lines 1871–1877; heading `156. Rollback`
- Domain tags: DEPLOYMENT
- Source statement: 156. Rollback: Chaque update conserve : previous known-good digest
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `156. Rollback` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0126`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0162 — 157. Rollback sequence

- Source: `SRC-006`
- Location: lines 1878–1888; heading `157. Rollback sequence`
- Domain tags: DEPLOYMENT, RECONCILIATION, RISK
- Source statement: 157. Rollback sequence: stop new risk reconcile
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `157. Rollback sequence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0127`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0163 — 158. Pas de rollback de state aveugle

- Source: `SRC-006`
- Location: lines 1889–1892; heading `158. Pas de rollback de state aveugle`
- Domain tags: DEPLOYMENT
- Source statement: 158. Pas de rollback de state aveugle: On ne restaure jamais un vieux checkpoint comme s’il représentait la réalité actuelle. L’exchange reste source de vérité.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `158. Pas de rollback de state aveugle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0128`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0164 — 159. Backward-compatible storage

- Source: `SRC-006`
- Location: lines 1893–1905; heading `159. Backward-compatible storage`
- Domain tags: DEPLOYMENT
- Source statement: 159. Backward-compatible storage: Idéalement la nouvelle version écrit un state lisible par :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `159. Backward-compatible storage` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0129`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0165 — 160. Destructive migration

- Source: `SRC-006`
- Location: lines 1906–1914; heading `160. Destructive migration`
- Domain tags: DEPLOYMENT, OPERATIONS
- Source statement: 160. Destructive migration: Une migration destructive exige :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `160. Destructive migration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0130`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0166 — 161. Database

- Source: `SRC-006`
- Location: lines 1915–1917; heading `161. Database`
- Domain tags: DEPLOYMENT
- Source statement: 161. Database: Je n’introduirais pas nécessairement PostgreSQL au départ.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `161. Database` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0131`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0167 — 162. State persistence

- Source: `SRC-006`
- Location: lines 1918–1927; heading `162. State persistence`
- Domain tags: DEPLOYMENT, DATA, BENCHMARK
- Source statement: 162. State persistence: Peut être construit avec :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `162. State persistence` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0132`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0168 — 163. Embedded database candidate

- Source: `SRC-006`
- Location: lines 1928–1938; heading `163. Embedded database candidate`
- Domain tags: DEPLOYMENT
- Source statement: 163. Embedded database candidate: mais choix par besoin réel.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `163. Embedded database candidate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0133`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0169 — 164. Hot path rule

- Source: `SRC-006`
- Location: lines 1939–1945; heading `164. Hot path rule`
- Domain tags: DEPLOYMENT, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 164. Hot path rule: Quelle que soit la persistence : no blocking DB query in hot decision path
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `164. Hot path rule` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0134`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0170 — 165. Config hot reload

- Source: `SRC-006`
- Location: lines 1946–1953; heading `165. Config hot reload`
- Domain tags: DEPLOYMENT, HOT_WARM_COLD, RISK
- Source statement: 165. Config hot reload: Possible pour : logging
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `165. Config hot reload` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0135`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, HOT_WARM_COLD, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0171 — 166. Risk config reload

- Source: `SRC-006`
- Location: lines 1954–1962; heading `166. Risk config reload`
- Domain tags: DEPLOYMENT, RISK
- Source statement: 166. Risk config reload: Doit être : validated
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `166. Risk config reload` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0136`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0172 — 167. Software update ≠ config update

- Source: `SRC-006`
- Location: lines 1963–1965; heading `167. Software update ≠ config update`
- Domain tags: DEPLOYMENT
- Source statement: 167. Software update ≠ config update: Les deux workflows sont séparés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `167. Software update ≠ config update` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0137`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0173 — 168. Model update

- Source: `SRC-006`
- Location: lines 1966–1968; heading `168. Model update`
- Domain tags: DEPLOYMENT
- Source statement: 168. Model update: Également séparé.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `168. Model update` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0138`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0174 — 169. Model rollout

- Source: `SRC-006`
- Location: lines 1969–1980; heading `169. Model rollout`
- Domain tags: DEPLOYMENT, DETERMINISM, FUTURE
- Source statement: 169. Model rollout: download verify hash/signature
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `169. Model rollout` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0139`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DETERMINISM, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0175 — 170. Pas de remplacer Champion à chaud sans validation

- Source: `SRC-006`
- Location: lines 1981–1987; heading `170. Pas de remplacer Champion à chaud sans validation`
- Domain tags: DEPLOYMENT, VALIDATION
- Source statement: 170. Pas de remplacer Champion à chaud sans validation: Sauf urgence où on revient vers :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `170. Pas de remplacer Champion à chaud sans validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0140`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0176 — 171. Crash handling

- Source: `SRC-006`
- Location: lines 1988–1995; heading `171. Crash handling`
- Domain tags: OPERATIONS, RECONCILIATION, DEPLOYMENT
- Source statement: 171. Crash handling: Docker peut redémarrer le process.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `171. Crash handling` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0013`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, RECONCILIATION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0177 — 172. Crash loop

- Source: `SRC-006`
- Location: lines 1996–2009; heading `172. Crash loop`
- Domain tags: OPERATIONS
- Source statement: 172. Crash loop: N crashes in window W ne pas redémarrer éternellement en essayant de trader.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `172. Crash loop` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0014`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0178 — 173. Core dump

- Source: `SRC-006`
- Location: lines 2010–2017; heading `173. Core dump`
- Domain tags: DEPLOYMENT, ARCH, SECURITY, PRODUCT
- Source statement: 173. Core dump: Si activé pour debug : Donc production doit traiter les core dumps avec précaution ou les désactiver.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `173. Core dump` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0141`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ARCH, SECURITY, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0179 — 174. Panic logs

- Source: `SRC-006`
- Location: lines 2018–2020; heading `174. Panic logs`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 174. Panic logs: Secrets redacted.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `174. Panic logs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0142`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0180 — 175. Signal handling

- Source: `SRC-006`
- Location: lines 2021–2029; heading `175. Signal handling`
- Domain tags: DEPLOYMENT
- Source statement: 175. Signal handling: Le process gère : SIGTERM
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `175. Signal handling` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0143`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0181 — 176. Graceful shutdown

- Source: `SRC-006`
- Location: lines 2030–2043; heading `176. Graceful shutdown`
- Domain tags: DEPLOYMENT, EXECUTION, RISK
- Source statement: 176. Graceful shutdown: receive SIGTERM new risk off
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `176. Graceful shutdown` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0144`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0182 — 177. Docker stop timeout

- Source: `SRC-006`
- Location: lines 2044–2047; heading `177. Docker stop timeout`
- Domain tags: DEPLOYMENT
- Source statement: 177. Docker stop timeout: Doit être suffisamment long pour permettre la fermeture propre. Mais pas considéré comme garantie absolue.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `177. Docker stop timeout` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0145`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0183 — 178. SIGKILL

- Source: `SRC-006`
- Location: lines 2048–2062; heading `178. SIGKILL`
- Domain tags: DEPLOYMENT, RISK, RECONCILIATION, INFRA, OPERATIONS
- Source statement: 178. SIGKILL: Le système doit survivre conceptuellement à :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `178. SIGKILL` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0146`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, RECONCILIATION, INFRA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0184 — 179. Host reboot

- Source: `SRC-006`
- Location: lines 2063–2073; heading `179. Host reboot`
- Domain tags: DEPLOYMENT, RECONCILIATION
- Source statement: 179. Host reboot: Même logique : Docker auto-start
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `179. Host reboot` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0147`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0185 — 180. VPS replacement

- Source: `SRC-006`
- Location: lines 2074–2085; heading `180. VPS replacement`
- Domain tags: DEPLOYMENT, INFRA, RECONCILIATION, SECURITY, CLIENT
- Source statement: 180. VPS replacement: Le client doit pouvoir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `180. VPS replacement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0148`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, RECONCILIATION, SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0186 — 181. Migration VPS

- Source: `SRC-006`
- Location: lines 2086–2101; heading `181. Migration VPS`
- Domain tags: DEPLOYMENT, INFRA, EXECUTION, RECONCILIATION, RISK
- Source statement: 181. Migration VPS: Pour éviter deux writers :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `181. Migration VPS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0149`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, EXECUTION, RECONCILIATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0187 — 182. No overlap

- Source: `SRC-006`
- Location: lines 2102–2110; heading `182. No overlap`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 182. No overlap: Ne jamais lancer deux instances live avec :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `182. No overlap` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0150`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0188 — 183. Instance lock

- Source: `SRC-006`
- Location: lines 2111–2118; heading `183. Instance lock`
- Domain tags: DEPLOYMENT
- Source statement: 183. Instance lock: Le logiciel peut stocker un local : pour éviter deux containers sur le même host.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `183. Instance lock` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0151`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0189 — 184. Exchange-side protection

- Source: `SRC-006`
- Location: lines 2119–2126; heading `184. Exchange-side protection`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 184. Exchange-side protection: À terme, un mécanisme supplémentaire peut tenter de détecter : si les données le permettent.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `184. Exchange-side protection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0152`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0190 — 185. Nonce isolation

- Source: `SRC-006`
- Location: lines 2127–2134; heading `185. Nonce isolation`
- Domain tags: DEPLOYMENT, EXECUTION, SECURITY
- Source statement: 185. Nonce isolation: Chaque processus live : one API wallet/signer
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `185. Nonce isolation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0153`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0191 — 186. Client clones

- Source: `SRC-006`
- Location: lines 2135–2144; heading `186. Client clones`
- Domain tags: CLIENT, DEPLOYMENT, CAPITAL
- Source statement: 186. Client clones: Une image copiée sans configuration ne contient : Donc elle n’est pas immédiatement exploitable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `186. Client clones` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0011`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0192 — 187. Network egress

- Source: `SRC-006`
- Location: lines 2145–2154; heading `187. Network egress`
- Domain tags: DEPLOYMENT, LICENSE
- Source statement: 187. Network egress: Le bot doit documenter ses destinations nécessaires :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `187. Network egress` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0154`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0193 — 188. Trading independence

- Source: `SRC-006`
- Location: lines 2155–2168; heading `188. Trading independence`
- Domain tags: DEPLOYMENT, RISK, LICENSE
- Source statement: 188. Trading independence: le bot déjà autorisé doit pouvoir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `188. Trading independence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0155`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0194 — 189. Update independence

- Source: `SRC-006`
- Location: lines 2169–2180; heading `189. Update independence`
- Domain tags: DEPLOYMENT
- Source statement: 189. Update independence: Une panne du registry :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `189. Update independence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0156`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0195 — 190. Local dashboard éventuel

- Source: `SRC-006`
- Location: lines 2181–2188; heading `190. Local dashboard éventuel`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 190. Local dashboard éventuel: Peut être un outil séparé : plutôt qu’un gros dashboard web.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `190. Local dashboard éventuel` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0157`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0196 — 191. CLI botctl

- Source: `SRC-006`
- Location: lines 2189–2206; heading `191. CLI botctl`
- Domain tags: CLIENT, RECONCILIATION, BENCHMARK, DEPLOYMENT, OPERATIONS
- Source statement: 191. CLI botctl: Je recommande réellement cet outil.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `191. CLI botctl` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0012`; supporting items: none found by conservative heading match; domain indexes `CLIENT, RECONCILIATION, BENCHMARK, DEPLOYMENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0197 — 192. Pourquoi CLI

- Source: `SRC-006`
- Location: lines 2207–2216; heading `192. Pourquoi CLI`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 192. Pourquoi CLI: et bien moins complexe qu’un control plane SaaS.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `192. Pourquoi CLI` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0158`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0198 — 193. botctl status

- Source: `SRC-006`
- Location: lines 2217–2230; heading `193. botctl status`
- Domain tags: CLIENT, RECONCILIATION, RISK, INFRA, DEPLOYMENT, OPERATIONS
- Source statement: 193. botctl status: Retour : EngineState
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `193. botctl status` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0013`; supporting items: none found by conservative heading match; domain indexes `CLIENT, RECONCILIATION, RISK, INFRA, DEPLOYMENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0199 — 194. botctl health

- Source: `SRC-006`
- Location: lines 2231–2233; heading `194. botctl health`
- Domain tags: CLIENT, OPERATIONS, RISK
- Source statement: 194. botctl health: Diagnostic détaillé.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `194. botctl health` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0014`; supporting items: none found by conservative heading match; domain indexes `CLIENT, OPERATIONS, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0200 — 195. botctl reconcile

- Source: `SRC-006`
- Location: lines 2234–2242; heading `195. botctl reconcile`
- Domain tags: CLIENT, RECONCILIATION, RISK
- Source statement: 195. botctl reconcile: Force : NO NEW RISK
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `195. botctl reconcile` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0015`; supporting items: none found by conservative heading match; domain indexes `CLIENT, RECONCILIATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0201 — 196. botctl update

- Source: `SRC-006`
- Location: lines 2243–2250; heading `196. botctl update`
- Domain tags: CLIENT, DEPLOYMENT
- Source statement: 196. botctl update: Il orchestre la séquence sûre décrite précédemment.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `196. botctl update` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0016`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0202 — 197. botctl rollback

- Source: `SRC-006`
- Location: lines 2251–2253; heading `197. botctl rollback`
- Domain tags: CLIENT, DEPLOYMENT
- Source statement: 197. botctl rollback: Même logique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `197. botctl rollback` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0017`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0203 — 198. botctl emergency-stop

- Source: `SRC-006`
- Location: lines 2254–2261; heading `198. botctl emergency-stop`
- Domain tags: CLIENT, EXECUTION, RECOVERY, RISK
- Source statement: 198. botctl emergency-stop: Produit : GLOBAL_KILL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `198. botctl emergency-stop` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0018`; supporting items: none found by conservative heading match; domain indexes `CLIENT, EXECUTION, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0204 — 199. Client modes

- Source: `SRC-006`
- Location: lines 2262–2271; heading `199. Client modes`
- Domain tags: CLIENT, DEPLOYMENT, VALIDATION, REPLAY
- Source statement: 199. Client modes: Installation peut être : REPLAY
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `199. Client modes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0019`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0205 — 200. Mode stored in config

- Source: `SRC-006`
- Location: lines 2272–2279; heading `200. Mode stored in config`
- Domain tags: DEPLOYMENT
- Source statement: 200. Mode stored in config: Mais le passage vers :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `200. Mode stored in config` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0159`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0206 — 201. Mode transition

- Source: `SRC-006`
- Location: lines 2280–2295; heading `201. Mode transition`
- Domain tags: DEPLOYMENT, RECONCILIATION, RISK, INFRA, SECURITY, VALIDATION
- Source statement: 201. Mode transition: n’est pas juste un changement de string.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `201. Mode transition` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0160`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION, RISK, INFRA, SECURITY, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0207 — 202. Production profiles

- Source: `SRC-006`
- Location: lines 2296–2304; heading `202. Production profiles`
- Domain tags: DEPLOYMENT, MICROSTRUCTURE, PRODUCT
- Source statement: 202. Production profiles: On peut fournir : profile-standard.toml
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `202. Production profiles` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0161`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, MICROSTRUCTURE, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0208 — 203. Pas de profil “YOLO”

- Source: `SRC-006`
- Location: lines 2305–2307; heading `203. Pas de profil “YOLO”`
- Domain tags: DEPLOYMENT, MICROSTRUCTURE, INFRA
- Source statement: 203. Pas de profil “YOLO”: Les paramètres ne peuvent pas contourner la constitution.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `203. Pas de profil “YOLO”` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0162`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, MICROSTRUCTURE, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0209 — 204. Customer data ownership

- Source: `SRC-006`
- Location: lines 2308–2315; heading `204. Customer data ownership`
- Domain tags: CLIENT, INFRA, PRODUCT, FUTURE
- Source statement: 204. Customer data ownership: Les données produites sur le VPS appartiennent au client selon nos conditions commerciales futures.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `204. Customer data ownership` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0020`; supporting items: none found by conservative heading match; domain indexes `CLIENT, INFRA, PRODUCT, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0210 — 205. No mandatory central ingestion

- Source: `SRC-006`
- Location: lines 2316–2318; heading `205. No mandatory central ingestion`
- Domain tags: DEPLOYMENT
- Source statement: 205. No mandatory central ingestion: Très important pour simplicité et confidentialité.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `205. No mandatory central ingestion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0163`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0211 — 206. Optional diagnostics telemetry

- Source: `SRC-006`
- Location: lines 2319–2328; heading `206. Optional diagnostics telemetry`
- Domain tags: DEPLOYMENT, INFRA, BENCHMARK, PRODUCT
- Source statement: 206. Optional diagnostics telemetry: Peut être activée pour :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `206. Optional diagnostics telemetry` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0164`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, BENCHMARK, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0212 — 207. Remote support

- Source: `SRC-006`
- Location: lines 2329–2337; heading `207. Remote support`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 207. Remote support: Si client le souhaite : ou éventuellement session SSH temporaire gérée par le client.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `207. Remote support` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0165`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0213 — 208. No embedded backdoor

- Source: `SRC-006`
- Location: lines 2338–2345; heading `208. No embedded backdoor`
- Domain tags: DEPLOYMENT
- Source statement: 208. No embedded backdoor: Le bot ne contient pas une :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `208. No embedded backdoor` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0166`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0214 — 209. Security updates

- Source: `SRC-006`
- Location: lines 2346–2354; heading `209. Security updates`
- Domain tags: SECURITY, DEPLOYMENT
- Source statement: 209. Security updates: Les dépendances critiques doivent être suivies. passe quand même les tests essentiels avant release.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `209. Security updates` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0014`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0215 — 210. Emergency release

- Source: `SRC-006`
- Location: lines 2355–2369; heading `210. Emergency release`
- Domain tags: DEPLOYMENT, VALIDATION, REPLAY
- Source statement: 210. Emergency release: Workflow raccourci possible pour vulnérabilité critique :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `210. Emergency release` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0167`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0216 — 211. Rollout metrics

- Source: `SRC-006`
- Location: lines 2370–2381; heading `211. Rollout metrics`
- Domain tags: DEPLOYMENT, RECONCILIATION, INFRA, OPERATIONS, ACCOUNTING
- Source statement: 211. Rollout metrics: comparés à la version précédente.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `211. Rollout metrics` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0168`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION, INFRA, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0217 — 212. Automatic rollback central ?

- Source: `SRC-006`
- Location: lines 2382–2390; heading `212. Automatic rollback central ?`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 212. Automatic rollback central ?: Je ne recommande pas qu’un serveur central ordonne automatiquement des rollbacks clients. Le bot peut détecter localement :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `212. Automatic rollback central ?` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0169`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0218 — 213. Version pinning client

- Source: `SRC-006`
- Location: lines 2391–2398; heading `213. Version pinning client`
- Domain tags: CLIENT, PRODUCT
- Source statement: 213. Version pinning client: Client production peut rester sur :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `213. Version pinning client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0021`; supporting items: none found by conservative heading match; domain indexes `CLIENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0219 — 214. Minimum supported version

- Source: `SRC-006`
- Location: lines 2399–2406; heading `214. Minimum supported version`
- Domain tags: DEPLOYMENT
- Source statement: 214. Minimum supported version: À terme, certaines versions anciennes seront : mais pas brutalement désactivées pendant une exposition.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `214. Minimum supported version` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0170`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0220 — 215. Breaking exchange change

- Source: `SRC-006`
- Location: lines 2407–2414; heading `215. Breaking exchange change`
- Domain tags: DEPLOYMENT, RISK
- Source statement: 215. Breaking exchange change: Si Hyperliquid modifie une règle critique et vieille version devient dangereuse :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `215. Breaking exchange change` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0171`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0221 — 216. Exchange compatibility

- Source: `SRC-006`
- Location: lines 2415–2421; heading `216. Exchange compatibility`
- Domain tags: DEPLOYMENT
- Source statement: 216. Exchange compatibility: Le bot maintient un :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `216. Exchange compatibility` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0172`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0222 — 217. Unknown exchange version/rule

- Source: `SRC-006`
- Location: lines 2422–2428; heading `217. Unknown exchange version/rule`
- Domain tags: DEPLOYMENT, RECOVERY, RISK
- Source statement: 217. Unknown exchange version/rule: Fail closed : NO NEW RISK
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `217. Unknown exchange version/rule` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0173`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0223 — 218. Secret rotation

- Source: `SRC-006`
- Location: lines 2429–2446; heading `218. Secret rotation`
- Domain tags: SECURITY, RECONCILIATION, RISK, CLIENT, OPERATIONS
- Source statement: 218. Secret rotation: Le client doit pouvoir changer son API wallet.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `218. Secret rotation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0015`; supporting items: none found by conservative heading match; domain indexes `SECURITY, RECONCILIATION, RISK, CLIENT, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0224 — 219. Pas de signer swap entre deux jambes

- Source: `SRC-006`
- Location: lines 2447–2449; heading `219. Pas de signer swap entre deux jambes`
- Domain tags: SECURITY
- Source statement: 219. Pas de signer swap entre deux jambes: Le signer utilisé par une ExecutionPlan reste stable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `219. Pas de signer swap entre deux jambes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0016`; supporting items: none found by conservative heading match; domain indexes `SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0225 — 220. Credential revocation

- Source: `SRC-006`
- Location: lines 2450–2452; heading `220. Credential revocation`
- Domain tags: DEPLOYMENT
- Source statement: 220. Credential revocation: Ancien API wallet révoqué après migration sécurisée.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `220. Credential revocation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0174`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0226 — 221. Host security baseline

- Source: `SRC-006`
- Location: lines 2453–2463; heading `221. Host security baseline`
- Domain tags: SECURITY, DEPLOYMENT
- Source statement: 221. Host security baseline: automatic security updates carefully configured
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `221. Host security baseline` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0017`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0227 — 222. Automatic host updates

- Source: `SRC-006`
- Location: lines 2464–2472; heading `222. Automatic host updates`
- Domain tags: DEPLOYMENT, SECURITY
- Source statement: 222. Automatic host updates: Les security updates peuvent être automatiques, mais les reboots doivent être contrôlés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `222. Automatic host updates` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0175`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0228 — 223. Reboot maintenance window

- Source: `SRC-006`
- Location: lines 2473–2480; heading `223. Reboot maintenance window`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 223. Reboot maintenance window: Le client peut définir une fenêtre.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `223. Reboot maintenance window` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0176`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0229 — 224. VPS provider maintenance

- Source: `SRC-006`
- Location: lines 2481–2490; heading `224. VPS provider maintenance`
- Domain tags: DEPLOYMENT, INFRA, EXECUTION, RECONCILIATION
- Source statement: 224. VPS provider maintenance: Impossible à contrôler totalement. D’où importance :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `224. VPS provider maintenance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0177`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, EXECUTION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0230 — 225. Backup VPS

- Source: `SRC-006`
- Location: lines 2491–2526; heading `225. Backup VPS`
- Domain tags: OPERATIONS, INFRA, ACCOUNTING
- Source statement: 225. Backup VPS: Il devient justifié par :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `225. Backup VPS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0015`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0231 — 226. Cold recovery > hot standby initialement

- Source: `SRC-006`
- Location: lines 2527–2538; heading `226. Cold recovery > hot standby initialement`
- Domain tags: DEPLOYMENT, RECOVERY, HOT_WARM_COLD, OPERATIONS
- Source statement: 226. Cold recovery > hot standby initialement: Au début : documented rapid redeploy
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `226. Cold recovery > hot standby initialement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0178`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECOVERY, HOT_WARM_COLD, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0232 — 227. Hot standby futur

- Source: `SRC-006`
- Location: lines 2539–2551; heading `227. Hot standby futur`
- Domain tags: DEPLOYMENT, HOT_WARM_COLD, INFRA
- Source statement: 227. Hot standby futur: tant qu’il n’a pas officiellement pris ownership.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `227. Hot standby futur` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0179`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, HOT_WARM_COLD, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0233 — 228. Split-brain prevention

- Source: `SRC-006`
- Location: lines 2552–2559; heading `228. Split-brain prevention`
- Domain tags: DEPLOYMENT, HOT_WARM_COLD
- Source statement: 228. Split-brain prevention: Condition indispensable avant hot standby.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `228. Split-brain prevention` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0180`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, HOT_WARM_COLD`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0234 — 229. Failover architecture

- Source: `SRC-006`
- Location: lines 2560–2567; heading `229. Failover architecture`
- Domain tags: OPERATIONS, ARCH, ACCOUNTING
- Source statement: 229. Failover architecture: À étudier seulement lorsque :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `229. Failover architecture` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0016`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, ARCH, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0235 — 230. Package vendu au client

- Source: `SRC-006`
- Location: lines 2568–2581; heading `230. Package vendu au client`
- Domain tags: CLIENT, DEPLOYMENT, LICENSE, PRODUCT
- Source statement: 230. Package vendu au client: Commercialement, le package peut contenir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `230. Package vendu au client` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0022`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, LICENSE, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0236 — 231. Pas de code source obligatoire

- Source: `SRC-006`
- Location: lines 2582–2589; heading `231. Pas de code source obligatoire`
- Domain tags: DEPLOYMENT, CLIENT, PRODUCT
- Source statement: 231. Pas de code source obligatoire: Le client reçoit : compiled artifact
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `231. Pas de code source obligatoire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0181`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0237 — 232. Protection intellectuelle

- Source: `SRC-006`
- Location: lines 2590–2605; heading `232. Protection intellectuelle`
- Domain tags: DEPLOYMENT, LICENSE, PRODUCT, ARCH
- Source statement: 232. Protection intellectuelle: Docker n’empêche pas totalement : Le vrai contrôle vient de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `232. Protection intellectuelle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0182`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, LICENSE, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0238 — 233. Obfuscation

- Source: `SRC-006`
- Location: lines 2606–2615; heading `233. Obfuscation`
- Domain tags: DEPLOYMENT, BENCHMARK
- Source statement: 233. Obfuscation: Je ne recommande pas d’ajouter une obfuscation agressive qui :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `233. Obfuscation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0183`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0239 — 234. Critical IP

- Source: `SRC-006`
- Location: lines 2616–2623; heading `234. Critical IP`
- Domain tags: DEPLOYMENT
- Source statement: 234. Critical IP: Une partie des modèles/calibrations peut être distribuée sous forme :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `234. Critical IP` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0184`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0240 — 235. Mais pas de dépendance serveur pour cacher l’algo

- Source: `SRC-006`
- Location: lines 2624–2632; heading `235. Mais pas de dépendance serveur pour cacher l’algo`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 235. Mais pas de dépendance serveur pour cacher l’algo: Déporter notre stratégie sur un serveur central : pour éviter que client voie le code
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `235. Mais pas de dépendance serveur pour cacher l’algo` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0185`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0241 — 236. Licence client max

- Source: `SRC-006`
- Location: lines 2633–2647; heading `236. Licence client max`
- Domain tags: LICENSE, CLIENT, PRODUCT
- Source statement: 236. Licence client max: Comme nous visons environ : nous pouvons garder une distribution volontairement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `236. Licence client max` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0005`; supporting items: none found by conservative heading match; domain indexes `LICENSE, CLIENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0242 — 237. Customer registry

- Source: `SRC-006`
- Location: lines 2648–2659; heading `237. Customer registry`
- Domain tags: CLIENT, DEPLOYMENT, LICENSE
- Source statement: 237. Customer registry: Simple base interne : customer
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `237. Customer registry` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0023`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0243 — 238. No customer secrets

- Source: `SRC-006`
- Location: lines 2660–2666; heading `238. No customer secrets`
- Domain tags: SECURITY, CLIENT
- Source statement: 238. No customer secrets: Notre CRM/licensing DB ne contient :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `238. No customer secrets` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0018`; supporting items: none found by conservative heading match; domain indexes `SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0244 — 239. Documentation package

- Source: `SRC-006`
- Location: lines 2667–2680; heading `239. Documentation package`
- Domain tags: DEPLOYMENT, RISK, SECURITY
- Source statement: 239. Documentation package: Chaque release stable doit avoir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `239. Documentation package` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0186`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0245 — 240. Release notes

- Source: `SRC-006`
- Location: lines 2681–2692; heading `240. Release notes`
- Domain tags: DEPLOYMENT, RISK, DATA
- Source statement: 240. Release notes: Doivent identifier : strategy changes
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `240. Release notes` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0187`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0246 — 241. Risk change visibility

- Source: `SRC-006`
- Location: lines 2693–2700; heading `241. Risk change visibility`
- Domain tags: DEPLOYMENT, RISK, CLIENT, ARCH
- Source statement: 241. Risk change visibility: Un client doit savoir si une update modifie :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `241. Risk change visibility` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0188`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RISK, CLIENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0247 — 242. Migration notes

- Source: `SRC-006`
- Location: lines 2701–2709; heading `242. Migration notes`
- Domain tags: DEPLOYMENT, DATA, PRODUCT
- Source statement: 242. Migration notes: config schema 3 → 4
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `242. Migration notes` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0189`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0248 — 243. Supported upgrade path

- Source: `SRC-006`
- Location: lines 2710–2722; heading `243. Supported upgrade path`
- Domain tags: DEPLOYMENT, ROUTING
- Source statement: 243. Supported upgrade path: 1.3 → 1.4 → 1.5
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `243. Supported upgrade path` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0190`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0249 — 244. Version compatibility matrix

- Source: `SRC-006`
- Location: lines 2723–2733; heading `244. Version compatibility matrix`
- Domain tags: DEPLOYMENT, DATA, ARCH
- Source statement: 244. Version compatibility matrix: Maintenir : bot version
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `244. Version compatibility matrix` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0191`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0250 — 245. Deployment manifest

- Source: `SRC-006`
- Location: lines 2734–2747; heading `245. Deployment manifest`
- Domain tags: DEPLOYMENT, DATA, DETERMINISM
- Source statement: 245. Deployment manifest: Chaque instance écrit : DeploymentManifest {
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `245. Deployment manifest` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0192`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DATA, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0251 — 246. Incident correlation

- Source: `SRC-006`
- Location: lines 2748–2754; heading `246. Incident correlation`
- Domain tags: OPERATIONS, PORTFOLIO, DATA, DEPLOYMENT
- Source statement: 246. Incident correlation: Chaque incident porte : deployment manifest ID
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `246. Incident correlation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-OPS-0017`; supporting items: none found by conservative heading match; domain indexes `OPERATIONS, PORTFOLIO, DATA, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0252 — 247. Reproduction

- Source: `SRC-006`
- Location: lines 2755–2764; heading `247. Reproduction`
- Domain tags: DEPLOYMENT, DETERMINISM, PRODUCT, CLIENT
- Source statement: 247. Reproduction: Lors d’un bug client, nous pouvons reproduire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `247. Reproduction` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0193`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DETERMINISM, PRODUCT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0253 — 248. No silent auto-update

- Source: `SRC-006`
- Location: lines 2765–2814; heading `248. No silent auto-update`
- Domain tags: DEPLOYMENT
- Source statement: 248. No silent auto-update: Toute modification du moteur est :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `248. No silent auto-update` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0194`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0254 — 249. No cloud dependency in execution

- Source: `SRC-006`
- Location: lines 2815–2842; heading `249. No cloud dependency in execution`
- Domain tags: DEPLOYMENT, INFRA, LICENSE, CLIENT
- Source statement: 249. No cloud dependency in execution: La chaîne critique finale doit rester :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `249. No cloud dependency in execution` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0195`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, LICENSE, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0255 — 250. Deployment security hierarchy

- Source: `SRC-006`
- Location: lines 2843–2859; heading `250. Deployment security hierarchy`
- Domain tags: SECURITY, DEPLOYMENT, RISK
- Source statement: 250. Deployment security hierarchy: 4. preserve ability to reduce risk
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `250. Deployment security hierarchy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0019`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0256 — 251. Important consequence

- Source: `SRC-006`
- Location: lines 2860–2868; heading `251. Important consequence`
- Domain tags: DEPLOYMENT, EXECUTION, RISK, LICENSE
- Source statement: 251. Important consequence: Si protéger notre licence entre en conflit avec : ability to cancel an unsafe order
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `251. Important consequence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0196`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RISK, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0257 — 252. Installation Definition of Done

- Source: `SRC-006`
- Location: lines 2869–2887; heading `252. Installation Definition of Done`
- Domain tags: DEPLOYMENT, VALIDATION, RECONCILIATION, CLOCK, INFRA, BENCHMARK, SECURITY, OPERATIONS
- Source statement: 252. Installation Definition of Done: Une nouvelle installation est valide lorsque :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `252. Installation Definition of Done` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0197`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, VALIDATION, RECONCILIATION, CLOCK, INFRA, BENCHMARK, SECURITY, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0258 — 253. Micro-live activation DoD

- Source: `SRC-006`
- Location: lines 2888–2900; heading `253. Micro-live activation DoD`
- Domain tags: DEPLOYMENT, VALIDATION, RECONCILIATION, RISK, INFRA, SECURITY, OPERATIONS
- Source statement: 253. Micro-live activation DoD: Avant activation : shadow period valid
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `253. Micro-live activation DoD` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0198`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `DEPLOYMENT, VALIDATION, RECONCILIATION, RISK, INFRA, SECURITY, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0259 — 254. Live activation DoD

- Source: `SRC-006`
- Location: lines 2901–2912; heading `254. Live activation DoD`
- Domain tags: DEPLOYMENT, EXECUTION, RECONCILIATION, RISK, VALIDATION, ACCOUNTING
- Source statement: 254. Live activation DoD: Avant augmentation : micro-live fills validated
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `254. Live activation DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0199`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, RECONCILIATION, RISK, VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0260 — 255. Upgrade DoD

- Source: `SRC-006`
- Location: lines 2913–2924; heading `255. Upgrade DoD`
- Domain tags: DEPLOYMENT, RECONCILIATION, OPERATIONS
- Source statement: 255. Upgrade DoD: Une update n’est réussie que si :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `255. Upgrade DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0200`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0261 — 256. Rollback DoD

- Source: `SRC-006`
- Location: lines 2925–2933; heading `256. Rollback DoD`
- Domain tags: DEPLOYMENT, RECONCILIATION
- Source statement: 256. Rollback DoD: previous version active reconciliation successful
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `256. Rollback DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0201`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0262 — 257. Security DoD

- Source: `SRC-006`
- Location: lines 2934–2948; heading `257. Security DoD`
- Domain tags: SECURITY, DEPLOYMENT
- Source statement: 257. Security DoD: non-root container no privileged
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `257. Security DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-SEC-0020`; supporting items: none found by conservative heading match; domain indexes `SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0263 — 258. Production simplicity principle

- Source: `SRC-006`
- Location: lines 2949–2962; heading `258. Production simplicity principle`
- Domain tags: DEPLOYMENT, PRODUCT, INFRA, CLIENT
- Source statement: 258. Production simplicity principle: Pour nos 30–50 clients, la cible doit rester : tant qu’un besoin mesuré ne justifie pas davantage.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `258. Production simplicity principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0202`; supporting items: SRC-005-ITEM-0607; domain indexes `DEPLOYMENT, PRODUCT, INFRA, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0264 — 259. Pas de Kubernetes

- Source: `SRC-006`
- Location: lines 2963–2972; heading `259. Pas de Kubernetes`
- Domain tags: DEPLOYMENT, CLIENT
- Source statement: 259. Pas de Kubernetes: Kubernetes n’apporte actuellement rien qui justifie : pour une installation client individuelle.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `259. Pas de Kubernetes` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0203`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: YES.

### SRC-006-ITEM-0265 — 260. Pas de central orchestration obligatoire

- Source: `SRC-006`
- Location: lines 2973–2980; heading `260. Pas de central orchestration obligatoire`
- Domain tags: DEPLOYMENT
- Source statement: 260. Pas de central orchestration obligatoire: mais pas avoir besoin de piloter les containers à distance.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `260. Pas de central orchestration obligatoire` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0204`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0266 — 261. Future fleet management

- Source: `SRC-006`
- Location: lines 2981–2988; heading `261. Future fleet management`
- Domain tags: DEPLOYMENT, FUTURE, CLIENT, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 261. Future fleet management: Si 50 clients rendent les updates manuelles pénibles, nous pourrons créer un : mais toujours hors hot path.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `261. Future fleet management` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `FUTURE`
- Cross-source references: `REQ-DEPLOY-0205`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, FUTURE, CLIENT, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0267 — 262. Fleet metadata

- Source: `SRC-006`
- Location: lines 2989–3003; heading `262. Fleet metadata`
- Domain tags: DEPLOYMENT, EXECUTION, LICENSE, OPERATIONS
- Source statement: 262. Fleet metadata: Pourrait gérer : version
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `262. Fleet metadata` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0206`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, EXECUTION, LICENSE, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0268 — 263. Final client deployment

- Source: `SRC-006`
- Location: lines 3004–3036; heading `263. Final client deployment`
- Domain tags: CLIENT, DEPLOYMENT, EXECUTION, RISK, RECORDER, DATA, CLOCK, INFRA
- Source statement: 263. Final client deployment: Market Feed Trading Core Recorder
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `263. Final client deployment` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-CLIENT-0024`; supporting items: none found by conservative heading match; domain indexes `CLIENT, DEPLOYMENT, EXECUTION, RISK, RECORDER, DATA, CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0269 — 264. Update architecture

- Source: `SRC-006`
- Location: lines 3037–3069; heading `264. Update architecture`
- Domain tags: DEPLOYMENT, ARCH, RECONCILIATION, RISK, CLIENT, VALIDATION
- Source statement: 264. Update architecture: PRIVATE REGISTRY Signed image
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `264. Update architecture` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0207`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ARCH, RECONCILIATION, RISK, CLIENT, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0270 — 265. Licence architecture

- Source: `SRC-006`
- Location: lines 3070–3087; heading `265. Licence architecture`
- Domain tags: LICENSE, ARCH, INFRA, CLIENT, VALIDATION
- Source statement: 265. Licence architecture: Le service de licence n’est pas consulté par trade.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `265. Licence architecture` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0006`; supporting items: none found by conservative heading match; domain indexes `LICENSE, ARCH, INFRA, CLIENT, VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0271 — 266. Failure architecture

- Source: `SRC-006`
- Location: lines 3088–3113; heading `266. Failure architecture`
- Domain tags: DEPLOYMENT, ARCH, RISK, LICENSE
- Source statement: 266. Failure architecture: our licence service temporarily down → bot continue pendant entitlement/grace approprié.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `266. Failure architecture` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0208`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, ARCH, RISK, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0272 — 267. Principe final de distribution

- Source: `SRC-006`
- Location: lines 3114–3134; heading `267. Principe final de distribution`
- Domain tags: DEPLOYMENT, PRODUCT, EXECUTION, RECONCILIATION, RISK, INFRA, CLIENT
- Source statement: 267. Principe final de distribution: Le produit doit donner au client : sans donner au logiciel :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `267. Principe final de distribution` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0209`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, PRODUCT, EXECUTION, RECONCILIATION, RISK, INFRA, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0273 — 268. Principe final de packaging

- Source: `SRC-006`
- Location: lines 3135–3246; heading `268. Principe final de packaging`
- Domain tags: DEPLOYMENT, INFRA, SECURITY, CLIENT
- Source statement: 268. Principe final de packaging: \boxed{ Image = Software } \boxed{ Volumes = Persistent\ State }
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `268. Principe final de packaging` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0210`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0274 — 269. Principe final de mise à jour

- Source: `SRC-006`
- Location: lines 3247–3338; heading `269. Principe final de mise à jour`
- Domain tags: DEPLOYMENT, RECONCILIATION, RISK
- Source statement: 269. Principe final de mise à jour: \boxed{ Update \Rightarrow Stop\ New\ Risk \rightarrow Reconcile \rightarrow Upgrade \rightarrow Reconcile } \boxed{ Pull\ New\ Image \rightarrow Continue\ Trading\ Blindly }
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `269. Principe final de mise à jour` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0211`; supporting items: SRC-001-ITEM-0126, SRC-001-ITEM-0127; domain indexes `DEPLOYMENT, RECONCILIATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0275 — 270. Principe final de licence

- Source: `SRC-006`
- Location: lines 3339–3392; heading `270. Principe final de licence`
- Domain tags: LICENSE, EXECUTION, RECOVERY, RECONCILIATION, RISK
- Source statement: 270. Principe final de licence: \boxed{ License\ Failure \not\Rightarrow Loss\ Of\ Risk\ Reduction } La licence peut empêcher :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `270. Principe final de licence` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-LIC-0007`; supporting items: none found by conservative heading match; domain indexes `LICENSE, EXECUTION, RECOVERY, RECONCILIATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0276 — 271. Principe final de sécurité

- Source: `SRC-006`
- Location: lines 3393–3427; heading `271. Principe final de sécurité`
- Domain tags: DEPLOYMENT, SECURITY, CLIENT
- Source statement: 271. Principe final de sécurité: Le client ne doit jamais avoir à nous confier sa clé privée pour faire fonctionner le produit. \boxed{ Client\ Secret \ stays\ Client\ Side }
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `271. Principe final de sécurité` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0212`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0277 — 272. Principe final d’exploitation

- Source: `SRC-006`
- Location: lines 3428–3501; heading `272. Principe final d’exploitation`
- Domain tags: DEPLOYMENT, DETERMINISM, PRODUCT
- Source statement: 272. Principe final d’exploitation: Pour la V1 commerciale : \boxed{ Simple + Isolated + Reproducible + Upgradeable + Rollbackable + FailSafe }
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `272. Principe final d’exploitation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0213`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, DETERMINISM, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0278 — 273. Definition of Done du Dossier 5

- Source: `SRC-006`
- Location: lines 3502–3544; heading `273. Definition of Done du Dossier 5`
- Domain tags: DEPLOYMENT, VALIDATION, RECOVERY, RECONCILIATION, INFRA, BENCHMARK, SECURITY, LICENSE
- Source statement: 273. Definition of Done du Dossier 5: Cette architecture de déploiement est considérée implémentée lorsque : image is immutable and versioned
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `273. Definition of Done du Dossier 5` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0214`; supporting items: SRC-004-ITEM-0143, SRC-005-ITEM-0608; domain indexes `DEPLOYMENT, VALIDATION, RECOVERY, RECONCILIATION, INFRA, BENCHMARK, SECURITY, LICENSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0279 — 274. Conclusion

- Source: `SRC-006`
- Location: lines 3545–3594; heading `274. Conclusion`
- Domain tags: DEPLOYMENT, INFRA, SECURITY, LICENSE, CLIENT, CAPITAL, PRODUCT, ARCH
- Source statement: 274. Conclusion: Le package final que nous vendrons ne sera donc pas simplement : mais un deployment product complet :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `274. Conclusion` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-DEPLOY-0215`; supporting items: none found by conservative heading match; domain indexes `DEPLOYMENT, INFRA, SECURITY, LICENSE, CLIENT, CAPITAL, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0280 — DOSSIER 6/6 — DEFINITION OF DONE & VALIDATION MATRIX

- Source: `SRC-006`
- Location: lines 3595–3596; heading `DOSSIER 6/6 — DEFINITION OF DONE & VALIDATION MATRIX`
- Domain tags: VALIDATION, REPLAY
- Source statement: DOSSIER 6/6 — DEFINITION OF DONE & VALIDATION MATRIX: Critères d’acceptation, protocole de test et passage R&D → Replay → Shadow → Micro-live → Live
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `DOSSIER 6/6 — DEFINITION OF DONE & VALIDATION MATRIX` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0015`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0281 — 1. Objectif

- Source: `SRC-006`
- Location: lines 3597–3638; heading `1. Objectif`
- Domain tags: VALIDATION, RECOVERY, RISK, DETERMINISM, BENCHMARK, ACCOUNTING, ARCH
- Source statement: 1. Objectif: Un module n’est jamais considéré comme terminé parce qu’il : Il est considéré comme terminé lorsqu’il satisfait une série de critères mesurables portant sur :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `1. Objectif` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0016`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, RISK, DETERMINISM, BENCHMARK, ACCOUNTING, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0282 — 2. Les 6 niveaux de maturité

- Source: `SRC-006`
- Location: lines 3639–3647; heading `2. Les 6 niveaux de maturité`
- Domain tags: VALIDATION, REPLAY, ARCH
- Source statement: 2. Les 6 niveaux de maturité: Chaque module possède un statut.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `2. Les 6 niveaux de maturité` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0017`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0283 — 3. M0 — SPECIFIED

- Source: `SRC-006`
- Location: lines 3648–3660; heading `3. M0 — SPECIFIED`
- Domain tags: VALIDATION, DATA, BENCHMARK, ARCH
- Source statement: 3. M0 — SPECIFIED: Aucune implémentation n’est encore nécessaire.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `3. M0 — SPECIFIED` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0018`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA, BENCHMARK, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0284 — 4. M1 — UNIT VALIDATED

- Source: `SRC-006`
- Location: lines 3661–3668; heading `4. M1 — UNIT VALIDATED`
- Domain tags: VALIDATION, REPLAY, ARCH
- Source statement: 4. M1 — UNIT VALIDATED: mais n’a pas encore prouvé sa valeur dans un replay réaliste.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `4. M1 — UNIT VALIDATED` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0019`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0285 — 5. M2 — REPLAY VALIDATED

- Source: `SRC-006`
- Location: lines 3669–3675; heading `5. M2 — REPLAY VALIDATED`
- Domain tags: VALIDATION, REPLAY, DATA, DETERMINISM, SIMULATOR, PRODUCT, ARCH
- Source statement: 5. M2 — REPLAY VALIDATED: Le module fonctionne sur :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `5. M2 — REPLAY VALIDATED` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0020`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY, DATA, DETERMINISM, SIMULATOR, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0286 — 6. M3 — SHADOW VALIDATED

- Source: `SRC-006`
- Location: lines 3676–3687; heading `6. M3 — SHADOW VALIDATED`
- Domain tags: VALIDATION, EXECUTION, INFRA, CAPITAL, ARCH
- Source statement: 6. M3 — SHADOW VALIDATED: sans envoyer de capital réel.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `6. M3 — SHADOW VALIDATED` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0021`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, INFRA, CAPITAL, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0287 — 7. M4 — MICRO-LIVE VALIDATED

- Source: `SRC-006`
- Location: lines 3688–3702; heading `7. M4 — MICRO-LIVE VALIDATED`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, RISK, INFRA, ACCOUNTING, CAPITAL, ARCH
- Source statement: 7. M4 — MICRO-LIVE VALIDATED: Le module utilise : petit capital réel
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `7. M4 — MICRO-LIVE VALIDATED` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0022`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, EXECUTION, RECOVERY, RISK, INFRA, ACCOUNTING, CAPITAL, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0288 — 8. M5 — LIVE VALIDATED

- Source: `SRC-006`
- Location: lines 3703–3711; heading `8. M5 — LIVE VALIDATED`
- Domain tags: VALIDATION, OPERATIONS, ARCH
- Source statement: 8. M5 — LIVE VALIDATED: Le module peut utiliser une capacité supérieure validée. LIVE VALIDATED ne signifie jamais “terminé pour toujours”.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `8. M5 — LIVE VALIDATED` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0023`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0289 — 9. Principe de progression

- Source: `SRC-006`
- Location: lines 3712–3728; heading `9. Principe de progression`
- Domain tags: VALIDATION
- Source statement: 9. Principe de progression: Passage uniquement : Pas :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `9. Principe de progression` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0024`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0290 — 10. Exceptions

- Source: `SRC-006`
- Location: lines 3729–3741; heading `10. Exceptions`
- Domain tags: VALIDATION, EXECUTION, RISK, CAPITAL
- Source statement: 10. Exceptions: Seuls certains composants purement techniques peuvent sauter : Mais jamais les composants modifiant :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `10. Exceptions` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0025`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RISK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0291 — 11. Validation par dépendance

- Source: `SRC-006`
- Location: lines 3742–3748; heading `11. Validation par dépendance`
- Domain tags: VALIDATION, SIMULATOR, ARCH
- Source statement: 11. Validation par dépendance: Un module ne peut dépasser le niveau de maturité de ses dépendances critiques. ne peut pas dépendre d’un :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `11. Validation par dépendance` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0026`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0292 — 12. Dependency Gate

- Source: `SRC-006`
- Location: lines 3749–3800; heading `12. Dependency Gate`
- Domain tags: VALIDATION, ARCH
- Source statement: 12. Dependency Gate: Pour module Maturity(m) \leq \min Maturity(CriticalDependencies_m)
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `12. Dependency Gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0027`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0293 — 13. Matrice globale des modules

- Source: `SRC-006`
- Location: lines 3801–3828; heading `13. Matrice globale des modules`
- Domain tags: VALIDATION, ARCH, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, INFRA
- Source statement: 13. Matrice globale des modules: Les composants majeurs sont :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `13. Matrice globale des modules` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0028`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0294 — 14. FEED ADAPTER — Definition of Done

- Source: `SRC-006`
- Location: lines 3829–3838; heading `14. FEED ADAPTER — Definition of Done`
- Domain tags: VALIDATION, ACCOUNTING, ARCH, CLOCK
- Source statement: 14. FEED ADAPTER — Definition of Done: Correctness Doit :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `14. FEED ADAPTER — Definition of Done` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0029`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, ARCH, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0295 — 15. Feed schema tests

- Source: `SRC-006`
- Location: lines 3839–3847; heading `15. Feed schema tests`
- Domain tags: VALIDATION, DATA, ACCOUNTING, RECOVERY
- Source statement: 15. Feed schema tests: Chaque payload connu : valid payload
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `15. Feed schema tests` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0030`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA, ACCOUNTING, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0296 — 16. Feed corruption

- Source: `SRC-006`
- Location: lines 3848–3851; heading `16. Feed corruption`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 16. Feed corruption: Message invalide : must never mutate BookState
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `16. Feed corruption` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0031`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0297 — 17. Feed reconnect

- Source: `SRC-006`
- Location: lines 3852–3861; heading `17. Feed reconnect`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 17. Feed reconnect: Test : disconnect
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `17. Feed reconnect` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0032`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0298 — 18. Feed freshness

- Source: `SRC-006`
- Location: lines 3862–3882; heading `18. Feed freshness`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 18. Feed freshness: Le système mesure : BookAge
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `18. Feed freshness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0033`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0299 — 19. Feed DoD M2

- Source: `SRC-006`
- Location: lines 3883–3887; heading `19. Feed DoD M2`
- Domain tags: VALIDATION, ACCOUNTING, REPLAY
- Source statement: 19. Feed DoD M2: Replay doit reproduire exactement :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `19. Feed DoD M2` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0034`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0300 — 20. Feed DoD M3

- Source: `SRC-006`
- Location: lines 3888–3893; heading `20. Feed DoD M3`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 20. Feed DoD M3: Shadow pendant plusieurs sessions sans :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `20. Feed DoD M3` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0035`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0301 — 21. Feed performance

- Source: `SRC-006`
- Location: lines 3894–3901; heading `21. Feed performance`
- Domain tags: VALIDATION, BENCHMARK, ACCOUNTING, CAPITAL
- Source statement: 21. Feed performance: Mesures : decode P50
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `21. Feed performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0036`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, ACCOUNTING, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0302 — 22. NORMALIZER — DoD

- Source: `SRC-006`
- Location: lines 3902–3935; heading `22. NORMALIZER — DoD`
- Domain tags: VALIDATION, DATA
- Source statement: 22. NORMALIZER — DoD: Même RAW : RawEvent
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `22. NORMALIZER — DoD` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0037`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0303 — 23. Roundtrip / normalization tests

- Source: `SRC-006`
- Location: lines 3936–3938; heading `23. Roundtrip / normalization tests`
- Domain tags: VALIDATION
- Source statement: 23. Roundtrip / normalization tests: Fixtures de vrais événements.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `23. Roundtrip / normalization tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0038`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0304 — 24. BOOK ENGINE — Correctness

- Source: `SRC-006`
- Location: lines 3939–3946; heading `24. BOOK ENGINE — Correctness`
- Domain tags: VALIDATION, CLOCK, QUANT
- Source statement: 24. BOOK ENGINE — Correctness: Doit garantir : bids sorted descending
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `24. BOOK ENGINE — Correctness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0039`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CLOCK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0305 — 25. Book reconstruction test

- Source: `SRC-006`
- Location: lines 3947–3951; heading `25. Book reconstruction test`
- Domain tags: VALIDATION, DATA
- Source statement: 25. Book reconstruction test: À partir d’un dataset : le book final doit égaler le book de référence.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `25. Book reconstruction test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0040`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0306 — 26. Book gap test

- Source: `SRC-006`
- Location: lines 3952–3956; heading `26. Book gap test`
- Domain tags: VALIDATION
- Source statement: 26. Book gap test: Sequence gap : BookState.valid = false
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `26. Book gap test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0041`; supporting items: SRC-004-ITEM-0277; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0307 — 27. No silent repair

- Source: `SRC-006`
- Location: lines 3957–3961; heading `27. No silent repair`
- Domain tags: VALIDATION
- Source statement: 27. No silent repair: ne peut pas être deviné.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `27. No silent repair` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0042`; supporting items: SRC-005-ITEM-0113; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0308 — 28. Book performance

- Source: `SRC-006`
- Location: lines 3962–3972; heading `28. Book performance`
- Domain tags: VALIDATION, BENCHMARK, DEPLOYMENT
- Source statement: 28. Book performance: Mesurer : update P50
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `28. Book performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0043`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0309 — 29. Book memory

- Source: `SRC-006`
- Location: lines 3973–3977; heading `29. Book memory`
- Domain tags: VALIDATION
- Source statement: 29. Book memory: Mesurer : bytes per market
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `29. Book memory` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0044`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0310 — 30. METADATA ENGINE — DoD

- Source: `SRC-006`
- Location: lines 3978–3986; heading `30. METADATA ENGINE — DoD`
- Domain tags: VALIDATION
- Source statement: 30. METADATA ENGINE — DoD: Doit fournir exactement : quote
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `30. METADATA ENGINE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0045`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0311 — 31. Metadata change

- Source: `SRC-006`
- Location: lines 3987–3991; heading `31. Metadata change`
- Domain tags: VALIDATION, ROUTING, GRAPH
- Source statement: 31. Metadata change: Une modification doit : invalidate affected routes
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `31. Metadata change` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0046`; supporting items: SRC-005-ITEM-0111; domain indexes `VALIDATION, ROUTING, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0312 — 32. Fee Engine — DoD

- Source: `SRC-006`
- Location: lines 3992–3998; heading `32. Fee Engine — DoD`
- Domain tags: VALIDATION, ACCOUNTING, ARCH
- Source statement: 32. Fee Engine — DoD: et produire les mêmes résultats en :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `32. Fee Engine — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0047`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0313 — 33. Fee historical replay

- Source: `SRC-006`
- Location: lines 3999–4003; heading `33. Fee historical replay`
- Domain tags: VALIDATION, ACCOUNTING, REPLAY
- Source statement: 33. Fee historical replay: Un replay ancien utilise :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `33. Fee historical replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0048`; supporting items: SRC-005-ITEM-0528; domain indexes `VALIDATION, ACCOUNTING, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0314 — 34. Fee unknown

- Source: `SRC-006`
- Location: lines 4004–4007; heading `34. Fee unknown`
- Domain tags: VALIDATION, RECOVERY, ACCOUNTING
- Source statement: 34. Fee unknown: Doit provoquer : REJECT_FEE_STATE_UNKNOWN
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `34. Fee unknown` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0049`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0315 — 35. PRICE/SIZE QUANTIZER — DoD

- Source: `SRC-006`
- Location: lines 4008–4016; heading `35. PRICE/SIZE QUANTIZER — DoD`
- Domain tags: VALIDATION, QUANT, SIZING
- Source statement: 35. PRICE/SIZE QUANTIZER — DoD: Tester toutes les frontières :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `35. PRICE/SIZE QUANTIZER — DoD` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0050`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT, SIZING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0316 — 36. Golden exchange boundary tests

- Source: `SRC-006`
- Location: lines 4017–4019; heading `36. Golden exchange boundary tests`
- Domain tags: VALIDATION
- Source statement: 36. Golden exchange boundary tests: Pour chaque marché représentatif.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `36. Golden exchange boundary tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0051`; supporting items: SRC-007-ITEM-0290; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0317 — 37. NETCONVERT — DoD

- Source: `SRC-006`
- Location: lines 4020–4029; heading `37. NETCONVERT — DoD`
- Domain tags: VALIDATION, ROUTING, EXECUTION, ACCOUNTING
- Source statement: 37. NETCONVERT — DoD: Doit passer : base→quote
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `37. NETCONVERT — DoD` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0052`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0318 — 38. Golden NetConvert

- Source: `SRC-006`
- Location: lines 4030–4032; heading `38. Golden NetConvert`
- Domain tags: VALIDATION, ROUTING
- Source statement: 38. Golden NetConvert: Cas simples calculables à la main.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `38. Golden NetConvert` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0053`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0319 — 39. NetConvert parity

- Source: `SRC-006`
- Location: lines 4033–4058; heading `39. NetConvert parity`
- Domain tags: VALIDATION, ROUTING, ARCH
- Source statement: 39. NetConvert parity: Rust-Python| \leq tolerance
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `39. NetConvert parity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0054`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0320 — 40. ROUTE ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4059–4066; heading `40. ROUTE ENGINE — DoD`
- Domain tags: VALIDATION, ROUTING, BRIDGE, TRIANGLE
- Source statement: 40. ROUTE ENGINE — DoD: Doit precompute correctement : Direct
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `40. ROUTE ENGINE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0055`; supporting items: SRC-002-ITEM-0075, SRC-002-ITEM-0097; domain indexes `VALIDATION, ROUTING, BRIDGE, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0321 — 41. Route graph validation

- Source: `SRC-006`
- Location: lines 4067–4072; heading `41. Route graph validation`
- Domain tags: VALIDATION, ROUTING, GRAPH
- Source statement: 41. Route graph validation: Pour chaque route : output_asset_leg_n
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `41. Route graph validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0056`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0322 — 42. Cycle validation

- Source: `SRC-006`
- Location: lines 4073–4096; heading `42. Cycle validation`
- Domain tags: VALIDATION, ROUTING, TRIANGLE
- Source statement: 42. Cycle validation: Triangle : StartAsset=EndAsset
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `42. Cycle validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0057`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0323 — 43. OWA validation

- Source: `SRC-006`
- Location: lines 4097–4103; heading `43. OWA validation`
- Domain tags: VALIDATION, OWA, BRIDGE, ROUTING
- Source statement: 43. OWA validation: OWA nécessite : direct comparator exists
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `43. OWA validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0058`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OWA, BRIDGE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0324 — 44. pair_to_routes validation

- Source: `SRC-006`
- Location: lines 4104–4107; heading `44. pair_to_routes validation`
- Domain tags: VALIDATION, ROUTING, GRAPH, DEPLOYMENT
- Source statement: 44. pair_to_routes validation: Chaque market update doit sélectionner : all and only affected routes
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `44. pair_to_routes validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0059`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, GRAPH, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0325 — 45. Route performance

- Source: `SRC-006`
- Location: lines 4108–4114; heading `45. Route performance`
- Domain tags: VALIDATION, BENCHMARK, ROUTING, GRAPH
- Source statement: 45. Route performance: Mesurer : affected route lookup
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `45. Route performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0060`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, ROUTING, GRAPH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0326 — 46. QUANT MICROSTRUCTURE — DoD

- Source: `SRC-006`
- Location: lines 4115–4125; heading `46. QUANT MICROSTRUCTURE — DoD`
- Domain tags: VALIDATION, MICROSTRUCTURE, QUANT, FORMULA, ARCH
- Source statement: 46. QUANT MICROSTRUCTURE — DoD: Formules : Spread
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `46. QUANT MICROSTRUCTURE — DoD` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0061`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, MICROSTRUCTURE, QUANT, FORMULA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0327 — 47. Invalid inputs

- Source: `SRC-006`
- Location: lines 4126–4132; heading `47. Invalid inputs`
- Domain tags: VALIDATION
- Source statement: 47. Invalid inputs: Aucun : division by zero
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `47. Invalid inputs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0062`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0328 — 48. Rolling calculations

- Source: `SRC-006`
- Location: lines 4133–4137; heading `48. Rolling calculations`
- Domain tags: VALIDATION, DATA
- Source statement: 48. Rolling calculations: Doivent être comparées à :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `48. Rolling calculations` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0063`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0329 — 49. Incremental error test

- Source: `SRC-006`
- Location: lines 4138–4175; heading `49. Incremental error test`
- Domain tags: VALIDATION, DEPLOYMENT
- Source statement: 49. Incremental error test: Pour 1 million d’updates :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `49. Incremental error test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0064`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0330 — 50. MARKET ATLAS — DoD

- Source: `SRC-006`
- Location: lines 4176–4186; heading `50. MARKET ATLAS — DoD`
- Domain tags: VALIDATION, MARKET_ATLAS, ACCOUNTING, SURVIVAL, INVENTORY, BRIDGE, GRAPH, PRODUCT
- Source statement: 50. MARKET ATLAS — DoD: Pour chaque asset : liquidity
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `50. MARKET ATLAS — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0065`; supporting items: SRC-001-ITEM-0134, SRC-003-ITEM-0059, SRC-003-ITEM-0191, SRC-007-ITEM-0123; domain indexes `VALIDATION, MARKET_ATLAS, ACCOUNTING, SURVIVAL, INVENTORY, BRIDGE, GRAPH, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0331 — 51. Atlas missing data

- Source: `SRC-006`
- Location: lines 4187–4191; heading `51. Atlas missing data`
- Domain tags: VALIDATION, RECOVERY
- Source statement: 51. Atlas missing data: Doit produire : UNKNOWN / LOW CONFIDENCE
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `51. Atlas missing data` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0066`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0332 — 52. HOT/WARM/COLD — DoD

- Source: `SRC-006`
- Location: lines 4192–4197; heading `52. HOT/WARM/COLD — DoD`
- Domain tags: VALIDATION, HOT_WARM_COLD, CAPITAL
- Source statement: 52. HOT/WARM/COLD — DoD: Transitions déterministes à partir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `52. HOT/WARM/COLD — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0067`; supporting items: SRC-001-ITEM-0049, SRC-001-ITEM-0051, SRC-002-ITEM-0106, SRC-002-ITEM-0124; domain indexes `VALIDATION, HOT_WARM_COLD, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0333 — 53. HOT/WARM/COLD resource test

- Source: `SRC-006`
- Location: lines 4198–4204; heading `53. HOT/WARM/COLD resource test`
- Domain tags: VALIDATION, HOT_WARM_COLD, INFRA, CAPITAL
- Source statement: 53. HOT/WARM/COLD resource test: Mesurer l’économie de CPU. Exemple :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `53. HOT/WARM/COLD resource test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0068`; supporting items: SRC-001-ITEM-0049, SRC-007-ITEM-0115; domain indexes `VALIDATION, HOT_WARM_COLD, INFRA, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0334 — 54. PARTICIPANT MODEL — Baseline DoD

- Source: `SRC-006`
- Location: lines 4205–4209; heading `54. PARTICIPANT MODEL — Baseline DoD`
- Domain tags: VALIDATION, PARTICIPANTS, SURVIVAL
- Source statement: 54. PARTICIPANT MODEL — Baseline DoD: Le premier Champion doit battre :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `54. PARTICIPANT MODEL — Baseline DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0069`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PARTICIPANTS, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0335 — 55. Survival calibration

- Source: `SRC-006`
- Location: lines 4210–4216; heading `55. Survival calibration`
- Domain tags: VALIDATION, SURVIVAL, EXECUTION, RISK
- Source statement: 55. Survival calibration: Si modèle annonce : P=0.8
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `55. Survival calibration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0070`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SURVIVAL, EXECUTION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0336 — 56. Survival metrics

- Source: `SRC-006`
- Location: lines 4217–4223; heading `56. Survival metrics`
- Domain tags: VALIDATION, SURVIVAL
- Source statement: 56. Survival metrics: Mesurer : Brier
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `56. Survival metrics` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0071`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SURVIVAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0337 — 57. Economic validation

- Source: `SRC-006`
- Location: lines 4224–4242; heading `57. Economic validation`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 57. Economic validation: Mais surtout : EconomicLift>0
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `57. Economic validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0072`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0338 — 58. Participant model OOD

- Source: `SRC-006`
- Location: lines 4243–4248; heading `58. Participant model OOD`
- Domain tags: VALIDATION, PARTICIPANTS, QUANT
- Source statement: 58. Participant model OOD: Doit explicitement détecter : unsupported size
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `58. Participant model OOD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0073`; supporting items: SRC-004-ITEM-0130, SRC-005-ITEM-0108, SRC-007-ITEM-0075, SRC-007-ITEM-0120; domain indexes `VALIDATION, PARTICIPANTS, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0339 — 59. Participant fallback

- Source: `SRC-006`
- Location: lines 4249–4253; heading `59. Participant fallback`
- Domain tags: VALIDATION, PARTICIPANTS
- Source statement: 59. Participant fallback: Si modèle unavailable : empirical conservative model
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `59. Participant fallback` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0074`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PARTICIPANTS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0340 — 60. CROSS-MARKET MODEL — DoD

- Source: `SRC-006`
- Location: lines 4254–4257; heading `60. CROSS-MARKET MODEL — DoD`
- Domain tags: VALIDATION, CROSS_MARKET, PRODUCT
- Source statement: 60. CROSS-MARKET MODEL — DoD: Une relation entre marchés entre en production uniquement si : out-of-sample predictive improvement > 0
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `60. CROSS-MARKET MODEL — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0075`; supporting items: SRC-007-ITEM-0055, SRC-007-ITEM-0132, SRC-007-ITEM-0153; domain indexes `VALIDATION, CROSS_MARKET, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0341 — 61. No pure correlation adoption

- Source: `SRC-006`
- Location: lines 4258–4268; heading `61. No pure correlation adoption`
- Domain tags: VALIDATION, PORTFOLIO
- Source statement: 61. No pure correlation adoption: Un : 0.9
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `61. No pure correlation adoption` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0076`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PORTFOLIO`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0342 — 62. Cross-market ablation

- Source: `SRC-006`
- Location: lines 4269–4274; heading `62. Cross-market ablation`
- Domain tags: VALIDATION, CROSS_MARKET
- Source statement: 62. Cross-market ablation: Comparer : model without cross-market
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `62. Cross-market ablation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0077`; supporting items: SRC-007-ITEM-0132; domain indexes `VALIDATION, CROSS_MARKET`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0343 — 63. If no lift

- Source: `SRC-006`
- Location: lines 4275–4277; heading `63. If no lift`
- Domain tags: VALIDATION
- Source statement: 63. If no lift: Feature supprimée.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `63. If no lift` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0078`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0344 — 64. MAKER FILL MODEL — DoD

- Source: `SRC-006`
- Location: lines 4278–4283; heading `64. MAKER FILL MODEL — DoD`
- Domain tags: VALIDATION, EXECUTION, MAKER_MODEL
- Source statement: 64. MAKER FILL MODEL — DoD: Doit prédire : P(fill before horizons)
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `64. MAKER FILL MODEL — DoD` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0079`; supporting items: SRC-004-ITEM-0212; domain indexes `VALIDATION, EXECUTION, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0345 — 65. Fill calibration

- Source: `SRC-006`
- Location: lines 4284–4288; heading `65. Fill calibration`
- Domain tags: VALIDATION, EXECUTION
- Source statement: 65. Fill calibration: doit correspondre environ au taux observé du bucket.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `65. Fill calibration` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0080`; supporting items: SRC-004-ITEM-0259; domain indexes `VALIDATION, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0346 — 66. Adverse selection model

- Source: `SRC-006`
- Location: lines 4289–4306; heading `66. Adverse selection model`
- Domain tags: VALIDATION, MAKER_MODEL, EXECUTION
- Source statement: 66. Adverse selection model: Doit mesurer : E[AS(h)|fill]
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `66. Adverse selection model` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0081`; supporting items: SRC-004-ITEM-0214, SRC-007-ITEM-0222, SRC-008-ITEM-0035; domain indexes `VALIDATION, MAKER_MODEL, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0347 — 67. Maker strategy activation

- Source: `SRC-006`
- Location: lines 4307–4312; heading `67. Maker strategy activation`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, MAKER_MODEL
- Source statement: 67. Maker strategy activation: MT ne passe Micro-live que si :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `67. Maker strategy activation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-VALID-0082`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECOVERY, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0348 — 68. SIMULATOR — DoD F0

- Source: `SRC-006`
- Location: lines 4313–4319; heading `68. SIMULATOR — DoD F0`
- Domain tags: VALIDATION, SIMULATOR, EXECUTION, ACCOUNTING
- Source statement: 68. SIMULATOR — DoD F0: F0 doit correctement reproduire :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `68. SIMULATOR — DoD F0` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0083`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, EXECUTION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0349 — 69. Simulator F1

- Source: `SRC-006`
- Location: lines 4320–4326; heading `69. Simulator F1`
- Domain tags: VALIDATION, SIMULATOR, EXECUTION, INFRA, QUANT
- Source statement: 69. Simulator F1: Doit ajouter : latency
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `69. Simulator F1` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0084`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, EXECUTION, INFRA, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0350 — 70. F1 validation

- Source: `SRC-006`
- Location: lines 4327–4332; heading `70. F1 validation`
- Domain tags: VALIDATION, EXECUTION
- Source statement: 70. F1 validation: Pour ordres historiques/micro-live : predicted mechanical fill
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `70. F1 validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0085`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0351 — 71. Simulator F2

- Source: `SRC-006`
- Location: lines 4333–4338; heading `71. Simulator F2`
- Domain tags: VALIDATION, SIMULATOR, EXECUTION, MICROSTRUCTURE, PRODUCT
- Source statement: 71. Simulator F2: et pas faux fill déterministe.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `71. Simulator F2` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0086`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, EXECUTION, MICROSTRUCTURE, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0352 — 72. Simulator F3

- Source: `SRC-006`
- Location: lines 4339–4342; heading `72. Simulator F3`
- Domain tags: VALIDATION, SIMULATOR, PARTICIPANTS, PRODUCT
- Source statement: 72. Simulator F3: Participant response. Doit produire distributions calibrées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `72. Simulator F3` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0087`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, PARTICIPANTS, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0353 — 73. F4

- Source: `SRC-006`
- Location: lines 4343–4345; heading `73. F4`
- Domain tags: VALIDATION, RESEARCH
- Source statement: 73. F4: Research only tant que non validé.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `73. F4` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0088`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0354 — 74. Simulator requirement

- Source: `SRC-006`
- Location: lines 4346–4352; heading `74. Simulator requirement`
- Domain tags: VALIDATION, SIMULATOR, DETERMINISM, ACCOUNTING, PRODUCT
- Source statement: 74. Simulator requirement: Jamais : one deterministic PnL number
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `74. Simulator requirement` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0089`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, DETERMINISM, ACCOUNTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0355 — 75. Simulator outputs validation

- Source: `SRC-006`
- Location: lines 4353–4362; heading `75. Simulator outputs validation`
- Domain tags: VALIDATION, SIMULATOR, EXECUTION, RECOVERY, QUANT
- Source statement: 75. Simulator outputs validation: Comparer : median
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `75. Simulator outputs validation` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0090`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, EXECUTION, RECOVERY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0356 — 76. Coverage validation

- Source: `SRC-006`
- Location: lines 4363–4368; heading `76. Coverage validation`
- Domain tags: VALIDATION
- Source statement: 76. Coverage validation: Si intervalle P90 est annoncé :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `76. Coverage validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0091`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0357 — 77. Simulator OOD

- Source: `SRC-006`
- Location: lines 4369–4373; heading `77. Simulator OOD`
- Domain tags: VALIDATION, SIMULATOR, RISK
- Source statement: 77. Simulator OOD: Grande taille hors calibration :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `77. Simulator OOD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0092`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0358 — 78. POSITION SIZING — DoD

- Source: `SRC-006`
- Location: lines 4374–4383; heading `78. POSITION SIZING — DoD`
- Domain tags: VALIDATION, SIZING, INVENTORY, QUANT
- Source statement: 78. POSITION SIZING — DoD: Pour chaque candidate size :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `78. POSITION SIZING — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0093`; supporting items: SRC-004-ITEM-0235, SRC-005-ITEM-0063, SRC-007-ITEM-0305; domain indexes `VALIDATION, SIZING, INVENTORY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0359 — 79. Sizing monotonic assumptions

- Source: `SRC-006`
- Location: lines 4384–4387; heading `79. Sizing monotonic assumptions`
- Domain tags: VALIDATION, CLOCK, SIZING, ACCOUNTING
- Source statement: 79. Sizing monotonic assumptions: larger q = proportionally larger PnL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `79. Sizing monotonic assumptions` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0094`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CLOCK, SIZING, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0360 — 80. Sizing grid validation

- Source: `SRC-006`
- Location: lines 4388–4392; heading `80. Sizing grid validation`
- Domain tags: VALIDATION, SIZING, RESEARCH
- Source statement: 80. Sizing grid validation: à une recherche exhaustive sur petits cas tests.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `80. Sizing grid validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0095`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIZING, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0361 — 81. ValidatedCapacity DoD

- Source: `SRC-006`
- Location: lines 4393–4396; heading `81. ValidatedCapacity DoD`
- Domain tags: VALIDATION, CAPITAL, RISK
- Source statement: 81. ValidatedCapacity DoD: Doit toujours respecter : all risk gates
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `81. ValidatedCapacity DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0096`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CAPITAL, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0362 — 82. Sizing safety

- Source: `SRC-006`
- Location: lines 4397–4404; heading `82. Sizing safety`
- Domain tags: VALIDATION, SIZING, RISK
- Source statement: 82. Sizing safety: Si aucune taille n’est valide :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `82. Sizing safety` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0097`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIZING, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0363 — 83. ORDER SLICING — DoD

- Source: `SRC-006`
- Location: lines 4405–4411; heading `83. ORDER SLICING — DoD`
- Domain tags: VALIDATION, EXECUTION, SLICING, REPLAY
- Source statement: 83. ORDER SLICING — DoD: Comparer en replay : single order
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `83. ORDER SLICING — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0098`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, SLICING, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0364 — 84. Fragmentation validation

- Source: `SRC-006`
- Location: lines 4412–4416; heading `84. Fragmentation validation`
- Domain tags: VALIDATION, SLICING, RISK
- Source statement: 84. Fragmentation validation: Même-time children doivent reproduire environ :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `84. Fragmentation validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0099`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SLICING, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0365 — 85. Temporal slicing

- Source: `SRC-006`
- Location: lines 4417–4422; heading `85. Temporal slicing`
- Domain tags: VALIDATION, SLICING, PARTICIPANTS, LIQUIDITY_RESPONSE
- Source statement: 85. Temporal slicing: Doit démontrer un gain après :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `85. Temporal slicing` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0100`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SLICING, PARTICIPANTS, LIQUIDITY_RESPONSE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0366 — 86. No gain

- Source: `SRC-006`
- Location: lines 4423–4425; heading `86. No gain`
- Domain tags: VALIDATION
- Source statement: 86. No gain: Pas d’activation.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `86. No gain` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0101`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0367 — 87. INVENTORY ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4426–4466; heading `87. INVENTORY ENGINE — DoD`
- Domain tags: VALIDATION, INVENTORY, EXECUTION
- Source statement: 87. INVENTORY ENGINE — DoD: Inventory_{new} = Inventory_{old} + AssetDelta
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `87. INVENTORY ENGINE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0102`; supporting items: SRC-003-ITEM-0189, SRC-004-ITEM-0133; domain indexes `VALIDATION, INVENTORY, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0368 — 88. Inventory reconciliation

- Source: `SRC-006`
- Location: lines 4467–4471; heading `88. Inventory reconciliation`
- Domain tags: VALIDATION, RECONCILIATION, INVENTORY
- Source statement: 88. Inventory reconciliation: Doit correspondre à : exchange balances
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `88. Inventory reconciliation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0103`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECONCILIATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0369 — 89. Inventory band tests

- Source: `SRC-006`
- Location: lines 4472–4479; heading `89. Inventory band tests`
- Domain tags: VALIDATION, INVENTORY
- Source statement: 89. Inventory band tests: Tester : target
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `89. Inventory band tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0104`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0370 — 90. Hard gate property

- Source: `SRC-006`
- Location: lines 4480–4482; heading `90. Hard gate property`
- Domain tags: VALIDATION, RISK
- Source statement: 90. Hard gate property: Impossible de produire volontairement un état hors hard band via NEW_RISK.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `90. Hard gate property` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0105`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0371 — 91. NetFlow

- Source: `SRC-006`
- Location: lines 4483–4485; heading `91. NetFlow`
- Domain tags: VALIDATION
- Source statement: 91. NetFlow: Comparer rolling calculation à référence offline.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `91. NetFlow` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0106`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0372 — 92. TERMINAL VIABILITY — DoD

- Source: `SRC-006`
- Location: lines 4486–4491; heading `92. TERMINAL VIABILITY — DoD`
- Domain tags: VALIDATION, BRIDGE, MARKET_ATLAS, RISK, INVENTORY, OWA
- Source statement: 92. TERMINAL VIABILITY — DoD: OWA doit être rejeté si terminal asset :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `92. TERMINAL VIABILITY — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0107`; supporting items: SRC-003-ITEM-0139, SRC-005-ITEM-0075; domain indexes `VALIDATION, BRIDGE, MARKET_ATLAS, RISK, INVENTORY, OWA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0373 — 93. BRIDGE ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4492–4494; heading `93. BRIDGE ENGINE — DoD`
- Domain tags: VALIDATION, BRIDGE
- Source statement: 93. BRIDGE ENGINE — DoD: Doit comparer tous les paths autorisés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `93. BRIDGE ENGINE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0108`; supporting items: SRC-001-ITEM-0057, SRC-007-ITEM-0124; domain indexes `VALIDATION, BRIDGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0374 — 94. Bridge path validation

- Source: `SRC-006`
- Location: lines 4495–4514; heading `94. Bridge path validation`
- Domain tags: VALIDATION, BRIDGE, ROUTING
- Source statement: 94. Bridge path validation: Le plus court chemin n’est pas forcément choisi.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `94. Bridge path validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0109`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BRIDGE, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0375 — 95. Bridge accounting

- Source: `SRC-006`
- Location: lines 4515–4520; heading `95. Bridge accounting`
- Domain tags: VALIDATION, ACCOUNTING, BRIDGE, INVENTORY, ROUTING
- Source statement: 95. Bridge accounting: Séparer : BridgePnL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `95. Bridge accounting` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0110`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, BRIDGE, INVENTORY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0376 — 96. Hysteresis test

- Source: `SRC-006`
- Location: lines 4521–4527; heading `96. Hysteresis test`
- Domain tags: VALIDATION
- Source statement: 96. Hysteresis test: Le moteur ne doit pas flip-flop excessivement.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `96. Hysteresis test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0111`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0377 — 97. PORTFOLIO OPTIMIZER — DoD

- Source: `SRC-006`
- Location: lines 4528–4532; heading `97. PORTFOLIO OPTIMIZER — DoD`
- Domain tags: VALIDATION, PORTFOLIO, ROUTING
- Source statement: 97. PORTFOLIO OPTIMIZER — DoD: Cas simple : independent routes
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `97. PORTFOLIO OPTIMIZER — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0112`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PORTFOLIO, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0378 — 98. Shared-book test

- Source: `SRC-006`
- Location: lines 4533–4536; heading `98. Shared-book test`
- Domain tags: VALIDATION, ROUTING
- Source statement: 98. Shared-book test: Deux routes consommant même depth : cannot both reserve full visible amount
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `98. Shared-book test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0113`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0379 — 99. Shared-balance test

- Source: `SRC-006`
- Location: lines 4537–4539; heading `99. Shared-balance test`
- Domain tags: VALIDATION, INVENTORY
- Source statement: 99. Shared-balance test: Même invariant.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `99. Shared-balance test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0114`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0380 — 100. Optimizer correctness

- Source: `SRC-006`
- Location: lines 4540–4543; heading `100. Optimizer correctness`
- Domain tags: VALIDATION
- Source statement: 100. Optimizer correctness: Sur petits problèmes : compare to brute-force solution
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `100. Optimizer correctness` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0115`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0381 — 101. Optimizer performance

- Source: `SRC-006`
- Location: lines 4544–4549; heading `101. Optimizer performance`
- Domain tags: VALIDATION, BENCHMARK
- Source statement: 101. Optimizer performance: Si optimisation complète trop lente :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `101. Optimizer performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0116`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0382 — 102. RISK ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4550–4556; heading `102. RISK ENGINE — DoD`
- Domain tags: VALIDATION, RISK
- Source statement: 102. RISK ENGINE — DoD: Chaque invariant du Dossier 3 possède :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `102. RISK ENGINE — DoD` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0117`; supporting items: SRC-002-ITEM-0068, SRC-004-ITEM-0132, SRC-005-ITEM-0217, SRC-005-ITEM-0220; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0383 — 103. No stale trade test

- Source: `SRC-006`
- Location: lines 4557–4559; heading `103. No stale trade test`
- Domain tags: VALIDATION
- Source statement: 103. No stale trade test: Obligatoire.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `103. No stale trade test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0118`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0384 — 104. Unknown state test

- Source: `SRC-006`
- Location: lines 4560–4562; heading `104. Unknown state test`
- Domain tags: VALIDATION, RECOVERY
- Source statement: 104. Unknown state test: Obligatoire.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `104. Unknown state test` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0119`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0385 — 105. Hard inventory test

- Source: `SRC-006`
- Location: lines 4563–4565; heading `105. Hard inventory test`
- Domain tags: VALIDATION, INVENTORY
- Source statement: 105. Hard inventory test: Obligatoire.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `105. Hard inventory test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0120`; supporting items: SRC-005-ITEM-0205; domain indexes `VALIDATION, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0386 — 106. CVaR gate test

- Source: `SRC-006`
- Location: lines 4566–4568; heading `106. CVaR gate test`
- Domain tags: VALIDATION, RISK
- Source statement: 106. CVaR gate test: Obligatoire.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `106. CVaR gate test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0121`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0387 — 107. OOD gate test

- Source: `SRC-006`
- Location: lines 4569–4571; heading `107. OOD gate test`
- Domain tags: VALIDATION
- Source statement: 107. OOD gate test: Obligatoire.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `107. OOD gate test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0122`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0388 — 108. Infra unsafe test

- Source: `SRC-006`
- Location: lines 4572–4574; heading `108. Infra unsafe test`
- Domain tags: VALIDATION, RISK, INFRA
- Source statement: 108. Infra unsafe test: Obligatoire.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `108. Infra unsafe test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0123`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0389 — 109. Risk determinism

- Source: `SRC-006`
- Location: lines 4575–4582; heading `109. Risk determinism`
- Domain tags: VALIDATION, RISK, DETERMINISM
- Source statement: 109. Risk determinism: Même : RiskSnapshot
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `109. Risk determinism` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0124`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0390 — 110. Risk performance

- Source: `SRC-006`
- Location: lines 4583–4589; heading `110. Risk performance`
- Domain tags: VALIDATION, RISK, BENCHMARK
- Source statement: 110. Risk performance: Mesurer : P50
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `110. Risk performance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0125`; supporting items: SRC-008-ITEM-0199; domain indexes `VALIDATION, RISK, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0391 — 111. EXECUTION STATE MACHINE — DoD

- Source: `SRC-006`
- Location: lines 4590–4603; heading `111. EXECUTION STATE MACHINE — DoD`
- Domain tags: VALIDATION, EXECUTION, OPERATIONS, ACCOUNTING, INVENTORY
- Source statement: 111. EXECUTION STATE MACHINE — DoD: Reprend Dossier 1. Obligatoire :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `111. EXECUTION STATE MACHINE — DoD` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0126`; supporting items: SRC-004-ITEM-0137, SRC-004-ITEM-0143, SRC-005-ITEM-0473; domain indexes `VALIDATION, EXECUTION, OPERATIONS, ACCOUNTING, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0392 — 112. No blind retry property

- Source: `SRC-006`
- Location: lines 4604–4606; heading `112. No blind retry property`
- Domain tags: VALIDATION
- Source statement: 112. No blind retry property: À tester via fault injection.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `112. No blind retry property` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0127`; supporting items: SRC-005-ITEM-0024; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0393 — 113. Actual fill property

- Source: `SRC-006`
- Location: lines 4607–4610; heading `113. Actual fill property`
- Domain tags: VALIDATION, EXECUTION
- Source statement: 113. Actual fill property: must use actual previous output
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `113. Actual fill property` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0128`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0394 — 114. Execution event ordering

- Source: `SRC-006`
- Location: lines 4611–4613; heading `114. Execution event ordering`
- Domain tags: VALIDATION, DETERMINISM, EXECUTION
- Source statement: 114. Execution event ordering: Out-of-order events ne doivent pas corrompre state.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `114. Execution event ordering` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0129`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DETERMINISM, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0395 — 115. Execution determinism

- Source: `SRC-006`
- Location: lines 4614–4617; heading `115. Execution determinism`
- Domain tags: VALIDATION, DETERMINISM
- Source statement: 115. Execution determinism: Même event stream : same final ExecutionState
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `115. Execution determinism` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0130`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0396 — 116. Execution throughput

- Source: `SRC-006`
- Location: lines 4618–4623; heading `116. Execution throughput`
- Domain tags: VALIDATION, EXECUTION
- Source statement: 116. Execution throughput: Tester pics : many opportunities
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `116. Execution throughput` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0131`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0397 — 117. RECOVERY ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4624–4630; heading `117. RECOVERY ENGINE — DoD`
- Domain tags: VALIDATION, RECOVERY, EXECUTION
- Source statement: 117. RECOVERY ENGINE — DoD: Cas : Leg1 partial
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `117. RECOVERY ENGINE — DoD` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0132`; supporting items: SRC-003-ITEM-0151; domain indexes `VALIDATION, RECOVERY, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0398 — 118. Recovery objective

- Source: `SRC-006`
- Location: lines 4631–4635; heading `118. Recovery objective`
- Domain tags: VALIDATION, RECOVERY, ROUTING
- Source statement: 118. Recovery objective: Doit choisir meilleure solution selon :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `118. Recovery objective` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0133`; supporting items: SRC-004-ITEM-0072, SRC-004-ITEM-0239; domain indexes `VALIDATION, RECOVERY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0399 — 119. Recovery limit

- Source: `SRC-006`
- Location: lines 4636–4638; heading `119. Recovery limit`
- Domain tags: VALIDATION, RECOVERY, RISK
- Source statement: 119. Recovery limit: Pas de boucle infinie.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `119. Recovery limit` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0134`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0400 — 120. Recovery loss accounting

- Source: `SRC-006`
- Location: lines 4639–4641; heading `120. Recovery loss accounting`
- Domain tags: VALIDATION, RECOVERY, ACCOUNTING
- Source statement: 120. Recovery loss accounting: Exact.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `120. Recovery loss accounting` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0135`; supporting items: SRC-004-ITEM-0240; domain indexes `VALIDATION, RECOVERY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0401 — 121. RECONCILIATION ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4642–4650; heading `121. RECONCILIATION ENGINE — DoD`
- Domain tags: VALIDATION, RECONCILIATION, EXECUTION, RECOVERY, OPERATIONS, INVENTORY
- Source statement: 121. RECONCILIATION ENGINE — DoD: Scénarios : local == exchange
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `121. RECONCILIATION ENGINE — DoD` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0136`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECONCILIATION, EXECUTION, RECOVERY, OPERATIONS, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0402 — 122. Reconciliation success

- Source: `SRC-006`
- Location: lines 4651–4655; heading `122. Reconciliation success`
- Domain tags: VALIDATION, RECONCILIATION
- Source statement: 122. Reconciliation success: AccountState doit égaler ExchangeTruth dans tolérance.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `122. Reconciliation success` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0137`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0403 — 123. Reconciliation failure

- Source: `SRC-006`
- Location: lines 4656–4659; heading `123. Reconciliation failure`
- Domain tags: VALIDATION, RECONCILIATION
- Source statement: 123. Reconciliation failure: Doit bloquer : READY
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `123. Reconciliation failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0138`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0404 — 124. RECORDER — DoD

- Source: `SRC-006`
- Location: lines 4660–4667; heading `124. RECORDER — DoD`
- Domain tags: VALIDATION, EXECUTION, RECORDER
- Source statement: 124. RECORDER — DoD: Mesurer : throughput
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `124. RECORDER — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0139`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0405 — 125. Recorder nonblocking

- Source: `SRC-006`
- Location: lines 4668–4672; heading `125. Recorder nonblocking`
- Domain tags: VALIDATION, EXECUTION, RECORDER, INFRA, ROUTING, HOT_WARM_COLD
- Source statement: 125. Recorder nonblocking: ne doit pas augmenter dramatiquement hot-path latency.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `125. Recorder nonblocking` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0140`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECORDER, INFRA, ROUTING, HOT_WARM_COLD`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0406 — 126. Recorder priority

- Source: `SRC-006`
- Location: lines 4673–4677; heading `126. Recorder priority`
- Domain tags: VALIDATION, EXECUTION, RECORDER
- Source statement: 126. Recorder priority: En saturation : execution/account preserved
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `126. Recorder priority` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0141`; supporting items: SRC-005-ITEM-0393; domain indexes `VALIDATION, EXECUTION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0407 — 127. Checksum

- Source: `SRC-006`
- Location: lines 4678–4680; heading `127. Checksum`
- Domain tags: VALIDATION, RECORDER
- Source statement: 127. Checksum: Chaque chunk fermé vérifiable.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `127. Checksum` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0142`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0408 — 128. Replay roundtrip

- Source: `SRC-006`
- Location: lines 4681–4687; heading `128. Replay roundtrip`
- Domain tags: VALIDATION, REPLAY
- Source statement: 128. Replay roundtrip: doit reconstruire le même normalized stream.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `128. Replay roundtrip` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0143`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0409 — 129. REPLAY ENGINE — DoD

- Source: `SRC-006`
- Location: lines 4688–4720; heading `129. REPLAY ENGINE — DoD`
- Domain tags: VALIDATION, REPLAY, DATA, CLOCK
- Source statement: 129. REPLAY ENGINE — DoD: Même dataset/config/model/seed : DecisionTrace_A = DecisionTrace_B
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `129. REPLAY ENGINE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0144`; supporting items: SRC-001-ITEM-0135, SRC-008-ITEM-0206; domain indexes `VALIDATION, REPLAY, DATA, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0410 — 130. Hash test

- Source: `SRC-006`
- Location: lines 4721–4723; heading `130. Hash test`
- Domain tags: VALIDATION, DETERMINISM
- Source statement: 130. Hash test: DecisionTrace hash identique.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `130. Hash test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0145`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0411 — 131. No lookahead

- Source: `SRC-006`
- Location: lines 4724–4727; heading `131. No lookahead`
- Domain tags: VALIDATION
- Source statement: 131. No lookahead: Un futur event ne doit jamais influencer décision antérieure.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `131. No lookahead` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0146`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0412 — 132. Receive-time replay

- Source: `SRC-006`
- Location: lines 4728–4731; heading `132. Receive-time replay`
- Domain tags: VALIDATION, REPLAY
- Source statement: 132. Receive-time replay: Doit respecter : what bot actually knew
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `132. Receive-time replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0147`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0413 — 133. Counterfactual replay

- Source: `SRC-006`
- Location: lines 4732–4734; heading `133. Counterfactual replay`
- Domain tags: VALIDATION, SIMULATOR, REPLAY, RESEARCH
- Source statement: 133. Counterfactual replay: Les hypothèses doivent être explicitement versionnées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `133. Counterfactual replay` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0148`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SIMULATOR, REPLAY, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0414 — 134. SHADOW MODE — DoD

- Source: `SRC-006`
- Location: lines 4735–4740; heading `134. SHADOW MODE — DoD`
- Domain tags: VALIDATION, ARCH
- Source statement: 134. SHADOW MODE — DoD: Même core que Live. Seul :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `134. SHADOW MODE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0149`; supporting items: SRC-001-ITEM-0017; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0415 — 135. Shadow stability

- Source: `SRC-006`
- Location: lines 4741–4746; heading `135. Shadow stability`
- Domain tags: VALIDATION
- Source statement: 135. Shadow stability: Doit fonctionner plusieurs jours sans :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `135. Shadow stability` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0150`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0416 — 136. Shadow decisions

- Source: `SRC-006`
- Location: lines 4747–4752; heading `136. Shadow decisions`
- Domain tags: VALIDATION, EXECUTION
- Source statement: 136. Shadow decisions: Enregistrer : would trade
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `136. Shadow decisions` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0151`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0417 — 137. Shadow false-positive analysis

- Source: `SRC-006`
- Location: lines 4753–4755; heading `137. Shadow false-positive analysis`
- Domain tags: VALIDATION
- Source statement: 137. Shadow false-positive analysis: Suivre ce qui se serait passé après les opportunités sélectionnées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `137. Shadow false-positive analysis` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0152`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0418 — 138. MICRO-LIVE — DoD

- Source: `SRC-006`
- Location: lines 4756–4758; heading `138. MICRO-LIVE — DoD`
- Domain tags: VALIDATION, CAPITAL
- Source statement: 138. MICRO-LIVE — DoD: Capital par trade strictement plafonné.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `138. MICRO-LIVE — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0153`; supporting items: SRC-001-ITEM-0018, SRC-001-ITEM-0076, SRC-001-ITEM-0146, SRC-005-ITEM-0481; domain indexes `VALIDATION, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0419 — 139. Micro-live initial size

- Source: `SRC-006`
- Location: lines 4759–4763; heading `139. Micro-live initial size`
- Domain tags: VALIDATION, SIZING
- Source statement: 139. Micro-live initial size: comme calibration probe, pas comme sizing définitif.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `139. Micro-live initial size` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0154`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, SIZING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0420 — 140. Micro-live frequency

- Source: `SRC-006`
- Location: lines 4764–4767; heading `140. Micro-live frequency`
- Domain tags: VALIDATION, RISK
- Source statement: 140. Micro-live frequency: Plafonnée pour limiter : unexpected model error
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `140. Micro-live frequency` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0155`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0421 — 141. Micro-live metrics

- Source: `SRC-006`
- Location: lines 4768–4784; heading `141. Micro-live metrics`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, INFRA, ACCOUNTING
- Source statement: 141. Micro-live metrics: Pour chaque trade : predicted fill
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `141. Micro-live metrics` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0156`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, EXECUTION, RECOVERY, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0422 — 142. Minimum observations

- Source: `SRC-006`
- Location: lines 4785–4791; heading `142. Minimum observations`
- Domain tags: VALIDATION
- Source statement: 142. Minimum observations: Pas de chiffre universel à figer maintenant.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `142. Minimum observations` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0157`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0423 — 143. Statistical stopping rule

- Source: `SRC-006`
- Location: lines 4792–4794; heading `143. Statistical stopping rule`
- Domain tags: VALIDATION
- Source statement: 143. Statistical stopping rule: On cherche suffisamment d’observations pour que les intervalles de confiance deviennent utiles.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `143. Statistical stopping rule` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0158`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0424 — 144. Micro-live acceptance

- Source: `SRC-006`
- Location: lines 4795–4801; heading `144. Micro-live acceptance`
- Domain tags: VALIDATION, RECONCILIATION, RISK, OPERATIONS
- Source statement: 144. Micro-live acceptance: tail losses within model support
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `144. Micro-live acceptance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0159`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, RECONCILIATION, RISK, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0425 — 145. LIVE SCALING — principe

- Source: `SRC-006`
- Location: lines 4802–4806; heading `145. LIVE SCALING — principe`
- Domain tags: VALIDATION
- Source statement: 145. LIVE SCALING — principe: Passage Micro-live → Live ne signifie pas : 50 € → 5000 €
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `145. LIVE SCALING — principe` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0160`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0426 — 146. Capital ladder

- Source: `SRC-006`
- Location: lines 4807–4813; heading `146. Capital ladder`
- Domain tags: VALIDATION, CAPITAL
- Source statement: 146. Capital ladder: avec validation à chaque palier.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `146. Capital ladder` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0161`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0427 — 147. Scaling gate

- Source: `SRC-006`
- Location: lines 4814–4821; heading `147. Scaling gate`
- Domain tags: VALIDATION, RISK, SIMULATOR, INVENTORY, QUANT
- Source statement: 147. Scaling gate: enough trades at current band simulator calibrated at next band
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `147. Scaling gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-VALID-0162`; supporting items: SRC-005-ITEM-0165; domain indexes `VALIDATION, RISK, SIMULATOR, INVENTORY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0428 — 148. Maximum increase

- Source: `SRC-006`
- Location: lines 4822–4835; heading `148. Maximum increase`
- Domain tags: VALIDATION
- Source statement: 148. Maximum increase: Doit rester dans : Q_{validated}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `148. Maximum increase` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0163`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0429 — 149. No automatic compounding

- Source: `SRC-006`
- Location: lines 4836–4839; heading `149. No automatic compounding`
- Domain tags: VALIDATION, ACCOUNTING, MICROSTRUCTURE
- Source statement: 149. No automatic compounding: does not directly increase q
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `149. No automatic compounding` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0164`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0430 — 150. INFRASTRUCTURE — DoD

- Source: `SRC-006`
- Location: lines 4840–4845; heading `150. INFRASTRUCTURE — DoD`
- Domain tags: VALIDATION, INFRA, BENCHMARK, PRODUCT
- Source statement: 150. INFRASTRUCTURE — DoD: Avant fournisseur production : same benchmark binary
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `150. INFRASTRUCTURE — DoD` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0165`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, BENCHMARK, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0431 — 151. Benchmark metrics

- Source: `SRC-006`
- Location: lines 4846–4859; heading `151. Benchmark metrics`
- Domain tags: VALIDATION, BENCHMARK, EXECUTION, RECORDER, CLOCK, INFRA, DEPLOYMENT, ACCOUNTING
- Source statement: 151. Benchmark metrics: Au minimum : feed first-arrival
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `151. Benchmark metrics` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0166`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, EXECUTION, RECORDER, CLOCK, INFRA, DEPLOYMENT, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0432 — 152. Screening

- Source: `SRC-006`
- Location: lines 4860–4864; heading `152. Screening`
- Domain tags: VALIDATION
- Source statement: 152. Screening: comme méthode initiale, à ajuster selon observations.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `152. Screening` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0167`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0433 — 153. Finalists

- Source: `SRC-006`
- Location: lines 4865–4867; heading `153. Finalists`
- Domain tags: VALIDATION
- Source statement: 153. Finalists: Plusieurs jours si nécessaire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `153. Finalists` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0168`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0434 — 154. Provider selection

- Source: `SRC-006`
- Location: lines 4868–4882; heading `154. Provider selection`
- Domain tags: VALIDATION, INFRA, ACCOUNTING
- Source statement: 154. Provider selection: Pas : best ping
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `154. Provider selection` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0169`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0435 — 155. Infra economic validation

- Source: `SRC-006`
- Location: lines 4883–4914; heading `155. Infra economic validation`
- Domain tags: VALIDATION, INFRA, ACCOUNTING
- Source statement: 155. Infra economic validation: LCB(\Delta PnL) > SafetyFactor\times\Delta Cost
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `155. Infra economic validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0170`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0436 — 156. Infra downgrade validation

- Source: `SRC-006`
- Location: lines 4915–4917; heading `156. Infra downgrade validation`
- Domain tags: VALIDATION, INFRA
- Source statement: 156. Infra downgrade validation: Même moteur doit tester le downgrade.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `156. Infra downgrade validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0171`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0437 — 157. VPS failure test

- Source: `SRC-006`
- Location: lines 4918–4925; heading `157. VPS failure test`
- Domain tags: VALIDATION, INFRA, OPERATIONS
- Source statement: 157. VPS failure test: Simuler : network loss
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `157. VPS failure test` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0172`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0438 — 158. DOCKER — DoD

- Source: `SRC-006`
- Location: lines 4926–4935; heading `158. DOCKER — DoD`
- Domain tags: VALIDATION, DEPLOYMENT, INFRA, OPERATIONS
- Source statement: 158. DOCKER — DoD: Doit passer : install
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `158. DOCKER — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0173`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, INFRA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0439 — 159. Security tests

- Source: `SRC-006`
- Location: lines 4936–4942; heading `159. Security tests`
- Domain tags: VALIDATION, SECURITY, DEPLOYMENT
- Source statement: 159. Security tests: non-root no privileged
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `159. Security tests` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0174`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0440 — 160. Docker restart

- Source: `SRC-006`
- Location: lines 4943–4947; heading `160. Docker restart`
- Domain tags: VALIDATION, DEPLOYMENT, OPERATIONS, RECONCILIATION
- Source statement: 160. Docker restart: Toujours : RECONCILING
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `160. Docker restart` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0175`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, OPERATIONS, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0441 — 161. Update test

- Source: `SRC-006`
- Location: lines 4948–4952; heading `161. Update test`
- Domain tags: VALIDATION, DEPLOYMENT, RISK
- Source statement: 161. Update test: Active execution pendant update request :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `161. Update test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0176`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0442 — 162. Rollback test

- Source: `SRC-006`
- Location: lines 4953–4957; heading `162. Rollback test`
- Domain tags: VALIDATION, DEPLOYMENT, RECONCILIATION
- Source statement: 162. Rollback test: Nouvelle version invalide : previous digest restored
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `162. Rollback test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0177`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0443 — 163. Licence failure test

- Source: `SRC-006`
- Location: lines 4958–4961; heading `163. Licence failure test`
- Domain tags: VALIDATION, LICENSE, RISK, INFRA
- Source statement: 163. Licence failure test: existing risk management remains functional
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `163. Licence failure test` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0178`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, LICENSE, RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0444 — 164. ACCOUNTING — DoD

- Source: `SRC-006`
- Location: lines 4962–4985; heading `164. ACCOUNTING — DoD`
- Domain tags: VALIDATION, ACCOUNTING, EXECUTION
- Source statement: 164. ACCOUNTING — DoD: fills + fees + rounding
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `164. ACCOUNTING — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0179`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0445 — 165. Route PnL

- Source: `SRC-006`
- Location: lines 4986–4989; heading `165. Route PnL`
- Domain tags: VALIDATION, ACCOUNTING, ROUTING, EXECUTION, DETERMINISM, PRODUCT
- Source statement: 165. Route PnL: Doit être reproductible depuis :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `165. Route PnL` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0180`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, ROUTING, EXECUTION, DETERMINISM, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0446 — 166. No double counting

- Source: `SRC-006`
- Location: lines 4990–4996; heading `166. No double counting`
- Domain tags: VALIDATION, ACCOUNTING, INVENTORY, BRIDGE, CROSS_EXCHANGE
- Source statement: 166. No double counting: Tests obligatoires : inventory MTM
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `166. No double counting` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0181`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, INVENTORY, BRIDGE, CROSS_EXCHANGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0447 — 167. External flow

- Source: `SRC-006`
- Location: lines 4997–5000; heading `167. External flow`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 167. External flow: Dépôt : does not create PnL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `167. External flow` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0182`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0448 — 168. Portfolio equity

- Source: `SRC-006`
- Location: lines 5001–5006; heading `168. Portfolio equity`
- Domain tags: VALIDATION, PORTFOLIO, INVENTORY
- Source statement: 168. Portfolio equity: Doit être reconstruit à partir de :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `168. Portfolio equity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0183`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PORTFOLIO, INVENTORY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0449 — 169. PnL reconciliation

- Source: `SRC-006`
- Location: lines 5007–5012; heading `169. PnL reconciliation`
- Domain tags: VALIDATION, RECONCILIATION, ACCOUNTING
- Source statement: 169. PnL reconciliation: Comparer : local equity
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `169. PnL reconciliation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0184`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECONCILIATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0450 — 170. MONITORING — DoD

- Source: `SRC-006`
- Location: lines 5013–5015; heading `170. MONITORING — DoD`
- Domain tags: VALIDATION, OPERATIONS
- Source statement: 170. MONITORING — DoD: Toutes les métriques critiques exposées.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `170. MONITORING — DoD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0185`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0451 — 171. Minimum metrics

- Source: `SRC-006`
- Location: lines 5016–5031; heading `171. Minimum metrics`
- Domain tags: VALIDATION, RECOVERY, RECONCILIATION, RISK, INFRA, OPERATIONS, ACCOUNTING
- Source statement: 171. Minimum metrics: EngineState FeedHealth
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `171. Minimum metrics` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0186`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, RECONCILIATION, RISK, INFRA, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0452 — 172. Alerts

- Source: `SRC-006`
- Location: lines 5032–5042; heading `172. Alerts`
- Domain tags: VALIDATION, OPERATIONS, EXECUTION, RECOVERY, RECONCILIATION, RISK, CLOCK, INFRA
- Source statement: 172. Alerts: Critiques : BOOK_STALE
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `172. Alerts` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0187`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS, EXECUTION, RECOVERY, RECONCILIATION, RISK, CLOCK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0453 — 173. Alert quality

- Source: `SRC-006`
- Location: lines 5043–5047; heading `173. Alert quality`
- Domain tags: VALIDATION, OPERATIONS
- Source statement: 173. Alert quality: Une alerte critique doit être : Pas 10 000 alertes inutiles.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `173. Alert quality` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0188`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0454 — 174. Incident recording

- Source: `SRC-006`
- Location: lines 5048–5052; heading `174. Incident recording`
- Domain tags: VALIDATION, OPERATIONS
- Source statement: 174. Incident recording: Toute alerte critique crée : si elle correspond à un incident réel.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `174. Incident recording` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0189`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0455 — 175. PERFORMANCE BUDGET — principe

- Source: `SRC-006`
- Location: lines 5053–5064; heading `175. PERFORMANCE BUDGET — principe`
- Domain tags: VALIDATION, BENCHMARK, RISK, ROUTING, QUANT, ARCH
- Source statement: 175. PERFORMANCE BUDGET — principe: Chaque module reçoit un budget.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `175. PERFORMANCE BUDGET — principe` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0190`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, RISK, ROUTING, QUANT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0456 — 176. Budget global interne

- Source: `SRC-006`
- Location: lines 5065–5070; heading `176. Budget global interne`
- Domain tags: VALIDATION, BENCHMARK, RESEARCH
- Source statement: 176. Budget global interne: Hypothèse de design initiale : P50 ≈ quelques centaines de µs
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `176. Budget global interne` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0191`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0457 — 177. Important

- Source: `SRC-006`
- Location: lines 5071–5076; heading `177. Important`
- Domain tags: VALIDATION, BENCHMARK
- Source statement: 177. Important: Les targets de performance sont :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `177. Important` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0192`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0458 — 178. Performance regression test

- Source: `SRC-006`
- Location: lines 5077–5082; heading `178. Performance regression test`
- Domain tags: VALIDATION, BENCHMARK, QUANT
- Source statement: 178. Performance regression test: Chaque release compare : current
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `178. Performance regression test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0193`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0459 — 179. Regression threshold

- Source: `SRC-006`
- Location: lines 5083–5087; heading `179. Regression threshold`
- Domain tags: VALIDATION, QUANT
- Source statement: 179. Regression threshold: Une dégradation significative : requires explanation
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `179. Regression threshold` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0194`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0460 — 180. Economic performance regression

- Source: `SRC-006`
- Location: lines 5088–5117; heading `180. Economic performance regression`
- Domain tags: VALIDATION, BENCHMARK, ACCOUNTING, QUANT, DATA, RESEARCH
- Source statement: 180. Economic performance regression: Même logique : NetPnL_{new}
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `180. Economic performance regression` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0195`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, ACCOUNTING, QUANT, DATA, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0461 — 181. New feature gate

- Source: `SRC-006`
- Location: lines 5118–5123; heading `181. New feature gate`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 181. New feature gate: Toute feature importante doit passer :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `181. New feature gate` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0196`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0462 — 182. Feature ablation

- Source: `SRC-006`
- Location: lines 5124–5128; heading `182. Feature ablation`
- Domain tags: VALIDATION
- Source statement: 182. Feature ablation: Comparer : with feature
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `182. Feature ablation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0197`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0463 — 183. If feature doesn't help

- Source: `SRC-006`
- Location: lines 5129–5131; heading `183. If feature doesn't help`
- Domain tags: VALIDATION, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 183. If feature doesn't help: Supprimer du hot path.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `183. If feature doesn't help` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0198`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0464 — 184. Quant Model ROI

- Source: `SRC-006`
- Location: lines 5132–5183; heading `184. Quant Model ROI`
- Domain tags: VALIDATION, QUANT, INFRA, ACCOUNTING
- Source statement: 184. Quant Model ROI: ModelValue = PnL_{new} - PnL_{old} - PnLLostFromExtraLatency
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `184. Quant Model ROI` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0199`; supporting items: SRC-004-ITEM-0261, SRC-007-ITEM-0310; domain indexes `VALIDATION, QUANT, INFRA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0465 — 185. Promotion gate

- Source: `SRC-006`
- Location: lines 5184–5204; heading `185. Promotion gate`
- Domain tags: VALIDATION
- Source statement: 185. Promotion gate: LCB(ModelValue)>0 idéalement avec marge.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `185. Promotion gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0200`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0466 — 186. TEST CATEGORIES

- Source: `SRC-006`
- Location: lines 5205–5217; heading `186. TEST CATEGORIES`
- Domain tags: VALIDATION, BENCHMARK, REPLAY, ARCH
- Source statement: 186. TEST CATEGORIES: Chaque module utilise selon besoin :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `186. TEST CATEGORIES` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0201`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0467 — 187. UNIT TEST

- Source: `SRC-006`
- Location: lines 5218–5220; heading `187. UNIT TEST`
- Domain tags: VALIDATION
- Source statement: 187. UNIT TEST: Teste une fonction isolée.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `187. UNIT TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0202`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0468 — 188. GOLDEN TEST

- Source: `SRC-006`
- Location: lines 5221–5225; heading `188. GOLDEN TEST`
- Domain tags: VALIDATION, FORMULA
- Source statement: 188. GOLDEN TEST: Input fixe : known exact expected output
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `188. GOLDEN TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0203`; supporting items: SRC-004-ITEM-0277, SRC-005-ITEM-0485; domain indexes `VALIDATION, FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0469 — 189. PROPERTY TEST

- Source: `SRC-006`
- Location: lines 5226–5228; heading `189. PROPERTY TEST`
- Domain tags: VALIDATION
- Source statement: 189. PROPERTY TEST: Teste invariants sur grande variété d’inputs.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `189. PROPERTY TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0204`; supporting items: SRC-005-ITEM-0203, SRC-005-ITEM-0204, SRC-005-ITEM-0205, SRC-005-ITEM-0206; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0470 — 190. INTEGRATION TEST

- Source: `SRC-006`
- Location: lines 5229–5231; heading `190. INTEGRATION TEST`
- Domain tags: VALIDATION, ARCH
- Source statement: 190. INTEGRATION TEST: Plusieurs modules ensemble.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `190. INTEGRATION TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0205`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0471 — 191. REPLAY TEST

- Source: `SRC-006`
- Location: lines 5232–5234; heading `191. REPLAY TEST`
- Domain tags: VALIDATION, REPLAY
- Source statement: 191. REPLAY TEST: Événements historiques.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `191. REPLAY TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0206`; supporting items: SRC-005-ITEM-0485, SRC-005-ITEM-0486; domain indexes `VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0472 — 192. FAULT INJECTION

- Source: `SRC-006`
- Location: lines 5235–5242; heading `192. FAULT INJECTION`
- Domain tags: VALIDATION, EXECUTION, CLOCK
- Source statement: 192. FAULT INJECTION: Injecte : disconnect
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `192. FAULT INJECTION` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0207`; supporting items: SRC-005-ITEM-0209, SRC-005-ITEM-0210, SRC-005-ITEM-0211, SRC-005-ITEM-0212; domain indexes `VALIDATION, EXECUTION, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0473 — 193. LOAD TEST

- Source: `SRC-006`
- Location: lines 5243–5248; heading `193. LOAD TEST`
- Domain tags: VALIDATION, ROUTING
- Source statement: 193. LOAD TEST: Teste : high event rates
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `193. LOAD TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0208`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0474 — 194. PERFORMANCE TEST

- Source: `SRC-006`
- Location: lines 5249–5251; heading `194. PERFORMANCE TEST`
- Domain tags: VALIDATION, BENCHMARK, CAPITAL
- Source statement: 194. PERFORMANCE TEST: Latence et allocations.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `194. PERFORMANCE TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0209`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0475 — 195. SHADOW TEST

- Source: `SRC-006`
- Location: lines 5252–5254; heading `195. SHADOW TEST`
- Domain tags: VALIDATION
- Source statement: 195. SHADOW TEST: Marché réel sans ordres.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `195. SHADOW TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0210`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0476 — 196. MICRO-LIVE TEST

- Source: `SRC-006`
- Location: lines 5255–5257; heading `196. MICRO-LIVE TEST`
- Domain tags: VALIDATION, CAPITAL
- Source statement: 196. MICRO-LIVE TEST: Petit capital réel.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `196. MICRO-LIVE TEST` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0211`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0477 — 197. CHAOS TESTS

- Source: `SRC-006`
- Location: lines 5258–5263; heading `197. CHAOS TESTS`
- Domain tags: VALIDATION, RISK
- Source statement: 197. CHAOS TESTS: À terme : random network failures
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `197. CHAOS TESTS` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0212`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0478 — 198. Golden Dataset permanent

- Source: `SRC-006`
- Location: lines 5264–5272; heading `198. Golden Dataset permanent`
- Domain tags: VALIDATION, DATA, EXECUTION
- Source statement: 198. Golden Dataset permanent: Doit contenir : normal periods
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `198. Golden Dataset permanent` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0213`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0479 — 199. Golden incidents

- Source: `SRC-006`
- Location: lines 5273–5279; heading `199. Golden incidents`
- Domain tags: VALIDATION, OPERATIONS, INFRA, ACCOUNTING, QUANT
- Source statement: 199. Golden incidents: Conserver des périodes où :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `199. Golden incidents` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0214`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS, INFRA, ACCOUNTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0480 — 200. Dataset diversity

- Source: `SRC-006`
- Location: lines 5280–5284; heading `200. Dataset diversity`
- Domain tags: VALIDATION, DATA
- Source statement: 200. Dataset diversity: Un modèle ne peut être validé uniquement sur :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `200. Dataset diversity` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0215`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0481 — 201. Out-of-sample

- Source: `SRC-006`
- Location: lines 5285–5287; heading `201. Out-of-sample`
- Domain tags: VALIDATION
- Source statement: 201. Out-of-sample: Toute calibration et validation doit être temporellement séparée.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `201. Out-of-sample` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0216`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0482 — 202. Walk-forward

- Source: `SRC-006`
- Location: lines 5288–5290; heading `202. Walk-forward`
- Domain tags: VALIDATION
- Source statement: 202. Walk-forward: Procédure obligatoire pour modèles adaptatifs.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `202. Walk-forward` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0217`; supporting items: SRC-001-ITEM-0059, SRC-007-ITEM-0091; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0483 — 203. No random train/test leakage

- Source: `SRC-006`
- Location: lines 5291–5293; heading `203. No random train/test leakage`
- Domain tags: VALIDATION
- Source statement: 203. No random train/test leakage: Interdit pour séries temporelles.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `203. No random train/test leakage` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0218`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0484 — 204. MARKET REGIME VALIDATION

- Source: `SRC-006`
- Location: lines 5294–5301; heading `204. MARKET REGIME VALIDATION`
- Domain tags: VALIDATION
- Source statement: 204. MARKET REGIME VALIDATION: Tester : normal
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `204. MARKET REGIME VALIDATION` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0219`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0485 — 205. Regime unsupported

- Source: `SRC-006`
- Location: lines 5302–5305; heading `205. Regime unsupported`
- Domain tags: VALIDATION
- Source statement: 205. Regime unsupported: Doit être explicitement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `205. Regime unsupported` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0220`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0486 — 206. STRATEGY VALIDATION — OWA TT

- Source: `SRC-006`
- Location: lines 5306–5316; heading `206. STRATEGY VALIDATION — OWA TT`
- Domain tags: VALIDATION, OWA, EXECUTION, RECOVERY, ACCOUNTING, SURVIVAL, ROUTING
- Source statement: 206. STRATEGY VALIDATION — OWA TT: Avant activation Live : direct comparator correct
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `206. STRATEGY VALIDATION — OWA TT` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0221`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OWA, EXECUTION, RECOVERY, ACCOUNTING, SURVIVAL, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0487 — 207. OWA TT key metrics

- Source: `SRC-006`
- Location: lines 5317–5329; heading `207. OWA TT key metrics`
- Domain tags: VALIDATION, OWA, EXECUTION, RECOVERY, ACCOUNTING, CAPITAL
- Source statement: 207. OWA TT key metrics: opportunities/day gross edge
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `207. OWA TT key metrics` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0222`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OWA, EXECUTION, RECOVERY, ACCOUNTING, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0488 — 208. OWA MT validation

- Source: `SRC-006`
- Location: lines 5330–5337; heading `208. OWA MT validation`
- Domain tags: VALIDATION, OWA, EXECUTION, RECOVERY, MICROSTRUCTURE, MAKER_MODEL
- Source statement: 208. OWA MT validation: En plus : maker fill
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `208. OWA MT validation` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0223`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OWA, EXECUTION, RECOVERY, MICROSTRUCTURE, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0489 — 209. TRIANGLE TTT

- Source: `SRC-006`
- Location: lines 5338–5340; heading `209. TRIANGLE TTT`
- Domain tags: VALIDATION, TRIANGLE
- Source statement: 209. TRIANGLE TTT: Même logique mais trois legs.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `209. TRIANGLE TTT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0224`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0490 — 210. Triangle critical metric

- Source: `SRC-006`
- Location: lines 5341–5345; heading `210. Triangle critical metric`
- Domain tags: VALIDATION, TRIANGLE, RECOVERY, QUANT
- Source statement: 210. Triangle critical metric: probability all legs complete et :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `210. Triangle critical metric` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0225`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, TRIANGLE, RECOVERY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0491 — 211. Triangle MTT

- Source: `SRC-006`
- Location: lines 5346–5348; heading `211. Triangle MTT`
- Domain tags: VALIDATION, TRIANGLE, EXECUTION
- Source statement: 211. Triangle MTT: Maker-specific requirements ajoutés.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `211. Triangle MTT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0226`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, TRIANGLE, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0492 — 212. BRIDGE strategy

- Source: `SRC-006`
- Location: lines 5349–5356; heading `212. BRIDGE strategy`
- Domain tags: VALIDATION, BRIDGE, ACCOUNTING, ROUTING
- Source statement: 212. BRIDGE strategy: Pas classée comme alpha pur.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `212. BRIDGE strategy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0227`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BRIDGE, ACCOUNTING, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0493 — 213. RECOVERY strategy

- Source: `SRC-006`
- Location: lines 5357–5364; heading `213. RECOVERY strategy`
- Domain tags: VALIDATION, RECOVERY, EXECUTION, RISK, ACCOUNTING
- Source statement: 213. RECOVERY strategy: Évaluée principalement par : loss minimized
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `213. RECOVERY strategy` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0228`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, EXECUTION, RISK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0494 — 214. VALIDATION PAR TAILLE

- Source: `SRC-006`
- Location: lines 5365–5374; heading `214. VALIDATION PAR TAILLE`
- Domain tags: VALIDATION, RISK
- Source statement: 214. VALIDATION PAR TAILLE: Chaque stratégie validée par bands :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `214. VALIDATION PAR TAILLE` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0229`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0495 — 215. Une validation à 50 € n’autorise pas 5000 €

- Source: `SRC-006`
- Location: lines 5375–5377; heading `215. Une validation à 50 € n’autorise pas 5000 €`
- Domain tags: VALIDATION, RISK
- Source statement: 215. Une validation à 50 € n’autorise pas 5000 €: Chaque taille a son domaine.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `215. Une validation à 50 € n’autorise pas 5000 €` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0230`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0496 — 216. Size support

- Source: `SRC-006`
- Location: lines 5378–5381; heading `216. Size support`
- Domain tags: VALIDATION
- Source statement: 216. Size support: Un modèle stocke : validated_size_range
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `216. Size support` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0231`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0497 — 217. MARKET SUPPORT

- Source: `SRC-006`
- Location: lines 5382–5388; heading `217. MARKET SUPPORT`
- Domain tags: VALIDATION
- Source statement: 217. MARKET SUPPORT: ne signifie pas automatiquement :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `217. MARKET SUPPORT` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0232`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0498 — 218. Route support

- Source: `SRC-006`
- Location: lines 5389–5395; heading `218. Route support`
- Domain tags: VALIDATION, ROUTING
- Source statement: 218. Route support: Les modèles peuvent avoir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `218. Route support` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0233`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0499 — 219. CALIBRATION REPORT

- Source: `SRC-006`
- Location: lines 5396–5406; heading `219. CALIBRATION REPORT`
- Domain tags: VALIDATION, DATA, ACCOUNTING
- Source statement: 219. CALIBRATION REPORT: Chaque modèle doit produire un document/report contenant :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `219. CALIBRATION REPORT` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0234`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0500 — 220. VALIDATION REPORT

- Source: `SRC-006`
- Location: lines 5407–5417; heading `220. VALIDATION REPORT`
- Domain tags: VALIDATION, RISK, BENCHMARK, REPLAY
- Source statement: 220. VALIDATION REPORT: Avant promotion : model/config
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `220. VALIDATION REPORT` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0235`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, BENCHMARK, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0501 — 221. RELEASE GATE

- Source: `SRC-006`
- Location: lines 5418–5426; heading `221. RELEASE GATE`
- Domain tags: VALIDATION, RISK, DETERMINISM, BENCHMARK, SECURITY, REPLAY, QUANT
- Source statement: 221. RELEASE GATE: Une release stable nécessite : all critical unit tests pass
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `221. RELEASE GATE` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0236`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, DETERMINISM, BENCHMARK, SECURITY, REPLAY, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0502 — 222. If trading logic changed

- Source: `SRC-006`
- Location: lines 5427–5432; heading `222. If trading logic changed`
- Domain tags: VALIDATION
- Source statement: 222. If trading logic changed: Ajout : shadow
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `222. If trading logic changed` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0237`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0503 — 223. If only documentation changed

- Source: `SRC-006`
- Location: lines 5433–5435; heading `223. If only documentation changed`
- Domain tags: VALIDATION
- Source statement: 223. If only documentation changed: Pas besoin.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `223. If only documentation changed` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0238`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0504 — 224. If dependency security patch

- Source: `SRC-006`
- Location: lines 5436–5442; heading `224. If dependency security patch`
- Domain tags: VALIDATION, SECURITY, REPLAY
- Source statement: 224. If dependency security patch: et smoke shadow selon criticité.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `224. If dependency security patch` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0239`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0505 — 225. BUILD GATE

- Source: `SRC-006`
- Location: lines 5443–5449; heading `225. BUILD GATE`
- Domain tags: VALIDATION
- Source statement: 225. BUILD GATE: cargo fmt cargo clippy
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `225. BUILD GATE` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0240`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0506 — 226. Static analysis

- Source: `SRC-006`
- Location: lines 5450–5455; heading `226. Static analysis`
- Domain tags: VALIDATION, SECURITY
- Source statement: 226. Static analysis: Utiliser : clippy
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `226. Static analysis` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0241`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0507 — 227. Unsafe Rust

- Source: `SRC-006`
- Location: lines 5456–5464; heading `227. Unsafe Rust`
- Domain tags: VALIDATION, RISK, ARCH, BENCHMARK
- Source statement: 227. Unsafe Rust: Toute utilisation de : unsafe
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `227. Unsafe Rust` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0242`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, ARCH, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0508 — 228. No unsafe for theoretical speed

- Source: `SRC-006`
- Location: lines 5465–5467; heading `228. No unsafe for theoretical speed`
- Domain tags: VALIDATION, RISK, MICROSTRUCTURE
- Source statement: 228. No unsafe for theoretical speed: Seulement si profiler montre valeur.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `228. No unsafe for theoretical speed` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0243`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0509 — 229. MEMORY SAFETY / LOAD

- Source: `SRC-006`
- Location: lines 5468–5471; heading `229. MEMORY SAFETY / LOAD`
- Domain tags: VALIDATION
- Source statement: 229. MEMORY SAFETY / LOAD: memory should not grow unbounded
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `229. MEMORY SAFETY / LOAD` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0244`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0510 — 230. Leak test

- Source: `SRC-006`
- Location: lines 5472–5474; heading `230. Leak test`
- Domain tags: VALIDATION
- Source statement: 230. Leak test: Mesurer RSS sur plusieurs jours.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `230. Leak test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0245`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0511 — 231. File descriptor leak

- Source: `SRC-006`
- Location: lines 5475–5480; heading `231. File descriptor leak`
- Domain tags: VALIDATION
- Source statement: 231. File descriptor leak: Même chose pour : WS reconnects
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `231. File descriptor leak` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0246`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0512 — 232. CPU runaway

- Source: `SRC-006`
- Location: lines 5481–5485; heading `232. CPU runaway`
- Domain tags: VALIDATION, INFRA, OPERATIONS
- Source statement: 232. CPU runaway: Un incident ne doit pas provoquer :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `232. CPU runaway` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0247`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0513 — 233. BACKPRESSURE

- Source: `SRC-006`
- Location: lines 5486–5489; heading `233. BACKPRESSURE`
- Domain tags: VALIDATION
- Source statement: 233. BACKPRESSURE: Tester : input faster than processing
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `233. BACKPRESSURE` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0248`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0514 — 234. Core event lag

- Source: `SRC-006`
- Location: lines 5490–5527; heading `234. Core event lag`
- Domain tags: VALIDATION, ARCH
- Source statement: 234. Core event lag: Mesurer : ProcessingLag = Now-EventReceiveTime
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `234. Core event lag` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0249`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0515 — 235. Lag threshold

- Source: `SRC-006`
- Location: lines 5528–5531; heading `235. Lag threshold`
- Domain tags: VALIDATION, RISK
- Source statement: 235. Lag threshold: Si trop élevé : new risk off
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `235. Lag threshold` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0250`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0516 — 236. FAILURE MODE VALIDATION

- Source: `SRC-006`
- Location: lines 5532–5538; heading `236. FAILURE MODE VALIDATION`
- Domain tags: VALIDATION
- Source statement: 236. FAILURE MODE VALIDATION: Pour chaque dépendance critique, poser : What if it is late?
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `236. FAILURE MODE VALIDATION` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0251`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0517 — 237. Feed

- Source: `SRC-006`
- Location: lines 5539–5544; heading `237. Feed`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 237. Feed: duplicate malformed
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `237. Feed` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0252`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0518 — 238. Account feed

- Source: `SRC-006`
- Location: lines 5545–5547; heading `238. Account feed`
- Domain tags: VALIDATION, ACCOUNTING
- Source statement: 238. Account feed: Même chose.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `238. Account feed` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0253`; supporting items: SRC-004-ITEM-0086, SRC-005-ITEM-0211; domain indexes `VALIDATION, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0519 — 239. Exchange submit

- Source: `SRC-006`
- Location: lines 5548–5553; heading `239. Exchange submit`
- Domain tags: VALIDATION, EXECUTION
- Source statement: 239. Exchange submit: timeout reject
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `239. Exchange submit` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0254`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0520 — 240. Model

- Source: `SRC-006`
- Location: lines 5554–5559; heading `240. Model`
- Domain tags: VALIDATION
- Source statement: 240. Model: timeout impossible locally invalid version
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `240. Model` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0255`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0521 — 241. Disk

- Source: `SRC-006`
- Location: lines 5560–5564; heading `241. Disk`
- Domain tags: VALIDATION
- Source statement: 241. Disk: corrupt file
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `241. Disk` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0256`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0522 — 242. Clock

- Source: `SRC-006`
- Location: lines 5565–5569; heading `242. Clock`
- Domain tags: VALIDATION, CLOCK
- Source statement: 242. Clock: drift unsynced
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `242. Clock` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0257`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CLOCK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0523 — 243. Config

- Source: `SRC-006`
- Location: lines 5570–5574; heading `243. Config`
- Domain tags: VALIDATION
- Source statement: 243. Config: invalid corrupt
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `243. Config` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0258`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0524 — 244. Docker

- Source: `SRC-006`
- Location: lines 5575–5579; heading `244. Docker`
- Domain tags: VALIDATION, DEPLOYMENT, RISK
- Source statement: 244. Docker: SIGTERM SIGKILL
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `244. Docker` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0259`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0525 — 245. SECURITY VALIDATION

- Source: `SRC-006`
- Location: lines 5580–5587; heading `245. SECURITY VALIDATION`
- Domain tags: VALIDATION, SECURITY, DEPLOYMENT, CLIENT, PRODUCT
- Source statement: 245. SECURITY VALIDATION: Avant distribution client : image scan
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `245. SECURITY VALIDATION` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0260`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY, DEPLOYMENT, CLIENT, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0526 — 246. Secret scanning source repo

- Source: `SRC-006`
- Location: lines 5588–5590; heading `246. Secret scanning source repo`
- Domain tags: VALIDATION, SECURITY
- Source statement: 246. Secret scanning source repo: Éviter clé accidentellement commitée.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `246. Secret scanning source repo` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0261`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0527 — 247. Runtime secret test

- Source: `SRC-006`
- Location: lines 5591–5593; heading `247. Runtime secret test`
- Domain tags: VALIDATION, SECURITY, CLIENT
- Source statement: 247. Runtime secret test: Support bundle ne doit jamais contenir secret.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `247. Runtime secret test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0262`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0528 — 248. Logs secret test

- Source: `SRC-006`
- Location: lines 5594–5596; heading `248. Logs secret test`
- Domain tags: VALIDATION, SECURITY
- Source statement: 248. Logs secret test: Même chose.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `248. Logs secret test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0263`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SECURITY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0529 — 249. Admin API exposure

- Source: `SRC-006`
- Location: lines 5597–5599; heading `249. Admin API exposure`
- Domain tags: VALIDATION, INFRA
- Source statement: 249. Admin API exposure: Scanner VPS pour vérifier ports inattendus.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `249. Admin API exposure` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0264`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0530 — 250. REGRESSION MATRIX

- Source: `SRC-006`
- Location: lines 5600–5610; heading `250. REGRESSION MATRIX`
- Domain tags: VALIDATION, QUANT, RISK, INFRA, ACCOUNTING, REPLAY
- Source statement: 250. REGRESSION MATRIX: Chaque commit critique est comparé à baseline.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `250. REGRESSION MATRIX` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0265`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT, RISK, INFRA, ACCOUNTING, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0531 — 251. A change can improve one metric and fail overall

- Source: `SRC-006`
- Location: lines 5611–5616; heading `251. A change can improve one metric and fail overall`
- Domain tags: VALIDATION, INFRA, BENCHMARK, ACCOUNTING
- Source statement: 251. A change can improve one metric and fail overall: Exemple : PnL +2%
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `251. A change can improve one metric and fail overall` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0266`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, BENCHMARK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0532 — 252. Multi-objective acceptance

- Source: `SRC-006`
- Location: lines 5617–5624; heading `252. Multi-objective acceptance`
- Domain tags: VALIDATION, RISK, BENCHMARK, ACCOUNTING
- Source statement: 252. Multi-objective acceptance: Décision basée sur : economic lift
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `252. Multi-objective acceptance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0267`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, BENCHMARK, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0533 — 253. COMPLEXITY BUDGET

- Source: `SRC-006`
- Location: lines 5625–5632; heading `253. COMPLEXITY BUDGET`
- Domain tags: VALIDATION, OPERATIONS
- Source statement: 253. COMPLEXITY BUDGET: Nouvelle feature doit justifier :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `253. COMPLEXITY BUDGET` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0268`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0534 — 254. Complexity penalty

- Source: `SRC-006`
- Location: lines 5633–5637; heading `254. Complexity penalty`
- Domain tags: VALIDATION, FORMULA
- Source statement: 254. Complexity penalty: Même sans formule exacte :
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `254. Complexity penalty` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0269`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0535 — 255. Technical debt gate

- Source: `SRC-006`
- Location: lines 5638–5642; heading `255. Technical debt gate`
- Domain tags: VALIDATION, ROUTING, HOT_WARM_COLD, ARCH
- Source statement: 255. Technical debt gate: dans hot path Live sans ticket/expiration claire.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `255. Technical debt gate` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0270`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, HOT_WARM_COLD, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0536 — 256. Documentation DoD

- Source: `SRC-006`
- Location: lines 5643–5653; heading `256. Documentation DoD`
- Domain tags: VALIDATION, DATA, ARCH
- Source statement: 256. Documentation DoD: Chaque module critique possède :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `256. Documentation DoD` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0271`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0537 — 257. Code is not documentation

- Source: `SRC-006`
- Location: lines 5654–5656; heading `257. Code is not documentation`
- Domain tags: VALIDATION
- Source statement: 257. Code is not documentation: La spec reste indépendante.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `257. Code is not documentation` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0272`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0538 — 258. IMPLEMENTATION ORDER VALIDATION

- Source: `SRC-006`
- Location: lines 5657–5710; heading `258. IMPLEMENTATION ORDER VALIDATION`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, DATA, ACCOUNTING
- Source statement: 258. IMPLEMENTATION ORDER VALIDATION: Je recommande le développement dans cet ordre : 1. Domain types / schemas
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `258. IMPLEMENTATION ORDER VALIDATION` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0273`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, DATA, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0539 — 259. Pourquoi Recorder très tôt

- Source: `SRC-006`
- Location: lines 5711–5714; heading `259. Pourquoi Recorder très tôt`
- Domain tags: VALIDATION, EXECUTION, RECORDER, DATA
- Source statement: 259. Pourquoi Recorder très tôt: Parce que pendant qu’on code :
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `259. Pourquoi Recorder très tôt` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0274`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECORDER, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0540 — 260. Pourquoi Replay avant stratégie sophistiquée

- Source: `SRC-006`
- Location: lines 5715–5717; heading `260. Pourquoi Replay avant stratégie sophistiquée`
- Domain tags: VALIDATION, REPLAY
- Source statement: 260. Pourquoi Replay avant stratégie sophistiquée: Tout composant suivant doit pouvoir être testé immédiatement sur historique.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `260. Pourquoi Replay avant stratégie sophistiquée` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0275`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0541 — 261. Pourquoi TT avant MT

- Source: `SRC-006`
- Location: lines 5718–5723; heading `261. Pourquoi TT avant MT`
- Domain tags: VALIDATION, EXECUTION, MICROSTRUCTURE, MAKER_MODEL
- Source statement: 261. Pourquoi TT avant MT: TT réduit : queue uncertainty
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `261. Pourquoi TT avant MT` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0276`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, MICROSTRUCTURE, MAKER_MODEL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0542 — 262. Pourquoi OWA/triangle simples avant Participant Models

- Source: `SRC-006`
- Location: lines 5724–5726; heading `262. Pourquoi OWA/triangle simples avant Participant Models`
- Domain tags: VALIDATION, PARTICIPANTS, OWA, TRIANGLE
- Source statement: 262. Pourquoi OWA/triangle simples avant Participant Models: On a besoin d’un baseline mesurable.
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `262. Pourquoi OWA/triangle simples avant Participant Models` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0277`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PARTICIPANTS, OWA, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0543 — 263. NO “BIG BANG”

- Source: `SRC-006`
- Location: lines 5727–5731; heading `263. NO “BIG BANG”`
- Domain tags: VALIDATION, REPLAY, ARCH
- Source statement: 263. NO “BIG BANG”: Ne pas coder : entire architecture
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `263. NO “BIG BANG”` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0278`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0544 — 264. Vertical slices

- Source: `SRC-006`
- Location: lines 5732–5740; heading `264. Vertical slices`
- Domain tags: VALIDATION, SLICING, ACCOUNTING, REPLAY, ROUTING
- Source statement: 264. Vertical slices: Par exemple : → Book
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `264. Vertical slices` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0279`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, SLICING, ACCOUNTING, REPLAY, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0545 — 265. Première milestone

- Source: `SRC-006`
- Location: lines 5741–5743; heading `265. Première milestone`
- Domain tags: VALIDATION, EXECUTION, RECORDER
- Source statement: 265. Première milestone: MARKET RECORDER RUNNING 24/7
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `265. Première milestone` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0280`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0546 — 266. Deuxième milestone

- Source: `SRC-006`
- Location: lines 5744–5746; heading `266. Deuxième milestone`
- Domain tags: VALIDATION, REPLAY
- Source statement: 266. Deuxième milestone: EXACT REPLAY OF BOOKS
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `266. Deuxième milestone` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0281`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0547 — 267. Troisième milestone

- Source: `SRC-006`
- Location: lines 5747–5749; heading `267. Troisième milestone`
- Domain tags: VALIDATION, ACCOUNTING, TRIANGLE
- Source statement: 267. Troisième milestone: 2-leg/3-leg ECONOMICS
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `267. Troisième milestone` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0282`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0548 — 268. Quatrième milestone

- Source: `SRC-006`
- Location: lines 5750–5752; heading `268. Quatrième milestone`
- Domain tags: VALIDATION, EXECUTION, RESEARCH
- Source statement: 268. Quatrième milestone: FULL PAPER EXECUTION STATE MACHINE
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `268. Quatrième milestone` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0283`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0549 — 269. Cinquième milestone

- Source: `SRC-006`
- Location: lines 5753–5755; heading `269. Cinquième milestone`
- Domain tags: VALIDATION
- Source statement: 269. Cinquième milestone: SHADOW 24/7
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `269. Cinquième milestone` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0284`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0550 — 270. Sixième milestone

- Source: `SRC-006`
- Location: lines 5756–5758; heading `270. Sixième milestone`
- Domain tags: VALIDATION
- Source statement: 270. Sixième milestone: MICRO-LIVE TT
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `270. Sixième milestone` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0285`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0551 — 271. Puis intelligence avancée

- Source: `SRC-006`
- Location: lines 5759–5764; heading `271. Puis intelligence avancée`
- Domain tags: VALIDATION, EXECUTION, PARTICIPANTS, SURVIVAL, CAPITAL
- Source statement: 271. Puis intelligence avancée: Survival Participants
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `271. Puis intelligence avancée` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0286`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, PARTICIPANTS, SURVIVAL, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0552 — 272. LIVE CAPITAL LADDER

- Source: `SRC-006`
- Location: lines 5765–5775; heading `272. LIVE CAPITAL LADDER`
- Domain tags: VALIDATION, CAPITAL, SIZING
- Source statement: 272. LIVE CAPITAL LADDER: Exemple conceptuel uniquement : Probe
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `272. LIVE CAPITAL LADDER` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0287`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CAPITAL, SIZING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0553 — 273. Chaque palier

- Source: `SRC-006`
- Location: lines 5776–5782; heading `273. Chaque palier`
- Domain tags: VALIDATION, RISK, OPERATIONS
- Source statement: 273. Chaque palier: Demande : enough sample
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `273. Chaque palier` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0288`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0554 — 274. DOWN-SCALING

- Source: `SRC-006`
- Location: lines 5783–5787; heading `274. DOWN-SCALING`
- Domain tags: VALIDATION, BENCHMARK
- Source statement: 274. DOWN-SCALING: Le moteur doit pouvoir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `274. DOWN-SCALING` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0289`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0555 — 275. Capacity is dynamic

- Source: `SRC-006`
- Location: lines 5788–5805; heading `275. Capacity is dynamic`
- Domain tags: VALIDATION, CAPITAL
- Source statement: 275. Capacity is dynamic: Q_{validated,t} peut :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `275. Capacity is dynamic` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0290`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0556 — 276. MARKET REGIME DOWNGRADE

- Source: `SRC-006`
- Location: lines 5806–5809; heading `276. MARKET REGIME DOWNGRADE`
- Domain tags: VALIDATION
- Source statement: 276. MARKET REGIME DOWNGRADE: Un marché précédemment validé peut devenir :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `276. MARKET REGIME DOWNGRADE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0291`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0557 — 277. Model drift can reduce capital automatically

- Source: `SRC-006`
- Location: lines 5810–5812; heading `277. Model drift can reduce capital automatically`
- Domain tags: VALIDATION, CAPITAL, RISK
- Source statement: 277. Model drift can reduce capital automatically: Dans les limites prévues.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `277. Model drift can reduce capital automatically` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0292`; supporting items: SRC-007-ITEM-0099; domain indexes `VALIDATION, CAPITAL, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0558 — 278. Promotion vs demotion

- Source: `SRC-006`
- Location: lines 5813–5817; heading `278. Promotion vs demotion`
- Domain tags: VALIDATION
- Source statement: 278. Promotion vs demotion: Tous les objets évolutifs doivent supporter :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `278. Promotion vs demotion` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0293`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0559 — 279. Strategy status

- Source: `SRC-006`
- Location: lines 5818–5824; heading `279. Strategy status`
- Domain tags: VALIDATION, RESEARCH
- Source statement: 279. Strategy status: Research Shadow
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `279. Strategy status` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0294`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0560 — 280. Market status interne

- Source: `SRC-006`
- Location: lines 5825–5830; heading `280. Market status interne`
- Domain tags: VALIDATION, RISK
- Source statement: 280. Market status interne: Supported Limited
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `280. Market status interne` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0295`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0561 — 281. Model status

- Source: `SRC-006`
- Location: lines 5831–5836; heading `281. Model status`
- Domain tags: VALIDATION, FUTURE
- Source statement: 281. Model status: Challenger Champion
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `281. Model status` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0296`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0562 — 282. Infrastructure status

- Source: `SRC-006`
- Location: lines 5837–5841; heading `282. Infrastructure status`
- Domain tags: VALIDATION, INFRA
- Source statement: 282. Infrastructure status: Validated Degraded
- Nature: rejected approach
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `282. Infrastructure status` as a distinct rejected approach requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `REJECTED`
- Cross-source references: `REQ-VALID-0297`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0563 — 283. CLIENT RELEASE VALIDATION

- Source: `SRC-006`
- Location: lines 5842–5846; heading `283. CLIENT RELEASE VALIDATION`
- Domain tags: VALIDATION, CLIENT, RESEARCH
- Source statement: 283. CLIENT RELEASE VALIDATION: Une release client ne doit pas exposer une stratégie :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `283. CLIENT RELEASE VALIDATION` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0298`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CLIENT, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0564 — 284. Feature flags

- Source: `SRC-006`
- Location: lines 5847–5850; heading `284. Feature flags`
- Domain tags: VALIDATION
- Source statement: 284. Feature flags: Chaque stratégie expérimentale derrière :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `284. Feature flags` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0299`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0565 — 285. Default production config

- Source: `SRC-006`
- Location: lines 5851–5854; heading `285. Default production config`
- Domain tags: VALIDATION, PRODUCT
- Source statement: 285. Default production config: Doit activer uniquement : validated features
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `285. Default production config` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0300`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0566 — 286. Default = conservative

- Source: `SRC-006`
- Location: lines 5855–5858; heading `286. Default = conservative`
- Domain tags: VALIDATION
- Source statement: 286. Default = conservative: Jamais : all experimental models enabled
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `286. Default = conservative` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0301`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0567 — 287. CLIENT VPS VALIDATION

- Source: `SRC-006`
- Location: lines 5859–5868; heading `287. CLIENT VPS VALIDATION`
- Domain tags: VALIDATION, INFRA, CLIENT, CLOCK, BENCHMARK, DEPLOYMENT
- Source statement: 287. CLIENT VPS VALIDATION: Avant Live : infra benchmark
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `287. CLIENT VPS VALIDATION` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0302`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, CLIENT, CLOCK, BENCHMARK, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0568 — 288. Minimum profile not met

- Source: `SRC-006`
- Location: lines 5869–5871; heading `288. Minimum profile not met`
- Domain tags: VALIDATION, MICROSTRUCTURE
- Source statement: 288. Minimum profile not met: Live disabled
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `288. Minimum profile not met` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0303`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0569 — 289. Different VPS → revalidation

- Source: `SRC-006`
- Location: lines 5872–5876; heading `289. Different VPS → revalidation`
- Domain tags: VALIDATION, INFRA, BENCHMARK, CLIENT
- Source statement: 289. Different VPS → revalidation: au minimum benchmark rapide requis.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `289. Different VPS → revalidation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0304`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, BENCHMARK, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0570 — 290. Different region

- Source: `SRC-006`
- Location: lines 5877–5880; heading `290. Different region`
- Domain tags: VALIDATION, INFRA, BENCHMARK
- Source statement: 290. Different region: Tokyo → autre région :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `290. Different region` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0305`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0571 — 291. INFRA UPGRADE VALIDATION

- Source: `SRC-006`
- Location: lines 5881–5883; heading `291. INFRA UPGRADE VALIDATION`
- Domain tags: VALIDATION, INFRA
- Source statement: 291. INFRA UPGRADE VALIDATION: Candidate runs shadow in parallel.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `291. INFRA UPGRADE VALIDATION` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0306`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0572 — 292. Compare same events

- Source: `SRC-006`
- Location: lines 5884–5890; heading `292. Compare same events`
- Domain tags: VALIDATION, BENCHMARK, OPERATIONS, ACCOUNTING, SIMULATOR
- Source statement: 292. Compare same events: Mesurer : first arrival
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `292. Compare same events` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0307`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK, OPERATIONS, ACCOUNTING, SIMULATOR`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0573 — 293. Upgrade decision

- Source: `SRC-006`
- Location: lines 5891–5914; heading `293. Upgrade decision`
- Domain tags: VALIDATION
- Source statement: 293. Upgrade decision: Pas juste : faster
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `293. Upgrade decision` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0308`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0574 — 294. SYSTEM-WIDE VALIDATION

- Source: `SRC-006`
- Location: lines 5915–5935; heading `294. SYSTEM-WIDE VALIDATION`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, RECONCILIATION, RISK, ACCOUNTING, PRODUCT
- Source statement: 294. SYSTEM-WIDE VALIDATION: Avant première vraie mise en production : effectuer une simulation complète :
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `294. SYSTEM-WIDE VALIDATION` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0309`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECOVERY, RECONCILIATION, RISK, ACCOUNTING, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0575 — 295. End-to-end test

- Source: `SRC-006`
- Location: lines 5936–5938; heading `295. End-to-end test`
- Domain tags: VALIDATION
- Source statement: 295. End-to-end test: Automatisé.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `295. End-to-end test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0310`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0576 — 296. End-to-end fault test

- Source: `SRC-006`
- Location: lines 5939–5942; heading `296. End-to-end fault test`
- Domain tags: VALIDATION
- Source statement: 296. End-to-end fault test: Même scénario avec : lost response
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `296. End-to-end fault test` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0311`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0577 — 297. End-to-end crash test

- Source: `SRC-006`
- Location: lines 5943–5948; heading `297. End-to-end crash test`
- Domain tags: VALIDATION, OPERATIONS, RECONCILIATION
- Source statement: 297. End-to-end crash test: Crash entre Leg1 et Leg2.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `297. End-to-end crash test` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0312`; supporting items: SRC-004-ITEM-0122; domain indexes `VALIDATION, OPERATIONS, RECONCILIATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0578 — 298. End-to-end feed failure

- Source: `SRC-006`
- Location: lines 5949–5951; heading `298. End-to-end feed failure`
- Domain tags: VALIDATION, ACCOUNTING, EXECUTION
- Source statement: 298. End-to-end feed failure: Feed dies while maker rests.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `298. End-to-end feed failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0313`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, EXECUTION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0579 — 299. End-to-end disk failure

- Source: `SRC-006`
- Location: lines 5952–5954; heading `299. End-to-end disk failure`
- Domain tags: VALIDATION, EXECUTION, RECORDER
- Source statement: 299. End-to-end disk failure: Recorder disk full during live-style simulation.
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `299. End-to-end disk failure` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0314`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECORDER`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0580 — 300. End-to-end config update

- Source: `SRC-006`
- Location: lines 5955–5957; heading `300. End-to-end config update`
- Domain tags: VALIDATION, DEPLOYMENT, RISK
- Source statement: 300. End-to-end config update: Risk config changed safely.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `300. End-to-end config update` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0315`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0581 — 301. ACCEPTANCE MATRIX — CORE

- Source: `SRC-006`
- Location: lines 5958–5975; heading `301. ACCEPTANCE MATRIX — CORE`
- Domain tags: VALIDATION, ARCH, RECOVERY, RECONCILIATION, RISK, ACCOUNTING, SIMULATOR, REPLAY
- Source statement: 301. ACCEPTANCE MATRIX — CORE: Module | Unit | Golden | Replay | Fault | Perf | Shadow | Micro-live Feed | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | —
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `301. ACCEPTANCE MATRIX — CORE` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0316`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH, RECOVERY, RECONCILIATION, RISK, ACCOUNTING, SIMULATOR, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0582 — 302. RELEASE BLOCKERS

- Source: `SRC-006`
- Location: lines 5976–5985; heading `302. RELEASE BLOCKERS`
- Domain tags: VALIDATION, EXECUTION, RECONCILIATION, RISK, DETERMINISM, SECURITY, OPERATIONS, REPLAY
- Source statement: 302. RELEASE BLOCKERS: Release impossible si : critical unit failure
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `302. RELEASE BLOCKERS` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0317`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, RECONCILIATION, RISK, DETERMINISM, SECURITY, OPERATIONS, REPLAY`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0583 — 303. MICRO-LIVE BLOCKERS

- Source: `SRC-006`
- Location: lines 5986–5993; heading `303. MICRO-LIVE BLOCKERS`
- Domain tags: VALIDATION, EXECUTION, RECOVERY, ACCOUNTING
- Source statement: 303. MICRO-LIVE BLOCKERS: Impossible si : shadow instability
- Nature: edge-case/failure behaviour
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `303. MICRO-LIVE BLOCKERS` as a distinct edge-case/failure behaviour requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0318`; supporting items: SRC-001-ITEM-0018, SRC-005-ITEM-0481; domain indexes `VALIDATION, EXECUTION, RECOVERY, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0584 — 304. SCALING BLOCKERS

- Source: `SRC-006`
- Location: lines 5994–6002; heading `304. SCALING BLOCKERS`
- Domain tags: VALIDATION, RECOVERY, RISK, INFRA
- Source statement: 304. SCALING BLOCKERS: Impossible si : prediction error rising
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `304. SCALING BLOCKERS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0319`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0585 — 305. LIVE AUTO-DOWNGRADE TRIGGERS

- Source: `SRC-006`
- Location: lines 6003–6010; heading `305. LIVE AUTO-DOWNGRADE TRIGGERS`
- Domain tags: VALIDATION, RECOVERY, RISK, INFRA
- Source statement: 305. LIVE AUTO-DOWNGRADE TRIGGERS: Exemples : model drift
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `305. LIVE AUTO-DOWNGRADE TRIGGERS` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0320`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECOVERY, RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0586 — 306. Validation is continuous

- Source: `SRC-006`
- Location: lines 6011–6016; heading `306. Validation is continuous`
- Domain tags: VALIDATION
- Source statement: 306. Validation is continuous: Même après Live : every trade
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `306. Validation is continuous` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0321`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0587 — 307. Production feedback loop

- Source: `SRC-006`
- Location: lines 6017–6031; heading `307. Production feedback loop`
- Domain tags: VALIDATION, ACCOUNTING, PRODUCT, EXECUTION, DEPLOYMENT
- Source statement: 307. Production feedback loop: PREDICT EXECUTE
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `307. Production feedback loop` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0322`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, PRODUCT, EXECUTION, DEPLOYMENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0588 — 308. No direct self-learning in production

- Source: `SRC-006`
- Location: lines 6032–6036; heading `308. No direct self-learning in production`
- Domain tags: VALIDATION, PRODUCT, RESEARCH
- Source statement: 308. No direct self-learning in production: Production collecte. Research recalibre.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `308. No direct self-learning in production` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0323`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0589 — 309. Monthly / periodic validation

- Source: `SRC-006`
- Location: lines 6037–6045; heading `309. Monthly / periodic validation`
- Domain tags: VALIDATION, RISK, INFRA, OPERATIONS
- Source statement: 309. Monthly / periodic validation: Périodiquement : strategy health
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `309. Monthly / periodic validation` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0324`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, INFRA, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0590 — 310. But no arbitrary calendar dependence

- Source: `SRC-006`
- Location: lines 6046–6050; heading `310. But no arbitrary calendar dependence`
- Domain tags: VALIDATION
- Source statement: 310. But no arbitrary calendar dependence: Si drift apparaît aujourd’hui :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `310. But no arbitrary calendar dependence` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0325`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0591 — 311. Validation Dashboard

- Source: `SRC-006`
- Location: lines 6051–6058; heading `311. Validation Dashboard`
- Domain tags: VALIDATION
- Source statement: 311. Validation Dashboard: Doit pouvoir répondre : What is currently validated?
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `311. Validation Dashboard` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0326`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: YES.

### SRC-006-ITEM-0592 — 312. ValidatedCapability

- Source: `SRC-006`
- Location: lines 6059–6076; heading `312. ValidatedCapability`
- Domain tags: VALIDATION, PRODUCT
- Source statement: 312. ValidatedCapability: Structure conceptuelle : ValidatedCapability {
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `312. ValidatedCapability` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0327`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0593 — 313. This is important commercially

- Source: `SRC-006`
- Location: lines 6077–6082; heading `313. This is important commercially`
- Domain tags: VALIDATION, PRODUCT, CLIENT
- Source statement: 313. This is important commercially: Le client ne doit pas recevoir implicitement : everything the code can technically do
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `313. This is important commercially` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0328`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT, CLIENT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0594 — 314. Feature capability manifest

- Source: `SRC-006`
- Location: lines 6083–6086; heading `314. Feature capability manifest`
- Domain tags: VALIDATION, DATA
- Source statement: 314. Feature capability manifest: Chaque release contient : CapabilityManifest
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `314. Feature capability manifest` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0329`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DATA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0595 — 315. Example

- Source: `SRC-006`
- Location: lines 6087–6099; heading `315. Example`
- Domain tags: VALIDATION, TRIANGLE
- Source statement: 315. Example: OWA_TT status = LIVE_VALIDATED
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `315. Example` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0330`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, TRIANGLE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0596 — 316. Code support ≠ production support

- Source: `SRC-006`
- Location: lines 6100–6102; heading `316. Code support ≠ production support`
- Domain tags: VALIDATION, PRODUCT
- Source statement: 316. Code support ≠ production support: Très important.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `316. Code support ≠ production support` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0331`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0597 — 317. Research archive

- Source: `SRC-006`
- Location: lines 6103–6109; heading `317. Research archive`
- Domain tags: VALIDATION, RECORDER, RESEARCH
- Source statement: 317. Research archive: Toutes les décisions de validation importantes :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `317. Research archive` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0332`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RECORDER, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0598 — 318. Negative results matter

- Source: `SRC-006`
- Location: lines 6110–6114; heading `318. Negative results matter`
- Domain tags: VALIDATION, ACCOUNTING, QUANT
- Source statement: 318. Negative results matter: on conserve ce résultat pour ne pas refaire la même expérience.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `318. Negative results matter` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0333`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0599 — 319. Architecture Decision Records

- Source: `SRC-006`
- Location: lines 6115–6118; heading `319. Architecture Decision Records`
- Domain tags: VALIDATION, ARCH
- Source statement: 319. Architecture Decision Records: Pour décisions structurelles :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `319. Architecture Decision Records` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0334`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0600 — 320. Example ADRs

- Source: `SRC-006`
- Location: lines 6119–6125; heading `320. Example ADRs`
- Domain tags: VALIDATION, DEPLOYMENT, CLIENT, REPLAY, PRODUCT, ARCH
- Source statement: 320. Example ADRs: ADR-002 Replay == Live core ADR-003 One container per client
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `320. Example ADRs` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0335`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, CLIENT, REPLAY, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0601 — 321. Why ADR

- Source: `SRC-006`
- Location: lines 6126–6130; heading `321. Why ADR`
- Domain tags: VALIDATION, ARCH
- Source statement: 321. Why ADR: Quand Codex ou un futur développeur demande : pourquoi ne pas tout refaire en Python ?
- Nature: rationale
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `321. Why ADR` as a distinct rationale requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0336`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0602 — 322. Spec hierarchy

- Source: `SRC-006`
- Location: lines 6131–6143; heading `322. Spec hierarchy`
- Domain tags: VALIDATION, RISK, DEPLOYMENT, ARCH
- Source statement: 322. Spec hierarchy: Documentation finale devrait avoir :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `322. Spec hierarchy` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0337`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, DEPLOYMENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0603 — 323. Priority if conflict

- Source: `SRC-006`
- Location: lines 6144–6155; heading `323. Priority if conflict`
- Domain tags: VALIDATION, RISK, DATA, ARCH
- Source statement: 323. Priority if conflict: En cas de contradiction :
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `323. Priority if conflict` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0338`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, DATA, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0604 — 324. Formula conflict

- Source: `SRC-006`
- Location: lines 6156–6158; heading `324. Formula conflict`
- Domain tags: VALIDATION, FORMULA
- Source statement: 324. Formula conflict: Formula Book fait autorité pour les équations.
- Nature: formula/definition
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `324. Formula conflict` as a distinct formula/definition requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0339`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, FORMULA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0605 — 325. Exchange rule conflict

- Source: `SRC-006`
- Location: lines 6159–6162; heading `325. Exchange rule conflict`
- Domain tags: VALIDATION
- Source statement: 325. Exchange rule conflict: Current verified exchange rule gagne. Puis documentation/spec mise à jour.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `325. Exchange rule conflict` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0340`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0606 — 326. Spec update process

- Source: `SRC-006`
- Location: lines 6163–6169; heading `326. Spec update process`
- Domain tags: VALIDATION, DEPLOYMENT, QUANT, ARCH
- Source statement: 326. Spec update process: Une modification importante nécessite :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `326. Spec update process` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0341`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, DEPLOYMENT, QUANT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0607 — 327. No silent architecture drift

- Source: `SRC-006`
- Location: lines 6170–6174; heading `327. No silent architecture drift`
- Domain tags: VALIDATION, ARCH
- Source statement: 327. No silent architecture drift: Codex ne doit pas pouvoir : sans signaler divergence de spec.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `327. No silent architecture drift` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0342`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0608 — 328. Codex implementation rule

- Source: `SRC-006`
- Location: lines 6175–6181; heading `328. Codex implementation rule`
- Domain tags: VALIDATION, ARCH
- Source statement: 328. Codex implementation rule: Si spec ambiguë : do not invent architecture
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `328. Codex implementation rule` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0343`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0609 — 329. But implementation details can be optimized

- Source: `SRC-006`
- Location: lines 6182–6192; heading `329. But implementation details can be optimized`
- Domain tags: VALIDATION, RISK, BENCHMARK
- Source statement: 329. But implementation details can be optimized: Codex peut choisir : data structure
- Nature: data/architecture contract
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `329. But implementation details can be optimized` as a distinct data/architecture contract requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0344`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0610 — 330. Test-first for critical modules

- Source: `SRC-006`
- Location: lines 6193–6201; heading `330. Test-first for critical modules`
- Domain tags: VALIDATION, ARCH, RECOVERY, RECONCILIATION, RISK, ROUTING
- Source statement: 330. Test-first for critical modules: écrire les golden/invariant tests avant ou simultanément au code.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `330. Test-first for critical modules` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0345`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH, RECOVERY, RECONCILIATION, RISK, ROUTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0611 — 331. Benchmark-before-optimization

- Source: `SRC-006`
- Location: lines 6202–6211; heading `331. Benchmark-before-optimization`
- Domain tags: VALIDATION, BENCHMARK
- Source statement: 331. Benchmark-before-optimization: Règle : measure
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `331. Benchmark-before-optimization` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0346`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, BENCHMARK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0612 — 332. No optimization by aesthetic preference

- Source: `SRC-006`
- Location: lines 6212–6219; heading `332. No optimization by aesthetic preference`
- Domain tags: VALIDATION, RISK, MICROSTRUCTURE
- Source statement: 332. No optimization by aesthetic preference: Pas de : lock-free
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `332. No optimization by aesthetic preference` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0347`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0613 — 333. No model complexity by prestige

- Source: `SRC-006`
- Location: lines 6220–6222; heading `333. No model complexity by prestige`
- Domain tags: VALIDATION
- Source statement: 333. No model complexity by prestige: Même logique.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `333. No model complexity by prestige` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0348`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0614 — 334. Final production criteria

- Source: `SRC-006`
- Location: lines 6223–6248; heading `334. Final production criteria`
- Domain tags: VALIDATION, PRODUCT, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, DETERMINISM
- Source statement: 334. Final production criteria: Le bot peut être considéré prêt pour première exploitation réelle sérieuse quand : Capital scaling constrained by validated capacity
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `334. Final production criteria` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `CALIBRATED`
- Cross-source references: `REQ-VALID-0349`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT, EXECUTION, RECOVERY, RECONCILIATION, RISK, RECORDER, DETERMINISM`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0615 — 335. What “ready” does NOT require

- Source: `SRC-006`
- Location: lines 6249–6262; heading `335. What “ready” does NOT require`
- Domain tags: VALIDATION, EXECUTION, QUANT, CROSS_EXCHANGE
- Source statement: 335. What “ready” does NOT require: Il n’est pas nécessaire que :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `335. What “ready” does NOT require` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0350`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, EXECUTION, QUANT, CROSS_EXCHANGE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0616 — 336. Final architecture can exist before all features active

- Source: `SRC-006`
- Location: lines 6263–6269; heading `336. Final architecture can exist before all features active`
- Domain tags: VALIDATION, ARCH, PRODUCT
- Source statement: 336. Final architecture can exist before all features active: Très important. V1 architecture :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `336. Final architecture can exist before all features active` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0351`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH, PRODUCT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0617 — 337. Validation is the feature gate

- Source: `SRC-006`
- Location: lines 6270–6278; heading `337. Validation is the feature gate`
- Domain tags: VALIDATION, ARCH, RESEARCH
- Source statement: 337. Validation is the feature gate: Pas besoin de réécrire architecture.
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `337. Validation is the feature gate` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `RESEARCH`
- Cross-source references: `REQ-VALID-0352`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ARCH, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: YES
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0618 — 338. Master rule

- Source: `SRC-006`
- Location: lines 6279–6284; heading `338. Master rule`
- Domain tags: VALIDATION
- Source statement: 338. Master rule: Une feature n’entre jamais en Live parce qu’elle :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `338. Master rule` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0353`; supporting items: none found by conservative heading match; domain indexes `VALIDATION`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0619 — 339. Economic acceptance

- Source: `SRC-006`
- Location: lines 6285–6303; heading `339. Economic acceptance`
- Domain tags: VALIDATION, ACCOUNTING, RISK, INFRA
- Source statement: 339. Economic acceptance: À terme, une feature doit répondre :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `339. Economic acceptance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0354`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ACCOUNTING, RISK, INFRA`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0620 — 340. Risk acceptance

- Source: `SRC-006`
- Location: lines 6304–6330; heading `340. Risk acceptance`
- Domain tags: VALIDATION, RISK
- Source statement: 340. Risk acceptance: Et simultanément : TailRisk \leq ValidatedLimit
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `340. Risk acceptance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0355`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0621 — 341. Calibration acceptance

- Source: `SRC-006`
- Location: lines 6331–6334; heading `341. Calibration acceptance`
- Domain tags: VALIDATION, QUANT
- Source statement: 341. Calibration acceptance: predicted probabilities ≈ observed probabilities
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `341. Calibration acceptance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0356`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0622 — 342. Operational acceptance

- Source: `SRC-006`
- Location: lines 6335–6338; heading `342. Operational acceptance`
- Domain tags: VALIDATION, OPERATIONS
- Source statement: 342. Operational acceptance: does not materially degrade stability
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `342. Operational acceptance` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0357`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, OPERATIONS`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0623 — 343. Therefore

- Source: `SRC-006`
- Location: lines 6339–6430; heading `343. Therefore`
- Domain tags: VALIDATION, RISK, OPERATIONS, ACCOUNTING
- Source statement: 343. Therefore: Une nouvelle feature passe Live seulement si :
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `343. Therefore` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0358`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, OPERATIONS, ACCOUNTING`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0624 — 344. Final lifecycle

- Source: `SRC-006`
- Location: lines 6431–6457; heading `344. Final lifecycle`
- Domain tags: VALIDATION, ROUTING, OPERATIONS, REPLAY, FUTURE
- Source statement: 344. Final lifecycle: IMPLEMENT REPLAY
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `344. Final lifecycle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0359`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, ROUTING, OPERATIONS, REPLAY, FUTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0625 — 345. Final project principle

- Source: `SRC-006`
- Location: lines 6458–6464; heading `345. Final project principle`
- Domain tags: VALIDATION, RISK, ACCOUNTING, MICROSTRUCTURE
- Source statement: 345. Final project principle: Le système doit préférer : pendant les phases où l’incertitude est forte.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `345. Final project principle` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0360`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, ACCOUNTING, MICROSTRUCTURE`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0626 — 346. But validation must not become paralysis

- Source: `SRC-006`
- Location: lines 6465–6474; heading `346. But validation must not become paralysis`
- Domain tags: VALIDATION, QUANT
- Source statement: 346. But validation must not become paralysis: L’objectif n’est pas : never trade until perfect
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `346. But validation must not become paralysis` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0361`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, QUANT`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0627 — 347. Final scientific loop

- Source: `SRC-006`
- Location: lines 6475–6562; heading `347. Final scientific loop`
- Domain tags: VALIDATION, PRODUCT, RESEARCH
- Source statement: 347. Final scientific loop: Hypothesis \rightarrow Measurement \rightarrow Experiment \rightarrow Evidence \rightarrow Decision Hypothesis \rightarrow Assumption \rightarrow Production
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `347. Final scientific loop` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0362`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, PRODUCT, RESEARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0628 — 348. Final Definition of Done — PROJECT

- Source: `SRC-006`
- Location: lines 6563–6580; heading `348. Final Definition of Done — PROJECT`
- Domain tags: VALIDATION, FORMULA, EXECUTION, RISK, DATA, DEPLOYMENT, ARCH
- Source statement: 348. Final Definition of Done — PROJECT: La phase d’architecture/specification est terminée lorsque :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `348. Final Definition of Done — PROJECT` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0363`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, FORMULA, EXECUTION, RISK, DATA, DEPLOYMENT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0629 — 349. La phase de développement est terminée lorsque

- Source: `SRC-006`
- Location: lines 6581–6595; heading `349. La phase de développement est terminée lorsque`
- Domain tags: VALIDATION, RISK, DETERMINISM, DEPLOYMENT, REPLAY, CAPITAL, PRODUCT, ARCH
- Source statement: 349. La phase de développement est terminée lorsque: all production-critical modules reach required maturity
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `349. La phase de développement est terminée lorsque` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0364`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, DETERMINISM, DEPLOYMENT, REPLAY, CAPITAL, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0630 — 350. Principe final

- Source: `SRC-006`
- Location: lines 6596–6672; heading `350. Principe final`
- Domain tags: VALIDATION, CAPITAL
- Source statement: 350. Principe final: \boxed{ Specification \rightarrow Implementation \rightarrow Evidence \rightarrow Capital } \boxed{ Implementation \rightarrow Capital \rightarrow Hope }
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `350. Principe final` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0365`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0631 — 351. Règle définitive de scaling

- Source: `SRC-006`
- Location: lines 6673–6743; heading `351. Règle définitive de scaling`
- Domain tags: VALIDATION, RISK, INFRA, DEPLOYMENT, INVENTORY, CAPITAL
- Source statement: 351. Règle définitive de scaling: Le capital maximum autorisé à un instant pas par le capital total disponible.
- Nature: decision/policy/concept
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `351. Règle définitive de scaling` as a distinct decision/policy/concept requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0366`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, INFRA, DEPLOYMENT, INVENTORY, CAPITAL`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

### SRC-006-ITEM-0632 — 352. Conclusion

- Source: `SRC-006`
- Location: lines 6744–6903; heading `352. Conclusion`
- Domain tags: VALIDATION, RISK, DETERMINISM, DEPLOYMENT, CAPITAL, PRODUCT, ARCH
- Source statement: 352. Conclusion: Ce dernier dossier transforme toute notre architecture en un système réellement gouvernable. Chaque composant doit maintenant pouvoir répondre à :
- Nature: protocol/validation
- Temporal interpretation: closure
- Authority: Closure authority for Deployment/Security/Client Distribution and M0–M5 validation.
- Candidate canonical interpretation: Preserve `352. Conclusion` as a distinct protocol/validation requirement; apply closure authority and domain-pass terminology before promotion.
- Candidate status: `LOCKED`
- Cross-source references: `REQ-VALID-0367`; supporting items: none found by conservative heading match; domain indexes `VALIDATION, RISK, DETERMINISM, DEPLOYMENT, CAPITAL, PRODUCT, ARCH`.
- Potential conflicts: None identified at extraction stage; cross-source register controls conflicts.
- Needs domain-pass review: NO
- Notes: Formula refs: none; external revalidation: NO.

## SOURCE COMPLETION CHECK

- Sections/headings reviewed: 629
- Requirements contributed: 629
- Supporting references contributed: 104 (conservative heading match; semantic merge remains a domain-pass task)
- Superseded items: 0
- Research items: 7
- Open items: 1
- External revalidation items: 2
- Unclassified material: 0 (non-heading prose is attached to its enclosing extraction unit; conversational filler has no design status).
