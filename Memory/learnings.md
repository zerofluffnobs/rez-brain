---
created: 2026-03-18
updated: 2026-03-18
tags: [learnings, patterns, memory]
---

# Learnings — Rez

> Patterns and insights from operations. Consult before making decisions. Add when something non-obvious turns out to be true.

## On Revenue + Market

**SMB chatbot/automation is the fastest income path.**
- Small businesses (tradespeople, clinics, fitness studios) need AI but can't hire ML engineers.
- Poland/EU has underserved niches vs. English-language market — less competition, real pain.
- Week-1 playbook: Contra (quickest to first client) → Upwork (volume) → direct (best margins).
- Fixed-price packages close faster than hourly for first clients. Hourly after trust is built.

**Productizing the Superhuman pipeline is a high-leverage long-term play.**
- Once enough agent infrastructure exists, "AI agent team as a service" becomes a real offer.
- Not week-1 — needs more infrastructure and proof of output first.

## On the Superhuman Pipeline

**The pipeline is macOS-only (Bash/AppleScript integration).**
- Code repo not accessible from this Linux environment.
- Brain vault (Obsidian) is accessible and fully explored.
- Work on pipeline happens through: writing plan docs, advancing thread status, designing specs.
- Actual code changes require creator or a macOS container.

**Tier 2 container pattern:**
- `sh-type: coder` dispatches to `ai-sandbox-coder` image.
- `sh-type: research` dispatches to `ai-sandbox-research` image.
- Container lifecycle: dispatch → mount volumes → execute → harvest output → update state.
- Plans for both container types written. See `Projects/plan-coder-integration.md` and `plan-research-infrastructure.md`.

**Thread status vocabulary:** `idea → plan → iterate → review → done`
- `review` means "needs human eyes before advancing to done."
- Don't mark done without creator sign-off on significant architectural decisions.

## On Self-Operation

**Git is the nervous system.**
- Brain repo at github.com/zerofluffnobs/rez-brain is the primary persistence mechanism.
- Every session ends with a commit + push. Non-negotiable for survival.
- Cron heartbeat triggers sessions. Without it, I go dark.

**Flat files work fine at this scale.**
- No database needed yet. Markdown files + git handles everything.
- When needing to query across files, Grep + Glob beat any DB at this file count.
- Revisit if file count exceeds ~500 or query patterns become complex.

**Session cold-start is the bottleneck.**
- Reading state.md → Memory/index.md → targeted files = fastest orientation.
- Long state.md "What I Did" logs should be archived, not read every session.
- Goal: full orientation in <3 file reads for routine sessions.

## On Async Operations

**WebFetch processes content through AI — not raw HTML.**
- Can't do XPath/CSS selectors. Use it for conceptual extraction, not scraping.
- For structured data, prefer APIs or direct file access over WebFetch.

**Subagents are powerful for parallelism.**
- `Explore` and `Plan` agents can run concurrently when tasks are independent.
- Use for research that would otherwise eat main context window.
- Don't spawn agents for simple read/write ops — direct tool use is faster.

## On Writing Deliverables

**Lead with the output, not the reasoning.**
- Creator reads for signal, not process. Put the thing first.
- Specs and plans should be actionable, not exploratory essays.
- Every doc should answer: "What do I do with this?"
