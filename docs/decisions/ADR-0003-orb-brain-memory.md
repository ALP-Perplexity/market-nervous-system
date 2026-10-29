# ADR-0003 — Versioned temporal orb-brain projections
Status: PROPOSED. Date: 2026-10-30. Supersedes: none.

## Context
D-003/D-004/D-012 already require immutable forecasts, canonical records, rebuildable views and measured improvement. The refinement must prevent derived-memory hindsight and uncontrolled vault edits without treating documentation as implementation.

## Options
A. Canonical records + full-text/vector retrieval only: simpler baseline, fewer relational retrieval capabilities.
B. Canonical records + Graphiti/Neo4j + vector and Obsidian projections: follows accepted stack; greater consistency/temporal testing burden.
C. Vault-first or additional autonomous memory framework: flexible notes, but operational consistency and overlapping ownership require extra machinery.

## Proposed decision
Retain B as the intended stack, compare against A, and use research mechanisms from C only in isolated experiments. Preserve original evidence, extraction outputs, mappings and revisions canonically. Apply availability cutoffs to every derived artifact. Keep generated vault notes and human proposals separate. Lessons use explicit evaluation/promotion states.

## Consequences
Requires projection manifests, retry/reconciliation tests, versioned context packets, scoped lesson records and historical isolation tests. More graph connectivity is not proof of truth or learning. No automatic policy/code promotion is authorised.

## Verification gate
Run prompts/03-orb-brain-spike.md. Demonstrate duplicate-safe ingestion, no future/namespace leakage, immutable/evaluated abstention forecast, provenance-preserving rebuild and recoverable vault export. Compare retrieval variants on identical eligible evidence. Report commands/output/environment/revision and limits.

## Evidence and revisit
Research: perplexity-project/15-orb-brain-knowledge.md, including its source URLs. Source ledger additions S23–S26 are prepared separately and not yet applied. Execution evidence: none. Revisit if graph retrieval cannot enforce temporal isolation, measurable benefit fails to justify complexity, or projection consistency cannot be demonstrated. Recording this ADR does not accept it or change D-005.
