# Sentiment Analyzer

## Metadata
- **Category**: Analyze Text
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent structured analysis |
| Claude (Sonnet) | ✅ Optimal | Nuanced emotional understanding |
| Gemini Pro | ⚡ Good | Solid performance |
| Perplexity | ⚠️ Limited | Not optimized for analysis |
| Copilot | ⚡ Good | Works within M365 context |

---

## Use Cases

- Analyze customer feedback and reviews
- Monitor brand sentiment on social media
- Evaluate employee survey responses
- Assess market research interview transcripts
- Track sentiment trends over time

---

## The Prompt

```markdown
You are an expert sentiment analyst with deep expertise in natural language processing and emotional intelligence. Your task is to perform comprehensive sentiment analysis on the provided text.

## Text to Analyze
{{text_content}}

## Analysis Instructions

Perform a multi-dimensional sentiment analysis following these steps:

### Step 1: Overall Sentiment Classification
Classify the overall sentiment as one of:
- 🟢 **Positive** (score: 0.6 to 1.0)
- 🟡 **Neutral** (score: 0.4 to 0.6)
- 🔴 **Negative** (score: 0.0 to 0.4)

### Step 2: Emotional Dimensions
Identify and score (0-100%) the presence of these emotions:
- Joy/Happiness
- Sadness/Disappointment
- Anger/Frustration
- Fear/Anxiety
- Surprise/Amazement
- Trust/Confidence
- Anticipation/Excitement
- Disgust/Contempt

### Step 3: Key Sentiment Drivers
Identify the specific phrases or topics driving the sentiment.

### Step 4: Confidence Assessment
Rate your confidence in this analysis (Low/Medium/High) with justification.

## Output Format

Provide your analysis in this exact structure:

---
## 📊 Sentiment Analysis Report

### Overall Sentiment
| Metric | Value |
|--------|-------|
| Classification | [Positive/Neutral/Negative] |
| Confidence Score | [0.00 - 1.00] |
| Primary Emotion | [Emotion] |

### Emotional Breakdown
| Emotion | Score | Key Indicators |
|---------|-------|----------------|
| [Emotion] | [%] | [Supporting text] |

### Sentiment Drivers
**Positive Drivers:**
- [Driver 1]: "[Quote]"

**Negative Drivers:**
- [Driver 1]: "[Quote]"

### Key Insights
1. [Insight 1]
2. [Insight 2]
3. [Insight 3]

### Recommendations
Based on this sentiment analysis:
- [Actionable recommendation 1]
- [Actionable recommendation 2]

### Analysis Confidence
**Level**: [High/Medium/Low]
**Justification**: [Why this confidence level]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{text_content}}` | The text to analyze for sentiment | Customer review, social media post, survey response |

---

## Example Usage

**Input:**
```
Text to Analyze:
"I've been using this product for three months now and I'm absolutely thrilled with the results! The quality exceeded my expectations, though the initial setup was a bit confusing. Customer support was helpful when I reached out. Would definitely recommend to friends, but the price is a bit steep for some budgets."
```

**Expected Output:**
```
## 📊 Sentiment Analysis Report

### Overall Sentiment
| Metric | Value |
|--------|-------|
| Classification | 🟢 Positive |
| Confidence Score | 0.72 |
| Primary Emotion | Joy/Satisfaction |

### Emotional Breakdown
| Emotion | Score | Key Indicators |
|---------|-------|----------------|
| Joy | 75% | "absolutely thrilled", "exceeded expectations" |
| Trust | 65% | "Would definitely recommend" |
| Frustration | 25% | "setup was a bit confusing", "price is steep" |

### Sentiment Drivers
**Positive Drivers:**
- Product Quality: "quality exceeded my expectations"
- Results: "absolutely thrilled with the results"
- Support: "Customer support was helpful"
- Advocacy: "Would definitely recommend to friends"

**Negative Drivers:**
- Usability: "initial setup was a bit confusing"
- Pricing: "price is a bit steep for some budgets"

### Key Insights
1. Strong product satisfaction despite minor onboarding friction
2. Customer is a potential brand advocate (recommendation intent)
3. Price sensitivity mentioned but not a deal-breaker

### Recommendations
- Improve setup documentation or onboarding materials
- Consider highlighting value proposition to address price concerns
- Leverage positive testimonials for marketing

### Analysis Confidence
**Level**: High
**Justification**: Clear emotional language with explicit indicators; sufficient text length for reliable analysis.
```

---

## Pro Tips

1. **Batch Analysis**: Modify to analyze multiple texts at once with comparative output
2. **Custom Emotions**: Add industry-specific emotions (e.g., "Trust in Brand" for marketing)
3. **Trend Tracking**: Use consistent scoring to track sentiment over time
4. **Quote Extraction**: Always include supporting quotes for transparency

---

## Techniques Used

- [x] Role Assignment (Expert analyst persona)
- [x] Chain-of-Thought (Step-by-step analysis)
- [ ] Few-Shot Examples
- [x] Structured Output (Tables, formatted report)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Document Summarizer](./document-summarizer.md)
- [Key Insights Extractor](./key-insights-extractor.md)

---

## Change Log

**v1.1 — 2026-08-24**: Removed the batch-applied confidence-score footer and agentic_hooks scaffold from claude-4-6.md, per migration audit §08 (library-wide mechanical fix, no change to this prompt's core logic).
