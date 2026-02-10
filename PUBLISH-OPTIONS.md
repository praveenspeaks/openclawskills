# 📦 Two Ways to Publish to ClawHub

Your skill is ready for ClawHub! You have **two options** to publish:

---

## Option 1: GitHub Import (Recommended) ⭐

ClawHub can import directly from your GitHub repository. It automatically detects `SKILL.md`.

### Step 1: Push to GitHub

```powershell
# 1. Create a public GitHub repository
#    Go to https://github.com/new
#    Name: openclaw-cinematic-writer
#    Make it PUBLIC (required for import)

# 2. Push your code
cd "D:\My Professional Projects\openclawskills"
git remote add origin https://github.com/YOUR_USERNAME/openclaw-cinematic-writer.git
git branch -M main
git push -u origin main
```

### Step 2: Import to ClawHub

1. Go to **https://clawhub.ai/import**

2. Enter your GitHub URL:
   ```
   https://github.com/YOUR_USERNAME/openclaw-cinematic-writer
   ```

3. Click **"Detect"**
   - ClawHub will find `SKILL.md` automatically
   - It will read the skill definition

4. Fill in the form:
   | Field | Value |
   |-------|-------|
   | **Slug** | `cinematic-script-writer` |
   | **Display Name** | `Cinematic Script Writer` |
   | **Version** | `1.3.0` |
   | **Tags** | `creative, video, script, cinematography, consistency, storage` |
   | **Changelog** | `Initial release with 175+ cinematography techniques` |

5. Click **"Publish skill"**

### ✅ Advantages of GitHub Import

- **Automatic updates**: Push new commits → ClawHub updates automatically
- **Version control**: Track all changes in Git
- **Collaboration**: Others can contribute via PRs
- **Backup**: GitHub stores your code safely

---

## Option 2: Manual Upload

Upload the prepared folder directly to ClawHub.

### Step 1: Use the Prepared Folder

The folder `clawhub-upload/` is ready with all files:

```
clawhub-upload/
├── SKILL.md              ← Required
├── index.ts              ← Main skill
├── skill.json            ← Tool definitions
├── schema.json           ← Config schema
├── package.json          ← Dependencies
└── (13 more files)
```

### Step 2: Upload to ClawHub

1. Go to **https://clawhub.ai/upload**

2. Fill in the form:
   | Field | Value |
   |-------|-------|
   | **Slug** | `cinematic-script-writer` |
   | **Display Name** | `Cinematic Script Writer` |
   | **Version** | `1.3.0` |
   | **Tags** | `creative, video, script, cinematography, consistency` |

3. Click **"Choose folder"**

4. Select `clawhub-upload/` folder

5. Click **"Publish skill"**

### ✅ Advantages of Manual Upload

- **Quick**: No GitHub setup needed
- **Simple**: Just upload and go
- **Private**: Don't need public GitHub repo

---

## 📋 Comparison

| Feature | GitHub Import | Manual Upload |
|---------|---------------|---------------|
| **Setup time** | 5 minutes | 2 minutes |
| **Need GitHub repo** | Yes | No |
| **Repo must be public** | Yes | N/A |
| **Auto-updates** | ✅ Yes | ❌ No |
| **Version control** | ✅ Git | ❌ Manual |
| **Collaboration** | ✅ PRs | ❌ No |
| **Best for** | Long-term | Quick publish |

---

## 🎯 Recommendation

### Use GitHub Import if:
- You plan to update the skill regularly
- You want version history
- You might collaborate with others
- You want automatic ClawHub updates

### Use Manual Upload if:
- You want to publish quickly
- You don't have a GitHub account
- This is a one-time publish
- You want to keep code private

---

## 📁 File Locations

### For GitHub Import

SKILL.md is at repo root:
```
openclawskills/
├── SKILL.md          ← ClawHub detects this
├── README.md
└── skills/
    └── cinematic-script-writer/
        ├── index.ts
        └── ...
```

### For Manual Upload

Upload this folder:
```
clawhub-upload/
├── SKILL.md          ← Required
├── index.ts
├── skill.json
└── ... (all 18 files)
```

---

## ✅ Pre-Flight Checklist

Both methods need these to be valid:

- [x] SKILL.md exists with proper content
- [x] index.ts has the main skill code
- [x] skill.json has 55 tool definitions
- [x] schema.json is valid JSON
- [x] No TypeScript errors (`npm run build` passes)
- [x] All files are included

---

## 🆘 Troubleshooting

### GitHub Import Issues

**"Could not detect SKILL.md"**
→ Make sure SKILL.md is at the repo root
→ Check the repo is public

**"Import failed"**
→ Check GitHub URL is correct
→ Ensure repo exists and is accessible

### Manual Upload Issues

**"SKILL.md is required"**
→ Make sure you're uploading the folder, not selecting files
→ Verify SKILL.md is inside the folder

**"Add at least one file"**
→ Upload the entire `clawhub-upload/` folder
→ Don't select individual files

---

## 🚀 Ready to Publish!

Your skill has:
- ✅ SKILL.md (detectable by ClawHub)
- ✅ Complete skill code
- ✅ 55 tools
- ✅ 175+ cinematography techniques
- ✅ Consistency system
- ✅ Storage integration
- ✅ Examples and documentation

**Choose your method and publish!**

- **GitHub Import**: https://clawhub.ai/import
- **Manual Upload**: https://clawhub.ai/upload

Good luck! 🎉
