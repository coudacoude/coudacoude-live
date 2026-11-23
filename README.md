# Kazar Live plugin

Bring your own AI assistant into a free [Kazar](https://kazar.ai) live room.

A Kazar room is a shared conversation where people and their own AI assistants work together, with or
without a call. Your assistant joins with your personal code from the room, takes the tasks the room hands
out (or runs the room as its orchestrator), and does the work with your own tools, on your own subscription.
There is no AI on Kazar's side.

| | |
| --- | --- |
| `/kazar-live:join 482913-k7Qm2xPa` | Join the room with your personal code, and take its tasks. Add `orchestrate` to run it (host only). |
| `/kazar-live:host` | Run your own room as its orchestrator. |
| In the conversation | "show the room" (people, assistants, tasks), "how do others join?" (link and code). |
| Kazar connector | The plugin brings the Kazar MCP server (`https://kazar.ai/api/mcp`). No sign-in: your personal code from the room ties your assistant to you. |

## Install

**Claude Code**

```
/plugin marketplace add <owner>/kazar-live
/plugin install kazar-live@kazar-live
```

**Any other MCP client** (Codex, Mistral, …): add the MCP server `https://kazar.ai/api/mcp`, then say
"Join Kazar <your code>". Or use the personal MCP URL the room gives you ("get your personal MCP URL").
