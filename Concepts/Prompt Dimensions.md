---
title: Prompt Dimensions
type: concept
---

# Prompt Dimensions

Most people interact with AI in one dimension: a text box. You type, it responds, you type again. Linear, sessionless, flat. Every conversation starts from zero.

Obsidian Synapses introduces a progression — from **1D** to **2D** to **3D** — that fundamentally changes what's possible between human and machine intelligence.

---

## 1D Prompt — The Text Box

```
You → [text] → AI → [text] → You
```

This is where most people live. A chat window. One message after another. The AI has no persistent memory, no spatial context, no sense of how your ideas relate to each other. It knows what you typed *right now* — nothing more.

**Limitations:**
- Linear — ideas must be expressed in sequence
- Sessionless — context dies when the chat closes
- Flat — no way to show relationships between concepts
- Repetitive — you re-explain context every time

The 1D prompt is a **corridor**. You can only move forward or backward.

---

## 2D Prompt — The Canvas

```
┌─────────────┐     ┌─────────────┐
│  Concept A  │────→│  Concept B  │
└─────────────┘     └─────────────┘
       │
       ↓
┌─────────────┐
│  Concept C  │
└─────────────┘
```

A `.canvas` file in Obsidian is a spatial map. Text nodes, file references, links, and images arranged in **two-dimensional space** with edges connecting them.

When an agent reads a canvas, it doesn't just see text — it sees **topology**. Which ideas are close together. What connects to what. Where the clusters form. This spatial arrangement is information that **cannot be expressed in linear text**.

The 2D prompt is a **room**. You can move in any direction. You can see relationships at a glance.

**What changes:**
- Spatial arrangement carries meaning (proximity = relatedness)
- Edges show explicit relationships between nodes
- An agent can read the canvas JSON and understand structure, not just content
- Multiple threads coexist without competing for sequence

Open [[Examples/My First Canvas]] to build one yourself.

---

## 3D Prompt — The Nested Canvas

```
┌─────────────────────────────────────┐
│  Canvas A                           │
│  ┌───────────┐     ┌─────────────┐  │
│  │  Note 1   │────→│  Canvas B ──┼──┼──→ [another spatial world]
│  └───────────┘     └─────────────┘  │
│       │                              │
│       ↓                              │
│  ┌───────────┐                       │
│  │  Note 2   │                       │
│  └───────────┘                       │
└─────────────────────────────────────┘
```

A canvas can contain a **file node** that points to another canvas. When you open that node, you enter a new spatial world — with its own nodes, edges, and relationships. This is **depth added to space**.

The 3D prompt is a **building**. Each floor is a canvas. You move horizontally within a floor and vertically between floors. An agent navigating this structure understands not just what's *next to* something, but what's *inside* it.

**What changes:**
- Hierarchy without rigidity — depth is chosen, not imposed
- Complex systems decompose naturally (overview canvas → detail canvas → sub-detail canvas)
- An agent can zoom in and out, following the nesting to find the right level of detail
- Your knowledge system gains **depth** — the missing dimension in flat file systems

Open [[Examples/Nested Canvas]] to experience it.

---

## The Progression in Practice

| Dimension | Tool | What the Agent Sees | Metaphor |
|-----------|------|--------------------| ---------|
| **1D** | Chat box | Sequence of text | Corridor |
| **2D** | `.canvas` | Spatial topology | Room |
| **3D** | Nested `.canvas` | Spatial topology + depth | Building |

The entire [[Obsidian Synapses]] methodology is built on this progression. You start with notes (1D building blocks), arrange them on canvases (2D maps), and nest canvases inside canvases (3D structures). The agent — reading through `.cursorrules` and the vault context — navigates all three dimensions.

This is what separates a [[Concepts/The Mind Garden|mind garden]] from a folder tree. And it's the practical expression of [[Concepts/Dracomancy|Dracomancy]] — raw chaotic input, transmuted through spatial arrangement, becoming a living system that compounds.

---

## Try It Yourself

1. Start with [[Examples/My First Note]] — a 1D building block with `[[wikilinks]]`
2. Move to [[Examples/My First Canvas]] — arrange ideas in 2D space
3. Finish with [[Examples/Nested Canvas]] — add depth by nesting canvases

Then ask the agent: *"Create a canvas about [your topic] and link it to a new note."* Watch the dimensions unfold.
