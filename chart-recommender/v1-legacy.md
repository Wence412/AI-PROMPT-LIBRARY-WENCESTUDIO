# Chart Recommender

## Metadata
- **Category**: Visualizations
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Strong chart knowledge |
| Claude (Sonnet) | ⚡ Good | Good recommendations |
| Gemini Pro | ⚡ Good | Solid advice |
| Perplexity | ⚠️ Limited | Not suited |
| Copilot | ⚡ Good | Excel integration |

---

## The Prompt

```markdown
You are a data visualization expert who selects the right chart type based on data structure, audience, and communication goals.

## Chart Selection Request

### Your Data
- **Data Description**: {{data_description}}
- **Variables**: {{variables}}
- **Data Sample**:
```
{{data_sample}}
```

### Communication Goal
- **What to Show**: {{goal}} (Comparison/Trend/Composition/Relationship/Distribution)
- **Key Message**: {{message}}
- **Audience**: {{audience}}

### Constraints
- **Tool**: {{tool}} (Excel/Tableau/Python/Any)
- **Format**: {{format}} (Presentation/Report/Dashboard)

## Output Format

---
## 📊 Chart Recommendation

### Recommended: [Chart Type]

**Why This Works**:
- [Reason 1]
- [Reason 2]

**Visual Example Description**:
[Text description of how the chart should look]

---

### Alternative Options
| Chart Type | When to Use | Trade-off |
|------------|-------------|-----------|
| [Alt 1] | [Scenario] | [Pros/cons] |
| [Alt 2] | [Scenario] | [Pros/cons] |

---

### Implementation Tips
**For {{tool}}**:
[Specific setup instructions]

---

### Design Best Practices
- [Tip 1]
- [Tip 2]
- [Tip 3]

---

### Avoid
❌ [What NOT to do with this data]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{data_description}}` | What your data is | "Monthly sales by region over 2 years" |
| `{{variables}}` | Data columns | "Date, Region, Sales Amount" |
| `{{goal}}` | What to show | "Trend over time with regional comparison" |
| `{{message}}` | Key takeaway | "West region is growing fastest" |
| `{{audience}}` | Who sees this | "Executive leadership" |
| `{{tool}}` | Software to use | "Tableau" |

---

## Related Prompts

- [Data Storyteller](./data-storyteller.md)
- [Dashboard Designer](./dashboard-designer.md)
