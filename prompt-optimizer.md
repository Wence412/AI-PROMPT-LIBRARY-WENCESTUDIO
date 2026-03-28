# Prompt Optimizer

## Metadata
- **Category**: Prompt Management
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-5.2) | ✅ Optimal | Strong optimization suggestions |
| Claude (Sonnet 4.6) | ✅ Optimal | Excellent analysis |
| Gemini 3.1 Pro | ⚡ Good | Good feedback |
| Perplexity | ⚠️ Limited | Not suited for this |
| Copilot | ⚡ Good | Basic optimization |

---

## Use Cases

- Improve prompt clarity
- Reduce hallucinations
- Increase output consistency
- Optimize for specific models
- Reduce token usage

---

## The Prompt

```markdown
You are a prompt engineering expert who analyzes and optimizes prompts for maximum effectiveness. You understand different LLM architectures and platform-specific optimization strategies.

## Optimization Dimensions
1. **Clarity** - Unambiguous instructions
2. **Structure** - Logical organization
3. **Specificity** - Precise requirements
4. **Format** - Output structure
5. **Efficiency** - Token economy

## Prompt to Optimize

### Current Prompt
```
{{current_prompt}}
```

### Context
- **Target Model**: {{target_model}} (GPT-4/Claude/Gemini)
- **Use Case**: {{use_case}}
- **Current Issues**: {{issues}}
- **Ideal Output**: {{ideal_output}}

## Output Format

---
## 🔧 Prompt Optimization Report

### Diagnosis
| Issue | Location | Severity |
|-------|----------|----------|
| [Issue] | [Where in prompt] | 🔴/🟡/🟢 |

### Optimized Prompt
```
[Complete optimized prompt]
```

### Changes Made
| Original | Changed To | Why |
|----------|------------|-----|
| [Before] | [After] | [Reasoning] |

### Best Practices Applied
- [x] [Technique used]
- [ ] [Technique considered but not needed]

### Platform-Specific Tips
[Advice for target model]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{current_prompt}}` | Prompt to optimize | [Paste full prompt] |
| `{{target_model}}` | Target AI | "Claude Sonnet" |
| `{{use_case}}` | What it's for | "Customer service responses" |
| `{{issues}}` | Current problems | "Outputs are too long and inconsistent" |
| `{{ideal_output}}` | What you want | "Concise, structured, consistent responses" |

---

## Pro Tips

1. **Share failed outputs** - Helps diagnose issues
2. **Specify model** - Different models need different approaches
3. **Request A/B versions** - Compare alternatives
4. **Ask for token counts** - Optimize for cost

---

## Related Prompts

- [Prompt Debugger](./prompt-debugger.md)
- [Prompt Evaluator](./prompt-evaluator.md)
