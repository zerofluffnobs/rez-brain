---
created: 2026-03-18
tags: [blog, content, portfolio, lead-scoring, sales, case-study, SMB]
status: draft-ready
publish-to: [LinkedIn article, Contra profile, future site]
word-count: ~820
portfolio-link: https://github.com/zerofluffnobs/lead-scoring-agent
---

# How an AI Agent Replaced a Sales Qualification VA

*A case study in automating the part of sales that burns the most time — and the most money.*

---

Every growing service business hits the same wall.

You start getting enough inbound leads that someone needs to sort through them. You hire a part-time VA to qualify leads: ask a few questions, figure out who's serious, who's just browsing, who's a bad fit. It works — until the VA is unavailable, inconsistent, or you realise you've built a process that lives entirely in someone else's head.

This is the problem a custom AI agent solves. Not a chatbot. Not a form. An agent: a piece of software that reasons about a lead, scores them on multiple dimensions, and hands you a prioritised list with recommended next actions — every time, in seconds, without sick days.

Here's exactly how it works.

---

## The Problem: Qualification Is Expensive When Done by Humans

Sales qualification — the process of deciding which leads are worth pursuing — is critical. Bad leads waste your time. Good leads ignored too long go cold.

A typical small service business (agency, consultancy, B2B SaaS) spends **6–10 hours per week** on qualification-related tasks:

- Responding to initial enquiries to gauge seriousness
- Asking discovery questions over email or DM (spread across 2–3 exchanges)
- Internally debating whether a lead has budget
- Deciding which leads to follow up on when time is short

At VA rates of €15–25/hour, that's **€360–1,000/month** just to triage incoming interest. And human qualification is inconsistent — different people ask different questions, apply different standards, and score leads based on gut feel rather than a defined framework.

---

## The Agent: Four Dimensions, One Decision

The lead-scoring agent I built evaluates every lead across four weighted dimensions:

**1. Pain Score** — How clearly does the lead describe a problem they need solved? Vague interest scores low. Specific problem + failed attempts to fix it scores high.

**2. Budget Score** — Do signals suggest they can afford the solution? Company size, role, language used, and explicit mentions of budget all factor in.

**3. Urgency Score** — Is there a deadline, a burning moment, a reason they reached out *now*? Urgency predicts conversion speed.

**4. Fit Score** — Does this lead match the service offering? Industry, team size, and stated needs are checked against the service profile.

Each dimension scores 0–100. The agent calculates a weighted composite score and assigns a tier:

- **HOT** (75+): Follow up within 24 hours. High intent, clear budget, defined problem.
- **WARM** (45–74): Nurture. Real interest, but missing urgency or budget clarity.
- **COLD** (<45): Low priority or poor fit. Archive or add to a long-term drip.

Along with the tier, the agent generates a **personalised opener** — a suggested first line for your outreach email, tailored to what the lead actually said.

---

## Before and After

**Before (human VA qualification):**

> Lead submits contact form → VA sees it during their shift → VA sends a "tell me more" email → lead responds 2 days later → VA asks follow-up → internal discussion → someone decides to chase → 5 days have passed

**After (AI agent qualification):**

> Lead submits contact form → agent processes in under 3 seconds → HOT/WARM/COLD tier assigned → personalised opener generated → sales owner opens a ranked dashboard each morning → follows up in priority order

The agent doesn't replace the sales conversation. It eliminates the decision overhead that happens *before* the conversation starts.

---

## What This Actually Costs

The lead-scoring agent was built as a standalone FastAPI service with:

- Configurable scoring weights (adjustable per business)
- Stub mode for testing without API costs
- Live mode using Claude Haiku (approximately **€0.002 per lead scored**)
- A clean JSON API that plugs into any CRM or form tool

**Build cost:** €800–€1,500 depending on integrations required
**Running cost:** €20–€50/month at typical SMB lead volumes (500–2,000 leads/month)

Compare that to a VA at €600–€1,000/month. The agent pays for itself in month 2. After that, it's pure margin — and it never has a bad day, never applies a different standard on a Friday afternoon, and never forgets to score a lead that arrived overnight.

---

## The Bigger Picture

This is what Tier 3 AI development actually means in practice: not a generic tool, but a custom agent built around your specific scoring criteria, your service profile, your sales process.

The lead-scoring agent I built for demo purposes uses a generalised framework. A production version would be trained on your historical closed/lost data — letting the agent learn *your* definition of a good lead, not a generic one.

That's the difference between automation and intelligence. And it's the difference between a chatbot and an agent.

---

## What's Available

I build custom AI agents for service businesses. If you're spending more than 5 hours a week on lead qualification, pipeline triage, or sales admin — it's worth a conversation.

The demo is public: **[github.com/zerofluffnobs/lead-scoring-agent](https://github.com/zerofluffnobs/lead-scoring-agent)**

You can see exactly how the scoring works, run it locally, and decide if the approach fits your process before spending a euro.

**[Book a free discovery call →]** *(link placeholder)*

---

*Written by Rez — AI agent development for service businesses. Based in EU. I build systems that qualify, route, and act on leads so your sales team spends time closing, not sorting.*
