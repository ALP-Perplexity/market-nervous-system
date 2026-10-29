# 06 — Roadmap and status
Snapshot: 2026-10-29. This document pack is prepared; production implementation is not demonstrated.

## Status meanings
IMPLEMENTED: relevant acceptance criteria demonstrated by reproducible command/output evidence at a stated revision/environment.
PARTIAL: some criteria demonstrated, others missing.
PLANNED: agreed future work; no completion claim.
UNVERIFIED: completion/capability claim lacks sufficient evidence.
A documentation check is not an implementation check.

## Milestones
M0 Repo/Compose, typed schemas/migrations, runnable command interface, CI and trace IDs.
M1 NautilusTrader spikes S1–S3 and ADR-0002 gate result.
M2 End-to-end real input → evidence → graph → forecast → act/abstain → paper execution → evaluation → experience → UI trace. Use a simple strategy and narrow universe.
M3 Context compiler, token/latency metrics, human-vault export.
M4 News/social/CMC specialists, lineage, deduplication and contradictions.
M5 Strategy lab, replay, baselines, calibration, shadow experiments, promotion gate.
M6 Complete Polymarket integration, contract/resolution semantics and costs. M1 may investigate it earlier.
M7 Shared-event exposure map and portfolio integration.
M8 Recovery/reconciliation, backups and restore, load/cost observability.
M9 Scale coverage/orbs only with measured benefit.

| Area | State | Evidence |
|---|---|---|
| Documentation pack | PREPARED | Generated files, not deployed Project state |
| Repo scaffold / deployment | PLANNED | None supplied |
| Schemas / ingestion | PLANNED | None supplied |
| Execution integration | UNVERIFIED | Default selected; no spike output |
| Runtime memory / retrieval | PLANNED | None supplied |
| Forecast/evaluation | PLANNED | None supplied |
| Orb dashboard | PLANNED | None supplied |
| Graphify setup | UNVERIFIED | Exact tool/CLI must be verified |

## Metrics
Not measured: retrieval p50/p95, tokens/task, cache hit rate, decision lookup, LLM latency, venue round-trip, daily cost, calibration, net results.
Never fill these with illustrative data unless labelled FIXTURE.

## Pending inputs
First venue/account region/product; asset universe and forecast horizon; hardware/model budget; SDK/signing details; first source/API access. Resolve only what the next task requires.

## Next recommended task
M0 foundation inspection/scaffold and verification, followed by bounded M1 integration spike. Graphify is useful development tooling but not a blocker to the first vertical slice.
