---
title: Obsidian Synapses
type: vault-entry-point
---
# Obsidian Synapses

The interfaces we inherited were designed to simulate an office inside a screen. Files in folders, documents on desktops, linear chat windows that forget everything the moment you close them. These structures were built for bureaucracy, not for thought.

**Obsidian Synapses** is a methodology for building something different: a living knowledge system where your notes, maps, and AI agents work together as a cognitive ecosystem. Instead of storing information in dead hierarchies, you arrange it with intention — spatially, relationally, organically. The way you structure your knowledge determines what an AI can understand about you and how faithfully it can act on your behalf.

The soul of this system is [[Concepts/Dracomancy|Dracomancy]] — the transmutation of raw, chaotic information into living technology. Not a productivity hack. An alchemical act.

---

## Vault Map

### Core Concepts

These are the ideas behind the system. Read them, link to them, build on them.

- [[Concepts/Dracomancy]] — Techné. The transformation of metal. Chaos is not the enemy — it's the fuel.
- [[Concepts/The Mind Garden]] — Why the office model is dead, and what replaces it.
- [[Concepts/Prompt Dimensions]] — The progression from 1D prompts (text) to 2D prompts (canvas) to 3D prompts (nested canvases).

### Hands-On Examples

Start here to learn by doing. Each one builds on the previous.

- [[Examples/My First Note]] — Create a simple note with `[[wikilinks]]`. See how connections form in the graph.
- [[Examples/My First Canvas]] — Arrange ideas spatially on a canvas. Your first 2D prompt.
- [[Examples/Nested Canvas]] — Embed a canvas inside another canvas. Welcome to the third dimension.

### Visual Maps

Open these in Obsidian to see spatial knowledge in action.

- [[Dracomancy.canvas]] — A visual map of alchemical transmutation: from raw material to living technology.
- [[Obsidian Synapses Workshop.canvas]] — The vault map as a canvas — a bird's-eye view of everything here.

### Reference Material

- [[Clippings/Karparthy on Obsidian and Agents]] — The thread that sparked a movement: Karpathy on knowledge compounding, compiler loops, and why directory structure is the key unlock for agents.

---

## Quick Start

### 1. Open in Obsidian

Open this folder as a vault in [Obsidian](https://obsidian.md/download). Press `Ctrl/Cmd + G` to open the **Graph View** — you'll see how every note connects to others through `[[wikilinks]]`. Click any node to navigate.

### 2. Open in Your Agentic IDE

Open this same folder in [Cursor](https://cursor.com), TRAE, Claude Code, or any AI-powered editor. If you're using Cursor, the agent **already has context** — it read the `.cursorrules` file automatically and knows how this vault works.

### 3. Build Something

Follow the [[Examples/My First Note|examples]] in order:
1. A note (`.md`) — the 1D building block
2. A canvas (`.canvas`) — spatial arrangement, the [[Concepts/Prompt Dimensions|2D prompt]]
3. A nested canvas — depth inside space, the [[Concepts/Prompt Dimensions|3D prompt]]

Then start creating your own. Ask the agent for help — that's what it's here for.

---

## For the Agent

> [!info] Agent Context
> You are inside an Obsidian vault called **Obsidian Synapses Workshop**. Your job is to help the user learn and build within this system.
>
> - **Files are `.md`** (Markdown notes with `[[wikilinks]]`) and **`.canvas`** (JSON spatial maps).
> - **Concepts** live in `Concepts/` — read them to understand what you're teaching.
> - **Examples** live in `Examples/` — guide users through these step by step.
> - When creating new content, **always add `[[wikilinks]]`** to existing notes. The graph should grow with every interaction.
> - Reference `.cursor/skills/json-canvas/SKILL.md` for canvas format and `.cursor/skills/obsidian-markdown/SKILL.md` for markdown syntax.
