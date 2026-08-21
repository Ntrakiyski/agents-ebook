# Beyond Chat — Agents Ebook

Working subtitle: **A practical guide to building AI systems from prompts to autonomous agents**.

A project-driven book about moving from ChatGPT-style AI use to complete production AI systems: context, agents, harnesses, runtime, evals, security, observability, orchestration, governance, economics, and AI-native organizations.

## Start Here

1. [`PROJECT-STATE.md`](PROJECT-STATE.md) — durable handoff: settled decisions, open questions, audit findings, and the correct next sequence.
2. [`CORE-PRINCIPLES.md`](CORE-PRINCIPLES.md) — the 10 principles through which the entire book should be read.
3. [`CONCEPTUAL-FRAMEWORKS.md`](CONCEPTUAL-FRAMEWORKS.md) — capability ladder, seven planes, AI-system iceberg, autonomy ladder, and recurring mental models.
4. [`BOOK-BLUEPRINT.md`](BOOK-BLUEPRINT.md) — the current 15-dimension, 66-chapter architecture of the book.
5. [`EDITORIAL-WORKFLOW.md`](EDITORIAL-WORKFLOW.md) — how we research, outline, build, write, evaluate, and edit the manuscript.
6. [`research/SOURCE-STANDARDS.md`](research/SOURCE-STANDARDS.md) — evidence and resource requirements for every chapter.
7. [`NEXT-SESSION-PROMPT.md`](NEXT-SESSION-PROMPT.md) — copy/paste handoff prompt for continuing the project in a fresh AI session.

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

The reader builds one evolving system throughout the book, currently named **ATLAS**.

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
