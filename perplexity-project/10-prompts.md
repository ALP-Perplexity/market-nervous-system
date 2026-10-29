# 10 — Prompt library

## Standard agent task
TASK: one measurable outcome.
READ: AGENTS.md, current STATUS.md, only the relevant KB and ADR files.
SKILL: relevant reference procedure, if supported by this agent.
PREREQUISITES: versions/credentials/environment actually needed; never assume.
SCOPE: included and excluded changes.
DELIVERABLES: concrete files, tests, evidence.
CONSTRAINTS: relevant invariants and approved dependencies.
ACCEPTANCE: explicit checks and pass criteria.
VERIFY: run actual repository commands; report exact command/output/revision/environment. Proposed commands are not automatically available.
REPORT: done, verified, partial/unverified, decisions, metrics if measured, next task.
STOP: request decision if scope requires changing an accepted invariant/dependency/interface.

## Execution spike
TASK: Verify NautilusTrader default against ADR-0002 S1–S3 without changing the production architecture.
READ: AGENTS.md, STATUS.md, venue KB, ADR-0002.
Use current official adapter/API docs. Pin exact package version. Distinguish local simulation, venue testnet/demo and live execution.
Report data, lifecycle, duplication, restart/reconcile, replay boundaries and actual commands. Do not require a live funded transaction for the initial paper spike. Failed criteria stay failed/unverified, not silently skipped.

## Graphify setup
TASK: Identify and verify the intended Graphify repo/skill before installation.
Check official source, package ownership, supported agent, license, CLI, generated files, update mechanism and any Obsidian export.
Inspect hooks before enabling. Build a development graph on a small code/docs subset; verify retrieval and source links. Export only if currently supported.
Do not confuse it with Graphiti or let a stale graph override source code. Report exact commands/output and version. Do not install a similarly named package by guess.

## Review request
REVIEW
Revision/branch:
Task and acceptance criteria:
Changed files/diff:
Agent report:
Commands and outputs:
Focus, if any:

## Audit request
AUDIT
Current STATUS.md:
Revision/environment:
Test and smoke outputs:
Repo tree/relevant files:
Claims to audit:

## Project refresh
KB
Here is the latest accepted handoff and STATUS.md. Identify divergence, draft exact patches for changed facts/status/decisions, and do not treat the files as updated until I upload or apply them.
