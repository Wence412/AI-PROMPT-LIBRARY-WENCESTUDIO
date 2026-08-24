# PROMPT UPDATE MANIFEST
Library Entry: habit-formation.md | Category: Coaching | Updated: 2026-03-26
Variables: {{CLIENT_NAME}}, {{HABIT_GOAL}}, {{WHY_IMPORTANT}}, {{PAST_ATTEMPTS}}, {{CURRENT_SCHEDULE}}, {{OBSTACLES}}
| Engine | File | Tools |
|---|---|---|
| Claude Sonnet 4.6 | claude-4-6.md | none |
| Gemini 3.1 Pro | gemini-3-1-pro.md | none |
| GPT-OSS 120B | gpt-oss-120b.md | none |

## Change Log

### v1.1 — 2026-08-24
- **[FIX]** Stripped batch-generated boilerplate from all three engine adapters: the forced-visible `<chain_of_thought>mandatory</chain_of_thought>` / mandatory `<thinking>` output block, the fake `<confidence>0–100</confidence>` / "Confidence" footer, and the dead `<agentic_hooks>` scaffold (where present).
- **[FIX]** Added an explicit missing-data fallback to all four variants (v1-legacy, claude-4-6, gemini-3-1-pro, gpt-oss-120b): if the client context is empty, a placeholder, or too thin to design a real plan, the prompt now says so and asks for the missing piece instead of inventing a client history or goal.
- Source: Migration Audit §08. No change to the prompt's core coaching logic or variables.
