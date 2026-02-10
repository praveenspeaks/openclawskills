CINEMATIC SCRIPT WRITER - CLAWHUB UPLOAD PACKAGE
================================================

Version: 1.3.0
Files: 16
Total Size: ~280KB

CONTENTS:
---------
SKILL.md              - Main skill documentation for ClawHub
index.ts              - Main skill implementation
skill.json            - Skill manifest with 55 tools
schema.json           - Configuration schema

CINEMATOGRAPHY:
--------------
cinematography-db.ts   - 175+ camera techniques
cinematography-api.ts  - Unified API
lighting-db.ts         - Lighting & composition
visual-styles-db.ts    - Visual aesthetics

CONSISTENCY:
-----------
consistency-system.ts  - Character/voice/env consistency
prompt-builder.ts      - Consistent prompt generation

STORAGE:
--------
storage-adapter.ts     - Google Drive/local adapters
storage-manager.ts     - File organization

DOCUMENTATION:
-------------
README.md              - Full documentation
EXAMPLE-KUTIL.md       - Kutil story example
EXAMPLE-CONSISTENCY.md - Consistency examples
EXAMPLE-STORAGE.md     - Storage examples

DEPENDENCIES:
------------
package.json           - NPM dependencies (uuid)

USAGE ON CLAWHUB:
----------------
1. Upload this folder to ClawHub
2. Set slug: "cinematic-script-writer"
3. Set display name: "Cinematic Script Writer"
4. Set version: "1.3.0"
5. Add tags: creative, video, script, cinematography, consistency, storage
6. Publish!

REQUIREMENTS:
------------
- OpenClaw Agent with memory:read, memory:write permissions
- Optional: http:request for Google Drive storage
