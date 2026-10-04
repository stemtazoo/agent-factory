# agent-factory

Agent Factory is a repository for designing, creating, auditing, and maintaining reusable AI-agent repositories.

The factory owns the **methodology** for building agents. Each child agent owns its **domain knowledge**.

## Goals

- Keep agent instructions small, clear, and maintainable.
- Separate global rules from task-specific and project-specific instructions.
- Prefer vendor-neutral design where possible.
- Track current official guidance from OpenAI, Anthropic, GitHub, and other relevant vendors.
- Convert repeated lessons into reusable patterns only after they prove broadly useful.
- Audit existing agents when the shared methodology changes.

## Core idea

```text
Official guidance
      ↓
research/
      ↓
Agent Factory principles and patterns
      ↓
templates/
      ↓
individual agent repositories
```

Individual agent repositories should not copy every vendor-specific recommendation directly. Agent Factory first evaluates whether a recommendation is broadly useful, vendor-specific, temporary, or unnecessary.

## Repository structure

```text
agent-factory/
├── AGENTS.md
├── README.md
├── docs/
│   ├── principles/
│   ├── vendors/
│   ├── patterns/
│   └── audit/
├── templates/
├── registry/
└── research/
```

## First child project

The first practical test for this factory will be a vehicle papercraft agent. It will be used to validate whether the factory can create a small, understandable, maintainable agent repository without accumulating one giant prompt.

## Design rule

**Keep always-on instructions small. Load detailed guidance only when it is relevant to the current task.**

See [AGENTS.md](AGENTS.md) for the operating rules used by AI agents working in this repository.

## Primary references

Agent Factory should prefer current official primary sources when reviewing agent architecture, instruction files, skills, custom agents, and related workflows.

### OpenAI

- [Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)
- [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra)

### Anthropic

- [Claude Code memory and instruction files](https://code.claude.com/docs/en/memory)
- [Claude Code documentation](https://code.claude.com/docs/en/overview)

### GitHub

- [Support for different types of custom instructions](https://docs.github.com/en/copilot/reference/custom-instructions-support)
- [Copilot customization cheat sheet](https://docs.github.com/en/copilot/reference/customization-cheat-sheet)
- [Adding repository custom instructions for GitHub Copilot](https://docs.github.com/en/copilot/how-tos/copilot-in-your-ide/customize-copilot/configure-custom-instructions/add-repository-instructions-in-your-ide)

These references are starting points, not frozen specifications. When guidance changes, record the review date and practical impact under `research/` and `docs/vendors/` before promoting any change into shared principles.
