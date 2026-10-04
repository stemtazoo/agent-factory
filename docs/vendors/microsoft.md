# Microsoft

Checked: 2026-10-04

## Why Microsoft is useful here

Microsoft's current guidance is especially useful for deciding **when an agent is appropriate**, **what should remain deterministic code**, and **how to define responsibility and delegation boundaries**.

## Useful official sources

- Microsoft AI Decision Framework:
  https://microsoft.github.io/Microsoft-AI-Decision-Framework/
- Capability model:
  https://microsoft.github.io/Microsoft-AI-Decision-Framework/docs/capability-model.html
- Decision framework:
  https://microsoft.github.io/Microsoft-AI-Decision-Framework/docs/decision-framework.html
- Microsoft Learn — Cloud Adoption Framework for AI agents:
  https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ai-agents/

## Relevant ideas

### 1. Do not use an agent when ordinary code is better

Microsoft explicitly distinguishes work that benefits from reasoning and ambiguity handling from work with a known correct answer.

A useful Agent Factory rule of thumb is:

- use agents for reasoning, planning, intent interpretation, ambiguity, and flexible orchestration
- use deterministic code for validation, routing, transformation, calculations, schema checks, and other predictable operations

This reduces latency, cost, and difficult-to-debug nondeterminism.

### 2. Define the agent's authority before adding capabilities

Microsoft guidance emphasizes deciding what an agent may recommend, draft, act on, or own.

For Agent Factory, each child agent should define:

- purpose
- boundaries
- non-goals
- allowed actions
- approval requirements
- what requires human review

### 3. Keep responsibilities narrow

Multi-agent designs work better when specialist responsibilities are explicit.

Agent Factory should not create subagents merely to appear sophisticated. Add a specialist agent only when the responsibility is separable and the coordination cost is justified.

## Candidate principles

These are candidates for future promotion into shared principles after practical validation:

- Before building an agent, ask whether deterministic code or simple retrieval is sufficient.
- Explicitly define delegation and approval boundaries.
- Prefer hybrid architectures where deterministic code performs measurable operations and agents perform reasoning-heavy operations.
- Treat every additional agent as an architectural cost that needs justification.

## Do not generalize blindly

Azure, Copilot Studio, Microsoft Agent Framework, and other Microsoft-specific implementation choices should remain optional unless a child project actually depends on them.
