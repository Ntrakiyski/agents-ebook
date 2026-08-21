# Shared Living Memory Reference Analysis

Analyzed: 2026-08-21  
Source repository: `https://github.com/Ntrakiyski/shared-living-memory`  
Source commit inspected: `b9dffaf` (`docs: add interactive architecture map`)

Naming update, 2026-08-21: this analysis was written before the author decided
that **ATLAS is the book-aware companion agent**, not the final memory product.
When this file says "ATLAS" as a product destination, interpret it as **the
shared memory system that ATLAS helps the reader build**.

This file records what the ebook project should learn from Shared Living Memory.
It is a reference analysis, not a decision to make the book vendor-specific.

## Role in the Ebook

Shared Living Memory is the clearest concrete ancestor for the shared memory
system.

Reader-facing decision: the book may explicitly say that the shared memory
system is inspired by Shared Living Memory, link to
`https://github.com/Ntrakiyski/shared-living-memory`, and use it as a reference
point that readers can inspect or use directly.

The shared memory system should be taught as a fresh build from first
principles, but its end state should rhyme with Shared Living Memory:

```text
Solo second brain
  -> durable memory
  -> evidence-backed recall
  -> versioned knowledge
  -> graph-linked context
  -> multi-user ownership
  -> private/public visibility
  -> governed agent access
  -> proposal/audit workflows
  -> small-team shared intelligence
```

The book should not become a line-by-line clone of Shared Living Memory.
Instead, Shared Living Memory gives the project a real destination: a
solo-to-team AI knowledgebase where humans and agents can share, retrieve,
correct, govern, and act on knowledge without losing ownership, privacy,
evidence, or history.

Final build target: a reader who builds along through the whole book should end
with the same kind of product as Shared Living Memory, or at least roughly 80% of
its core capability in the teaching implementation.

## Core Product Insight

The strongest framing from the project is:

> The real product is translation between different mental maps.

The system is not just searchable notes. It is a governed knowledge layer that
lets one person's, team's, or agent's context become useful to another person,
team, or agent without pretending everyone shares the same vocabulary, purpose,
or risk boundary.

For the ebook, this gives the shared memory system a deeper promise:

- The human gains a higher-level map of the system.
- The agent gains durable operating knowledge.
- The team gains a shared layer that survives handoffs.
- Knowledge remains inspectable, attributable, and governable.

## Current Implementation Example

Treat these as current implementation examples, not permanent architectural
rules:

- Runtime: Cloudflare Workers
- Durable store: Cloudflare D1
- Retrieval index: Cloudflare Vectorize
- AI layer: Workers AI for embeddings and grounded answer generation
- Protocols: REST API, dashboard, and MCP
- Language: TypeScript
- Tests: Vitest
- Operations: health/readiness endpoints, scheduled canaries, runbooks, pilot
  scorecards

Durable principle:

```text
The authoritative memory store and the retrieval index are different layers.
The durable store must preserve truth, history, ownership, and provenance.
The vector index may accelerate recall, but it must be rebuildable.
```

## Capability Arc for the Shared Memory System

This is the likely shared-memory feature arc to adapt during TOC/outline work.

1. **Capture** — save useful knowledge from chat, notes, docs, links, files, and
   work sessions.
2. **Structure** — classify entries by source, tags, kind, status, importance,
   and project.
3. **Search** — retrieve with keyword search, embeddings, hybrid ranking, and
   useful result formatting.
4. **Evidence** — attach sources, passages, citations, authorship, and confidence.
5. **History** — preserve episodes, snapshots, versions, and what was believed
   at a past time.
6. **Memory Lifecycle** — distinguish draft, canonical, outdated, deprecated,
   superseded, retracted, and forgotten knowledge.
7. **Graph** — link related entries with explicit or inferred relationships such
   as supports, contradicts, derives_from, clarifies, and has_limitation.
8. **Personal Recall** — answer one user's questions from their own authorized
   memory with citations and uncertainty.
9. **Identity** — introduce users, personal keys, service identities, and
   ownership.
10. **Visibility** — support private and public/team knowledge with filtering
    before retrieval or LLM synthesis.
11. **Team Recall** — let a user retrieve their own private knowledge plus team
    public knowledge.
12. **Awareness** — surface overlap, contradictions, stale assumptions, and
    relevant teammate knowledge.
13. **Integrations** — capture from tools where work already happens: dashboard,
    REST, CLI, browser/mobile capture, docs, and MCP clients.
14. **Governed Agents** — give agents scoped access through MCP/API tools rather
    than direct database access.
15. **Proposals and Review** — route consequential, uncertain, cross-user, or
    public changes through human-reviewable proposal flows.
16. **Operations and Evals** — measure recall quality, zero-result rate,
    helpfulness, latency, privacy incidents, recovery, and onboarding success.
17. **Autonomous Operations** — add scheduled scouts, digest agents, contradiction
    monitors, and maintenance agents only after the earlier layers earn trust.

## Product Principles to Preserve

These principles are useful candidates for shared-memory checkpoints and chapter
callbacks:

- Memory is not a dump; it is a governed knowledge layer.
- Tags can be an organizing layer, but privacy and ownership must be enforced by
  the system, not trusted to client behavior.
- Private knowledge should not leak into vector recall, graph traversal, export,
  chat grounding, or agent tools.
- Public team knowledge should preserve authorship and source context.
- A current answer should not erase history.
- Contradicted or deprecated knowledge should usually be invalidated, not
  silently deleted.
- Citation-backed recall is different from search results.
- The system should show uncertainty and conflicting evidence.
- Agents should operate through scoped tools, proposal inboxes, and audit
  boundaries.
- Hard deletion is for compliance or explicit erasure, not ordinary correction.
- Operational logs should avoid becoming a second copy of private content.
- Autonomy expands only after privacy, recall quality, evidence, recovery, and
  review loops are working.

## Strong Teaching Moves From the Reference Project

The project naturally teaches many ebook concepts by exposing a limitation and
adding one system layer:

- Chat history does not survive across tools -> build capture.
- Saved notes are not usable context -> build recall.
- Search without evidence is hard to trust -> add citations/passages.
- Updated knowledge can erase the past -> add episodes/snapshots/history.
- One user's memory does not equal team knowledge -> add identity/ownership.
- Team memory creates privacy risk -> add visibility enforcement.
- Shared knowledge creates conflicts -> add contradiction and proposal flows.
- Agents need memory but should not own the database -> add MCP and service
  identities.
- Agent autonomy creates risk -> add scopes, approval, audit, and evals.
- A growing team needs confidence, not anecdotes -> add scorecards and metrics.

## Fit With the Existing Book Architecture

Shared Living Memory should become the concrete shared-memory destination while
the existing 15-dimension blueprint remains the systems map.

Do not collapse the book into a memory-app tutorial. The memory product is the
through-line that lets the book teach:

- models and prompts;
- context and RAG;
- tools, APIs, CLI, and MCP;
- agents and harnesses;
- runtime and state;
- evals and reliability;
- security, identity, permissions, provenance, and governance;
- human oversight and collaboration;
- operations, economics, versioning, and portability.

The book's final reader should be able to look at the shared memory system and
recognize the same kind of product logic as Shared Living Memory, while
understanding each layer well enough to adapt it to another domain.

## Settled Reader-Facing Position

- The book can mention Shared Living Memory as the inspiration for the shared
  memory system.
- The book can link to the Shared Living Memory GitHub repository.
- The book can use Shared Living Memory as a destination/reference point.
- The shared memory system should still be taught from first principles so the
  book remains useful even if the reference implementation changes.
- The target for readers building along is not a superficial demo; it is a
  substantial solo-to-team knowledgebase that reaches roughly 80% of the
  reference project's core capability.

## Open Questions for the Author

- Should the final shared-memory implementation use the same broad stack as
  Shared Living Memory, or should the ebook use a simpler local-first/reference
  stack for approachability?
- Which features are required for the first edition, and which belong in
  advanced/optional chapters?
