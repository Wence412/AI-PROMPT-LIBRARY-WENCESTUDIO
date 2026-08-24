# PROMPT UPDATE MANIFEST
Library Entry: legal-document-analyzer.md | Category: Legal | Updated: 2026-08-24
Upgraded By: WenceStudio Prompt Modernization Agent (UPOS-GF v3.0)
Version: 2.0.0 (MAJOR — merge + safety-critical change)

Governance Gate: 🟠 HUMAN REVIEW (legal counsel) recommended before relying on
  any negotiation or execution recommendation from this prompt.

Variables: {{DOCUMENT_TYPE}}, {{PARTIES}}, {{JURISDICTION}}, {{INDUSTRY}}, {{DEAL_VALUE}}, {{DOCUMENT_CONTENT}}, {{MY_ROLE}}, {{CONCERNS}}, {{QUESTIONS}}, {{MUST_HAVES}}, {{RED_LINES}}, {{NICE_TO_HAVES}}

| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | search (optional) |

## Change Log

### v2.0.0 — 2026-08-24 (this update)
- **[MERGE]** Absorbed `contract-reviewer` into this entry, per Migration
  Audit §07 finding "contract-reviewer ⇄ legal-document-analyzer — MERGE
  (near-identical purpose)." This entry was chosen as canonical because it
  already shipped the Disclaimer + Questions for Specialized Counsel
  escalation pattern in v1, which contract-reviewer lacked.
  contract-reviewer's negotiation-specific output (must-haves/red-lines/
  nice-to-haves, dealbreaker analysis, negotiation strategy) is preserved as
  an optional "Negotiation Mode" section, active only when those inputs are
  supplied — no functionality was dropped, both variable sets are retained.
  `contract-reviewer/` is now a deprecated redirect stub pointing here.
- **[FIX]** Added a Hallucination Guard clause for jurisdiction-specific and
  "market standard" claims (module: `modules/hallucination-guard.md`) —
  previously these were stated as fact with no uncertainty flag in either
  source prompt.
- **[GOVERNANCE]** Flagged for legal review before negotiation/execution
  reliance (audit §11: "contract-reviewer / legal-document-analyzer —
  Negotiation/execution decisions — Legal review before reliance").
- **[REMOVED]** The bare `<confidence>0–100</confidence>` footer from
  claude-4-6.md (both source variants had it) — replaced by the Hallucination
  Guard's explicit "Data Unavailable" marking, which is more actionable than
  an uncalibrated number.

### v1.0 — 2025-12-19 (prior, both entries)
- legal-document-analyzer and contract-reviewer existed as separate,
  overlapping prompts with no cross-cutting hallucination guard.

Deployment checklist:
  ☑ Variables populated (including optional Negotiation Mode inputs)
  ☑ Thinking Mode set to Extended in model panel
  ☑ Hallucination Guard present in every variant
  ☑ Negotiation Mode renders only when negotiation inputs are supplied
  ☑ Disclaimer present in every variant
  ☐ Legal counsel review obtained before acting on any negotiation/execution recommendation
