---
title: Workshop Obsidian + Agents — Master Plan (Package & Repository)
type: workshop-master-plan
status: active
language: en
owner: Stefano Mastella
event_date: 2026-04-15
context: Ipê Village / Luma — Obsidian Synapses
related_canvas: "[[Workshop Obsidian + Agents.canvas]]"
related_event_doc: "[[Workshop Obsidian + Agentes.md]]"
---

# Workshop + Repository Master Plan

**Single source of truth** for delivering the Apr 15, 2026 workshop package: starter vault, agent-agnostic context, multi-IDE setup, Antigravity validation, and live **Ipê Journalist** demo.

---

## 1. Executive summary

| Item | Decision |
|------|----------|
| **Positioning** | **Generic-first** package: any IDE agent consumes the same [Context Contract](#5-context-contract-agent-agnostic). |
| **Flagship example** | **Ipê Journalist + `ipe-news-shared`**: mature, daily-tested Obsidian + Cursor editorial system (reference case, not the only architecture). |
| **Workshop structure** | **Part 1 — Theory** → **Part 2 — Live end-to-end** Ipê Journalist run in the shared vault. |
| **Primary artifact** | This note + folder `Arquivo/Workshop-Package-Context/` (`00`–`04` markdown files). |

---

## 2. Scope & non-scope (v1 — by Apr 15)

### In scope

- Starter **Ipê-oriented** vault (or documented subset) ready to clone: structure, hub notes, link to context files.
- **Portable prompts** and rules that work without assuming Cursor-only features.
- **Setup guides** via Context Contract + **minimal per-tool adapters** (Cursor, TRAE, Claude Code, Antigravity).
- **Antigravity plug-and-play validation** (fresh profile / clean machine protocol; pass/fail recorded).
- **Live demo script** for full Ipê Journalist pipeline (see §8).
- Master plan sections: deliverables, risks, **Apr 12–15 timeline**, launch-day runbook.

### Out of scope for v1 (backlog)

- Draco Network site launch (track on canvas checklist only).
- Replit-generated slide deck (optional; narrate from thesis card + this doc if needed).
- Training participants on paid API keys unless listed as prerequisite.

---

## 3. Workshop narrative spine

### Part 1 — Theory (~30–40 min; adjust to slot)

1. **Desktop / folder metaphor** — Why hierarchical “office simulation” constrains both human thinking and what an agent can safely infer. Bridge: Ted Nelson, graphs, canvases, **intentional arrangement** (Synapses idea).
2. **Karpathy-style compiler loop** — Raw captures → **compile** into structured markdown / ledgers → **agents act** on stable ground truth. Not one-off prompts: a **loop** that compounds. (Thread: [Karpathy status](https://x.com/karpathy/status/2039805659525644595); clipping: `Clippings/Karparthy on Obsidian and Agents.md`.)
3. **Personal → collective** — Personal second brain first; then **shared memory** and interoperable habits (continuity with **Ipê Mind Tree**).

**Opening optional**: Long-form thesis text on canvas (desktop metaphor, “cognitive gardens”, telebrain) — use as spoken framing, not required reading.

### Part 2 — Practice (live end-to-end)

- **Ipê Journalist** in `ipe-news-shared`: show real files — map, phases, edition pattern, canvas/newsroom behavior.
- Frame as **operations**: “This is what daily work looks like when the vault *is* the system.”
- Close: “You replicate the **shape** (context contract + tasks), not every secret key or pipeline flag.”

---

## 4. Canvas checklist → deliverables

Source: `Workshop Obsidian + Agents.canvas` (text node `e2f355f9ac928263`).

| # | Canvas item | Deliverable | Owner | Dependencies | Definition of done |
|---|-------------|-------------|--------|----------------|-------------------|
| 1 | Site Draco Network pronto | Backlog milestone only | TBD | — | Site live (post-v1). |
| 2 | Estudar tweet Karpathy + contrastar com nosso sistema | §3.2 + §10 + clipping notes | Host | Thread + clipping | Written “take vs leave” list in §10; verbal summary in Part 1. |
| 3 | Repositório Ipê Vault + pré-config agente | Cloneable repo / folder + `Workshop-Package-Context/*` | Host | Git policy, vault hygiene | New user: install Obsidian + IDE, open folder, read `00-START-HERE.md`, completes **Task A** in `03-TASKS.md` in ≤20 min (see success criteria). |
| 3a | Instruções para Cursor, TRAE, Claude Code, Antigravity | §7 + adapter files | Host | Tools installed | Each tool: adapter note **or** subsection with load instructions + same starter task. |
| 3b | Vault “ano passado + expandido” | Documented scope of starter vault | Host | What is redacted vs shipped | README or `01-CONTEXT.md` lists what ships and what stays private. |
| 3c | Testar Antigravity plug-and-play | §8 validation report | Host | Package freeze | Checklist §8.3 all **Pass** or documented **Fail** + workaround. |
| 4 | Parte teórica + texto card linkado | Part 1 outline + optional slides | Host | — | Theory deck optional; narrative covered live. |
| 4a | Slides Replit | Backlog | TBD | Replit | Deck exists OR explicitly dropped for v1. |

---

## 5. Context contract (agent-agnostic)

**Principle:** The agent reads the same markdown ground truth; only “how you attach workspace” changes per IDE.

| File | Purpose |
|------|---------|
| `Workshop-Package-Context/00-START-HERE.md` | Outcome, 5-minute quickstart, links to rest. |
| `Workshop-Package-Context/01-CONTEXT.md` | System purpose, glossary, **what is Ipê Journalist** (reference), vault boundaries. |
| `Workshop-Package-Context/02-RULES.md` | Do/don’t, safety, git/write boundaries, hallucination hygiene. |
| `Workshop-Package-Context/03-TASKS.md` | **Task A** (onboarding proof) + optional **Task B** (journalist-shaped exercise without secrets). |
| `Workshop-Package-Context/04-PROMPTS.md` | Role prompts + invocation patterns (paste into any agent chat). |

**Repository layout (target):**

```text
ipe-news-shared/   (or dedicated workshop repo root)
├── Arquivo/
│   ├── Workshop Obsidian + Agents - Master Plan.md   (this file)
│   ├── Workshop-Package-Context/
│   │   ├── 00-START-HERE.md
│   │   ├── 01-CONTEXT.md
│   │   ├── 02-RULES.md
│   │   ├── 03-TASKS.md
│   │   └── 04-PROMPTS.md
│   └── Agent-Adapters/
│       ├── README.md
│       ├── cursor.md
│       ├── trae.md
│       ├── claude-code.md
│       └── antigravity.md
└── (vault content — Obsidian)
```

---

## 6. Tool adapters (minimal)

Full per-tool steps live in `Arquivo/Agent-Adapters/`. Summary:

| Tool | Open as | Load context | Caveat |
|------|---------|--------------|--------|
| **Cursor** | Workspace = vault folder | Auto-read `.cursorrules` / rules; point agent to `Workshop-Package-Context/` | Your reference setup; mention pricing tiers. |
| **TRAE** | Project root = vault | Add `Workshop-Package-Context/*.md` to context / instructions | Confirm TRAE project-instructions UI. |
| **Claude Code** | Terminal `cd` to vault | `/read` or project docs; paste `00-START-HERE.md` summary | CLI-first; less ideal for non-dev audience. |
| **Antigravity** | Open project folder | Same files; use agent onboarding to “read project docs first” | Preview/free tier limits; verify Gemini vs other models. |

**Starter test (shared):** Complete **Task A** in `03-TASKS.md` and paste the artifact path into chat.

---

## 7. Ipê Journalist — live demo script (Part 2)

**Goal:** One coherent path through a system participants can *feel*, not every automation at once.

**Pre-flight:** Open Obsidian vault `ipe-news-shared`; IDE open on same folder; agent chat fresh.

1. **Orient** (2 min) — Open `Arquivo/Ipê-News-Mapa-Redação-e-Agência.md` (or equivalent hub). State: Phase 0 vs stages, ground truth = files not chat.
2. **Show structure** (3 min) — `Sala de Redação Ipe News - Shared.canvas`, `Edições Anteriores/`, `Arquivo/Ipe News - Banco de Notícias Cobertas.md`.
3. **Live agent** (15–25 min) — Pick *one* path aligned with workshop time:
   - **Path A:** Curate/add one item format → show database + canvas update rules.  
   - **Path B:** Phase 0 research pattern (if keys + time available): link gathering → draft MD.  
   - **Path C:** Run one pipeline stage you already trust (`ipe_edition_pipeline.py` mention only if demo machine ready).  
4. **Tie back** (3 min) — Compiler loop: raw → structured → agent. “Your package uses the same *contract*; Ipê is the *reference*.”

**Fallback if live fails:** Walk through saved screenshots or a pre-recorded screen capture; still narrate the same script.

---

## 8. Antigravity plug-and-play validation

### 8.1 Environment

- OS: Windows / macOS / Linux (pick primary workshop default).
- Fresh: new Antigravity profile OR machine without prior vault clone.
- Network: stable; Google account if required by Antigravity.

### 8.2 Steps (validator executes)

1. Install Obsidian + Antigravity per vendor docs.
2. Clone or copy workshop package to `~/workshop-ipe-vault` (path arbitrary).
3. Open folder as vault in Obsidian; confirm graph opens.
4. Open same folder as Antigravity project.
5. In agent: “Read `Arquivo/Workshop-Package-Context/00-START-HERE.md` and `03-TASKS.md`; complete Task A.”
6. Confirm artifact exists (file path in vault).
7. Repeat **Task A** with zero extra copy-paste from host (agent only uses repo files).

### 8.3 Pass / fail criteria

| ID | Check | Pass |
|----|--------|------|
| V1 | Obsidian opens vault without manual path fixes | Yes |
| V2 | Antigravity sees full tree | Yes |
| V3 | Task A completes without host intervention | Yes |
| V4 | Same instructions work on second cold run within 24h | Yes |

**Fail actions:** Document blocker in §11; add workaround to `Agent-Adapters/antigravity.md`; consider TRAE/Cursor as primary recommendation for workshop day.

---

## 9. Timeline — Apr 12 → Apr 15

| Date | Focus | Milestones |
|------|--------|------------|
| **Apr 12 (Sun)** | Freeze scope; context contract v0 | All `Workshop-Package-Context/*` drafted; adapter stubs exist. |
| **Apr 13 (Mon)** | Package + redaction | Starter vault subset decided; no secrets in repo; `.env` excluded. |
| **Apr 14 (Tue)** | Antigravity + dry run | §8.3 complete; demo script rehearsed once end-to-end. |
| **Apr 15 (Wed)** | Workshop | Morning: runbook check; execute Part 1 + Part 2. |

---

## 10. Karpathy thread — “take vs leave” (for this system)

**Take (aligned):**

- Treat the vault as **compiled knowledge**, not only chat logs.
- **Directory structure** as navigation for humans *and* agents (reply theme in thread).
- “Compiler” / **compounding loop**: outputs feed the next pass; avoid one-shot prompting.
- Optional: **ledger** of covered facts (Ipê: `Banco de Notícias Cobertas.md`).

**Leave or adapt:**

- Full “any modality dump → ingestion pipeline” product stack — you may use **segments** (e.g. markdown + canvas) rather than one giant ingestor.
- NotebookLM / hosted-only flows — not required; local-first Obsidian stays canonical.
- Fine-tuning / “knowledge into weights” — out of scope for workshop; mention as future frontier only.

---

## 11. Risk log & mitigations

| Risk | Mitigation |
|------|------------|
| Live demo breaks (API, path, network) | Fallback Path: pre-recorded clip + static files; shorten live segment. |
| Antigravity UX differs from Cursor | Over-invest in §8; emphasize Cursor + Obsidian as host’s **reference** stack. |
| Audience non-dev scared by CLI | Lead with Cursor/Antigravity GUI; Claude Code listed last. |
| Scope creep (full pipeline teach) | One path only in §7; defer “full pipeline” to post-event doc. |
| Secret leak in shared vault | Pre-package audit; gitignore `.env`; never paste keys during workshop. |

---

## 12. Launch-day runbook (Apr 15)

**T–60 min**

- [ ] Clone/pull latest package; open Obsidian + IDE on same folder.
- [ ] Run Task A locally (smoke test).
- [ ] Close unrelated projects; disable noisy notifications.

**T–15 min**

- [ ] Open canvas + hub MD in tabs.
- [ ] Test screen share: Obsidian graph + agent chat visible.

**T–0**

- [ ] Part 1 narrative: desktop → compiler loop → personal/collective.
- [ ] Part 2: follow §7; state where `Workshop-Package-Context` lives for attendees.

**Post-workshop**

- [ ] Publish link to repo / zip + one-line “open `00-START-HERE.md`”.

---

## 13. Success criteria (v1)

- New participant: Obsidian + **one** agent IDE → opens package → completes **Task A** in **≤20 minutes** without personalized help.
- Same core markdown contract works in **≥3** tools with **minimal** adapter steps (documented).
- Antigravity cold run: §8.3 passes OR blockers documented with workaround.
- Workshop **connects** Part 1 themes to Part 2 Ipê Journalist demo without conceptual jump.

---

## 14. References

- Canvas checklist & thesis card: `Workshop Obsidian + Agents.canvas`
- Event copy & blocks: `Workshop Obsidian + Agentes.md`, `Descrição Oficial Luma.md`
- Karpathy clipping: `Clippings/Karparthy on Obsidian and Agents.md`
- Journalist agent spec (canonical): personal vault `Obsidian Vault/Arquivo/Agentes/11-ipe-news-journalist.md` and repo copy under `ipe-news-shared` if present
