# Rankscale onboarding: deck copy draft (v2, for review)

**Session:** 60 min · opening 3 min → live walkthrough 20 min → deck 25 min → Q&A 12 min
**Audience:** client marketing team; fluent in GEO, new to Rankscale
**Slides:** 16 · **Sources:** Rankscale Search Academy (Modules 2–8), rankscale.ai/features, help centre, changelog

---

## 1 · Title
**Rankscale onboarding**
From tracking to action in your AI visibility platform
*[Client name] marketing team · VertoDigital · [date]*

---

## 2 · Today's session
| Time | Block |
|---|---|
| 0–3 min | Kick-off |
| 3–23 min | **Live walkthrough** in your account |
| 23–35 min | Setup, metrics and benchmarks |
| 35–48 min | Features, actions and reporting |
| 48–60 min | Q&A and discussion |

> Notes: Hold questions until the end, or drop them in chat.

---

## 3 · Live walkthrough: our route *(on screen during the demo)*
1. **Brand setup**: domain, competitors, region and language, tags
2. **Search Terms**: Bulk Add, Find Terms, manual runs, View Detailed Insights
3. **Brand Visibility Dashboard**: Visibility, Mentions, Citations, Sentiment, Position; filters by engine, topic and tag
4. **One prompt up close**: each engine's answer, where you appear, who's cited
5. **Quick Insights**: this week's anomalies at a glance

> Notes: ~20 min live in the client account. Come back to this slide between steps.

---

## 4 · Setting up prompt groups: the 3x2x2
**12 short, tagged prompts per segment:** 3 intents × 2 scopes × branded and non-branded

| Intent | Non-branded | Branded |
|---|---|---|
| Information | mobile phone plans | mobile phone plans [Brand] |
| Consideration | best mobile phone plans | best mobile phone plans [Brand] |
| Transaction | mobile phone plans price | mobile phone plans price [Brand] |
*…repeat for the niche scope (e.g. "prepaid mobile phone plans")*

**Three required tags:** Branded / Non-branded · Intent · Scope. No tags means you can't filter or act on the data later.
**Rules:** 2–5 words, no filler words ("what", "how", "a"). Every extra word adds run-to-run volatility.
**Where to find prompts:** Prompt Research (50 credits per segment) · Find Terms after a Page Audit · query fan-out in Detailed Insights

> Notes: Tip: run ~10 branded consideration prompts first and read the Sentiment view. The benefits AI already ties to your category are niche prompts you can win.

---

## 5 · The 7 core metrics
| Metric | What it tells you |
|---|---|
| **Visibility Score** | Headline 0–100 per prompt or group; read branded and non-branded separately |
| **Detection Rate** | % of runs where you appear at all |
| **Position** | Where you're named in the answer: #1–3, #4–6, #7+ or Not Found |
| **Mentions vs Citations** | Awareness vs trust. The gap between them is the **Trust Gap**. |
| **Sentiment** | Positive, neutral, mixed or negative |
| **Share of Voice** | Your mention share against competitors |
| **Share of Citations** | Your citation share against competitors |

**How to read it:** the headline score hides the cause. A score of 40 could be a detection, position or trust problem, and each has a different fix.

---

## 6 · What good looks like: benchmarks
| | Floor | Standard | Elite |
|---|---|---|---|
| Global category | 1.0% | 2.8% | 6.0%+ |
| Niche in segment | 5.0% | 24.5% | 40%+ |
| Niche-in-niche | 12% | 38% | 55%+ |

- **Branded detection:** ≥95% good · 90–95% bad · <90% means fix entity signals first
- **Sentiment:** >65% strong · 55–65% healthy · 45–55% warning · <45% crisis
- **Position:** #1–3 strong · #4–6 mid · #7+ weak
- **Always cross-check** against the median of your top 3 competitors. If theirs is higher, that's your Standard.

*Thresholds from the Rankscale Search Academy; they are guidance, not settings in the platform.*

---

## 7 · Beyond the dashboard: feature map
Citation Analysis · Query Fanout · Competitor Analysis · Sentiment Analysis and Sentiment Radar · Page Audit V2 · Prompt Research · Rankscale Scout · AI Visits `NEW` · ChatGPT Follow-up Forms `NEW`

> Notes: The dashboard was covered live. These are the tools that explain *why*.

---

## 8 · Citation Analysis
**Which domains and URLs win citation share, and where you stand.**
- Filter by prompt, engine and niche, and see your Share of Citations against competitors
- A domain newly cited this week is a new PR target
- Prioritise by citation share, not volume: an 18% source is worth 3x a 6% one

**Use it to:** build outreach lists of 3–6 domains where competitors are cited and you aren't, and open the top 3 cited URLs to see why they win.

---

## 9 · Query Fanout and Detailed Insights
**The searches AI engines run before they answer.**
- Search Terms → View Detailed Insights on a prompt → scroll to fan-out
- See the sub-queries, the words engines add (e.g. "best", "2026"), the domains they check, and which ones win

**Use it to:** turn hidden queries into new tracked prompts and content briefs.

---

## 10 · Competitors and Sentiment
**Competitor Analysis:** auto-detected rivals compared side by side on visibility, position, detection, Share of Voice and citations.
**Sentiment and Sentiment Radar:** how LLMs describe you compared with competitors, with the recurring positive and negative phrases behind the score.

**Use it to:**
- Find prompts where competitors are named and you aren't
- Take competitors' top 3 recurring negatives and write your answering positives into your content
- Trace recurring negatives to their source, and respond only to the 3–5 sources actually feeding the score

---

## 11 · Page Audit V2
**One URL, checked in seconds, with the failing line shown.**
- **Access:** AI crawlers allowed, indexed on Google, content in raw HTML
- **Parsing:** JSON-LD schema, heading hierarchy, self-contained paragraphs
- Rule-based scoring, so results are the same every time you run it

**Use it to:** check the page that should answer your most important prompt before you start content or PR work.

---

## 12 · Rankscale Scout and what's new
- **Rankscale Scout:** auto-generated recommendations per prompt and per engine, plus content ideas from Sentiment Radar. Use it as your action list.
- **AI Visits** `NEW`: which AI bots visit your site, which pages they read, and which links send them to a 404 *(read-only Cloudflare connection)*
- **ChatGPT Follow-up Forms** `NEW`: the clarifying questions ChatGPT asks before recommending brands, and which answers it pre-selects

---

## 13 · From metric to action
| If you see… | It usually means… | Gap |
|---|---|---|
| Low branded detection | AI can't verify your entity | PR (entity) |
| No mentions or citations | Blocked crawlers or missing content | SEO / Content |
| Mentioned but not cited | Content isn't citable (Trust Gap) | Content |
| Position #7+ or Not Found | Competitor content preferred | Content |
| Volatile position across runs | Thin third-party coverage | PR (citations) |
| Negative or conflicting sentiment | Reputation or source conflict | PR (sentiment) |
| One competitor always wins | Format gap: reverse-engineer their page | Content / SEO |

**Fix order:** SEO → Content → PR. Ship one fix, then re-check in 4 weeks.

---

## 14 · Reporting: dashboards that get read
**Build these four Custom Dashboards:**
1. **Funnel Health:** non-branded prompts by intent. Where does the funnel leak?
2. **Engine Gap:** engines side by side. Fix the engine your buyers use most.
3. **Niche Dominance:** visibility and Share of Citations per priority segment
4. **Scenario Proof:** locked long-tail prompts for before/after proof

**Share it:** read-only dashboard links, PDF export, Looker Studio integration, API and MCP server
**Match the audience:** C-suite monthly (1 slide) · marketing lead bi-weekly (2–3 metrics) · practitioners weekly (everything)

---

## 15 · The weekly 5-minute read and tips
**Every Monday:**
1. **Visibility:** any prompt flipped red?
2. **Branded detection:** below 90%? Fix it first.
3. **Mentions:** who moved in Share of Voice?
4. **Citations:** any newly cited domain? That's a PR target.
5. **Sentiment:** any negative phrase showing up more than 3 times in 7 days? Trace it.

**Tips**
- Run daily for the first 14 days to build a baseline, then weekly
- Ignore single-digit swings; detection settles in 2–4 weeks
- Tag everything, and judge trends rather than single runs
- Segment AI referrers (chatgpt.com, perplexity.ai…) as their own channel in GA4

---

## 16 · Your first week, then Q&A
- [ ] Build one 3x2x2 prompt group with all three tags
- [ ] Run Page Audit V2 on your most important page
- [ ] Set up the Funnel Health dashboard
- [ ] Book a 90-minute audit once 7 days of data exist

**Keep learning:** Rankscale Search Academy (rankscale.ai/resources) · help.rankscale.ai · your VertoDigital team

**Questions?**

---

### Open points
1. Client name and date for slide 1.
2. Benchmarks (slide 6) are included and labelled as Academy guidance. Cut them if you'd rather not set targets in this session.
