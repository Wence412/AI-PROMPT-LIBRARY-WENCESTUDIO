# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      market-research.md
Category:           Entrepreneurs
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-path change affecting market-sizing figures)

Governance Gate:    🟡 VERIFY BEFORE USING IN A PITCH DECK OR FUNDING APPLICATION
  This prompt produces market-sizing and competitor data that can end up in
  front of investors. Every figure marked "Data Unavailable" or "(estimate,
  not verified)" requires independent verification before use.

| Engine           | File                  | Complexity   | Tools Used                   |
|------------------|-----------------------|--------------|--------------------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Intermediate | none                            |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Intermediate | search                          |
| GPT-OSS 120B     | gpt-oss-120b.md       | Intermediate | search, code interpreter (optional) |

Variables to inject before use:
  {{MARKET}}, {{GEOGRAPHY}}, {{TIMEFRAME}}, {{PRODUCT}}, {{CUSTOMER}},
  {{HYPOTHESIS}}, {{DEPTH}}, {{DATA_PRIORITY}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added the mandatory Hallucination Guard (from
  `modules/hallucination-guard.md`) to every variant (v1-legacy, claude-4-6,
  gemini-3-1-pro, gpt-oss-120b). Every TAM/SAM/SOM figure, growth rate
  (CAGR), market-share percentage, and named-competitor claim must now be
  labeled "Data Unavailable" or explicitly "(estimate, not verified)"
  unless supplied by the user or retrieved via an actual tool lookup this
  turn. Source: Migration Audit §10, finding "~55 of 70 prompts had no
  missing-data fallback; market-research produces TAM/SAM/SOM and
  competitor-share figures that read as sourced market data with no
  distinction from estimates, and these numbers routinely flow into pitch
  decks and funding applications."
- **[ADDED]** "Insufficient Data" as a valid hypothesis-validation outcome,
  and a requirement that the Gaps in Research section enumerate every
  "Data Unavailable" field.
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md, the `### Confidence` section from gemini-3-1-pro.md, and
  the `**Confidence & Caveats**` field from gpt-oss-120b.md — a bare
  confidence score invited treating an unverified market figure as
  researched fact.
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>` and converted the `<thinking>` node under
  `<output_format>` from a mandatory visible block into internal-reasoning
  guidance that is not rendered in the report.
- **[GOVERNANCE]** Added a Yellow governance gate (see above); this prompt
  was previously deployed with no missing-data fallback on market-sizing
  data at all.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No missing-data fallback — TAM/SAM/SOM figures,
  growth rates, and competitor market shares were filled in freely with no
  distinction between sourced and invented numbers. claude-4-6.md carried a
  bare `<confidence>` footer and mandatory chain-of-thought; gemini/gpt-oss
  variants carried bare confidence fields.

Deployment checklist:
  ☑ Variables populated
  ☑ Extended Thinking / Extended Reasoning enabled in model panel
  ☑ Hallucination Guard present and evaluated for every market figure
  ☑ Unsupplied/unretrieved figures rendered as "Data Unavailable" or
    "(estimate, not verified)," not presented as sourced fact
  ☑ No numeric confidence score anywhere in the output
  ☐ Independent verification obtained for every unverified figure before use in investor-facing materials
