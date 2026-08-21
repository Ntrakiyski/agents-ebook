# Editorial Workflow

This project uses the structure and discipline of [Bookwright](https://github.com/AdrianMastronardi/bookwright) as its editorial foundation, with additional rules specific to a technical, project-driven book about AI systems.

The upstream `SKILL.md` is stored under `skills/bookwright/` with its MIT license.

Bookwright's core idea is that a long-form project should not jump directly from an idea to prose. The project first establishes its constitution, voice, structure, bibliography, and evidence-rich outline; drafting then passes through distinct editorial roles and a final blind assessment.

For this book we keep that model and add three project-specific layers:

1. **Core Principles** — the reader receives the book's worldview before the technical journey begins.
2. **Evidence Layer** — important claims are supported by primary sources, research, practitioners, books, repositories, talks, experiments, and evaluations.
3. **Build Layer** — every technical chapter is organized around a real project that upgrades the evolving ATLAS system.

---

# Project Law

Once created through the Bookwright bootstrap process, these files become project law:

```text
manifesto.md
voice.md
CORE-PRINCIPLES.md
```

Before drafting or materially restructuring a chapter, the writer/editor should read these documents.

Their roles are different:

- `manifesto.md` — what the book is, why it exists, who it is for, and what is in/out of scope.
- `voice.md` — how the book should sound and how prose, terminology, citations, formatting, and technical language are handled.
- `CORE-PRINCIPLES.md` — the ten beliefs through which the book interprets AI-system engineering.

`BOOK-BLUEPRINT.md` is the current architectural map of the book and will feed the formal `toc.md` and `outline.md`.

---

# The Adapted Pipeline

## Phase 0 — Principles

**Artifact:** `CORE-PRINCIPLES.md`

Before teaching tools or terminology, establish the mindset the reader should use throughout the book.

The principles should be referenced repeatedly rather than confined to the opening pages.

Examples:

- Context engineering can point back to **Context Is a System, Not a Giant Prompt**.
- Permissions can point back to **Give Agents Capabilities Deliberately and Authority Conservatively**.
- Evals can point back to **Evals Are the Feedback Loop of AI Engineering**.
- Multi-agent systems can point back to **Use the Simplest System That Can Reliably Produce the Outcome**.

The principles are the interpretive layer of the book.

---

## Phase 1 — Idea

**Artifact:** `manifesto.md`

Use the Bookwright bootstrap interview. Do not infer unanswered publishing decisions from the existing blueprint.

The manifesto should settle:

- working title/subtitle
- genre and intended format
- specific gap the book fills
- primary and secondary audiences
- scope and exclusions
- methodological influences
- research strategy
- distribution strategy
- decisions already taken

**Gate:** The reader should be able to understand what the book is, why it deserves to exist, and whom it serves without additional explanation.

---

## Phase 2 — Voice

**Artifact:** `voice.md`

Use the Bookwright voice interview to settle:

- writing language and variant
- register
- citation system
- terminology rules
- handling of product/vendor names
- handling of code and diagrams
- style authority
- failure modes to avoid

For this book, the eventual voice should support a reader moving from beginner mental models into sophisticated systems engineering without becoming academic, hype-driven, or product-manual prose.

**Gate:** A separate editor should be able to enforce the writing style without asking the author how a section should sound.

---

## Phase 3 — Structure

**Artifacts:** `BOOK-BLUEPRINT.md` → `toc.md`

`BOOK-BLUEPRINT.md` contains the broad architecture. The formal `toc.md` should turn that into a concise publishing spine where every part and chapter has:

- title
- one-sentence function
- primary AI-system dimension
- project/build outcome

The opening order should be:

```text
Opening / Preface
The 10 Core Principles of Building With AI

Part I — Intelligence
...
```

The principles therefore frame the technical chapters rather than appearing late as a summary.

---

## Phase 4 — Bibliography and Resource Corpus

**Artifacts:**

```text
references.bib
research/
```

This phase is broader than a normal bibliography because the subject is technical and fast-moving.

We intentionally collect:

- official documentation
- specifications
- papers
- repositories
- technical articles
- engineering blogs
- books
- videos and conference talks
- people worth following
- channels, newsletters, and podcasts
- production case studies
- datasets and benchmarks

Follow `research/SOURCE-STANDARDS.md`.

Resources have two jobs:

1. **Evidence** — substantiate important claims.
2. **Continuation** — give readers a path to keep learning after the chapter and after the book ages.

**Gate:** Every part has a minimum viable research corpus. Each chapter must eventually have sources bound to its important claims before becoming `DRAFT-READY`.

---

## Phase 5 — Evidence-Rich Outline

**Artifact:** `outline.md`

Each chapter card should combine the Bookwright outline model with the project's chapter contract.

A chapter card should contain:

```text
CHAPTER

Function
Why this chapter exists.

Dimension
Which of the 15 AI-system dimensions it primarily teaches.

Reader state before
What the reader currently understands/can build.

Problem
The practical failure or limitation that creates the need for this chapter.

Mental model
The simplest correct conceptual explanation.

Core claims
Important assertions the chapter must establish.

Evidence
Sources or experiments supporting each important claim.

Build
The real project implemented during the chapter.

Break It
How the project will intentionally fail or expose its limits.

Under the Hood
What internal mechanics the reader will inspect.

Production Lens
Data, integrations, reliability, security, observability, human oversight, governance, and economics relevant to the chapter.

Evaluate
How we prove whether the chapter's change improved the system.

ATLAS Upgrade
The permanent capability added to the book's evolving system.

Resources
Primary sources, implementations, videos, books, people, and channels worth keeping.

Cross-references
Earlier principles/chapters this chapter depends on and later chapters it enables.

Gaps / Queries
Unresolved research or author decisions.
```

### DRAFT-READY gate

A chapter is ready for drafting only when:

- its purpose is clear
- its argument/mental model is clear
- its project is defined
- important claims have evidence
- the evaluation approach is defined
- evidence gaps are explicit
- dependencies on earlier chapters are understood
- there is enough source material to draft without inventing facts

---

## Phase 6 — Writing

**Artifacts:** `chapters/*.md`

Follow Bookwright's three sequential writing roles.

### Role 1 — Draft Editor

Produce the technically sound first draft from the chapter card and source corpus.

Priority:

```text
Correctness
→ Structure
→ Evidence
→ Teaching flow
→ Project continuity
→ Prose polish
```

Do not hide research gaps with confident prose.

### Role 2 — Development + Line Editor

Check:

- Does the chapter solve the problem it promised to solve?
- Does the project teach the concept rather than distract from it?
- Does complexity rise at the right pace?
- Does the chapter connect to the core principles?
- Are important claims supported?
- Does the reader understand where the new capability fits in the complete AI system?
- Is the prose clear and technically precise?

### Role 3 — Copy Editor

Mechanical and consistency pass:

- grammar
- punctuation
- terminology
- code formatting
- references
- citation consistency
- cross-references
- product names
- chapter numbering
- diagram labels

---

# The Mandatory Chapter Contract

Every technical chapter uses the following reader-facing sequence unless there is a strong reason not to:

## 1. The Problem
Begin with the practical limitation that makes the concept necessary.

## 2. What We Are Building
Show the project and expected outcome before diving into terminology.

## 3. Mental Model
Explain the concept at the simplest correct level.

## 4. Build
Implement the project progressively.

## 5. Break It
Expose where the naive version fails.

## 6. Under the Hood
Inspect what actually happened: prompt, context, tokens, routing, tools, state, traces, etc.

## 7. Production Lens
Ask what changes once the capability is placed inside a real system.

## 8. Evaluate
Measure success rather than declaring it.

## 9. ATLAS Upgrade
Show exactly what capability the evolving system gained.

This section should also act as a light checkpoint in the reader's journey:

```text
Capability unlocked
What ATLAS can now do
What still breaks or remains missing
What's next
```

The goal is to give the book a game-like sense of progression without turning
the prose into a gimmick. Each chapter should leave the reader knowing both
where they are in the system and why the next capability matters.

## 10. Evidence & Resources
Give the reader the source trail and continuation path.

The chapter project is not an end-of-chapter exercise. **The project is the teaching mechanism of the chapter.**

---

# Recurring Evidence & Resources Section

Each chapter's final resource section should normally contain:

```text
Evidence & Resources

Primary Sources
See It in Practice
Watch
Read Deeper
People & Channels to Follow
```

Every resource gets a short explanation of why it matters. Avoid uncurated lists.

---

# Recurring Principles Section

Where useful, a chapter should explicitly state which core principle it demonstrates.

Example:

```text
PRINCIPLE IN PRACTICE

Principle 5 — Autonomy Must Be Earned

This chapter's agent currently requires approval before sending external email.
We will not remove that approval until the evaluation suite demonstrates the
reliability threshold defined in Chapter X.
```

This is how the principles become a working mindset rather than an opening manifesto the reader forgets.

---

# Phase 7 — Whole-Manuscript Assessment

Once the manuscript has passed all chapter-level editorial stages, use the Bookwright acquiring-editor role as a blind read of the rendered manuscript.

The final reviewer should not be given the author's internal intentions. The book must communicate its own:

- promise
- audience
- argument
- progression
- usefulness
- differentiation

This catches a different class of problems than chapter-level editing.

---

# The Operating Loop

The workflow is iterative rather than waterfall.

```text
Principles
   ↓
Manifesto
   ↓
Voice
   ↓
Structure
   ↓
Research + Evidence
   ↓
Outline
   ↓
Build + Draft
   ↓
Evaluate
   ↓
Development Edit
   ↓
Copy Edit
   ↓
Chapter complete
   ↓
New evidence / new technology / reader feedback
   └──────────────────────────────→ Research + Outline
```

New AI developments should usually update evidence, examples, resources, or implementation details before they change the book's durable principles.
