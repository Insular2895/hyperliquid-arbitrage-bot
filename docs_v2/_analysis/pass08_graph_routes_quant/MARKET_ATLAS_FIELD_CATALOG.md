# Market Atlas Field Catalog

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Exact serialized names are Data Contracts-owned. Rows below are required semantic fields, not a premature schema. Learned rows carry horizon, support/confidence, model version and dataset/manifest lineage; structural rows carry Graph/Route/Metadata versions.

| Group/field family | Meaning/unit | Kind | Horizon | Producer | Consumers | Point-in-time/source |
|---|---|---|---|---|---|---|
| MARKET identity/status | venue, market, base/quote, current availability | Structural | current | Graph/metadata | all | GraphVersion; SRC-003/005 |
| spread/depth/liquidity | QF-002–006 summaries in price/base/quote units | Derived/learned aggregate | multi | Feature/Recorder | HWC, Risk, Capital | book/formula versions; SRC-001/004 |
| volatility/jump | QF-036–039 regime evidence | Derived | multi | Feature Engine | HWC, Risk, Simulator | evidence available by T |
| replenishment/resilience | observed recovery/response with support | Learned | multi | Participants/Recorder | HWC, Simulator | model/dataset version; QF-043 |
| competition/event intensity | observed opportunity/correction/competition evidence | Learned | multi | Participants/Recorder | activation/research | QF-082/083; no causal claim |
| execution quality | completion, partial, reject, recovery and capture distributions | Learned | multi | Execution/Simulator/Recorder | Risk, Capital | actual vs predicted separate |
| ROUTE identity/counts | RouteId/type; structural, active, reachable counts | Mixed | current | Route/Activation | Atlas, Capital | RouteVersion; counts distinct |
| opportunity frequency | episodes detected/accepted/rejected/captured per time | Learned | multi | Opportunity/Recorder | activation/research | episode definition avoids tick duplication |
| edge distribution | size-specific QF-019/022/026 observations | Learned | multi | Opportunity/Recorder | sizing/research | q and versions mandatory |
| edge survival/correction | survival, half-life, QF-082 | Learned | multi | Participants | HWC, Simulator | PASS02 authority |
| route capacity | QF-027 and externally supplied QF-076 | Mixed | current/multi | Route; PASS07 | Capital/Sizing | do not conflate them |
| expected EV/capture | predicted route outcomes and QF-048 | Learned | multi | Participants/Simulator | Risk/Sizing | confidence/OOD mandatory |
| ASSET connectivity | reachable route counts and exit paths | Structural | current | Graph/Route | Capital | topology at T |
| exit liquidity/cost | size-dependent executable exit evidence | Derived/learned | multi | Route/PASS07 | Terminal Viability | QF-068 owner PASS07 |
| inventory/terminal utility | class/bands/terminal viability reference | External state | current | PASS07 | Atlas/activation | not recomputed here |
| bridge usefulness | route availability and historical relocation evidence | Mixed | multi | Graph/PASS07/Recorder | Capital | QF-070/072 boundary |
| CAPITAL-LOCATION reachability | current inventory-accessible/productive region | External state | current | PASS07 | HWC/Activation | venue-aware, point-in-time |
| capital utility/idle evidence | opportunity utility, utilization, idle observations | Learned | multi | PASS07/Recorder | placement research | no automatic relocation |
| stranded/exit risk | QF-068/069 consumer view | External/learned | multi | PASS07 | HWC/research | PASS07 authority |
| REGIME horizon/window | FAST/RECENT/MEDIUM/LONG identity | Structural config | multi | Atlas config | all Atlas consumers | exact windows calibrated |
| confidence/support | sample/episode support, uncertainty, OOD | Learned | per field/window | Atlas/model governance | all | model/dataset/version |
| AtlasVersion | immutable publication identity/time | Structural | snapshot | Atlas Engine | Replay/DecisionTrace | no lookahead |

No universal weighted Atlas score is locked. A source-inspired score is a governed calibrated/research heuristic and never substitutes for exact current route economics or constitutional gates.
