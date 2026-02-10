---
name: cinematic-script-writer
version: 1.4.0
description: "Create professional cinematic scripts for AI video generation with character consistency and cinematography knowledge. Use when the user wants to write a cinematic script, create story contexts with characters, generate image prompts for AI video tools (Midjourney, Sora, Veo), or needs cinematography guidance (camera angles, lighting, color grading). Also use for character consistency sheets, voice profiles, anachronism detection, and saving scripts to Google Drive."
metadata:
  openclaw:
    emoji: "🎬"
    requires:
      bins:
        - node
    install:
      - id: npm-install
        kind: npm
        package: openclaw-skills
        bins:
          - cinematic-script
tags:
  - creative
  - video
  - script
  - cinematography
  - youtube
  - camera
  - lighting
  - consistency
  - character-design
  - voice
  - era-accurate
  - storage
  - google-drive
---

# Cinematic Script Writer

Create professional cinematic scripts for AI video generation with character consistency and cinematography knowledge.

## Installation

```bash
# Install via npm
npm install -g openclaw-skills

# Or install via OpenClaw CLI
openclaw skills install cinematic-script-writer
```

## CLI Usage

### Create a new story context
```bash
cinematic-script context create --name "My Story" --era "Ancient India" --period "Ramayana Era"
```

### List saved contexts
```bash
cinematic-script context list
```

### Generate story ideas
```bash
cinematic-script ideas --context "My Story" --count 3
```

### Create a full cinematic script
```bash
cinematic-script create --context "My Story" --idea 1 --output ./my-script.json
```

### Generate YouTube metadata
```bash
cinematic-script youtube --script ./my-script.json
```

### Save to Google Drive
```bash
cinematic-script save --script ./my-script.json --storage google-drive
```

### Export script
```bash
# Export as Markdown
cinematic-script export --script ./my-script.json --format markdown --output ./script.md

# Export as JSON
cinematic-script export --script ./my-script.json --format json --output ./script.json

# Export as plain text
cinematic-script export --script ./my-script.json --format text --output ./script.txt
```

### Character consistency tools
```bash
# Create character reference
cinematic-script character create --name "Kutil" --description "Purple rakshasa with golden eyes"

# Get character reference
cinematic-script character get --name "Kutil"

# Generate consistency prompt
cinematic-script character prompt --name "Kutil"
```

### Cinematography reference
```bash
# List all camera angles
cinematic-script cameras list

# Get specific camera angle
cinematic-script cameras get --angle "low-angle"

# List all shot types
cinematic-script shots list

# List all lighting techniques
cinematic-script lighting list

# Suggest setup for scene
cinematic-script suggest --scene "dialogue" --mood "dramatic"
```

## Features

- **Story Context Management**: Create and manage story settings, characters, and eras
- **Story Idea Generation**: Generate multiple story concepts with hooks and twists
- **Cinematic Script Writing**: Full scripts with camera angles, lighting, and shot types
- **Character Consistency**: Reference sheets and voice profiles for consistent characters
- **Environment Consistency**: Era-appropriate style guides and anachronism detection
- **YouTube Metadata**: Generate titles, descriptions, and SEO tags
- **Storage Integration**: Save to Google Drive or local storage
- **Export Options**: JSON, Markdown, or plain text formats

## When to Use

- Writing cinematic scripts or screenplays
- Creating stories with characters for animation/video
- Generating image/video prompts for AI tools (Midjourney, Sora, Veo, Runway)
- Getting cinematography guidance (camera angles, lighting, color grading)
- Maintaining character consistency across scenes
- Saving script projects to Google Drive

## Cinematography Reference

### Camera Angles

| Angle | Emotional Impact | Best For |
|-------|-----------------|----------|
| Eye-level | Connection, equality, neutrality | Dialogue, emotional moments |
| Low-angle | Power, dominance, heroism | Villain reveals, hero moments |
| High-angle | Vulnerability, weakness, overview | Defeat, establishing scale |
| Bird-eye | Insignificance, detachment, patterns | Epic scale, isolation |
| Worm-eye | Awe, grandeur, overwhelming presence | Monuments, giants, deities |
| Dutch angle | Unease, disorientation, tension | Chaos, dreams, horror |
| Overhead | Omniscience, surveillance | Table scenes, fight choreography |
| Shoulder-level | Intimate, casual, documentary feel | Walking conversations |
| Hip-level | Cowboy feel, casual tension | Westerns, standoffs |
| Knee-level | Childlike perspective, grounding | Children's stories, humility |

### Camera Movements

| Movement | Effect | Use For |
|----------|--------|---------|
| Static | Stability, observation | Contemplation, portraits |
| Pan | Revealing space | Following action horizontally |
| Tilt | Revealing height | Following vertical action |
| Dolly | Immersion, intimacy | Moving toward/away from subject |
| Truck | Following action | Side-to-side parallel movement |
| Crane | Epic scale, drama | Sweeping reveals, transitions |
| Handheld | Urgency, realism | Documentary, action, chaos |
| Steadicam | Smooth floating | Following through space, dreams |
| Zoom | Sudden focus, surprise | Dramatic emphasis, comedy |
| Rack-focus | Revealing connections | Shifting attention between subjects |

### Shot Types

| Shot | Framing | Emotional Impact |
|------|---------|-----------------|
| Establishing | Wide location | Sets scene, geography, time |
| Wide/Full | Subject + surroundings | Context, environment, scale |
| Medium | Waist up | Dialogue, body language |
| Close-up | Head/shoulders | Emotion, reaction, intimacy |
| Extreme close-up | Detail only (eyes, hands) | Intense emotion, symbolism |
| Over-shoulder | Past one subject to another | Conversation, perspective |
| POV | Character's view | Immersion, subjectivity |
| Insert | Object detail | Plot info, symbolism |
| Two-shot | Two subjects together | Relationship, tension |

### Lighting Techniques

| Technique | Mood | Best For |
|-----------|------|----------|
| Three-point | Professional, balanced | Dialogue, interviews |
| High-key | Happy, optimistic, bright | Comedy, commercials |
| Low-key | Dramatic, mysterious | Drama, horror, noir |
| Golden-hour | Romantic, nostalgic, magical | Romance, emotional moments |
| Blue-hour | Melancholic, mysterious | Urban, cityscapes |
| Chiaroscuro | Dramatic contrast | Art films, period pieces |
| Rim/backlight | Separation, ethereal | Silhouettes, divine presence |
| Practical | Realistic, natural | Candles, fires, lamps |
| God-rays | Divine, revelation | Spiritual moments, forests |
| Neon | Urban, futuristic | Cyberpunk, nightlife |

### Color Grading

| Style | Look | Genre |
|-------|------|-------|
| Teal-orange | Blockbuster cinematic | Action, sci-fi |
| Noir | High-contrast desaturated | Crime, mystery |
| Vintage/sepia | Warm, nostalgic | Period pieces, memory |
| Pastel | Soft, dreamy | Romance, coming-of-age |
| Bleach bypass | Desaturated, gritty | War, thriller |
| Cross-process | Surreal colors | Music videos, dreams |

## Image Prompt Format

When generating image prompts for AI tools:

```
[Shot type] [camera angle] of [subject doing action], [visual style] style,
[lighting technique], [composition rule], [color grading],
[era-appropriate details], [mood keywords], highly detailed, cinematic
```

Example:
```
Low-angle close-up of Kutil the purple rakshasa with mischievous golden eyes,
Pixar 3D style, dramatic underlighting with rim light, rule-of-thirds composition,
warm golden color grading, ancient Lanka palace background with ornate pillars,
playful yet mysterious mood, highly detailed, cinematic, 8k
```

## Output Structure

When saving a project, the following files are generated:

```
Story Title/
├── 00_INDEX.md           # Navigation
├── 01_SCRIPT_README.md   # Human-readable script
├── 02_IMAGE_PROMPTS.md   # All AI generation prompts
├── 03_CHARACTER_REFS.md  # Character design guides
├── 04_VOICE_GUIDES.md    # Dialogue consistency guides
├── 05_YOUTUBE_META.md    # Title, description, tags
└── 99_CONTEXT_INFO.md    # Story context and background
```

## Important Rules

1. **Always maintain character consistency** - include character's full visual description in every image prompt
2. **Never include anachronisms** - validate props, clothing, objects against the era
3. **Match cinematography to emotion** - use low angles for power, high angles for vulnerability
4. **Include both image and video prompts** - image prompts are static, video prompts describe motion
5. **Production-ready output** - every script should include enough detail for a team to produce it
6. **Respect the tone** - comedy needs comedic timing; drama needs longer holds on reactions

## License

MIT

## Author

Praveen Kumar
