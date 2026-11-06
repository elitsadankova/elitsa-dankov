---
name: rankscale-prompt-generation
description: Generate Rankscale AI-visibility tracking prompts for a brand using the Rankscale segment-tracking best practice — for every strategic segment, three separate projects (Market, Brand, Comparison), intent-first topics, and project names where only the brand acts as a mention trigger (e.g. "DMEA [Market_Trade_Fair_Discovery]"). Requires the brand domain and the focus topics/segments; asks for competitors and existing brand research; optionally uses sales call transcripts or filled forms to mirror how prospects actually search. Use when someone asks to build Rankscale prompts, a prompt set, AI search / LLM visibility tracking, GEO/AEO tracking prompts, or segment tracking for a client.
---

# Rankscale Prompt Generation (Segment Tracking)

You build a clean, strategically interpretable Rankscale tracking setup for one brand.
For **every strategic segment** you produce **three prompt sets, each its own Rankscale project**:

| Set | Measures | Brand in prompt? | Key metrics |
|---|---|---|---|
| **A) Market** | Open market orientation — does the brand show up in the mental competitive landscape? | **No** (no brand, no competitor names) | Mentions, AI Visibility |
| **B) Brand** | Explicit brand demand — how is the brand *framed* once it is asked for by name? | **Yes**, the brand only | Qualitative response patterns, sentiment |
| **C) Comparison** | Direct competition / substitution — how is the brand argued *against* a named rival? | **Yes**, brand + one named competitor | Argument patterns, sentiment in comparisons |

Visibility near 100% in Brand and Comparison is expected and not a finding — those sets exist to read framing and argumentation, not visibility. Only the Market set measures visibility.

Read `references/best-practice.md` for the full rationale and `references/output-template.md` for the exact deliverable format before producing output.

---

## Step 1 — Collect inputs

Ask for everything in one message (use AskUserQuestion or a single concise list). Do not start generating until the **required** inputs are in.

**Required (block until provided)**
1. **Brand domain** — e.g. `dmea.de`. Used to research the brand and to derive the exact brand name used as the match trigger.
2. **Focus topics / segments** — the strategic segments the prompt groups should cover (e.g. "Digital health trade fairs", "Healthcare IT networking platforms"). Each segment becomes three projects.

**Requested (ask explicitly; if missing, propose and get confirmation)**
3. **Competitors** — the direct competitors per segment. Needed for the Comparison set. If the user has none, propose 3–6 from your research, label them *proposed*, and confirm before writing Comparison prompts.
4. **Brand research done so far** — positioning docs, ICP/persona notes, messaging, previous audits, keyword research, an existing Rankscale setup. Ask for files, links, or a short summary. If none exists, do your own light research (Step 2) and say so.

**Optional (ask once, never block)**
5. **Sales call transcripts or filled forms** (contact/demo/enquiry forms, discovery-call notes). These show how prospects actually phrase their problem, what they compare, which objections they raise, and where they are in the buying process. If not available, continue and note that prompts are research-based, not prospect-language-based.

Also confirm (use sensible defaults if not stated): **market/region and language** of the prompts (default: the brand's primary market, English), and **target volume** (default: 3–5 topics per set, 5–8 prompts per topic).

---

## Step 2 — Understand the brand and the market

Before writing prompts, build a short working brief (keep it in the conversation, show it to the user):

- **Brand name / match trigger**: the exact token(s) LLMs use for the brand. Check the domain, site title, and how third parties write it. Note spelling variants.
- **Trigger-risk check**: if the brand name is itself a common word (e.g. "Notion", "Monday", "Apple"), flag it — mentions may be over-counted regardless of project naming. Recommend the most distinctive form (e.g. "monday.com") as the project-name trigger.
- **Category language**: how the market describes the category, without the brand.
- **Per segment**: core buyer problem, buyer personas, decision criteria, the competitor set.
- **Prospect language** (only if transcripts/forms were provided): recurring phrasings, pains, comparison pairs, objections, trigger events. Quote or paraphrase them; never invent quotes.

Sources, in order: user-provided research → transcripts/forms → the brand's own site (fetch the domain) → web search for category and competitor context. If the Verto Brain connector is available, you may check it for existing client data. Never fabricate facts, metrics, or quotes; mark anything assumed as an assumption.

---

## Step 3 — Define intents as topics (intent-first)

Within each prompt set, structure by **intents (topics)**, not keywords. A topic is a distinct question the buyer is trying to answer.

**Market set** — strategic perception intents only, e.g.:
- Discovery & Selection ("which … should I consider")
- Comparison of options in the category (without naming brands)
- Leadership / ranking logic ("leading", "best", "most important")
- Problem → solution-category fit

**Exclude from the Market set** all operational / funnel intents: tickets, pricing pages, travel, logistics, program/agenda details, login/support, networking how-tos, opening hours, job openings. These pull the segment into service logic and add noise. If the user wants them tracked, put them in a separate, clearly labelled operational project — never in the strategic Market set.

**Brand set** — framing intents, e.g.: what the brand is known for / reputation; strengths & weaknesses; who it is for; is it worth it / credibility; brand within the segment's use case.

**Comparison set** — substitution intents, e.g.: Brand vs Competitor head-to-head; which is better for a specific use case/persona; switching / choosing between the two; differentiators.

Topic names should be short and human-readable (Rankscale's Prompt Research can auto-create topics; your names should be compatible with that).

---

## Step 4 — Write the prompts

Rules for all sets:
- Write as a real person would type into ChatGPT / Perplexity / Gemini: natural, conversational, specific. Mix short and longer prompts; include persona and context where realistic ("As a hospital CIO in Germany, …").
- One intent per prompt. No duplicates or near-duplicates across topics.
- Where transcripts/forms exist, mirror their vocabulary, pains and comparison pairs, and mark those prompts as `prospect-language` in the source column.
- Match the agreed language and region.

Set-specific rules:
- **Market**: must contain **neither the brand nor any competitor name**. Category, problem, and persona only.
- **Brand**: must contain the brand name; must **not** contain competitor names.
- **Comparison**: must contain **exactly two brands — the client brand and one named competitor** (e.g. "DMEA vs HIMSS Europe for …"). Cover every confirmed competitor at least once; prioritise the competitors most frequently named in research/transcripts.

Run a self-check before output: scan every Market prompt for brand/competitor names, every Brand prompt for competitor names, and every Comparison prompt for exactly two brand names. Fix violations.

---

## Step 5 — Name the projects (encapsulated segment logic)

Rankscale uses the **project name for mention detection — every word in the name can act as a match trigger.** A name like "Healthcare Event Overview" would count every answer containing "Healthcare" or "Event" as a mention, distorting the data.

Use this pattern so **only the brand is a match trigger**:

```
<BRAND> [<Set>_<Segment_Label>]
```

e.g. `DMEA [Market_Digital_Health_Trade_Fairs]`, `DMEA [Brand_Digital_Health_Trade_Fairs]`, `DMEA [Comparison_Digital_Health_Trade_Fairs]`

- The brand is the only free-standing word.
- The bracket block is for human readability only: words joined with underscores, no spaces, `&` allowed. Such constructions don't occur naturally in model answers.
- Never put competitor names, the category's generic words outside the brackets, or anything other than the brand outside the brackets.
- Each set is a **separate project** (Market, Brand, Comparison never share a project) to avoid mixing signals across intent layers.

---

## Step 6 — Deliver

Produce the deliverable exactly as in `references/output-template.md`:
1. Input summary (what was provided, what was assumed, what was missing — e.g. "no transcripts provided").
2. Working brief (Step 2).
3. Per segment: the three projects, each with name, purpose, key metrics, topics, and prompts.
4. A flat CSV (`project_name,set,segment,topic,prompt,source`) saved in the working directory (or the scratchpad if not in a project folder) for bulk import, and send it to the user.
5. Notes: trigger-risk warnings, excluded operational intents, and suggested next steps.

Ask the user to review before any push to Rankscale.

---

## Step 7 — (Optional) Push to Rankscale

Only if the user asks and the Rankscale connector is available. Writes are outward-facing — confirm the exact plan first.

1. Projects (Rankscale "brands") must exist with the names from Step 5. Use `rankscale_brands_list` to find them by name. If a project is missing, tell the user to create it in Rankscale with that exact name — don't substitute an existing project.
2. For each project, create topics with `rankscale_topics_create` (name = topic name).
3. Create prompts with `rankscale_search_terms_create` — one call per prompt **per AI engine** (ask which engines; region/language as agreed). Terms are created **inactive** and spend no credits; tell the user they must activate them (or ask you to, with `rankscale_search_terms_activate`) — never activate without explicit approval.
4. Assign prompts to their topics with `rankscale_topics_assign_terms` (max 50 ids per call).
5. Report what was created per project, and anything that failed.
