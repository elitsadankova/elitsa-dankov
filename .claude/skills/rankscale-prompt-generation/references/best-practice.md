# Rankscale Best Practice for Segment Tracking

## Three prompt sets per segment

For every strategic segment, three separate prompt sets are created.

### A) Market
Measures open market orientation without explicit brand binding.
Shows whether the brand appears in the mental competitive landscape and how visible it is in the open field.
**Key metrics:** Mentions and AI Visibility.

### B) Brand
Measures explicit brand demand.
The prompts already contain the brand name, so Mentions and AI Visibility naturally approach 100%.
The goal is not visibility measurement but understanding how the brand is framed once it is explicitly requested.
**Key metrics:** qualitative response patterns and sentiment.

### C) Comparison
Measures direct competitive and substitution logic.
Prompts typically contain two predefined brands (Brand A vs Brand B), so visibility is structurally given.
The focus is on how the brand is evaluated and positioned within direct competitive comparisons.
**Key metrics:** qualitative argument patterns and sentiment within direct comparisons.

This three-part structure cleanly separates **perception, demand, and competition**.

## Structure intents as topics

The approach is intent-first. Within a prompt set you do not structure individual keywords but intents as topics.
Intents are generated through Prompt Research in Rankscale and can be created as topics with one click.

Example (Market set, trade fair segment):
- Trade Fair Discovery & Selection
- Comparison of Trade Fairs
- Leadership or Ranking Logic

Operational intents — tickets, travel, program details, networking — are **not** included in the strategic Market set. This keeps the segment on the level of strategic perception and stops it drifting into service or funnel logic.

## Each prompt set is a separate project

- Market = separate project
- Brand = separate project
- Comparison = separate project

This avoids data noise, mixed signals and statistical distortion across intent layers. Each project measures exactly one strategic mode.

## The naming problem

Rankscale uses the project name for mention detection. All words in the project name can be treated as match triggers.
A project named "Healthcare Event Overview" would also match "Healthcare" or "Event" when the brand isn't mentioned — distorting the data.

## The solution: encapsulated segment logic

```
DMEA [Trade_Fair_Discovery_&_Selection]
```

- "DMEA" is the only true match trigger (DMEA is Europe's leading trade fair for digital health).
- The bracket block serves human readability only.
- Such constructions do not naturally appear in model answers.
- Data collection stays clean and brand-focused.

Semantic clarity for analysts, without artificial mention triggers.

Because each segment has three projects, this skill prefixes the bracket label with the set so the names stay unique:
`DMEA [Market_…]`, `DMEA [Brand_…]`, `DMEA [Comparison_…]`.

## Summary (per segment)

- 3 prompt sets: Market, Brand, Comparison
- Intent-first structure using topics
- Each set as a separate project
- Project names designed so only the brand acts as match trigger
- Segment description encapsulated in brackets
