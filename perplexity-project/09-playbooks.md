# 09 — Perplexity playbooks (reference skills)
These workflows are selected by trigger words. They are not automatically installed executable skills.

## REVIEW
Read relevant KB/ADR plus report/diff. Establish reviewed revision and scope. Check all 11 invariants and acceptance tests; distinguish code inspection from executed evidence.
Return BLOCKERS / SHOULD-FIX / NITS, then a bounded paste-ready agent task where useful.
Check: deterministic execution; immutable forecasts; as_of everywhere; idempotency; preserved evidence; external text handling; fixture labels; rebuilds; real UI events; tests/status.
If only a report is supplied, state “report-only review”; do not pretend code was audited.

## AUDIT
Map each implementation claim to exact command/output, revision and environment. Produce area | claimed state | evidence | verdict | missing check.
Missing evidence gives UNVERIFIED; demonstrated incompleteness gives PARTIAL. Do not automatically mark every unproven claim a known failure.
Inspect leakage/replay/reconciliation/rebuild tests and realistic metric provenance. Name scope limitations, top issues and next three tasks.

## RESEARCH
Define the decision. Use current primary docs/repos/papers, record checked date and exact version where relevant. Compare at least two plausible alternatives or explain why none applies.
Table: role, maintenance/license, documented capability, unverified gaps, integration effort. Recommend; specify minimal spike; draft ADR; update source ledger.
No transferable profit claim from a README/backtest or precise performance figure without reproducible context.

## KB
Provide exact patch: FILE, operation, exact heading/anchor, complete replacement/addition text. List dependent files. Update decisions/status/source ledger as applicable. Never claim applied unless verified.

## PROMPT
Bound task to one outcome. Include minimal context files, prerequisites, scope, deliverables, invariant constraints, acceptance tests, reporting requirements and stop conditions.

## ADR
Separate architectural selection from execution verification. Include alternatives, consequences, gate, revisit trigger and proposed/accepted status.

## WEEKLY
Status delta; actual evidence; measured metric changes; decisions; KB/code divergence; unresolved dependencies; next three tasks. Produce one bounded agent task, not an expanding backlog.

## EXPLAIN
Answer plainly, use one project-specific example, then connect it to the actual files and status.

## Report triage
Extract claims → classify document/code/execution evidence → identify contradictions → request the smallest missing artifact → draft updates.

## Core acceptance checklist
Forecast insert-only; abstention evaluated; later information excluded; duplicate events do not duplicate intents; partial fill/cancel/restart reconciled; expired packets rejected; contradictory sources preserved; derived views rebuild; outcome labels not premature; promotions versioned; UI events traceable; baseline retained.
