# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      real-estate-market-researcher.md (renamed from market-researcher.md on 2026-08-24)
Category:           Real Estate
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-path change affecting local market statistics)

Governance Gate:    🟡 VERIFY BEFORE ACTING ON ANY MARKET STATISTIC
  This prompt produces local market statistics that can drive an investment
  or relocation decision. Every figure marked "Data Unavailable" requires
  independent verification (MLS, county records, a live lookup) before use.

| Engine           | File                  | Complexity   | Tools Used |
|------------------|-----------------------|--------------|------------|
| Claude Sonnet 4.6| claude-4-6.md         | Intermediate | none       |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Intermediate | search     |
| GPT-OSS 120B     | gpt-oss-120b.md       | Intermediate | search     |

Variables to inject before use:
  {{LOCATION}}, {{PROPERTY_TYPES}}, {{PURPOSE}}, {{FOCUS}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added the mandatory Hallucination Guard (from
  `modules/hallucination-guard.md`) to every variant (v1-legacy, claude-4-6,
  gemini-3-1-pro, gpt-oss-120b). Every Market Snapshot statistic (median
  home price, median rent, days on market, inventory), comp, and trend
  percentage must now be labeled "Data Unavailable — [what input or lookup
  would resolve this]" unless supplied by the user or retrieved via an
  actual tool lookup this turn. Source: Migration Audit §10, finding "~55
  of 70 prompts had no missing-data fallback; real-estate-market-researcher
  produced specific-looking median-price and comp figures with no
  distinction between sourced data and general knowledge presented as
  current local statistics."
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md, the `### Confidence` section from gemini-3-1-pro.md, and
  the `**Confidence & Caveats**` field from gpt-oss-120b.md — a bare
  confidence score invited treating an unverified local statistic as
  researched fact.
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>`.
- **[GOVERNANCE]** Added a Yellow governance gate (see above); this prompt
  was previously deployed with no missing-data fallback on local market
  statistics at all.

### v1.1 — 2026-08-24
- **[RENAME]** `market-researcher` → `real-estate-market-researcher`, per
  Migration Audit §07: confirmed distinct from `market-research` (a
  startup/business validation report) on direct comparison — the only
  collision was the folder name and a shared "📊 Market Research" header.
  No content or variable changes; disambiguation only.

### v1.0 — 2025-12-19 (prior)
- Initial library entry (as `market-researcher.md`). No missing-data
  fallback — median price, rent, DOM, and inventory figures were filled in
  freely with no distinction between sourced and invented numbers.
  claude-4-6.md carried a bare `<confidence>` footer and mandatory
  chain-of-thought; gemini/gpt-oss variants carried bare confidence fields.

Deployment checklist:
  ☑ Variables populated
  ☑ Extended Thinking / Extended Reasoning enabled in model panel
  ☑ Hallucination Guard present and evaluated for every market statistic
  ☑ Unsupplied/unretrieved figures rendered as "Data Unavailable," not
    presented as researched fact
  ☑ No numeric confidence score anywhere in the output
  ☐ Independent verification obtained for every "Data Unavailable" field before acting on it
