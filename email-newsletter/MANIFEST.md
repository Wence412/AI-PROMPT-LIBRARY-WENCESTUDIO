# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      email-newsletter.md
Category:           Creative Writing & Content
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-integrity change)

| Engine           | File                  | Complexity  | Tools Used |
|------------------|-----------------------|-------------|------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none       |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none       |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none       |

Variables to inject before use:
  {{NEWSLETTER_NAME}}, {{EMAIL_TYPE}}, {{FREQUENCY}}, {{PRIMARY_CTA}},
  {{MAIN_TOPIC}}, {{KEY_POINTS}}, {{LINKS}}, {{TONE}}, {{AUDIENCE_SEGMENT}},
  {{JOURNEY_STAGE}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Hallucination Guard clause to
  v1-legacy.md's prompt body and to the `<constraints>`/`[CONSTRAINTS]` block
  of every model variant (claude-4-6, gemini-3-1-pro, gpt-oss-120b). The
  Performance Prediction section's Open Rate % and CTR % were being
  presented as fact with no data source — this prompt has no access to a
  list's actual send history or a live benchmark unless the user supplies
  one. The section is renamed "Performance Target (Illustrative, not a
  measured prediction)" and every figure in it must now carry that label,
  grounded in user-supplied historical data when available rather than a
  generic invented industry number. Source: Migration Audit §10, P1 finding
  "Performance Prediction section presented as fact with no data source";
  clause drawn from
  [modules/hallucination-guard.md](../modules/hallucination-guard.md)
  ("engagement metric" row).
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md and the "Confidence Level & Known Gaps" /
  "Confidence & Caveats" fields from gemini-3-1-pro.md and gpt-oss-120b.md.
  A numeric confidence score does not fix an unlabeled fabricated metric;
  the guard above does.
- **[FIX]** Removed the `<agentic_hooks>` block from claude-4-6.md — it was
  inert scaffolding (`tool_use`/`sub_agent_trigger` never wired to anything).
- **[FIX]** claude-4-6.md no longer declares
  `<chain_of_thought>mandatory</chain_of_thought>` in `<thinking_config>`,
  and the `<thinking>` output node is now brief internal-reasoning guidance
  rather than a required separate visible output block.
- **[CLEANUP]** Trimmed persona inflation in claude-4-6.md ("expert email
  copywriter" → "email copywriter") across the prompt body.
- **[UNCHANGED]** Core section structure (Subject Lines through Send Time
  Recommendation), all variables, and domain task logic are unchanged — this
  pass is a hardening pass, not a rewrite.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. Performance Prediction section stated a specific
  Open Rate % / CTR % as fact with no data source or labeling; claude-4-6.md
  carried a bare `<confidence>` footer, an unused `<agentic_hooks>` block,
  and forced mandatory chain-of-thought output.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Hallucination Guard present in all four files
  ☑ Performance Target section labeled "Illustrative, not a measured
    prediction" in every variant
  ☑ No numeric confidence score anywhere in the output
  ☑ Output reviewed against CATALOG.md quality standard
