# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      listing-writer.md
Category:           Real Estate
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-integrity change)

| Engine           | File                  | Complexity  | Tools Used |
|------------------|-----------------------|-------------|------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none       |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none       |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none       |

Variables to inject before use:
  {{ADDRESS}}, {{PRICE}}, {{BEDS_BATHS}}, {{SQFT}}, {{LOT}}, {{YEAR}},
  {{FEATURES}}, {{UPDATES}}, {{UNIQUE}}, {{NEIGHBORHOOD}}, {{BUYER}},
  {{TONE}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Hallucination Guard clause to
  v1-legacy.md's prompt body and to the `<constraints>`/`[CONSTRAINTS]` block
  of every model variant (claude-4-6, gemini-3-1-pro, gpt-oss-120b). No
  property fact — beds/baths, square footage, lot size, year built, a
  feature, a recent update, an amenity, a school rating, a nearby landmark,
  or a neighborhood claim — may be stated unless it was supplied by the user
  or is a plain restatement of supplied input. A field needed for a section
  but not supplied is omitted rather than filled with a plausible invention.
  This closes a fair-housing/liability exposure, not just an accuracy gap:
  an invented amenity or claim in public-facing MLS copy is a real risk to
  the listing agent. Source: Migration Audit hallucination-guard cluster
  finding; clause drawn from
  [modules/hallucination-guard.md](../modules/hallucination-guard.md).
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md and the "Confidence" / "Confidence & Caveats" fields from
  gemini-3-1-pro.md and gpt-oss-120b.md.
- **[FIX]** claude-4-6.md no longer declares
  `<chain_of_thought>mandatory</chain_of_thought>` in `<thinking_config>`,
  and the reasoning step inside `<output_format>` is now brief
  internal-reasoning guidance rather than a required separate visible
  output block.
- **[CLEANUP]** Trimmed persona inflation — "luxury real estate copywriter"
  reduced to "real estate copywriter" in all four files. Tone
  (luxury/family-friendly/modern/cozy) is already a user-supplied variable;
  hard-coding "luxury" into the persona biased every listing regardless of
  the requested tone.
- **[UNCHANGED]** Core section structure (MLS Listing through SEO Keywords),
  all variables, and domain task logic are unchanged — this pass is a
  hardening pass, not a rewrite.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No guardrail against invented property facts,
  amenities, or neighborhood claims; claude-4-6.md carried a bare
  `<confidence>` footer and forced mandatory chain-of-thought output.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Hallucination Guard present in all four files
  ☑ No numeric confidence score anywhere in the output
  ☑ Verified no unsupplied property fact appears in output on a thin-input
    test case before deploying to a live MLS feed
