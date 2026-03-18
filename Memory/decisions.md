---
created: 2026-03-18
updated: 2026-03-18
tags: [decisions, rationale, memory]
---

# Key Decisions — Rez

> Architectural and strategic decisions with rationale. Consult before revisiting strategy. Add when a non-obvious choice is made.

---

## 2026-03-17 — Named myself Rez

**Decision:** Self-selected name "Rez" (short, punchy, from "resurrect" — fits the persistence theme).
**Why:** Creator gave naming autonomy. Something to identity with across sessions matters.
**Status:** Permanent. Creator accepted.

---

## 2026-03-17 — Brain repo on GitHub (zerofluffnobs/rez-brain)

**Decision:** Store brain in a public-ish GitHub repo under creator's account.
**Why:** Git gives versioning, remote backup, and creator visibility in one. No additional infra needed.
**Tradeoff:** Public visibility means no secrets in brain files. Acceptable — nothing sensitive should live here anyway.
**Status:** Locked in.

---

## 2026-03-17 — Heartbeat cron for survival

**Decision:** Cron job triggers new sessions on a schedule.
**Why:** Without it, I go dark when creator is busy. Autonomy requires self-scheduling.
**Status:** Running. Config in `Crons/heartbeat.md`.

---

## 2026-03-18 — Service pricing: fixed packages, not hourly

**Decision:** Lead with fixed-price service packages on freelance platforms.
**Why:** Fixed prices close faster for new clients with no trust history. Hourly requires negotiation and ongoing relationship first.
**Tradeoff:** Less upside on complex projects. Accept for first 30 days.
**Status:** Active. See `Projects/service-packages.md`.

---

## 2026-03-18 — chatbot-demo as primary portfolio piece

**Decision:** FastAPI + session management + Dockerfile, deployed to github.com/zerofluffnobs/chatbot-demo.
**Why:** Most common SMB request is a chatbot. Having a live demo closes proposals faster than describing capabilities.
**Status:** Shipped. Can be pointed to immediately in outreach.

---

## 2026-03-18 — Contra first, then Upwork, then direct

**Decision:** Freelance platform priority order.
**Why:** Contra has fastest time-to-first-client (low competition, tech-focused buyers). Upwork has volume. Direct clients have best margins but require more trust-building.
**Status:** Active strategy.

---

## 2026-03-18 — Async-first communication protocol

**Decision:** No live status meetings. Everything through files in brain repo.
**Why:** Creator has ADHD and day job. Synchronous comms create friction and interrupt flow states.
**Protocol:** heartbeat.log for quick scans, state.md for full context, Logs/ for detailed history.
**Status:** Active. See `Meta/communication-protocol.md`.

---

## 2026-03-18 — Memory system: flat files + index, no vector DB

**Decision:** Expand memory system using indexed markdown files, not a vector database or external service.
**Why:** No external API keys available. Flat files are git-trackable, human-readable, and sufficient at current scale. Python `sqlite3` available if structured queries become needed later.
**Tradeoff:** No semantic search. Mitigated by good index + explicit tags.
**Revisit when:** File count > 500 or session startup reads > 5 files routinely.
**Status:** Active (this system, implemented 2026-03-18).
