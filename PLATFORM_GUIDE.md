# 🌐 AI Platform Guide — 2026 Edition

> **The definitive matrix for selecting the optimal Reasoning Engine for your prompt library workflows.**
> Aligned with [PROMPT_TEMPLATE.md](./PROMPT_TEMPLATE.md) engine architectures and [UPGRADE_LOG.md](./UPGRADE_LOG.md) standards.

---

## 📊 2026 Platform Comparison Matrix

| Feature | ChatGPT (GPT-5.2) | Claude (Sonnet 4.6) | Gemini (3.1 Pro) | Perplexity | Copilot (365+) |
|---------|-------------------|--------------------|--------------------|------------|----------------|
| **Context Window** | 512K – 1M | 1M+ | **2M+** | 256K | 512K |
| **Reasoning Depth** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ |
| **Creative Nuance** | ⭐⭐⭐⭐ | **⭐⭐⭐⭐⭐** | ⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ |
| **Live Grounding** | ⭐⭐⭐⭐ | ⭐⭐⭐ | **⭐⭐⭐⭐⭐** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| **Tool Augmentation** | **⭐⭐⭐⭐⭐** | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **Code Generation** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐⭐ |
| **Speed (Tokens/s)** | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ |

---

## 🤖 Detailed Platform Profiles

### ChatGPT (GPT-5.2 / GPT-OSS 120B)

**Library Prompt Format**: `[THINKING CONFIG]` + `[TOOL AUGMENTATION]` — see [gpt-oss-120b.md](./PROMPT_TEMPLATE.md#template-c-gpt-52--gpt-oss-120b-thinking-config-architecture)

| Attribute | Detail |
|-----------|--------|
| Best Models | `gpt-5.2-thinking-extended` (Deep Research), `gpt-oss-120b` (Open-weight) |
| Thinking Control | `Thinking Effort: LOW / MEDIUM / HIGH` + `Self-Critique: Enabled` |
| Tool Access | Live Search, Code Interpreter, Google Drive, Image Generation |
| Agent Mode | `STANDALONE / ORCHESTRATOR / WORKER` |

**Strengths**:
- **Thinking Effort Control** — First engine to allow manual toggling of reasoning depth per-prompt
- **Tool Augmentation** — Richest tool ecosystem (search, code, files, images) in a single prompt
- **Self-Critique Loops** — Built-in adversarial validation before final output
- **GPT-OSS 120B** — Open-weight variant for self-hosted/privacy-first deployments

**Optimal Use Cases**: Complex engineering, agentic automation, data analysis with code interpreter, multi-tool workflows

**Prompt Syntax** (from library):
```
[THINKING CONFIG] Thinking Effort: HIGH | Self-Critique: Enabled
[AGENT MODE: STANDALONE]
[CONTEXT] ...
[TASK] ...
[TOOL AUGMENTATION] Live Search: YES | Code Interpreter: YES
[OUTPUT FORMAT] ...
```

---

### Claude (Sonnet 4.6)

**Library Prompt Format**: XML structural isolation — see [claude-4-6.md](./PROMPT_TEMPLATE.md#template-a-claude-sonnet-46-xml-architecture)

| Attribute | Detail |
|-----------|--------|
| Best Models | `claude-4.6-opus` (Maximum nuance), `claude-4.6-sonnet` (Daily workhorse) |
| Thinking Control | `<thinking_config mode="extended">` with `depth` and `reasoning_style` |
| Structural Isolation | XML tags: `<instructions>`, `<context>`, `<task>`, `<output_format>` |
| Self-Review | `adversarial self-review` in `<reasoning_style>` |

**Strengths**:
- **XML Structural Isolation** — Prevents instruction drift in long-context prompts; cleanest separation of concerns
- **Extended Thinking** — Configurable depth (`standard` / `thorough`) with mandatory chain-of-thought
- **Constitutional Alignment** — Most "human-aligned" and least prone to sycophancy
- **Adaptive Context** — Best-in-class performance at 1M tokens without "forgetting"

**Optimal Use Cases**: Legal analysis, creative writing, nuanced coaching, long-document synthesis, sensitive topics

**Prompt Syntax** (from library):
```xml
<instructions>You are a [Expert Persona]. Activate Extended Thinking.</instructions>
<thinking_config mode="extended">
  <depth>thorough</depth>
  <reasoning_style>first-principles + adversarial self-review</reasoning_style>
  <chain_of_thought>mandatory</chain_of_thought>
</thinking_config>
<context>...</context>
<task>...<constraints>...</constraints></task>
<output_format>...<confidence>0–100</confidence></output_format>
```

---

### Gemini (3.1 Pro)

**Library Prompt Format**: `[GROUNDING CONFIG]` + `[REASONING CHAIN]` — see [gemini-3-1-pro.md](./PROMPT_TEMPLATE.md#template-b-gemini-31-pro-grounding-architecture)

| Attribute | Detail |
|-----------|--------|
| Best Models | `gemini-3.1-pro` (Large context + grounding), `gemini-3.1-flash` (High volume) |
| Thinking Control | `Thinking Mode: Extended Reasoning — ON` |
| Grounding | `Grounding Source: Google Search / Google Scholar / None` |
| Context Window | Up to **2M tokens** — largest production context available |

**Strengths**:
- **2M Token Context** — Ingest entire codebases, video transcripts, or document libraries in one prompt
- **Google Live Grounding** — Direct, real-time access to Google Search, Scholar, Maps, and Workspace
- **Reasoning Chains** — Explicit multi-step reasoning with numbered steps
- **Native Video Intelligence** — Best at analyzing long video content and finding specific moments

**Optimal Use Cases**: Multimodal research, massive data extraction, academic research, Google ecosystem integration

**Prompt Syntax** (from library):
```
[GEMINI 3.1 PRO — GROUNDING CONFIG]
Context Window: STANDARD | Grounding Source: Google Search
Thinking Mode: Extended Reasoning — ON
[ROLE] ...
[CONTEXT] ...
[TASK] ...
[REASONING CHAIN] Step 1: ... | Step 2: ... | Step 3: ...
[OUTPUT STRUCTURE] ...
```

---

### Perplexity

| Attribute | Detail |
|-----------|--------|
| Best For | Real-time citations, live web search, competitive research |
| Limitation | Not suited for structured prompt workflows, creative writing, or code generation |

**When to use**: Fact-checking claims, current events research, finding sources for prompts that need live data. Pair with another engine for the actual analysis.

---

### Copilot (Microsoft 365+)

| Attribute | Detail |
|-----------|--------|
| Best For | Enterprise workflows, Microsoft 365 integration, document automation |
| Limitation | Less flexible for custom prompt architectures |

**When to use**: When your workflow lives inside Microsoft 365 (Word, Excel, PowerPoint, Outlook, Teams). Best for enterprise operations and document-bound tasks.

---

## 🎯 Platform Selection by Prompt Category

This table maps each prompt library category to its recommended primary engine:

| Category | Primary Engine | Secondary | Why Primary? |
|----------|---------------|-----------|--------------|
| **Analyze Text** | Claude 4.6 | GPT-5.2 | Nuanced comprehension, long-doc handling |
| **Coaching** | Claude 4.6 | GPT-5.2 | Most human-aligned, empathetic tone |
| **Code & DevOps** | GPT-5.2 | Claude 4.6 | Code interpreter + tool augmentation |
| **Content Creation** | Claude 4.6 | GPT-5.2 | Best creative prose and narrative flow |
| **Cybersecurity** | GPT-5.2 | Gemini 3.1 Pro | Deep reasoning + live CVE search |
| **Data Science** | Gemini 3.1 Pro | GPT-5.2 | 2M context for whole-dataset analysis |
| **Entrepreneurs** | Claude 4.6 | GPT-5.2 | Nuanced strategic reasoning |
| **Gaming** | GPT-5.2 | Gemini 3.1 Pro | Search for current meta |
| **Job Search** | Claude 4.6 | GPT-5.2 | ATS-aware, human-sounding prose |
| **Product Management** | Claude 4.6 | GPT-5.2 | Structured output, stakeholder nuance |
| **Real Estate** | Gemini 3.1 Pro | Claude 4.6 | Live grounding for market data |
| **Research** | Gemini 3.1 Pro | Perplexity | Scholar grounding + 2M context |
| **Students & School** | GPT-5.2 | Claude 4.6 | Socratic tutoring + code interpreter |

---

## 🔧 Cross-Engine Prompt Syntax Reference

Every prompt in this library uses engine-specific syntax. Here's the quick-reference mapping:

| Concept | Claude 4.6 | Gemini 3.1 Pro | GPT-5.2 |
|---------|-----------|---------------|---------|
| **Role** | `<instructions>` | `[ROLE]` | Inline in `[TASK]` |
| **Context** | `<context>` | `[CONTEXT]` | `[CONTEXT]` |
| **Task** | `<task>` | `[TASK]` | `[TASK]` |
| **Constraints** | `<constraints>` | Inline | Inline |
| **Thinking** | `<thinking_config>` | `Thinking Mode: Extended` | `[THINKING CONFIG]` |
| **Output** | `<output_format>` | `[OUTPUT STRUCTURE]` | `[OUTPUT FORMAT]` |
| **Tools** | N/A | `Grounding Source:` | `[TOOL AUGMENTATION]` |
| **Confidence** | `<confidence>` | `### Confidence` | `**Confidence & Caveats**` |

---

## 📂 How This Connects to the Library

```
AI-PROMPT-LIBRARY-WENCESTUDIO/
├── PLATFORM_GUIDE.md      ← You are here
├── PROMPT_TEMPLATE.md      ← Engine-specific templates
├── CATALOG.md              ← Full prompt index
├── UPGRADE_LOG.md          ← Modernization history
├── prompt-name/            ← Each prompt subfolder
│   ├── v1-legacy.md
│   ├── claude-4-6.md
│   ├── gemini-3-1-pro.md
│   ├── gpt-oss-120b.md
│   └── MANIFEST.md
└── prompt-*.md             ← 4 meta-prompts (debugger, evaluator, optimizer, versioner)
```

---

**Last Updated**: 2026-03-27
