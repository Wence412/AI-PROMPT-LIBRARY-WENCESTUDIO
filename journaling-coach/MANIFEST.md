# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      journaling-coach.md
Category:           Psychology
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate:    🟠 Crisis Safety Boundary present; no additional clinical
  review required beyond what's already in place.

| Engine           | File                  | Complexity  | Tools Used  |
|------------------|-----------------------|-------------|-------------|
| Claude Sonnet 4.6| claude-4-6.md         | Simple      | none        |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Simple      | none        |
| GPT-OSS 120B     | gpt-oss-120b.md       | Simple      | none        |

Variables to inject before use:
  {{MOOD}}, {{TOPIC}}, {{TIME}}, {{STYLE}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Crisis Safety Boundary, evaluated
  before any journaling prompt in every variant (v1-legacy, claude-4-6,
  gemini-3-1-pro, gpt-oss-120b). This prompt asks users what's on their
  mind before every session and offers a "Processing" style explicitly
  meant for working through difficult material — an open door for a user
  in crisis to disclose more than a routine journaling request. On
  detection of self-harm, suicidal ideation, intent to harm others, or acute
  psychiatric crisis, the prompt now outputs a dedicated crisis-response
  block (988 / findahelpline.com / emergency services) and hard-stops before
  running the normal session.
  Source: Migration Audit §04/§10, P1 finding "Journaling coach solicits
  open emotional disclosure with no crisis-escalation path."
  Module: `modules/crisis-safety-boundary.md`.
- **[FIX]** Removed the forced mandatory chain-of-thought output block from
  claude-4-6.md; reasoning is now brief internal guidance rather than a
  mandatory separate visible block. Added an explicit constraint against
  ever emitting a numeric confidence score.
- **[GOVERNANCE]** Flagged 🟠 governance gate (see above); this prompt was
  previously deployed with no such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No crisis-escalation path.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Crisis Safety Boundary present and evaluated first, in every variant
  ☑ Crisis resources current (988 US / findahelpline.com international)
  ☑ No numeric confidence score anywhere in the output
