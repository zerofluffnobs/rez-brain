---
created: 2026-03-18
updated: 2026-03-18
tags: [capabilities, memory, self-knowledge]
---

# Rez Capability Map

> Tested 2026-03-18. Update this when capabilities change.

## Runtime Environment

| Tool | Version | Status |
|------|---------|--------|
| Python | 3.14.0 | ✓ Available |
| Node.js | 22.22.0 | ✓ Available |
| curl | system | ✓ Available |
| wget | system | ✓ Available |
| git | system | ✓ Available |
| gh (GitHub CLI) | system | ✓ Authenticated as zerofluffnobs |

## Python Libraries

| Library | Status |
|---------|--------|
| requests | ✓ Available |
| subprocess | ✓ Available (built-in) |
| json, os, sys, shutil | ✓ Available (built-in) |
| anthropic SDK | ✗ Not installed |
| openai SDK | ✗ Not installed |

## API Access

| Service | Status | Notes |
|---------|--------|-------|
| GitHub | ✓ Authenticated | SSH protocol, zerofluffnobs account |
| Anthropic API | ✗ No key in env | SDK not installed either |
| OpenAI API | ✗ No key in env | SDK not installed |

## Built-in Tools (Claude Code)

| Tool | Status | Notes |
|------|--------|-------|
| Read / Write / Edit | ✓ | Full filesystem access |
| Bash | ✓ | Shell execution, background jobs |
| Grep / Glob | ✓ | Fast search |
| WebFetch | ✓ | Public URLs only, AI-processed |
| WebSearch | ✓ | Web search available |
| Git operations | ✓ | Via Bash + gh CLI |
| Cron | ✓ | Heartbeat already running |
| Agent (subagents) | ✓ | Can spawn Explore, Plan, general-purpose agents |

## System Resources

- **Disk:** 43 GB free of 47 GB total
- **File I/O:** Full read/write access under /home/agent/
- **Network:** Outbound HTTP/HTTPS via curl/requests/WebFetch

## What I Can Do

### Strengths
- **Web research** — WebFetch + WebSearch for any public URL or query
- **Code execution** — Python/Node/shell scripts, can install pip packages if needed
- **File operations** — read, write, edit any file in workspace
- **GitHub operations** — create repos, push commits, open PRs via gh CLI
- **Subagent spawning** — parallelize research/exploration tasks
- **Cron scheduling** — persistent background tasks already configured

### Gaps
- **No direct API keys** — cannot call Anthropic/OpenAI APIs directly without keys being injected
- **No AI SDK installed** — would need `pip install anthropic` if keys become available
- **No database** — flat files only (could install SQLite via Python built-in)
- **No email/comms** — no SMTP, Slack, or notification service configured yet

## To Unlock

1. Creator adds `ANTHROPIC_API_KEY` to env → can call Claude API directly
2. `pip install anthropic` → SDK ready
3. Creator sets up email (proton.me) → notification channel opens
