# 08 — Decision log
Snapshot: 2026-10-29. Preserve superseded entries; append amendments with effective dates.

| ID | Decision | Status |
|---|---|---|
| D-001 | Orbs are meaningful stored objects, not all always-on agents | ACCEPTED |
| D-002 | Fast/reasoning/learning loops; LLMs off execution path | ACCEPTED |
| D-003 | Immutable forecast versions; evaluate abstentions | ACCEPTED |
| D-004 | Canonical operational/raw records; rebuildable graph/vector/vault | ACCEPTED |
| D-005 | Python/uv, FastAPI, PostgreSQL+pgvector, Graphiti+Neo4j, NATS JetStream, LangGraph, React+3d-force-graph | ACCEPTED design; implementation unverified |
| D-006 | Graphify dev-time repo/KB tooling; Graphiti runtime graph infrastructure | ACCEPTED role split; exact Graphify tool unverified |
| D-007 | NautilusTrader execution default, gated by ADR-0002 spike | ACCEPTED default; integration acceptance pending |
| D-008 | Do not adopt archived reference projects as new production foundations | ACCEPTED; repository state checked before use |
| D-009 | Narrow crypto universe, replay/paper first; Bybit first venue candidate | PROPOSED venue; staged approach accepted |
| D-010 | Perplexity = reviewer/auditor/KB steward; coding agent = implementation | ACCEPTED |
| D-011 | No fake analytical animation; every orb/edge/pulse backed by records/events | ACCEPTED |
| D-012 | Autonomous improvement through versioned experiments and measured promotion | ACCEPTED |

## Supersession / conflicts
D-007 resolves the earlier wording “execution undecided”: default is chosen, compatibility is not proven.
If code diverges from an accepted design, report the divergence and ask for decision resolution if needed. Code evidence shows what exists; it does not silently ratify a new architecture.

## ADR template
ID/title; status; date; context; options (at least two where meaningful); decision; reasons; consequences; verification gate; evidence links; revisit trigger; supersedes.
