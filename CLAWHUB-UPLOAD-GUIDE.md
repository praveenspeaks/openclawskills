# ClawHub Upload Guide

## ✅ Your Skill is Ready for ClawHub!

The folder `clawhub-upload/` contains everything needed to publish your skill.

## 📁 Upload Package Contents

```
clawhub-upload/ (18 files, ~280KB)
├──
├── SKILL.md                    ← REQUIRED: Main documentation
├── index.ts                    ← REQUIRED: Main skill code
├── skill.json                  ← REQUIRED: Tool definitions
├── schema.json                 ← REQUIRED: Config schema
├── package.json                ← Dependencies
├──
├── cinematography-*.ts         ← Camera techniques (3 files)
├── lighting-db.ts              ← Lighting database
├── visual-styles-db.ts         ← Visual aesthetics
├── consistency-*.ts            ← Consistency system (2 files)
├── storage-*.ts                ← Storage system (2 files)
├──
├── README.md                   ← Full documentation
├── EXAMPLE-*.md                ← 3 example guides
└── README.txt                  ← Quick reference
```

## 🚀 How to Upload to ClawHub

### Step 1: Go to ClawHub

Visit: https://clawhub.ai/upload

### Step 2: Fill in the Form

| Field | Value |
|-------|-------|
| **Slug** | `cinematic-script-writer` |
| **Display Name** | `Cinematic Script Writer` |
| **Version** | `1.3.0` |
| **Tags** | `creative, video, script, cinematography, consistency, character-design, voice, storage, google-drive, youtube` |
| **Changelog** | Initial release with 175+ cinematography techniques, consistency system, and Google Drive storage |

### Step 3: Upload Files

1. Click **"Choose folder"** button
2. Select the `clawhub-upload/` folder
3. Wait for validation to complete
4. Click **"Publish skill"**

### Step 4: Wait for Review

- ClawHub will review your submission
- Usually takes 1-3 days
- You'll receive email notification

## 📋 Validation Checklist

Before uploading, verify:

- [x] SKILL.md exists and is complete
- [x] index.ts is present (main skill code)
- [x] skill.json has proper structure
- [x] schema.json is valid JSON
- [x] package.json lists dependencies
- [x] All TypeScript files compile (npm run build passed)
- [x] No syntax errors

## 🔍 What ClawHub Validates

✅ **SKILL.md** - Must exist with description, features, usage  
✅ **index.ts** - Main entry point for the skill  
✅ **skill.json** - Tool definitions and metadata  
✅ **schema.json** - Configuration validation  
✅ **File count** - At least one file besides SKILL.md  

## 📝 Skill.json Summary

Your skill.json includes:
- **Name**: cinematic-script-writer
- **Version**: 1.3.0
- **Tools**: 55 methods
- **Permissions**: memory:read, memory:write, http:request
- **Tags**: 13 tags

### Main Tools Categories:
1. **Context Management** (4 tools)
2. **Story Generation** (3 tools)
3. **Consistency** (10 tools)
4. **Cinematography** (20+ tools)
5. **Storage** (7 tools)

## 🎨 What Makes This Skill Special

### Unique Features:
1. **175+ Cinematography Techniques** - Camera, lighting, composition
2. **Character Consistency** - Same appearance across all shots
3. **Voice Consistency** - Consistent dialogue patterns
4. **Anachronism Detection** - No modern items in historical settings
5. **Google Drive Integration** - Auto-save organized folders

### Use Cases:
- AI video generation (Midjourney, Sora, Veo)
- Comic/cartoon creation
- YouTube content creation
- Animation pre-production
- Storyboarding

## 📊 Skill Statistics

| Metric | Value |
|--------|-------|
| Total Files | 18 |
| Code Files | 11 TypeScript files |
| Documentation | 7 markdown files |
| Tools | 55 methods |
| Techniques | 175+ cinematography |
| Size | ~280KB |

## 🆘 Common Issues

### "SKILL.md is required"
→ Make sure SKILL.md is in the root of uploaded folder

### "Add at least one file"
→ Upload the entire `clawhub-upload/` folder, not individual files

### "Slug is required"
→ Use: `cinematic-script-writer` (lowercase, hyphens)

### "Display name is required"
→ Use: `Cinematic Script Writer` (title case)

## ✅ After Publishing

Once approved:

1. Your skill appears at: `https://clawhub.ai/skills/cinematic-script-writer`
2. Users can install with: `npx clawhub@latest install cinematic-script-writer`
3. You'll get analytics on usage
4. Can push updates with new versions

## 📦 Alternative: Create ZIP

If you need to upload as ZIP:

```powershell
# Navigate to clawhub-upload folder
cd "D:\My Professional Projects\openclawskills\clawhub-upload"

# Create ZIP
Compress-Archive -Path * -DestinationPath "../cinematic-script-writer-v1.3.0.zip"
```

Then upload the ZIP file to ClawHub.

## 🎯 Ready to Upload!

Your skill is production-ready. The `clawhub-upload/` folder contains everything ClawHub needs.

**Next step**: Go to https://clawhub.ai/upload and upload the `clawhub-upload/` folder!

Good luck! 🚀
