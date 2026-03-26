# 📄 PROMPT\_TEMPLATE.md (Reasoning-Aware)

````markdown

# [Prompt Name]

## 📋 Metadata
- **Category**: [Category Name]
- **Difficulty**: ⭐ / ⭐⭐ / ⭐⭐⭐ (Basic / Intermediate / Agentic)
- **Last Updated**: 2026-02-26
- **Version**: 2.0 (Reasoning-Optimized)

---

## ⚙️ Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| **ChatGPT (GPT-5.4)** | ✅ / ⚡ / ⚠️ | Set 'Thinking Effort' to [Standard/Extended] |
| **Claude (4.6 Opus)** | ✅ / ⚡ / ⚠️ | Best for XML-tagged complex logic |
| **Gemini (3.1 Pro)** | ✅ / ⚡ / ⚠️  | Use for 1M+ token context or live grounding |
| **Perplexity Pulse** | ✅ / ⚡ / ⚠️  | Use for real-time citations & search |

---

## 🧠 Cognitive Framework (The Prompt)

```markdown
# [THINKING_CONFIG]
- Effort: [Low | High]
- Strategy: [Chain-of-Thought | First-Principles | Tree-of-Thought]
- Tool_Access: [Enabled | Disabled]

<role>
Act as a [Expert Persona]. Your objective is [Objective].
</role>

<context>
Background: {{context_variable}}
Constraints: [Constraint 1, Constraint 2]
Primary Data: {{data_input}}
</context>

<logic_chain>
Before providing the final output, perform the following internal reasoning steps:
1. Analyze {{data_input}} for [X].
2. Identify potential [Risks/Contradictions].
3. Formulate a strategy based on [Industry Standard].
4. Self-Correct: Review your initial thought for bias or inefficiency.
</logic_chain>

<output_format>
- Structure: [Markdown Table / JSON / Executive Summary]
- Tone: [Professional / Creative / Technical]
- Mandatory Elements: [Element 1, Element 2]
</output_format>

<instruction_override>
If [Condition], then [Alternative Action]. Do not hallucinate data; if unknown, state "Data Unavailable."
</instruction_override>
````

-----

## 🛠️ Variables & Inputs

| Variable | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `{{context_variable}}` | String | Industry or specific background | "SaaS Fintech" |
| `{{data_input}}` | Text/File | The raw data for the AI to process | "Q4 Revenue Report" |

-----

## 🧪 Reasoning Audit (Techniques Used)

  - [x] **Internal Monologue:** Forced reasoning via `<logic_chain>` tags.
  - [x] **XML Semantic Isolation:** Prevents instruction drift in 1M+ token windows.
  - [x] **Agentic Hooks:** Includes "Instruction Overrides" for autonomous decision-making.
  - [ ] **Few-Shot Learning:** (Check if examples are included in the prompt above).
  - [ ] **Multimodal Grounding:** (Check if image/video inputs are required).

-----

## 💡 Pro Tips

1.  **Thinking Depth:** For GPT-5, always explicitly state if you want "Extended Thinking" to avoid wasting tokens on simple tasks.
2.  **Claude Artifacts:** If this prompt generates code or UI, instruct Claude to "Render in a Preview Artifact."
3.  **Gemini Grounding:** For Gemini, always include a URL or file reference to utilize its massive 2026 context window.

-----

## 🔗 Related Frameworks

  - [Related Prompt 1](https://www.google.com/search?q=./related-prompt-1.md)
  - [Master Catalog](https://www.google.com/search?q=../CATALOG.md)

<!-- end list -->

```
**Would you like me to take one of your existing prompts from the library and "migrate" it into this new template to show you the difference?**
```
