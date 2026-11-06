# Output template

Use this structure for the deliverable. The example content is illustrative (DMEA, digital health trade fairs) — replace it with the client's real research. Do not copy example prompts into a client deliverable.

---

## 1. Inputs

| Input | Status | Notes |
|---|---|---|
| Brand domain | Provided | dmea.de |
| Focus topics / segments | Provided | Digital health trade fairs |
| Competitors | Provided / Proposed & confirmed | HIMSS Europe, MEDICA, … |
| Brand research | Provided / None — own research used | … |
| Sales transcripts / forms | Provided / Not provided | If not provided: "Prompts are research-based, not based on prospect language." |
| Region / language | DE, English + German | |

## 2. Working brief

- **Match trigger:** `DMEA` (variants seen: …). Trigger risk: low / high — reason.
- **Category language:** …
- **Segment: Digital health trade fairs** — buyer problem, personas, decision criteria, competitor set.
- **Prospect language** (only if transcripts/forms provided): recurring phrases, pains, comparison pairs, objections.

## 3. Projects per segment

### Segment: Digital health trade fairs

#### Project: `DMEA [Market_Digital_Health_Trade_Fairs]`
- **Set:** Market — open-field visibility. **Key metrics:** Mentions, AI Visibility.
- **Excluded operational intents:** tickets, travel, programme details, networking.

**Topic: Trade Fair Discovery & Selection**
| # | Prompt | Source |
|---|---|---|
| 1 | Which trade fairs should a hospital IT leader in Europe attend to keep up with digital health? | research |
| 2 | … | prospect-language |

**Topic: Comparison of Trade Fairs**
| # | Prompt | Source |
|---|---|---|
| 1 | How do the major European digital health events differ in audience and focus? | research |

**Topic: Leadership or Ranking Logic**
| # | Prompt | Source |
|---|---|---|
| 1 | What is the most important digital health trade fair in Europe? | research |

#### Project: `DMEA [Brand_Digital_Health_Trade_Fairs]`
- **Set:** Brand — framing of explicit demand. **Key metrics:** response patterns, sentiment.

**Topic: Reputation & What It's Known For**
| # | Prompt | Source |
|---|---|---|
| 1 | What is DMEA known for in the digital health industry? | research |

#### Project: `DMEA [Comparison_Digital_Health_Trade_Fairs]`
- **Set:** Comparison — direct competitive argumentation. **Key metrics:** argument patterns, sentiment.

**Topic: Head-to-Head**
| # | Prompt | Source |
|---|---|---|
| 1 | DMEA vs HIMSS Europe: which is better for meeting healthcare IT decision-makers? | research |

## 4. CSV for import

File: `<brand>_rankscale_prompts.csv`

```
project_name,set,segment,topic,prompt,source
"DMEA [Market_Digital_Health_Trade_Fairs]",Market,Digital health trade fairs,Trade Fair Discovery & Selection,"Which trade fairs should a hospital IT leader in Europe attend to keep up with digital health?",research
```

## 5. Notes & next steps

- Trigger-risk warnings (if any).
- Operational intents excluded and where they could go instead.
- Competitors proposed by Claude that still need client confirmation.
- Next steps: create the projects in Rankscale with the exact names above → import prompts / create topics → choose engines → activate.
