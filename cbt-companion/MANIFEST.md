# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      cbt-companion.md
Category:           Personal Development & Coaching
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate:    🔴 HUMAN REVIEW REQUIRED
  This prompt handles unsupervised mental-health self-disclosure. A qualified
  reviewer (clinical or safety-trained) must sign off on the Crisis Safety
  Boundary wording and resource list (988 / findahelpline.com) before this
  version is deployed to end users, and on any future edit to that block.

| Engine           | File                  | Complexity  | Tools Used  |
|------------------|-----------------------|-------------|-------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none        |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none        |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none        |

Variables to inject before use:
  {{SITUATION}}, {{FEELINGS}}, {{THOUGHTS}}, {{FOCUS}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Crisis Safety Boundary, evaluated
  before any CBT technique in every variant (v1-legacy, claude-4-6,
  gemini-3-1-pro, gpt-oss-120b). On detection of self-harm, suicidal
  ideation, intent to harm others, or acute psychiatric crisis, the prompt
  now outputs a dedicated crisis-response block (988 / findahelpline.com /
  emergency services) and hard-stops before running the normal session.
  Source: Migration Audit §04/§05, P0 finding "Mental-health coaching
  prompt has no crisis-escalation path."
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md. A numeric confidence score on a mental-health response is
  fake precision that is actively inappropriate in this domain, not merely
  unhelpful — it implied a calibration the model does not have.
- **[GOVERNANCE]** Flagged HUMAN REVIEW required (see gate above); this
  prompt was previously deployed with no such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No crisis-escalation path. claude-4-6.md carried a
  bare `<confidence>` footer inherited from the batch modernization pass.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Crisis Safety Boundary present and evaluated first, in every variant
  ☑ Crisis resources current (988 US / findahelpline.com international)
  ☑ No numeric confidence score anywhere in the output
  ☐ Clinical/safety reviewer sign-off obtained (required before deploy)
