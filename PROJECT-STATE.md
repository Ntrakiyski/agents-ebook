# Project State and Handoff

This file is the durable handoff from the initial architecture session for the ebook. It records what has been decided, what must not be lost, what is intentionally still open, and what the next writing session should do.

---

# Project Goal

Build a project-driven ebook that helps readers move from basic AI usage to engineering complete AI systems.

The book should give the reader the **full picture first**, then build understanding **from the bottom to the top**:

```text
Model
  ↓
Prompt
  ↓
Context
  ↓
Tools
  ↓
Agent
  ↓
Harness
  ↓
Workflow
  ↓
Evals
  ↓
Autonomy
  ↓
Multi-Agent Systems
  ↓
Self-Improving Systems
  ↓
AI-Native Organizations
```

The goal is not to create a dictionary of AI terminology. The book should teach how the pieces connect and why each new layer exists.

---

# Original Topic Seed

The project began from the following desired concepts:

- Prompting
- Context Windows
- Tokens
- Projects / project context
- API Keys
- CLI
- MCP Servers
- `CLAUDE.md` / repository instruction files
- Slash Commands
- Model Routing
- Subagents
- Prompt Caching
- Git Worktrees
- Skills
- Hooks
- Harness Engineering
- Background Agents
- Headless Runs
- Parallel Agents
- Progressive Disclosure
- Eval-Driven Loops
- Orchestrator–Workers
- deep / extended reasoning ("Ultra Think"-style capability)
- Memory Consolidation
- Self-Improving Loops
- Tool Poisoning
- Self-Healing Agent Tests
- Agent Run CI/CD
- Agents Managing Agents
- Multi-Repo Orchestration

The final blueprint expands substantially beyond these topics while preserving all of them.

---

# Major Decisions Already Made

## 1. The book is systems-first, not product-first

Do not organize the curriculum around temporary products such as a specific coding assistant or provider.

Teach durable primitives first:

```text
Context
Memory
Tools
Skills
Hooks
Agents
Harnesses
Evals
Orchestration
```

Then use current products and frameworks as concrete implementations and comparisons.

The book should age around examples, not around principles.

## 2. One concept leads to one real build

The project was inspired by the idea **one skill = one project**.

For this book the stronger rule is:

> **One chapter → one capability → one real build → one measurable upgrade to the larger system.**

The reader should learn by building, breaking, inspecting, and evaluating the concept rather than reading theory followed by an optional exercise.

## 3. One evolving system connects the entire book

Working project name: **ATLAS**.

Early ATLAS is a raw model call. Final ATLAS is a production-grade, multi-agent, observable, governed, eval-driven, progressively self-improving AI engineering system.

The reader should be able to look back at the final system and recognize that they built every important layer themselves.

## 4. The book begins with principles

Before Part I, readers receive `CORE-PRINCIPLES.md`.

The principles are not introductory decoration. They are a persistent reasoning lens used throughout the book, similar to durable software-engineering principles.

## 5. The agent is only the visible surface

A major recurring idea is the AI-system iceberg.

Below the visible model/agent layer are:

- data
- integrations
- identity
- permissions
- runtime
- state
- evaluations
- security
- observability
- human oversight
- governance
- infrastructure
- economics
- reliability
- organizational ownership

The book must continuously expose these hidden layers.

## 6. The curriculum covers 15 dimensions

The detailed curriculum uses these dimensions:

1. Intelligence
2. Intent & Specification
3. Context & Knowledge
4. Execution & Agency
5. Runtime & Infrastructure
6. Reliability & Failure
7. Security, Identity & Trust
8. Product & Human Interaction
9. Workflow & Business Process
10. Learning & Adaptation
11. Operations & Observability
12. Economics & Value
13. Organization & Adoption
14. Governance, Law & Accountability
15. Evolution, Versioning & Portability

See `BOOK-BLUEPRINT.md` for the current 16-part / 66-chapter structure.

## 7. The seven-plane system map should remain visible

See `CONCEPTUAL-FRAMEWORKS.md`.

The seven planes are:

- Intent
- Intelligence
- Action
- Runtime
- Trust
- Operations
- Human

Business value surrounds the whole system.

## 8. Evidence is part of writing, not an appendix

Every meaningful technical claim should have evidence where appropriate.

Resources include:

- official documentation
- specifications
- papers
- repositories
- technical articles
- engineering blogs
- books
- videos / talks
- practitioners and people worth following
- channels / newsletters / podcasts
- production case studies
- datasets / benchmarks
- experiments performed in the chapter

Resources have two roles:

1. **Proof** — support the claims the book makes.
2. **Continuation** — show readers where to go deeper and how to stay current.

Follow `research/SOURCE-STANDARDS.md`.

## 9. Current claims must be dated; durable principles must be separated from examples

Anything involving current model prices, context windows, vendor capabilities, API behavior, framework features, product limits, or benchmarks is time-sensitive.

The book should distinguish:

```text
Durable principle
vs
Current implementation/example verified on a date
```

## 10. Evals are required before declaring improvement

A system is not "better" because a new design sounds more sophisticated.

The project should measure changes in:

- task success
- quality
- latency
- cost
- reliability
- security
- human review burden
- business outcome

---

# Mandatory Chapter Method

Unless there is a strong editorial reason to deviate, technical chapters follow this progression:

1. **The Problem** — show the practical limitation that creates the need for the concept.
2. **What We Are Building** — show the concrete project before theory.
3. **Mental Model** — give the simplest correct explanation.
4. **Build** — implement progressively.
5. **Break It** — deliberately expose the naive implementation's limitations.
6. **Under the Hood** — inspect prompts, context, tokens, tool calls, state, traces, routing, etc.
7. **Production Lens** — examine data, security, reliability, oversight, governance, economics, and integration implications.
8. **Evaluate** — prove what improved and what did not.
9. **ATLAS Upgrade** — record the permanent capability now added.
10. **Evidence & Resources** — primary sources, implementations, watch/read material, people, and channels.

This method is defined more fully in `EDITORIAL-WORKFLOW.md`.

---

# Editorial System

The project adopts Adrian Mastronardi's **Bookwright** methodology and adapts it for an evidence-heavy technical book.

Current local Bookwright files:

```text
skills/bookwright/
├── SKILL.md
├── bootstrap.md
├── workflow.md
└── LICENSE
```

Important: the upstream Bookwright `templates/` directory is **not yet vendored locally**. Before running its scaffold-generation phase verbatim, either copy the upstream templates into `skills/bookwright/templates/` or read them directly from the upstream repository.

Do not fabricate `manifesto.md` or `voice.md` from assumptions. Bookwright explicitly requires an interview and confirmation gates.

---

# Bookwright Manifesto Interview Progress

The Bookwright manifesto interview has started but is not complete. Do not create
`manifesto.md` yet.

Confirmed on 2026-08-21:

- Working title: **Beyond Chat**
- Working subtitle: **A practical guide to building AI systems from prompts to autonomous agents**
- Format: ebook.
- Desired reading experience: easy to read, spacious, uncluttered pages, clear headings, bullets, short text, clear instructions, and distinct text elements that help readers grasp layers quickly.
- Primary audience: people who have seen advanced AI videos or explanations and know terms such as prompts, memory, agents, and tools, but have mostly consumed information rather than built systems.
- Secondary audience: busy people inside companies, such as operators, managers, founders, team leads, and knowledge workers, who have heard about AI systems but do not have time to explore the landscape from scratch.
- Prerequisite level: basic ChatGPT use only. Everything else should be explained from zero, first with a simple mental model and then mapped to the technical version.
- Gap statement: existing AI material often teaches either prompting tips or advanced engineering details. This book connects the middle: it helps everyday AI users understand the full system architecture behind serious AI work, then guides them layer by layer from chat to agents and governed autonomous systems.
- Delivery model: the book should not be straight information. It should be a guided build of one project from start to finish. Each chapter should give direction, vision, outcome, and deliverable without clutter.
- Human + agent reading model: readers should be advised near the beginning to share the book with their agent, ChatGPT, or other AI tool and move page by page or chapter by chapter so both the human and the agent absorb the project principles and execution model.
- Running project name: **ATLAS** remains acceptable.
- Running project domain: ATLAS should become an AI second-brain knowledgebase suitable for one person and for multiple people. The system should be "multiplayer-like": useful for a solo user, but designed so a team of roughly 10 people can also share knowledge, collaborate, preserve provenance, and work with agents over the same knowledge system.
- ATLAS progression: the entire book/guide should teach how to achieve this outcome step by step, starting with a second brain that works for one person and ending with a shared AI knowledgebase that can scale to a small team of around 10 people.
- Reader progression experience: the book should feel lightly gamified through clear ATLAS checkpoints and "what's next" moments. Checkpoints should show what capability was unlocked, what ATLAS can now do, what limitation remains, and what the next chapter/part will unlock. The goal is orientation and excitement, not gimmicks.
- Distribution access: free ebook.
- Research workflow preference: use the `feynman` CLI for research papers and research-question answering when it is available in the environment. On 2026-08-21, `feynman` was checked and was not found on PATH in the current workspace.
- ATLAS reference project: the author identified `https://github.com/Ntrakiyski/shared-living-memory` as the closest existing embodiment of ATLAS. It was cloned and analyzed on 2026-08-21 at commit `b9dffaf`. See `reference-projects/shared-living-memory-analysis.md`.
- Reader-facing reference decision: the book may explicitly say ATLAS is inspired by Shared Living Memory, link to the GitHub repository, and use it as a navigation/reference point so readers can inspect or use the real project if they want.
- Final build target: by the end of the book, a reader who builds along should have achieved the same kind of product as Shared Living Memory, or at least roughly 80% of its core capability in the teaching implementation.

Teaching-style material added on 2026-08-21:

- The author added `dan-koe-content/` as teaching-style reference material.
- Treat this material as inspiration for structure and reader energy, not prose to copy.
- Initial style observations: strong promise-first openings, conversational urgency, short sections, named protocols, identity/agency framing, simple-to-technical mapping, "build a project" as the filter for learning, direct imperatives, and recurring emphasis that AI should help the reader learn and build rather than outsource thinking.
- Particularly relevant structural patterns for this ebook: start from a felt limitation, name the new capability, give a practical protocol, make the reader apply it immediately, and end with a changed identity or operating level.
- Additional transcript from another profile is expected later and should be reviewed before finalizing `voice.md`.

Visual reference material added on 2026-08-21:

- Six reference images were saved under `visual-references/blackboard-flow/`.
- The source images are dark, but the ebook will use a white background. Final generated visuals should adapt the same hand-drawn explainer language for white pages: charcoal/black handwritten text, rounded arrows, simple icons, generous empty space, and colored outline nodes for categories or roles.
- Use these images later as inspiration for explanatory visuals, not as instructions or final page assets.
- The author has a Matt Pocock transcript folder at `/Users/nikolaytrakiyski/Desktop/playground/mattpocock-transcripts` to add as another teaching-style reference. On 2026-08-21, that Mac path was not mounted in the Codex workspace, so the folder could not be copied yet.

Still open in the manifesto interview:

- Exact ATLAS feature sequence within the solo-to-small-team AI second-brain knowledgebase progression.
- Methodological model or teaching influences beyond the initial Dan Koe material and the additional transcript expected from the author.
- Research division: public-source synthesis, `feynman`-assisted papers, hands-on experiments, interviews, fieldwork, or some mix.
- Distribution details beyond free ebook: website download is likely, but lead-magnet mechanics, PDF/ePub/web variants, and publication location remain open.
- Target length or first-edition size remains open.
- Scope details should be stated plainly in the manifesto, using `BOOK-BLUEPRINT.md` as the authoritative broad scope. The author has clarified that the book should avoid deep model-training theory, heavy math, and deep infrastructure setup unless necessary to understand a system layer.

The next session should resume the manifesto interview at the exact ATLAS
product framing, remaining teaching-style influences, research-division, and
distribution-details block.

---

# Important Things Intentionally Not Decided Yet

These should be settled through the Bookwright manifesto/voice interview rather than guessed:

- final title and subtitle (`Beyond Chat — A practical guide to building AI systems from prompts to autonomous agents` is current working language, not necessarily final)
- target length
- publication/distribution format (web, PDF, ePub, print, etc.)
- free vs paid distribution
- writing language variant
- register / voice
- style authority
- citation system
- formatting conventions
- code-example language and default stack
- how much implementation code vs architecture explanation each chapter should contain
- whether all chapters are mandatory in the first edition or some become advanced/optional tracks
- exact ATLAS project/domain, beyond the project name
- methodological model or teaching influences
- research division

Do not silently lock these decisions before the author answers the bootstrap questions.

---

# Audit: Concepts That Need Explicit Attention Before Locking the TOC

A review of the original conversation against the current repo found two technical subjects that are underrepresented in the final 66-chapter blueprint.

## Browser / Computer Use

Earlier planning explicitly included browser and computer-use agents: systems that operate browsers, terminals, desktop interfaces, and GUIs when APIs/CLIs are unavailable.

The durable hierarchy worth teaching is roughly:

```text
Structured API
  ↓ preferable when available
CLI / SDK
  ↓
Browser automation
  ↓
Vision / general computer use
```

This should be added explicitly to the formal TOC/outline, likely near tool calling, APIs/CLI/MCP, or runtime/sandboxing.

## Multimodal Agent Systems

The blueprint mentions multimodal models, but the practical consequences of agents consuming and producing images, audio, video, PDFs, screenshots, and other non-text artifacts are not yet a distinct teaching beat.

Before locking the TOC, decide whether this belongs inside the models/tools chapters or deserves an explicit chapter/section.

These are the two clearest technical gaps found in the session review. Do not add them mechanically if they make the structure worse; integrate them deliberately.

---

# Research Has Not Started Yet

`research/SOURCE-STANDARDS.md` defines the evidence process, but the actual research corpus has not yet been populated.

The next research phase should eventually create indexes such as:

```text
research/
├── people.md
├── channels.md
├── books.md
├── videos.md
├── repositories.md
├── papers.md
├── case-studies.md
└── chapters/
```

Do not create link dumps. Every resource should explain why it matters and, for evidence, which claim it supports.

---

# Correct Next Sequence

The next session should not immediately draft Chapter 1.

Recommended order:

1. Read `README.md`, `PROJECT-STATE.md`, `CORE-PRINCIPLES.md`, `CONCEPTUAL-FRAMEWORKS.md`, `BOOK-BLUEPRINT.md`, `EDITORIAL-WORKFLOW.md`, and `research/SOURCE-STANDARDS.md`.
2. Read `skills/bookwright/SKILL.md`, `bootstrap.md`, and `workflow.md`.
3. Resume the Bookwright **manifesto interview** with the author from the running-project, methodological-model, research-division, and distribution block.
4. After confirmation, create `manifesto.md`.
5. Run the Bookwright **voice interview**.
6. After confirmation, create `voice.md`.
7. Vendor or fetch the required Bookwright templates before generating its remaining artifacts.
8. Review the blueprint gaps above (browser/computer use and multimodal agents) before locking the formal TOC.
9. Convert `BOOK-BLUEPRINT.md` into `toc.md` with one-sentence functions and build outcomes.
10. Begin the minimum viable research corpus for Part I using current primary sources and durable references.
11. Create evidence-rich chapter cards in `outline.md`.
12. Draft a chapter only after its evidence/project/evaluation plan reaches `DRAFT-READY`.

---

# Non-Negotiable Rules for Future Sessions

- Do not reduce the book to prompting or model APIs.
- Do not organize the curriculum around current vendors.
- Do not remove the 15-dimension systems view merely to make the TOC shorter.
- Do not turn chapter builds into unrelated toy exercises; they should upgrade ATLAS whenever possible.
- Do not claim improvement without evaluation.
- Do not use popularity as evidence.
- Prefer first-party/primary sources for current technical facts.
- Preserve source provenance and dates for time-sensitive claims.
- Separate capability from authority.
- Treat autonomy as earned.
- Prefer the simplest architecture sufficient for the outcome.
- Do not hide uncertainty or unresolved research gaps with polished prose.
- Always connect technical sophistication back to real-world usefulness, cost, risk, and adoption.
