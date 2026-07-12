# RBF Uniform Marketing Playbook
_Tier 3 knowledge file. One repeatable launch sequence + studio brand architecture for every Resting Bot Face app. Compiled 2026-07-11 from multi-app studio market research._

---

## Part 1 — Studio Brand Architecture

### The principle
Digital-only multi-app studios succeed on brand in one of two ways:
- **Branded house (Not Boring model):** the studio has a strong point of view; every app inherits it; users buy the studio, not the app. Requires one shared audience. Two-person studio, Apple Design Awards, single membership across all apps.
- **House of brands (Bending Spoons model):** apps stand alone; the parent is invisible. Works at scale with paid UA budgets — its known weakness is zero cross-app synergy. Not viable for a solo operator who depends on organic compounding.

### RBF's structure: one house, two rails
RBF apps split into two audience clusters, so a pure Not Boring model doesn't fit. Instead:

- **Studio layer (restingbotface.dev):** one visual identity, one voice, one build-in-public presence, one "About the studio" page every app links to. The studio brand carries the *maker credibility* — solo builder, health/family domain expertise, no-ads promise, craft. This is what makes app #3 launch easier than app #1.
- **Rail A — Family/Consumer:** MamaBot, Cruel Summer, Family Coordination. Shared audience: parents managing household logistics. These apps cross-promote each other directly (in-app "More from RBF" screen, shared email list segment, bundle/membership candidate once 2+ are live).
- **Rail B — B2B/Professional:** Carry, Clinic Scheduling. Shared audience: small practice owners/providers. Cross-promote within the rail only. Acquisition is niche-channel (provider communities, RTM reimbursement angle), not App Store browse.

**Rule: cross-promote within a rail, never across rails.** A parent using Cruel Summer doesn't care about clinic scheduling; showing it dilutes trust. The studio brand is the only thing that spans both.

### Studio brand assets (build once, reuse forever)
- [ ] Studio manifesto — one page, the RBF point of view (modular craft, no ads, small tools done well). Not Boring's manifesto is the reference.
- [ ] Studio design tokens — shared logo lockup treatment, "from Resting Bot Face" badge for app splash/about screens
- [ ] Per-app brand kits derive from studio kit (unique font + palette per app — already planned)
- [ ] One email list, tagged by rail and by app
- [ ] One social presence (build-in-public), posting across all apps
- [ ] restingbotface.dev: studio home + one landing page per app (template, reused)

---

## Part 2 — The RBF Launch Sequence

Repeatable for every app. Phase-gated like everything else: don't advance until the prior phase's exit criteria are met. Timeline anchors to launch day (L).

### Phase 0 — Positioning (before any marketing work)
- Write the one-sentence positioning: **[Who] uses [App] to [outcome] in [context].** This sentence drives the landing page, screenshots, ASO copy, and every post. Vague positioning → vague screenshots → no conversion.
- Identify the rail (A or B) — this sets the channel list for everything below.
- **Exit criteria:** positioning sentence approved; 5–10 target ASO keywords chosen (long-tail, realistic difficulty — "bodyweight workout log," not "fitness").

### Phase 1 — Foundation (L-90 to L-60)
- Landing page live on restingbotface.dev from template: one sentence, one hero visual, email capture, "coming [Month]." Nothing more — multi-screenshot pages underperform.
- Waitlist with referral mechanic ("invite 3, move up the line" / "skip the TestFlight queue"). Target: **500–2,000 engaged signups** — that's the practical floor for launch-day ranking signal; don't chase 50k.
- Analytics wired before any user touches anything: App Store Connect + crash reporting (Sentry/Crashlytics) + event tracking (install → first-open → activation → D7). Attribution set up pre-launch or the first month is guesswork.
- ASO draft: title, subtitle, keyword field (comma-separated, no spaces, don't repeat title words), screenshots with benefit captions, icon.
- **Exit criteria:** landing page converting; analytics verified end-to-end; ASO assets drafted.

### Phase 2 — Beta & signal (L-60 to L-21)
- TestFlight beta: 50–200 real users recruited **from the waitlist in queue order** (rewards referrers, fills beta with highest-intent users). Not friends and family.
- Structured feedback form: first impression, friction points, favorite feature, bugs. Fix core-flow bugs first.
- Watch the three metrics that predict launch week: onboarding completion rate, D1 retention proxy, crash-free %.
- Harvest 3–5 beta testimonials → landing page + screenshot captions (social proof).
- Content drip starts: 1–2 build-in-public posts/week showing the product in action (short video > text). Rail-appropriate communities only (A: parenting subreddits/groups; B: practice-owner communities) — honest, non-spammy.
- **Submit Apple editorial featuring nomination by L-30** (needs 4–6 weeks lead; miss this and launch-week featuring is gone).
- **Exit criteria:** D1/crash metrics acceptable; testimonials collected; featuring nomination in.

### Phase 3 — Lock & load (L-21 to L-1)
- ASO finalized and frozen by L-14. Not launch-day work — fixing it post-launch corrupts ranking signals during the only week that matters.
- Submit for App Store review by L-10 (review is 1–3 days but rejections reset the clock; buffer is non-negotiable).
- Write the launch-day email to the waitlist. Line up any creator/influencer posts to land within the first 48 hours, not spread across a week.
- Prep launch posts for: Product Hunt (rail A apps), relevant subreddits, build-in-public feed, personal networks.
- **Exit criteria:** app approved and pending developer release; launch email drafted; all posts scheduled.

### Phase 4 — Launch (L-day to L+3)
- **Launch Tuesday or Wednesday.** Never Monday or Friday.
- Everything fires in one coordinated 72-hour window — install velocity in the first 72 hours is the heaviest-weighted store ranking signal. A slow rollout wastes the waitlist.
  - Morning: release live → waitlist email → all scheduled posts
  - Day 1–2: creator posts land; respond to every comment/review
  - Landing page: swap waitlist CTA for App Store badge (update in place, keep SEO)
- Watch ratings from hour one; respond publicly to negative reviews immediately.

### Phase 5 — Compound (L+3 to L+90)
- In-app review prompt triggered **after a success event** (completed task, milestone) via SKStoreReviewController — never on first open.
- Ship small updates every 2–3 weeks — active development is a ranking signal and retains early users.
- A/B test the first screenshot (largest conversion impact), then title/subtitle.
- Add the app to the rail's cross-promotion surface: "More from RBF" in sibling apps, email list announcement to the rail segment.
- **L+30 and L+90 review gates** (matches existing business plan): D7 retention below ~20% = product issue, fix before spending anything on acquisition. Decide continue / iterate / sunset.

---

## Part 3 — What compounds across launches

Each launch feeds the next — this is the marketing equivalent of the modular code units:

| Reusable unit | Built during | Reused for |
|---|---|---|
| Landing page template | App #1, Phase 1 | Every app |
| Waitlist + referral setup | App #1, Phase 1 | Every app |
| ASO checklist + screenshot template | App #1, Phase 3 | Every app |
| Launch email + post templates | App #1, Phase 4 | Every app |
| Studio email list | Continuous | Warm audience per rail, day one |
| Build-in-public audience | Continuous | Pre-warmed launch cohort |
| Review-prompt module (code) | App #1, Phase 5 | Every app — this is literally a modular skill |
| Cross-promo "More from RBF" screen (code) | App #2 in a rail | Every rail sibling |

**Standing rule:** after each launch, do a 30-minute retro and update this file. The sequence should get tighter every time, same as the codebase.

---

## Sources (key)
- RevenueCat — App portfolios vs. single-app focus (shared playbooks/infrastructure economics)
- IndieRadar — Multi-product portfolio playbook (same-audience cross-sell economics)
- Not Boring Software / Andy Allen profiles (branded-house model, membership across apps)
- Bending Spoons analyses (house-of-brands synergy failure mode)
- vmobify 30-day pre-launch playbook; SEM Nexus 90-day timeline & waitlist playbook; LaunchList checklist; AppScreenshotStudio 2026 launch checklist (sequence mechanics, thresholds, timing rules)
