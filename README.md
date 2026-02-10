# 🎬 Cinematic Script Writer Skill

[![CI](https://github.com/yourusername/openclawskills/actions/workflows/ci.yml/badge.svg)](https://github.com/yourusername/openclawskills/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue.svg)](https://www.typescriptlang.org/)

> Professional cinematic script generation for AI video creation with character consistency, comprehensive cinematography knowledge, and Google Drive integration.

## 🚀 Two Ways to Use This Skill

### Option 1: Import from GitHub (Recommended)

ClawHub can import directly from this GitHub repository:

1. Make sure this repo is **public**
2. Go to https://clawhub.ai/import
3. Enter: `https://github.com/YOUR_USERNAME/openclawskills`
4. Click **"Detect"** - it will find `SKILL.md` automatically
5. Fill in the details and publish

### Option 2: Upload Folder

1. Download the `clawhub-upload/` folder
2. Go to https://clawhub.ai/upload
3. Upload the folder
4. Fill in details and publish

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

## 📁 Repository Structure

```
openclawskills/
├──
├── SKILL.md                    ← ClawHub detects this automatically
├──
├── 📁 skills/
│   └── 📁 cinematic-script-writer/  # Main skill
│       ├── SKILL.md                 # Skill documentation
│       ├── index.ts                 # Main implementation
│       ├── skill.json               # Tool definitions
│       ├── cinematography-*.ts      # Camera techniques
│       ├── consistency-*.ts         # Consistency system
│       ├── storage-*.ts             # Storage system
│       └── EXAMPLE-*.md             # Usage examples
│
├── 📁 clawhub-upload/          ← Ready-to-upload folder
│   └── (all skill files for manual upload)
│
├── 📄 README.md                # This file
├── 📄 SETUP-GUIDE.md           # Complete setup guide
└── 📄 CLAWHUB-UPLOAD-GUIDE.md  # Upload instructions
```

## 📊 Skill Statistics

| Metric | Value |
|--------|-------|
| **Total Files** | 38 |
| **Code Size** | ~320KB |
| **TypeScript Files** | 13 |
| **Documentation** | 7 guides |
| **Tools** | 55 methods |
| **Cinematography Techniques** | 175+ |

## 🛠️ Development

```bash
# Install dependencies
npm install

# Build
npm run build

# Test
npm test

# Lint
npm run lint
```

## 📦 Publishing to ClawHub

### Method 1: GitHub Import (Easiest)

1. **Push to GitHub** (make repo public):
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/openclawskills.git
   git push -u origin main
   ```

2. **Import to ClawHub**:
   - Go to https://clawhub.ai/import
   - Enter: `https://github.com/YOUR_USERNAME/openclawskills`
   - Click **Detect**
   - Fill in:
     - Slug: `cinematic-script-writer`
     - Display name: `Cinematic Script Writer`
     - Version: `1.3.0`
     - Tags: `creative, video, script, cinematography, consistency`
   - Click **Publish**

### Method 2: Manual Upload

See [CLAWHUB-UPLOAD-GUIDE.md](CLAWHUB-UPLOAD-GUIDE.md)

## 📚 Documentation

- [SETUP-GUIDE.md](SETUP-GUIDE.md) - Complete setup and testing guide
- [CLAWHUB-UPLOAD-GUIDE.md](CLAWHUB-UPLOAD-GUIDE.md) - ClawHub upload instructions
- [skills/cinematic-script-writer/EXAMPLE-KUTIL.md](skills/cinematic-script-writer/EXAMPLE-KUTIL.md) - Complete Kutil example
- [skills/cinematic-script-writer/EXAMPLE-CONSISTENCY.md](skills/cinematic-script-writer/EXAMPLE-CONSISTENCY.md) - Consistency guide
- [skills/cinematic-script-writer/EXAMPLE-STORAGE.md](skills/cinematic-script-writer/EXAMPLE-STORAGE.md) - Storage guide

## 🔧 Requirements

- Node.js 18+
- TypeScript 5.0+
- OpenClaw Agent with memory permissions

## 📄 License

MIT License - see [LICENSE](LICENSE)

---

**Made for OpenClaw** 🦞
