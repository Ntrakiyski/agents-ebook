# Conceptual Frameworks

This file preserves the recurring mental models that should appear throughout the book. `BOOK-BLUEPRINT.md` contains the chapter architecture; this file contains the visual and conceptual maps that help the reader understand how the pieces fit together.

---

# 1. The Capability Ladder

The reader should repeatedly see the system grow from a model call into an autonomous system.

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

The important teaching idea is that each layer solves a limitation exposed by the layer before it.

---

# 2. The Seven Planes of an AI System

The 15 dimensions in `BOOK-BLUEPRINT.md` can be compressed into seven planes. This is useful as a high-level diagram near the beginning of the book and as a diagnostic framework later.

```text
┌──────────────────────────────────────────────────────────┐
│                     INTENT PLANE                         │
│ Goals · Specs · Constraints · Success · Uncertainty      │
├──────────────────────────────────────────────────────────┤
│                  INTELLIGENCE PLANE                      │
│ Models · Reasoning · Context · Knowledge · Memory        │
├──────────────────────────────────────────────────────────┤
│                     ACTION PLANE                         │
│ Tools · Skills · MCP · Agents · Workflows · Orchestration│
├──────────────────────────────────────────────────────────┤
│                    RUNTIME PLANE                         │
│ Sandboxes · Compute · State · Time · Durable Execution   │
├──────────────────────────────────────────────────────────┤
│                     TRUST PLANE                          │
│ Identity · Security · Evidence · Evals · Permissions     │
├──────────────────────────────────────────────────────────┤
│                   OPERATIONS PLANE                       │
│ Observability · Cost · Reliability · CI/CD · Evolution   │
├──────────────────────────────────────────────────────────┤
│                     HUMAN PLANE                          │
│ UX · Oversight · Organization · Adoption · Governance    │
└──────────────────────────────────────────────────────────┘

                    BUSINESS VALUE
          Why does this system deserve to exist?
```

The 15 dimensions are the detailed curriculum. The seven planes are the reader's systems map.

---

# 3. The AI-System Iceberg

The visible agent is only a small part of a production system.

```text
                    VISIBLE
             ┌────────────────┐
             │ Model / Agent  │
             │ Prompt / Tools │
             └────────────────┘
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
                  BELOW THE SURFACE

Data
Integrations
Identity
Permissions
Runtime
State
Evals
Security
Observability
Human oversight
Governance
Infrastructure
Cost
Failure recovery
Organization
```

This should recur as the book progresses. Early chapters expose only a few underwater layers; later chapters reveal the full system.

Core lesson:

> Building the agent is not the same as building the system that makes the agent trustworthy and useful.

---

# 4. The Definition Keeps Expanding

The reader's definition of "building with AI" should change throughout the book.

```text
AI =
Prompt + Model
```

then:

```text
AI System =
Model
+ Prompt
+ Context
+ Knowledge
```

then:

```text
Agent =
Model
+ Context
+ Memory
+ Tools
+ Loop
```

then:

```text
Production Agent =
Agent
+ Harness
+ Runtime
+ Evals
+ Security
+ Observability
+ Human Oversight
```

then:

```text
Autonomous System =
Production Agents
+ Workflows
+ Orchestration
+ Learning
+ Governance
```

and finally:

```text
AI-Native Organization =
Humans
+ Agents
+ Data
+ Tools
+ Processes
+ Infrastructure
+ Trust
+ Governance
+ Economics
+ Continuous Learning
```

The narrative arc begins with **"How do I talk to a model?"** and ends with **"How do I design and operate an intelligent organization?"**

---

# 5. Capability Is Not Authority

This distinction should appear repeatedly.

```text
Capability = what the system can technically do.
Authority  = what the system is permitted to do.
```

A tool can give an agent the capability to send an email. Policy may permit the agent only to draft it. A GitHub integration can technically merge a pull request while organizational policy restricts the agent to opening a PR.

This distinction connects tools, permissions, identity, human oversight, governance, and autonomy.

---

# 6. Context, Knowledge, and Memory Are Different

```text
Knowledge
What exists somewhere and may be available to the system.

Context
What the model can see for the current inference/task.

Memory
What the system intentionally preserves across interactions or runs.
```

RAG is primarily a context-selection mechanism. A database is not automatically memory. Chat history is not automatically useful memory. More context is not automatically better context.

---

# 7. The Agent Loop

The primitive underlying increasingly sophisticated agents is simple:

```text
Observe
   ↓
Reason
   ↓
Decide
   ↓
Act
   ↓
Observe
   ↓
Repeat / Stop / Escalate
```

Harnesses, tools, memory, planning, hooks, permissions, evals, and orchestration constrain and improve this loop.

---

# 8. The Learning Loop

The book should distinguish memory from system improvement.

```text
Run
 ↓
Observe
 ↓
Evaluate
 ↓
Classify failure / success
 ↓
Decide where the lesson belongs
 ↓
Prompt / Skill / Retrieval / Code / Eval / Memory / Policy
 ↓
Re-evaluate
```

Not every correction belongs in memory. Some lessons belong in code, tests, prompts, skills, retrieval, documentation, datasets, or policy.

---

# 9. The Autonomy Ladder

```text
Suggest
  ↓
Draft
  ↓
Act with approval
  ↓
Act autonomously inside explicit boundaries
  ↓
Operate end-to-end with supervision and escalation
```

Autonomy is earned through evidence, not enabled because the model appears capable.

---

# 10. Products Are Examples, Not the Curriculum

The book must not be organized around temporary products or vendors.

Do not structure the book as:

```text
Claude
Codex
Cursor
OpenCode
MCP product X
```

Teach the durable primitive first:

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

Then show how current systems such as coding agents, model providers, MCP implementations, workflow engines, and agent platforms implement the primitive.

The book should age around its examples, not around its principles.
