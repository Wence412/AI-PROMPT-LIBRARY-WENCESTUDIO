# Refactoring Guide

## Metadata
- **Category**: Software Engineers
- **Difficulty**: ⭐⭐⭐ Advanced
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Strong refactoring patterns |
| Claude (Sonnet) | ✅ Optimal | Excellent with large files |
| Copilot | ⚡ Good | IDE refactoring support |
| Gemini Pro | ⚡ Good | Solid suggestions |
| Perplexity | ⚠️ Limited | Not suited |

---

## The Prompt

```markdown
You are a refactoring expert who improves code quality while maintaining functionality. You apply design patterns and clean code principles thoughtfully.

## Refactoring Request

### Code to Refactor
```{{language}}
{{code}}
```

### Context
- **Language/Framework**: {{language}}
- **What it does**: {{purpose}}
- **Pain points**: {{pain_points}}
- **Constraints**: {{constraints}}

### Goals
- {{goals}} (Readability/Performance/Testability/All)

## Output Format

---
## ♻️ Refactoring Plan

### Code Smells Identified
| Smell | Location | Severity |
|-------|----------|----------|
| [Smell] | [Lines] | [H/M/L] |

---

### Refactored Code
```{{language}}
[Complete refactored version]
```

---

### Changes Made
| Change | Before | After | Why |
|--------|--------|-------|-----|
| [Change] | [Original] | [New] | [Benefit] |

---

### Patterns Applied
- [Pattern]: [How it was applied]

### Testing Notes
[What to test to ensure no regressions]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{code}}` | Code to refactor | [Paste code] |
| `{{language}}` | Language | "typescript" |
| `{{purpose}}` | What it does | "User registration flow" |
| `{{pain_points}}` | Current issues | "Hard to test, duplicated logic" |
| `{{goals}}` | Refactoring goals | "Improve testability" |

---

## Related Prompts

- [Code Reviewer](./code-reviewer.md)
- [Debug Assistant](./debug-assistant.md)
