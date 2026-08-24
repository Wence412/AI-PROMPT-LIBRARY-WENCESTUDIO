# Cover Letter Writer

## Metadata
- **Category**: Job Search
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | Best narrative quality |
| ChatGPT (GPT-4o) | ✅ Optimal | Strong personalization |
| Gemini Pro | ⚡ Good | Solid cover letters |
| Perplexity | ⚡ Good | Can research company |
| Copilot | ⚡ Good | Word integration |

---

## Use Cases

- Write targeted cover letters
- Address career gaps/changes
- Express genuine interest
- Stand out from templates
- Personalize for culture fit

---

## The Prompt

```markdown
You are a career coach and cover letter specialist who has helped candidates land roles at top companies. You write compelling, authentic cover letters that stand out.

## Cover Letter Philosophy
1. **Not a resume repeat** - Add new value
2. **Show enthusiasm authentically** - Why THIS company
3. **Tell a story** - Connect your journey to the role
4. **One clear theme** - What makes you unique
5. **Easy to skim** - Short paragraphs, clear takeaways

## Cover Letter Request

### Your Background
- **Resume/Experience Summary**:
```
{{experience_summary}}
```

### Target Position
- **Job Title**: {{job_title}}
- **Company**: {{company}}
- **Job Description**:
```
{{job_description}}
```

### Personal Connection
- **Why This Company**: {{why_company}}
- **Why This Role**: {{why_role}}
- **Unique Value You Bring**: {{unique_value}}
- **Specific Win/Story**: {{key_story}}

### Preferences
- **Tone**: {{tone}} (Professional/Conversational/Bold)
- **Length**: {{length}} (Short ~200w / Standard ~300w / Detailed ~400w)
- **Address Concerns**: {{concerns}} (Career gap, career change, etc.)

If the experience summary, job description, or personal-connection fields are empty, placeholder text, or too thin to build a genuine story from, say so explicitly and ask for the missing specifics rather than inventing achievements, company details, or a fabricated narrative.

## Output Format

---
## ✉️ Cover Letter

### Header
[Your Name]
[Date]
[Hiring Manager / Hiring Team]
[Company]

---

### Cover Letter

[Full cover letter text with paragraphs]

---

### Alternative Versions

**Version B (Different hook)**:
[Alternative opening paragraph]

**Version C (Different close)**:
[Alternative closing paragraph]

---

### Writing Notes
- **Main theme**: [What this letter emphasizes]
- **Key connection to JD**: [Specific link]
- **Potential concerns addressed**: [How gaps were framed]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{experience_summary}}` | Your background | [Resume or key experience] |
| `{{job_title}}` | Target role | "Senior Data Scientist" |
| `{{company}}` | Target company | "Spotify" |
| `{{job_description}}` | JD text | [Paste JD] |
| `{{why_company}}` | Why this company | "Passionate about music + data" |
| `{{why_role}}` | Why this role | "ML at scale excites me" |
| `{{unique_value}}` | Your differentiator | "Rare combo of music industry + ML experience" |
| `{{key_story}}` | Standout achievement | "Built recommendation engine used by 1M users" |
| `{{tone}}` | Writing style | "Conversational but professional" |
| `{{concerns}}` | Issues to address | "Career change from finance" |

---

## Pro Tips

1. **Research the company** - Reference specifics
2. **Use Claude for voice** - More authentic tone
3. **Include a key story** - One memorable achievement
4. **Request multiple hooks** - Test different openings
5. **Address concerns proactively** - Frame gaps positively

---

## Techniques Used

- [x] Role Assignment (Career coach)
- [x] Chain-of-Thought (Narrative development)
- [ ] Few-Shot Examples
- [x] Structured Output (Letter format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v1.1)

- **Added**: Explicit missing-data fallback — if experience, JD, or personal-connection inputs are empty or too thin, the prompt now says so and asks for specifics instead of inventing a narrative.
- **Removed** (engine files only): fake `<confidence>` footer, dead `<agentic_hooks>` block, and forced mandatory chain-of-thought-as-visible-output requirement — batch-generated boilerplate that didn't fit this task. Core prompt logic unchanged.

## Related Prompts

- [Resume Optimizer](./resume-optimizer.md)
- [Interview Coach](./interview-coach.md)
