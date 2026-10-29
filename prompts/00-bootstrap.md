# Bootstrap task
1. Read AGENTS.md, current STATUS, KB index, vision, architecture and roadmap.
2. Inspect the actual repository/manifests/deployment; preserve useful existing work.
3. Propose a bounded M0 plan: layout, dependency compatibility, schemas/migrations,
   Compose, command interface, CI and trace IDs. Confirm material scope choices.
4. Implement M0. Make proposed commands real or replace them with actual commands;
   record execution evidence and honest status. Do not invent results.
5. Next run M1 using ADR-0002 and execution-spike skill; report acceptance evidence.
6. Implement M2 as a separate bounded task: narrow real input through frozen forecast,
   act/abstain, paper lifecycle, evaluation/experience and event-backed UI.
7. Load relevant skills only when needed. Graphify setup is optional and not a blocker.
Finish every task with verify-and-report and a reproducible handoff.
