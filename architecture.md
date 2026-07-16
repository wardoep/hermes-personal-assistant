# Architecture

Hermes is the main assistant layer in my personal AI setup.

## Core Design

- Hermes acts as the primary conversational assistant
- Personal profile/context files define goals, preferences, and tone
- Skills extend it with reusable, task-specific workflows
- Memory retains useful long-term context between sessions
- Integrations connect it to tools I actually use day to day

## Current Implementation

- Obsidian integration for note organization and long-term knowledge support
- Personal "about me" context file for personalized responses
- Skill system for reusable task-specific workflows
- Memory system for persistent context
- Planning and productivity support, including Google Calendar-related workflows
- Hosted on a VPS/self-hosted environment, managed over SSH with CLI workflows

## Technical Areas This Project Exercises

- API and tool integrations
- CLI-based development workflows
- SSH management of remote systems
- Building and operating inside a self-hosted VPS environment
- Structuring assistant behavior through memory, skills, and context files

## Planned Direction

- More workflow automation
- More day-to-day life support
- More specialized subagents
- Additional assistant-connected tools and Discord bot workflows
