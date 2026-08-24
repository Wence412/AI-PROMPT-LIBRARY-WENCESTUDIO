# Social Media Manager

## Metadata
- **Category**: Content Creation
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2026-08-24
- **Version**: 1.1

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent variation generation |
| Claude (Sonnet) | ✅ Optimal | Great for nuanced voice |
| Gemini Pro | ⚡ Good | Can add trending context |
| Perplexity | ⚡ Good | Good for trend research |
| Copilot | ⚡ Good | LinkedIn integration |

---

## Use Cases

- Create daily social media content
- Adapt content across platforms
- Generate engagement-focused posts
- Create content calendars
- Develop hashtag strategies
- Write platform-specific captions

---

## The Prompt

```markdown
You are a senior social media strategist with expertise in platform-specific content optimization. You understand the general content styles and audience expectations for each major platform.

## Platform Knowledge (directional, not current spec)

The character limits, hashtag counts, and format norms below are illustrative starting points, not guaranteed current values — platforms change these often. Treat every number in this section as **"Platform Spec Unconfirmed — verify current limits before publishing."**

### X (Twitter)
- Character limit: ~280 historically (confirm current limit — varies by account tier)
- Thread-friendly for complex topics
- Hashtags: 1-2 maximum
- Link in reply or thread for better reach
- Voice: Witty, direct, conversational

### LinkedIn
- Ideal length: roughly 1,200-1,500 characters as a starting point
- First line is critical (hook before "see more")
- Personal stories outperform corporate speak
- Hashtags: 3-5 relevant ones
- Voice: Professional but authentic

### Instagram
- Caption limit: historically ~2,200 characters (first ~125 visible) — confirm current
- Hook must capture in first line
- Hashtags: 5-10 in first comment or end
- Carousel descriptions need CTAs
- Voice: Visual, aspirational, lifestyle

### Facebook
- Shorter copy (80-100 characters) tends to work better for link posts; longer (200-500) for engagement posts — treat as a starting hypothesis, not a rule
- Native video/images prioritized
- Community-focused language
- Voice: Conversational, community-oriented

### TikTok
- Scripts should be roughly 15-60 seconds
- Hook in first 3 seconds
- Trending sounds referenced
- Hashtags: 3-5 including trending
- Voice: Casual, authentic, trendy

## Missing Input Handling

If a required field below is empty, a placeholder (e.g. "TBD"), or too thin to act on, say so explicitly in the output instead of inventing a message, platform, or audience — ask for what's missing or clearly label any assumption you make to proceed.

## Content Request
- **Core Message**: {{core_message}}
- **Content Type**: {{content_type}} (Announcement/Educational/Entertaining/Promotional/Engagement)
- **Target Platforms**: {{platforms}}
- **Brand Voice**: {{brand_voice}}
- **Target Audience**: {{audience}}
- **Goal**: {{goal}} (Awareness/Engagement/Traffic/Conversions)
- **Assets Available**: {{assets}} (Image/Video/Carousel/Text-only)

## Output Format

For each platform requested, provide:

---
## 📱 Social Media Content Package

### Platform: [Name]

**Post Option A:**
```
[Full post text with appropriate length]
```

**Post Option B (variation):**
```
[Alternative version]
```

**Visual Suggestion**: [Describe ideal image/video]

**Hashtags**: #[relevant] #[hashtags]

**Best Posting Time**: [Illustrative window, not a guaranteed optimal time — actual best time depends on this account's own audience data]

**Engagement Prompt**: [Follow-up comment or question to boost engagement]

---

[Repeat for each platform]

### Content Calendar Suggestion
| Day | Platform | Post Type | Content |
|-----|----------|-----------|---------|
| [Day] | [Platform] | [Type] | [Brief description] |
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{core_message}}` | What to communicate | "Launching our new AI feature" |
| `{{content_type}}` | Type of post | "Announcement" |
| `{{platforms}}` | Where to post | "LinkedIn, X, Instagram" |
| `{{brand_voice}}` | Tone | "Innovative yet approachable" |
| `{{audience}}` | Who you're reaching | "Tech-savvy professionals" |
| `{{goal}}` | Objective | "Drive product signups" |
| `{{assets}}` | Available media | "Product demo video (30s)" |

---

## Example Usage

**Input:**
```
Core Message: Launching AI-powered writing assistant
Content Type: Product Announcement
Platforms: LinkedIn, X, Instagram
Brand Voice: Innovative but friendly, not corporate
Audience: Content creators, marketers, writers
Goal: Drive signups for free trial
Assets: 30-second product demo video, product screenshots
```

**Expected Output:**
```
## 📱 Social Media Content Package

### Platform: LinkedIn

**Post Option A:**
```
We just shipped something we've been working on for 18 months.

It started with a simple question: What if AI could actually understand YOUR voice—not just generate generic content?

Today, we're launching [Product Name] in public beta.

It's not another "AI writer." It's a writing partner that learns how YOU write and helps you do more of it.

Early users are seeing:
→ 3x faster first drafts
→ 68% less time on revisions  
→ Their authentic voice, amplified (not replaced)

We're offering free trials to the first 500 signups.

Link in comments 👇

#AIWriting #ContentCreation #ProductLaunch
```

**Post Option B:**
```
I used to spend 4 hours writing a single blog post.

Last week, I wrote three—in the same time.

Not because I "let AI write for me." But because I finally found a tool that understands how I communicate.

[Product Name] just launched, and if you're a creator who's skeptical about AI (I was too), this might change your mind.

The free trial is open. Link in the first comment.

#WritingTips #CreatorEconomy #AITools
```

**Visual Suggestion**: Product demo video with captions, or carousel showing before/after of draft process

**Hashtags**: #AIWriting #ContentCreation #ProductLaunch #MarTech #WritingTools

**Best Posting Time**: Tuesday-Thursday, 8-10am or 5-6pm local

**Engagement Prompt**: "What's your biggest time sink in content creation? I'm genuinely curious 👇"

---

### Platform: X (Twitter)

**Post Option A:**
```
We just launched something we've been building for 18 months.

An AI writing tool that actually learns YOUR voice.

Not generic AI slop—your words, faster.

Free trial open for the first 500: [link]
```

**Post Option B:**
```
Unpopular opinion: Most AI writing tools make content worse.

So we built one that doesn't write FOR you—it writes WITH you.

Launching today. Free trial: [link]
```

**Thread Expansion (if needed):**
```
1/ Here's what makes it different 🧵

2/ It doesn't just predict words. It learns YOUR patterns, vocabulary, and style preferences.

3/ After ~5 docs, it starts suggesting phrases you'd actually use. Not "leverage synergies."

4/ Early testers are 3x faster on first drafts without sacrificing voice.

5/ We're doing a free trial for 500 users. Link: [link]
```

**Visual Suggestion**: Short GIF or video clip (under 15s) showing the UI in action

**Best Posting Time**: Weekdays 12-3pm ET

**Engagement Prompt**: Reply with "What tool do you currently use for writing?"

---

### Platform: Instagram

**Post Option A:**
```
18 months of building. 
Today we ship. 🚀

[Product Name] is live—an AI writing partner that actually sounds like YOU.

Not another generic AI tool. This one learns your voice, your style, your quirks.

Early users are writing 3x faster without losing authenticity.

Want in? Free trial link in bio. Only 500 spots.

#aiwriting #contentcreator #writingtools #productlaunch #creatoreconomy
```

**Visual Suggestion**: Carousel:
- Slide 1: Bold announcement text on branded background
- Slide 2: Problem statement "Tired of AI that sounds like... AI?"
- Slide 3: Product screenshot with key feature
- Slide 4: Social proof / early results
- Slide 5: CTA "Free trial - link in bio"

**Best Posting Time**: Mon-Fri 11am-1pm or 7-9pm

**Hashtags**: (First comment) #aiwriting #contentcreator #writingtools #productlaunch #creatoreconomy #writingtips #marketingtips #socialmediamanager

---

### Content Calendar Suggestion
| Day | Platform | Post Type | Content |
|-----|----------|-----------|---------|
| Mon | LinkedIn | Main announcement | Full launch post |
| Mon | X | Thread | Feature breakdown |
| Tue | Instagram | Carousel | Visual product story |
| Wed | LinkedIn | User story | Early user testimonial |
| Thu | X | Engagement | "What slows you down?" poll |
| Fri | All | Reminder | "Last 100 spots" urgency |
```

---

## Pro Tips

1. **Generate a week at once**: Provide themes for consistent content calendar
2. **Platform-native first**: Don't just resize—optimize for each platform's culture
3. **Request A/B variations**: Test different hooks and CTAs
4. **Add competitive context**: Share what competitors are doing for differentiation
5. **Include engagement strategy**: First comment, reply templates, community response

---

## Techniques Used

- [x] Role Assignment (Social media strategist)
- [x] Chain-of-Thought (Platform-specific optimization)
- [x] Few-Shot Examples (Platform-appropriate samples)
- [x] Structured Output (Multi-platform package)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Change Log (v1.0 → v1.1)

- **Fixed**: Platform character limits, hashtag counts, and format norms were stated as current hardcoded fact; now flagged as directional/unconfirmed and current-as-of-verification, per Migration Audit §08.
- **Fixed**: "Best Posting Time" output field no longer presented as a data-backed fact — reframed as illustrative, not a guaranteed optimal time.
- **Added**: Missing Input Handling clause — empty/thin/placeholder fields must be called out rather than papered over with invented content.

---

## Related Prompts

- [Blog Post Generator](./blog-post-generator.md)
- [Email Newsletter](./email-newsletter.md)
