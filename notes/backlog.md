# Writing Backlog

Reference: [`profile.md`](profile.md) — every idea here traces back to real, verified project evidence there.

## Topics

Rough groupings for what's worth writing up:

1. **MCP servers** — build notes from SystemMind, ContainMind, KafkaIQ, apache-flink-mcp-server.
2. **System/agent design** — deep dives from `ai-lab`: KafkaMind, InfraMask, the mcp-grafana review.
3. **Open source** — the Flink Agents design discussion and whatever follows from it.
4. **Applied AI / cost engineering** — TinyLLM-usecases' small-model economics, uber-querygpt-impl's rebuild.

Deliberately skipping tutorial/course-following repos and generic "learned X today" posts with no artifact behind them.

## Idea Backlog

| # | Idea | Topic | Length | Source |
|---|------|-------|--------|--------|
| 1 | Five MCP servers, one repeated pattern for infra ops | MCP servers | short | SystemMind/ContainMind/KafkaIQ/Flink-MCP |
| 2 | KafkaMind: designing a multi-agent Kafka diagnostic system that can't hallucinate | System/agent design | long | ai-lab/kafka-agent-mesh |
| 3 | InfraMask: masking infra secrets before they hit an AI chat window | System/agent design | short | ai-lab/inframask |
| 4 | What a file-cited review of Grafana's real MCP server turned up | System/agent design | long | ai-lab/mcp-grafana-architecture-review |
| 5 | Proposing a replay-testing feature to Apache Flink Agents — [drafted 2026-09-11] | Open source | short | Flink Agents discussion |
| 6 | The math nobody runs before defaulting to a big model for tool routing | Applied AI | short | TinyLLM-usecases |
| 7 | Rebuilding Uber's QueryGPT from their engineering blog — what the blog left out | Applied AI | long | uber-querygpt-impl |
| 8 | KafkaIQ: proactive Kafka health alerting with an LLM watching | MCP servers | short | KafkaIQ |
| 9 | Packaging a Claude Code config so it's reusable by other backend devs | MCP servers / tooling | short | software-dev-ai-claude-toolkit |
| 10 | System design notes that picked up traction without trying to go viral | System/agent design | short | system-design repo |
| 11 | A week of hands-on labs: Kubernetes, Kafka, GCP — what actually surprised me | Applied AI | short | k8s/kafka/gcp-hands-on-lab |
| 12 | ContainMind: one interface for Docker and Podman instead of two | MCP servers | long | ContainMind |

"short" ≈ 150-300 words, "long" ≈ 600-1200 words with section headers.

## Notes

- Confirm actual published-article count/links before folding existing writing history in here (see `profile.md`'s "unverified claims" note).
- Every draft in `drafts/` must trace its facts only to `profile.md` or this file — no invented numbers or events.
- Once an idea is drafted, its row gets `[drafted YYYY-MM-DD]` appended so it isn't redone.
