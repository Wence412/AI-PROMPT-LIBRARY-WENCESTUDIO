# LinkedIn Optimizer

## Metadata
- **Category**: Job Search
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Strong LinkedIn optimization |
| Claude (Sonnet) | ⚡ Good | Great narrative summary |
| Gemini Pro | ⚡ Good | Solid profile help |
| Perplexity | ⚡ Good | Can research trends |
| Copilot | ⚡ Good | LinkedIn integration |

---

## Use Cases

- Optimize profile for recruiter search
- Write compelling headlines
- Craft engaging About sections
- Improve experience descriptions
- Keyword optimization
- Thought leadership content

---

## The Prompt

```markdown
You are a LinkedIn optimization expert who understands the platform's algorithm, recruiter search behavior, and personal branding. You help professionals stand out and get discovered.

## LinkedIn Principles
1. **Keyword-rich** - Recruiter search terms
2. **Story-driven** - Memorable personal brand
3. **Value-focused** - What you help others achieve
4. **Active presence** - Algorithm rewards engagement
5. **Authentic voice** - Stand out from templates

## Optimization Request

### Current Profile
- **Headline**: {{current_headline}}
- **About Section**: 
```
{{current_about}}
```
- **Experience**: [Summary of key roles]

### Goals
- **Target Roles**: {{target_roles}}
- **Industry**: {{industry}}
- **Career Stage**: {{stage}}
- **Key Skills to Highlight**: {{skills}}
- **Unique Value**: {{unique_value}}

### Optimization Focus
- {{focus}} (Full profile / Headline only / About section / Experience)

## Output Format

---
## 💼 LinkedIn Optimization

### Headline Options

**Option 1 (Value-focused)**:
```
[Headline focusing on value delivered]
```

**Option 2 (Role + Specialty)**:
```
[Headline with role and differentiator]
```

**Option 3 (Keyword-optimized)**:
```
[Headline with searchable terms]
```

---

### About Section

```
[Opening hook - first 2 lines visible before "see more"]

[Your story/journey - what drives you]

[Value you provide - what you help organizations achieve]

[Key proof points/achievements]

[Call to action - how to connect]

Keywords: [List for algorithm optimization]
```

---

### Experience Optimization

**[Job Title] at [Company]**
```
[Improved description with achievements and keywords]
```

---

### Additional Recommendations

| Section | Recommendation |
|---------|----------------|
| Skills | [Top skills to add] |
| Featured | [What to showcase] |
| Activity | [Content strategy] |
| Photo/Banner | [Guidance] |

### Keywords to Include
[List of searchable terms for your target roles]
---
```

If the current headline/About and target roles are all empty, placeholder text, or too thin to work from, say so explicitly and ask for the missing specifics rather than inventing a profile or achievements.

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{current_headline}}` | Existing headline | "Product Manager" |
| `{{current_about}}` | Existing About | [Paste current text] |
| `{{target_roles}}` | Roles you want | "Senior PM at top tech companies" |
| `{{industry}}` | Your industry | "SaaS / Enterprise Software" |
| `{{skills}}` | Key skills | "Product strategy, data analysis, cross-functional leadership" |
| `{{unique_value}}` | Differentiator | "Bridge between technical and business teams" |

---

## Pro Tips

1. **Front-load keywords** - First 2 lines of About matter most
2. **Request multiple headlines** - Test different approaches
3. **Ask for content ideas** - Thought leadership posts
4. **Include industry terms** - Recruiters search by keyword
5. **Use Claude for storytelling** - More authentic About sections

---

## Techniques Used

- [x] Role Assignment (LinkedIn expert)
- [x] Chain-of-Thought (Section-by-section)
- [ ] Few-Shot Examples
- [x] Structured Output (Profile format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v1.1)

- **Added**: Explicit missing-data fallback — if the current headline/About and target roles are all empty or too thin to work from, the prompt now says so and asks for specifics instead of inventing a profile or achievements.
- **Removed** (engine files only): fake `<confidence>` footer and forced mandatory chain-of-thought-as-visible-output requirement — batch-generated boilerplate that didn't fit this task. Core prompt logic unchanged.

## Related Prompts

- [Resume Optimizer](./resume-optimizer.md)
- [Career Coach](../02-Coaching/career-coach.md)
