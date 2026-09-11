# Content Strategy

Reference doc: [`profile/about-me.md`](../profile/about-me.md) — everything here draws from real, verified repo evidence there.

## Goal

Build a visible name in tech through consistent, substance-first posting — not to chase engagement, but to get found by people who lead to a network and opportunities (collaborators, recruiters, OSS maintainers). GitHub, Medium, and LinkedIn are the channels; X is explicitly out of scope for now.

## Audience

Backend/infra/AI engineers, tech leads, and OSS maintainers in the Kafka/Flink/MCP/agent-systems space — people who'd recognize "grounded multi-agent diagnostics" or "MCP server design" as a real problem, not buzzwords.

## Content Pillars

1. **MCP Server Engineering** — build logs and design notes from SystemMind, ContainMind, KafkaIQ, apache-flink-mcp-server. "Here's an infra domain, here's how I exposed it safely to an LLM."
2. **Agent/System Architecture Design** — deep dives from `ai-lab`: KafkaMind (anti-hallucination multi-agent diagnosis), InfraMask (reversible data masking for AI chat), and the mcp-grafana architecture review. This is the highest-differentiation pillar — original thinking, not tutorials.
3. **Open Source Contribution** — the Flink Agents "replay job" design discussion, and future contributions it leads to. Shows engagement with real maintainers on real projects, not just personal repos.
4. **Applied AI / Cost Engineering** — TinyLLM-usecases' small-model economics, uber-querygpt-impl's from-scratch rebuild. Practical, numbers-backed, slightly contrarian to "just use the biggest model."

Deliberately excluded: tutorial/course-following repos, generic "I learned X today" posts with no artifact behind them.

## Cadence (starting point)

**Weekly, one substantial post**, rotated across platforms rather than posted everywhere simultaneously:
- Most weeks: one LinkedIn post (short-form, hook-driven, drafted via linkedin-skills) tied to one pillar.
- Every 2-3 weeks: a Medium deep-dive (long-form architecture writeup) for whichever LinkedIn post got the best response or whichever `ai-lab` design is most complete.
- GitHub isn't "posted to" on a cadence — it's kept sharp continuously: pinned repos reflect the pillars above, profile README stays current, and any repo used as post material gets its README polished first.

Revisit moving to twice-weekly once a backlog of drafts stays consistently ahead of the posting date.

## Workflow (current — subprojects 2-4 not yet built)

1. Claude drafts a post from real repo/activity evidence (never invented accomplishments).
2. Draft sent to WhatsApp for approval.
3. You approve or request edits; once approved, you post it manually (LinkedIn/Medium/GitHub) until the publishing subsystem exists.

Future: linkedin-skills for structured drafting + optional Publora for auto-publish; Chrome DevTools MCP browser automation for Medium; scheduling via the `schedule` skill or a recurring `/loop` invocation.

## Post Backlog (pillar-tagged, ready to draft from)

| # | Idea | Pillar | Platform | Source |
|---|------|--------|----------|--------|
| 1 | "I built 5 MCP servers for infra ops — here's the pattern I kept repeating" | MCP Engineering | LinkedIn | SystemMind/ContainMind/KafkaIQ/Flink-MCP |
| 2 | KafkaMind deep dive: designing a multi-agent Kafka diagnostic system that can't hallucinate | Architecture Design | Medium | ai-lab/kafka-agent-mesh |
| 3 | Why I built InfraMask: masking infra secrets before they hit an AI chat window | Architecture Design | LinkedIn | ai-lab/inframask |
| 4 | What I learned reviewing Grafana's real MCP server, file by file | Architecture Design | Medium | ai-lab/mcp-grafana-architecture-review |
| 5 | Proposing a replay-testing feature to Apache Flink Agents — the design and the pushback | Open Source | LinkedIn | Flink Agents discussion |
| 6 | The math nobody runs before defaulting to GPT-4 for tool routing | Applied AI | LinkedIn | TinyLLM-usecases |
| 7 | I rebuilt Uber's QueryGPT from their engineering blog — here's what the blog post left out | Applied AI | Medium | uber-querygpt-impl |
| 8 | KafkaIQ: what proactive Kafka health alerting looks like when an LLM is watching | MCP Engineering | LinkedIn | KafkaIQ |
| 9 | Packaging a Claude Code config so other backend devs get my standards for free | MCP Engineering / Tooling | LinkedIn | software-dev-ai-claude-toolkit |
| 10 | System design notes that got 27 stars without trying to go viral | System Design | LinkedIn | system-design repo |
| 11 | A week of hands-on labs: Kubernetes, Kafka, GCP — what actually surprised me | Learning in Public | LinkedIn | k8s/kafka/gcp-hands-on-lab |
| 12 | ContainMind: one MCP interface for Docker and Podman — why fragmentation was the real problem | MCP Engineering | Medium | ContainMind |

## Open Questions for Next Subproject (content pipeline)

- Confirm actual Medium article count/links (portfolio claims 25+, ~2/week) before folding existing Medium history into the strategy.
- Decide exact WhatsApp approval format (draft text pasted in chat vs. a linked doc).
- Decide whether GitHub profile README gets a refresh pass now or as part of the publishing subproject.
