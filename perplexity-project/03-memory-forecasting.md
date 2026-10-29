# 03 — Memory, forecasting and learning

## Store ownership
| Layer | Proposed store | Role |
|---|---|---|
| Raw evidence/historical payloads | Object/file storage | Canonical originals |
| Operational records | PostgreSQL | Canonical forecasts, decisions, orders, fills, evaluations |
| Temporal graph | Graphiti + Neo4j | Derived relational representation |
| Semantic index | pgvector | Derived retrieval |
| Hot state | In-process; Redis only if justified | Ephemeral features/current packets |
| Human vault | Obsidian-compatible Markdown | Readable projection |
| Development map | Graphify | Repo/KB navigation, not live trading memory |

Graphiti is graph-construction/retrieval infrastructure, not a complete turnkey memory service. Our application owns ingestion, identity, lineage, access, consistency and rebuilds.
For rebuildability, persist extraction outputs/versions and entity mappings in canonical storage; rerunning an LLM on raw text alone does not guarantee an identical graph.
Preserve original evidence and both sides of contradictions. Supersede facts, do not erase historical assertions. Separate recency from truth and importance.
Vault exports use stable IDs, typed frontmatter, updated timestamps, evidence references and wikilinks; exports are not a bidirectional execution authority.

## Context compiler
Input: instrument/event, decision type, horizon, as_of, token budget.
Retrieve bounded relevant graph neighbourhood, current state, unresolved forecasts, comparable experiences and meaningful counterevidence. Rank/deduplicate; preserve source IDs, availability and freshness.
Cache with evidence/version-aware invalidation. Do not load the entire vault or history.
Measure retrieval p50/p95, tokens/task, cache hit rate, relevance, missed relevant evidence and downstream decision-quality change.

## Forecast lifecycle
Observation → immutable forecast → trade/wait/reject → scheduled evaluation → outcome and attribution → experience → candidate improvement.
Freeze precise outcome, horizon, reference state, probability/distribution, evidence snapshot, information cutoff and model/prompt/feature/strategy versions before outcome.
Abstention reasons: insufficient_evidence, weak_expected_edge, poor_execution_conditions, portfolio_overlap, stale_information, unresolved_disagreement.
A decision may change; its earlier forecast stays immutable and evaluated.

## Evaluation
Score probabilities with appropriate Brier/log-loss and calibration analysis; evaluate return distributions with suitable separately specified metrics. Report by horizon, regime and sample size.
Separate forecasting from execution, costs and portfolio effects. Evaluate repeated forecasts as cohorts; one probabilistic miss is not automatic proof of model failure.
Counterfactual trades are SIMULATED with explicit feasible entry/exit, fees, spread, slippage and fill uncertainty. A missed move is not proven hypothetical profit.

## Four improvement mechanisms
1 Memory: entity resolution, facts, summaries, indexing and expiry.
2 Forecasting: calibration, source reliability, features and regime-specific performance.
3 Strategies: versioned parameters and policies.
4 Code/model research: isolated candidate artifacts and evaluated training changes.
Adding memory is not updating model weights.
Use hypothesis → implementation → experiment → evaluation → promotion/rejection → monitoring, with out-of-sample evaluation, realistic costs, baseline comparison, attempted-experiment registry and rollback.
Start simple: memory + calibration + supervised forecasting; add complexity only if justified.
