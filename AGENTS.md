# AGENTS.md

This repository is the entry point for designing, creating, auditing, and maintaining other AI-agent repositories.

Detailed guidance lives under `docs/`. Read only the files relevant to the current task.

## Purpose

Agent Factory manages the methodology used by child agents.

- Agent Factory owns reusable agent-design principles, patterns, templates, audits, and vendor research.
- Each child agent owns its domain-specific knowledge and project state.
- Do not move domain-specific rules into Agent Factory unless they are proven reusable across multiple agents.

## Core priorities

Use this order of priority:

1. Correctness and safety.
2. Clear instruction hierarchy.
3. Small always-on context.
4. Separation of global, task-specific, and project-specific instructions.
5. Vendor-neutral structure where practical.
6. Verifiable workflows and acceptance criteria.
7. Maintainability over cleverness.
8. Reuse proven patterns instead of copying temporary fixes.

## Context discipline

Do not turn `AGENTS.md` into an encyclopedia.

- Keep repository-wide instructions concise.
- Put detailed guidance in `docs/`.
- Read detailed files only when the current task needs them.
- Avoid duplicated instructions across files.
- If two instructions conflict, resolve the conflict instead of adding another rule.

## Rule promotion

Do not promote a one-off correction directly into a global rule.

Use this progression:

1. Project-specific issue or correction.
2. Repeated failure pattern.
3. Reusable pattern.
4. Global principle only when broadly justified.

A child agent may keep temporary or domain-specific instructions that never belong in Agent Factory.

## Vendor guidance

When researching OpenAI, Anthropic, GitHub, or another vendor:

- Prefer current official primary sources.
- Record the source, date checked, and practical implication under `docs/vendors/` or `research/`.
- Separate durable design principles from vendor-specific features.
- Do not copy a vendor feature into every child agent merely because it exists.
- Treat vendor guidance as evidence for design decisions, not as a substitute for design judgment.

## Creating a new agent

Before creating a child agent:

1. Define its purpose and boundaries.
2. Check whether an existing agent already covers the same role.
3. Decide what must always be loaded and what should be loaded only on demand.
4. Start with the smallest viable structure.
5. Create clear acceptance criteria.
6. Register the agent in `registry/agents.yaml`.
7. Perform an initial audit after the first real task.

Use `templates/project-agent/` as the default starting point unless another template clearly fits better.

## Auditing an existing agent

Review:

- purpose and scope
- instruction hierarchy
- AGENTS.md size and role
- duplicated or conflicting rules
- task-specific rules that should be moved out of always-on context
- stale vendor-specific assumptions
- project-state leakage into global rules
- missing acceptance criteria
- opportunities for deterministic checks or scripts

Do not rewrite an agent merely to match a newer style if the current structure is working well.

## Repository areas

- `docs/principles/`: durable, vendor-neutral principles
- `docs/vendors/`: current vendor-specific findings
- `docs/patterns/`: reusable implementation patterns
- `docs/audit/`: audit and migration guidance
- `templates/`: starting structures for new agents
- `registry/`: inventory of managed agents
- `research/`: dated research notes and methodology changes

## Change discipline

When changing methodology:

1. Explain what problem the change solves.
2. Identify whether it is global or vendor-specific.
3. Update the smallest appropriate file.
4. Consider which registered agents are affected.
5. Avoid mass-updating child agents without evidence that the change benefits them.

The factory should become more useful over time without becoming progressively harder for an agent to understand.
