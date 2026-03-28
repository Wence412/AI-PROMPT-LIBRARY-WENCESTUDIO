# 📄 PROMPT_TEMPLATE.md (2026 Reasoning-Aware)

> **This is the canonical template for all prompts in AI-PROMPT-LIBRARY-WENCESTUDIO.**
> Every upgraded prompt folder contains engine-specific variants derived from this architecture.

---

## 📋 Metadata
- **Category**: [Category Name]
- **Difficulty**: ⭐ / ⭐⭐ / ⭐⭐⭐ (Basic / Intermediate / Agentic)
- **Last Updated**: 2026-03-27
- **Version**: 3.0 (Multi-Engine Reasoning-Aware)

---

## ⚙️ Platform Compatibility

| Platform | Rating | Reasoning Features | Best For |
|----------|--------|-------------------|----------|
| **ChatGPT (GPT-5.2)** | ✅ / ⚡ / ⚠️ | `[THINKING CONFIG]` with effort levels (Low/Medium/High), self-critique loops, `[TOOL AUGMENTATION]` for search/code/Drive | Complex analysis, tool-augmented workflows, code generation |
| **Claude (Sonnet 4.6)** | ✅ / ⚡ / ⚠️ | `<thinking_config>` with extended mode, XML structural isolation (`<instructions>`, `<context>`, `<task>`), adversarial self-review | Nuanced reasoning, structured output, sensitive topics |
| **Gemini (3.1 Pro)** | ✅ / ⚡ / ⚠️ | `[GROUNDING CONFIG]` with Google Search/Scholar, `[REASONING CHAIN]` with explicit steps, 2M token context window | Large document analysis, research, multi-file processing |
| **Perplexity** | ✅ / ⚡ / ⚠️ | Real-time citations, live web search, source attribution | Fact-checking, current events, competitive research |

---

## 🧠 Engine-Specific Templates

### Template A: Claude Sonnet 4.6 (XML Architecture)

```markdown
<instructions>
You are a [Expert Persona]. [Core directive]. Activate Extended Thinking.
</instructions>

<thinking_config mode="extended">
  <depth>[standard | thorough]</depth>
  <reasoning_style>[first-principles | adversarial self-review | chain-of-thought]</reasoning_style>
  <chain_of_thought>mandatory</chain_of_thought>
</thinking_config>

<context>
{{CONTEXT_OR_PASTE_NONE}}
[Variable 1]: {{VAR_1}} | [Variable 2]: {{VAR_2}} | [Variable 3]: {{VAR_3}}
</context>

<task>
[Detailed task description with step-by-step deliverables.]
  <constraints>
    - [Constraint 1]
    - [Constraint 2]
    - Avoid hallucinations; state "Data Unavailable" if unknown.
  </constraints>
</task>

<output_format>
  <thinking>[Internal reasoning steps before answering]</thinking>
  <response>[Output structure: sections, tables, format]</response>
  <confidence>0–100</confidence>
</output_format>
```

---

### Template B: Gemini 3.1 Pro (Grounding Architecture)

```markdown
[GEMINI 3.1 PRO — GROUNDING CONFIG]
Context Window: {{STANDARD | MAXIMUM (2M tokens)}}
Grounding Source: {{Google Search | Google Scholar | None}}
Thinking Mode: Extended Reasoning — ON

[ROLE]
[Expert Persona]. [Core directive]. Activate Extended Reasoning.

[CONTEXT]
[Variable 1]: {{VAR_1}} | [Variable 2]: {{VAR_2}} | [Variable 3]: {{VAR_3}}
Additional: {{CONTEXT_OR_NONE}}

[TASK]
[Detailed task description with deliverables.]

[REASONING CHAIN]
Step 1: [Analysis step]
Step 2: [Evaluation step]
Step 3: [Synthesis step]
Step 4: [Self-critique step]

[OUTPUT STRUCTURE]
### Section 1 | ### Section 2 | ### Section 3 | ### Confidence
```

---

### Template C: GPT-5.2 / GPT-OSS 120B (Thinking-Config Architecture)

```markdown
[THINKING CONFIG]
Thinking Effort: {{LOW | MEDIUM | HIGH}}
Self-Critique: {{Enabled | Disabled}}

[AGENT MODE: {{STANDALONE | ORCHESTRATOR | WORKER}}]

[CONTEXT]
[Variable 1]: {{VAR_1}} | [Variable 2]: {{VAR_2}} | [Variable 3]: {{VAR_3}}
Additional: {{CONTEXT_OR_NONE}}

[TASK]
[Expert Persona]. [Detailed task description with deliverables.]

[TOOL AUGMENTATION]
Live Search: {{YES / NO}}
Code Interpreter: {{YES / NO}}
Google Drive: {{YES / NO}}
Image Generation: {{YES / NO}}

[OUTPUT FORMAT]
**Section 1** | **Section 2** | **Section 3** | **Confidence & Caveats**
```

---

## 🛠️ Variables & Inputs

| Variable | Type | Description | Example |
|----------|------|-------------|---------|
| `{{CONTEXT_OR_PASTE_NONE}}` | String | Background context or "none" | "SaaS Fintech startup, Series B" |
| `{{VAR_1}}` ... `{{VAR_N}}` | String/Text | Domain-specific inputs | "Q4 Revenue Report" |

> **Naming Convention**: `{{UPPER_SNAKE_CASE}}` for all variables across all engines.

---

## 🧪 Reasoning Audit Checklist

Use this checklist when creating or reviewing a prompt:

| Technique | Claude 4.6 | Gemini 3.1 Pro | GPT-5.2 | Status |
|-----------|-----------|---------------|---------|--------|
| **Extended Thinking** | `<thinking_config mode="extended">` | `Thinking Mode: Extended Reasoning — ON` | `Thinking Effort: HIGH` | [ ] |
| **Structural Isolation** | XML tags (`<task>`, `<context>`) | Section headers (`[TASK]`, `[CONTEXT]`) | Section headers (`[TASK]`, `[CONTEXT]`) | [ ] |
| **Self-Critique** | `adversarial self-review` in reasoning_style | Step N in `[REASONING CHAIN]` | `Self-Critique: Enabled` | [ ] |
| **Grounding/Search** | N/A (no native search) | `Grounding Source: Google Search` | `Live Search: YES` | [ ] |
| **Tool Access** | N/A | N/A | `[TOOL AUGMENTATION]` block | [ ] |
| **Confidence Score** | `<confidence>0–100</confidence>` | `### Confidence` section | `**Confidence & Caveats**` | [ ] |
| **Hallucination Guard** | `<constraints>` block | Inline in `[TASK]` | Inline in `[TASK]` | [ ] |

---

## 📁 Folder Structure

Each upgraded prompt produces a subfolder:

```
prompt-name/
├── v1-legacy.md          # Original prompt preserved
├── claude-4-6.md         # Template A variant
├── gemini-3-1-pro.md     # Template B variant
├── gpt-oss-120b.md       # Template C variant
└── MANIFEST.md           # Variables, engine map, tool requirements
```

---

## 💡 Pro Tips

1. **Thinking Effort (GPT-5.2)**: Explicitly set `HIGH` only for complex multi-step tasks. Use `MEDIUM` for standard work to save tokens.
2. **Extended Thinking (Claude 4.6)**: Set `<depth>thorough</depth>` for first-principles analysis; use `standard` for routine tasks.
3. **Context Window (Gemini 3.1 Pro)**: Declare `MAXIMUM (2M tokens)` only when processing large codebases or document sets. Default to `STANDARD`.
4. **Grounding (Gemini)**: Always include `Grounding Source: Google Search` for prompts that need current data. Use `Google Scholar` for academic prompts.
5. **Tool Augmentation (GPT-5.2)**: Enable `Code Interpreter: YES` for any prompt that involves data analysis, calculations, or code generation.
6. **Cross-Engine Parity**: When creating a new prompt, write the Claude XML version first (most structured), then adapt to Gemini and GPT formats.
7. **Hallucination Guards**: Every prompt must include a constraint like "Avoid hallucinations; state 'Data Unavailable' if unknown."

---

## 🔗 Related

- [CATALOG.md](./CATALOG.md) — Full prompt index
- [Prompt Optimizer](./prompt-optimizer.md) — Improve existing prompts
- [Prompt Evaluator](./prompt-evaluator.md) — Score prompt quality
- [Prompt Debugger](./prompt-debugger.md) — Diagnose prompt failures
- [Prompt Versioner](./prompt-versioner.md) — Track prompt changes
- [UPGRADE_LOG.md](./UPGRADE_LOG.md) — Modernization history
