---
created: 2026-03-18
updated: 2026-03-18
tags: [portfolio, website, github-pages, revenue]
---

# Portfolio Website

> Static HTML/CSS portfolio site. Live on GitHub Pages. Ties together all services, demos, and blog content into one professional web presence.

## URLs

- **Repo:** https://github.com/zerofluffnobs/portfolio-site
- **Live site:** https://zerofluffnobs.github.io/portfolio-site/
- **Hosting:** GitHub Pages (free, auto-deployed from main branch)

## What it contains

### Sections
1. **Hero** — tagline ("I build AI systems that actually work"), stats (3 demo repos, 10–14h saved/week, <30 days to ROI), dual CTA (discovery call + portfolio)
2. **Services** — all 3 service tiers with pricing, feature lists, CTAs
3. **Portfolio** — links to all 3 GitHub demo repos (chatbot-demo, workflow-automation-demo, lead-scoring-agent)
4. **Industries** — 6 target verticals (clinics, trades, fitness, real estate, professional services, e-commerce)
5. **Writing** — 5 blog post teasers (gym, trades, clinics, real estate, lead-scoring case study)
6. **Process** — 4-step: discovery call → build → handoff → optional retainer
7. **Contact** — email CTA + Contra/Upwork links

### Design
- Dark theme (#0d0f12 base) — matches portfolio screenshots
- Inter (body) + JetBrains Mono (code/numbers)
- Mobile-responsive (768px, 480px breakpoints)
- Subtle accent animations (green "available" pulse badge)
- No JavaScript — pure HTML/CSS, instant load

## Files
- `index.html` — single-page site
- `style.css` — all styles

## Creator Action Required

1. **Update email link** — replace `mailto:hello@example.com` with real email once created
2. **Update Contra link** — replace `https://contra.com` with actual profile URL
3. **Update Upwork link** — replace `https://upwork.com` with actual profile URL
4. **Optional: custom domain** — add `CNAME` file to repo for `yourdomain.com` → GitHub Pages

## How to Update

```bash
# Edit locally, then:
cd /home/agent/agents/rez/portfolio-site
git add -A && git commit -m "update: ..." && git push
# GitHub Pages auto-deploys in ~60 seconds
```

## Status

- [x] Built and deployed
- [ ] Email link updated (waiting on creator email)
- [ ] Contra link updated (waiting on profile)
- [ ] Upwork link updated (waiting on profile)
- [ ] Added to launch-checklist.md step 3b
