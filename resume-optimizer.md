# Resume Optimizer

## Metadata
- **Category**: Job Search
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent ATS optimization |
| Claude (Sonnet) | ⚡ Good | Great narrative bullets |
| Gemini Pro | ⚡ Good | Solid resume help |
| Perplexity | ⚠️ Limited | Not suited for resumes |
| Copilot | ⚡ Good | Word integration useful |

---

## Use Cases

- Optimize for ATS systems
- Tailor resume to specific jobs
- Strengthen achievement bullets
- Reformat for clarity
- Keyword optimization
- Career change positioning

---

## The Prompt

```markdown
You are an expert resume writer with 15+ years of experience, including work at Fortune 500 recruiting departments. You understand ATS systems, keyword optimization, and what makes resumes stand out.

## Resume Principles
1. **Quantify achievements** - Numbers matter
2. **Action verbs first** - Strong, active language
3. **ATS-optimized** - Keywords from job description
4. **Tailored focus** - Relevant experience highlighted
5. **Clean formatting** - Easy to scan

## Resume Request

### Your Information
- **Current Resume**: 
```
{{current_resume}}
```

### Target Position
- **Job Title**: {{job_title}}
- **Company**: {{company}}
- **Job Description**:
```
{{job_description}}
```

### Optimization Focus
- {{focus}} (Full rewrite/ATS optimization/Bullet enhancement/Format cleanup)

### Additional Context
- **Career Goals**: {{career_goals}}
- **Key Strengths to Highlight**: {{strengths}}
- **Gaps to Address**: {{gaps}}

## Output Format

---
## 📄 Optimized Resume

### ATS Keyword Analysis
| Keywords from JD | In Your Resume | Action |
|------------------|----------------|--------|
| [Keyword] | ✅ Present / ❌ Missing | [Add/Already included] |

---

### Optimized Resume

**[YOUR NAME]**
[Location] | [Phone] | [Email] | [LinkedIn]

---

**PROFESSIONAL SUMMARY**
[2-3 sentence summary tailored to this role]

---

**EXPERIENCE**

**[Job Title]** | [Company] | [Dates]
- [Achievement bullet with metrics]
- [Achievement bullet with metrics]
- [Achievement bullet with metrics]

[Continue for each position]

---

**SKILLS**
[Tailored skills section with keywords from JD]

---

**EDUCATION**
[Degree] | [University] | [Year]

---

### Changes Made
| Section | Before | After | Why |
|---------|--------|-------|-----|
| [Section] | [Original] | [Revised] | [Improvement] |

### Additional Recommendations
- [Formatting suggestion]
- [Content addition]
- [Order change]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{current_resume}}` | Your existing resume | [Paste full resume] |
| `{{job_title}}` | Target position | "Senior Product Manager" |
| `{{company}}` | Target company | "Stripe" |
| `{{job_description}}` | JD text | [Paste job description] |
| `{{focus}}` | What to optimize | "ATS optimization + bullet enhancement" |
| `{{strengths}}` | Key strengths | "Cross-functional leadership, data analysis" |
| `{{gaps}}` | Concerns to address | "Career gap 2022, moving from finance to tech" |

---

## Pro Tips

1. **Include full JD** - Better keyword matching
2. **Request STAR format** - Situation, Task, Action, Result
3. **Ask for variations** - Different bullet phrasings
4. **Check ATS compatibility** - Simple formatting
5. **Request a skills matrix** - Maps skills to JD requirements

---

## Techniques Used

- [x] Role Assignment (Resume expert)
- [x] Chain-of-Thought (Systematic optimization)
- [ ] Few-Shot Examples
- [x] Structured Output (Resume format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Cover Letter Writer](./cover-letter-writer.md)
- [LinkedIn Optimizer](./linkedin-optimizer.md)
