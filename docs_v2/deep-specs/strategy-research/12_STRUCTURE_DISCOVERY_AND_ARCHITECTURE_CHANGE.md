# 12 — Structure Discovery and Architecture Change

`DOCUMENTATION STATUS: F2 PART 2 / INTERMEDIATE DOCUMENTARY WORK / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE PROPOSAL MECHANISM / NOT ACTIVE`

A Strategy is not an Economic Structure. Structure Discovery is a future documentary mechanism for
proposing an economic mechanism that canonical Direct/OWA/Triangle—or later separately approved
Bridge—cannot faithfully represent. It does not create a live route type or authorize a Core
change.

## 1. Representation test

Ordinary q/threshold changes, a new parameter region, a filter, feature, regime restriction,
priority proposal or execution-mode choice remain within Configuration/Strategy lineage. They are
not new Structures. A proposal crosses the Structure boundary only when the economic mechanism,
required graph representation or comparator/accounting semantics cannot be expressed faithfully
under current canonical contracts.

### D10 — New Structure Discovery and Architecture Review

```text
RESEARCH OBSERVATION / HYP-* PROPOSAL
                  |
                  v
     CAN AN EXISTING STRUCTURE REPRESENT IT?
             +----+----+
             |         |
            YES        NO / UNCERTAIN
             |         |
             v         v
     Strategy Hypothesis     StructureHypothesis
     / version lineage       documentary proposal only
                                   |
                                   v
                      HUMAN ARCHITECTURE REVIEW
                                   |
                  +----------------+----------------+
                  |                                 |
                  v                                 v
          reject / narrow / defer          identify impacts owned by:
                                      Formula / Graph / Data / Risk / ESM
                                      Inventory / Recovery / Accounting
                                                      |
                                                      v
                                   separately authorized specification
                                                      |
                                                      v
                                     later implementation + validation
                                                      |
                                                      v
                                      Falsifier support (not approval)
```

Read top-to-bottom: the representation test keeps normal strategy changes in strategy lineage; only
an unrepresentable mechanism becomes a proposal, which must pass human Architecture Review and
separate owner specifications before any implementation.

Contract — **Inputs:** observation, existing `HYP-*`, mechanism/comparator explanation and current
canonical Structure contracts. **Operations:** representation test, cross-owner impact analysis,
human Architecture Review and, only if authorized later, separate specification/implementation/
validation. **Outputs:** strategy hypothesis, rejected/deferred proposal or documentary
`StructureHypothesis`; never a live route. **Canonical authority:** Graph, Formula, Data, Risk,
ESM, Inventory, Recovery and Accounting each retain their domain; humans own architecture
approval. **Failure/uncertainty:** incomplete facts, unclear comparator or unresolved owner impact
stays `to_review`/deferred; no automatic classification or Core mutation. **Activation timing:**
proposal documentation may exist later; integration requires separate governance, authorization,
implementation and Falsifier evidence.

## 2. Required StructureHypothesis record

A proposal links an existing `HYP-*` and records:

- proposed economic mechanism and expected source of edge;
- why Direct/OWA/Triangle/later Bridge plus existing strategy policy cannot represent it;
- required assets, legs, topology and fair comparator;
- structural route, economic class, execution mode and accounting/capital intent separately;
- Formula and exact-once cost-ownership impact;
- Graph/routing and point-in-time Data/feed requirements;
- fee, precision, metadata, external rules and validity/retrieval dates;
- possible execution modes and capability prerequisites;
- Risk, Inventory, Reservations, Recovery, Reconciliation and Accounting implications;
- partial/zero/failure/UNKNOWN states and conservative fallback;
- Simulator/Replay/Falsifier needs and evidence capable of refuting the claim;
- security, infrastructure and operational effects;
- affected canonical documents/owners, unresolved conflicts and explicit human decisions;
- author, reviewer, lineage, evidence links, immutable artifacts/hashes and status.

`StructureHypothesis` is a record type, not a new runtime ID namespace in this prompt. Final
serialization, identifier policy and status vocabulary are `HUMAN_DECISION_REQUIRED`; safe default
is an `HYP-*`-linked proposal marked draft/to-review with no Core representation.

## 3. Review dispositions and authority

Human Architecture Review may `REJECT`, `NARROW`, `DEFER`, `REQUEST_EVIDENCE` or declare the
proposal eligible for separately scoped specification. “Eligible for specification” is not
architecture approval, implementation authorization or capability permission.

Any accepted future architecture change must identify, without silently editing:

1. canonical Graph/type/topology changes;
2. Formula/comparator/cost ownership and QF implications;
3. Data/Recorder/Replay schemas, clocks, ordering and historical admissibility;
4. Simulator scenario/fidelity impact;
5. Risk hard gates and failure containment;
6. ESM/transport/order-state implications;
7. Inventory/Reservations/Recovery/Reconciliation/Accounting truth;
8. security, keys, infrastructure and Operations;
9. Validation M0–M5, evidence stages, rollback and authorization;
10. roadmap/governance impact.

Each domain owner must approve its own future specification. Research or AI cannot change QF,
Formula, Risk, ESM, Graph, accounting, `Q_validated`, capital or live configuration. A
`StructureHypothesis` cannot be fed directly to code generation or execution.

## 4. Evidence and lifecycle

Pre-architecture evidence may demonstrate that the observation is reproducible and that existing
representations are inadequate. It cannot claim executable economics under a mechanism the Core
cannot yet represent. Current exchange/API/feed facts remain dated external facts and require
primary-source revalidation before a consuming specification.

If a Structure is separately specified and implemented later, it still begins without maturity.
It must pass its own formula/schema/golden/property tests, Data/Replay support, Simulator and
Falsifier evidence, Risk/ESM/Recovery validation, Shadow, separately authorized actual evidence and
human capability progression. Positive Falsifier evidence cannot retroactively approve the
architecture.

All rejected, superseded and failed proposals remain in lineage so the same unsupported mechanism
is not repeatedly rediscovered. A later material fact may open a new linked proposal version; it
does not rewrite the prior decision.

## 5. Prompt-3 boundary

F2 Part 2 creates only this proposal contract. It does not modify master architecture, Formula,
Graph, Risk, ESM, Inventory, roadmaps, HDC ledgers, review forms or authorization. Prompt 3 may
reconcile governance placement, but may not infer approval of any proposed Structure.
