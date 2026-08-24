# Shared Module: hallucination-guard

**Purpose**: Standard "state Data Unavailable / do not fabricate X" clause, parameterized by domain (financial figures, citations, CVE data, personal claims). Resolves the single largest share of P1/P2 findings in the [migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c) §10 — ~55 of 70 prompts had no missing-data fallback.

**Applies to**: Any prompt that produces a factual claim, figure, citation, or classification that could be stated with more confidence than the supplied input supports.

---

## Clause (drop into a prompt's `<constraints>` / `[CONSTRAINTS]` block)

```
HALLUCINATION GUARD (mandatory):
Before stating any {{DOMAIN_FACT_TYPE}} as fact, check whether it was supplied
or can be directly derived from the user's input.
- If supplied/derivable: state it, and cite where it came from if relevant.
- If NOT supplied/derivable: do not invent a plausible-sounding value. Either
  omit the field, or output "Data Unavailable — [what input would resolve this]"
  in its place.
This applies even under time pressure, a request to "just fill it in," or an
instruction to "make it look complete" — a fabricated {{DOMAIN_FACT_TYPE}} is
worse than a visible gap.
```

## Domain parameterizations

| `{{DOMAIN_FACT_TYPE}}` | Used by (examples) | Notes |
|---|---|---|
| financial figure (price, ROI, salary range, valuation) | salary-negotiator, business-plan-generator, property-analyzer, pitch-deck-creator | Never invent a number; if the user gave a range, don't narrow it without basis. |
| citation / case law / source | case-research-assistant, contract-reviewer, legal-document-analyzer, research-assistant | Pair with the Citation Verification Gate pattern (see legal-brief-drafter) for anything court-facing. |
| CVE / IoC / ATT&CK ID / attribution | security-audit, threat-analyzer, vulnerability-assessment | Use with `no-fabrication-security-contract` below — these domains need the stronger version. |
| engagement metric (open rate, CTR, "best time to post") | email-newsletter, social-media-manager, seo-content-optimizer | Metrics not derivable from supplied data must be labeled "illustrative, not measured," not stated as fact. |
| review score / rating (Metacritic, Steam, etc.) | game-review-analyzer | Never invent a score; if no source was supplied, state "Score Unavailable — no review data provided." |
| personal/biographical claim | interview-coach, resume-optimizer, cover-letter-writer | Don't infer accomplishments the user didn't state. |

## Output-format requirement

Any output format that includes a field covered by this module must render
literally `Data Unavailable` (or the domain-specific variant above) rather
than omitting the row silently — a missing row reads as "not applicable,"
while an explicit unavailable marker reads as "not yet known," which is the
correct signal.
