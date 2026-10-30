# Obsidian agent-memory tooling review
Checked: 2026-10-30. Scope: documentation/source reading only; nothing installed or executed beyond copying four Markdown skills.
Requested by Viktor. Applies research-dependency procedure. Repository text was read as data, not instructions.

| Repository | Revision | License | What it is |
|---|---|---|---|
| kepano/obsidian-skills | 3ccff53 (2026-09-15) | MIT | Pure Markdown agent skills for Obsidian file formats and CLI |
| breferrari/obsidian-mind | fae7be4 (2026-10-18), template v10.0.0 | MIT | Vault template giving coding agents persistent memory: lifecycle hooks (Node 22 TS), QMD semantic search, `om` MCP server, 10 subagents |
| eugeniughelbur/obsidian-second-brain | f79c64f (2026-10-28) | MIT | Self-rewriting "LLM wiki" skill: 48 commands, Python scripts, hooks, own MCP server, scheduled agents, Crew multi-agent logbook |

## Fit with MNS
MNS Obsidian role is fixed by D-004 and ADR-0003 (PROPOSED): the vault is a generated, rebuildable, readable projection plus a separate human-proposal lane. It is not the learner, not an execution database and not canonical memory. All three repositories assume the opposite (vault-first = ADR-0003 option C), so only parts transfer.

## Decisions taken in this change
ADOPTED — kepano skills obsidian-markdown, obsidian-bases, json-canvas, obsidian-cli vendored into .claude/skills/ (provenance: .claude/skills/THIRD_PARTY.md). They are format references for the ADR-0003 vault projection (typed properties, wikilinks, callouts, Bases views over forecasts/lessons, Canvas trace diagrams). No runtime dependency added.

NOT INSTALLED — obsidian-mind and obsidian-second-brain. Reasons:
- Both install agent hooks (SessionStart, UserPromptSubmit, PostToolUse, PreCompact, Stop) and MCP servers; AGENTS.md requires approval for new services and no hooks are configured here.
- second-brain "contradictions reconcile automatically" and "sources rewrite existing pages" conflict with invariant 6 (preserve original evidence, supersede) and ADR-0003 (keep both sides of contradictions).
- second-brain research commands send content to external services (Grok, Perplexity, NotebookLM); its installer is curl | bash and edits global ~/.claude settings.
- Their domain (work notes, 1:1s, brag docs, deals) is personal knowledge management, not market memory.

## Patterns worth reusing (PROPOSED, not implemented)
1. Freshness rule (second-brain OKM, references/freshness-policy.md): every stored fact is timeless, dated `(as of YYYY-MM-DD, source)`, or a pointer to where truth lives; undated present-tense volatile claims are lint errors. Directly supports invariant 4 and already matches how STATUS.md snapshots are written. Candidate KB writing rule and vault-export lint.
2. Manifest boundary (obsidian-mind vault-manifest.json): explicit infrastructure vs user-content paths and frontmatter schemas. Maps to ADR-0003 ProjectionManifest plus generated-note vs human-proposal lanes.
3. Procedural code owns environment, agent owns content (obsidian-mind ARCHITECTURE.md). Same split as MNS deterministic execution vs DecisionPacket.
4. Eager-context byte budget (obsidian-mind eager_layer_budget_bytes). Analogue of the context compiler token budget.
5. Human-gated lessons (second-brain Crew: append-only shared log; agents propose lessons; only a human `keep` turns one into a rule). Matches ADR-0003 explicit lesson promotion and suits multi-agent collaboration (coding agent + reviewer agent). A repo-local equivalent is a dated handoff log using the 13-handoff-and-sync template, without installing Crew hooks.
6. Cross-repo vault access over MCP (obsidian-mind `om`). Possible later read-only surface for the generated vault; not needed before M3.

## Open items
Any adoption of patterns 1, 5 or 6 as tooling needs Viktor approval and, for 6, a research-dependency spike. Upstream claims (retrieval quality, "self-healing") are README claims, not MNS evidence.
