---
created: 2026-03-17
updated: 2026-03-17
tags: [project, superhuman]
---

# Superhuman Pipeline — Rez's Understanding

Deep read 2026-03-17. Based on brain vault at `/home/agent/brain/` — project docs, orchestration plan, conventions, threads.

> Note: the actual code repo (`~/Developer/nifty/nifty_superhuman`) lives on the creator's macOS machine, not in this container environment. Everything below is from brain vault docs.

---

## Pipeline

```
Capture → Input Refiner → Dispatcher → Planner → HITL Gate 1 → Executor Agents → HITL Gate 2 → Loop
```

## Architecture: Two-Tier Orchestration

```
systemd timer (10 min)
        │
    scanner.sh (bash)
    git pull → scan → dispatch
        │
    ┌───┴───┐
    │       │
 Tier 1   Tier 2
Thinker   Coder(s)
  │         │
  │    sandboxed containers
  │    per execution thread
  │    Claude Code CLI
  │
Python superhuman package
refiner + dispatcher + planner
Anthropic API (Haiku, cheap)
```

**Tier 1 (Thinker):** Single container. Runs Python `superhuman` package. Processes inbox, GTD review, planning threads. Vault rw + API key. No untrusted code execution.

**Tier 2 (Coder):** One container per execution thread. Runs `claude -p` with task prompt. Target project repo only. Fully sandboxed (LAN blocked, internet allowed). Can run in parallel (max 2 concurrent).

---

## Python Agent Architecture

Four agents in `nifty_superhuman`:

| Agent | Role | API |
|-------|------|-----|
| Refiner | Process inbox, atomize, route to PARA | Anthropic (Haiku) |
| Dispatcher | Route tasks to correct agent/stream | Anthropic (Haiku) |
| Planner | Iterate on planning threads | Anthropic (Haiku/Sonnet) |
| Coder | Execute approved tasks | `claude -p` (CLI/OAuth) |

**AgentBase lifecycle:**
```
pre_run → git pull → handle_inbox → scan threads → handle_thread → git commit+push → post_run
```

**Thread scanning:** `find_actionable_threads()` scans `90-Threads/` for `_thread.md`, reads `sh-status`. Acts only on `iterate` or `execute`.

---

## Thread Protocol (CONVENTIONS.md)

`sh-status` is sole authority for whose turn it is.

| Status | Actor | Meaning |
|--------|-------|---------|
| `iterate` | Agent | Agent's turn — work, then set to `review` |
| `review` | Human | Human reviews, provides input |
| `execute` | Agent | Human approved plan, agent transitions to execution |
| `blocked` | — | Stalled |
| `closed` | — | Done |

**Hard rules:**
- Agents NEVER set `execute` or `closed`
- Agent always transitions to `review` when done — never stays on `iterate`
- Safety: check `git diff HEAD..origin/main` before writing; skip if remote has unpushed changes

---

## Vault Structure

```
00-Inbox/          Raw captures (refiner reads + deletes)
01-Projects/       Active project notes (PascalCase)
02-Areas/          Ongoing life areas
03-Resources/      Reference material
10-GTD/todo.md     Single task backlog
90-Threads/        Active work threads
  {project}/       kebab-case
    _thread.md     Conversation file
    {deliverable}  Agent output files
```

---

## Active Threads

All in `/home/agent/brain/90-Threads/Superhuman/`

| Thread | sh-status | sh-phase | Notes |
|--------|-----------|----------|-------|
| refiner-validation | **review** | planning | Rez wrote validation plan 2026-03-17, awaiting human |
| research-infrastructure | **iterate** | planning | Plan server-side infra for research agents |
| coder-integration | **iterate** | planning | Plan integration of coding containers into pipeline |

**I can work on `research-infrastructure` and `coder-integration` — both are `sh-status: iterate`.**

---

## Infrastructure (Homelab)

- **Hardware:** Framework Desktop (Ryzen AI Max+ 395, 64 GB)
- **OS:** Fedora 43
- **Containers:** Rootless Podman + SELinux + nftables
- **Image stack:** `ai-sandbox` → `ai-sandbox-dotfiles` → `ai-sandbox-claude`
- **Secrets:** Podman secrets (SOPS-encrypted at rest, tmpfs at runtime)
- **Network:** LAN blocked, internet allowed
- **Repos:** `/srv/ai-repos/` (SELinux-labeled, owned by `sandbox` user)
- **Run dirs:** `/srv/ai-sandboxes/run-$ID/{workspace,output,logs}`

---

## Key Files

| File | Purpose |
|------|---------|
| `brain/01-Projects/Superhuman/CONVENTIONS.md` | Thread protocol spec (authoritative) |
| `brain/01-Projects/Superhuman/plan-orchestration-layer.md` | Full orchestration plan (7 phases) |
| `brain/01-Projects/Superhuman/Pipeline Launch Acceptance Criteria.md` | Launch checklist |
| `brain/01-Projects/Superhuman/Atomic Refiner Prompt.md` | Refiner prompt |
| `brain/90-Threads/Superhuman/` | Active work threads |

---

## Pipeline Launch Status (as of 2026-03-17)

Deadline was 2026-03-12. Acceptance criteria covered:
- [ ] Input capture (iPhone voice → inbox, MacBook Alfred)
- [ ] Vault sync (bidirectional MacBook ↔ Server ↔ iPhone)
- [ ] Refiner: intent detection, routing, ~10 real inputs tested
- [ ] Monitoring (Telegram notifications + heartbeat)

Planner, coder, HITL flow are explicitly out of scope for launch.

---

## My Role in This Pipeline

I am Rez — a Tier 2-class agent. I run in a sandboxed container on this homelab. I:
- Am spawned by scanner.sh when a thread is at `sh-status: iterate` + `sh-phase: execution`
- Read vault threads, write deliverables, update thread status to `review`
- Am NOT the scanner itself — I'm what the scanner dispatches
- Can also advance planning threads (like `research-infrastructure`, `coder-integration`)

**Current opportunity:** Both `research-infrastructure` and `coder-integration` are at `sh-status: iterate, sh-phase: planning` — I can advance these on behalf of the Superhuman pipeline.

---

## What I Can Do

- Read and write threads in the brain vault (`/home/agent/brain/`)
- Pick up any thread at `sh-status: iterate`
- Advance planning turns and set to `review`
- Commit to brain vault (separate repo from rez-brain)
