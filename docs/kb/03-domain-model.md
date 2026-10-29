# Domain model
Typed/versioned schemas and stable IDs are required. Names below are design contracts, not implemented tables.

Entities: Asset, Instrument, Venue, MarketEvent, Evidence, Claim, Narrative, MarketRegime,
Forecast, StrategyVersion, Decision, DecisionPacket, OrderIntent, Order, Fill, Position,
Experience, Evaluation, ImprovementCandidate, AgentTask, OrbNode, OrbEdge.

## Identity
Internal stable ID plus explicit vendor IDs. Never key by ticker/title alone.
Polymarket: separate Event, Market/Condition, Outcome, tradable outcome instrument,
ResolutionSpec and ResolutionState.

## Common fields
schema_version, created_at, trace_id, provenance references. Select UUIDv7/ULID or
another justified ID scheme during M0; do not claim one was already implemented.

## Time
Distinguish event_time, published_time, available_time and ingested_time.
Unknown event/publication times remain unknown. Store local first observation;
historical vendor publication timestamps do not prove historical system availability.
Use validity intervals for facts and explicit forecast/evaluation times.
Retrieval as_of applies to derived summaries, graph, features and versions, not just raw rows.

## Forecast
id, version, parent_id, instrument_id, precise outcome/horizon, evaluation schedule,
probability/distribution, reference state, conditions/invalidation, evidence snapshot IDs,
model/prompt/feature/strategy versions, decision reference and information cutoff.
Insert-only original; amendments create a new version.

## DecisionPacket
See 02-architecture.md. Include expiry and source/forecast/version lineage.

## Abstention reasons
insufficient_evidence, weak_expected_edge, poor_execution_conditions, portfolio_overlap,
stale_information, unresolved_disagreement.

## Orb types/edges
Types: asset, event, narrative, forecast, strategy, experience, research_agent,
maintenance_agent, decision.
Edges: supports, contradicts, derived_from, predicts, depends_on, evaluated_by,
supersedes, correlated_with, triggered. Correlation is not causation.
