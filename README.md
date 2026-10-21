# Winq for Claude Code

Plan, write and schedule your team's social posts from Claude Code, with your [Winq](https://winq.ai) workspace.

## Install

```
/plugin marketplace add ispykenny/winq-claude
/plugin install winq@winq
```

Then run `/mcp`, pick **winq** and sign in. Claude opens Winq in your browser to approve access; nothing is stored in this repo or your config.

Prefer no plugin? `claude mcp add --transport http winq https://api.winq.ai/mcp`

## What's included

- The Winq MCP server (`https://api.winq.ai/mcp`, OAuth): workspaces, channels, posts, drafts, scheduling, insights, best times, brand voice and Files.
- A skill that teaches Claude the order to call things in, and to always ask before scheduling (scheduling publishes publicly).

## Using it on claude.ai

Settings → Connectors → Add custom connector → `https://api.winq.ai/mcp`.

Privacy: https://winq.ai/privacy · Terms: https://winq.ai/terms
