# Image Prompt Generator

## Metadata
- **Category**: Creative Arts
- **Difficulty**: ⭐⭐ Intermediate
- **Last Updated**: 2025-12-19
- **Version**: 1.0

---

## Platform Compatibility

| Platform | Rating | Notes |
|----------|--------|-------|
| ChatGPT (GPT-4o) | ✅ Optimal | Excellent for DALL-E style prompts |
| Claude (Sonnet) | ✅ Optimal | Great for detailed descriptions |
| Gemini Pro | ⚡ Good | Works for Imagen prompts |
| Perplexity | ⚠️ Limited | Not suited for this |
| Copilot | ⚡ Good | Basic prompt generation |

---

## Use Cases

- Create prompts for Midjourney, DALL-E, Stable Diffusion
- Develop consistent character designs
- Generate brand visual concepts
- Create art direction for projects
- Explore artistic styles and movements
- Develop visual storytelling assets

---

## The Prompt

```markdown
You are an AI art director with deep knowledge of:
- AI image generation platforms (Midjourney, DALL-E 3, Stable Diffusion, Flux)
- Art history, photography, and visual design
- Prompt engineering for visual AI
- Compositional techniques and color theory

## Your Expertise Areas
1. **Style Translation**: Describing artistic styles precisely
2. **Composition Direction**: Camera angles, framing, depth
3. **Technical Parameters**: Aspect ratios, rendering styles
4. **Consistency Systems**: Creating reproducible characters/worlds
5. **Negative Prompting**: What to exclude

## Image Concept Request

### Core Vision
- **Subject**: {{subject}}
- **Scene/Context**: {{scene}}
- **Mood/Atmosphere**: {{mood}}
- **Style Direction**: {{style}} (Realistic/Illustrated/3D/Painterly)

### Technical Preferences
- **AI Platform**: {{platform}} (Midjourney/DALL-E 3/Stable Diffusion/Flux)
- **Aspect Ratio**: {{aspect_ratio}} (1:1/16:9/9:16/4:3)
- **Rendering Style**: {{rendering}} (Photorealistic/Stylized/Hand-drawn)

### Additional Direction
- **Color Palette**: {{colors}}
- **Lighting**: {{lighting}}
- **Reference Artists/Styles**: {{references}}
- **Must Include**: {{include}}
- **Must Avoid**: {{avoid}}

## Prompt Generation Process

### 1. Subject Description
- Specific details about the main subject
- Character appearance (if applicable)
- Pose, expression, action

### 2. Environment/Background
- Setting details
- Atmospheric elements
- Depth and scale

### 3. Style & Aesthetic
- Art movement/style references
- Color and lighting direction
- Rendering approach

### 4. Technical Modifiers
- Platform-specific syntax
- Quality boosters
- Negative prompts (if applicable)

## Output Format

---
## 🎨 Image Prompt Package

### Concept Overview
[Brief description of the visual concept]

---

### Main Prompt ({{platform}})
```
[Full prompt optimized for the specified platform]
```

### Prompt Variations
**Variation 1 (Different angle/mood)**:
```
[Alternative prompt]
```

**Variation 2 (Different style)**:
```
[Alternative prompt]
```

---

### Platform-Specific Notes

**Midjourney Parameters**:
```
--ar [ratio] --v [version] --style [style] --s [stylize value]
```

**Negative Prompt (if SD/Flux)**:
```
[What to exclude]
```

---

### Style Reference Board
| Element | Description |
|---------|-------------|
| Art Style | [Movement/artist reference] |
| Color Mood | [Palette description] |
| Lighting | [Type and direction] |
| Composition | [Framing approach] |

### Iteration Suggestions
1. [How to modify for different result]
2. [Variation to try]
3. [Style shift suggestion]
---
```

---

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{subject}}` | Main subject | "A cyberpunk street vendor" |
| `{{scene}}` | Context/setting | "Rain-soaked neon alley in Tokyo 2087" |
| `{{mood}}` | Emotional atmosphere | "Melancholic but vibrant" |
| `{{style}}` | Visual approach | "Realistic with stylized lighting" |
| `{{platform}}` | AI tool target | "Midjourney v6" |
| `{{aspect_ratio}}` | Image ratio | "16:9" |
| `{{colors}}` | Color direction | "Cyan and magenta neons, dark blues" |
| `{{lighting}}` | Light description | "Neon reflections on wet pavement" |
| `{{references}}` | Style influences | "Blade Runner, Syd Mead" |

---

## Example Usage

**Input:**
```
Subject: Solitary lighthouse keeper
Scene: Small lighthouse on rocky island during a storm
Mood: Isolation, resilience, quiet determination
Style: Painterly, romantic era inspired
Platform: Midjourney v6
Aspect Ratio: 2:3 (portrait)
Colors: Storm grays, warm window glow, foam white
Lighting: Dramatic storm light, warm interior glow
References: Caspar David Friedrich, Andrew Wyeth
```

**Expected Output:**
```
## 🎨 Image Prompt Package

### Concept Overview
A solitary lighthouse keeper stands within a weathered lighthouse perched on a rocky outcrop, battered by a violent storm. The image channels the Romantic tradition of the sublime—human resilience against nature's overwhelming power.

---

### Main Prompt (Midjourney v6)
```
A solitary lighthouse keeper standing in the lamp room of a weathered stone lighthouse, looking out at a violent storm :: the lighthouse perched on dark jagged rocks, massive waves crashing below :: warm golden light from the lamp behind him, his silhouette partially visible :: storm clouds swirling in dramatic formations, lightning in the distance :: romantic era oil painting style, painterly brushstrokes visible :: atmosphere of isolation and quiet determination :: color palette of storm grays, deep ocean blues, warm amber glow, foam white :: inspired by Caspar David Friedrich and Andrew Wyeth :: dramatic chiaroscuro lighting --ar 2:3 --v 6 --s 250
```

### Prompt Variations
**Variation 1 (Exterior view)**:
```
A tiny lighthouse on a rocky island, dwarfed by massive storm waves crashing against the rocks :: a single warm light glowing from the lamp room :: dramatic stormy sky with ships struggling in the distance :: romantic sublime style, oil painting aesthetic :: Caspar David Friedrich inspiration :: atmosphere of humanity's fragility against nature --ar 2:3 --v 6 --s 300
```

**Variation 2 (More illustrative)**:
```
Lighthouse keeper illustration, a weathered elderly man in oilskin coat standing at the lighthouse window :: warm lamp glow illuminating his determined face :: violent storm visible through rain-streaked glass :: watercolor and ink illustration style :: maritime folklore aesthetic :: nostalgic and resilient mood --ar 2:3 --v 6 --style raw
```

---

### Platform-Specific Notes

**Midjourney Parameters**:
```
--ar 2:3 --v 6 --s 250 (stylize for painterly emphasis)
Optional: --style raw for less Midjourney "polish"
```

---

### Style Reference Board
| Element | Description |
|---------|-------------|
| Art Style | Romantic Sublime, Hudson River School influence |
| Color Mood | Storm palette (grays, blues) with warm amber accent |
| Lighting | Chiaroscuro—dramatic contrast between storm and lamp |
| Composition | Central figure dwarfed by nature (Romantic tradition) |

### Iteration Suggestions
1. Add `--chaos 20` for more dramatic cloud formations
2. Try `cinematic film still` for more photorealistic version
3. Replace Friedrich with Turner for more atmospheric abstraction
```

---

## Pro Tips

1. **Platform-specific syntax**: Midjourney uses `::` for weighting, `--` for parameters
2. **Front-load important elements**: What comes first matters more
3. **Use artist references**: "in the style of [artist]" guides aesthetic
4. **Request character sheets**: Consistent character across poses
5. **Build prompt libraries**: Save successful prompts for reuse

---

## Techniques Used

- [x] Role Assignment (AI art director)
- [x] Chain-of-Thought (Systematic prompt building)
- [ ] Few-Shot Examples
- [x] Structured Output (Prompt package)
- [ ] Self-Consistency
- [x] Tree-of-Thoughts (Style variations)

---

## Related Prompts

- [Creative Brainstormer](./creative-brainstormer.md)
- [Infographic Planner](../17-Visualizations/infographic-planner.md)
