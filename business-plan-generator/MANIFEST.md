# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      business-plan-generator.md
Category:           Business, Strategy & Planning
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — grounding/hallucination-guard hardening)

| Engine           | File                  | Complexity  | Tools Used          |
|------------------|-----------------------|-------------|----------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Complex     | search (optional)   |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Complex     | search (optional)   |
| GPT-OSS 120B     | gpt-oss-120b.md       | Complex     | search, code interp |

Variables to inject before use:
  {{BUSINESS_NAME}}, {{INDUSTRY}}, {{BUSINESS_MODEL}}, {{ONE_LINER}},
  {{STAGE}}, {{PRODUCT_DESCRIPTION}}, {{PROBLEM}}, {{TARGET_CUSTOMER}},
  {{UNIQUE_VALUE}}, {{PURPOSE}}, {{FUNDING_AMOUNT}}, {{TIMEFRAME}},
  {{TEAM_INFO}}, {{TRACTION}}, {{ASSETS}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Hallucination Guard clause to
  v1-legacy.md's prompt body and to the `<constraints>`/`[CONSTRAINTS]` block
  of every model variant (claude-4-6, gemini-3-1-pro, gpt-oss-120b). Any
  market size (TAM/SAM/SOM), revenue projection, unit-economics figure (CAC,
  LTV, LTV:CAC, payback period), or funding allocation that is not supplied
  by the user or directly derivable from their input must now be rendered as
  "Data Unavailable — [what input would resolve this]" instead of a
  plausible-sounding fabricated number. Source: Migration Audit §10/§16,
  P1 finding "forced-precision numeric output with no data grounding";
  clause drawn from [modules/hallucination-guard.md](../modules/hallucination-guard.md)
  ("financial figure" row).
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md and the "Confidence Level & Known Gaps" /
  "Confidence & Caveats" fields from gemini-3-1-pro.md and gpt-oss-120b.md.
  A bare numeric confidence score on an investor-facing financial document
  is fake precision, not a genuine calibration signal.
- **[FIX]** Removed the `<agentic_hooks>` block from claude-4-6.md — it was
  inert scaffolding (`tool_use`/`sub_agent_trigger` never wired to anything).
- **[FIX]** claude-4-6.md no longer declares `<chain_of_thought>mandatory</chain_of_thought>`
  in `<thinking_config>`, and the `<thinking>` node inside `<output_format>`
  is now internal-reasoning guidance rather than a required separate output
  block — extended thinking is still used, just not forced into the visible
  response.
- **[FIX]** Trimmed unearned credential-stacking language ("world-class
  business strategist... 100+ companies") from the role description in all
  four files, replaced with a plain, defensible framing.
- **[UNCHANGED]** Core section structure (Executive Summary through
  Appendix), all variables, and domain task logic are unchanged — this pass
  is a hardening pass, not a rewrite.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No missing-data fallback for financial figures;
  fake confidence footers present in claude-4-6/gemini/gpt-oss variants;
  inert `<agentic_hooks>` block in claude-4-6; chain-of-thought forced as a
  mandatory separate output block in claude-4-6.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  ☑ Hallucination Guard present in all four files
  ☑ No numeric confidence score anywhere in the output
  ☑ Output reviewed against CATALOG.md quality standard
