---
name: winq-social
description: Use when the person wants to plan, write, draft, schedule or review social media posts, check how posts performed, or find images in their Winq workspace.
---

# Working with Winq

Winq is a team tool for planning, writing and scheduling social media posts. The `winq` MCP server acts as the signed-in person, with their role in each workspace.

## Order of calls

1. `list_workspaces` first. Every other tool takes a workspace slug; if there's more than one, ask which.
2. Before writing: `get_brand_voice` (tone and the team's remembered preferences) and `list_channels` (which accounts are connected and each platform's character limit).
3. When planning: `get_insights` and `get_best_times` to pick topics and times that have worked.

## Writing posts

- `create_draft` saves a draft only. Nothing is published. Drafts are the default.
- Use per-platform text when one version won't fit every channel (X counts links as 23 characters; LinkedIn and Facebook allow long posts).
- To attach images or videos, find them with `search_files` and pass their ids as `file_ids`. To add a new file, use `upload_file` (≤15 MB, base64) or `start_file_upload` + `finish_file_upload` (≤250 MB).

## Scheduling is publishing

`schedule_post` publishes publicly to real accounts at the chosen time. Always show the person the final text, channels and time and get an explicit yes before calling it. Times without an offset are read in the workspace's time zone.

## Checking results

`list_posts` and `get_post` show status and per-channel delivery; `get_post_insights` gives one post's numbers against that channel's usual. Insights come from stored snapshots, so very recent posts may not have numbers yet.
