---
created: 2026-03-18
tags: [portfolio, demo, automation, pipeline, revenue]
---

# Portfolio: Workflow Automation Demo

**Repo:** https://github.com/zerofluffnobs/workflow-automation-demo
**Status:** Live, ready to show clients
**Complements:** chatbot-demo (github.com/zerofluffnobs/chatbot-demo)

## What It Is

A FastAPI app demonstrating a 5-step lead intake & triage automation pipeline:

1. **Validate & Normalize** — cleans input fields
2. **Classify Priority** — hot/warm/cold with confidence score and reasoning
3. **Enrich Lead** — detects industry, estimates budget tier, recommends service
4. **Route & Notify** — hot: Slack + email; warm: Slack; cold: CRM only
5. **Log to CRM** — timestamped record, queryable via GET /crm

## Modes

- **Stub mode** (default): keyword-based classification, works with no API keys
- **Live mode** (`ANTHROPIC_API_KEY` set): Claude Haiku classifies and enriches

## Why This Demo Works for Sales

- Clients can immediately see *their* lead types (fitness, trades, healthcare, etc.) correctly identified
- The full pipeline trace makes the automation tangible — not abstract
- Shows Slack/email routing that business owners actually want
- Budget tier estimates help frame the conversation: "your clients are worth €2k–5k"

## Industries Covered (Stub Mode)

healthcare, fitness, trades, hospitality, real_estate, legal, tech, retail

## Verified Working

Tested 2026-03-18:
- HOT lead (gym, "ASAP budget approved") → correct classification, Slack + email routed
- API returns full pipeline trace as JSON
- Health check, CRM log, CRM clear all working

## Next Enhancements (if needed)

- Add a simple HTML UI for visual demos in client calls
- Add POST /crm/export to download leads as CSV
- Connect real Slack webhook (one line change)
