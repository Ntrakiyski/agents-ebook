# Next Session Prompt

Copy the prompt below into a new session before continuing the ebook project.

---

You are continuing an existing long-form technical ebook project. The repository is the source of truth:

**https://github.com/Ntrakiyski/agents-ebook**

Do not assume you have access to any previous chat. Recover the project state from the repository before making decisions.

## First action: read the project law and handoff

Read these files in this order:

1. `README.md`
2. `PROJECT-STATE.md`
3. `CORE-PRINCIPLES.md`
4. `CONCEPTUAL-FRAMEWORKS.md`
5. `BOOK-BLUEPRINT.md`
6. `EDITORIAL-WORKFLOW.md`
7. `research/SOURCE-STANDARDS.md`
8. `skills/bookwright/SKILL.md`
9. `skills/bookwright/bootstrap.md`
10. `skills/bookwright/workflow.md`

Treat the repo as authoritative. If something in this prompt conflicts with a newer committed decision in the repo, surface the conflict rather than silently choosing one.

## What we are building

The ebook teaches people how to move from basic AI usage to engineering complete AI systems, bottom-up.

It starts with models, tokens, prompts, structured output, reasoning, and context; progresses through knowledge, retrieval, memory, tools, APIs, CLI, MCP, skills, agent loops, harness engineering, hooks, runtime, worktrees, subagents, parallel agents, orchestration, workflows, evals, reliability, security, identity, human interaction, learning, observability, economics, organization, governance, versioning, and portability; and ends with autonomous and AI-native organizations.

The goal is **not** to teach a temporary collection of products. Teach durable primitives and mental models first, then use current products such as coding agents, model providers, MCP implementations, workflow systems, and frameworks as examples of how those primitives are implemented today.

## Core architecture of the book

The reader builds one evolving system throughout the book, currently called **ATLAS**.

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
Evaluation
  ↓
Autonomy
  ↓
Multi-Agent System
  ↓
Self-Improving AI System
  ↓
AI-Native Organization
```

One chapter should generally produce one real capability and permanently upgrade ATLAS.

The teaching rule is:

> **One chapter → one capability → one real build → break it → inspect it → evaluate it → add it to the larger system.**

Do not turn the builds into disconnected toy exercises unless a small isolated experiment is genuinely the clearest way to teach the concept.

## Core principles are project law

The book begins with `CORE-PRINCIPLES.md`. The principles are the reader's permanent lens, not an introductory appendix.

In particular preserve these ideas:

- Intelligence is a component; the complete system is the product.
- Specify the outcome before optimizing intelligence.
- Context is a system, not a giant prompt.
- Capability and authority are different.
- Autonomy must be earned with evidence.
- Prefer evidence over eloquence.
- Evals are the feedback loop of AI engineering.
- Design for failure, recovery, and reversibility.
- Use the simplest architecture that can reliably produce the outcome.
- Optimize for the real-world outcome, not the impressiveness of the agent run.

## The complete systems view

Do not focus only on the visible model/agent layer. The book deliberately covers the hidden infrastructure beneath it:

- data
- integrations
- runtime
- state
- identity
- permissions
- evaluations
- reliability
- security
- observability
- human oversight
- governance
- economics
- organizational ownership and adoption
- evolution/versioning/portability

The detailed curriculum is organized around 15 AI-system dimensions documented in `BOOK-BLUEPRINT.md` and a seven-plane mental model documented in `CONCEPTUAL-FRAMEWORKS.md`.

## Mandatory chapter method

For technical chapters, follow the chapter contract in `EDITORIAL-WORKFLOW.md`:

1. The Problem
2. What We Are Building
3. Mental Model
4. Build
5. Break It
6. Under the Hood
7. Production Lens
8. Evaluate
9. ATLAS Upgrade
10. Evidence & Resources

Start from the practical limitation, not from a glossary definition. Let the need for the concept emerge from the project.

## Evidence and resources are mandatory

This book must not ask technical readers to believe important claims merely because the prose sounds confident.

Use `research/SOURCE-STANDARDS.md`.

For important claims prefer, where applicable:

1. official documentation, specifications, source code, primary papers, release notes
2. first-hand engineering/practitioner evidence
3. durable books and systems literature
4. strong educational material
5. community signals only as supporting/discovery evidence

Every chapter should eventually curate useful resources such as:

- official docs
- papers
- repositories
- technical articles
- books
- videos / conference talks
- production case studies
- benchmarks / datasets
- people worth following
- channels, engineering blogs, newsletters, podcasts

Resources have two jobs:

- **Proof:** support what the chapter says.
- **Continuation:** help readers keep learning after the book and after current tools change.

Bind sources to claims during outlining. Do not create a giant link dump at the end.

For current model capabilities, pricing, API behavior, context windows, product features, framework support, benchmarks, or vendor limits, research the latest primary sources and record the verification date. Separate durable principles from current implementations.

## Bookwright workflow

We adopted Adrian Mastronardi's Bookwright methodology.

Do **not** jump straight into Chapter 1.

The next task is to bootstrap the editorial project correctly.

Follow `skills/bookwright/bootstrap.md`. Bookwright requires an interview for `manifesto.md` and `voice.md`; do not infer unanswered publishing decisions from the existing blueprint.

Ask the manifesto questions in grouped blocks, summarize my answers, and wait for confirmation at the required gates. Then do the same for voice.

Only after manifesto and voice are confirmed should we lock the formal TOC, research corpus, evidence-rich outline, and chapters.

The upstream Bookwright templates have not all been vendored locally yet. Before the scaffold-generation phase, either copy the required templates from `https://github.com/AdrianMastronardi/bookwright/tree/main/templates` into `skills/bookwright/templates/` while preserving the upstream license, or read them from upstream when generating the project artifacts.

## Known blueprint audit items

Before locking the formal TOC, review two areas called out in `PROJECT-STATE.md`:

- **Browser / computer use:** browsers, desktop/GUI operation, and the API → CLI/SDK → browser automation → general computer-use capability hierarchy should be explicitly represented.
- **Multimodal agent systems:** the practical use of images, screenshots, audio, video, PDFs, and other non-text artifacts is currently less explicit than it should be. Decide where it belongs without bloating the curriculum unnecessarily.

Do not randomly add chapters. Integrate these deliberately into the existing architecture.

## Important things that are still open

Do not invent these. The Bookwright interview should settle them with me:

- final title/subtitle
- primary and secondary audience
- prerequisite level
- final scope and exclusions
- target length
- distribution format and access
- language variant
- register and voice
- style authority
- citation system
- code-example language/default stack
- implementation-depth expectations

`Beyond Chat — A practical guide to building AI systems from prompts to autonomous agents` is the current working title/subtitle. `ATLAS` remains the accepted running project name. Neither is immutable branding.

## Current Bookwright manifesto progress

The manifesto interview has started but is incomplete. Do not create `manifesto.md` yet.

Confirmed:

- Format: ebook.
- Reading experience: spacious, uncluttered, easy to read, with clear headings, bullets, short text, clear instructions, and distinct text elements.
- Primary audience: people who have seen advanced AI videos/explanations and know terms like prompts, memory, agents, and tools, but have mostly consumed information rather than built systems.
- Secondary audience: busy people inside companies who have heard about AI systems but do not have time to explore the landscape from scratch.
- Prerequisite level: basic ChatGPT use only.
- Gap: existing AI material often jumps between prompting tips and advanced engineering detail. This book connects the middle by helping everyday AI users understand serious AI-system architecture and build upward from chat to agents and governed autonomy.
- Delivery model: the book is a guided build of one project from start to finish, not straight information.
- Human + agent reading model: readers should be advised to share the book with their AI assistant and move page by page or chapter by chapter so both the human and the agent absorb the system principles.
- Running project domain: ATLAS becomes an AI second-brain knowledgebase that works for one person and can scale to a small team, roughly 10 people, in a multiplayer-like shared knowledge environment.
- Distribution access: free ebook.
- Research workflow preference: use the `feynman` CLI for research papers and research-question answering when available. It was checked on 2026-08-21 and was not found on PATH in the current workspace.
- Teaching-style reference: `dan-koe-content/` has been added. Use it as inspiration for structure and reader energy, not prose to copy. Initial observations: promise-first openings, short sections, named protocols, identity/agency framing, simple-to-technical mapping, project-based learning, direct imperatives, and emphasis on using AI to learn and build rather than outsource thinking.

Still open:

- Exact ATLAS product framing and feature sequence inside the AI second-brain knowledgebase domain.
- Additional teaching-style influences: the author expects to provide another transcript from another profile.
- Research division.
- Distribution details beyond free access: website, PDF/ePub/web variants, lead magnet, or other.
- Target length / first-edition size.
- Voice interview items.

## Working behavior

- Inspect the repo before proposing changes.
- Preserve settled architecture unless research or the manifesto exposes a real contradiction.
- Ask questions when Bookwright requires author judgment; do not fill gaps with defaults.
- Use current web research when current technical facts are involved.
- Prefer primary sources.
- Mark uncertainty and conflicting evidence explicitly.
- Keep project files in the GitHub repo updated as decisions are made.
- When a major decision changes, update the relevant project-law/state documents so a future session can recover without this chat.
- Do not start prose drafting until the relevant chapter card is `DRAFT-READY`: purpose, mental model, project, claims/evidence, evaluation plan, dependencies, and gaps must be clear.

## Start now

First, read the repository files listed above and give me a **short recovery report** containing:

- what the book is trying to achieve
- the current architecture
- what is already locked
- what remains open
- the correct next step

Then immediately resume the **Bookwright manifesto interview** at the exact ATLAS product framing, remaining teaching-style influences, research-division, and distribution-details block. Do not redesign the book or start Chapter 1 before completing the Bookwright gates.
