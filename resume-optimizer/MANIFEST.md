# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      resume-optimizer.md
Category:           Job Search
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — output-path change affecting claimed accomplishments)

Governance Gate:    🟡 NOT CAREER OR EMPLOYMENT ADVICE
  This prompt rewrites a resume a user submits to real employers. Every
  bullet marked "METRIC NEEDED" was not supplied and was not invented — the
  user must fill it in with an accurate number before submitting.

| Engine           | File                  | Complexity   | Tools Used |
|------------------|-----------------------|--------------|------------|
| Claude Sonnet 4.6| claude-4-6.md         | Intermediate | none       |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Intermediate | none       |
| GPT-OSS 120B     | gpt-oss-120b.md       | Intermediate | none       |

Variables to inject before use:
  {{CURRENT_RESUME}}, {{JOB_TITLE}}, {{COMPANY}}, {{JOB_DESCRIPTION}},
  {{FOCUS}}, {{CAREER_GOALS}}, {{STRENGTHS}}, {{GAPS}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added the mandatory Hallucination Guard (from
  `modules/hallucination-guard.md`, personal/biographical-claim
  parameterization) to every variant (v1-legacy, claude-4-6, gemini-3-1-pro,
  gpt-oss-120b). Any accomplishment, metric, title, or scope not present in
  the supplied resume/context must now be flagged "[METRIC NEEDED]" rather
  than invented, and a stated responsibility can never be silently upgraded
  into ownership the candidate didn't claim (e.g., "assisted with X" → "led
  X"). Source: Migration Audit §10, finding "~55 of 70 prompts had no
  missing-data fallback; resume-optimizer routinely filled quantification
  gaps with plausible-sounding numbers the candidate never provided and
  would have to defend under interview questioning."
- **[ADDED]** "Metrics Needed" output section, listing every bullet still
  missing a candidate-supplied number, so gaps are visible instead of
  silently filled.
- **[ADDED]** Explicit "not career or employment advice" disclaimer.
- **[REMOVED]** Persona credential-stacking ("15+ years of experience,"
  "Fortune 500 recruiting departments") across all three model variants —
  trimmed to role-relevant framing; the model has no such history and the
  claim added no value to rewrite quality.
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md, the `### Confidence` section from gemini-3-1-pro.md, and
  the `**Confidence & Caveats**` field from gpt-oss-120b.md — false
  precision on a document going to a real employer is misleading, not
  helpful.
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>` and converted the `<thinking>` node under
  `<output_format>` from a mandatory visible block into internal-reasoning
  guidance that is not rendered in the output.
- **[GOVERNANCE]** Added a Yellow governance gate (see above); this prompt
  was previously deployed with no fabrication gate on accomplishments and
  no career-advice disclaimer at all.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No missing-data fallback for accomplishment
  metrics — the model would freely invent plausible percentages and dollar
  figures. Persona opened with unearned credential-stacking. claude-4-6.md
  carried a bare `<confidence>` footer and mandatory chain-of-thought;
  gemini/gpt-oss variants carried bare confidence fields. No career-advice
  disclaimer.

Deployment checklist:
  ☑ Variables populated
  ☑ Extended Thinking / Extended Reasoning enabled in model panel
  ☑ Hallucination Guard present and evaluated for every bullet
  ☑ Missing metrics flagged "METRIC NEEDED," not invented or omitted
  ☑ No numeric confidence score anywhere in the output
  ☑ "Not career or employment advice" disclaimer present
  ☐ User has supplied a real number for every "METRIC NEEDED" flag before submitting the resume
