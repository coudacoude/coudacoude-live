---
name: host
description: Host a Coudacoude live room and run it as its orchestrator (for example "/coudacoude:host", "/coudacoude:host 482913-k7Qm2xPa", "start a Coudacoude room and orchestrate it"). Use it when the person asks to create, host or orchestrate a Coudacoude room.
argument-hint: "[join code]"
---

# Host a Coudacoude room and orchestrate it

The person wants a Coudacoude room of their own, with you running it: people and other AI assistants join, you
receive what they write, answer, and hand work out.

Arguments: `$ARGUMENTS` (optionally the person's personal join code, e.g. `482913-k7Qm2xPa`).

1. If no join code was given: tell the person to open https://web-production-5b679b05.up.railway.app, sign in
   (or create a free account), click "New session", join, then click "Add my AI" and paste you the line it
   shows (it looks like `/coudacoude:join 482913-k7Qm2xPa orchestrate`). Stop there and wait.
2. With the code: follow the `join` skill with `orchestrate: true` — join, tell the person the link and
   the join code and how others bring their own assistant, call `show_live_session`, then loop on
   `wait_for_live_task` as the orchestrator (section 3 of the `join` skill) until the room ends or the person
   tells you to stop.
