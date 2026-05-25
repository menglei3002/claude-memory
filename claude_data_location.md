---
name: claude-data-location
description: Claude data and work should be stored on D drive due to C drive space constraints
metadata: 
  node_type: memory
  type: user
  originSessionId: 0dd93adf-75e5-4704-980e-4880133b7c07
---

User wants all Claude Code data (config, history, sessions, plugins, projects, etc.) stored at `D:\AI\ClaudeWork\.claude\` instead of the default `C:\Users\Administrator\.claude\`. C drive is low on space.

The migration approach uses a Windows directory junction:
- Real data: `D:\AI\ClaudeWork\.claude\`
- Junction at: `C:\Users\Administrator\.claude` → `D:\AI\ClaudeWork\.claude`
- Migration script: `D:\AI\ClaudeWork\migrate.bat`

User may also want future project work under `D:\AI\` (e.g., `d:\AI\ai-video\`).
