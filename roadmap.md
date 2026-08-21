# ATLAS + Shared Memory Roadmap

Status: proposed checkpoint roadmap for Bookwright manifesto approval.  
Created: 2026-08-21

This is not the final table of contents. It is the first practical capability
path for the book: the reader first creates **ATLAS**, the book-aware companion
agent, then uses ATLAS to build the **shared memory system**.

The roadmap keeps the book honest:

```text
one checkpoint
  -> one capability
  -> one real build
  -> one limitation exposed
  -> one system upgrade
```

---

# The Arc

The reader starts as someone who can use ChatGPT.

By the end of the first-edition build path, the reader should have:

- ATLAS configured as a useful local agent companion
- a local project workspace
- a source-grounded personal memory system
- basic retrieval and context rules
- provenance and citation habits
- a simple evaluation loop
- a path from solo memory to small-team shared knowledge
- early permissions, review, and governance boundaries

The shared memory system remains the product. ATLAS is the companion that helps
the human build, inspect, and govern it.

---

# Checkpoints

| # | Checkpoint | ATLAS Gains | Shared Memory System Gains | What Breaks | Next Unlock |
|---|---|---|---|---|---|
| 1 | Leave Cloud Chat | A local agent environment and a reason to exist beyond conversation | Nothing yet; the workspace is born | Cloud chat cannot see files, run tools, or preserve project state reliably | Local project workspace |
| 2 | Become ATLAS | The `soul.md` persona, reader contract, chapter loop, and safety posture | A named guide that understands the mission | A generic assistant treats the book as passive reading | First project folder |
| 3 | Create The Workspace | Project folders, operating notes, and a shared place to work | A home for notes, sources, outputs, and decisions | Unstructured files become messy quickly | Knowledge capture |
| 4 | Capture First Knowledge | Instructions for saving notes, links, docs, and chapter outputs | First source-backed memory entries | Saved text is not the same as usable context | Source-grounded answers |
| 5 | Answer With Evidence | A habit of citing files, passages, and uncertainty | Answers grounded in known sources instead of vibes | ATLAS can still overclaim or cite weak context | Context selection |
| 6 | Choose Context | Rules for selecting relevant files instead of dumping everything | Basic context engineering and retrieval discipline | Wrong or excessive context produces drift, cost, and confusion | Memory structure |
| 7 | Structure Memory | A simple schema for source, kind, tags, status, owner, and project | Searchable, filterable knowledge entries | Tags and folders do not solve trust or truth | History and lifecycle |
| 8 | Add Memory Lifecycle | Rules for draft, canonical, outdated, deprecated, and superseded knowledge | Knowledge can change without erasing history | Old beliefs and new beliefs conflict | Evaluation |
| 9 | Evaluate Recall | Simple tests for answer quality, missing sources, hallucination, and usefulness | A repeatable way to measure whether memory got better | One good answer does not prove the system works | Tool and API access |
| 10 | Give ATLAS Tools | Scoped file, CLI, API, or MCP access with explicit authority boundaries | The system becomes buildable and inspectable through tools | Capability can exceed permission or safety | Sharing and identity |
| 11 | Add Team Boundaries | Awareness of users, owners, private vs shared knowledge, and review points | Solo memory starts becoming multiplayer memory | Team memory can leak private context or blur ownership | Governance |
| 12 | Govern The System | Proposal flows, audit notes, permissions, and human oversight habits | A small-team knowledgebase that can be trusted, reviewed, and improved | More autonomy creates more risk | Advanced autonomy and operations |

---

# First-Edition Interpretation

The first edition does not need to build every production feature in full depth.
It should build enough that the reader understands the system and owns a working
local version.

Required by the end:

- ATLAS can guide the reader through the book.
- ATLAS can work inside a local project folder.
- The shared memory system can capture and retrieve knowledge.
- Answers can point back to sources.
- The reader can inspect what context was used.
- The system has a small evaluation loop.
- The design has an explicit path toward team use.
- Permissions and provenance appear before autonomy expands.

Deferred or optional for later chapters/advanced tracks:

- production-grade auth
- full multi-tenant deployment
- enterprise compliance
- complex graph algorithms
- deep infrastructure setup
- model training or fine-tuning
- autonomous background operations without review

---

# Chapter 1 Position

Chapter 1 should cover Checkpoints 1-3 lightly and begin Checkpoint 4.

The reader should finish Chapter 1 with:

- a local/free agent path chosen or understood
- ATLAS created from the short system prompt or `soul.md`
- a project workspace
- one source or note saved
- one grounded answer attempted
- one failure inspected

The next limitation should be clear:

ATLAS can help, but it does not yet know how to choose the right context
reliably.
