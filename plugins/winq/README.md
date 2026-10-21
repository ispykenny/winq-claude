# Winq for Claude

![Winq](logo.png)

Plan, write and schedule your team's social posts from Claude, with your [Winq](https://winq.ai) workspace. Ask how last month's posts did, when your audience is around, or for a draft in your brand voice with a photo from your Files, and Claude does it in Winq as you.

## What's included

- The Winq MCP server at `https://api.winq.ai/mcp`. You sign in to Winq and approve access in your browser (OAuth); no keys are stored in this plugin or your config. Its tools cover workspaces, channels, posts, drafts, scheduling, insights, best times, brand voice and Files.
- A skill that tells Claude the order to call things in: workspaces first, then brand voice and channels before writing. Drafts are the default, and Claude always asks before scheduling, because scheduling publishes publicly to your connected accounts.

## What it sends where

The plugin only talks to Winq's server (`api.winq.ai`), as the signed-in person, with their role in each workspace. It runs nothing on your computer. Disconnect it any time from Integrations in Winq.

## Install in Claude Code

```
/plugin marketplace add ispykenny/winq-claude
/plugin install winq@winq
```

Then run `/mcp`, pick **winq** and sign in.

You need a Winq account. Privacy: https://winq.ai/privacy · Terms: https://winq.ai/terms · Support: hello@winq.ai
