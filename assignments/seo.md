# Assignment — SEO Specialist

Hi 👋 This assignment is designed to see how you think about SEO end-to-end: technical health, content/keyword strategy, and a prioritized plan that actually moves traffic — not a generic checklist.

CallMissed is a developer-and-business AI platform (LLM API, image generation, speech, voice agents, WhatsApp automation). Our public surfaces include a marketing site (`www.callmissed.com`), developer docs (`docs.callmissed.com`), a blog (`blogs.callmissed.com`), and a model catalog.

**Time:** ~6–10 focused hours. AI tools are fully allowed (and expected).

---

## What to do

Produce an **SEO audit + 90-day growth plan** for CallMissed. Treat `www.callmissed.com` and `docs.callmissed.com` as your primary targets (use the live sites). Deliver it as Markdown in your public repo (a short slide deck or sheet may supplement, but the repo is the source of truth).

### Part 1 — Technical SEO audit
Audit the live site(s) and report concrete findings (with URLs/screenshots where useful):
- Indexability & crawl: `robots.txt`, XML sitemaps, canonical tags, noindex, redirect chains, status codes.
- Core Web Vitals / page speed (use PageSpeed Insights / Lighthouse) — LCP, CLS, INP — with the specific offenders.
- On-page: titles, meta descriptions, heading structure, image alt text, internal linking.
- Structured data / schema (Organization, Product, FAQ, Article, Breadcrumbs) — what exists, what's missing.
- Mobile-friendliness, HTTPS, hreflang/i18n if relevant.
- For the **docs** specifically: are they crawlable and AI-crawler-friendly? Any thin/duplicate pages?

For each issue: **what it is, why it matters, severity (high/med/low), and the fix.**

### Part 2 — Keyword & content strategy
- Identify **15–25 target keywords** for our core themes (e.g. "LLM API", "OpenAI alternative", "Indic/Indian-language AI", "text to speech API", "WhatsApp AI chatbot", "image generation API"). Group by intent (informational / commercial / transactional) and note rough difficulty & why each fits CallMissed.
- Map keywords → existing pages, and flag **content gaps** (pages/posts we should create). Propose **5 blog/landing topics** with a one-line angle + primary keyword for each.
- Pick **one** existing page and rewrite its `<title>` + meta description + H1 as a concrete before/after example.

### Part 3 — Competitor snapshot
- Pick **2–3 competitors** (e.g. OpenAI, OpenRouter, Sarvam, Twilio, or whoever you think is relevant) and give a short comparison: what they rank for that we don't, and one tactic worth borrowing.

### Part 4 — 90-day prioritized plan
- A prioritized roadmap (table is fine): **task → expected impact → effort → priority → how you'd measure success** (the KPI and the tool).
- Be honest about what's quick-win vs. long-game.

---

## What we're evaluating
- **Prioritization & judgment** — do you fix what matters, or list 100 trivial things?
- **Specificity** — real URLs, real numbers, real before/afters > generic advice.
- **Measurability** — every recommendation tied to a metric and a way to track it.
- **Communication** — clear, skimmable, decision-ready writing.
- **Tooling** — sensible use of GSC-style thinking, Lighthouse/PSI, Ahrefs/Semrush/Ubersuggest (free tiers fine), screaming-frog-style crawl, etc. Tell us what you used.

> We don't have a "right answer" key. We're hiring for how you reason about growth.

---

## Submission
See the [root README rules](../README.md). In short:
1. Build in a **public** GitHub repo under your account.
2. Put the audit + plan as Markdown (e.g. `SEO_AUDIT.md`) and update the repo **`README.md`** to summarize your work, tools used, and where you used AI.
3. Commit your **`resume.pdf`**.
4. **Email the repo link to [karan@callmissed.com](mailto:karan@callmissed.com)** — subject `Assignment — SEO — <Your Name>`.

Good luck! 🚀
