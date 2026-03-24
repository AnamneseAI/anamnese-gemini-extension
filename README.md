# Anamnese – Cloud Memory for Gemini CLI

Portable, secure cloud memory for any AI. Your facts, goals, tasks, and knowledge — synced everywhere, owned by you. Self-learning AI that gets better every conversation.

## Installation

```bash
gemini extensions install https://github.com/AnamneseAI/anamnese-gemini-extension
```

## First Use

Run the onboarding command to authenticate and set up your profile:

```
/anamnese:start
```

This will open your browser for OAuth login via Supabase. Once authenticated, Anamnese will guide you through setting up your profile.

## What You Get

### Memory (18 tools)

**Memory:** `save_memory`, `search_memories`, `update_memory`, `delete_memory`, `get_user_profile`

**Notes:** `save_note`, `search_notes`, `get_note`, `update_note`, `delete_note`

**Tasks:** `create_task`, `search_tasks`, `update_task`, `delete_task`

**Goals:** `save_goal`, `search_goals`, `update_goal`, `delete_goal`

### Proactive Capture

Anamnese captures information automatically as you chat — personal details, decisions, tasks, goals, and knowledge. No need to explicitly ask it to remember things.

### Self-Learning

The AI learns from your corrections and preferences. Over time, it gets better at anticipating what you want. Say "review your learnings" to see what it's picked up.

### Cross-App Sync

Your memory syncs across all AI apps that support Anamnese: Claude, ChatGPT, Claude Code, Cursor, Gemini CLI, and more. Your data is always yours — edit, delete, or export it at [anamneseai.app](https://anamneseai.app).

## Available Commands

| Command | Description |
|---------|-------------|
| `/anamnese:start` | Onboard, authenticate, and set up your profile |

## Development

To develop locally, link the extension from the repo directory:

```bash
gemini extensions link .
```

## How It Works

This extension connects to the Anamnese MCP server at `https://anamneseai.app/api/mcp` using Gemini CLI's native `httpUrl` support. Authentication is handled automatically — Gemini CLI detects the 401 response, discovers the OAuth endpoints, opens a browser for login, and manages token refresh.

No dependencies, no API keys, no manual configuration needed.

## License

MIT
