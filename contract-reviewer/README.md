# ⚠️ Deprecated — merged into `legal-document-analyzer`

**As of 2026-08-24**, `contract-reviewer` has been merged into
[`legal-document-analyzer`](../legal-document-analyzer/) per the
[migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c)
§07 finding: the two prompts served near-identical purposes
(contract/legal-document risk analysis producing a party-perspective
recommendation), and `legal-document-analyzer` was the stronger-designed of
the two (it already shipped a Disclaimer and "Questions for Specialized
Counsel" escalation pattern that `contract-reviewer` lacked).

**Nothing was dropped.** `contract-reviewer`'s negotiation-specific output —
must-haves / red-lines / nice-to-haves intake, dealbreaker analysis,
negotiation strategy, and the sign/negotiate/walk-away recommendation
checklist — is preserved in `legal-document-analyzer` as an optional
**Negotiation Mode** section, which activates automatically when you supply
`{{must_haves}}`, `{{red_lines}}`, or `{{nice_to_haves}}`. Both prompts'
full variable sets are preserved.

**Use [`legal-document-analyzer`](../legal-document-analyzer/) going
forward.** This folder is kept only so existing links/references don't
404, and carries no prompt content of its own.

See `legal-document-analyzer/MANIFEST.md` for the full merge changelog.
