# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      executive-coach.md
Category:           Coaching
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — safety-critical output-path change + false-promise removal)

Governance Gate:    🟠 Crisis Safety Boundary present; no additional clinical review
  required beyond what's already in place. Additionally: confidentiality claim
  removed — verify no other unenforceable promises remain on any future edit.

| Engine           | File                  | Complexity  | Tools Used  |
|------------------|-----------------------|-------------|-------------|
| Claude Sonnet 4.6| claude-4-6.md         | Moderate    | none        |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Moderate    | none        |
| GPT-OSS 120B     | gpt-oss-120b.md       | Moderate    | none        |

Variables to inject before use:
  {{COACHEE_NAME}}, {{COACHEE_ROLE}}, {{COMPANY_CONTEXT}}, {{COACHING_FOCUS}},
  {{CURRENT_CHALLENGE}}, {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a Crisis Safety Boundary, evaluated before any
  coaching logic in every variant (v1-legacy, claude-4-6, gemini-3-1-pro,
  gpt-oss-120b). Framed as a lower-emphasis safety net appropriate to
  executive coaching's lower baseline exposure (per severity tiering in
  `modules/crisis-safety-boundary.md`), but carrying the same concrete
  resources (988 / findahelpline.com) and hard stop on the normal session as
  the rest of the emotionally-sensitive-disclosure cluster.
  Source: Migration Audit §04/§10, extending the cbt-companion P0 fix.
- **[CRITICAL FIX]** Removed the unenforceable confidentiality promise
  ("Maintain strict confidentiality mindset") from v1-legacy.md and replaced
  it with an honest "A Note on Privacy" statement — this is an AI tool, not a
  licensed human coach bound by a professional ethics code, and the prior
  wording implied a guarantee the tool cannot make.
  Source: Migration Audit §08, "Unenforceable confidentiality promise + PII
  in prompt."
- **[FIX]** Trimmed persona inflation — "elite executive coach with 20+
  years... ICF Master Certified" credential-stacking reduced to role-relevant
  framing, per `modules/coaching-session-scaffold.md` persona-inflation
  guidance and Migration Audit §08.
- **[FIX]** Removed the `<confidence>` footer pattern risk and the
  `<agentic_hooks>` block from claude-4-6.md (this prompt never carried a
  literal `<confidence>` tag, but the constraint against emitting one is now
  explicit, matching the rest of the cluster).
- **[FIX]** claude-4-6.md: removed `<chain_of_thought>mandatory</chain_of_thought>`
  from `<thinking_config>`; the `<thinking>` output node is now brief internal-
  reasoning guidance rather than a mandatory separate visible block.
- **[GOVERNANCE]** Flagged 🟠 governance gate (see above) — lower acuity than
  cbt-companion's 🔴 gate, but the confidentiality fix should be spot-checked
  against any other unenforceable claims on future edits.

### v1.0 — 2025-12-19 (prior)
- Initial library entry. No crisis-escalation path. Contained an
  unenforceable confidentiality promise and unearned credential-stacking
  persona ("20+ years," "ICF Master Certified"). claude-4-6.md carried a
  mandatory chain-of-thought output block and an unused `<agentic_hooks>`
  block.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Crisis Safety Boundary present and evaluated first, in every variant
  ☑ Crisis resources current (988 US / findahelpline.com international)
  ☑ No numeric confidence score anywhere in the output
  ☑ No unenforceable confidentiality promise in the prompt
  ☐ Spot-check for any other unenforceable claims on next edit
