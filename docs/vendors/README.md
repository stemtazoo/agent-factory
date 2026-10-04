# Vendor Guidance

This directory stores vendor-specific findings that may influence Agent Factory design.

## Rules

- Prefer official primary sources.
- Record when guidance was checked.
- Distinguish product capability from durable design principle.
- Do not require every child agent to implement every vendor feature.
- Promote broadly useful lessons into `docs/principles/` only after evaluating whether they are vendor-neutral.

## Vendors

Primary instruction / coding-agent references:

- OpenAI
- Anthropic
- GitHub

Supplementary architecture references:

- [Google](google.md) — lifecycle, evaluation, observability, modular skills
- [Microsoft](microsoft.md) — agent-vs-code decisions, delegation, responsibility boundaries

Google and Microsoft are intentionally supplementary at this stage. Their strongest value for Agent Factory is architectural rather than repository instruction-file conventions.
