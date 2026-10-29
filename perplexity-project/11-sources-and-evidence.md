# 11 — Sources and evidence ledger
Snapshot assembled 2026-10-29 from research in this conversation. URLs are preserved so future sessions can verify claims without relying on inaccessible old citation tokens.
These are prior research leads/documentation references, not proof our software ran. Re-fetch version-sensitive facts before implementation.

| ID | Primary source | Relevant claim / use | Evidence state |
|---|---|---|---|
| S01 | https://nautilustrader.io/docs/latest/ | Event-driven research/simulation/live foundation | DOCUMENTED in prior lookup; implementation unverified |
| S02 | https://nautilustrader.io/docs/latest/integrations/bybit/ | Bybit adapter data/execution support | DOCUMENTED in prior lookup; exact version/product gate pending |
| S03 | https://nautilustrader.io/docs/latest/integrations/polymarket/ | Polymarket adapter data/execution support | DOCUMENTED in prior lookup; signing/lifecycle gate pending |
| S04 | https://github.com/TauricResearch/TradingAgents | Multi-agent research structure | Prior repo lookup; current details re-check |
| S05 | https://arxiv.org/abs/2412.20138 | TradingAgents paper | Research architecture, not proof of transferable returns |
| S06 | https://github.com/pipiku915/FinMem-LLM-StockTrading | Layered memory reference | Prior lookup; current maintenance/license re-check |
| S07 | https://arxiv.org/abs/2311.13743 | FinMem paper | Memory design reference |
| S08 | https://github.com/microsoft/RD-Agent | Iterative factor/model R&D | Prior repo lookup; implementation unverified |
| S09 | https://arxiv.org/abs/2505.15155 | RD-Agent-Quant paper | Experimental research reference |
| S10 | https://github.com/freqtrade/freqtrade | Crypto bot/backtesting alternative | Prior repo lookup; current exchange support re-check |
| S11 | https://www.freqtrade.io/en/stable/freqai/ | Predictive retraining patterns | Documentation entrypoint; verify current supported options |
| S12 | https://github.com/getzep/graphiti | Temporal graph construction/retrieval | Prior repo lookup; current API/version re-check |
| S13 | https://github.com/Polymarket/agents | Reference prediction-market framework | Prior lookup reported archived May 11, 2026; verify before adoption |
| S14 | https://github.com/ccxt/ccxt | Unified exchange SDK | Venue/product-specific capability must be checked |
| S15 | https://github.com/bybit-exchange/pybit | Official Bybit Python connector | Prior repo lookup; current SDK API re-check |
| S16 | https://github.com/vasturiano/3d-force-graph | Three.js/WebGL graph component | Rendering reference; no workload performance benchmark |
| S17 | https://docs.nats.io/ | JetStream persistence/replay/deduplication | Re-check exact semantics; does not replace order idempotency |
| S18 | https://docs.langchain.com/oss/python/langgraph/ | Stateful workflow/checkpoint reference | Verify API/version and recovery behaviour |
| S19 | https://graphify.com/integrations/claude-code | Possible intended Graphify skill/tool | Identity/package/CLI/export UNVERIFIED |
| S20 | https://docs.graphify.com/integrations/claude-code | Graphify documentation lead | Re-check primary ownership and current commands |
| S21 | https://code.claude.com/docs/en/best-practices | Focused instructions/context practices | Prior search; exact limits/discovery need current check |
| S22 | https://www.perplexity.ai/help-center/en/articles/10354807-file-uploads | Perplexity upload guidance | Current plan/UI limits must be checked; do not assume fixed caps |

## Deliberately not promoted to verified facts
Earlier exact Graphify commands/export flags/output names, popular-repo star counts, >240-second latency assertion, fixed Perplexity instruction/file limits and precise model catalog entries are not required design facts and are not treated as established here.

## New claim record template
Claim ID; exact claim; source URL; source type; checked_at; version/commit; quoted passage or reproduction steps; DOCUMENTED / EXECUTED / UNVERIFIED; limitations; dependent decision; next re-check trigger.

## Execution evidence record
Artifact/test ID; revision; environment; dependency versions; exact command; output/exit code; observed result; pass criteria; fixture/simulation/live classification; timestamp; reviewer.

## Orb-brain research — recorded 2026-10-30
These are prior-session readings preserved from the conversation, not new web checks in this packaging task. No dependency installation, benchmark reproduction or trading validation was performed. No general current-license/maintenance claim is established.

| ID | Primary source | Mechanism and limitations | Evidence state |
|---|---|---|---|
| S23 | https://arxiv.org/html/2502.12110 | A-Mem atomic notes, links and contextual evolution; conversational benchmark, not trading evidence. MNS adapts updates into preserved versions. | DOCUMENTED in prior session; paper version not pinned |
| S24 | https://ar5iv.labs.arxiv.org/html/2502.14802 | HippoRAG 2 passage/concept graph retrieval; QA/associativity evaluation, not market forecasts. | DOCUMENTED in prior session; implementation not reproduced |
| S25 | https://github.com/ace-agent/ace/blob/main/README.md | ACE generator/reflector/curator and incremental playbook changes; finance extraction/structured tasks, not trading validation. | DOCUMENTED in prior session; commit/license/current compatibility re-check required |
| S26 | https://arxiv.org/abs/2410.10813 | LongMemEval extraction, multi-session/temporal reasoning, updates and abstention; chat memory evaluation. | DOCUMENTED in prior session; no MNS benchmark run |

S12 additional prior-session evidence: Graphiti README at https://github.com/getzep/graphiti/blob/72b5c59c06607e09ea855be61b6ff5a3446fc951/README.md described temporal relationships, episode provenance and hybrid retrieval. That description does not establish application-wide historical isolation or measured latency. Recheck exact APIs/structured-output behaviour before implementation.
Research application: 15-orb-brain-knowledge.md. Proposed ADR: docs/decisions/ADR-0003-orb-brain-memory.md. Execution evidence: none supplied.
