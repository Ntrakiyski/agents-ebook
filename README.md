# Beyond Chat

Working subtitle: **A practical guide to building AI systems from prompts to autonomous agents**.

An in-progress, project-driven ebook for people who know basic ChatGPT and have
watched advanced AI content, but have not yet built real AI systems.

The book teaches durable AI-system primitives through one evolving project:
**ATLAS**, an AI second-brain knowledgebase that starts useful for one person
and grows toward a shared, multiplayer-like knowledge system for a small team of
around 10 people.

The core stance is direct: **doing is learning, not reading**. A reader can
upload the PDF to cloud ChatGPT and read along, but the recommended path moves
them into a local/free agent workflow so they can build ATLAS chapter by
chapter.

## Start Here

1. [`PROJECT-STATE.md`](PROJECT-STATE.md) — durable handoff: settled decisions, open questions, audit findings, and the correct next sequence.
2. [`CORE-PRINCIPLES.md`](CORE-PRINCIPLES.md) — the 10 principles through which the entire book should be read.
3. [`CONCEPTUAL-FRAMEWORKS.md`](CONCEPTUAL-FRAMEWORKS.md) — capability ladder, seven planes, AI-system iceberg, autonomy ladder, and recurring mental models.
4. [`BOOK-BLUEPRINT.md`](BOOK-BLUEPRINT.md) — the current 15-dimension, 66-chapter architecture of the book.
5. [`EDITORIAL-WORKFLOW.md`](EDITORIAL-WORKFLOW.md) — how we research, outline, build, write, evaluate, and edit the manuscript.
6. [`research/SOURCE-STANDARDS.md`](research/SOURCE-STANDARDS.md) — evidence and resource requirements for every chapter.
7. [`NEXT-SESSION-PROMPT.md`](NEXT-SESSION-PROMPT.md) — copy/paste handoff prompt for continuing the project in a fresh AI session.

## Current Status

The project is still in the Bookwright bootstrap phase.

Do **not** start drafting chapters yet. The next editorial gate is to finish the
Bookwright manifesto interview, create `manifesto.md`, run the voice interview,
and create `voice.md`. Only after those are confirmed should the formal TOC,
research corpus, evidence-rich outline, and chapters be locked.

Settled direction so far:

- Main format: free PDF.
- Distribution: a dedicated page on the author's website with the PDF,
  instructions, links, and resources.
- Chapter balance: roughly 70% reading/visual explanation and 30% project work.
- Every technical chapter should permanently upgrade ATLAS.
- First practical move: install or use a local agent environment rather than
  staying only in cloud chat.
- Default free-model path under review: DeepSeek Harness Desktop with OpenRouter
  free models; Pi and Hermes are CLI alternatives; Codex app is an option for
  ChatGPT users. Current facts must be re-verified before publication.

## Bookwright

The editorial workflow is based on Adrian Mastronardi's [Bookwright](https://github.com/AdrianMastronardi/bookwright) seven-phase long-form writing system.

The vendored Bookwright material currently lives under `skills/bookwright/`:

- [`SKILL.md`](skills/bookwright/SKILL.md)
- [`bootstrap.md`](skills/bookwright/bootstrap.md)
- [`workflow.md`](skills/bookwright/workflow.md)
- [`LICENSE`](skills/bookwright/LICENSE)

The upstream `templates/` directory has not yet been vendored; fetch/copy it before running Bookwright's scaffold-generation phase verbatim.

Bookwright gives the project a disciplined progression through manifesto, voice, structure, bibliography, evidence-rich outline, writing/editorial passes, and final whole-manuscript assessment. This project extends that model with three requirements:

- **Core principles first** — the book begins with the mindset used to reason about every later technology.
- **One concept → one real build** — projects are the teaching mechanism, not optional exercises at the end.
- **Evidence with every chapter** — documentation, papers, repositories, articles, books, talks, people, channels, case studies, experiments, and evaluations support what the book says.

## Current Direction

The reader builds one evolving system throughout the book, currently named
**ATLAS**.

ATLAS is inspired by
[`shared-living-memory`](https://github.com/Ntrakiyski/shared-living-memory).
The teaching implementation does not need to copy that repository, but the
reader should reach the same kind of product, or roughly 80% of its core
capability, by the end of the book.

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

The goal is not to teach a temporary collection of AI products. The goal is to teach the durable primitives, mental models, engineering practices, and operating principles needed to build complete AI systems.

## Reference Material

Creator and technical reference material lives under
[`creator-profiles/`](creator-profiles/).

- Dan Koe and Matt Pocock are teaching/style references.
- Nate Herk, AI Engineer, and Stanford CS329A are content, knowledge, and
  principle references.

Visual direction lives under [`visual-references/`](visual-references/). The
approved generated samples use a white-page, spacious, hand-drawn explainer
style with short labels and colored outline accents.
