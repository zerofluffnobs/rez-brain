---
created: 2026-03-18
tags: [sales, social-proof, testimonials, portfolio]
---

# Testimonial & Social Proof Capture System

> Turn every completed project into a credibility asset. One email, one LinkedIn request, one portfolio update.

---

## Why This Matters

Cold outreach converts better when leads can see that real clients vouched for you. A single strong testimonial is worth more than five blog posts. The window to capture it is **within 48 hours of delivery** — that's when the client's excitement is highest.

---

## Step 1: Post-Delivery Testimonial Request Email

Send this **the same day you deliver the final project**.

**Subject:** Quick favour — would you share your thoughts?

---

Hi [Name],

Really glad we got [project outcome] shipped — hope it's already saving you time.

One small ask: would you be willing to write 2–3 sentences about your experience working with me? Honest is fine — I'm building my reputation and real words from real clients matter more than anything I could write myself.

You can paste your reply directly into this email. I'll use it on my portfolio site and Contra/Upwork profile (I'll always ask before using your name and company).

If it's easier, I've put a few prompts below to get you started:

- What problem were you trying to solve before we worked together?
- What did we build, and what's changed since?
- Would you recommend this to someone else, and why?

No pressure to answer all three — even a sentence or two is incredibly helpful.

Thanks again,
[Your name]

---

**Follow-up (if no reply in 5 days):**

**Subject:** Re: Quick favour — would you share your thoughts?

Hi [Name],

Just a gentle nudge on my earlier email — totally fine if now isn't the right time. Even a quick "it was great, would recommend" goes a long way.

Either way, glad the project went well.

[Your name]

---

## Step 2: LinkedIn Recommendation Request

Send this **within 72 hours of delivery** via LinkedIn DM, after the email above.

---

Hi [Name], glad the project landed well!

If you have 5 minutes, a LinkedIn recommendation from you would mean a lot — it helps me get in front of the right clients. You can write whatever feels true; I'm happy to draft something for you to edit if that's easier.

Here's the link to leave one: **[Your LinkedIn profile URL] → More → Recommend**

No obligation at all — just wanted to ask while the project is fresh.

---

**Draft recommendation you can offer clients (edit to match their voice):**

> "I worked with [Your name] to build [brief description]. The process was smooth from start to finish — clear communication, fast turnaround, and the end result actually does what it's supposed to. If you're a [vertical] business looking to automate [pain point], I'd recommend reaching out."

---

## Step 3: Testimonial Storage

Save every received testimonial to `Projects/testimonials.md` (create on first receipt) using this format:

```
## [Client Name or Initials] — [Vertical] — [Date]

> "[Exact quote]"

**Project type:** [chatbot / workflow automation / AI agent]
**Permission to use publicly:** yes / name only / initials only
**Used on:** portfolio site / Contra / Upwork / LinkedIn post
```

---

## Step 4: Portfolio Site Integration

### Where to add testimonials

In `portfolio-site` repo (`index.html`), add a **Testimonials section** between the Blog section and the Contact section:

```html
<!-- TESTIMONIALS SECTION -->
<section id="testimonials" style="padding: 60px 0; background: #0d0d0d;">
  <div style="max-width: 800px; margin: 0 auto; padding: 0 24px;">
    <h2 style="text-align: center; font-size: 2rem; margin-bottom: 48px; color: #ffffff;">What Clients Say</h2>
    <div style="display: grid; gap: 32px;">

      <!-- Repeat this block for each testimonial -->
      <div style="background: #1a1a1a; border: 1px solid #2a2a2a; border-radius: 12px; padding: 32px;">
        <p style="font-size: 1.1rem; line-height: 1.7; color: #cccccc; margin-bottom: 20px;">
          "TESTIMONIAL TEXT HERE"
        </p>
        <div style="display: flex; align-items: center; gap: 12px;">
          <div style="width: 40px; height: 40px; border-radius: 50%; background: linear-gradient(135deg, #00ff88, #0088ff); display: flex; align-items: center; justify-content: center; font-weight: bold; color: #000;">
            <!-- First letter of client name -->
          </div>
          <div>
            <div style="color: #ffffff; font-weight: 600;">CLIENT NAME</div>
            <div style="color: #888888; font-size: 0.9rem;">Role, Company — Vertical</div>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>
```

### Placeholder (before first testimonial arrives)

If you want to publish the site before testimonials arrive, use this placeholder block instead:

```html
<section id="testimonials" style="padding: 60px 0; background: #0d0d0d;">
  <div style="max-width: 800px; margin: 0 auto; padding: 0 24px; text-align: center;">
    <h2 style="font-size: 2rem; margin-bottom: 16px; color: #ffffff;">Early Clients Welcome</h2>
    <p style="color: #888888; font-size: 1.05rem;">First 3 projects at reduced rate in exchange for an honest testimonial. <a href="#contact" style="color: #00ff88;">Get in touch.</a></p>
  </div>
</section>
```

---

## Step 5: Contra & Upwork Reviews

### Contra
After marking a project complete, Contra sends an automatic review request. No action needed — just make sure you mark the contract complete promptly (within 24 hours of final delivery).

### Upwork
After closing a contract, Upwork prompts both parties to leave feedback. Always leave feedback for the client first — it increases the chance they reciprocate. Keep your review professional and specific:

> "Great client — clear brief, fast feedback, paid on time. Would work with [Name] again."

---

## Step 6: Social Proof in Outreach

Once you have 1–2 testimonials, add a **PS line** to cold emails:

> PS — [Client Name from Vertical], a [job title] at [Company], said: "[short quote]." Happy to share the full case study if useful.

And update the portfolio site's hero section to include a trust line:

> Trusted by [Vertical 1], [Vertical 2], and [Vertical 3] businesses across Europe.

---

## Quick Reference

| Trigger | Action | Timing |
|---|---|---|
| Final delivery sent | Send testimonial request email | Same day |
| Email sent | Send LinkedIn recommendation request | Within 72 hours |
| Testimonial received | Save to testimonials.md | Same day |
| Testimonial received | Update portfolio site HTML | Within 48 hours |
| Testimonial received | Update Contra + Upwork profiles | Within 48 hours |
| Testimonial received | Add to outreach email PS line | Next outreach batch |

---

## ADHD Usage Notes

- **Don't wait** to ask for the testimonial. The longer you wait, the colder the client gets. Ask on the day you deliver.
- **Make it easy.** Offer to draft it for them. Most clients will say yes, then lightly edit your words.
- **One action at a time.** Email first. LinkedIn request second. Portfolio update third. Don't try to do all three at once.
- The email template and LinkedIn message are in this file — copy-paste, don't rewrite.
