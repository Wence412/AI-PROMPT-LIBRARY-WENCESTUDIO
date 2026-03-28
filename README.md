# 🚀 AI-PROMPT-LIBRARY-WENCESTUDIO | 2026 Edition

> **A professional-grade collection of 70 Reasoning-Aware prompts, each with engine-specific variants for Claude Sonnet 4.6, Gemini 3.1 Pro, and GPT-OSS 120B.** Built on 2026 extended thinking protocols, XML structural isolation, and grounded reasoning chains.

---

## 🧠 Why This Library is Different

Every prompt in this library ships as **3 engine-optimized variants** + a deployment manifest:

| File | Engine | Architecture |
|------|--------|-------------|
| `claude-4-6.md` | Claude Sonnet 4.6 | XML structural isolation (`<instructions>`, `<thinking_config>`, `<task>`) |
| `gemini-3-1-pro.md` | Gemini 3.1 Pro | `[GROUNDING CONFIG]` + `[REASONING CHAIN]` with Google Search/Scholar |
| `gpt-oss-120b.md` | GPT-OSS 120B | `[THINKING CONFIG]` + `[TOOL AUGMENTATION]` with self-critique |
| `MANIFEST.md` | — | Variables, engine map, tool requirements |
| `v1-legacy.md` | — | Original prompt preserved for reference |

---

## 📚 Prompt Categories & Engine Recommendations

| Category | Prompts | Primary Engine | Why? |
|----------|---------|---------------|------|
| **Analyze Text** | sentiment-analyzer, document-summarizer, key-insights-extractor | Claude 4.6 | Nuanced comprehension |
| **Coaching** | career-coach, executive-coach, fitness-coach, life-coach, interview-coach, journaling-coach, mindfulness-guide, habit-formation | Claude 4.6 | Human-aligned tone |
| **Code & DevOps** | code-reviewer, debug-assistant, devops-pipeline, github-actions, api-documentation, refactoring-guide | GPT-5.2 | Code interpreter + tools |
| **Content Creation** | blog-post-generator, email-newsletter, email-writer, content-repurposer, seo-content-optimizer, social-media-manager, video-script-writer, linkedin-optimizer | Claude 4.6 | Best prose quality |
| **Creative Arts** | creative-brainstormer, story-writer, poetry-composer, narrative-designer | Claude 4.6 | Literary nuance |
| **Cybersecurity** | security-audit, threat-analyzer, vulnerability-assessment, incident-response | GPT-5.2 | Deep reasoning + CVE search |
| **Data & Visualization** | data-analyst, dashboard-designer, graph-generator, infographic-planner | Gemini 3.1 Pro | 2M context for datasets |
| **Entrepreneurs** | startup-advisor, business-plan-generator, pitch-deck-creator, growth-hacker | Claude 4.6 | Strategic nuance |
| **Gaming** | game-design-consultant, strategy-guide-creator | GPT-5.2 | Search for current meta |
| **Job Search** | resume-optimizer, cover-letter-writer, salary-negotiator | Claude 4.6 | ATS-aware, human tone |
| **Legal** | legal-document-analyzer, legal-brief-drafter, business-contract-generator | Claude 4.6 | Constitutional alignment |
| **Product Management** | prd-generator, feature-prioritizer, roadmap-planner, user-story-writer, stakeholder-communicator | Claude 4.6 | Structured output |
| **Real Estate** | property-analyzer, listing-writer | Gemini 3.1 Pro | Live market grounding |
| **Research** | research-assistant, market-research, market-researcher, competitor-analyzer | Gemini 3.1 Pro | Scholar + 2M context |
| **Students** | tutor, study-guide-creator, concept-explainer, debate-partner, essay-improver | GPT-5.2 | Socratic tutoring |
| **Writing & Docs** | brand-voice-analyzer, grant-writer, financial-advisor, image-prompt-generator, meeting-summarizer | Claude 4.6 | Tone sensitivity |

> See **[CATALOG.md](./CATALOG.md)** for the full index.

---

## 🎯 2026 Reasoning Techniques

| Technique | Claude 4.6 | Gemini 3.1 Pro | GPT-5.2 |
|-----------|-----------|---------------|---------|
| **Extended Thinking** | `<thinking_config mode="extended">` | `Thinking Mode: Extended Reasoning — ON` | `Thinking Effort: HIGH` |
| **Self-Critique** | `adversarial self-review` | Step N in `[REASONING CHAIN]` | `Self-Critique: Enabled` |
| **Structural Isolation** | XML tags (`<task>`, `<context>`) | Section headers (`[TASK]`) | Section headers (`[TASK]`) |
| **Live Grounding** | N/A | `Grounding Source: Google Search` | `Live Search: YES` |
| **Tool Access** | N/A | N/A | `[TOOL AUGMENTATION]` block |
| **Confidence Score** | `<confidence>0–100</confidence>` | `### Confidence` | `**Confidence & Caveats**` |
| **Hallucination Guard** | `<constraints>` block | Inline in `[TASK]` | Inline in `[TASK]` |

---

## 💻 Platform Quick Reference

| Platform | Best For | Key 2026 Feature |
|----------|---------|-----------------|
| **ChatGPT (GPT-5.2)** | Logic, coding, multi-tool agents | Thinking Effort control + Tool Augmentation |
| **Claude (Sonnet 4.6)** | Legal, creative, long docs | Extended Thinking + XML isolation |
| **Gemini (3.1 Pro)** | Massive context, research | 2M token window + Google grounding |
| **Perplexity** | Market research, fact-checking | Real-time citations |

> Full comparison in **[PLATFORM_GUIDE.md](./PLATFORM_GUIDE.md)**

---

## 📖 How to Use

1. **Pick a prompt** → Browse [CATALOG.md](./CATALOG.md) or find the subfolder by name
2. **Choose your engine** → Open `claude-4-6.md`, `gemini-3-1-pro.md`, or `gpt-oss-120b.md`
3. **Fill variables** → Replace `{{VARIABLE_NAME}}` placeholders with your data
4. **Paste & run** → Copy into your AI engine of choice
5. **Iterate** → Use the built-in confidence scores and constraints to refine output

---

## 📁 Repository Structure

```
AI-PROMPT-LIBRARY-WENCESTUDIO/
├── README.md               ← You are here
├── CATALOG.md              ← Full prompt index
├── PLATFORM_GUIDE.md       ← Engine comparison & selection guide
├── PROMPT_TEMPLATE.md      ← Engine-specific template reference
├── UPGRADE_LOG.md          ← Modernization history (70 prompts × 3 engines)
│
├── prompt-name/            ← 70 prompt subfolders, each containing:
│   ├── v1-legacy.md            Original prompt
│   ├── claude-4-6.md           Claude Sonnet 4.6 variant
│   ├── gemini-3-1-pro.md       Gemini 3.1 Pro variant
│   ├── gpt-oss-120b.md         GPT-OSS 120B variant
│   └── MANIFEST.md             Variables & engine map
│
├── prompt-debugger.md      ← Meta-prompt: diagnose prompt failures
├── prompt-evaluator.md     ← Meta-prompt: score prompt quality
├── prompt-optimizer.md     ← Meta-prompt: improve prompts
└── prompt-versioner.md     ← Meta-prompt: version control prompts
```

---

## 📜 License & Attribution

**Copyright 2026 WenceStudio by SmartDesign**
Licensed under the [Apache License 2.0](./LICENSE). See [NOTICE](./NOTICE) for attribution requirements.

---

**Last Updated**: 2026-03-27 · **Prompts**: 70 · **Engine Variants**: 210 · **Total Files**: 350+
