# 05 — Research landscape
Snapshot: 2026-10-29. These projects informed the design. Repository descriptions are not execution evidence or independently verified trading performance. Source ledger: 11-sources-and-evidence.md.

| Project | Useful pattern | Intended use |
|---|---|---|
| TradingAgents | Specialist analysts, bounded disagreement, synthesis | Research-workflow reference |
| FinMem | Layered memories, importance and decay | Memory-lifetime experiments |
| Microsoft RD-Agent / RD-Agent-Quant | Propose, implement, evaluate factor/model candidates | Strategy laboratory, not order executor |
| Freqtrade + FreqAI | Crypto execution/backtesting and predictive retraining | Alternative foundation; training/inference separation |
| NautilusTrader | Event-driven simulation/live infrastructure and venue adapters | Execution default pending spike |
| Graphiti | Incremental temporal graph, provenance and hybrid retrieval | Runtime relational memory infrastructure |
| Graphify | Repo/docs graph skill or tool | Development-time navigation; verify exact project/CLI |
| Polymarket/agents | Prediction-market RAG/metadata examples | Reference only; prior lookup reported archived |
| CCXT / pybit | Exchange connectivity | SDKs behind stable adapters where needed |
| 3d-force-graph | Three.js/WebGL graph rendering | Orb dashboard |
| NATS JetStream | Durable transport/replay patterns | Event bus |
| LangGraph | Bounded, stateful workflows/checkpoints | Research orchestration |

## Design synthesis
Specialisation plus measurable feedback is more important than agent count. Keep learning and reasoning separate from deterministic order management. Use a small reusable worker pool and meaningful stored graph objects.

## Claims requiring re-check before reliance
Exact licenses/releases, supported order types/products, Graphify package/installation/output formats/Obsidian flags, repository archival date, current API tiers and account requirements.
Do not carry forward earlier precise star counts, model catalog names, fixed latency claims or performance figures as verified project facts.
A point-in-time retrieval system cannot remove knowledge already present in an LLM's pretrained weights. Document evaluation contamination limitations separately.

## Agent-KB practice
Use a concise root entrypoint, a task-to-file index, small focused references, explicit status and decision records, and task-specific playbooks. Avoid duplicating policy across many files. Agent-tool discovery and import behaviour must be verified per tool/version; no universal symlink/discovery rule is assumed.
