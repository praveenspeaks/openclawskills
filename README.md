# OpenClaw Skills

A collection of skills for OpenClaw AI agents. These are modular, reusable capabilities that extend your agent's functionality.

## Quick Start

### Creating a New Skill

1. Copy the template:
   ```bash
   cp -r skill-template my-skill
   cd my-skill
   ```

2. Update `skill.json` with your skill's info

3. Implement your logic in `index.ts`

4. Test and publish!

### Installing Skills

```bash
# Using clawhub CLI
npx clawhub@latest install skill-name

# Or manually copy to your agent's skills folder
cp -r my-skill /path/to/openclaw/skills/
```

## Skill Structure

```
my-skill/
├── skill.json          # Manifest - name, version, tools, permissions
├── index.ts            # Main implementation
├── schema.json         # Configuration schema (optional)
├── README.md           # Documentation
└── tests/              # Tests (optional)
    └── index.test.ts
```

## Available Examples

### Basic Examples

| Skill | Description | Permissions |
|-------|-------------|-------------|
| [weather-skill](examples/weather-skill) | Get weather from OpenWeatherMap | `http:request` |
| [todo-skill](examples/todo-skill) | Todo list with persistent storage | `fs:read`, `fs:write` |
| [file-manager-skill](examples/file-manager-skill) | Read/write files | `fs:read`, `fs:write`, `fs:delete` |

### Production Skills

| Skill | Description | Permissions |
|-------|-------------|-------------|
| [cinematic-script-writer](skills/cinematic-script-writer) | 🎬 Create cinematic scripts with camera angles, prompts for AI video tools, YouTube metadata | `memory:read`, `memory:write` |

## Skill Manifest (skill.json)

```json
{
  "name": "my-skill",
  "version": "1.0.0",
  "description": "What this skill does",
  "author": "Your Name",
  "entry": "index.ts",
  "config": {
    "schema": "schema.json"
  },
  "permissions": ["fs:read", "http:request"],
  "tools": [
    {
      "name": "doSomething",
      "description": "Does something useful"
    }
  ]
}
```

### Permissions

Skills must declare what they need access to:

- `fs:read` - Read files
- `fs:write` - Write files
- `fs:delete` - Delete files
- `http:request` - Make HTTP requests
- `memory:read` - Read from agent memory
- `memory:write` - Write to agent memory

## Context API

Skills receive a `context` object with:

```typescript
interface SkillContext {
  userId: string;           // Current user ID
  sessionId: string;        // Current session ID
  memory: MemoryStore;      // Persistent key-value storage
  logger: Logger;           // Logging utilities
  http: HttpClient;         // HTTP client (if http:request permission)
}
```

### Memory Store

```typescript
await context.memory.set('key', value);
const value = await context.memory.get('key');
await context.memory.delete('key');
```

### Logger

```typescript
context.logger.debug('Debug message');
context.logger.info('Info message');
context.logger.warn('Warning');
context.logger.error('Error!');
```

## Writing a Skill

```typescript
// index.ts
interface MyConfig {
  apiKey?: string;
}

interface SkillContext {
  memory: MemoryStore;
  logger: Logger;
}

export class MySkill {
  constructor(private config: MyConfig, private context: SkillContext) {}

  async doSomething(input: string): Promise<string> {
    this.context.logger.info(`Doing something with: ${input}`);
    
    // Your logic here
    const result = `Processed: ${input}`;
    
    // Store in memory
    await this.context.memory.set('lastInput', input);
    
    return result;
  }
}

export default function createSkill(config: MyConfig, context: SkillContext) {
  return new MySkill(config, context);
}
```

## Publishing to ClawHub

Coming soon! For now, share skills via GitHub.

## License

MIT
