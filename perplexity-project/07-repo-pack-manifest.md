# 07 — Coding-agent companion map
The companion coding-agent-repo directory is self-contained; it does not require recovering earlier chat blocks.

## Entrypoints
AGENTS.md: short universal project rules and command-status policy.
CLAUDE.md: Claude-specific pointer; verify current import/discovery behaviour.
README.md: initial setup/status, not a claim of executable production code.
docs/kb/00-INDEX.md through 10-glossary.md: focused references.
docs/decisions/ADR-0001-stack.md: selected design stack.
docs/decisions/ADR-0002-execution-engine.md: NautilusTrader default and pending spike.
docs/status/STATUS.md: current implementation evidence.

## Skills
.claude/skills/{research-dependency,add-connector,forecast-lifecycle,context-compiler,orb-ui,verify-and-report,execution-spike}/SKILL.md.
.claude/agents/reviewer.md: review reference; automatic discovery depends on the agent.
Skills are Markdown procedures. They do not grant tools, credentials or execution privileges.
For non-Claude tools, configure the supported instruction/skill mechanism explicitly rather than assuming a symlink works everywhere.

## Prompts
00-bootstrap.md, 01-execution-spike.md, 02-graphify-setup.md.

## Sync
Repository code/status and accepted ADRs are the implementation/decision sources. Project files mirror the current relevant facts. Agent can use Git access or explicit handoff; Project uploads are not automatically exposed to it.
