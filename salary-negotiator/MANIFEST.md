# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      salary-negotiator.md
Category:           Job Search
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — grounding/hallucination-guard hardening)

| Engine           | File                  | Complexity  | Tools Used          |
|------------------|-----------------------|-------------|----------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none                 |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | search (optional)   |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | search (optional)   |

Variables to inject before use:
  {{POSITION}}, {{COMPANY}}, {{STAGE}}, {{BASE}}, {{BONUS}}, {{EQUITY}},
  {{BENEFITS}}, {{OTHER}}, {{CURRENT_COMP}}, {{MARKET_RATE}}, {{COMPETING}},
  {{WALK_AWAY}}, {{IDEAL}}, {{LEVERAGE}}, {{CONCERNS}}, {{RELATIONSHIP}},
  {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Hallucination Guard clause to
  v1-legacy.md's prompt body and to the `<constraints>`/`[CONSTRAINTS]` block
  of every model variant (claude-4-6, gemini-3-1-pro, gpt-oss-120b). Any
  market rate, counter-offer number, or negotiation-outcome probability that
  is not supplied by the user or directly derivable from their input must
  now be rendered as "Data Unavailable — [what input would resolve this]"
  instead of a plausible-sounding fabricated figure — a fabricated
  compensation number can cost the user real money if they act on it.
  Source: Migration Audit §10/§16, P1 finding "forced-precision numeric
  output with no data grounding"; clause drawn from
  [modules/hallucination-guard.md](../modules/hallucination-guard.md)
  ("financial figure" row).
- **[FIX]** Added a user-facing "not financial or employment advice"
  disclaimer to the output format of all four files, instructing the user
  to verify any market-rate figures independently. Source: Migration Audit
  §11.
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md and the "Confidence Level & Known Gaps" /
  "Confidence & Caveats" fields from gemini-3-1-pro.md and gpt-oss-120b.md.
  A bare numeric confidence score on financial negotiation guidance is fake
  precision, not a genuine calibration signal.
- **[FIX]** Removed the `<agentic_hooks>` block from claude-4-6.md — it was
  inert scaffolding (`tool_use`/`sub_agent_trigger` never wired to anything).
- **[FIX]** claude-4-6.md no longer declares `<chain_of_thought>mandatory</chain_of_thought>`
  in `<thinking_config>`, and the reasoning step inside `<output_format>` is
  now internal-reasoning guidance rather than a required separate output
  block — extended thinking is still used, just not forced into the visible
  response.
- **[FIX]** Trimmed unearned credential-stacking language ("coached
  executives through thousands of negotiations") from the role description
  in all four files, replaced with a plain, defensible framing.
- **[UNCHANGED]** Core section structure (Situation Assessment through Risk
  Assessment), all variables, and domain task logic are unchanged — this
  pass is a hardening pass, not a rewrite.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No missing-data fallback for market rates,
  counter-offer numbers, or outcome probabilities; fake confidence footers
  present in claude-4-6/gemini/gpt-oss variants; inert `<agentic_hooks>`
  block in claude-4-6; chain-of-thought forced as a mandatory separate
  output block in claude-4-6.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Hallucination Guard present in all four files
  ☑ No numeric confidence score anywhere in the output
  ☑ "Not financial or employment advice" disclaimer present in output
  ☑ Output reviewed against CATALOG.md quality standard
