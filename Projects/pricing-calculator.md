---
created: 2026-03-18
updated: 2026-03-18
tags: [revenue, tools, sales, quoting, cli]
---

# Pricing Calculator

> Quick quoting CLI tool. Run during discovery calls to generate instant package recommendations and a copy-paste price pitch.

## Status: LIVE

Repo: https://github.com/zerofluffnobs/pricing-calculator

## What it does

Interactive CLI questionnaire — 4–7 questions, ~60 seconds. Outputs:

- Recommended package tier + price range
- Scope summary in plain English
- Vertical-specific pitch note (trades / fitness / clinic / real estate)
- Upsell path to next tier
- Copy-paste price pitch sentence for the call
- Next-steps checklist (send one-pager → book scoping call → deposit invoice)

## Usage

```bash
# Interactive mode (live calls)
python calculator.py

# Demo mode (test / training)
python calculator.py --demo
```

No dependencies — pure Python stdlib. Runs anywhere.

## Services + pricing covered

| Service | Tiers | Price |
|---|---|---|
| AI Chatbot | Starter / Pro / Business | €400–€1,200 setup + €150–€400/mo |
| Workflow Automation | Single Flow / Bundle / Retainer | €300–€1,500 one-time or €500–€1,200/mo |
| Custom AI Agent | Integration / Agent / Pipeline / Hourly | €500–€8,000+ or €120–€180/hr |

Retainer tiers (Maintenance / Growth / Partner) surfaced as upsells.

Pricing matches service-packages.md and retainer-packages.md. Update `CHATBOT_TIERS`, `WORKFLOW_TIERS`, `AGENT_TIERS` dicts in calculator.py to change rates.

## Why this matters

Without this tool: creator has to mentally calculate and pitch pricing under pressure during a live call. Mistakes erode confidence.

With this tool: creator runs the script before or during the call, reads the copy-paste pitch sentence verbatim, looks sharp.

## Where to run it

- On any machine with Python 3.x (no install required)
- On the homelab once it's set up (`/srv/ai-repos/pricing-calculator/`)
- Clone to laptop: `git clone git@github.com:zerofluffnobs/pricing-calculator.git`
