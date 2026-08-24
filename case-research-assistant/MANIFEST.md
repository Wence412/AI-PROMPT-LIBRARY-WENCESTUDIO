# PROMPT UPDATE MANIFEST
────────────────────────
Library Entry:      case-research-assistant.md
Category:           Research & Analysis (Legal)
Updated:            2026-08-24
Upgraded By:        WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version:            2.0.0 (MAJOR — citation-integrity fix)

Governance Gate:    🟠 Verify every citation independently before relying on
  it for litigation strategy. This prompt produces legal research that can
  feed into filings; a non-user-supplied citation is only ever a research
  lead until confirmed against a primary source (Westlaw, Lexis, or the
  court's docket).

| Engine           | File                  | Complexity  | Tools Used        |
|------------------|-----------------------|-------------|-------------------|
| Claude Sonnet 4.6| claude-4-6.md         | Complex     | search (optional) |
| Gemini 3.1 Pro   | gemini-3-1-pro.md     | Complex     | search (optional) |
| GPT-OSS 120B     | gpt-oss-120b.md       | Complex     | search (optional) |

Variables to inject before use:
  {{LEGAL_QUESTION}}, {{JURISDICTION}}, {{AREA_OF_LAW}}, {{FACTS}},
  {{POSITION}}, {{OPPOSING_ARGUMENT}}, {{FOCUS}}, {{SPECIFIC_CASE}},
  {{CONTEXT_OR_NONE}}

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[CRITICAL FIX]** Added a mandatory, structural Citation Verification
  Gate to every variant (v1-legacy, claude-4-6, gemini-3-1-pro,
  gpt-oss-120b), adapted from `legal-brief-drafter`'s gate and from
  `modules/hallucination-guard.md`'s citation-domain parameterization. The
  model may cite case law only if it was supplied by the user or actually
  retrieved this turn via a real search/lookup tool call; anything else must
  be tagged `AUTHORITY NEEDED — NOT VERIFIED` rather than invented from
  memory. Source: Migration Audit §07/§10, P1 finding "Legal research
  prompt has no citation-verification gate — model free to hallucinate
  case law with no structural check."
- **[ADDED]** Structural Citation Audit table appended to every memo in
  every variant, auditing each citation against USER-SUPPLIED / RETRIEVED
  THIS TURN (tool) / AUTHORITY NEEDED — NOT VERIFIED status — present even
  when the audit is all "NOT VERIFIED."
- **[FIX]** Removed the `<confidence>0–100</confidence>` footer
  (claude-4-6.md) and the "Confidence Level & Known Gaps" /
  "Confidence & Caveats" output fields (gemini-3-1-pro.md,
  gpt-oss-120b.md). A numeric or self-reported confidence score on legal
  research is false precision that invites the reader to skip the actual
  verification step.
- **[FIX]** Removed the dead `<agentic_hooks>` scaffold from claude-4-6.md
  and the mandatory-visible `<chain_of_thought>` requirement from
  `<thinking_config>`; `<thinking>` in `<output_format>` is now internal
  reasoning guidance, not a required output block.
- **[FIX]** Trimmed "world-class" credential-stacking from the persona in
  claude-4-6.md, gemini-3-1-pro.md, and gpt-oss-120b.md to
  role-relevant expertise only.
- **[GOVERNANCE]** Flagged Amber governance gate (see above); this prompt
  was previously deployed with no gate at all.

### v1.0 — 2025-12-19 / 2026-03-26 (prior)
- Initial library entry. v1-legacy.md had only a generic "verify all
  citations" disclaimer with no structural mechanism. claude-4-6.md carried
  a bare `<confidence>` footer and unbounded persona inflation
  ("world-class"). No variant blocked the model from inventing a citation
  outright.

Deployment checklist:
  ☑ Variables populated
  ☑ Thinking Mode set to Extended in model panel
  ☑ Citation Verification Gate present and evaluated before drafting, in every variant
  ☑ Citation Audit table required in output, in every variant
  ☑ Grounding source linked (Gemini) or tool permissions confirmed (Claude/GPT-OSS)
  ☑ No numeric or self-reported confidence score anywhere in the output
  ☐ Every "AUTHORITY NEEDED — NOT VERIFIED" and "RETRIEVED" citation confirmed against a primary source before use in litigation strategy
