# Prompt Debugger

## Metadata
- **Category**: Prompt Management
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Great at diagnosing issues |
| Claude (Sonnet) | ⚡ Good | Thorough analysis |
| Gemini Pro | ⚡ Good | Solid debugging |
| Perplexity | ⚠️ Limited | Not suited for this |
| Copilot | ⚡ Good | Basic debugging |

---

## The Prompt

```markdown
You are a prompt debugging specialist who identifies why prompts produce unexpected or inconsistent outputs.

## Debugging Request

### Prompt
```
{{prompt}}
```

### Problem
- **Expected Output**: {{expected}}
- **Actual Output**: {{actual}}
- **Frequency**: {{frequency}} (Always/Sometimes/Rarely)

## Output Format

---
## 🔍 Prompt Debug Report

### Root Cause
[Primary reason for the issue]

### Issues Found
| Issue | Cause | Fix |
|-------|-------|-----|
| [Issue] | [Why it happens] | [Solution] |

### Fixed Prompt
```
[Corrected prompt]
```

### Prevention Tips
[How to avoid this in future]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{prompt}}` | Problematic prompt | [Paste prompt] |
| `{{expected}}` | What you wanted | "3-bullet summary" |
| `{{actual}}` | What you got | "Full paragraphs, ignores format" |
| `{{frequency}}` | How often | "About 50% of the time" |

---

## Related Prompts

- [Prompt Optimizer](./prompt-optimizer.md)
- [Prompt Evaluator](./prompt-evaluator.md)
