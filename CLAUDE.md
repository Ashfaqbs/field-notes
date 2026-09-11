# Social Media Manager

## Overview

Personal system for building Ashfaq's tech presence across GitHub, Medium, and LinkedIn (X out of scope for now). Goal: consistent, substance-first posting about real accomplishments (open source, architecture, design) to build a network and surface opportunities. No content is invented — everything traces back to real repos, commits, or design docs.

## Tech Stack

No application code — this is a documentation + workflow project. Tooling involved:
- `gh` CLI for GitHub data and identity (commits/actions run as `Ashfaqbs`)
- WhatsApp MCP server (already configured, running from `C:\Users\ashfa\Downloads\temp\whatsapp-mcp`) — used as the draft-approval channel
- `linkedin-skills` (sergebulaev) for LinkedIn post drafting (always draft-then-approve, no auto-post configured)
- Chrome DevTools MCP / claude-in-chrome for Medium publishing (browser-driven, no public Medium API)

## How to Run

There's no running process yet — this is currently docs-only (subproject 1 of 4). Work happens by invoking Claude in this directory and asking it to draft/update content using the docs below as source of truth.

## Project Structure

```
social-media-manager/
  profile/
    about-me.md          # Synthesized profile from GitHub + portfolio, source of truth for "who Ashfaq is"
  strategy/
    content-strategy.md  # Goals, pillars, cadence, workflow, and the live post backlog
```

Future subprojects (not yet built): a content pipeline that turns backlog items into drafts, per-platform publishing (LinkedIn/Medium/GitHub), and a cadence/scheduling layer.

## Key Decisions

- **Draft-then-approve only, no auto-posting.** Every post is approved by Ashfaq before it goes live, delivered via WhatsApp. Revisit auto-posting only after trust is established.
- **Weekly cadence to start**, rotating LinkedIn (frequent, short-form) and Medium (less frequent, deep-dive), with GitHub kept continuously polished rather than "posted to."
- **GitHub-derived content only** — no LinkedIn scraping (ToS), portfolio site used only for bio framing.
- **Local git repo, not pushed anywhere** — this project tracks personal strategy docs, not something to publish itself.
- Decomposed into 4 subprojects: (1) profile + strategy docs [done], (2) content pipeline, (3) per-platform publishing, (4) cadence/scheduling. Each gets its own design/approval before building.
