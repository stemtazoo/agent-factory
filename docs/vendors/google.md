# Google

Checked: 2026-10-04

## Why Google is useful here

Google's current agent tooling is most useful to Agent Factory for **lifecycle design**, **evaluation**, and **observability** rather than for repository instruction-file conventions.

## Useful official sources

- Agents CLI getting started:
  https://google.github.io/agents-cli/guide/getting-started/
- Agents CLI development guide:
  https://google.github.io/agents-cli/guide/development/
- Agents CLI skills reference:
  https://google.github.io/agents-cli/reference/skills/
- Agent Development Kit documentation:
  https://google.github.io/adk-docs/

## Relevant ideas

### 1. Treat agent development as a lifecycle

Google's Agents CLI organizes work around a lifecycle such as:

- scaffold
- build
- evaluate
- deploy
- publish
- observe

For Agent Factory, the durable lesson is not the specific CLI. The useful idea is that **evaluation and observability belong in the development process, not only after deployment**.

### 2. Keep task knowledge modular

Agents CLI distributes guidance through multiple task-oriented skills, including workflow, scaffolding, evaluation, deployment, and observability.

This supports the Agent Factory principle of keeping always-on context small and loading detailed guidance only when the task needs it.

### 3. Add deterministic checks around agent behavior

Google's development workflow combines agent work with linting, tests, eval datasets, and grading.

Agent Factory should prefer deterministic validation where possible and use model-based evaluation where deterministic checks are insufficient.

## Candidate principles

These are candidates for future promotion into shared principles after practical validation:

- Define an explicit evaluation step for every serious child agent.
- Add observability when an agent becomes operational or autonomous enough that failures cannot be understood from final output alone.
- Keep evaluation, deployment, and observability guidance modular rather than embedding all of it in `AGENTS.md`.

## Do not generalize blindly

Google-specific infrastructure such as ADK, Cloud Run, Agent Engine, and Agents CLI should not become default requirements for child agents unless the project actually uses that stack.
