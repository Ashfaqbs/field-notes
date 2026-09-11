# About Ashfaq

**GitHub:** [Ashfaqbs](https://github.com/Ashfaqbs) · **LinkedIn:** [b-s-mohammed-ashfaq](https://www.linkedin.com/in/b-s-mohammed-ashfaq/) · **Portfolio:** [ashfaqdevfolio.vercel.app](https://ashfaqdevfolio.vercel.app/)

*Sources: GitHub (115 public repos, READMEs, activity) + ashfaqdevfolio.vercel.app. Not scraped from LinkedIn.*

## Tagline

"Engineer Systems That Scale Beyond the Horizon" — Software Developer & System Engineer, AI-first engineering, based in Bengaluru.

## Core Stack

- **Languages:** Java, Python, JavaScript, Go
- **Backend:** Spring Boot 3, FastAPI, Express.js, Flask
- **Data:** PostgreSQL, MongoDB, Redis, Cosmos DB, vector DBs
- **Streaming/Infra:** Apache Kafka, Apache Flink, Apache Beam, Docker, Kubernetes
- **AI/ML:** RAG, agents, Model Context Protocol (MCP), ADK (Google Agent Development Kit), LLM tuning, small/local LLMs

## What Actually Stands Out (from repo evidence, not self-description)

### 1. A consistent habit of building MCP servers across infra domains
Not one MCP project — a pattern across five:
- **[SystemMind](https://github.com/Ashfaqbs/SystemMind)** — cross-platform OS diagnostics (Windows/macOS/Linux) exposed as MCP tools
- **[ContainMind](https://github.com/Ashfaqbs/ContainMind)** — container management (Docker/Podman) via MCP
- **[KafkaIQ](https://github.com/Ashfaqbs/KafkaIQ)** — Kafka cluster ops via MCP, with proactive health alerting
- **[apache-flink-mcp-server](https://github.com/Ashfaqbs/apache-flink-mcp-server)** (13 stars) — Flink cluster/job monitoring via MCP
- **[Model-Context-Protocol](https://github.com/Ashfaqbs/Model-Context-Protocol)** — reference implementation/notes on the protocol itself

The through-line: take an infra domain (OS, containers, Kafka, Flink) and give an AI assistant a safe, structured way to operate on it in natural language. This is a genuine specialty, not a one-off tutorial.

### 2. Real architecture design work, not just code
**[ai-lab](https://github.com/Ashfaqbs/ai-lab)** (most active repo, pushed within the last 2 days) is a documentation-only lab for system design proposals and architecture reviews:
- **KafkaMind** — a design for a grounded, multi-agent diagnostic system across multiple Kafka clusters, built explicitly to prevent LLM hallucination during incident response (every claim must trace to a real tool call). Builds on KafkaIQ.
- **InfraMask** — a design for a reversible browser extension that masks infra identifiers (IPs, hostnames, connection strings) before they reach an AI chat UI, restoring them in the response. Inspired by a similar tool at a prior employer.
- **mcp-grafana architecture review** — a file-cited teardown of how `grafana/mcp-grafana` (a real production MCP server) is actually built, with the generalized lessons extracted into a separate, reusable checklist.

This is the strongest content source: original architecture thinking, written with the discipline of "cite the file, don't guess."

### 3. Active open-source engagement, not just personal repos
Found in local contribution work (`C:\tmp\opensource\Contribution-projects`): a detailed design proposal posted to an Apache Flink Agents GitHub discussion, arguing for a "replay job" feature (replay recorded input against a savepoint to test agent/prompt changes safely before shipping). It's a real, current back-and-forth with a maintainer (@wenjin272), including open questions and explicit trade-offs — the kind of contribution that shows systems judgment, not just a PR.

### 4. Applied AI with a cost/engineering lens
**[TinyLLM-usecases](https://github.com/Ashfaqbs/TinyLLM-usecases)** (36 stars, most-starred repo) argues for small/local LLMs (<4B params) for tool-routing and classification instead of defaulting to frontier models, with a cost table showing a $30/month CPU server replacing $50k+/month in API costs at scale. Practical, contrarian-to-hype, and numbers-backed.

**[uber-querygpt-impl](https://github.com/Ashfaqbs/uber-querygpt-impl)** — a from-scratch rebuild of Uber's internal QueryGPT (NL-to-SQL) system, done specifically to understand it by building it rather than just reading the engineering blog.

### 5. System design as a teaching habit
**[system-design](https://github.com/Ashfaqbs/system-design)** (27 stars) — centralized notes and real-world architecture observations. **[Application-Programming-Interface](https://github.com/Ashfaqbs/Application-Programming-Interface)** (7 stars, actively updated) — a practical API reference spanning REST/GraphQL/gRPC with Spring Boot. Plus a current run of hands-on labs (Kubernetes, Kafka, GCP) pushed in the last week — visible "learning in public."

### 6. Developer tooling for other engineers
**[software-dev-ai-claude-toolkit](https://github.com/Ashfaqbs/software-dev-ai-claude-toolkit)** (24 stars) — a packaged Claude Code configuration (rules, commands, agents, skills, MCP servers) for backend/full-stack developers. Second most-starred repo; shows an instinct for building tools other developers actually adopt.

## Claims Carried From the Portfolio Site (unverified, worth confirming before quoting publicly)

- Official Microsoft Azure Cosmos DB Contributor
- 25+ published Medium articles, ~2/week publishing cadence

These came from ashfaqdevfolio.vercel.app, not from GitHub evidence directly — confirm actual Medium article count/links before the Medium subsystem is built, since we'll want to link to them.

## Repos Explicitly Not Featured

Tutorial-follow-alongs and course exercises (e.g. `HTML-And-CSS`, `Javascript`, `servlets`, `ProductCRUD`, `Google-Contacts-Clone-Springboot-and-Thyemleaf`) — real learning history, but not accomplishment content. Kept out of the strategy doc's backlog for that reason.
