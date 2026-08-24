# Shared Module: content-brief-intake

**Purpose**: Shared audience/tone/brand-voice/CTA intake block for marketing-content prompts, per [migration audit](https://claude.ai/code/artifact/ae8b9b2e-9e0f-4ddc-ab57-06f62ded444c) §07/§10.

**Applies to**: blog-post-generator, seo-content-optimizer, social-media-manager, email-newsletter, video-script-writer — genuinely different output shapes (net-new post vs. optimize-existing vs. repurpose-for-social vs. video), sharing one intake problem.

---

## Shared intake variables

```
{{audience}}        — who this content is for (role, interests, funnel stage)
{{tone}}             — voice/register (e.g. "professional but warm," "punchy and direct")
{{brand_voice_notes}} — any house-style constraints (banned words, required
                         disclaimers, existing brand guide reference)
{{cta}}              — the single action the content should drive
{{platform_context}} — where this runs (affects length/format norms — see
                         hallucination-guard note below)
```

## Intake block (drop into each prompt's Context section)

```
### Content Brief
- Audience: {{audience}}
- Tone: {{tone}}
- Brand voice notes: {{brand_voice_notes}}
- Call to action: {{cta}}
- Platform: {{platform_context}}
```

## Fabrication note (pair with `hallucination-guard`)

Per audit §04, several prompts in this cluster hard-code stale or invented
platform facts as if they were current specs (character limits, "best
posting time," performance predictions). Any platform-specific fact
(character limit, format requirement, algorithmic behavior) must be treated
as **`{{DOMAIN_FACT_TYPE}} = platform spec`** under `hallucination-guard`:
state it only if the user supplied it or it's common knowledge stable enough
not to have changed recently (e.g. "posts need a caption"), otherwise output
"Platform Spec Unconfirmed — verify current [platform] limits before
publishing." Never predict a performance metric (open rate, CTR, engagement)
as a number; if requested, label it "illustrative target, not a prediction"
and say so explicitly.

## What stays prompt-specific

- blog-post-generator: SEO structure, heading hierarchy
- seo-content-optimizer: keyword-density mechanics, existing-content diffing
- social-media-manager: per-platform format adaptation
- email-newsletter: subject-line variants, preview text
- video-script-writer: shot/scene structure, VO vs. on-screen text split
