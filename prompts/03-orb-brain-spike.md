# Orb-brain verification spike
Status: PROPOSED bounded coding-agent task, 2026-10-30.

## TASK
Demonstrate one traceable evidence-to-evaluated-memory loop without live orders or a platform rewrite.

## READ
AGENTS.md; docs/status/STATUS.md; docs/kb/00-INDEX.md; 04-memory-design.md; 05-forecasting-learning.md; 12-orb-brain-knowledge.md; docs/decisions/ADR-0003-orb-brain-memory.md; perplexity-project/15-orb-brain-knowledge.md.
Inspect actual repository instructions and runnable components. Report files read and missing prerequisites. Do not assume this documentation scaffold contains executable commands.

## PREREQUISITES
Verify current official documentation, exact dependency versions and repository revisions. Recheck the sources linked in the full specification and applicable Obsidian integration documentation. Record maintenance/license constraints; do not blindly install research frameworks.
Reuse accepted dependencies. No assumed venue, credential, instrument universe, horizon, budget or model. A labelled FIXTURE may demonstrate invariants, not market performance. If M0 prerequisites are absent, implement only the minimal test harness needed and report remaining integration as UNVERIFIED.

## SCOPE
1. Typed canonical Evidence, Claim, RelationshipAssertion, Forecast, Outcome, Evaluation, LessonCandidate, ContextPacket, MemoryChange, ProjectionManifest and BrainActivityEvent records with stable IDs/revisions.
2. Idempotent input and committed-change projection; preserve raw payloads, extraction output/version and lineage.
3. as_of retrieval with namespace isolation. Test availability of derived summaries/relationships and calibration/experience state; prevent future graph expansion and cache leaks.
4. Compare direct/full-text/vector baseline with bounded graph-assisted retrieval on identical eligible evidence. Preserve counterevidence and unknowns; store packet IDs/revisions/configuration/hash.
5. Freeze one forecast before its outcome, record abstention and evaluate it using a predefined label/scoring rule. Reflection cannot invent ground truth.
6. Propose one scoped lesson with support, counterexamples, test and review conditions. Do not automatically activate a trading policy or code change.
7. Generate one Obsidian-compatible note through an idempotent atomic projection; separate human annotations/proposals, prevent export loops and test reconciliation/regeneration.
8. Emit real activity events and expose a minimal trace inspector using existing UI facilities where available. No decorative analytical activity.

## ACCEPTANCE
Tests cover duplicate ingestion; copied-source corroboration; contradictory claims; late evidence; future summaries/entity merges; immutable forecasts; abstention evaluation; delayed labels; namespace/cache isolation; export crash/retry/manual edits; provenance-preserving rebuilds; context budget limits.
Historical replay and retrospective reconstruction are labelled separately. State residual model-pretraining hindsight risk. Keep live/paper/replay/experiment data isolated in storage, caches and workers.
Record recall, contradiction recall, provenance completeness, temporal violations, context size, latency, calls/tokens and evaluation coverage where measured. Do not claim graph benefit or learning from fixture success alone.

## DELIVER / VERIFY
Deliver schemas/migrations, bounded harness, tests, retrieval comparison, vault projection, trace evidence and updated STATUS/handoff. Use actual repository commands; record command, exit code, relevant output, environment, dependency versions, revision and FIXTURE/real/SIMULATED classification.
Separate IMPLEMENTED / PARTIAL / PLANNED / UNVERIFIED and documentation versus execution checks. Retain all existing invariants and accepted stack decisions.

## STOP
Stop for a decision if work requires changing accepted architecture, ordering trades, assuming missing commercial access or promoting code/policy. Do not expand to a full multi-agent deployment, model-training platform or entire dashboard.
