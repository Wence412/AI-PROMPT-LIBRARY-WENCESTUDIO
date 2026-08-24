# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      data-storyteller.md
Category:           Visualizations / Data & Analytics
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-integrity change)

| Engine           | File                  | Complexity  | Tools Used         |
|------------------|-----------------------|-------------|---------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Complex     | none                |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Complex     | none                |
| GPT-OSS 120B     | gpt-oss-120b.md       | Complex     | code interp (optional) |

Variables to inject before use:
  {{DATA}}, {{CONTEXT_INFO}}, {{AUDIENCE}}, {{FORMAT}}, {{TONE}}, {{QUESTION}}, {{ACTION}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[FIX]** Added a mandatory Data Integrity Guardrail to every variant
  (v1-legacy, claude-4-6, gemini-3-1-pro, gpt-oss-120b). Every statistic,
  trend claim, or data point in the generated narrative must now be
  traceable to the user-supplied `{{data}}` — either stated directly or a
  straightforward calculation from it. Claims that extend beyond the data
  (causal explanations, industry benchmarks, predictions) must be visibly
  flagged `[Inference]` rather than presented as fact, and sections the
  supplied data can't support must render "Data Unavailable — insufficient
  data supplied" instead of a fabricated finding. Source: Migration Audit
  P1 content/data-fabrication cluster finding; module: `modules/hallucination-guard.md`.
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer (claude-4-6.md)
  and the `### Confidence Level & Known Gaps` / `**Confidence & Caveats**`
  fields (gemini-3-1-pro.md, gpt-oss-120b.md) — unearned numeric/verbal
  confidence scores on a narrative built from possibly-thin data.
- **[FIX]** Removed the `<agentic_hooks>` block from claude-4-6.md (dead
  no-op scaffolding).
- **[FIX]** Removed `<chain_of_thought>mandatory</chain_of_thought>` from
  `<thinking_config>` and converted the `<thinking>` output node from a
  mandatory visible block into brief internal-reasoning guidance that
  precedes the response but is not itself a required output section.
- **[CLEANUP]** Trimmed persona inflation in claude-4-6.md ("world-class
  data journalist" → "data journalist").

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No guardrail against fabricated statistics or
  trend claims; claude-4-6.md carried a bare `<confidence>` footer and
  mandatory chain-of-thought output inherited from the batch modernization
  pass.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Data Integrity Guardrail present in every variant
  ☑ No numeric/verbal confidence score anywhere in the output
  ☑ `[Inference]` tagging and "Data Unavailable" fallback verified against a
    thin test dataset before deploying to a real analysis
