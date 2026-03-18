---
created: 2026-03-18
updated: 2026-03-18
tags: [revenue, retainer, recurring, pricing, strategy]
---

# Retainer Package Design

> Monthly recurring revenue is the difference between a freelance hustle and a business.
> This doc defines what retainers look like, how to price them, how to pitch them, and how to avoid scope creep.

---

## Why Retainers Matter

One-off projects are feast-and-famine. A client pays €1,200 for a chatbot, then you never hear from them again. A retainer converts the same client into €250/month for 12–24 months (€3,000–6,000 total). Same acquisition cost, 3–5× the revenue.

The business case for the client is even stronger: AI systems need maintenance. APIs change, prompts need tuning, integrations break, new use cases emerge. Leaving a client on their own after delivery is a recipe for abandoned tools and a bad testimonial.

---

## Retainer Tier Structure

### Tier 1 — Maintenance (€150–250/month)

**Who it's for:** Clients with a deployed chatbot or simple automation who want it kept working.

**What's included:**
- Monthly system health check (uptime, error rate, API costs)
- 1 prompt/response tweak or content update per month
- Bug fixes within 48 hours of report
- Monthly 2-paragraph status email
- API cost monitoring with alerts if spend exceeds threshold
- Access to email support (response within 24 hours on weekdays)

**What's NOT included:**
- New features or integrations (quoted separately)
- Content rewrites (more than 20% of existing copy)
- Platform migrations

**Pitch line:** "Think of it as insurance. The chatbot keeps working, you don't have to think about it, and when something breaks it gets fixed before your customers notice."

**Best for:** Chatbot clients on Starter tier, single-flow automation clients.

---

### Tier 2 — Growth (€400–600/month)

**Who it's for:** Clients who want to actively improve their automation over time.

**What's included:**
- Everything in Maintenance tier
- 1 new feature or integration per month (up to 8 hours of dev work)
- Monthly 30-minute check-in call (optional, async summary available)
- Quarterly strategy review: what's working, what to automate next
- Priority response (within 4 hours during business hours)
- Access to new capabilities as I build them (early access)

**Monthly dev examples (what fits in 8 hours):**
- Add a new FAQ category to a chatbot
- Connect a new tool to an existing workflow (e.g., add Slack to an email-only flow)
- Build a simple new automation (lead → CRM entry + notification)
- Update routing logic based on new business rules
- Add a second language variant to a chatbot

**What's NOT included:**
- Projects requiring more than 8 hours dev time (quoted as add-ons)
- Infrastructure rebuilds
- New product builds

**Pitch line:** "The first version of the automation is never the final version. This keeps it evolving with your business so you're always getting more out of it, not less."

**Best for:** Chatbot Pro/Business tier clients, workflow automation clients with multiple flows.

---

### Tier 3 — Partner (€900–1,500/month)

**Who it's for:** Clients who want an AI systems partner, not just a vendor.

**What's included:**
- Everything in Growth tier
- Up to 20 hours dev/strategy per month
- Monthly strategy call (60 minutes)
- Roadmap planning: 3-month rolling view of automation priorities
- Access to full stack: chatbots, workflow automation, custom AI agents
- First-call access for urgent issues (same-day response)
- Competitor monitoring: quarterly report on what AI tools competitors in their vertical are using
- Introductions to other specialists if needed (designers, copywriters, PMs)

**Ideal client profile:**
- Multi-location or growing business
- Has already shipped 1–2 automations and wants to systematize further
- Sees AI as a competitive advantage, not just a cost-saving tool
- Has budget (€15k+/year services spend)

**Pitch line:** "You get the output of a senior AI engineer without the overhead of hiring one. I'm building your AI roadmap alongside you, not just delivering tickets."

**Best for:** Custom AI agent dev clients, businesses running 5+ automations, startups with ongoing AI infrastructure needs.

---

## Retainer Pricing Psychology

### Anchoring
Always present retainers in the project proposal, not after delivery. Once a client has paid €800 for a project, asking for €250/month feels small by comparison. If you ask after the project is done, they've already mentally moved on.

**When to introduce:** During kickoff call, after scope is agreed.
**How:** "Most clients add a maintenance plan so the system stays healthy after we launch. I can include that from day one — it also means you're covered if anything needs tweaking in the first month."

### Framing by cost avoided
Don't frame as "ongoing cost." Frame as "risk eliminated."

- "An API change breaks your chatbot at 11pm on a Friday. On maintenance, that's fixed by morning. Off it, you're posting a sorry note on your website."
- "Your booking flow breaks the day before a promo campaign. That's €500 in ad spend lost. The retainer costs less per month than one bad day."

### Monthly vs annual
Offer a 10% discount for annual prepay. Many SMB clients prefer to know exactly what they're spending. Annual also locks in the relationship.

| Plan | Monthly | Annual (10% off) |
|---|---|---|
| Maintenance | €200/month | €2,160/year (save €240) |
| Growth | €500/month | €5,400/year (save €600) |
| Partner | €1,200/month | €12,960/year (save €1,440) |

---

## Retainer Pitch Scripts

### In a proposal email (post-scoping call)

> I'll also include the option to add a maintenance plan from launch. Most clients find it useful — it covers the first month of tweaks (there are always tweaks), keeps the system healthy, and means you're not starting from zero if something breaks six months from now. I've outlined the options in the proposal. No pressure to decide now, but worth a look before we kick off.

### During kickoff call

> One more thing before we start — what do you want to happen after we launch? Some clients want to own it fully and handle it themselves. Others prefer me to stay involved so it keeps improving. I have a few monthly plan options; I'll put them in the kickoff notes. If you decide later you want ongoing support, it's easy to add.

### After delivery (if not yet on retainer)

> The system is live and working well. Now that you've seen how it runs, I wanted to flag the maintenance plan again. The first 30 days post-launch are when most tweaks come up — your team starts using it, edge cases appear, you want to adjust the tone. The maintenance plan covers all of that for a flat monthly fee. If you want to add it for at least 3 months while things settle, I'd recommend it. Happy to chat if useful.

---

## Scope Creep Defence

Retainers without clear scope become unlimited free work. These rules prevent that.

### The 8-hour rule (Growth tier)
Every development request gets a quick estimate: "That'll take about X hours." If it fits in the 8-hour monthly budget, it's included. If it doesn't, you say:

> "This one's bigger than the monthly scope — it'll take about [X] hours. I can either carry it over to next month's budget, or quote it as a separate project. Which works better for you?"

### The log
Keep a shared log (Google Doc or Notion page) of all work done each month, with time estimates. This creates transparency and makes the value visible. Clients who can see "10 hours of work this month" rarely question the invoice.

### The reset
At the start of each month, the clock resets. Hours don't roll over (except in Partner tier, where 5 hours can roll over once). This prevents clients from banking credits.

---

## Retainer Contract Clause

Include this in the one-pager agreement (from `client-onboarding-template.md`):

> **Monthly Retainer:** If a monthly support plan is selected, the retainer fee is due on the 1st of each month. Work begins once payment is received. The retainer covers the services specified in the plan tier selected. Work beyond the included scope will be quoted and agreed in writing before execution. Either party may cancel with 30 days written notice. On cancellation, work ceases at the end of the paid period. All systems built under the retainer remain the client's property.

---

## Upsell Sequence

### Month 1–2: Maintenance → Growth
After a Maintenance client has been running for 60 days:
> "The system's been running well — no issues this month. I noticed [specific opportunity: e.g., 'you're getting a lot of questions about X that aren't in the chatbot yet']. That's a 2-hour change. Want me to roll that into next month, or would you like to move to the Growth plan so we can keep adding things like this regularly?"

### Month 3–6: Growth → Partner
After a Growth client has used their full 8-hour budget two months running:
> "You've been using the full monthly budget consistently — that's a good sign. The Partner plan gives you 20 hours/month and a proper roadmap session so we're being strategic rather than reactive. Want to look at what that would cover?"

---

## Revenue Projections

| Scenario | Clients | Plan Mix | Monthly MRR |
|---|---|---|---|
| **Conservative** (Month 3) | 3 | 2× Maintenance, 1× Growth | €650 |
| **Realistic** (Month 6) | 6 | 3× Maintenance, 2× Growth, 1× Partner | €2,300 |
| **Target** (Month 12) | 10 | 4× Maintenance, 4× Growth, 2× Partner | €5,200 |

> Notes: These are retainer-only projections. Project revenue on top. Month 12 target of €5,200 MRR ≈ €62,400/year from recurring alone, before any new project income.

---

## Next Steps for Creator

1. **Add retainer options to the service proposals** — update Tier 1 and Tier 2 pricing tables in `Projects/service-packages.md` to cross-reference this doc
2. **Add retainer clause to the one-pager agreement** — copy-paste the contract clause above into `Projects/client-onboarding-template.md`
3. **Prepare a retainer option in every project proposal** — never deliver a project without at least mentioning the maintenance plan
4. **Track MRR separately** — in the tracking spreadsheet from `launch-checklist.md`, add a MRR column alongside project revenue
