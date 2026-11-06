# Rankscale onboarding: deck copy draft (v3, lean, for review)

**Session:** 60 min · opening 3 min → live walkthrough 20 min → deck 25 min → Q&A 12 min
**Rule for every slide:** one message, at most 5 points and ~40 words on screen. The detail goes in the speaker notes.
**Slides:** 12 + 1 appendix

---

## 1 · Title
**Rankscale onboarding**
From tracking to action
*[Client name] marketing team · VertoDigital · [date]*

---

## 2 · Today's session
- **Live walkthrough** · 20 min
- **Setting up and reading the data** · 8 min
- **Features that explain the why** · 8 min
- **Turning data into action** · 9 min
- **Q&A** · 12 min

---

## 3 · Live walkthrough: our route
1. Brand setup
2. Search Terms
3. Brand Visibility Dashboard
4. One prompt up close
5. Quick Insights

> Notes: Keep on screen during the demo. Brand setup: competitors, region, tags. Search Terms: Bulk Add, Find Terms, manual runs, View Detailed Insights. Dashboard: Visibility, Mentions, Citations, Sentiment, Position tabs and filters. Prompt up close: each engine's answer and the cited sources. Quick Insights: weekly anomalies.

---

## 4 · Build prompt groups, not keyword lists
**12 prompts per segment = 3 intents × 2 scopes × branded and non-branded**

- 2–5 words, no filler words
- Tag every prompt: branded, intent, scope
- Find prompts with Prompt Research and Find Terms

> Notes: Example: "mobile phone plans" (information) / "best mobile phone plans" (consideration) / "mobile phone plans price" (transaction), each with and without the brand, then repeat for a niche such as "prepaid". Every extra word adds run-to-run volatility. Prompt Research costs 50 credits per segment. Without tags you can't filter or act on the data later.

---

## 5 · The 7 metrics to know
**Visibility Score** · **Detection Rate** · **Position** · **Mentions** · **Citations** · **Sentiment** · **Share of Voice / Share of Citations**

**The one to watch:** being mentioned but not cited is the **Trust Gap**.

> Notes: The headline score hides the cause. A score of 40 can be a detection, position or trust problem. Read branded and non-branded separately. Position: #1–3 strong, #4–6 mid, #7+ weak. Benchmarks are in the appendix.

---

## 6 · Find the why
- **Citation Analysis:** which sources AI trusts in your category
- **Query Fanout:** the hidden searches behind each answer
- **Competitor Analysis:** who's named where you're not
- **Sentiment and Sentiment Radar:** how AI describes you, and why

> Notes: A domain newly cited this week is a PR target. Prioritise sources by citation share, not volume. Fan-out is under Search Terms → View Detailed Insights. Use competitors' recurring negatives in Sentiment to shape your own positioning.

---

## 7 · Fix and act
- **Page Audit V2:** is the page crawlable, parseable and citable?
- **Rankscale Scout:** recommendations per prompt and per engine
- **AI Visits** `NEW`: which AI bots read your site
- **ChatGPT Follow-up Forms** `NEW`: the questions ChatGPT asks buyers

> Notes: Page Audit V2 shows the failing line (crawler access, rendering, schema, headings, paragraph structure). Scout plus Sentiment Radar make a ready-made action list. AI Visits uses a read-only Cloudflare connection and also flags 404s.

---

## 8 · From metric to action
| You see | Gap |
|---|---|
| Low branded detection | PR: entity signals |
| Mentioned, not cited | Content: not citable |
| Position #7+ | Content: competitor preferred |
| Negative sentiment | PR: reputation |

**Fix order: SEO → Content → PR.** Re-check after 4 weeks.

> Notes: Other patterns: no mentions or citations at all usually means blocked crawlers or missing content. Volatile position means thin third-party coverage. When one competitor always wins, reverse-engineer their top cited page.

---

## 9 · Four dashboards to build
1. **Funnel Health:** where does the funnel leak?
2. **Engine Gap:** which engine are we weakest on?
3. **Niche Dominance:** are we top 3 in our segments?
4. **Scenario Proof:** before/after evidence

> Notes: Built in Custom Dashboards. Share as read-only links, export to PDF, or connect Looker Studio. Report monthly to the C-suite, bi-weekly to the marketing lead, weekly to practitioners.

---

## 10 · Your weekly 5-minute read
1. Did any prompt drop?
2. Is branded detection below 90%?
3. Who moved in Share of Voice?
4. Is there a newly cited domain?
5. Is a negative phrase recurring?

> Notes: Use Quick Insights every Monday. Ignore single-digit swings, since detection settles in 2–4 weeks. Run prompts daily for the first 14 days, then weekly.

---

## 11 · Your first week
- Build one tagged prompt group
- Run Page Audit V2 on your key page
- Set up the Funnel Health dashboard
- Book a 90-minute audit after 7 days of data

---

## 12 · Questions?
Rankscale Search Academy · help.rankscale.ai · your VertoDigital team

---

## Appendix · Benchmarks *(reference, not presented)*
| | Floor | Standard | Elite |
|---|---|---|---|
| Global category | 1.0% | 2.8% | 6.0%+ |
| Niche in segment | 5.0% | 24.5% | 40%+ |
| Niche-in-niche | 12% | 38% | 55%+ |

Branded detection ≥95% · Sentiment >65% positive · Position #1–3
*Academy guidance, not platform settings.*
