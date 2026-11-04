# Rankscale onboarding: deck copy draft (v1, for review)

**Session:** 60 min · **Format:** opening 3 min → live walkthrough 20 min → deck 25 min → Q&A 12 min
**Audience:** client marketing team; already fluent in GEO, new to Rankscale
**Slides:** 17

---

## 1 · Title
**Rankscale onboarding**
Getting the most out of your AI visibility platform
*[Client name] marketing team · VertoDigital · [date]*

> Notes: Welcome. Today is hands-on: how Rankscale works, how to read it, and how to make it part of your weekly routine.

---

## 2 · Today's session
| Time | Block |
|---|---|
| 0–3 min | Kick-off |
| 3–23 min | **Live walkthrough** in your account |
| 23–26 min | Reading the metrics |
| 26–40 min | Features that go deeper |
| 40–48 min | Use cases and tips |
| 48–60 min | Q&A and discussion |

> Notes: Hold questions about the walkthrough until the end, or drop them in chat. We'll pick them up in Q&A.

---

## 3 · Live walkthrough: our route *(on screen during the demo)*
1. **Brand setup**: domain, competitors, country and language, tags
2. **Search terms and Topics**: adding terms, "Find Terms", choosing engines, how often each runs, region
3. **Brand Visibility Dashboard**: the headline metrics, filtering by engine, topic and tag
4. **One search term up close**: the answer from each engine, and where your brand appears
5. **Competitors, Citations and Sentiment**: who wins and why

> Notes: Live in the client account, ~20 min. Keep this slide up as a map, and come back to it between steps.

---

## 4 · Reading the dashboard: metrics cheat sheet *(~3 min)*
| Metric | What it tells you |
|---|---|
| **Visibility score** | Headline score that combines mentions, position and citations. Track the trend. |
| **Detection rate** | Share of AI answers that mention your brand |
| **Average position** | Where your brand appears in the answer when it is mentioned |
| **Top 3 rate** | How often you're among the first three brands named |
| **Mentions** | Times your brand is named in answers |
| **Citations** | Times your URLs are linked as a source |
| **Sources** | Your URLs supported an answer *without* your brand being named |
| **Sentiment** | Positive, neutral or negative tone of mentions |

**How to read it:** AI answers vary from run to run. Judge trends over weeks, not single runs, and compare the same engines and time frames.

---

## 5 · How tracking works: engines and run types
**Engines tracked:** ChatGPT · Google AI Mode · Google AI Overviews · Gemini · Perplexity · Bing Copilot · Meta Muse Spark

**Two ways a prompt is run:**
| | **GUI run** | **API run** |
|---|---|---|
| How | Automated browser queries the engine's public interface | Direct connection to the model's API |
| What you see | What a real user sees, including web search and citations | The model's raw answer, faster and more consistent |
| Credits | 0.25 per run | From 1 per run (some models cost more) |
| Best for | Day-to-day visibility tracking | Model-level comparisons, extra engines |

**Credit tip:** cost = terms × engines × how often they run. Weekly runs on the core engines cover most needs.

---

## 6 · Beyond the dashboard: feature map
- **Citation Analysis**: which domains win citation share
- **Query Fanout**: the hidden searches AI engines run
- **Competitor Analysis**: side-by-side visibility against rivals
- **Sentiment Analysis**: how LLMs describe you compared with competitors
- **Page Audit**: AI citation readiness, URL by URL
- **Prompt Research**: real prompt patterns and intents
- **AI Visits** `NEW`: which AI bots read your site
- **ChatGPT Follow-up Forms** `NEW`: the clarifying questions ChatGPT asks

> Notes: The dashboard was covered live. These are the tools for the *why*, which we take one by one next.

---

## 7 · Citation Analysis
**See which domains win citation share, and where you stand.**
- Most-cited domains and URLs by engine, topic and search term
- Your share of citations against competitors
- Spot third-party sites (reviews, media, forums) that shape AI answers

**Use it to:** build PR and outreach lists, and find pages worth updating.

---

## 8 · Query Fanout
**See the searches AI engines run before they answer.**
- The sub-queries ChatGPT, AI Overviews and Copilot fire behind one prompt
- Appendix words engines add (e.g. "2026", "best", "reviews")
- The domains they check, and which ones win

**Use it to:** turn hidden queries into content briefs and on-page wording.

---

## 9 · Competitor Analysis and Sentiment
**Competitors:** auto-detected and compared side by side on visibility, average rank, detection rate, top 3 rate, mentions and citations.
**Sentiment:** how LLMs describe your brand, and how that compares with rivals.

**Use it to:** find search terms where competitors appear and you don't, and spot negative narratives early.

---

## 10 · Page Audit
**Score any URL for human trust and AI citation readiness.**
- Classifies the page type (e.g. e-commerce, local, YMYL)
- Rule-based checks: SEO, AI readiness, schema, E-E-A-T, links, content structure
- No LLMs in the scoring, so results are the same every time you run it

**Use it to:** prioritise fixes on the pages you want AI to cite.

---

## 11 · New: AI Visits and ChatGPT Follow-up Forms
**AI Visits:** which AI bots visit your site, which pages they read, and which links send them to a 404. *(Read-only Cloudflare connection.)*
**ChatGPT Follow-up Forms:** the clarifying questions ChatGPT asks before it recommends brands, and which answers it pre-selects.

**Use it to:** fix crawl gaps, and shape content around the criteria ChatGPT asks buyers about.

---

## 12 · Prompt Research and better search terms
**Prompt Research:** surfaces real prompt patterns and intents from large-scale AI query data.
**Find Terms:** AI-suggested terms inside each Topic, ranked by simulated volume.

**Use it to:** track the prompts your buyers actually use, not the keywords you'd guess.

---

## 13 · Reporting and automation
- **Custom dashboard views:** build widget-based views, save several, export to PDF
- **Shareable links:** read-only dashboards for stakeholders without an account
- **API and MCP server:** pull visibility, citations, fan-out and sentiment data into your own tools or AI assistants
- **Beta:** recommendations, GA4 and Search Console connection

---

## 14 · Five ways marketing teams use Rankscale
1. **Benchmark:** visibility and share of voice against competitors, by engine
2. **Find gaps:** terms where competitors are named and you're not
3. **Earn citations:** target the sites AI engines trust most
4. **Optimise content:** Page Audit and Query Fanout insights turned into briefs
5. **Report:** shared views for leadership, monthly trend stories

---

## 15 · A simple weekly routine *(20–30 min)*
1. **Visibility tab:** what moved this week?
2. **Drill in:** open the tab that moved most (Competitors, Citations, Sentiment)
3. **Check the why:** Query Fanout and the cited sources for the terms that dropped
4. **Act:** one content, PR or technical fix per week
5. **Log it:** note what you changed, so next month's trend has a story

---

## 16 · Tips from the field
- **Relevance over volume:** fewer, sharper search terms produce cleaner data
- **Tag everything:** split branded and non-branded terms, and tag by funnel stage
- **Group by Topic:** report on themes, not single prompts
- **Watch your credits:** GUI runs for tracking, API runs only where needed
- **Trends, not snapshots:** wait for several runs before reacting
- **Keep competitors current:** review the auto-detected list each month
- **Share, don't screenshot:** use saved views and live links

---

## 17 · Keep learning, then Q&A
- **Rankscale Learning Hub:** 9 modules, free (rankscale.ai/resources)
- **GEO Glossary:** 90+ terms
- **Help centre:** help.rankscale.ai
- **Your VertoDigital team:** [contact]

**Questions?**

---

### Open points to confirm
1. **"Normal vs GPU" (slide 5).** I read this as **GUI vs API** runs, Rankscale's two run types. Please correct me if you meant something else.
2. **API run credits.** These come from third-party reviews (Claude ~2, DeepSeek ~1), so please check them in your account. Slide 5 currently says only "from 1 per run".
3. **Engines (slide 5).** The list follows your screenshot. Should we also name the API-only models (e.g. Claude, DeepSeek)?
4. **Metric definitions (slide 4).** These come from Rankscale's help centre and review sites. The exact Visibility score formula isn't public.
5. **Client name and date** for slides 1 and 17.
