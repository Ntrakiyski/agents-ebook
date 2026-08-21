# Manifesto

Status: confirmed project law.
Generated: 2026-08-21
Final review applied: 2026-08-21
Author confirmed: 2026-08-21

Beyond Chat: A practical guide to building AI systems from prompts to autonomous agents

## 1. What this project is

*Beyond Chat* is a free, project-driven technical ebook for people who know how
to use ChatGPT and want to understand what comes next. It is not a dictionary of
AI terms and not a vendor tour. It is a practical guide to the durable layers of
AI systems: models, prompts, context, tools, agents, harnesses, workflows,
evaluation, autonomy, multi-agent systems, operations, economics, governance,
versioning, and portability.

The first edition is a PDF ebook, provisionally targeted at 80-120 pages. The
reading experience should be spacious and low-noise: clear headings, short
sections, bullets where useful, visual explanation, and direct instructions.
Each technical chapter should be roughly 70 percent content and visual
explanation, and 30 percent project work.

The reader builds through two connected layers. First, they turn an existing
local agent environment into **ATLAS**, the book-aware companion agent defined
in `soul.md`. Then they use ATLAS to build the **shared memory system**, a
local-first AI second-brain knowledgebase that begins useful for one person and
can grow toward a small team of around 10 people.

## 2. Why this project

Many people have moved beyond basic prompting in their curiosity, but not in
their practice. They have watched videos about agents, memory, MCP, tools,
automation, and coding assistants. They recognize the words. But they have not
built the layers, felt the limitations, inspected the failures, or learned how
the pieces fit into a complete system.

Existing AI education often splits into two unsatisfying paths. One path gives
prompting tricks and surface-level productivity advice. The other jumps into
advanced engineering detail before the reader understands the system map. This
book fills the middle: it helps everyday AI users move from passive AI content
to practical AI-system building without pretending that a complete system is
only "prompt plus model plus tools."

The book's claim is simple: doing is learning, not reading. A reader may upload
the PDF to cloud ChatGPT and read along, but the recommended path moves them to
a local or free agent workflow where they can build, break, inspect, evaluate,
and permanently upgrade a real system.

## 3. Target audience

**Primary audience.** The primary reader is an AI-curious ChatGPT user who has
seen advanced AI videos or explanations and knows terms like prompts, memory,
agents, tools, MCP, and evals, but has mostly consumed information rather than
built systems. This reader needs a clear path from "I understand the idea" to "I
can make this work." The writing must explain every new idea first in simple
language, then map it to the technical version used in real systems.

**Secondary audience.** The secondary reader is a busy person inside a company:
an operator, manager, founder, team lead, or knowledge worker who has heard that
AI systems can change how work happens but does not have time to explore the
landscape from scratch. This reader needs the full map, the practical stakes,
and enough technical clarity to make decisions, guide agents, and understand
what a team should build or avoid.

Both audiences should leave with a higher-level overview of each system layer,
while ATLAS and the reader's own agent environment gain practical operating
knowledge.

## 4. Period or scope

The scope is practical AI-system building for the current agent era, written so
the principles survive changes in vendors and tools. The book begins with the
smallest useful unit - the model call - and builds upward through prompts,
context, tools, agents, harnesses, workflows, evals, autonomy, multi-agent
systems, self-improving systems, and the organizational conditions around
AI-native work.

The concrete first-edition capability path is approved in `roadmap.md`. Its
checkpoints are not chapter numbers; they are gates the formal TOC must preserve
while allowing chapters to split, merge, or combine work as needed. The reader
leaves cloud chat, creates ATLAS, creates a workspace, captures first knowledge,
grounds answers in evidence, chooses context, structures memory, adds memory
lifecycle rules, evaluates recall, gives ATLAS scoped tools, adds team
boundaries, and introduces governance.

The formal TOC must explicitly place two capability areas that are easy to
underrepresent. First, browser and computer use should be taught through the
capability hierarchy of structured API, CLI/SDK, browser automation, and then
vision or general computer use. Second, multimodal agent systems should appear
where relevant: agents consuming and producing screenshots, PDFs, images,
audio, video, and other artifacts. These areas should be integrated deliberately
instead of mechanically added as extra chapters.

The book excludes deep model-training theory, heavy math, and deep
infrastructure setup unless a limited explanation is necessary to understand a
system layer. It may discuss production, deployment, security, identity,
permissions, observability, and governance, but the first-edition deliverable is
a working local ATLAS companion and shared memory system, not an enterprise
platform. Later layers such as self-improving systems and AI-native
organizations should be taught as architectural destinations and production
lenses unless the first-edition roadmap explicitly gives them build depth.

## 5. Methodological model

The book combines momentum with engineering discipline. Dan Koe and Matt Pocock
are teaching references: Dan for promise-first openings, reader energy, short
sections, identity-level framing, and simple-to-technical mapping; Matt for a
disciplined build workflow that moves from idea to research, prototype,
specification, tickets, implementation, review, and QA.

The content and evidence references are different from the teaching references.
Nate Herk informs the bridge from AI curiosity into automation and second-brain
thinking. AI Engineer contributes production examples and current research
leads. Stanford CS329A contributes research-backed framing for self-improving
agents, verification, feedback, planning, tool use, and evaluation. Shared
Living Memory is the concrete product ancestor for the shared memory system.

The method is not to copy any source's prose or structure. The method is to
teach durable AI-system primitives through one evolving build, while binding
important claims to evidence and separating durable principles from current
implementation examples.

## 6. Division of research labor

The author's existing expertise and experience building autonomous systems
drives the judgment, structure, and practical tradeoffs. The book is not framed
as detached academic research; it is a research-backed technical guide written
by someone who already understands the domain and wants to make that knowledge
usable for readers and their agents.

Bibliographic synthesis is required for the durable technical claims: official
documentation, specifications, source code, papers, technical reports,
engineering blogs, production case studies, benchmarks, and durable systems
literature. Current facts about model capabilities, pricing, context windows,
API behavior, product features, framework support, and vendor limitations must
be verified from current primary sources and dated.

Primary investigation for the first edition is mainly hands-on experimentation:
building the chapter artifacts, breaking them, inspecting traces or outputs,
and evaluating whether the system improved. Interviews and fieldwork are not
required for the first edition, though they may become useful later. The
`feynman` CLI should be used for research papers and research-question answering
when available.

## 7. Priority sources

The source hierarchy follows `research/SOURCE-STANDARDS.md`.

First priority: official documentation, specifications, source code, release
notes, and product docs for current implementation details. These sources prove
what a tool or platform currently does, but they must not become permanent
architectural law.

Second priority: original papers, technical reports, and research lectures for
claims about models, agents, planning, tool use, retrieval, memory, evaluation,
and self-improving systems.

Third priority: first-hand engineering evidence, production case studies,
technical blogs, and repositories that show how systems behave outside toy
examples.

Fourth priority: durable systems literature, strong educational material,
videos, talks, newsletters, podcasts, and practitioner references that help the
reader continue learning. Community evidence may be used for discovery or
practical signals, but not as the main proof for important technical claims.

Every chapter should curate resources for two purposes: proof and continuation.
The book should not use giant link dumps.

## 8. Format and distribution

The first edition is a free PDF ebook distributed from the author's website. The
website page should explain what the book is, provide the PDF, give setup
instructions, link to tools and resources, and explain how to upload or use the
book with an agent.

The recommended reading path is practical: use a local or free agent workflow,
give the agent the ATLAS persona, and build chapter by chapter. A cloud ChatGPT
upload path is allowed as a fallback reading mode, but the book should be
honest that reading alone keeps the reader mostly in the same place.

Optional formats such as ePub, web-book, print, or lead-magnet mechanics remain
deferred. PDF page size is not decided yet. The visual direction is a
white-background, spacious, hand-drawn explainer style with short labels,
simple icons, rounded arrows, and colored outline accents.

## 9. Positioning against existing work

The book is positioned against three broad categories of existing AI education.

Prompting and productivity content helps people get more value from chat, but
often leaves the system underneath invisible. This book starts from chat but
moves the reader into local agents, files, tools, context, memory, evaluation,
permissions, and governance.

Advanced engineering content often assumes the reader already knows how the
layers fit together. This book gives the full map first, then builds
bottom-up. It uses technical language, but every concept is introduced through a
practical limitation and a real build.

Vendor- or framework-centered tutorials can be useful, but they age quickly.
This book teaches durable primitives first and uses current tools such as local
agent apps, OpenRouter, Eve, GitHub, Vercel, MCP implementations, and agent
frameworks as examples requiring re-verification before publication.

## 10. Decisions taken and recorded

- Title: *Beyond Chat*.
- Subtitle: *A practical guide to building AI systems from prompts to autonomous agents*.
- Main format: free PDF ebook.
- Provisional target length: 80-120 pages, to be recalibrated after Chapter 1.
- Primary audience: AI-curious ChatGPT users who have watched advanced content but have not built real systems.
- Secondary audience: busy company people who need the map and a practical path.
- Prerequisite level: basic ChatGPT use only.
- Core reader contract: doing is learning, not reading.
- ATLAS is the book-aware companion agent, defined in `soul.md`.
- The product is called the shared memory system or shared second-brain knowledgebase.
- The approved checkpoint path lives in `roadmap.md`.
- Chapter method: problem, build, break, inspect, evaluate, system upgrade, evidence and resources.
- Chapter balance: roughly 70 percent content and visual explanation, 30 percent project work.
- Research posture: research-backed technical guide.
- Voice baseline: direct and simple, with energetic openings and grounded technical prose.
- Tooling path: local/free agent workflow first; DeepSeek Harness Desktop, Pi, Hermes, Codex app, OpenRouter, Eve, GitHub, Vercel, and Docker are current implementation examples, not permanent curriculum anchors.
- Browser/computer use must be placed deliberately through the API to CLI/SDK to browser automation to general computer-use hierarchy.
- Multimodal artifacts such as screenshots, PDFs, images, audio, and video must be integrated where they clarify models, tools, context, runtime, and evaluation.
- Scope exclusions: deep model-training theory, heavy math, and deep infrastructure setup unless needed to understand a system layer.
- Citation system, page size, exact language variant, and detailed style authority remain for the voice gate.
