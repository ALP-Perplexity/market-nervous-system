# ADR-0001 — Initial stack
Date: 2026-10-29.
Status: ACCEPTED design; integration/versions UNVERIFIED.

## Context
Need typed ingestion, canonical history, temporal retrieval, bounded research,
deterministic execution and inspectable event-backed visualisation.

## Decision
Python/uv, FastAPI, PostgreSQL+pgvector, Graphiti+Neo4j, NATS JetStream,
LangGraph, React/TypeScript+3d-force-graph, Docker Compose.
Keep graph/vector/vault derived and rebuildable. Store extraction outputs/version mappings
canonically to avoid relying on identical future LLM extraction.
Execution default is NautilusTrader, with its separate ADR-0002 gate.

## Alternatives
FalkorDB instead of Neo4j; in-process state instead of Redis initially;
Freqtrade for crypto-first execution; thin custom adapters.
Avoid expanding dependencies without demonstrated need.

## Consequences
Multiple stores add consistency/operations work. NATS transport dedupe does not
replace application order-intent idempotency. Pin versions after compatibility checks.
Python 3.12 is a starting candidate, not a verified universal minimum/requirement.

## Revisit
Failed integration gate, measured performance/ops cost or materially changed requirements.
