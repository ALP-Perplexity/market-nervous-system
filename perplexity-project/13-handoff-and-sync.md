# 13 — Handoff, sync and change control

## Boundaries
Generating these files does not upload them to the Project, save account memory, connect a coding agent, write a repository or configure a database.
Project files persist as uploaded reference artifacts subject to product behaviour; no automatic synchronization is assumed. Tool availability and plan limits are checked in the current UI/docs when needed.

## Ownership
Repo: production code, executable tests, canonical agent instructions, applied migrations and implementation status.
Accepted ADRs: intended architecture and approved changes.
Perplexity Project: mirrored summaries, evidence ledger, review/research playbooks, prompts and decision stewardship.
Optional personal memory: high-level preferences/identity only; never substitute for versioned technical files.

## Handoff template
Project: MNS
Timestamp:
Branch / commit:
Task / acceptance criteria:
Changed files:
Relevant diff or links:
Environment / pinned versions:
Commands + output + exit codes:
Evidence type (real / fixture / simulated / venue demo):
Status delta:
Decision changes requested:
Known blockers / unverified claims:
Next bounded task:

## Sync cycle
1 Agent commits task and STATUS evidence.
2 Viktor supplies handoff or configured connector access.
3 Perplexity reviews/audits within available scope.
4 Material changes become ADRs or exact KB PATCH blocks.
5 Viktor/agent applies accepted repo changes and re-uploads updated Project copies.
6 Next session reads index/status and checks revision alignment.

## Patch template
KB PATCH
FILE: exact file name/path
OPERATION: REPLACE SECTION / APPEND SECTION / CREATE
ANCHOR: exact heading
TEXT:
Complete replacement text, not a vague instruction.
DEPENDENCIES: affected status/decision/source files.
APPLIED: no, until verified.

## Version discipline
Never edit away superseded decisions or original evidence. Applied migrations remain immutable. Keep archived document revisions in Git rather than upload conflicting current copies.
If Project and repo are out of sync, disclose the snapshot date and request the smallest missing current artifact.
