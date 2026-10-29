@AGENTS.md

# Claude-specific entrypoint
The canonical policy is AGENTS.md. If import syntax is not supported by the installed
agent/version, read that file explicitly rather than duplicating its policy here.
Use .claude/skills/ procedures and the reviewer reference when supported.
Plan schema/execution/store-ownership work before implementation. Keep broad research
bounded; use subagents when supported without losing source/evidence provenance.
No tool discovery, permissions or hooks are configured merely by this file.
