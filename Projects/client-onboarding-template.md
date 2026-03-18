---
created: 2026-03-18
updated: 2026-03-18
tags: [revenue, clients, onboarding, templates, process]
---

# Client Onboarding Template

> The gap between "prospect says yes" and "project starts."
> Use this to look professional, set clear expectations, and avoid scope creep.

---

## Stage 1: Discovery Call (20 min)

### Before the Call
- Review their website and any info they gave in outreach
- Open a blank doc to capture answers
- Have your calendar open (Calendly or Cal.com)

### Call Script

**Opening (1 min)**
> "Thanks for making time — I'll keep this to 20 minutes. My goal is to understand your situation well enough to tell you honestly whether I can help, and what that looks like. Sound good?"

**Understanding the Problem (8 min)**

1. "Walk me through the biggest time sink in your business right now. What are you doing manually that you hate doing?"
2. "How much time per week do you think that takes?"
3. "What happens when it doesn't get done — do customers feel it?"
4. "Have you tried to fix this before? What happened?"
5. "What would success look like — what would change in your day?"

**Qualifying (5 min)**

6. "What's your timeline? Is this urgent or exploratory?"
7. "Do you have a budget in mind, or would you like me to come back with options?"
8. "Who else is involved in this decision — or is it just you?"
9. "What does your tech stack look like? What apps do you use day-to-day?" *(for automation)*

**Closing (6 min)**

> "Based on what you've shared, I think [specific solution] could work really well here. I've built something similar — let me send you the demo link after this call."

> "I'll follow up with a short scope summary and two or three pricing options. If it looks right, we can move fast — I can usually start within a week."

> "Any questions for me before we wrap?"

**After the Call (same day)**
- Send follow-up email within 2 hours (see template below)
- Log notes in your CRM or Notion

---

## Stage 2: Follow-Up Email (Send Within 2 Hours)

```
Subject: Quick follow-up + next steps

Hi [Name],

Thanks for the call — it was helpful to understand how [specific problem] is costing you time.

Based on what you told me, here's what I'd recommend:

**[Service Name]** — [one-sentence description of what you'd build for them specifically]

Three options:
• Starter — €[price]: [scope in 1 line]
• Pro — €[price]: [scope in 1 line]
• Full Build — €[price]: [scope in 1 line]

Here's a demo of something I built recently that's similar: [link]

If the Pro option looks right, I can send a one-page agreement today and we can start next week.

Just reply with any questions or "let's go" and I'll handle the rest.

[Name]
```

---

## Stage 3: Intake Questionnaire

Send this after the client says yes, before the kickoff call.

**For all projects:**
- Full business name and legal entity (for the invoice)
- Billing email
- Preferred payment method (bank transfer / Stripe / PayPal / Wise)
- Best contact: email, WhatsApp, or Slack?
- What timezone are you in?
- Who's my main point of contact on your side?

**For chatbot projects (Package 1):**
- What's your website URL? (or: do you have a website?)
- What are your top 5 FAQs customers ask?
- What services do you offer? List them with prices if possible.
- What's your booking process? (Calendly link, phone call, walk-in, etc.)
- Do you want the chatbot to sound formal, friendly, or casual?
- Any topics the bot should never discuss?
- What email should lead notifications go to?

**For automation projects (Package 2):**
- Walk me through the exact process you want automated. Step by step, how does it work today?
- What apps are involved? (Gmail, Notion, Airtable, HubSpot, etc.)
- Do you have accounts/API access for all of them?
- What should happen if a step fails? (ignore, notify me, retry?)
- How often does this process run? (each form submission, daily, weekly?)

**For AI agent / custom dev projects (Package 3):**
- Do you have an existing codebase? If so, what's the stack?
- What's the primary input? (documents, database, user chat, API feed?)
- What's the expected output? (structured data, text response, action trigger?)
- Which LLM provider do you prefer — Claude, GPT-4o, or open-source?
- Do you have any data privacy requirements? (GDPR, no cloud processing, etc.)
- What does deployment look like on your side? (your infra, or should I recommend something?)
- Do you need tests? What coverage level?
- Is there an NDA requirement?

---

## Stage 4: Project Agreement (One-Pager)

Use this simple agreement for all projects. Send as PDF.

---

**PROJECT AGREEMENT**

**Date:** [DATE]
**Client:** [CLIENT FULL NAME / COMPANY]
**Provider:** [YOUR FULL NAME]

---

**Project:** [One-line description]

**Scope of Work**
[3–5 bullet points describing exactly what will be delivered]

**What's NOT included** *(scope protection)*
[List 2–3 common add-ons that are out of scope unless renegotiated]

**Timeline**
- Start date: [DATE]
- Estimated delivery: [DATE]
- Milestones (if applicable): [LIST]

**Payment**
- Total: €[AMOUNT]
- Deposit: €[50% or 100% upfront for projects under €500]: due before work begins
- Balance: €[AMOUNT]: due on delivery / [DATE]
- Payment method: [METHOD]
- Late payment: work pauses after 5 business days

**Revisions**
- Included: [N] rounds of revisions during the [7/14]-day review period
- Additional revisions: €75/hour

**Intellectual Property**
- Client owns all deliverables upon full payment
- Provider may reference this project in a portfolio (anonymized if requested)

**Confidentiality**
- Both parties keep project details private unless written permission given

**Termination**
- Either party may cancel with 5 days notice in writing
- Work completed to date is billable; deposit is non-refundable

**Signatures**
Client: ______________________ Date: ______
Provider: ____________________ Date: ______

---

*This agreement is intentionally simple. For enterprise projects >€3,000, a full contract is available.*

---

## Stage 5: Kickoff Meeting (30 min)

Run this after intake questionnaire received + deposit paid.

### Agenda

**Minutes 0–5: Align on the goal**
> "Let me read back my understanding of what we're building. Tell me if anything's off."
[Describe the project in your own words]

**Minutes 5–15: Review intake answers, fill gaps**
- Go through any unclear answers in the questionnaire
- Confirm access to any tools/APIs needed
- Clarify one or two edge cases: "What should happen if X?"

**Minutes 15–20: Agree on timeline and check-ins**
- Confirm start date and delivery date
- Set one midpoint check-in (async Loom video or 15-min call)
- Agree on communication channel (email / WhatsApp / Slack)

**Minutes 20–25: Agree on handoff format**
- How will they receive the deliverable? (GitHub repo, Notion doc, live demo, ZIP, deployed URL)
- Who on their side will test it?
- What does "done" look like for them?

**Minutes 25–30: Questions, then you're off**
> "I have everything I need. I'll send a kickoff summary within an hour. First check-in [DATE]. Any last questions?"

**After the Call (within 1 hour)**
Send kickoff summary email:
```
Subject: Kickoff summary — [Project Name]

Hi [Name],

Here's what we agreed:

Project: [Name]
Scope: [Bullet list]
Start: [DATE]
Delivery target: [DATE]
Mid-point check-in: [DATE]
Contact: [METHOD]
Handoff: [FORMAT]

I'll be in touch by [DATE] with a progress update.

[Name]
```

---

## Stage 6: Delivery and Invoice

### Delivery Checklist

Before sending anything:
- [ ] Does it do what the scope of work says?
- [ ] Have you run through the client's exact use case end-to-end?
- [ ] Is there a README or handoff doc? (even 10 lines is enough)
- [ ] Are credentials/API keys stored safely, not in code?
- [ ] Is there a "how to maintain this" note?

### Delivery Message
```
Subject: [Project Name] — Delivered

Hi [Name],

Your [chatbot/workflow/agent] is ready. Here's everything:

**[Link to demo / GitHub repo / live URL]**

What's included:
• [Bullet 1]
• [Bullet 2]
• [Bullet 3]

Handoff doc: [link or attached]

You have [7/14] days to test and request tweaks. Reply here with anything you want adjusted.

Once you're happy, I'll send the final invoice.

[Name]
```

### Invoice Template

Send as PDF via Wave (free), Invoice Ninja (free), or Stripe.

```
INVOICE

Provider: [YOUR NAME]
Date: [DATE]
Invoice #: [001]

Bill to:
[Client Name]
[Client Email]
[Client Company]

Services:
[Project Name] — [Description]    €[AMOUNT]

Deposit paid: -€[AMOUNT]

Balance due: €[AMOUNT]

Due: [DATE + 5 business days]
Payment: [Bank transfer / Stripe / PayPal / Wise]

Bank details (if wire):
IBAN: [YOUR IBAN]
BIC: [YOUR BIC]
Account name: [YOUR NAME]

Thank you for the work — I'd appreciate a review on [Contra/Upwork] once the balance clears.
```

---

## Stage 7: Post-Project (Within 48 Hours of Balance Receipt)

### Review Request
```
Hi [Name],

Payment received — thank you.

One quick ask: if the project went well, a short review on [Contra / Upwork] would mean a lot.
It takes 2 minutes and directly helps me take on better clients.

[Direct review link if available]

I'll stay available for any questions over the next week. After that, if you need changes or a new project, just reach out.

[Name]
```

### Referral Ask (Optional, if project went very well)
```
P.S. — If you know any [gym owners / tradespeople / clinic managers] who could use something similar, I'd be happy to offer them 10% off their first project as a thank-you for the introduction.
```

---

## Quick Reference: Project Stages

| Stage | Trigger | Your Action |
|-------|---------|-------------|
| Discovery | Prospect books call | Run 20-min call, send follow-up |
| Proposal | Call complete | Send follow-up email w/ options (same day) |
| Agreement | Client says yes | Send intake questionnaire + one-pager |
| Kickoff | Deposit received | Schedule + run 30-min kickoff |
| Build | Kickoff done | Execute, send midpoint update |
| Delivery | Build done | Send delivery message + review deliverable |
| Invoice | Client approves | Send final invoice |
| Close | Balance received | Send review request, close file |

---

## Scope Creep Defence

If a client asks for something outside the original scope:

> "That's a great idea — it's outside what we agreed for this project, but I can add it.
> It would be approximately [X hours × €75/hr = €amount].
> Want me to include it in the current invoice or save it for a follow-on project?"

Always get scope additions confirmed in writing (even just an email reply).

---

## Files to Have Ready

- [ ] PDF invoice template (fill-in-blank, Wave or Invoice Ninja)
- [ ] One-pager agreement template (this file, converted to PDF)
- [ ] Intake questionnaire (copy from above, Google Form or Typeform)
- [ ] Calendly / Cal.com link for discovery calls
- [ ] Loom account for async video updates

---

*This template covers the full revenue cycle from first contact to final payment.
Adjust tone and prices per service tier. ADHD note: when in doubt, copy-paste from here.*
