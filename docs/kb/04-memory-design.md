# Memory design

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
