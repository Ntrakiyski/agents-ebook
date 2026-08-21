# Research, Evidence, and Source Standards

The book should not ask the reader to accept important claims because the author says so. Technical claims, architectural recommendations, historical context, security guidance, performance assertions, and statements about how current AI systems work should be supported by evidence.

Resources are not an appendix added after writing. They are part of the chapter-building process.

---

# The Evidence Rule

For every meaningful claim, ask:

> What would make a skeptical technical reader believe this?

The answer may be:

- official documentation or a specification
- a peer-reviewed paper or technical report
- source code or an official repository
- an experiment performed in the chapter
- an evaluation result
- a production case study
- a practitioner explaining the system they built
- a book that establishes the broader concept

A polished sentence without evidence is not proof.

---

# Source Hierarchy

Prefer sources in roughly this order when they are available.

## Tier A — Primary Evidence

Highest priority for factual and technical claims.

- official documentation
- specifications and standards
- research papers
- technical reports from the organization that built the system
- official repositories and source code
- release notes and changelogs
- first-party security documentation
- benchmark methodology and raw results

Examples: OpenAI documentation, Anthropic documentation, MCP specification, Git documentation, Kubernetes documentation, official GitHub repositories, original research papers.

## Tier B — First-Hand Practitioner Evidence

Useful for architecture, implementation details, trade-offs, and production lessons.

- engineering blogs
- conference talks
- technical presentations
- interviews with system builders
- postmortems
- production case studies

Prefer the person or team that actually built or operated the system.

## Tier C — Books and Durable Explanations

Useful for deeper mental models and principles that outlive individual products.

- technical books
- systems-engineering books
- distributed-systems literature
- software architecture books
- security books
- HCI and organizational design books

These should often support the book's principles rather than fast-changing product facts.

## Tier D — High-Quality Educational Resources

Useful for alternate explanations and continued learning.

- expert YouTube channels
- courses
- lectures
- podcasts
- newsletters
- technical tutorials

These are learning resources, not automatically authoritative evidence.

## Tier E — Community Signals

Useful for discovering problems, edge cases, adoption patterns, and emerging practices.

- GitHub issues and discussions
- community forums
- Reddit
- social posts
- independent experiments

Community evidence should not be used as the sole basis for an important factual claim when primary evidence exists.

---

# Resource Types We Intentionally Collect

The research corpus should include more than papers and documentation.

Each part of the book should actively collect relevant:

- **Documentation** — specifications, APIs, model/platform docs
- **Papers** — foundational and current research
- **Articles** — engineering posts, analyses, postmortems
- **Repositories** — real implementations the reader can inspect
- **Books** — durable conceptual foundations
- **Videos / Talks** — architecture explanations and demonstrations
- **People** — researchers, builders, engineers, and thinkers worth following
- **Channels** — YouTube channels, newsletters, blogs, podcasts, communities
- **Case studies** — systems running in production
- **Datasets / Benchmarks** — where claims can be tested
- **Tools / Products** — concrete examples of a concept in practice

People and channels are not cited as authorities merely because they are popular. They are included because following good practitioners helps readers continue learning after the book becomes dated.

---

# Every Chapter Gets an Evidence Layer

Each chapter should maintain a source set before it is considered `DRAFT-READY`.

Recommended minimum for a normal technical chapter:

- 2+ primary sources
- 1+ real implementation, repository, or specification when applicable
- 1+ practitioner or production source when applicable
- 1+ durable conceptual resource for major engineering ideas
- additional learning resources where they genuinely help

The exact number is less important than coverage. Some foundational chapters may require many sources; some project chapters may rely primarily on experiments and official documentation.

---

# Chapter Resource Sections

Every finished chapter should end with a curated section such as:

## Evidence & Resources

### Primary Sources
The sources that substantiate the chapter's important factual claims.

### See It in Practice
Repositories, case studies, systems, tools, or demonstrations that implement the concepts.

### Watch
Videos, talks, lectures, interviews, or demonstrations worth the reader's time.

### Read Deeper
Books, papers, articles, and long-form material for deeper understanding.

### People & Channels to Follow
A small curated set of people, engineering blogs, channels, newsletters, or communities that regularly produce useful work on the topic.

This section should be curated, not a link dump. Every item should include one sentence explaining why it is worth the reader's attention.

---

# Sources Must Be Bound to Claims

Resources should not merely accumulate in a giant bibliography.

During outlining, important claims should be associated with the evidence supporting them.

Example:

```text
CLAIM
Subagents can reduce context interference by isolating task-specific information.

EVIDENCE
- Source A: architecture/documentation describing isolated subagent contexts
- Source B: practitioner implementation
- Chapter experiment: compare single-context vs isolated-context execution

STATUS
SUPPORTED
```

Possible claim states:

- `UNSOURCED`
- `SOURCE-FOUND`
- `SUPPORTED`
- `CONFLICTING-EVIDENCE`
- `NEEDS-EXPERIMENT`
- `TIME-SENSITIVE`

---

# Demonstration Is Also Evidence

Because this is a project-driven book, many claims should be tested directly.

Instead of only saying:

> Parallel agents reduce completion time.

The chapter should run the same workload sequentially and in parallel and report:

```text
Sequential execution
Time: ...
Cost: ...
Quality: ...
Conflicts: ...

Parallel execution
Time: ...
Cost: ...
Quality: ...
Conflicts: ...
```

This lets the book distinguish between:

- what documentation promises
- what experts recommend
- what the chapter actually observed

---

# Time-Sensitive Claims

AI tooling changes quickly. Any statement about current:

- model capabilities
- model prices
- context windows
- API behavior
- product features
- framework support
- security controls
- benchmarks
- vendor limits

must be treated as time-sensitive.

For these claims:

1. Prefer first-party sources.
2. Record the date checked.
3. Avoid wording that implies permanence.
4. Separate the durable principle from the current implementation.

Example:

```text
Durable principle:
Models differ in capability, latency, and cost, so routing can improve system economics.

Current implementation example:
Provider/model pricing and capabilities as verified on YYYY-MM-DD.
```

The book should age around examples, not around principles.

---

# Contradictory Sources

When credible sources disagree, do not quietly select the convenient one.

Record:

- what each source claims
- source date
- source authority
- whether the difference is version-specific
- what the chapter's own experiment shows
- what remains uncertain

Disagreement is useful information.

---

# Research Repository Structure

As research grows, use a structure like:

```text
research/
├── SOURCE-STANDARDS.md
├── people.md
├── channels.md
├── books.md
├── videos.md
├── repositories.md
├── papers.md
├── case-studies.md
└── chapters/
    ├── ch-01/
    │   ├── sources.md
    │   ├── claims.md
    │   └── notes.md
    ├── ch-02/
    └── ...
```

The global files are discovery indexes. The chapter folders contain the evidence actually being used.

---

# Evidence Gate for Drafting

A chapter should not move to `DRAFT-READY` until:

- its core argument is clear
- major factual claims have evidence
- time-sensitive claims have current sources
- contradictory evidence has been recorded
- the chapter project has an evaluation plan
- the most useful further-learning resources have been curated
- remaining evidence gaps are explicitly marked

This extends the Bookwright outline gate: the chapter must be structurally ready **and evidence-ready** before prose drafting begins.
