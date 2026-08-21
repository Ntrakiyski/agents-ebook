# Hard Parts Review

Date: 2026-08-21
Scope: manifesto, ATLAS persona, roadmap, Bookwright bootstrap state, and
recovery docs.

This report records the concepts and repo states most likely to confuse future
writing sessions, readers, or ATLAS itself.

---

# Summary

The project direction is coherent:

- **ATLAS** is the book-aware companion agent.
- The **shared memory system** is the product ATLAS helps the reader build.
- `roadmap.md` is the approved capability path.
- `manifesto.md` is generated and self-reviewed, pending final author
  confirmation.
- Chapter drafting remains blocked until `manifesto.md` is confirmed,
  `voice.md` is created and confirmed, and Chapter 1 reaches `DRAFT-READY`.

The review found no need to redesign the book. The fixes below reduce ambiguity
around naming, roadmap interpretation, template readiness, and ATLAS's knowledge
boundaries.

---

# Fixes Applied

## 1. Roadmap vs TOC

Risk: the 12 roadmap checkpoints could be mistaken for 12 chapters. That would
make the book feel artificially compressed and could distort the formal TOC.

Fix:

- `roadmap.md` now states that checkpoints are capability gates, not chapter
  numbers.
- `manifesto.md` now says the formal TOC must preserve the checkpoint
  progression while allowing chapters to split, merge, or combine work.
- `PROJECT-STATE.md` and `NEXT-SESSION-PROMPT.md` now repeat this distinction.

## 2. ATLAS Knowledge Boundary

Risk: because ATLAS represents the book, a deployed assistant might pretend to
know chapters, pages, sources, or project files that were not actually uploaded
or available in the current environment.

Fix:

- `soul.md` now instructs ATLAS to claim knowledge only of available book pages,
  chapter text, project files, and messages.
- If a requested chapter or resource is missing, ATLAS must ask for it or say it
  is reasoning from project rules rather than from the missing text.

## 3. Bookwright Template Readiness

Risk: the repo previously had only `templates/manifesto.md`, which would cause a
future interruption before `voice.md`, `toc.md`, `outline.md`,
`references.bib`, `conventions.md`, and the role files could be generated.

Fix:

- The upstream Bookwright templates are now vendored under
  `skills/bookwright/templates/`.
- The local MIT license remains at `skills/bookwright/LICENSE`.
- README, `PROJECT-STATE.md`, and `NEXT-SESSION-PROMPT.md` now state that the
  templates are vendored.

## 4. Stale Next-Step Numbering

Risk: `PROJECT-STATE.md` had a skipped number in the correct next sequence after
earlier edits.

Fix:

- The next sequence now runs cleanly from manifesto confirmation to voice,
  scaffold generation, TOC, research corpus, outline, and Chapter 1 readiness.

---

# Hard Concepts To Preserve

## ATLAS Is Not The Product

ATLAS is the agent persona that reads the book and helps the reader act. The
shared memory system is the product.

This distinction must stay visible in:

- the pre-Chapter-1 setup
- Chapter 1's first workspace
- checkpoint language
- later references to tools, memory, permissions, and governance

## Current Tooling Is Example, Not Law

DeepSeek Harness Desktop, OpenRouter, Pi, Hermes, Codex app, Eve, GitHub,
Vercel, and Docker are current implementation examples. The durable curriculum
is about primitives:

- context
- memory
- tools
- skills
- MCP
- harnesses
- runtime
- evals
- permissions
- governance

Every current tooling claim must be re-verified before publication.

## The Book Is Not A Memory-App Tutorial

The shared memory system is the teaching project, not the whole curriculum. It
exists so the reader has a real product through which to learn complete
AI-system architecture.

The formal TOC still needs to preserve the 15 dimensions and seven-plane map,
including reliability, security, identity, operations, economics, governance,
versioning, and portability.

## The First Edition Must Stay Buildable

The first edition should deliver a working local ATLAS companion and shared
memory system. Production, enterprise, and organization-scale topics should be
taught as production lenses or advanced paths unless the TOC gives them actual
build depth.

This prevents the book from overpromising.

## Browser, Computer Use, And Multimodal Work Need Placement

These are easy to lose because they cut across chapters.

The formal TOC should place browser/computer use through this hierarchy:

```text
structured API
  -> CLI / SDK
  -> browser automation
  -> vision / general computer use
```

Multimodal artifacts should appear where they naturally teach a system layer:

- screenshots as context
- PDFs as sources
- images as input/output artifacts
- audio/video as captured knowledge
- visual evidence in evaluation

Do not add chapters mechanically. Place the capabilities where they make the
project clearer.

---

# Still Requires Author Or Voice-Gate Decision

- Final approval or correction of `manifesto.md`.
- Primary language variant.
- Style authority.
- Citation system.
- PDF page size.
- Formatting conventions for code, prompts, callouts, source cards, and
  checkpoint pages.
- Default implementation depth and stack details after the voice gate.
- Chapter-level conversion of the approved checkpoint roadmap into the formal
  TOC.
- Whether optional ePub/web-book/lead-magnet mechanics matter for first
  release.

---

# Recommendation

Approve `manifesto.md` after reading the self-reviewed draft, then proceed to
the Bookwright voice interview.

Do not start Chapter 1 yet. The next real unlock is `voice.md`, because it will
settle how the book sounds, how evidence appears on the page, and how prompts,
code, checkpoints, quotes, and resource cards are rendered.
