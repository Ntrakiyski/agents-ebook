# Building With AI
## From Prompts to Autonomous Systems

**Core promise:** By the end, the reader understands not only how to use models, but how to design, build, evaluate, secure, operate, evolve, and economically justify complete AI systems.

The reader builds one evolving system throughout the book — working name **ATLAS**. Early ATLAS is one model call. Final ATLAS is a production-grade, multi-agent, self-improving engineering system.

---

# The 15 Dimensions of the Book

| Dimension | Main part |
|---|---|
| 1. Intelligence | Part I |
| 2. Intent & Specification | Part II |
| 3. Context & Knowledge | Part III |
| 4. Execution & Agency | Part IV |
| 5. Runtime & Infrastructure | Part IV |
| 6. Reliability & Failure | Part VII |
| 7. Security, Identity & Trust | Part VIII |
| 8. Product & Human Interaction | Part IX |
| 9. Workflow & Business Process | Part VI |
| 10. Learning & Adaptation | Part X |
| 11. Operations & Observability | Part XI |
| 12. Economics & Value | Part XII |
| 13. Organization & Adoption | Part XIII |
| 14. Governance, Law & Accountability | Part XIV |
| 15. Evolution, Versioning & Portability | Part XV |

Part V, **Agentic Software Engineering**, deliberately cuts across several dimensions and shows how they combine in practice.

Part XVI is the final integration.

---

# Every Chapter Follows the Same Contract

Every chapter should contain:

1. **Problem** — why this concept exists.
2. **Mental model** — the simplest correct explanation.
3. **Build** — implement the capability.
4. **Break It** — deliberately expose its limitations.
5. **Under the Hood** — inspect prompts, context, tools, state, tokens, cost, etc.
6. **Production Lens** — security, reliability, data, human oversight, economics.
7. **Evaluate** — prove whether the change improved the system.
8. **ATLAS Upgrade** — permanently add the capability to the growing system.

The reader never reads 25 pages about RAG and then gets an exercise. **The RAG system itself is the chapter.**

---

# Part I — Intelligence

The reader begins at the absolute bottom: intelligence without agents, tools, memory, or frameworks.

## Chapter 1 — The New Computing Model

### Includes
- deterministic software vs probabilistic software
- what an LLM is
- model vs assistant vs agent vs workflow
- inference
- why AI software behaves differently
- the complete AI-system map

### Build
Make ATLAS's first raw model call from a tiny CLI.

```text
Human → Prompt → Model → Response
```

---

## Chapter 2 — Models and Capabilities

### Includes
- language models
- reasoning models
- coding models
- multimodal models
- model families
- capability differences
- intelligence vs knowledge
- hallucination
- nondeterminism
- temperature and sampling
- provider differences

### Build
Create a model comparison harness that sends the same task to several models and compares results.

---

## Chapter 3 — Tokens and Context Windows

### Includes
- tokenization
- input/output/reasoning tokens
- token budgets
- context windows
- context overflow
- lost-in-the-middle effects
- cost implications
- why more context is not automatically better

### Build
Create a token/cost inspector, then intentionally overflow a model's usable context.

---

## Chapter 4 — Prompting as Programming

### Includes
- system instructions
- user instructions
- roles
- goals
- constraints
- examples
- few-shot prompting
- output contracts
- instruction hierarchy
- prompt composition

### Build
Turn the generic ATLAS model into a structured project analyst.

---

## Chapter 5 — Structured Output and Reasoning

### Includes
- JSON Schema
- Pydantic/Zod-style schemas
- validators
- retries
- deterministic boundaries around probabilistic systems
- reasoning effort
- deep-thinking / “Ultra Think”-style modes
- reasoning cost
- when reasoning hurts instead of helps

### Build
Architecture Decision Agent returning typed alternatives, trade-offs, confidence, and recommendation.

---

## Chapter 6 — Model Routing and Prompt Caching

### Includes
- model routers
- task classification
- escalation
- fallback models
- cheap vs expensive models
- latency vs quality
- prompt caching
- static/dynamic context separation

### Build
Create an intelligent router and measure quality, tokens, latency, and cost before/after routing and caching.

### Checkpoint

```text
ATLAS
├── Models
├── Prompts
├── Schemas
├── Reasoning
├── Router
└── Cost awareness
```

---

# Part II — Intent & Specification

Before an agent acts, it needs to understand **what success actually means**.

## Chapter 7 — Intent Before Prompts

### Includes
- request vs intent
- task vs outcome
- explicit vs implicit goals
- constraints
- priorities
- conflicting goals

### Build
Intent Normalizer that turns a vague user request into a structured goal.

---

## Chapter 8 — Requirements, Assumptions and Ambiguity

### Includes
- knowns
- unknowns
- assumptions
- ambiguity
- clarification
- requirement extraction
- requirement conflicts
- confidence

### Build
Give ATLAS a vague product request and force it to produce a specification before implementation.

---

## Chapter 9 — Planning and Task Decomposition

### Includes
- goals
- plans
- tasks
- subtasks
- dependency graphs
- DAGs
- milestones
- replanning
- stopping criteria

### Build
Turn one requirement into an executable task graph.

---

## Chapter 10 — Acceptance Criteria and Architecture Decisions

### Includes
- Definition of Done
- measurable success
- acceptance tests
- architecture alternatives
- trade-offs
- ADRs
- constraints
- eval-first thinking

### Build
Create an executable specification containing requirements, plan, ADR, acceptance criteria, and evaluation strategy.

---

# Part III — Context & Knowledge

Now ATLAS learns how to know things it wasn't trained on.

## Chapter 11 — Making Data AI-Ready

### Includes
- ingestion
- parsing
- normalization
- duplicate removal
- metadata
- freshness
- provenance
- canonical sources
- conflicting information
- ownership
- document lifecycle

### Build
Turn a deliberately messy company document collection into an AI-ready corpus.

> RAG over bad data gives sophisticated access to bad data.

---

## Chapter 12 — Search, Embeddings and Retrieval

### Includes
- keyword search
- BM25
- embeddings
- semantic similarity
- vector databases
- metadata filtering
- hybrid search
- reranking

### Build
Search the same dataset using keyword, vector and hybrid retrieval and compare results.

---

## Chapter 13 — RAG

### Includes
- chunking
- indexing
- retrieval
- reranking
- grounding
- context assembly
- citations
- RAG failure modes
- retrieval evaluation

### Build
**Hybrid Search RAG Over Internal Documents.**

```text
Question
   ↓
 ┌───────────────┐
 │ Keyword Search│
 │ Vector Search │
 │ Metadata      │
 └───────┬───────┘
         ↓
      Rerank
         ↓
      Context
         ↓
       Model
```

---

## Chapter 14 — Context Engineering

### Includes
- context selection
- context prioritization
- compression
- context budgets
- context pollution
- dynamic context
- task-specific context compilation

### Build
Context Compiler that decides what information the model should see for each task.

---

## Chapter 15 — Project Context and Progressive Disclosure

### Includes
- repository instructions
- project-scoped context
- hierarchical documentation
- `AGENTS.md`
- `CLAUDE.md`
- README architecture
- rule scoping
- progressive disclosure
- just-in-time context

### Build

```text
project/
├── AGENTS.md
├── architecture/
├── product/
├── decisions/
├── systems/
└── skills/
```

ATLAS navigates information instead of loading everything.

---

## Chapter 16 — Memory

### Includes
- conversation history vs memory
- working memory
- episodic memory
- semantic memory
- procedural memory
- user memory
- project memory
- retrieval from memory
- retention
- forgetting

### Build
Give ATLAS persistent project memory.

### Checkpoint

```text
ATLAS
├── Intelligence
├── Intent
├── Search
├── RAG
├── Context Compiler
├── Project Knowledge
└── Memory
```

---

# Part IV — Execution, Agency & Runtime

We now give intelligence hands.

## Chapter 17 — Tool Calling

### Includes
- function calling
- schemas
- tool selection
- tool observations
- tool errors
- retries
- deterministic tool boundaries

### Build

```text
read_file()
search_code()
write_file()
run_command()
```

---

## Chapter 18 — APIs, API Keys, OAuth and CLI

### Includes
- REST
- SDKs
- APIs
- API keys
- OAuth
- tokens
- environment variables
- service accounts
- scopes
- command-line tools
- why CLIs are excellent agent interfaces

### Build
Give ATLAS GitHub API + `git`, `gh`, `rg`, `jq`, and shell capabilities.

---

## Chapter 19 — MCP Servers

### Includes
- MCP clients
- MCP servers
- tools
- resources
- prompts
- transports
- authentication
- local vs remote MCP
- capability discovery

### Build
Build an MCP server from scratch.

---

## Chapter 20 — Skills and Slash Commands

### Includes
- tools vs skills
- procedural knowledge
- reusable instructions
- scripts
- references
- examples
- skill discovery
- slash commands as workflow entrypoints

### Build

```text
skills/
└── review-pr/
    ├── SKILL.md
    ├── scripts/
    ├── examples/
    └── references/

/plan
/research
/build
/review
```

---

## Chapter 21 — The Agent Loop

### Includes
- observe
- reason
- decide
- act
- observe again
- termination
- replanning
- runaway loops

### Build
Implement an agent loop **without an agent framework**.

---

## Chapter 22 — Harness Engineering

One of the central chapters of the book.

### Includes
- model access
- context
- memory
- tools
- permissions
- state
- routing
- retries
- lifecycle
- evaluation
- recovery

### Build
The first complete ATLAS harness.

```text
             HARNESS
                │
   ┌────────────┼─────────────┐
 Context      Models         Tools
   │            │             │
 Memory       Router      Permissions
   └────────────┼─────────────┘
                ↓
             Agent
```

---

## Chapter 23 — Hooks, State and Checkpoints

### Includes
- lifecycle hooks
- before/after tool
- before/after edit
- validation hooks
- state
- checkpoints
- resumability
- idempotency

### Build
Kill ATLAS halfway through work and successfully resume it.

---

## Chapter 24 — Runtimes, Sandboxes, Headless and Background Agents

### Includes
- local runtime
- remote runtime
- containers
- VMs
- filesystem isolation
- network isolation
- persistent vs ephemeral runtime
- workers
- headless execution
- scheduled agents
- background agents
- event-driven execution
- time and deadlines

### Build
Run ATLAS autonomously inside a sandbox and wake it when an event occurs.

---

# Part V — Agentic Software Engineering

Now the book starts looking like modern Codex/Claude Code/OpenCode-style engineering.

## Chapter 25 — Git as Agent Infrastructure and Worktrees

### Includes
- Git as audit trail
- reversibility
- branches
- commits
- diffs
- merge boundaries
- worktrees
- isolated agent environments

### Build
Three independent agents working in three Git worktrees.

---

## Chapter 26 — Subagents and Context Isolation

### Includes
- specialist agents
- delegation
- isolated context
- task boundaries
- typed handoffs
- context pollution prevention

### Build

```text
ATLAS
├── Researcher
├── Backend Builder
├── Frontend Builder
└── Reviewer
```

> Subagents aren't simply “more AI.” They are also a context-management primitive.

---

## Chapter 27 — Parallel Agents and Orchestrator–Workers

### Includes
- parallel execution
- task partitioning
- dependencies
- fan-out/fan-in
- workers
- orchestration
- typed agent communication contracts
- scheduling

### Build

```text
             Orchestrator
           /      |       \
       Worker   Worker   Worker
           \      |       /
             Synthesis
```

---

## Chapter 28 — Agents Managing Agents, Arbitration and Multi-Repo Orchestration

### Includes
- manager agents
- reviewer agents
- judges
- disagreement
- arbitration
- confidence
- evidence
- shared state
- multi-repository changes
- agent communication protocols

### Build
One feature that requires coordinated changes across:

```text
frontend/
backend/
sdk/
infrastructure/
docs/
```

---

# Part VI — Workflow & Business Process

The reader now learns that an agent is not the same thing as a workflow.

## Chapter 29 — Script vs Workflow vs LLM vs Agent

### Includes
- deterministic automation
- probabilistic automation
- when to use each
- workflows surrounding agents
- agents inside workflows

### Build
Implement the same business requirement four different ways and compare them.

---

## Chapter 30 — State Machines, Events, Queues and Time

### Includes
- states
- transitions
- events
- queues
- waiting
- deadlines
- schedules
- retries
- delayed execution
- temporal workflows

### Build
Long-running ticket-resolution process that may wait days for external events.

---

## Chapter 31 — Handoffs, Approvals, SLAs and Compensation

### Includes
- human handoffs
- agent-to-agent handoffs
- approvals
- escalation
- SLA
- compensating actions
- rollback
- exception paths

### Build
Business process that automatically handles normal cases and escalates exceptions.

---

## Chapter 32 — Enterprise Integration Architecture

### Includes
- multiple SaaS systems
- APIs
- MCP
- OAuth
- identities
- rate limiting
- token expiry
- unavailable dependencies
- malformed responses
- connector architecture

### Build
ATLAS connected to three systems with different permission models and intentional integration failures.

---

# Part VII — Reliability & Failure

Now the question changes from **Can it work?** to **Can we prove it works repeatedly?**

## Chapter 33 — Evaluations

### Includes
- evals vs tests
- deterministic tests
- behavioral evaluation
- golden datasets
- regression suites
- task-completion evals
- retrieval evals
- tool-use evals

### Build
The first 100-task ATLAS benchmark.

---

## Chapter 34 — Eval Datasets, LLM Judges and Uncertainty

### Includes
- production traces → eval cases
- clustering failures
- representative samples
- LLM-as-judge
- judge bias
- calibration
- confidence
- known vs inferred vs assumed vs unknown

### Build
Automated Eval Dataset Generator + reviewer agent.

---

## Chapter 35 — Eval-Driven Loops and Self-Healing Tests

### Includes
- build → evaluate → diagnose → improve
- regression prevention
- implementation failure vs test failure
- agent repair
- agents gaming evals

### Build
Break twenty tests and let ATLAS diagnose, repair and prove the repairs.

---

## Chapter 36 — Failure Engineering, Simulation and Agent Run CI/CD

### Includes
- failure domains
- blast radius
- fallbacks
- retries
- graceful degradation
- circuit breakers
- chaos testing
- simulations
- red teaming
- CI/CD for prompts, skills, models and agents

### Build
A fake company environment containing email, database, customers and tasks. ATLAS must survive deliberately injected failures before deployment.

---

# Part VIII — Security, Identity & Trust

## Chapter 37 — Identity and Delegated Authority

### Includes
- who is acting?
- user identity
- service identity
- authentication
- authorization
- delegation
- impersonation
- scopes
- authority chains
- audit identity

### Build

```text
Human
 ↓ delegates
Manager Agent
 ↓ delegates
Worker Agent
 ↓
External System
```

with explicit authority at every level.

---

## Chapter 38 — Permissions, Secrets and Privacy

### Includes
- least privilege
- API secrets
- credential isolation
- PII
- data boundaries
- network permissions
- read/write/delete boundaries
- kill switches

### Build
Capability policy:

```yaml
github:
  read: true
  create_branch: true
  merge: false

production:
  read: false
  write: false
```

---

## Chapter 39 — Prompt Injection and Tool Poisoning

### Includes
- untrusted data vs instructions
- indirect prompt injection
- poisoned documents
- malicious websites
- malicious MCP servers
- poisoned tool descriptions
- data exfiltration
- dependency risks

### Build
Attack your own RAG/MCP agent and then defend it.

---

## Chapter 40 — Provenance, Evidence and Trust

### Includes
- claim provenance
- citations
- source authority
- freshness
- conflicts
- versions
- confidence
- audit trails

### Build
Every important ATLAS claim becomes:

```text
Claim
Source
Version
Author
Freshness
Confidence
Conflicting evidence
```

---

# Part IX — Product & Human Interaction

The best architecture still fails if people cannot work with it.

## Chapter 41 — Agent UX Beyond Chat

### Includes
- chat
- CLI
- voice
- forms
- buttons
- generated UI
- artifacts
- notifications
- background work
- dashboards

### Build
Three interfaces for the same ATLAS capability.

---

## Chapter 42 — Human In, On, Over and Out of the Loop

### Includes
- human-in-the-loop
- human-on-the-loop
- human-over-the-loop
- autonomous operation
- approval boundaries

### Build
Deploy one email agent at four autonomy levels.

---

## Chapter 43 — Explainability, Control and Reversibility

### Includes
- previews
- diffs
- action plans
- undo
- confirmation
- sources
- decision summaries
- audit history
- reversible actions

### Build
ATLAS Action Preview:

```text
I plan to:

1. Modify X
2. Create Y
3. Send Z

Why:
...

Evidence:
...

Risk:
...

Approve?
```

---

## Chapter 44 — Trust-Calibrated Interaction

### Includes
- when to ask
- when to act
- when to escalate
- uncertainty communication
- confidence thresholds
- interruption cost
- notification fatigue
- graceful human handoff

### Build
Decision policy governing autonomous action vs clarification vs escalation.

---

# Part X — Learning & Adaptation

## Chapter 45 — Feedback as Data

### Includes
- acceptance
- rejection
- edits
- explicit feedback
- implicit feedback
- failure classification
- telemetry → learning signal

### Build
Capture every human correction and turn it into structured feedback.

---

## Chapter 46 — Memory Consolidation

### Includes
- raw events
- summarization
- deduplication
- contradiction resolution
- importance
- decay
- forgetting
- stale memory
- memory confidence

### Build
Nightly memory consolidation pipeline.

```text
1000 Events
    ↓
Observations
    ↓
Patterns
    ↓
Lessons
    ↓
Long-Term Memory
```

---

## Chapter 47 — Fine-Tuning and LoRA

### Includes
- when prompting is enough
- when RAG is enough
- when tuning helps
- datasets
- train/eval split
- fine-tuning
- LoRA
- adapters
- overfitting

### Build
LoRA fine-tuning pipeline for one narrow capability and benchmark it against the base model.

---

## Chapter 48 — Self-Improving Systems

### Includes
- prompt improvement
- skill improvement
- retrieval improvement
- routing improvement
- harness improvement
- self-modification vs self-improvement
- eval-gated changes

### Build
Allow ATLAS to propose modifications to itself, but accept changes only when objective evaluation improves.

```text
Old score       82%
New score       89%
Security        PASS
Cost            +2%
Latency         -9%

→ Accept
```

---

# Part XI — Operations & Observability

This is the underwater part of the iceberg: what production systems depend on below the visible model/agent layer.

## Chapter 49 — Agent Observability

### Includes
- traces
- prompts
- context
- model selection
- tool calls
- state
- retries
- tokens
- latency
- costs
- outputs

### Build
Agent Run Explorer.

---

## Chapter 50 — Reliability Operations and Incident Response

### Includes
- SLOs
- SLIs
- error budgets
- incidents
- runbooks
- circuit breakers
- degraded operation
- escalation
- emergency shutdown

### Build
Deliberately create an ATLAS production incident and diagnose it from traces.

---

## Chapter 51 — Latency, Concurrency and Semantic Caching

### Includes
- perceived latency
- streaming
- parallel execution
- batching
- semantic caching
- prompt caching
- cache invalidation
- incorrect cache hits

### Build
Optimize one workflow from slow and expensive to fast and economical.

---

## Chapter 52 — The Agent Control Room

### Includes
- fleet monitoring
- active runs
- agent health
- approvals
- security events
- cost
- latency
- failures
- model usage
- intervention

### Build
Operations dashboard for the entire ATLAS fleet.

---

# Part XII — Economics & Value

## Chapter 53 — The Full Cost of an AI Agent

### Includes

```text
Model cost
+ Tokens
+ Infrastructure
+ Data
+ Integrations
+ Evaluations
+ Security
+ Observability
+ Human review
+ Governance
+ Engineering
+ Failure cost
```

### Build
Complete ATLAS cost model.

---

## Chapter 54 — Unit Economics and Business Value

### Includes
- cost/request
- cost/run
- cost/successful run
- cost/business outcome
- human review cost
- time saved
- throughput
- revenue
- error prevention
- ROI
- payback period

### Build
Cost/value calculator for an actual agent deployment.

---

## Chapter 55 — When Not to Build an Agent

One of the most important chapters.

### Includes

```text
Rule
vs
Script
vs
Workflow
vs
LLM call
vs
Agent
vs
Multi-agent system
```

### Build
Architecture Decision Matrix that selects the simplest sufficient solution.

---

# Part XIII — Organization & Adoption

## Chapter 56 — Ownership and Operating Roles

### Includes
- agent owner
- data owner
- integration owner
- model owner
- security owner
- business owner
- escalation ownership

### Build
Operating responsibility map for ATLAS.

---

## Chapter 57 — Adoption and Change Management

### Includes
- why users reject agents
- trust calibration
- gradual rollout
- workflow friction
- training
- adoption metrics
- champion users
- progressive autonomy

### Build
30-day introduction plan for ATLAS inside an organization.

---

## Chapter 58 — Designing Human + Agent Organizations

### Includes
- human responsibilities
- agent responsibilities
- managers of agents
- teams of agents
- delegated work
- new operating procedures
- AI-native roles

### Build
Redesign one traditional team into a human-agent operating model.

---

# Part XIV — Governance, Law & Accountability

## Chapter 59 — Agent Governance

### Includes
- policy
- audit
- allowed actions
- prohibited actions
- required approval
- policy enforcement
- governance-as-code

### Build

```yaml
may:
  - read_docs
  - draft_email

requires_approval:
  - send_external_email
  - merge_pull_request

prohibited:
  - delete_production_data
```

---

## Chapter 60 — Privacy, IP, Data Rights and Law

### Includes
- privacy
- retention
- deletion
- data residency
- copyrights
- generated code
- licenses
- training rights
- regulated data
- third-party content

### Build
Rights and data-governance registry for every ATLAS information source and capability.

---

## Chapter 61 — Accountability and Autonomous Authority

### Includes
- who is responsible?
- agent decisions
- human accountability
- autonomy limits
- auditability
- escalation
- risk classification
- approval gates

### Build
ATLAS autonomy charter defining what it may decide at every risk level.

---

# Part XV — Evolution, Versioning & Portability

AI systems change far faster than ordinary applications.

## Chapter 62 — Version Everything

### Includes
Versioning of:
- model
- prompt
- instruction files
- skills
- MCP servers
- tools
- memory schema
- retrieval pipeline
- datasets
- eval suites
- agent configuration
- harness

### Build
One reproducible ATLAS release manifest.

---

## Chapter 63 — Model Upgrades and Regression Management

### Includes
- upgrade testing
- shadow runs
- canaries
- A/B evaluation
- rollback
- behavioral regressions
- cost regressions
- latency regressions

### Build
Upgrade ATLAS to another model and determine objectively whether deployment should happen.

---

## Chapter 64 — Portability and Continuous Modernization

### Includes
- provider independence
- abstraction boundaries
- vendor-specific advantages
- lock-in
- lowest-common-denominator traps
- model adapters
- replacing infrastructure
- deprecation
- architectural debt

### Build
Replace one major ATLAS provider without rewriting the system.

---

# Part XVI — The Complete AI System

Everything converges here.

## Chapter 65 — Build the Production ATLAS System

The reader now combines everything:

```text
                          HUMAN
                            │
                     Intent / Goal
                            │
                            ▼
                    SPECIFICATION
                            │
                            ▼
                     ORCHESTRATOR
                            │
        ┌───────────────────┼──────────────────┐
        ▼                   ▼                  ▼
    Researcher           Builder            Reviewer
        │                   │                  │
      RAG               Worktree             Evals
     Search               Skills             Tests
     Memory               Tools             Security
        │                   │                  │
        └───────────────────┼──────────────────┘
                            ▼
                       Integration
                            │
                           CI/CD
                            │
                         Deployment
                            │
                      Observability
                            │
                         Feedback
                            │
                  Memory Consolidation
                            │
                      Improvement
                            │
                            └──────────────→ Next Run
```

Surrounding the visible agent system are:

```text
DATA
INTEGRATIONS
IDENTITY
PERMISSIONS
SECURITY
EVALUATIONS
OBSERVABILITY
HUMAN OVERSIGHT
GOVERNANCE
ECONOMICS
ORGANIZATION
```

That is the **full production architecture**.

---

## Chapter 66 — Build It Again Without the Book

The final exam gives only the objective:

> Build an autonomous engineering system capable of receiving a requirement, understanding the repository, researching necessary information, planning the work, delegating implementation, evaluating results, repairing failures, creating a pull request, requesting human approval where required, and learning from the result.

The implementation must demonstrate:

```text
✓ Intent
✓ Specification
✓ Models
✓ Routing
✓ Context engineering
✓ RAG
✓ Memory
✓ Tools
✓ MCP
✓ Skills
✓ Harness
✓ Hooks
✓ Runtime
✓ Sandboxing
✓ Git worktrees
✓ Subagents
✓ Parallel agents
✓ Orchestration
✓ Multi-repo work
✓ Evals
✓ Self-healing
✓ CI/CD
✓ Security
✓ Identity
✓ Provenance
✓ Observability
✓ Human oversight
✓ Workflow
✓ Feedback
✓ Economics
✓ Governance
✓ Versioning
✓ Portability
```

And the reader must prove:

```text
It works.
It is reliable.
It is safe.
It is observable.
It is affordable.
It has business value.
We know who is responsible for it.
We know how to upgrade it.
```

---

# Narrative Arc of the Book

The reader's definition of **building with AI** keeps changing.

At the beginning:

```text
AI = Prompt + Model
```

Then:

```text
AI System =
Model
+ Prompt
+ Context
+ Knowledge
```

Then:

```text
Agent =
Model
+ Context
+ Memory
+ Tools
+ Loop
```

Then:

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

Then:

```text
Autonomous System =
Production Agents
+ Workflows
+ Orchestration
+ Learning
+ Governance
```

And finally:

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

The book starts with **“How do I talk to a model?”** and ends with **“How do I design and operate an intelligent organization?”**

The 15 dimensions prevent the reader from making the common mistake of thinking the model or agent is the whole system. The subject of the book is **engineering complete AI systems from first principles to production autonomy**.
