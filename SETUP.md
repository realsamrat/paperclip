# Paperclip — Local Setup

## Start the server

```bash
cd "/Volumes/untitledcompanies/creative/sam/Open Intel/paperclip"
pnpm dev
```

Open: http://localhost:3100

## Agent Configuration

When you create agents in the UI, use these adapter configs:

---

### Claude Code Agent
- **Adapter:** `claude_local`
- **cwd:** `/Volumes/untitledcompanies/creative/sam/Open Intel/paperclip/agents/claude-ceo`
- **model:** `claude-sonnet-4-6` (or `claude-opus-4-6` for heavier tasks)
- **Auth:** Subscription login — no API key needed (`claude` is at `/Users/sam/.local/bin/claude`)
- **dangerouslySkipPermissions:** `true` for fully autonomous runs

---

### OpenClaw Agent
- **Adapter:** `openclaw`
- **cwd:** `/Volumes/untitledcompanies/creative/sam/Open Intel/paperclip/agents/openclaw-engineer`
- **openclaw binary:** `/Users/sam/Library/pnpm/openclaw`
- **Auth:** OpenClaw has its own auth (already logged in)

---

### Cursor Agent
- **Adapter:** `cursor_local`
- **cwd:** `/Volumes/untitledcompanies/creative/sam/Open Intel/paperclip/agents/cursor-designer`
- **cursor binary:** `/usr/local/bin/cursor`
- **Auth:** Cursor subscription (already logged in)

---

## Suggested First Company

1. Create company → give it a goal (e.g. "Build and ship X")
2. Create CEO agent → Claude Code adapter → cwd: `agents/claude-ceo`
3. Create Engineer agent → OpenClaw adapter → cwd: `agents/openclaw-engineer`
4. Create Designer/Frontend agent → Cursor adapter → cwd: `agents/cursor-designer`
5. Set monthly budgets per agent
6. Create first task under the company goal → assign to CEO
7. Hit go

## Fork

Source: https://github.com/paperclipai/paperclip
Your fork: https://github.com/realsamrat/paperclip
