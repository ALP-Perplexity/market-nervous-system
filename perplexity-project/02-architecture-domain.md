# 02 — Architecture and domain

## Three loops
FAST: market/account state → deterministic features → cached policy + prepared DecisionPacket → order management. No LLM or full-graph traversal in routine execution.
REASONING: material event/scheduled review → context compiler → bounded specialists → structured DecisionPacket.
LEARNING: matured forecast/completed action → evaluation → experience → experiment → candidate promotion/rejection.

## Components
Typed ingestion; durable event transport; canonical records; graph/vector projections; context compiler; specialist workflows; forecast service; strategy laboratory; portfolio/execution/reconciliation; FastAPI event API; orb dashboard.
Logical specialists: microstructure, technical/regime, asset research, social/narrative, prediction markets, strategy lab, memory curation, decision synthesis and portfolio management. Role is not synonymous with a dedicated model/container.

## DecisionPacket contract (design, not implemented schema)
Stable ID, schema version, instrument/contract and venue IDs, as_of, information cutoff, regime, horizon, forecast reference/probability, supporting and opposing evidence IDs, strategy version, entry/invalidation conditions, expires_at, reconsideration triggers, portfolio implications and trace_id.
Deterministic validation checks freshness, instrument validity, permitted intent, constraints, live state and duplication before creating OrderIntent. Expired packets are not silently reused.

## Domain entities
Asset, Instrument, Venue, MarketEvent, Evidence, Claim, Narrative, MarketRegime, Forecast, StrategyVersion, Decision, DecisionPacket, OrderIntent, Order, Fill, Position, Experience, Evaluation, ImprovementCandidate, AgentTask, OrbNode, OrbEdge.
Polymarket: distinguish Event, Market/Condition, Outcome, tradable outcome instrument, ResolutionSpec and ResolutionState. Do not use a bare ticker or market title as an identifier.

## Identity and time
Stable internal IDs plus explicit vendor IDs; UUIDv7/ULID are candidate choices, not an implemented standard.
Every record has schema_version, created_at, trace_id and applicable provenance.
Event time, publication time, first verified availability and local ingestion time are distinct. Unknown publication/event times stay null/unknown, not fabricated.
Record local first observation. A vendor's claimed historical publication time alone does not prove historical system availability.
Historical retrieval must enforce as_of across evidence, summaries, graph facts, features and model/training versions.

## Relationships
supports, contradicts, derived_from, predicts, depends_on, evaluated_by, supersedes, correlated_with, triggered. Correlation is not proof of causation.

## Failure handling
Persist workflow progress; retries/timeouts are bounded. Stable idempotency keys, startup recovery and venue reconciliation are requirements. Broker deduplication alone is not business-level order idempotency.
