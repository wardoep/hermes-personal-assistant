# Hermes Personal Assistant

Design documentation for a self-hosted AI assistant system I built, run, and administer on my own Linux server.

## Overview

Hermes is my personal AI assistant: a conversational layer extended with context files, reusable skills, persistent memory, and integrations to the tools I use daily (Obsidian notes, Google Calendar). This repository is the design documentation for that system — the architecture, the features that exist today, and where it is heading. The assistant itself runs on a self-hosted VPS that I administer entirely over SSH, so the project is as much a systems and automation exercise as an AI one.

## Documentation in This Repo

| Document | Covers |
|---|---|
| [architecture.md](architecture.md) | Core design: assistant layer, context files, skills, memory, integrations, hosting |
| [features.md](features.md) | What is built and working today vs. what is in progress |
| [roadmap.md](roadmap.md) | Near/mid/long-term direction, including subagents and Discord workflows |

## System Design at a Glance

- **Assistant layer** — Hermes handles conversation and task execution
- **Context files** — a personal profile defines goals, preferences, and tone, so behavior is configured through versionable files rather than ad hoc prompting
- **Skills** — reusable, task-specific workflows instead of one-off instructions
- **Memory** — persistent context that survives across sessions
- **Integrations** — Obsidian for long-term notes, Google Calendar for planning
- **Infrastructure** — self-hosted on a VPS, managed over SSH with CLI-only workflows (see my [homelab-vps-setup](https://github.com/wardoep/homelab-vps-setup) repo for the underlying environment)

## Key Skills Demonstrated

- Systems design: separating configuration (context files), capabilities (skills), and state (memory)
- Linux server operation: the assistant is a real running service on a machine I maintain
- API and tool integration: connecting independent services into one working system
- Remote administration: SSH- and CLI-based management of a self-hosted environment
- Documentation discipline: architecture, feature status, and roadmap kept current as the system evolves

## What I Learned

- **Configuration belongs in files, not in your head.** Defining Hermes's behavior through a profile file, skill files, and memory means every behavior change is a file edit I can review and roll back — the same reason IT teams keep configs in version control instead of clicking through settings.
- **Running a service is different from building one.** Because Hermes lives on a server I administer over SSH, I deal with the operational side: is the environment up, did an update break something, where do I look when it misbehaves. That day-to-day maintenance taught me more Linux than the initial build did.
- **Integrations fail at the seams.** Connecting Obsidian and Google Calendar showed me that most problems live at the boundary between tools — authentication, paths, and assumptions each side makes. I learned to test each connection in isolation before blaming the system as a whole.
- **Separate "built" from "planned" honestly.** Keeping features.md split into Built vs. In Progress forces me to be precise about what actually works, which is the same discipline as accurate ticket notes: the next person (or future me) needs the real state, not the intended one.
- **Structure beats cleverness for reliability.** The biggest improvements to Hermes came from organizing skills and memory better, not from smarter prompts — a lesson that maps directly to IT work, where good structure and documentation outlast any individual fix.

## Status

Active project, in daily use. The documentation here is updated as the system evolves.

---
Built and documented by **Edward J. Penna** — [github.com/wardoep](https://github.com/wardoep)
