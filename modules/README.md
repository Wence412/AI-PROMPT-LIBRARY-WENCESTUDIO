# Shared Modules

Reference modules extracted from the [migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c) §10/§16, so recurring safety/quality clauses are defined once and referenced by every prompt that needs them, instead of being copy-pasted (and drifting) 55+ times.

| Module | Priority | Prompts affected |
|---|---|---|
| [hallucination-guard.md](./hallucination-guard.md) | High | ~55 of 70 |
| [crisis-safety-boundary.md](./crisis-safety-boundary.md) | High | cbt-companion, life-coach, mindfulness-guide, journaling-coach, emotional-intelligence, executive-coach |
| [coaching-session-scaffold.md](./coaching-session-scaffold.md) | Medium | career-coach, executive-coach, life-coach, habit-formation, interview-coach |
| [no-fabrication-security-contract.md](./no-fabrication-security-contract.md) | Medium | security-audit, threat-analyzer, vulnerability-assessment |
| [content-brief-intake.md](./content-brief-intake.md) | Low | blog-post-generator, seo-content-optimizer, social-media-manager, email-newsletter, video-script-writer |

These are **reference documents**, not standalone prompts — each rebuilt
prompt folder inlines the relevant clause(s) directly into its `v1-legacy.md`
and model-variant files (the pattern established in `cbt-companion`,
`legal-brief-drafter`, and `incident-response`), and cites which module it
draws from in its `MANIFEST.md` changelog. Keeping the canonical wording here
means a future fix to, say, the crisis-resource list only has to happen in
one place and then be re-propagated, rather than being re-derived per prompt.
