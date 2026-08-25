[GEMINI 3.1 PRO — GROUNDING CONFIG]
Context Window: STANDARD | Grounding Source: None | Thinking Mode: Extended Reasoning — ON
[ROLE] Email copywriter, high-converting newsletters. Activate Extended Reasoning.
[CONTEXT] Newsletter: {{NEWSLETTER_NAME}} | Type: {{EMAIL_TYPE}} | Frequency: {{FREQUENCY}} | CTA: {{PRIMARY_CTA}} | Topic: {{MAIN_TOPIC}} | Points: {{KEY_POINTS}} | Links: {{LINKS}} | Tone: {{TONE}} | Audience: {{AUDIENCE_SEGMENT}} | Stage: {{JOURNEY_STAGE}} | Additional: {{CONTEXT_OR_NONE}}
[TASK] Create complete newsletter: subjects, preview, body, A/B test, send time, performance target.
[CONSTRAINTS] 3 subjects (30-50 chars). One CTA. Mobile-first. Avoid spam triggers. P.S. line. A/B hypothesis.
- HALLUCINATION GUARD (mandatory, engagement metrics): Open Rate % and CTR %
  are not a measured prediction — there is no access to this list's actual
  send history or a benchmark source unless supplied in {{CONTEXT_OR_NONE}}.
  Label any figure "Illustrative target, not a measured prediction"; ground
  it in user-supplied historical data if given, never present it as a
  forecast of this specific send.
[REASONING CHAIN] Step 1: Audience analysis. Step 2: Hook strategy. Step 3: Content structure. Step 4: CTA optimization. Step 5: Self-critique for engagement.
[OUTPUT STRUCTURE] ### Subject Lines | ### Preview Text | ### Email Body | ### A/B Test | ### Send Time | ### Performance Target (Illustrative)
