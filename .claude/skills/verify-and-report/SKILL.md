---
name: verify-and-report
description: Finish an MNS task with reproducible verification, honest status, documentation updates and a review handoff.
---
# Verify and report
Version: 1.1, 2026-10-29. Reconstructed reference procedure.

## Procedure
1. Read task acceptance criteria, AGENTS.md, relevant ADRs and current STATUS.
2. Discover real repository commands. make verify and other targets are proposals until implemented; never invent execution or quietly skip a missing target.
3. Run scoped lint/types, unit/integration tests and applicable replay/recovery checks. Report failures and skipped checks explicitly.
4. Capture exact command, output/exit code, revision, environment and dependency versions. Distinguish FIXTURE, SIMULATED, real-feed, venue-demo and live evidence.
5. Mark IMPLEMENTED only for demonstrated criteria; PARTIAL for demonstrated subsets, PLANNED for future work, UNVERIFIED for unsupported claims. Missing evidence is not automatically a proven defect.
6. Update STATUS, changed interfaces/schema docs, source records and accepted ADR amendments. Do not silently change architecture to match accidental code drift.
7. Produce exact KB PATCH blocks for the Perplexity mirror; do not claim those uploads or account memory changed.
8. Request an independent diff review when supported and deliver the smallest next task.

## Final report
Done and changed paths; verified commands/results; partial/unverified items; measured metrics only; decisions required; next bounded task. No secrets in evidence. Documentation verification is not execution verification.
