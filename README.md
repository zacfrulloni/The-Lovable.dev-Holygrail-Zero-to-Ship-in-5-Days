# Vibe Coding Zero to Ship in 5 Days — The Holy Grail

*A simple, story-style path from idea to live app (with copy-paste prompts).*

> I quit my 9–5 after building 20+ Lovable MVPs and earning $29k in 5 months. Here’s the 5-day loop I still use.

**Quick links**

- 📘 Free Playbook (Notion): https://cedar-salute-3ea.notion.site/Lovable-Zero-to-Ship-in-5-Days-25a47b7b39aa80baab12d1f4849cf973  
- 🎥 YouTube: https://www.youtube.com/@Zac-Frulloni  
- 💬 X: https://x.com/zacfrulloni  
- 👥 Community (Skool): https://www.skool.com/lovable-vibe-coding  
- 📧 Contact: info@aidevelopers.tech

---

## Why this exists

Most builders spend weeks scaffolding. This playbook compresses it into **5 focused days** with a PRD, prompts, and guardrails so you can ship a paid-ready MVP fast (auth, core features, Stripe, SEO, deploy).

---

## Mini TOC

- [Day 1 – Problems to PRD to Skeleton](#day-1--problems-to-prd-to-skeleton)  
- [Day 2 – Finish core features](#day-2--finish-core-features)  
- [Day 3 – Auth in two prompts](#day-3--auth-in-two-prompts)  
- [Day 4 – Stripe + SEO for LLMs](#day-4--stripe--seo-for-llms)  
- [Day 5 – Clean deploy](#day-5--clean-deploy)  
- [Quick Prompt Toolbox](#quick-prompt-toolbox)  
- [FAQs](#faqs)  
- [Credits & Community](#credits--community)

---

## Day 1 – Problems to PRD to Skeleton

### Find a real problem
- Collect 3–5 pain screenshots (Reddit, Discord, YouTube/TikTok comments).
- Write a 10-word “value moment.”

### Write a PRD Lovable will follow
- Names, exact routes, user stories with single acceptance checks, and states.
- Keep it human and specific.

### Generate the skeleton in Lovable
- Use a skeleton-only prompt (routes, nav, placeholders, empty/loading/error).
- No auth or data yet.

### Verify
- Every PRD route exists.
- Labels match exactly.
- Empty/loading/error visible.

**PRD kickstart prompt**
You will create a PRD I can paste into lovable.dev.
Ask 5–8 clarifying questions in one list, wait for answers.

Then produce:

Project summary (~50w)

Pages (exact routes + 1-line purpose)

Core features (6–8 user stories + 1 acceptance check each)

Data objects (names + 3–5 behaviors; no fields)

UX flow (happy path + one empty + one failure)

2-week plan (we’ll compress to 5 days)

Copy (3 hero, 5 microcopy)

Skeleton Build Prompt

Constraints: non-technical language; consistent route names; no DB fields.

yaml
Copy
Edit

---

## Day 2 – Finish core features

Connect Supabase in Lovable (top-right green icon). Build 1–2 core features guided by the PRD. Keep scope tiny and testable.

**Feature prompt**
Build a [FEATURE_NAME] for my [APP_TYPE]:

[Primary function]

[Key user action]

[Data requirement]

Create [ComponentName] with [specific UI elements].
Focus only on [main functionality] initially.
Do not change layout, auth, pricing, or route names.

yaml
Copy
Edit

**Verify**
- Action works end-to-end.  
- Refresh persists.  
- No unrelated changes.

---

## Day 3 – Auth in two prompts

**Prompt A – Login, Register, Reset**
Add Supabase authentication.

Do:

Login, Register, and Password Reset pages (match current design)

After login or registration, land on the main page from the PRD

A header user menu (email, Account/Settings link, Logout)

Friendly empty, loading, and error states

css
Copy
Edit

**Prompt B – Email verification guard**
Require email verification before accessing the main app.

Do:

After registration, show a “check your inbox” screen with a resend button

If an unverified user hits a protected page, show a blocker + resend

yaml
Copy
Edit

**Verify**
- Register → verify → login → protected pages work.  
- Reset password OK.

---

## Day 4 – Stripe + SEO for LLMs

### Stripe (test mode)
- Set plans, paywall, real-time status.  
- Use test clocks to simulate trials, renewals, cancellations.

**Stripe prompt**
Add Stripe subscriptions and a simple paywall.

Plans:

Basic $29/mo

Pro $290/yr

Requirements:

Update subscriber status in real time

Lock premium pages until subscription is active

markdown
Copy
Edit

### SEO for LLMs
- Sitemap, solid titles/descriptions.  
- Minimal JSON-LD.  
- 40–70 word “Summary” under H1.  
- Visible “Updated YYYY-MM-DD.”  
- Canonical + OG/Twitter tags.  
- Optional /llms.txt index.

**JSON-LD prompt**
Add minimal JSON-LD:

Home: WebSite (name, url)

Pricing: Product + Offer (plan names, prices)

Guides: Article (headline, dateModified)

Render with <script type="application/ld+json"> matching visible content.

yaml
Copy
Edit

---

## Day 5 – Clean deploy

**Option A**: Deploy inside Lovable with a custom domain.  
**Option B**: Push to GitHub → Vercel/Netlify (dev/main branches).

**Final check**
- Routes match PRD.  
- Auth + Stripe pass.  
- SEO basics present.  
- Core flow demos in under 2 minutes.

---

## Quick Prompt Toolbox

**Constrain scope**
Touch only these files: [list]. Do not modify layouts, auth, pricing, or global styles.

markdown
Copy
Edit

**Investigate before coding**
List the 3 most likely causes of <bug> and how to confirm each. Wait for approval before changing code.

vbnet
Copy
Edit

**Try a new angle**
Use a different solution than before. Keep the same scope and constraints.

yaml
Copy
Edit

**UI nit (Visual Edit)**  
“Reduce top padding by half and left align the text.”

---

## FAQs

**Do I need Cursor?**  
Only if your app is complex. For most micro-SaaS, Lovable is enough.

**Will clients care that it’s AI-assisted?**  
Clients care about outcomes. Show a working product and clean code.

**How much time per day?**  
Plan 1–3 focused hours for 5 days. Short, scoped prompts beat marathons.

---

## Credits & Community

Created by **Zac Frulloni**. This playbook (and the Notion version) is free. If you want help getting your first Upwork client, stuck on prompts, or need reviews:

- 👥 Join the Skool community: https://www.skool.com/lovable-vibe-coding  
- 📘 Free Playbook (Notion): https://cedar-salute-3ea.notion.site/Lovable-Zero-to-Ship-in-5-Days-25a47b7b39aa80baab12d1f4849cf973

If this saved you time, **star this repo** and share it with a builder who needs momentum.
