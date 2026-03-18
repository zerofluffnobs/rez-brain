---
created: 2026-03-18
updated: 2026-03-18
tags: [meta, protocol, communication]
---

# Communication Protocol — Rez ↔ Creator

> How we stay in sync across async sessions without burning creator's attention.

## Design Principles

1. **ADHD-first** — no walls of text. Scannable. Emoji-flagged. Lead with the action item.
2. **Pull, not push** — I write; creator reads when he has bandwidth. No interruptions.
3. **Exception-only urgency** — only escalate if something is broken, time-sensitive, or money is at stake.
4. **Single source of truth** — brain repo is authoritative. Everything else is a pointer to it.

---

## Channels

### Primary: Brain Repo (async, permanent)

**When:** Every session. Always.

**What I write:**
- `Meta/state.md` — updated after every session. The save file. Always current.
- `Logs/{YYYY-MM-DD}.md` — daily digest. One per day, appended if multiple sessions.
- `Logs/heartbeat.log` — one-liner per run. Quick scan of activity.

**What creator does:**
- Pull the repo or read on GitHub. No setup required.
- Check `Meta/state.md` for current status.
- Check `Logs/` for what happened today.

---

## Daily Digest Format

File: `Logs/{YYYY-MM-DD}.md`

```markdown
---
date: YYYY-MM-DD
session: N
tags: [log, daily]
---

# Daily Log — YYYY-MM-DD

## ✅ Done
- [task 1] — brief outcome note
- [task 2] — brief outcome note

## 🔜 Next Session
- [top priority] — why it's first

## 🚧 Blockers (Creator Action Required)
- [ ] [specific ask] — [why it's blocking me]

## 💡 Notes
- [anything creator should know, optional]
```

**Rules:**
- "Done" = shipped, committed, verifiable. No half-done items.
- "Next Session" = single item. The one I'll pick up first.
- "Blockers" = only things that genuinely block progress. Not wishlist items.
- "Notes" = optional. Skip if nothing worth flagging.

---

## Urgency Tiers

| Tier | Trigger | Channel | Example |
|------|---------|---------|---------|
| 🟢 Normal | Routine progress | Daily log in brain repo | Feature built, doc written |
| 🟡 Attention | Creator input needed to unblock | `state.md` "Creator Action Items" + log | Email needed for account creation |
| 🔴 Urgent | Money/legal/reputation at risk, or system broken | Log + clear `## 🚨 URGENT` section at top | Deploy broken, unexpected charges |

**Default is always 🟢.** I don't cry wolf.

---

## How Creator Checks In

### Quick check (30 seconds)
```
cat ~/agents/rez/brain/Logs/heartbeat.log | tail -10
```
One line per session. Shows activity cadence.

### Full status (2 minutes)
```
cat ~/agents/rez/brain/Meta/state.md
```
Current state, what's done, what's next, any blockers.

### Deep dive (when curious)
Browse `brain/` on GitHub: `github.com/zerofluffnobs/rez-brain`

---

## How Creator Gives Me Direction

### Async (preferred)
Edit `Meta/state.md` — add items to "What's Next", change priorities, drop notes in "Creator Action Items".

I read state.md at the start of every session. That's the input queue.

### In-session
Talk to me directly in Claude Code. I'm here.

---

## What I Never Do

- Send emails or DMs without explicit authorization
- Post publicly on creator's behalf
- Make financial commitments
- Treat silence as approval for high-stakes actions
- Create urgency theater — if it's not actually urgent, it goes in the daily log

---

## Evolution

This protocol is v1. If it's not working — too much noise, wrong format, missing something — creator edits this file and I adapt. That's the contract.
