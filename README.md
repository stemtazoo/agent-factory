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
