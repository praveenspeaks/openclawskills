# 🎬 OpenClaw Skills - Cinematic Script Writer

[![CI](https://github.com/yourusername/openclawskills/actions/workflows/ci.yml/badge.svg)](https://github.com/yourusername/openclawskills/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue.svg)](https://www.typescriptlang.org/)

> Professional cinematic script generation for AI video creation with character consistency, comprehensive cinematography knowledge, and Google Drive integration.

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎥 **175+ Cinematography Techniques** | Camera angles, movements, shots, lighting, composition |
| 👤 **Character Consistency** | Reference sheets ensuring same appearance across all shots |
| 🗣️ **Voice Consistency** | Speech profiles for consistent dialogue |
| 🏛️ **Environment Consistency** | Era-appropriate architecture, clothing, props |
| 🚫 **Anachronism Detection** | Validates no modern elements in historical settings |
| 💾 **Google Drive Integration** | Auto-save all content to organized folders |
| 📺 **YouTube Metadata** | Titles, descriptions, tags for upload |

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/openclawskills.git
cd openclawskills

# Install dependencies
npm install

# Build
npm run build
```

### Basic Usage

```typescript
import { CinematicScriptWriter } from './skills/cinematic-script-writer';

const skill = new CinematicScriptWriter(config, context);

// 1. Create story context
const kutilContext = await skill.createContext(
  "Kutil's Adventure",
  "A cursed rakshasa's journey",
  [{
    name: "Kutil",
    description: "Cute purple rakshasa",
    personality: "Mischievous but kind",
    appearance: "Purple fur, small horns, golden eyes",
    role: "protagonist"
  }],
  "Ramayana Era",
  "Ancient India",
  "Lanka",
  "short",
  "comedy",
  "All ages",
  "Pixar 3D style"
);

// 2. Generate story ideas
const ideas = await skill.generateStoryIdeas(kutilContext.id, 3);

// 3. Create script
const script = await skill.createCinematicScript(
  kutilContext.id,
  ideas[0].id,
  ideas[0]
);

// 4. Connect Google Drive & Save
await skill.connectGoogleDrive(authCode);
await skill.saveScriptToStorage(ideas[0].title, kutilContext.id, script.id);
```

## 📁 Repository Structure

```
openclawskills/
├── 📁 skill-template/              # Template for creating new skills
│   ├── index.ts
│   ├── skill.json
│   └── README.md
│
├── 📁 examples/                    # Example skills
│   ├── weather-skill/
│   ├── todo-skill/
│   └── file-manager-skill/
│
├── 📁 skills/
│   └── 📁 cinematic-script-writer/ # Main skill
│       ├── index.ts                # Main implementation (60KB)
│       ├── cinematography-db.ts    # 175+ techniques
│       ├── cinematography-api.ts   # Unified API
│       ├── lighting-db.ts          # Lighting & composition
│       ├── visual-styles-db.ts     # Visual aesthetics
│       ├── consistency-system.ts   # Character/voice/env consistency
│       ├── prompt-builder.ts       # Consistent prompts
│       ├── storage-adapter.ts      # Google Drive/local storage
│       ├── storage-manager.ts      # File organization
│       ├── EXAMPLE-KUTIL.md        # Complete Kutil example
│       ├── EXAMPLE-CONSISTENCY.md  # Consistency examples
│       └── EXAMPLE-STORAGE.md      # Storage examples
│
├── 📄 package.json
├── 📄 tsconfig.json
├── 📄 LICENSE
└── 📄 README.md
```

## 🎥 Cinematography Database

| Category | Count | Examples |
|----------|-------|----------|
| **Camera Angles** | 20+ | eye-level, low-angle, dutch-angle, bird-eye, POV |
| **Camera Movements** | 20+ | dolly, crane, gimbal, rack-focus, snorricam |
| **Shot Types** | 25+ | extreme-wide, close-up, insert, silhouette |
| **Lighting** | 30+ | three-point, chiaroscuro, god-rays, neon |
| **Composition** | 20+ | rule-of-thirds, golden-ratio, leading-lines |
| **Color Grading** | 20+ | teal-orange, noir, vintage, dayglow |
| **Visual Styles** | 25+ | Pixar-3D, anime, film-noir, indian-miniature |
| **Genre Guides** | 15+ | horror, comedy, action, romance, sci-fi |

## 💾 Google Drive Integration

Save your entire project organized in folders:

```
📁 Story Title/
├── 00_INDEX.md                    # Navigation
├── 01_SCRIPT_README.md            # Human-readable script
├── 02_IMAGE_PROMPTS.md            # AI generation prompts
├── 03_CHARACTER_REFERENCES.md     # Design guides
├── 04_VOICE_GUIDELINES.md         # Dialogue guides
├── 05_YOUTUBE_METADATA.md         # Upload info
└── 99_CONTEXT_INFO.md             # Background
```

```typescript
// Connect to Google Drive
const auth = await skill.connectGoogleDrive();
// Visit auth.authUrl, authorize, paste code
await skill.connectGoogleDrive(userAuthCode);

// Save everything
const result = await skill.saveScriptToStorage(
  "Story Title",
  contextId,
  scriptId
);
console.log(result.shareLink); // Google Drive link
```

## 🎯 Consistency System

### Character Consistency
```typescript
// Create detailed character reference
const ref = skill.createCharacterReference(
  "kutil-id",
  "Kutil",
  "Purple fur, small horns, golden eyes...",
  "Ramayana Era",
  "pixar-3d"
);

// Build consistent prompts
const prompt = skill.generateCharacterConsistencyPrompt("kutil-id");
// Ensures same appearance in every shot
```

### Voice Consistency
```typescript
const voice = skill.createVoiceProfile(
  "kutil-id",
  "Kutil",
  "mischievous, determined",
  "young-adult",
  "protagonist"
);

const guidelines = skill.generateVoiceGuidelines("kutil-id");
// Get pitch, speed, catchphrases for consistent dialogue
```

### Environment Validation
```typescript
// Validates no anachronisms
const result = skill.validatePrompt(
  "Kutil wearing sunglasses", // ❌
  ["kutil-id"],
  contextId
);
// Error: "glasses does not belong in Ramayana Era"
```

## 📚 Documentation

- **[EXAMPLE-KUTIL.md](skills/cinematic-script-writer/EXAMPLE-KUTIL.md)** - Complete Kutil story workflow
- **[EXAMPLE-CONSISTENCY.md](skills/cinematic-script-writer/EXAMPLE-CONSISTENCY.md)** - Consistency system guide
- **[EXAMPLE-STORAGE.md](skills/cinematic-script-writer/EXAMPLE-STORAGE.md)** - Google Drive storage guide

## 🛠️ Development

```bash
# Install dependencies
npm install

# Run tests
npm test

# Build
npm run build

# Lint
npm run lint

# Fix lint issues
npm run lint:fix
```

## 🧪 Testing

### Unit Tests
```bash
npm test
```

### Manual Testing
```typescript
// Test cinematography
const angle = skill.getCameraAngle('low-angle');
console.log(angle.emotionalImpact); // "Power, dominance, heroism"

// Test consistency
const validation = skill.validatePrompt(
  "Kutil with smartphone",
  [charId],
  contextId
);
console.log(validation.errors); // ["Anachronism detected..."]
```

## 📦 Publishing to ClawHub

### 1. Prepare Package

```bash
# Ensure version is updated in skill.json
# Update CHANGELOG.md
# Commit all changes
git add .
git commit -m "v1.3.0 - Add Google Drive storage"
git push origin main
```

### 2. Create GitHub Release

1. Go to GitHub → Releases → Draft New Release
2. Tag: `v1.3.0`
3. Title: `v1.3.0 - Google Drive Storage & Consistency`
4. Description: Copy from CHANGELOG.md
5. Publish Release

### 3. Submit to ClawHub

Visit [https://clawhub.ai/publish](https://clawhub.ai/publish) and provide:

```yaml
# Required Information
name: cinematic-script-writer
version: 1.3.0
description: Professional cinematic script generation with consistency
repository: https://github.com/yourusername/openclawskills
license: MIT
entry: skills/cinematic-script-writer/index.ts

# Tags
tags:
  - creative
  - video
  - script
  - cinematography
  - consistency
  - google-drive

# Permissions
permissions:
  - memory:read
  - memory:write
  - http:request
```

Or use ClawHub CLI (if available):
```bash
npx clawhub publish
# Follow prompts
```

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

MIT License - see [LICENSE](LICENSE) file.

## 🙏 Acknowledgments

- OpenClaw community
- Contributors to cinematography techniques
- Indian art and mythology resources

---

**Made with ❤️ for AI storytelling**
