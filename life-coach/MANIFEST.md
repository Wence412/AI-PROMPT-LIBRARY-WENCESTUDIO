# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      life-coach.md
Category:           Coaching
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — safety-critical output-path change)

Governance Gate:    🟠 Crisis Safety Boundary present; no additional clinical
  review required beyond what's already in place.

| Engine           | File                  | Complexity  | Tools Used  |
|------------------|-----------------------|-------------|-------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none        |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none        |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none        |

Variables to inject before use:
  {{CLIENT_NAME}}, {{LIFE_STAGE}}, {{PRIMARY_GOAL}}, {{CURRENT_SITUATION}},
  {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory Crisis Safety Boundary, evaluated
  before any coaching logic in every variant (v1-legacy, claude-4-6,
  gemini-3-1-pro, gpt-oss-120b). This prompt solicits open-ended emotional
  disclosure ("what's on your heart"), placing it in the full-boundary tier
  of the cluster alongside cbt-companion — not the lower-emphasis tier used
  for executive-coach. On detection of self-harm, suicidal ideation, intent
  to harm others, or acute psychiatric crisis, the prompt now outputs a
  dedicated crisis-response block (988 / findahelpline.com / emergency
  services) and hard-stops before running the normal session.
  Source: Migration Audit §04/§10, P1 finding "Life coach solicits open
  emotional disclosure with no crisis-escalation path."
  Module: `modules/crisis-safety-boundary.md`.
- **[FIX]** Removed the forced mandatory chain-of-thought output block from
  claude-4-6.md; the `<thinking>` output node is now brief internal-
  reasoning guidance rather than a mandatory separate visible block. Added
  an explicit constraint against ever emitting a numeric confidence score —
  false precision is inappropriate on emotionally personal output.
- **[FIX]** Trimmed the unearned "certified" credential claim from the
  persona ("compassionate, certified life coach" → "compassionate life
  coach") — an AI tool cannot hold a coaching certification.
- **[GOVERNANCE]** Flagged 🟠 governance gate (see above); this prompt was
  previously deployed with no such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No crisis-escalation path. Persona claimed
  "certified" status the tool cannot hold.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Crisis Safety Boundary present and evaluated first, in every variant
  ☑ Crisis resources current (988 US / findahelpline.com international)
  ☑ No numeric confidence score anywhere in the output
  ☑ No unearned "certified" credential claim in the persona
