# The 10 Core Principles of Building With AI

These principles are the lens for the entire book. They come before the technical chapters and should remain visible as the reader moves from models and prompts to agents, harnesses, production systems, and AI-native organizations.

The goal is not to memorize terminology. The goal is to develop a durable way of thinking about intelligent systems even as models, frameworks, products, and vendors change.

---

## 1. Intelligence Is a Component. The System Is the Product.

A powerful model is not a production AI system.

The useful system is the combination of intelligence, specification, context, data, tools, runtime, permissions, evaluation, observability, human oversight, governance, and economics.

```text
Model ≠ Agent
Agent ≠ Product

Production AI System =
Intelligence
+ Context
+ Actions
+ Runtime
+ Trust
+ Operations
+ Humans
```

**Builder mindset:** Never evaluate an AI product only by how impressive the model response looks. Inspect the complete system around it.

---

## 2. Specify the Outcome Before You Optimize the Intelligence.

An agent cannot reliably succeed when nobody has defined success.

Before prompting, orchestration, or autonomy, establish:

- the goal
- constraints
- knowns and unknowns
- assumptions
- acceptance criteria
- risk boundaries
- stopping conditions
- evaluation criteria

**Builder mindset:** If `done` cannot be described, it cannot be reliably delegated or evaluated.

---

## 3. Context Is a System, Not a Giant Prompt.

The model does not need everything. It needs the right information at the right moment.

Context should be selected, prioritized, compressed, scoped, refreshed, and progressively disclosed according to the task.

```text
More context ≠ better context

Useful context =
Relevant
+ Timely
+ Authoritative
+ Sufficient
```

**Builder mindset:** Treat context engineering as information architecture for intelligence.

---

## 4. Give Agents Capabilities Deliberately and Authority Conservatively.

Tools determine what an agent *can* do. Permissions determine what it is *allowed* to do.

These are separate design decisions.

```text
Capability without authority control = risk
Authority without capability = useless
```

Agents should receive the minimum capability and authority required for the current responsibility, with escalation when the boundary is reached.

**Builder mindset:** Every new tool increases capability and potential blast radius at the same time.

---

## 5. Autonomy Must Be Earned.

Autonomy is not a boolean feature. It is a progression based on evidence.

```text
Suggest
  ↓
Draft
  ↓
Act with approval
  ↓
Act within boundaries
  ↓
Operate autonomously
```

Higher autonomy should require stronger evaluation, observability, reversibility, permission controls, and proven reliability.

**Builder mindset:** Do not start by asking, “How autonomous can this agent be?” Ask, “What evidence would justify the next level of autonomy?”

---

## 6. Prefer Evidence Over Eloquence.

A confident answer is not evidence of correctness.

Important claims and actions should be grounded in sources, tool results, tests, measurements, or reproducible observations.

The system should distinguish:

```text
I know
I observed
I infer
I assume
I do not know
I need to verify
```

**Builder mindset:** Build systems that can show why something should be believed, not merely systems that sound convincing.

---

## 7. Evals Are the Feedback Loop of AI Engineering.

You cannot improve an intelligent system consistently if improvement is subjective.

Evals turn agent engineering into an engineering discipline by allowing changes to prompts, context, models, tools, skills, routing, memory, and harnesses to be compared against a stable definition of success.

```text
Build
 ↓
Run
 ↓
Evaluate
 ↓
Diagnose
 ↓
Improve
 ↓
Run again
```

**Builder mindset:** Never call a system “better” without deciding what better means and measuring it.

---

## 8. Design for Failure, Recovery, and Reversibility.

Models will be wrong. Tools will fail. APIs will change. Context will become stale. Agents will misunderstand tasks. Dependencies will disappear.

Production systems assume failure and provide ways to:

- detect it
- contain it
- retry safely
- recover state
- roll back actions
- degrade gracefully
- escalate to a human
- learn from the incident

**Builder mindset:** A successful demo proves the happy path. Engineering begins with the unhappy paths.

---

## 9. Use the Simplest System That Can Reliably Produce the Outcome.

Not every problem needs an agent. Fewer still need multiple agents.

The normal decision ladder should be:

```text
Rule
 ↓
Script
 ↓
Workflow
 ↓
LLM call
 ↓
Agent
 ↓
Multi-agent system
```

Move upward only when the simpler level cannot handle the uncertainty, reasoning, flexibility, or environment required by the problem.

**Builder mindset:** Complexity must earn its place in the architecture.

---

## 10. Optimize for the Real-World Outcome, Not the Agent Run.

The ultimate metric is not token count, benchmark score, number of agents, or technical sophistication.

The question is whether the system produces useful outcomes at acceptable cost and risk.

```text
Business Value =
Useful outcomes
- Total operating cost
- Human review burden
- Failure cost
- Adoption friction
- Risk
```

Measure things such as:

- cycle time reduced
- human capacity released
- errors prevented
- throughput increased
- revenue created
- cost removed
- adoption achieved

**Builder mindset:** The purpose of an AI system is not to demonstrate AI. It is to improve an outcome worth improving.

---

# The Reader's Lens

Throughout the book, every new concept should be examined through these questions:

1. **What outcome are we trying to produce?**
2. **What information does the intelligence actually need?**
3. **What capabilities does it need, and what authority should it receive?**
4. **What evidence tells us the result is correct?**
5. **How can this fail, and how do we recover?**
6. **How much autonomy has the system earned?**
7. **Can a simpler architecture achieve the same result?**
8. **Can we observe and explain what happened?**
9. **What is the full cost and risk of operating it?**
10. **Does the system create measurable value for the people or organization using it?**

These questions should recur throughout the chapters. They are intended to become instinctive — the AI-systems equivalent of engineering principles that experienced developers use to reason about software before choosing an implementation.
