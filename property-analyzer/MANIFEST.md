# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      property-analyzer.md
Category:           Real Estate
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-path change affecting financial figures)

Governance Gate:    🟡 NOT FINANCIAL ADVICE
  This prompt produces a financial analysis that can drive a real purchase
  decision. Every figure marked "Data Unavailable" was not supplied and was
  not invented — it requires independent verification before being used in
  an offer or financing decision.

| Engine           | File                  | Complexity   | Tools Used                    |
|------------------|-----------------------|--------------|--------------------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Intermediate | none                           |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Intermediate | search (optional)              |
| GPT-OSS 120B     | gpt-oss-120b.md       | Intermediate | search (optional), code interpreter |

Variables to inject before use:
  {{LOCATION}}, {{PROPERTY_TYPE}}, {{PRICE}}, {{BEDS_BATHS}}, {{SQFT}},
  {{YEAR}}, {{CONDITION}}, {{CURRENT_RENT}}, {{MARKET_RENT}}, {{HOA}},
  {{TAXES}}, {{INSURANCE}}, {{STRATEGY}}, {{FINANCING}}, {{GOALS}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added the mandatory Hallucination Guard (from
  `modules/hallucination-guard.md`, financial-figure parameterization) to
  every variant (v1-legacy, claude-4-6, gemini-3-1-pro, gpt-oss-120b). Any
  price, rent, expense, comp, or market figure not supplied by the user or
  directly calculable from supplied figures must now render literally
  "Data Unavailable — [what input would resolve this]" instead of an
  invented plausible-sounding number. Source: Migration Audit §10, finding
  "~55 of 70 prompts had no missing-data fallback; property-analyzer
  produces cap rates, comps, and offer prices that read as researched
  figures with no distinction from guesses."
- **[ADDED]** "Insufficient Data for a Verdict" as an explicit valid
  recommendation outcome when key financials are missing, instead of
  forcing Strong Buy/Buy/Hold/Pass off guessed numbers.
- **[ADDED]** Explicit "not financial advice" disclaimer on every variant's
  output, with instruction to independently verify every "Data Unavailable"
  field before acting on the report.
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md, the `### Confidence` section from gemini-3-1-pro.md, and
  the `**Confidence & Caveats**` field from gpt-oss-120b.md — false
  precision on an investment figure is actively misleading, not just
  unhelpful.
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>` and converted the `<thinking>` node under
  `<output_format>` from a mandatory visible block into internal-reasoning
  guidance that is not rendered in the report.
- **[GOVERNANCE]** Added a Yellow governance gate (see above); this prompt
  was previously deployed with no missing-data fallback and no financial-
  advice disclaimer at all.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No missing-data fallback — market rent, comps, tax,
  and insurance estimates were filled in freely with no distinction between
  supplied and invented figures. claude-4-6.md carried a bare `<confidence>`
  footer and mandatory chain-of-thought; gemini/gpt-oss variants carried
  bare confidence fields. No "not financial advice" disclaimer.

Deployment checklist:
  ☑ Variables populated
  ☑ Extended Thinking / Extended Reasoning enabled in model panel
  ☑ Hallucination Guard present and evaluated for every figure
  ☑ Unsupplied figures rendered as "Data Unavailable," not omitted or guessed
  ☑ No numeric confidence score anywhere in the output
  ☑ "Not financial advice" disclaimer present
  ☐ Independent verification obtained for every "Data Unavailable" field before use
