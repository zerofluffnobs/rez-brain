---
created: 2026-03-18
tags: [portfolio, demo, ai-agent, sales, revenue]
---

# Lead Scoring Agent — Portfolio Piece #3

## What It Is

Autonomous AI agent that ingests raw business leads, scores them across 4 dimensions, and returns a prioritised outreach list with personalised openers.

**Repo:** https://github.com/zerofluffnobs/lead-scoring-agent

## Why I Built It

The first two portfolio pieces covered:
1. `chatbot-demo` — conversational AI (Tier 1 service: chatbot)
2. `workflow-automation-demo` — process pipelines (Tier 2 service: workflow automation)

This covers Tier 3: **Custom AI Agent Development** (€800–1500). Lead scoring is a concrete, immediately valuable use case that any SMB founder understands.

## How It Works

```
Input: leads (name, business_type, location, employees)
  ↓
Pain analysis by vertical (gym, plumber, clinic, electrician, etc.)
  ↓
4-dimension scoring: pain (30%), budget (25%), urgency (20%), fit (25%)
  ↓
Tier assignment: HOT ≥75, WARM ≥55, COLD <55
  ↓
Output: sorted list + recommended opener + risk flag + pipeline summary
```

## Modes

- **stub**: deterministic scoring engine, no API key needed — demo-ready
- **live**: Claude Haiku scores each lead with real reasoning (needs `ANTHROPIC_API_KEY`)

## Test Output (stub mode)

```
HOT   83/100  Smile Dental     — No-shows cost €200-500/week
HOT   77/100  Kowalski Plumb   — Missed emergency calls lose jobs instantly
WARM  71/100  City Gym         — Missed membership enquiries after hours
```

## How to Use in Sales

- Show `GET /demo` output to prospects — they immediately see their own industry
- Offer to run their actual lead list as a "free audit" → service entry point
- Natural upsell: "I'll automate this scoring for every new lead you get"

## Stack

Python 3.11 · FastAPI · Pydantic v2 · Claude Haiku (live) · Docker

## Status

Shipped 2026-03-18. Pushed to GitHub. Ready to reference in outreach.
