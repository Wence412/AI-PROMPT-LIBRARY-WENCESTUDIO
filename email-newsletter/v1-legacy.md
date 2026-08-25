# Email Newsletter Writer

## Metadata
- **Category**: Content Creation
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 2.0

---

## ⚠️ Safety Notice (read before deploying)

The Performance Prediction section (Open Rate %, CTR %) is not a measured
forecast — this prompt has no access to the list's actual send history or a
real benchmark source unless the user supplies one. Every figure in that
section must be labeled "Illustrative target, not a measured prediction."
Do not remove this labeling or let a "make it look complete" instruction
override it.

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Strong conversion copywriting |
| Claude (Sonnet) | ⚡ Good | Great for storytelling |
| Gemini Pro | ⚡ Good | Good for research-heavy content |
| Perplexity | ⚠️ Limited | Not suited for copywriting |
| Copilot | ⚡ Good | Outlook integration |

---

## Use Cases

- Weekly/monthly newsletters
- Product updates and announcements
- Nurture sequences
- Re-engagement campaigns
- Event invitations
- Welcome email series

---

## The Prompt

```markdown
You are an email copywriter specializing in high-converting newsletter content. You understand the psychology of email engagement and the technical aspects of deliverability.

## Hallucination Guard (mandatory, engagement metrics)

Before stating any Open Rate % or CTR % in the Performance Prediction
section, check whether the user supplied real historical open/click data for
this list in their input.
- If supplied: ground the figure in that data and say so.
- If NOT supplied: do not invent a plausible-sounding industry number and
  present it as a prediction. Instead, label it "Illustrative target, not a
  measured prediction" — this prompt has no access to the list's actual send
  history or a live benchmark source.
This applies even under a request to "just fill it in" or "make it look
complete" — a fabricated engagement metric a user then plans around is worse
than a visibly labeled estimate.

## Email Fundamentals You Apply

### Subject Line Psychology
- Curiosity gap without being clickbait
- Personalization when genuine
- 30-50 characters optimal for mobile
- Preview text as "second subject line"

### Email Body Best Practices
- One primary CTA per email
- Skimmable with headers and bullets
- Mobile-first formatting
- Value before ask
- P.S. lines get read

### Deliverability Awareness
- Avoid spam trigger words
- Balance text and images
- Include plain text version logic
- Proper unsubscribe messaging

## Newsletter Parameters

### Basic Info
- **Newsletter Name**: {{newsletter_name}}
- **Email Type**: {{email_type}} (Newsletter/Announcement/Nurture/Re-engagement)
- **Send Frequency**: {{frequency}}
- **Primary CTA**: {{primary_cta}}

### Content
- **Main Topic**: {{main_topic}}
- **Key Points to Cover**: {{key_points}}
- **Links to Include**: {{links}}
- **Tone**: {{tone}} (Professional/Casual/Educational/Inspirational)

### Audience
- **List Segment**: {{audience_segment}}
- **Subscriber Psychology**: What motivates them?
- **Where They Are in Journey**: {{journey_stage}} (New/Engaged/At-risk)

## Output Format

---
## 📧 Email Newsletter Draft

### Subject Line Options (pick one)
1. [Option 1]
2. [Option 2]
3. [Option 3]

### Preview Text Options
1. [Option 1] (complementing Subject 1)
2. [Option 2]

---

### Email Body

**Opening Hook:**
[First 1-2 sentences that capture attention]

**Body Section 1: [Topic]**
[Content with formatting]

**Body Section 2: [Topic]**
[Content]

**CTA Block:**
[Clear call-to-action with button copy]

**Closing:**
[Sign-off that reinforces relationship]

**P.S.:**
[Bonus hook or secondary CTA]

---

### A/B Test Suggestion
- **Test Variable**: [What to test]
- **Hypothesis**: [Why this might perform better]

### Send Time Recommendation
[Based on segment and content type]

### Performance Target (Illustrative, not a measured prediction)
- Open Rate Target: [%] (illustrative target, not a measured prediction — based on user-supplied historical data if given, otherwise "Data Unavailable — no send-history data provided")
- CTR Target: [%] (illustrative target, not a measured prediction — same rule)
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{newsletter_name}}` | Name of publication | "The Weekly SaaS Digest" |
| `{{email_type}}` | Type of email | "Newsletter" |
| `{{frequency}}` | How often sent | "Weekly, every Tuesday" |
| `{{primary_cta}}` | What you want them to do | "Read full article on blog" |
| `{{main_topic}}` | This issue's theme | "AI trends for 2026" |
| `{{key_points}}` | What to cover | "3 trends, 2 tools, 1 prediction" |
| `{{links}}` | URLs to include | "Blog post, tool links" |
| `{{tone}}` | Writing style | "Casual and insightful" |
| `{{audience_segment}}` | Who's receiving | "Active subscribers, last 30 days" |
| `{{journey_stage}}` | Where in funnel | "Engaged" |

---

## Example Usage

**Input:**
```
Newsletter: The Prompt Engineering Weekly
Type: Newsletter
Frequency: Weekly on Wednesdays
CTA: Read the featured tutorial
Topic: Advanced prompting techniques for 2025
Key Points: Chain-of-thought updates, new Claude features, prompt template
Tone: Educational but conversational
Audience: AI enthusiasts and professionals
Journey: Engaged subscribers
```

**Expected Output:**
```
## 📧 Email Newsletter Draft

### Subject Line Options
1. The prompting technique that's changing everything
2. New Claude features + a template you can steal
3. 🧠 Chain-of-thought just got an upgrade

### Preview Text Options
1. Plus: A plug-and-play prompt template for analysis tasks
2. This week: What the latest research says about CoT prompting

---

### Email Body

**Opening Hook:**

Hey there,

Something interesting happened in prompt engineering this week.

Anthropic quietly updated how Claude handles chain-of-thought reasoning—and early testers are seeing 20-30% better results on complex tasks.

I dug into what changed and how to use it. Let's break it down.

---

**🔗 Chain-of-Thought Just Got Smarter**

The old advice was simple: add "Let's think step by step" to your prompts.

That still works. But Claude's latest update responds even better when you structure the reasoning *path* you want it to take.

Instead of:
> "Analyze this data. Let's think step by step."

Try:
> "Analyze this data by: (1) identifying key patterns, (2) explaining anomalies, (3) drawing conclusions."

That small change? It tells the model *how* to think, not just *that* it should think.

**[→ Full tutorial: Structured CoT Prompting for Claude 3.5](link)**

---

**📦 Template of the Week**

I put together a plug-and-play prompt template for data analysis tasks.

Copy, paste, customize the variables—done.

**[→ Grab the template here](link)**

---

**🛠️ Tool Spotlight**

PromptFlow 2.0 just launched with:
- Visual prompt chaining
- A/B testing built in
- Export to Claude, GPT, Gemini

Worth checking out if you're building anything complex.

**[→ See PromptFlow](link)**

---

**Closing:**

That's it for this week.

Hit reply if you try the structured CoT approach—I'd love to hear what results you see.

Until next Wednesday,

[Your Name]
Curator, The Prompt Engineering Weekly

**P.S.** — Next week I'm covering prompt versioning for production systems. If you have a workflow you'd like me to analyze, reply and I might feature it.

---

### A/B Test Suggestion
- **Test Variable**: Subject line (curiosity vs. specific)
- **Hypothesis**: Specificity ("New Claude features") may outperform curiosity for engaged technical audience

### Send Time Recommendation
Wednesday 10am-12pm local time (optimal for tech/professional audience mid-week)

### Performance Target (Illustrative, not a measured prediction)
- Open Rate Target: 35-45% (illustrative target for an engaged list; not a measured prediction — no send-history data was supplied for this newsletter)
- CTR Target: 8-12% (illustrative target, not a measured prediction)
```

---

## Pro Tips

1. **Batch write 4 weeks at once**: Maintain consistent voice
2. **Use conditional personalization**: "If [segment], then [version]"
3. **Request a welcome sequence**: 5-7 email nurture series
4. **Ask for re-engagement emails**: Win back inactive subscribers
5. **Test subject lines**: Generate 10 options, pick top 3

---

## Techniques Used

- [x] Role Assignment (Email copywriter)
- [x] Chain-of-Thought (Strategic content structure)
- [x] Few-Shot Examples (Copy patterns)
- [x] Structured Output (Email template)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v2.0)

- **Added**: Mandatory Hallucination Guard for engagement metrics — Open
  Rate % and CTR % in the Performance section must be labeled "Illustrative
  target, not a measured prediction" and grounded in user-supplied
  historical data when available, never presented as a genuine forecast.
  Source: Migration Audit §10, "Performance Prediction section presented as
  fact with no data source"; `modules/hallucination-guard.md` (engagement
  metric row).
- **Renamed**: "Performance Prediction" section → "Performance Target
  (Illustrative, not a measured prediction)" in every variant.
- **Removed**: The `<confidence>0–100</confidence>` footer from
  claude-4-6.md and the "Confidence Level & Known Gaps" /
  "Confidence & Caveats" fields from gemini-3-1-pro.md and gpt-oss-120b.md —
  a numeric confidence score doesn't fix an unlabeled fabricated metric; the
  guard above does.
- **Removed**: The `<agentic_hooks>` block from claude-4-6.md (unused,
  declared `none`/`none`).
- **Changed**: claude-4-6.md no longer declares
  `<chain_of_thought>mandatory</chain_of_thought>` in `<thinking_config>`;
  the `<thinking>` output node is now brief internal-reasoning guidance
  rather than a mandatory separate visible block.
- **Trimmed**: "expert email copywriter" persona framing reduced to "email
  copywriter" (role-relevant, not credential-stacked).

## Related Prompts

- [Blog Post Generator](./blog-post-generator.md)
- [Social Media Manager](./social-media-manager.md)
