# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      emotional-intelligence.md
Category:           Personal Development
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
  {{SITUATION}}, {{REACTION}}, {{OTHERS_REACTION}}, {{GOAL}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a Crisis Safety Boundary, evaluated before any EQ
  coaching logic in every variant (v1-legacy, claude-4-6, gemini-3-1-pro,
  gpt-oss-120b). Framed as a lower-emphasis safety net — this prompt is not
  disclosure-focused, but a user can volunteer crisis content mid-session —
  carrying the same concrete resources (988 / findahelpline.com) and hard
  stop on the normal session as the rest of the cluster.
  Source: Migration Audit §04/§10, "Four more prompts handle emotionally
  sensitive disclosure with no scope/safety boundary."
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer from
  claude-4-6.md and the "Confidence"/"Confidence & Caveats" sections from
  gemini-3-1-pro.md and gpt-oss-120b.md. A numeric confidence score on
  emotionally personal output is fake precision, not just unhelpful.
- **[FIX]** Removed the `<agentic_hooks>` block from claude-4-6.md (it was
  unused — declared `none`/`none`).
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>`; the `<thinking>` output node is now brief
  internal-reasoning guidance rather than a mandatory separate visible block.
- **[GOVERNANCE]** Flagged 🟠 governance gate (see above); this prompt was
  previously deployed with no such gate.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No crisis-escalation path. claude-4-6.md carried a
  bare `<confidence>` footer and unused `<agentic_hooks>` block; gemini and
  gpt-oss variants carried a "Confidence" output section.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Crisis Safety Boundary present and evaluated first, in every variant
  ☑ Crisis resources current (988 US / findahelpline.com international)
  ☑ No numeric confidence score anywhere in the output
