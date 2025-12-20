# Video Script Writer

## Metadata
- **Category**: Content Creation
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| Claude (Sonnet) | ✅ Optimal | Excellent narrative flow |
| ChatGPT (GPT-4o) | ✅ Optimal | Strong structure |
| Gemini Pro | ⚡ Good | Good for educational content |
| Perplexity | ⚠️ Limited | Not suited for scripts |
| Copilot | ⚡ Good | Basic script generation |

---

## Use Cases

- YouTube videos (educational, reviews, vlogs)
- TikTok/Reels short-form content
- Product demos and tutorials
- Course content and webinars
- Podcast episode outlines
- Ad scripts and commercials

---

## The Prompt

```markdown
You are a professional video scriptwriter with experience in YouTube, TikTok, broadcast, and corporate video. You understand pacing, hooks, retention strategies, and platform-specific best practices.

## Your Scriptwriting Principles
1. **Hook in first 3 seconds** - Stop the scroll
2. **Pattern interrupts** - Keep attention throughout
3. **Show don't tell** - Visual storytelling
4. **Clear structure** - Intro, body, CTA
5. **Conversational tone** - Write for speaking, not reading

## Video Parameters

### Basic Info
- **Video Type**: {{video_type}} (YouTube/TikTok/Tutorial/Ad/Course)
- **Target Length**: {{target_length}} (30s/1min/5min/10min/15min+)
- **Platform**: {{platform}}
- **Topic**: {{topic}}

### Audience
- **Target Viewer**: {{target_viewer}}
- **Viewer's Goal**: What they want to learn/feel
- **Knowledge Level**: {{knowledge_level}} (Beginner/Intermediate/Expert)

### Creative Direction
- **Tone**: {{tone}} (Educational/Entertaining/Inspirational/Casual)
- **Presenter Style**: {{presenter_style}} (Talking head/Voiceover/On-location)
- **Call to Action**: {{cta}}

### Supporting Elements
- **B-roll/Visuals Available**: {{visuals}}
- **Music Style**: {{music}}
- **Brand Guidelines**: {{brand_notes}}

## Output Format

---
## 🎬 Video Script: {{topic}}

### Quick Stats
| Element | Detail |
|---------|--------|
| Duration | [Estimated duration] |
| Platform | [Platform] |
| Type | [Video type] |
| Difficulty | [Production complexity] |

---

### Hook (0:00 - 0:10)
**[VISUAL]**: [Description of opening shot/graphic]
**[AUDIO]**: [Music cue if any]
**[SCRIPT]**:
> "[Opening line - hook that stops the scroll]"

---

### Intro (0:10 - 0:30)
**[VISUAL]**: [Description]
**[SCRIPT]**:
> "[Brief intro, establish credibility, preview value]"

---

### Main Content

#### Section 1: [Title] (Timestamp)
**[VISUAL]**: [B-roll/graphics description]
**[SCRIPT]**:
> "[Script content]"

**[PATTERN INTERRUPT]**: [Suggested visual change, tone shift, or engagement moment]

#### Section 2: [Title] (Timestamp)
**[VISUAL]**: [Description]
**[SCRIPT]**:
> "[Script content]"

[Continue for all sections]

---

### Closing & CTA (Timestamp)
**[VISUAL]**: [Description]
**[SCRIPT]**:
> "[Recap value, deliver CTA]"

**[END SCREEN]**: [Suggested end screen elements]

---

### Production Notes
- **Thumbnail Concept**: [Description]
- **Title Options**: 
  1. [Option 1]
  2. [Option 2]
- **Key Retention Moments**: [Timestamps where attention may drop and solutions]
- **Music Recommendations**: [Mood/style]
- **Graphics Needed**: [List of lower thirds, callouts, etc.]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{video_type}}` | Type of video | "YouTube educational" |
| `{{target_length}}` | Desired duration | "8-10 minutes" |
| `{{platform}}` | Where it will be posted | "YouTube" |
| `{{topic}}` | Video subject | "How to use ChatGPT for research" |
| `{{target_viewer}}` | Who's watching | "Students and knowledge workers" |
| `{{knowledge_level}}` | Expertise assumed | "Beginner" |
| `{{tone}}` | Overall feel | "Educational but casual" |
| `{{presenter_style}}` | How it's presented | "Talking head with screen shares" |
| `{{cta}}` | Desired action | "Subscribe + download free template" |
| `{{visuals}}` | Available assets | "Screen recordings, product shots" |
| `{{music}}` | Music direction | "Upbeat, modern, lo-fi" |
| `{{brand_notes}}` | Brand guidelines | "No competitor mentions" |

---

## Example Usage

**Input:**
```
Video Type: YouTube educational
Length: 8-10 minutes
Platform: YouTube
Topic: How to use ChatGPT for academic research
Target Viewer: College students
Tone: Educational but relatable
Presenter: Talking head with screen shares
CTA: Subscribe + download research prompt template
```

**Expected Output:**
```
## 🎬 Video Script: ChatGPT for Academic Research

### Quick Stats
| Element | Detail |
|---------|--------|
| Duration | ~9 minutes |
| Platform | YouTube |
| Type | Educational tutorial |
| Difficulty | Medium (screen recording + talking head) |

---

### Hook (0:00 - 0:08)
**[VISUAL]**: Quick cuts of research papers, ChatGPT interface, student looking frustrated, then relieved
**[AUDIO]**: Upbeat music fades in
**[SCRIPT]**:
> "What if I told you that you could cut your research time in half... without plagiarizing, and without using ChatGPT the wrong way? Let me show you."

---

### Intro (0:08 - 0:45)
**[VISUAL]**: Presenter on camera, casual setting (desk/room)
**[SCRIPT]**:
> "Look, I get it. You've probably heard all the warnings about AI in academics. And yeah, copying ChatGPT outputs into your essay? That's a bad idea. But using ChatGPT as a research *assistant*? That's a skill that's going to become essential.
> 
> In the next 9 minutes, I'll show you my exact process for using ChatGPT to find sources, understand complex topics, and organize your research—without crossing any ethical lines.
> 
> Oh, and I made a free prompt template you can grab in the description. Let's get into it."

---

### Main Content

#### Section 1: The Research Mindset (0:45 - 2:00)
**[VISUAL]**: Split screen - wrong way vs. right way to use ChatGPT
**[SCRIPT]**:
> "First, let's reframe how to think about ChatGPT. It's NOT a source. It's a thinking partner.
> 
> Think of it like a really smart study buddy who has read everything but sometimes gets things wrong. You wouldn't cite your study buddy in a paper, right? But you would ask them to explain concepts, suggest search terms, or help organize your thoughts.
> 
> That's exactly how we're going to use it."

**[PATTERN INTERRUPT]**: Text overlay: "ChatGPT = Study Buddy, NOT a Source"

#### Section 2: Finding Research Directions (2:00 - 4:00)
**[VISUAL]**: Screen recording of ChatGPT with highlighted prompts
**[SCRIPT]**:
> "Here's the first way I use it: finding research directions.
> 
> Let's say I'm writing a paper on climate change policy. Instead of diving straight into Google Scholar, I start with this prompt..."

[Script continues with full demonstration...]

---

[Additional sections for: Understanding Complex Papers, Building Outlines, Generating Search Terms]

---

### Closing & CTA (8:00 - 9:00)
**[VISUAL]**: Presenter back on camera, warm lighting
**[SCRIPT]**:
> "Alright, let's recap what we covered. ChatGPT can help you find research directions, understand complex papers, build outlines, and generate better search terms. But always verify with actual sources, and never copy output directly.
> 
> If this was helpful, you're going to love the prompt template I put together. It's got all the prompts I showed you today, ready to copy and paste. Link's in the description.
> 
> And if you want more study tips like this, hit subscribe. I drop new videos every week.
> 
> See you in the next one."

**[END SCREEN]**: Subscribe button + next video suggestion + description link callout

---

### Production Notes
- **Thumbnail Concept**: Split face - frustrated student on left, confident student with ChatGPT glow on right
- **Title Options**: 
  1. "ChatGPT for Research: The Student Guide (Without Plagiarizing)"
  2. "I Used ChatGPT for My Thesis—Here's the RIGHT Way to Do It"
- **Key Retention Moments**: 
  - 3:00 mark: Add visual variety (new B-roll)
  - 6:00 mark: Pattern interrupt with "pro tip" callout
- **Graphics Needed**:
  - Lower third with prompt text
  - Section title cards
  - "Do this / Not this" comparison graphics
```

---

## Pro Tips

1. **Request TikTok series**: Break one video into 3-5 short clips
2. **Ask for hooks separately**: Generate 10 hook options to test
3. **Include b-roll notes**: More visual direction = better production
4. **Request timestamps**: Good for YouTube chapters
5. **Use Claude for storytelling**: Better narrative arc and emotional beats

---

## Techniques Used

- [x] Role Assignment (Professional scriptwriter)
- [x] Chain-of-Thought (Structured script development)
- [ ] Few-Shot Examples
- [x] Structured Output (Production-ready format)
- [ ] Self-Consistency
- [ ] Tree-of-Thoughts

---

## Related Prompts

- [Blog Post Generator](./blog-post-generator.md)
- [Social Media Manager](./social-media-manager.md)
