# 15 — Orb brain: evidence, memory and evaluated learning
Prepared: 2026-10-30. Status: PROPOSED refinements; production implementation UNVERIFIED.
This supplement extends 03-memory-forecasting.md and 12-orb-interface.md. It does not replace accepted decisions or the four improvement mechanisms already recorded.

## Research summary
The brain is an evaluated learning loop, not a growing vault:
observe → preserve evidence → extract attributed claims → retrieve eligible context → freeze forecast → act/abstain → evaluate outcome → propose scoped improvement → test → versioned promotion/rejection.
Memory acquisition, organisation, forecasting, strategy/procedural improvement and model/code research are distinct activities. Procedural lessons refine the existing strategy/research mechanisms; this is not a new accepted taxonomy.
More notes, edges, agent messages or successful trades alone do not establish improved intelligence.

## Research basis and limits
Prior-session primary-source readings, recorded 2026-10-30; not re-fetched during this packaging task. Current API, license, maintenance and deployment compatibility remain to be checked before implementation.
- Graphiti: https://github.com/getzep/graphiti — temporal graph construction, provenance and hybrid retrieval. It is infrastructure; MNS owns consistency, isolation, canonical history and historical retrieval verification. Prior-session README revision: 72b5c59c06607e09ea855be61b6ff5a3446fc951.
- A-Mem: https://arxiv.org/html/2502.12110 — structured atomic notes, links and evolved contextual representations. Borrow organisation, but create versioned revisions rather than overwriting MNS history. Conversational evaluation does not establish trading performance.
- HippoRAG 2: https://ar5iv.labs.arxiv.org/html/2502.14802 — passage/concept graph-assisted associative retrieval. Treat as a challenger mechanism, not a required extra runtime memory stack. QA/retrieval results do not establish market forecasting gains.
- ACE: https://github.com/ace-agent/ace/blob/main/README.md — generator/reflector/curator and incremental playbook edits. Helpful/harmful counters are diagnostics, not causal proof. Documented finance tasks concern extraction/structured processing, not demonstrated profitable trading.
- LongMemEval: https://arxiv.org/abs/2410.10813 — extraction, multi-session reasoning, temporal reasoning, updates and abstention. Borrow test categories; develop separate market-specific evaluations.
No dependencies were installed, benchmarks reproduced or trading results established by this research. Source-ledger additions S23–S26 are prepared in the accompanying update package, not yet applied to the existing ledger.

## Canonical ownership and rebuildability
PostgreSQL holds canonical record IDs, revisions, extraction outputs, mappings, forecasts, evaluations and projection manifests; raw storage preserves original payloads and hashes. Graphiti/Neo4j, pgvector and the Obsidian vault are derived views. LangGraph checkpoints manage workflow state; they are not the sole market record.
Use committed-change publication with retries and idempotent consumers. Save extraction outputs, model/prompt versions and entity mappings. Replaying saved changes is different from rerunning an LLM and expecting an identical graph.
Preserve the accepted Python/uv, FastAPI, PostgreSQL+pgvector, Graphiti+Neo4j, NATS JetStream, LangGraph, React+3d-force-graph stack. Graphify remains dev-time tooling. LLMs never place orders.

## Knowledge objects and evidence semantics
Orb objects include Evidence, Claim, Entity, Event, Narrative, Hypothesis, Forecast, Decision, Experience, Lesson and actual AgentTask records.
A source publishing a statement proves publication, not the statement's truth. Keep attribution, original-source lineage, scope and supporting/contradicting evidence.
Candidate relationship types: asserts, supports, contradicts, derived_from, informs, predicts, assessed_by, supersedes. Version inferred relationships; do not promote correlation to causation.
Keep extraction confidence, entity-match confidence, source reliability, claim support, forecast probability, calibration evidence and freshness separate. A single confidence glow obscures their different meanings.
Copied articles are an evidence family, not independent corroboration. Retrieval frequency, graph degree and mention count are not truth or demonstrated forecasting utility.

## Point-in-time contract
Track event_at, published_at, available_at, ingested_at, derived_available_at and validity intervals when known. Unknown timestamps remain explicit, not invented.
Retrieval takes namespace, mode, as_of, scope and configuration version. Apply eligibility to summaries, edges, embeddings, entity resolution, experiences, lessons, calibration and cached packets, not just raw documents. Filter before graph expansion; enforce isolation in queries, caches and worker inputs.
Use version-eligible projections or isolated snapshots if the current graph cannot satisfy historical isolation. Test late arrivals, entity merges and future-derived summaries explicitly.
Knowledge replay asks what the deployed system knew then. Retrospective reconstruction asks what a later pipeline extracts from old evidence. Label them separately. Modern model pretraining may contain historical outcomes; archive filtering does not prove model-level absence of hindsight. Include prospective frozen-version evaluation.

## Context compiler
Input: task purpose, instrument/event scope, horizon, as_of, namespace, token budget and retrieval version.
Resolve scope → eligibility filter → direct/full-text/vector retrieval → bounded graph expansion → comparable evaluated experiences → counterevidence → source-lineage deduplication → ranking and budget enforcement → persisted ContextPacket.
Record selected IDs/revisions, configuration, unknowns and packet hash. Use evidence/version-aware cache invalidation. Never load the full vault by default.
Compare the graph-assisted path against a simpler retrieval baseline on identical eligible evidence. Graph structure must earn its complexity through measured retrieval and downstream benefit.

## Forecasts, outcomes and lessons
Freeze outcome specification, horizon, probability/distribution, cutoff, evidence snapshot and model/prompt/feature/policy versions before outcomes. Revisions create new forecasts. Retain and evaluate abstentions.
Outcome states include pending, resolved, unresolved, missing data and disputed. Use deterministic scoring where specified; LLM reflection is not the ground-truth label. Separate forecast, retrieval, decision, execution and evaluation quality.
Evaluate cohorts by horizon/regime/sample size. One probabilistic miss does not establish method failure; one profit does not validate reasoning. Counterfactual trades remain SIMULATED with explicit fill/cost assumptions.
LessonCandidate fields: scope, proposed change, supporting episode IDs, counterexamples, alternative explanations, required experiment, expiry/review conditions and state.
Proposed lifecycle: candidate → evaluated → shadow → active; deprecated/superseded remain preserved. Promotion policy is a separate explicit versioned decision. This spike proposes lessons; it does not autonomously deploy code or trading-policy changes.
FIXTURE illustration: test source-lineage deduplication before treating repeated announcements as corroboration. This is a procedural hypothesis, not an established market edge.

## Obsidian contract
Obsidian is the readable projection and controlled human-input surface, not an execution database or learning engine.
Suggested folders: Home, Entities, Events, Claims, Narratives, Hypotheses, Forecasts, Experiences, Lessons, Evaluations, Annotations, Proposals, System.
Generated frontmatter includes stable ID, type, revision, canonical_record_id, available_at, projection_version and source_hash. Bodies show scope, evidence, counterevidence, unknowns, connected forecasts, outcomes and revision changes.
Separate generated notes from human annotations/proposals. Import human input as attributed candidate records; never silently overwrite canonical history. Ordinary wikilinks are navigation, not automatically typed factual assertions.
Write temporary files, validate, atomically replace, then update a manifest. Test retries, crash recovery, title/path changes, link integrity, export-loop prevention and canonical/export reconciliation. Regenerate the vault without Obsidian running. Do not export every market tick as Markdown.

## Maintenance, activation and UI
A bounded curator processes changed/overdue neighbourhoods: deduplication proposals, contradictions, unsupported summaries, stale applicability, due evaluations, provenance repair and projection recovery.
Archive by lowering default retrieval priority; preserve original evidence. Consolidation creates revisions, not erased history.
A small worker pool activates relevant objects on evidence changes, contradictions, maturity deadlines or scheduled reviews. Use task deduplication, concurrency limits and stopping conditions.
Every orb/edge maps to stored records; pulses carry real event/trace IDs and timestamps. Coalescing animation is allowed without fabricating activity. Display concise recorded rationale, not invented internal thoughts.

## Alternatives and verification spike
A: canonical records plus full-text/vector retrieval — simpler comparison baseline.
B: same records plus Graphiti/Neo4j bounded retrieval — accepted stack direction, integration and benefit unverified.
C: A-Mem/HippoRAG-inspired challenger — experiment only, not an automatic dependency change.
Vault-only authority is not recommended for operational consistency.
Bounded spike: one labelled observation through evidence → claim → as_of context → immutable forecast → abstention → outcome → candidate lesson → vault note → real activity trace. No live orders; fixtures cannot establish forecasting improvement.
Measure recall, contradiction recall, provenance completeness, temporal violations, context size, p50/p95 latency, calls/tokens, export lag and evaluation coverage. Report uncertainty and sample sizes; do not invent performance thresholds or gains.
Tests: duplicates, copied-source families, contradictions, late evidence, future summaries/merges, forecast mutation, abstention evaluation, delayed labels, namespace leaks, cache contamination, export failures/manual edits and lesson overgeneralisation.
Implementation gate: exact commands, relevant outputs/exit codes, revision, environment and dependency versions. Documentation verification is not execution verification.

## Reviewer instructions
For every learning claim ask: what changed, why, supporting evidence, cutoff, preserved history, falsifier, evaluation and rollback?
For memory changes inspect ownership, provenance, temporal isolation, contradictions, rebuilds, namespace isolation and cost.
Return BLOCKERS / SHOULD-FIX / NITS plus coverage limitations. Never equate graph size with intelligence, reflection with validation, historical replay with prospective proof, or missing evidence with a confirmed defect.
Read index/status first and task-relevant files only. Accepted decisions remain accepted; refinements stay PROPOSED until explicitly resolved. Do not claim account memory, Project uploads or repository changes without verified writes.
